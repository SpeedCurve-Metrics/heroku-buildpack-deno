# Heroku Buildpack for Deno

This is the Heroku buildpack for Deno apps.

Web processes must bind to `$PORT`, and only the HTTP protocol is permitted for incoming connections.

The buildpack parse `Procfile` and download all dependencies at push time.The downloaded files are cached.

## Specify a Deno version

You can specify a particular Deno version by setting the `DENO_RELEASE_NAME` config variable. The value must be a [valid Deno release](https://github.com/denoland/deno/releases) e.g. `v1.38.3`.
```
## Customizing the build process

You can run arbitrary code during the build process by creating a file in the root of your project called `heroku_build.ts`.
