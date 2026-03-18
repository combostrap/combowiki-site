# How to develop the ComboStrap Website

## On Windows WSL, Linux or macOS

On your desktop:

* Clone and go to the root

```bash
git clone https://github.com/combostrap/combowiki-site
cd combowiki-site
```

* Create and start the container

```bash
task run
# or
docker run \
  --name combowiki-site \
  -d \
  -p 8082:80 \
  --user 1000:1000 \
  -e DOKU_DOCKER_ENV=dev \
  -e DOKU_DOCKER_ACL_POLICY='public' \
  -e DOKU_DOCKER_ADMIN_NAME='admin' \
  -e DOKU_DOCKER_ADMIN_PASSWORD='welcome' \
  -v $PWD:/var/www/html \
  ghcr.io/combostrap/dokuwiki:php8.3-latest
```

The ComboStrap site should be available at: http://localhost:8082

## Check Command

See the [Taskfile](../Taskfile.yml)

* broken: broken link
* frontmatter: frontmatter sync
