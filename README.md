# Redirects component theme

The _Redirects_ component theme for [Cecil](https://cecil.app) provides support of `_redirects` file generation.

After installation and without any configuration, this component theme generates a [`_redirects`](./layouts/_default/page.redirects.twig) file containing HTML redirections created by Cecil, in all languages (automatic or created manually with the [`redirect`](https://cecil.app/documentation/content/#redirect) front matter variable).

Services that support the [`_redirects`](https://specs.ipfs.tech/ipips/ipip-0002/) file:

- [Netlify](https://docs.netlify.com/manage/routing/redirects/redirect-options/)
- [statichost](https://www.statichost.eu/docs/routing/)
- [Cloudflare Pages](https://developers.cloudflare.com/pages/configuration/redirects/)

## Installation

```bash
composer require cecil/theme-redirects
```

> Or [download the latest archive](https://github.com/Cecilapp/theme-redirects/releases/latest/) and uncompress its content in `themes/redirects`.

## Usage

Add `redirects` in the `theme` section of your site configuration:

```yaml
theme:
  - redirects
```

### Add redirections

```yaml
server:
  redirects:
    - from: https://xxxxxx/*
      to: https://xxxxxx/:splat
      status: 301 # HTTP status code, optional (301 by default if `force` is set)
      force: true # redirect even if the file exists, optional
```

## License

_Redirects_ is a free software distributed under the terms of the MIT license.

© [Arnaud Ligny](https://arnaudligny.fr)
