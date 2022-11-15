---
title: "TIL: Building a simple site using Hugo"
date: 2022-11-14T13:55:09Z
categories: [development, learning]
tags: [hugo, content]
draft: false
---

![](/img/hugo.png)

Today I learned how to build a simple site using Hugo. 

For the initial setup, install hugo then create a new site. 

        brew install hugo
        hugo new site my-website

In the directory that has been created, initialise a git repo, and add the theme of your choice as a submodule. I chose this nice theme [`papermod`](https://github.com/adityatelange/hugo-PaperMod).
    
    git init
    git submodule add https://github.com/adityatelange/hugo-PaperMod themes/PaperMod

You can use `hugo new` to create a post:

    hugo new posts/today-i-learned.md


and populate the newly created markdown file with some content

    ---
    title: "TIL: Building a simple site using Hugo"
    date: 2022-11-14T13:55:09Z
    categories: [development, learning]
    tags: [hugo, content]
    draft: true
    ---

    Today I learned how to...

Then run the server locally (allowing drafts).

    hugo server -D

To build static pages to the `public` directory, simply run

    hugo