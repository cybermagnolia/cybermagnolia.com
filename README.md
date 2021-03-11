# README

[![Netlify Status](https://api.netlify.com/api/v1/badges/0b948f9f-1f4f-4ad6-adb3-5a6cf7b886bc/deploy-status)](https://app.netlify.com/sites/infallible-sinoussi-4e1719/deploys)

This is the main website of [CyberMagnolia](https://cybermagnolia.com/).

## Content :memo:

### Blog Posts

All posts are written in Markdown and live in the `content/blog/` directory. If you'd like to add a blog post, we've got some love for you:

* [Docs on adding blog posts](https://github.com/cybermagnolia/cybermagnolia.com/blob/main/docs/adding-posts.md)

Please shout out if you find the docs insufficient (either on CyberMagnolia Slack, or by creating an issue for this repo.)

### Other Pages

You will find the rest of pages in `content/` directory. You will find corresponding pages listed in the [Hugo config](https://github.com/cybermagnolia/cybermagnolia.com/blob/main/config.toml) in the `[Menu]` section.

## Running Locally And Development :computer:

Requires [Hugo v0.79.0 or newer](https://gohugo.io/getting-started/installing/). When creating PRs tag `@core-team` group for reviews. You'll need at least one approval to deploy.

### Theme

The website uses an [Hugo Future Imperfect Slim](https://github.com/pacollins/hugo-future-imperfect-slim) theme for Hugo. It's installed as a git submodule and lives in the `themes` directory. To initialize the module:

```sh
  git init submodules
```

### Hugo's Built-In Server

To see a live version of your site locally, use the following command:

```sh
  hugo server
```

Hugo will build your site and host a server locally. You can view this live at localhost:1313.

See more [docs on Hugo](https://gohugo.io/getting-started/usage/) if you'd like to learn more.

### Customization

Custom CSS can be found in `static/css`.

## Deployment

The website is deployed using Netlify. You can see the [config](https://github.com/cybermagnolia/cybermagnolia.com/blob/main/netlify.toml) for details. Currently only [Daria](https://github.com/dariagrudzien) has access to the Netlify project. Poke her if you have any questions about that.

## Contributing

If you're here because you'd like to contribute by adding a blog post or tinkering on the design - here's some serious dose of love for you:

![Hug](https://p.favim.com/orig/2018/12/16/friends-monica-rachel-Favim.com-6697610.png)
