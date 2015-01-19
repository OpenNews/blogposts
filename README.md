# How to write blog posts on opennews.org

Writing blog posts on OpenNews is easy but requires knowing a few things about file formats and how Jekyll deals with blog posts.

## Creating a file

Blog posts are written in Markdown and need to be stored in the `_Posts` folder. In order for Jekyll to know what to do with them, files most follow this naming convention: `YEAR-MONTH-DAY-FILE-NAME.md`. For an example from our actual blog, theres: `2014-10-22-announcing-2015-fellows.md`

Jekyll uses this file name to assign chronological order to the blog post, so it's important. The title itself doesn't matter a ton, but I find it's easier to just keep going with the hyphens. NO SPACES though--that won't work.

You have two options with which to create the file: 
* Create your blog post file in your local copy of the site, make sure you've run `jekyll serve` after doing so so that it renders out the HTML (this will render out not only the page itself, but also add your blog post to the various places on the site that list blog entries) and, once you've confirmed it's all good, push all changes up to master (see [publishing](#publishing) below). 
* In github, if you're in Mozilla/Master, you *could* navigate into the _posts folder, create a new file there, name it correctly and edit using the text editor built into github. In a pinch, that'll get the post written, however it won't actually get it into the site, as then someone will need to pull down master and run `jekyll serve`. However, there are probably some use-cases where this is useful.

## YAML front matter

Jekyll knows how to build your blog post via the YAML front matter that preceeds your entry. 

## Publishing
