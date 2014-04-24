This how-to will guide you on how to setup a jekyll blog from scratch,
hosted on [Github Pages](https://pages.github.com/).

## Gem installation

You will need a fresh ruby installation. If you don't, follow
[lewagon/setup](https://github.com/lewagon/setup)

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

## Publish your blog on the Internet

You need to create a new GitHub repository. Go to [github.com/new](https://github.com/new), and create repository named `<your_github_username>.github.io`.
The name is very important. Once created, you will get instructions to add this
remote to your local git repository (the two command specified at the bottom).

To publish your article, it's just a push:

```bash
$ git push origin master
```

## Using your own domain

You will have to create a `CNAME` file. [Here is a great guide](https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages).

## Adding static pages

Suppose you want to have an "About" page or a "Resume" page. These are not really
blog articles. And you want to have a special URL:

### /about.html

Just create a file at the root of your jekyll project:

```bash
$ touch about.html
```

And then, inside this file, don't forget the head:

```markdown
---
layout: default
title: About me
---
```

Note that the layout in this case is `default`, not `post`. They are related
to what you can find in the `_layouts` folder!

### /about

You can drop the `.html` suffix in your URL, in that case you need a folder:

```bash
$ mkdir about
$ touch about/index.html
```

## Adding images

The Markdown syntax to add an image is:

```markdown
![Alt text](/path/to/img.jpg)
```

You should create an `images` folder to put your images in:

```bash
$ mkdir images
```

This way, if you have an image `me.jpg` in your `images` folder,
you can put it in your article with the following:

```markdown
![Me](/images/me.jpg)
```

## I want a contact form!

You can use **Wufoo** or **Brace forms**, I wrote [an article](http://sebastien.saunier.me/blog/2014/04/15/you-do-not-need-a-database-for-your-contact-form.html)
about it.

## I don't like the default look & feel!

Well, you can tweak the layout, or the CSS. You can also find some inspiration
on [jekyllthemes.org](http://jekyllthemes.org/)

## I want to put comments on my blog!

Use [Disqus](http://help.disqus.com/customer/portal/articles/472138-jekyll-installation-instructions)!