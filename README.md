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
