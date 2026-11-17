# Writing a blog post

The blog is built by Jekyll, which GitHub Pages runs automatically on every push.
No build step and no backend.

## New post

1. Put images in `assets/img/blog/` (`.webp` keeps the page fast).
2. Create `_posts/YYYY-MM-DD-short-name.md`. The date in the filename is the post
   date; `short-name` becomes the URL: `squeakincgames.com/posts/short-name`.
3. Write it:

```markdown
---
title: "Designer Diary: Something New"
image: /assets/img/blog/cover.webp      # big image at the top (optional)
image_alt: Box art for Something New    # optional, defaults to the title
description: One sentence for link previews.   # optional
---
*"An opening quote." — Someone*

### A heading

A paragraph. **Bold**, *italic*, [a link](https://example.com).

![Image description](/assets/img/blog/photo.webp)

1. Numbered
2. List

- Bullet
- List

> A blockquote
```

4. Commit and push. The post appears at the top of `/blog`, gets its own page,
   and shows up in the sidebar and the RSS feed (`/feed.xml`) automatically.

Tips:
- Put titles with a colon in quotes (`title: "A: B"`).
- Leave a blank line between paragraphs.
- Raw HTML also works inside a post if Markdown can't do something.

## Preview locally (optional)

```bash
gem install --user-install jekyll:3.10.0 jekyll-feed kramdown-parser-gfm webrick
jekyll serve      # then open http://localhost:4000/blog
```
