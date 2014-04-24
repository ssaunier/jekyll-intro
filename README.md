This how-to will guide you on how to setup a jekyll blog from scratch,
hosted on [Github Pages](https://pages.github.com/).

## Gem installation

First, make sure you have jekyll installed with:

```bash
$ gem install jekyll
```

## Repo initialization

We will create a site served at `http://<your_github_username>.github.io` and hosted on Github at `<your_github_username>.github.io`. In the previous terms, just remplace `<your_github_username>` with your own GitHub username, obviously.

```bash
$ cd ~/code/<your_github_username>
$ jekyll new <your_github_username>.github.io
$ cd <your_github_username>.github.io
$ git init
$ git add .
$ git commit -m "Jekyll blog generated"
```

## Serve the blog locally

You can preview your blog articles locally. **Open a new terminal tab**, and run, in the root folder of your blog:

```bash
$ jekyll serve --watch
```

It will run forever, that's why we opened a new terminal tab. Then you can
your browser, and go to the following URL:

```bash
http://0.0.0.0:4000
```

Great, this is your new blog! Time to write a new article.

## Create a new article

Your articles live in the `_posts` folder of your jekyll project. To create a new article, you need to create a new file in this folder, with a filename **strictly following** the convention:

```bash
YYYY-MM-DD-the-blog-article.markdown
```

Where `YYYY-MM-DD` is the date of the date, and `the-blog-article` will be
the URL where the article will be served:

```bash
http://0.0.0.0:4000/the-blog-article.html
```

Open this file in Sublime Text, and make sure the 4 first lines follow the
following convention:

```markdown
---
layout: post
title: "The Blog Article"
---
```

Then you can save your file, go to your browser and refresh your blog
root page (listing all your articles). You should see a link to your
new article. Click on it, you should see a blank article. Time to add
some content with Sublime Text to `posts/YYYY-MM-DD-the-blog-article.markdown`!



