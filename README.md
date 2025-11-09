# Personal Website

[![GitHub](https://img.shields.io/github/license/JulianFrattini/JulianFrattini.github.io/LICENSE.md)](./LICENSE)

This repository contains the code for a personal website built with the [Jekyll framework](http://jekyllrb.com/) using the [Hyde theme](https://github.com/poole/hyde).

## Usage and Development

The [GitHub actions](.github/workflows/jekyll-docker.yml) are set up in a way that the content of this repository will be hosted via GitHub pages directly.

### Structure

This repository contains the following files.

```
├── _includes: abstract website elements
│   ├── head.html : header of each page
│   └── sidebar.html : DOM of the sidebar, including the site and platform links
├── _layouts: template html files
│   ├── default.html : detaul web page
│   ├── page.html : simple content web page
│   └── post.html : template for a blog post
├── posts : directory of blog entries
├── .devcontainer/devcontainer.json : configuration for a containerized developer environment
├── .github/workflows : directory containing GitHub actions
│   ├── docker-image-dev.yml : compilation of a Docker image with a working Jekyll environment
│   └── jekyll-docker.yml : parsing and hosting the Jekyll website via GitHub pages
├── public : public files to share via the website
│   ├── css : CSS style sheets
│   ├── docs : directory of downloadable documents
│   │   ├── dissertation-frattini-kappa.pdf : introductory chapter of the doctoral thesis
│   │   └── dissertation-frattini.pdf : doctoral thesis
│   ├── img : image files for the website
│   └── jf.ico : logo for the website
├── _config.yml : configuration of static variables
└── Dockerfile.dev : specification of a Docker container with a Ruby and Jekyll environment.
```

### Development

To run the website locally, you need a Ruby setup with Jekyll installed.
Alternatively, you can use the [Devcontainer](.devcontainer/devcontainer.json) setup.
This setup pulls a development environment with Ruby and Jekyll pre-installed.
The environment is specified in the [Dockerfile.dev](Dockerfile.dev) and automatically hosted at `ghcr.io/julianfrattini/julianfrattini.github.io-dev:latest` via the [docker-image-dev.yml action](.github/workflows/docker-image-dev.yml).

Once an appropriate environment is set up (e.g., by starting loading this project in its devcontainer environment), serve the website via the following command from the terminal: 

```
jekyll serve
```

The website will become available at localhost:4000.

### Configuration

The [README of the Hyde project](https://github.com/poole/hyde/blob/master/README.md) contains advise on how to customize the theme of the website.

## License

The general architecture of the website was derived from the [Hyde project](https://github.com/poole/hyde) by [Mark Otto](https://github.com/mdo), which is licensed under the [MIT license](./LICENSE.md).
All changes to the source code are also licensed under [MIT license](./LICENSE.md).
