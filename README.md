# How to write blog posts on opennews.org

Writing blog posts on OpenNews is easy but requires knowing a few things about file formats and how Jekyll deals with blog posts.

## Creating a file

Blog posts need to be stored in the `_Posts` folder. In order for Jekyll to know what to do with them, files most follow this naming convention: `YEAR-MONTH-DAY-FILE-NAME.md`. For an example from our actual blog, theres: `2014-10-22-announcing-2015-fellows.md`

Jekyll uses this file name to assign chronological order to the blog post, so it's important. The title itself doesn't matter a ton, but I find it's easier to just keep going with the hyphens. NO SPACES though--that won't work.

You have two options with which to create the file: 
* Create your blog post file in your local copy of the site, make sure you've run `jekyll serve` after doing so so that it renders out the HTML (this will render out not only the page itself, but also add your blog post to the various places on the site that list blog entries) and, once you've confirmed it's all good, push all changes up to master (see [publishing](#publishing) below). 
* In github, if you're in Mozilla/Master, you *could* navigate into the _posts folder, create a new file there, name it correctly and edit using the text editor built into github. In a pinch, that'll get the post written, however it won't actually get it into the site, as then someone will need to pull down master and run `jekyll serve`. However, there are probably some use-cases where this is useful.

## YAML front matter

Jekyll knows how to build your blog post via the YAML front matter that preceeds your entry. Your YAML front matter should follow this pattern: 
```
---
layout: blogpost
title: 2015 Fellowship Onboarding is GO
date: 2015-1-12 9:00
author: Dan Sinker
tags: fellowship announcements
excerpt: The OpenNews team brings our 2015 Knight-Mozilla Fellows to Los Angeles to start the work of their fellowship years. We also welcome Kavya Sukumar as our seventh 2015 fellow, who will spend her fellowship year working with Vox Media. Yay fellows! Yay Los Angeles!
---
```

* **layout**: this needs to be 'blogpost'
* **title**: this can be anything, and will automatically become the title of your blog post both on the post page and in all listings of the blog (front page, blog page, etc)
* **date**: this needs to follow the pattern of: YEAR-MONTH-DAY HR:MIN and sets the timestamp that displays with the blog post and in lists
* **author**: your name.this is not yet hooked up to an auto-generating author block, but it will be eventually)
* **tags**: whatever (we haven't yet formalized a taxonomy, but should. otherwise, tags are separated by spaces)
* **excerpt**: This is an excerpt that will display with every list of blog posts. Make it relatively lengthy and grabby. If this is left off, the first paragraph of your post will automatically be put in its place in lists.

Also, note that this whole thing needs to be both preceeded and followed by three hyphens.

## Writing

Blog posts are written in [Markdown](https://daringfireball.net/projects/markdown/basics), and linked there is the basic markdown syntax. The [Jekyll documentation](http://jekyllrb.com/docs/posts/) also goes in to quite a bit of detail about writing posts and has some useful advice, especially for hightlighting code snippets. 

If you want to include images in your posts you have a a couple workable options:
* store your images inside the `/media/img/` and link accordingly.
* store your images on a third-party service like dropbox and link accordingly.

There's no real reason **not** to put images into `/media/img/` unless you really don't want to deal with `git add --all` and committing. But you're going to be doing that anyway, so really, nbd.

## Publishing

