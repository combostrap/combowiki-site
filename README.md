# ComboWiki Website

## About

This repository contains the [combowiki website](https://combowiki.combostrap.com)
written as [combo site](https://combowiki.combostrap.com/admin/combostrap-website-yfi22ewn)

## How to Run

To get the `ComboWiki` website available at http://localhost:8082, execute:

```bash
docker run \
  --name combowiki-site \
  --rm \
  -p 8082:80 \
  -e DOKU_DOCKER_GIT_SITE=https://github.com/combostrap/combowiki-site \
  ghcr.io/combostrap/dokuwiki:php8.3-latest
```
