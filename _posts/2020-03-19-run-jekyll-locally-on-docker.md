---
layout: post
title: run Jekyll with Github Pages locally in Docker
description: how to
---

If you need to run Jekyll with Github Pages locally on Docker without install all the Ruby stuff (on Windows is a mess).

```bash
docker run --name <container_name> -ti --rm -p 4000:4000 -v /<path_to_jekyll_folder>/:/srv/jekyll jekyll/jekyll:pages jekyll serve --watch --incremental
```

Don't forget to change the `<container_name>` with a name that matches for you and the `<path_to_jekyll_folder>` with the **full path**.
And why "temporarily"? Because with the `--rm` when you stop the container, it will be deleted automatically.
