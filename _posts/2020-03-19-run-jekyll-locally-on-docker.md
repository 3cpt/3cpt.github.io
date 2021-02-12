---
layout: post
title: run Jekyll with Github Pages locally in Docker
description: how to
---

Temporarily run Jekyll with Github Pages locally on Docker without install everything in your machine use:

```bash
docker run --name <container_name> \
    -ti --rm \
    -p 4000:4000 \
    -v /<path_to_your_jekyll_folder>/:/srv/jekyll jekyll/jekyll:pages \
    jekyll serve --watch --incremental
```

Don't forget to change the `<container_name>` with a name that matches for you and the `<path_to_jekyll_folder>` with the **full path**.
Why _temporarily_? Because with the `--rm` will remove the container when you stop it.
