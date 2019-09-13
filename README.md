# pandoc docker image

This image can be used to run `pandoc` within a docker container.

One use case of [`pandoc`](https://github.com/jgm/pandoc) is to convert markdown to HTML or PDF:

```
    # build the image
    docker build -t pandoc_docker .

    # example (assuming existing file ./README.md)
    docker run --rm -it -v ${PWD}:/data normoes/pandoc -o README.pdf README.md

    docker run --rm -it -v ${PWD}:/data normoes/pandoc -o README.html README.md
```

## Engines

At the moment only `texlive` is installed.
