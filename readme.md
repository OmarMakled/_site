## Get image

    docker pull jekyll/jekyll

## Initial

    mkdir myblog; cd myblog

    docker run --rm --volume="$PWD:/srv/jekyll" -it jekyll/jekyll jekyll new .

## Srever

    docker run --name myblog --volume="$PWD:/srv/jekyll" -p 3000:4000 -it jekyll/jekyll jekyll serve --force_polling --incremental

## Bash

    docker exec -it myblog /bin/bash
    jekyll build --watch
