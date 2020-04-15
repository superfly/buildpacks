# Buildpacks - Fly.io builders and Buildpacks

Note: for most languages, use the CNB buildpacks abd builders

Currently supporting - Deno

## Create deno buildpacks

pack package-buildpack flyio/deno-cnb --package-config ./package.toml --publish

Detects the present of a deno-app.ts file to trigger build.
(Deno is so lightweight it has no ancillary files that could act as a signatre so we mandate an app name)

## Create deno builder which includes deno-cnb buildpack

pack create-builder flyio/flyio-builder:cflinuxfs3 --builder-config ./builder.toml
