# Python Notebook DevContainer Playground

This is a simple repository to experiment with devcontainers for Python Notebook

In this case, I want to start from scratch, without relying on features available via VSCode extension.

## Steps

- Create a repository
- Add folder `.devcontainer`
- Create `devcontainer.json` inside `.devcontainer`

  This file defines the container we will be using to developer an application: we do not need dotnet to be installed on the host machine.

## What's inside `devcontainer.json`?

In this case, I want to build a cusotm image, using an existing image as a base; in this case we need:

- A `Dockerfile` 
- `devcontainer.json`

In this case, we're not referencing an existing image in `devcontainer.json`: either `"image"` or `"build"` are used, but not both.

```json
{
  "name": "jupyter notebook",
  "build": {
    "dockerfile": "Dockerfile",
    "context": "."
  },
  "customizations": {
    "vscode": {
      "extensions": [
        "ms-toolsai.jupyter",
        "ms-python.python"
      ]
    }
  }
}
```

## References

**TODO**