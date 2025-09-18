# Python Devcontainers Examples

This repository contains sample setup for python devcontainers:

- `development` contains a simple devcontainer setup, using Microsoft-based image 
- `notebook` extends the previous one, adding the ability to use notebook

  Additional packages are installed via `pip`, using `postCreateCommand`

- `custom-image` replicate the previous one, but using a custom image to install packages directly into the image instead of using `postCreateCommand`.