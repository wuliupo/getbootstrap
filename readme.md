getbootstrap
============

static web page from http://getbootstrap.com

## Running documentation locally

Bootstrap's documentation, included in this repo in the root directory, is built with [Jekyll](http://jekyllrb.com) and publicly hosted on GitHub Pages at <http://getbootstrap.com>. The docs may also be run locally.

https://github.com/twbs/bootstrap/tree/v3.3.7

1. install bundle: `sudo gem install bundler`, `sudo gem install bundle`
1. If necessary, [install Jekyll](http://jekyllrb.com/docs/installation) and other Ruby dependencies with `bundle install`.
   **Note for Windows users:** Read [this unofficial guide](http://jekyll-windows.juthilo.com/) to get Jekyll up and running without problems.
1. From the root `/bootstrap` directory, run `bundle exec jekyll serve` in the command line.
1. Open `http://localhost:9001` in your browser, and voilà.
1. The document were generated under `_gh_pages` folder.

## Remove third-party assets (googleapis, google-analytics)
- docs/_includes/header.html
- jquery in docs/examples/*/index.html
  ```html
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
    <script>window.jQuery || document.write('<script src="../../assets/js/vendor/jquery.min.js"><\/script>')</script>
  ```

## Remove ga hard code
- `onclick="ga(` -> `onclick2="ga(`
- `"/apple-touch-icon.png"` -> `"../apple-touch-icon.png"`
- `"/favicon.ico"` -> `"../favicon.ico"`

## ads
- carbon ads