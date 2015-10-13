# Dokku App Version Plugin

Automatically adds the application version to container environment using the [git describe](http://www.git-scm.com/docs/git-describe) format.  This means that building releases you must tag the commit with a version tag, such as v0.0.1, v.0.0.2, and so forth.

The value will be injected into the container environment as the `APP_VER` variable.  You can then access this in your application to use however you see fit.

## Installation

`dokku plugin:install https://github.com/robinbolton/dokku-app-version.git`

## Usage

This plugin is automatically run whenever you deploy a new release via `git push`.

The `APP_VER` environmental variable will be injected into the container, which you can verify by running `dokku config:get <APP> APP_VER`.
