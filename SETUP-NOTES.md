# Jekyll conversion notes

This folder is a proposed Jekyll version of the starter site.

## Before publishing
1. Newsletter signup is currently disabled. When you are ready, uncomment the newsletter include in `_layouts/default.html` and configure `_includes/newsletter.html` with your Buttondown username.
2. Check the About page and homepage wording.
3. Add future posts as Markdown files in `_posts/` named `YYYY-MM-DD-short-title.md`.
4. Put YAML front matter at the top of every post, for example:

   ---
   layout: post
   title: "A new post"
   date: 2026-11-10
   ---

5. Test locally with Ruby/Bundler and `bundle exec jekyll serve`, or let GitHub Pages build the site after pushing.

## GitHub Pages
- Keep the `CNAME` file in the repository root.
- The site uses the `github-pages` gem. The `jekyll-feed` plugin and RSS link are commented out for now.
- The newsletter include is retained in `_includes/newsletter.html` but is disabled in `_layouts/default.html`.
- To enable RSS later, uncomment the plugin entry in `_config.yml`, uncomment the dependency in `Gemfile`, and uncomment the RSS link in `_layouts/default.html`; then run `bundle install`.
- To enable the newsletter later, uncomment the newsletter include in `_layouts/default.html` and replace `YOUR_BUTTONDOWN_USERNAME` in `_includes/newsletter.html`.

## URL note
The existing `/blog/test.html` address is retained as a simple redirect page. The Jekyll post itself uses `/blog/2026/11/04/test/`.
