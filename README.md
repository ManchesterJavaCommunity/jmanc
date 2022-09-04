As this site is hosted via a Github Pages sub-project you need to run it locally using the following command to ensure all links work as expected:

```
bundle exec jekyll serve --incremental --baseurl ''
```

## Docker

To check website locally using Docker comment the following line out of `_config.yml` so the images load:

```
baseurl: /
```

NOTE: this change shouldn't be committed.

Then execute the following commands from the root of the project:

```
$ export JEKYLL_VERSION=3.8
$ docker run --rm --volume="$PWD:/srv/jekyll" -p 3000:4000 -it jekyll/jekyll:$JEKYLL_VERSION jekyll serve --watch
```

Website will be available at http://localhost:3000
