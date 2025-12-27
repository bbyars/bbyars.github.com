# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is Brandon Byars's personal author website built with Jekyll 4.2 using the "Horace" theme. The site is deployed to brandon-byars.com.

## Build Commands

```bash
# Install dependencies
bundle install

# Serve locally with live reload (http://localhost:4000)
bundle exec jekyll serve

# Build for production (output to _site/)
bundle exec jekyll build
```

## Architecture

**Layouts** (`_layouts/`): Three-tier hierarchy
- `default.html` - Base template with head, header, footer
- `page.html` - Static pages (extends default)
- `post.html` - Blog posts with author box, sharing (extends default)

**Includes** (`_includes/`): Reusable components
- `postbox.html` - Post preview card
- `author.html` - Author bio section
- `image-caption.html` - Images with captions (supports `#wide`, `#left`, `#right` modifiers)

**Content**:
- Posts go in `_posts/` with format `YYYY-MM-DD-title.md`
- Posts use front matter: `layout`, `title`, `tags`, `featured_image`, `featured_image_thumbnail`
- Use `<!--more-->` to define excerpt break point

**Styling** (`_sass/`): Sass stylesheets compiled by Jekyll

## Configuration

Site settings in `_config.yml`:
- `production_url`: https://brandon-byars.com
- Pagination: 5 posts per page
- Plugins: jekyll-paginate, jekyll-seo-tag, jekyll-sitemap
