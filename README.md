Access the blog via https://josefgull.github.io/Blog/


## Test locally

One-time setup (macOS):

```sh
brew install ruby@3.4
echo 'export PATH="/opt/homebrew/opt/ruby@3.4/bin:$PATH"' >> ~/.zshrc
# open a new terminal, then in this folder:
bundle install
```

Start the local server:

```sh
cd ~/Documents/Blog
bundle exec jekyll serve
```

Open http://localhost:4000/Blog/ in the browser. Pages rebuild when you save a file;
after changing `_config.yml`, stop the server with `Ctrl+C` and start it again.
The theme is downloaded on every build, so you need internet access.

Note: Ruby 4 does not work yet with the `github-pages` gem, so use Ruby 3.4.

## Write a new post

Create a file in `_posts/` named `YYYY-MM-DD-title.md` that starts with:

```yaml
---
title: "My Post"
categories: [Bread]
---
```

Images go in `assets/images/` and are included with
`![Text]({{ site.baseurl }}/assets/images/my-picture.jpeg)`.
