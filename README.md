# STAC browser for birdhouse

> [!WARNING]
> This repo is for demo purposes only at the moment. No credentials have been added to push images to docker hub.

This repo simply contains a github workflow to build a docker image based on [STAC Browser](https://github.com/radiantearth/stac-browser).

This image is built with the `pathPrefix` variable set to `/stac-browser/` which is required when it is deployed behind
the [birdhouse-deploy](https://github.com/bird-house/birdhouse-deploy/)'s reverse proxy.

The built image can be found at https://hub.docker.com/repository/docker/marbleclimate/stac-browser

To update the version of [STAC Browser](https://github.com/radiantearth/stac-browser) that is included in the image, update
the `ref:` argument to the `actions/checkout@v4` step in `.github/workflows/deploy-image.yml`.

A new image will be built every time a new release is made to _this_ repository.
