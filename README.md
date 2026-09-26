## Developer Portfolio Landing Page Template

### AI Case Studies

The `/ai/` section uses its own layouts and `assets/css/ai.css`. The existing
Data Science portfolio keeps its Minimal theme and root URL.

To add a case study, create `ai/<project-slug>/index.md` using the Navigator
page's front matter as a reference. Set `layout: ai-case-study`,
`ai_case_study: true`, a unique numeric `display_order`, and an explicit
`permalink: /ai/<project-slug>/`. Provide `title`, `subtitle`, `card_subtitle`,
`summary`, `description`, and a `demonstrates` list. Set `featured: false`
unless the project should carry the featured label. The landing page discovers
these pages automatically and renders `_includes/ai-project-card.html`.

Place product screenshots in `assets/images/ai/<project-slug>/`, set `thumbnail`
to the site-root asset path, and supply meaningful `thumbnail_alt` text. Provide a real product screenshot and alt text for each published case study.

Case-study prose is limited to a 780px reading width; screenshots can use the
full page grid. Image metadata (`src`, `alt`, `width`, `height`, and `caption`)
feeds `_includes/ai-screenshot.html`. Images link to their full-size files.
The project footer accepts an optional `repository_url` for a public repository
and `demo_url` / `demo_label` when demo access expectations are clear.

The portfolio uses real application captures, cropped and compressed to WebP. No
application UI has been fabricated. Screenshot provenance and crop coordinates
are documented in `assets/images/ai/ai-opportunity-navigator/SOURCES.txt`.

Validate with the existing GitHub Pages/Jekyll environment when available.
Check `/`, `/ai/`, and direct access to each case-study URL; check internal
links and images, keyboard navigation, and desktop/mobile layouts. Keep local
build output and review screenshots outside the repository. No Node build step
or additional Jekyll plugin is required by this section.

### Introduction

Use this template if you need a quick developer / data science portfolio! Based on a Minimal Jekyll theme for GitHub Pages.

<img src="images/demo.gif?raw=true"/>

### Installation

See full step by step tutorial [on Medium](https://medium.com/@evanca/set-up-your-portfolio-website-in-less-than-10-minutes-with-github-pages-d0efa8ff56fd).
___

You can use the editor on GitHub to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Roadmap

See the [open issues](https://github.com/evanca/quick-portfolio/issues) for a list of proposed features (and known issues).
___

### References

[1] Jekyll theme "Minimal" for GitHub Pages: https://github.com/pages-themes/minimal (CC0 1.0 Universal License)
<br>[2] Dummy photo via: https://pixabay.com/photos/man-male-adult-person-caucasian-1209494/ (Pixabay License)
<br>[3] Dummy thumbnail image created by rawpixel.com: https://www.freepik.com/free-vector/set-elements-infographic_2807573.htm (Standard Freepik License)
