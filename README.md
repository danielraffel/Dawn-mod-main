<img width="1132" alt="Screenshot 2023-10-11 at 12 04 26 PM" src="https://github.com/danielraffel/Dawn-mod-main/assets/25807/d14a4b32-cf8f-4024-b508-c3fb990d7108">

# Dawn Mod Read Me
I made some very modest modifications to Dawn which can be seen on my [journal](https://danielraffel.me)
- enhanced index.hbs home page to an infinite scrolling feed (from casper)
- for each post the publish date and first tag appear above each item
- if there's a featured image it appears beneath publish date / tag and above title
- using excerpt text from ghost admin as the post content (if no custom content then it truncates)
- added a 'read more' link since may not always be obvious these are truncated stories
- adding ability to hover over each post content (image, content extract, read more) to hyperlink to the feature
- disabled some ghost upsell / subscriber details that were appearing and distracting
- created some mobile media tags in feed.css to render the content better on phones using post-card-image img
- I added photo-via-link CSS but disabled the feature in index.hbs that supports image source attribution to images that appear on the homepage (eg if you add a URL to the alt tag of a featured image in ghost editor and uncomment the text in index.hbs you will get a link in small text under the photo that says 'Photo via' which will link to the alt tag URL you added)
- I have added prism.js and their CSS to make it easy to embed code (with copy code plugin) using twilight and disabled the border
- in content.hbs added a #nofeature tag to prevent the feature image from appearing on article posts from https://hooshmand.net/ghost-blog-different-hero-image-feature-image/ since I also don't want these images appearing in emails i'm currently publishing, sending the email, then updating the post with the feature image and #nofeature tag (but i'll probably soon just remove the featured image from the email newsletter template just haven't gotten around to it)

**Note: The rest of this read me are the original "dawn" read me notes.**

# Dawn

A highly functional [Ghost](https://github.com/TryGhost/Ghost) theme that adapts to the reader's preferences. Let them read, search, subscribe, navigate, and more with ease.

**Demo: https://dawn.ghost.io**

# Instructions

1. [Download this theme](https://github.com/TryGhost/Dawn/archive/main.zip)
2. Log into Ghost, and go to the `Design` settings area to upload the zip file

# Development

Styles are compiled using Gulp/PostCSS to polyfill future CSS spec. You'll need [Node](https://nodejs.org/), [Yarn](https://yarnpkg.com/) and [Gulp](https://gulpjs.com) installed globally. After that, from the theme's root directory:

```bash
# Install
yarn

# Run build & watch for changes
yarn dev
```

Now you can edit `/assets/css/` files, which will be compiled to `/assets/built/` automatically.

The `zip` Gulp task packages the theme files into `dist/dawn.zip`, which you can then upload to your site.

```bash
yarn zip
```

# Contribution

This repo is synced automatically with [TryGhost/Themes](https://github.com/TryGhost/Themes) monorepo. If you're looking to contribute or raise an issue, head over to the main repository [TryGhost/Themes](https://github.com/TryGhost/Themes) where our official themes are developed.

# Copyright & License

Copyright (c) 2013-2023 Ghost Foundation - Released under the [MIT license](LICENSE).
