+++
title = "Semantic Release Container"
date = "2019-10-20"
author = "GuiAdCo"
description = "This repository is use to build a docker image with semantic-release."
+++

# Semantic Release Container

This repository is use to build a docker image with semantic-release.

It's include the following plugins:

- @semantic-release/git
- @semantic-release/changelog
- @semantic-release/gitlab

## Usage

```sh
docker run -it cclorg/semantic-release:latest
bash-4.4# git clone https://github.com/your/repo.git
bash-4.4# cd repo
bash-4.4# semantic-release ...
```