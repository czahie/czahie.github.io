## What's this
This is my personal website based on the [Indigo Jekyll Theme](https://github.com/sergiokopplin/indigo).

## What's new
I added support for multi-language. Now this website supports English and Chinese.

## Setup

0. :star: to the project. :metal:
1. Fork the project [czahie.github.io](https://github.com/czahie/czahie.github.io/fork)
2. Edit `_config.yml` with your data (check <a href="README.md#settings">settings</a> section)
3. Write some posts :bowtie:

If you want to test locally on your machine, do the following steps also:

1. Install [Jekyll](https://jekyllrb.com), [NodeJS](https://nodejs.org/) and [Bundler](https://bundler.io/).
2. Clone the forked repo on your machine
3. Enter the cloned folder via terminal and run `bundle install`
4. Then run `bundle exec jekyll serve --config _config.yml,_config-dev.yml`
5. Open it in your browser: `http://localhost:4000`
6. Do you want to use the [jekyll-admin](https://jekyll.github.io/jekyll-admin/) plugin to edit your posts? Go to the admin panel: `http://localhost:4000/admin`. The admin panel will not work on GitHub Pages, [only locally](https://github.com/jekyll/jekyll-admin/issues/341#issuecomment-292739469).

## Settings

You must fill some informations on `_config.yml` to customize your site.

```
name: John Doe
bio: 'A Man who travels the world eating noodles'
picture: 'assets/images/profile.jpg'
...

and lot of other options, like width, projects, pages, read-time, tags, related posts, animations, multiple-authors, etc.
```

---
## License

[MIT](https://kopplin.mit-license.org/) License © Sérgio Kopplin
