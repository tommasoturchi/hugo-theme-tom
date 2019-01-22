<h1>Call me Tom: a theme for Hugo</h1>

Tom is a Simple and Minimalist theme for Hugo, forked from the much more famous Sam. It lets you categorize and showcase your content the way you want to.

# Features:

- Showcase content
    - Content-focused page templates for list pages, single pages, and posts
    - A responsive CSS grid gallery page that renders from a folder of images
- Customize
    - Custom navigation menu set via `config.toml`
    - Custom footer text
- Developer-approved
    - Syntax highlighting
    - Share-ready metadata set via `config.toml` (OpenGraph and Twitter Cards integration)
    - Easy-to-navigate Sass files included
- *Interactive particles*


# Quick start

## 1. Get the theme

Run from the root of your Hugo site:
```sh
$ git clone https://github.com/tommasoturchi/hugo-theme-tom.git themes/tom
```

Alternatively you can include this repository as a [git submodule](https://git-scm.com/book/de/v1/Git-Tools-Submodule). This makes it easier to update this theme if you have your Hugo site in git as well. For this you need to run:

```sh
$ git submodule add https://github.com/vickylai/hugo-theme-tom.git themes/tom
```

## 2. Configure your site

From the [sam repository](https://github.com/vickylai/hugo-theme-sam), copy `config.toml` to the root folder of your Hugo site and change the fields as you like. There are helpful hints in the file.

## 3. Create pages

Run:
```sh
$ hugo new page.md
```
Where `page` can be anything you like. A contact page, a bio, dates for your upcoming world tour... Anything!

## 4. Design your main menu and index page

In `config.toml`, customize the entries for `[[params.mainMenu]]` however you like. You can have as many or as few entries as you like. You can even include external links.

This list comprises the index page and part of the navigation menu at the bottom of single content pages. Here's an example:

```
[[params.mainMenu]]
    link = "/photography"
    text = "photography"

[[params.mainMenu]]
    link = "/posts"
    text = "writing"

[[params.mainMenu]]
    link = "/about"
    text = "who dis?"
```

## Preview your site locally

Use Hugo's built-in server to see your site in action as you make changes.

```sh
$ hugo serve -t tom
```

Visit `localhost:1313` in your browser to see a live preview of your site.

## Posts

To create a new post, run:
```sh
$ hugo new posts/your-post-title.md
```

## Image gallery

To create an image gallery, place all the files you want included in a folder within `/content/gallery/`.

```
content/
 └── gallery/
    └── images/
    |   ├── file_1.jpg
    |   ├── file_2.jpg
    |   └── file_3.jpg
    └── _index.md
```

The gallery title is defined in the front matter of `_index.md`. You can also optionally define the page URL using `url`:

```
---
title: "Portraits"
type: "gallery"
url: "/portrait-gallery"
---
```

In order to create more than one gallery, create multiple folders in `content/` with this file structure and `type: "gallery"` defined in the `_index.md` front matter.

In `config.toml`, you can set `smallPreviewImages` to `true` in order to use small sized thumbnails. Include those thumbnail files in your gallery image folder.

The thumbnails need to have the same filenames as the larger images they represent.

That's it! Tom's gallery layout template will automagically build the page from your images.


# Editing the theme

All the theme's Sass files are included. You can compile these to CSS using the npm scripts included in `package.json`.

Prerequisites:
* Node.js and npm: https://www.npmjs.com/get-npm

To install all dependencies:

```sh
$ npm install
```

Available commands are:

* `npm run build:sass` compiles Sass files to compressed CSS
* `npm run autoprefixer` autoprefixes the compiled CSS
* `npm run build` does all the above
* `npm run watch` watches Sass files for changes and automatically recompiles and autoprefixes the CSS

# Contributing

Pull requests for bug fixes and enhancements are welcome.

__Thank you to:__ @vickylai!

# License
Licensed under [AGPL-3.0](https://github.com/tommasoturchi/hugo-theme-tom/blob/master/LICENSE)
