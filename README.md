![PyGrid logo](https://raw.githubusercontent.com/OpenMined/design-assets/master/logos/PyGrid/horizontal-primary-trans.png)

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/OpenMined/Grid/master) [![Build Status](https://travis-ci.org/OpenMined/PyGrid.svg)](https://travis-ci.org/OpenMined/PyGrid) [![Chat on Slack](https://img.shields.io/badge/chat-on%20slack-7A5979.svg)](https://openmined.slack.com/messages/team_pysyft) [![FOSSA Status](https://camo.githubusercontent.com/c0cb82174c3eb8fcbb00a46eb237556f63b36804/68747470733a2f2f6170702e666f7373612e696f2f6170692f70726f6a656374732f6769742532426769746875622e636f6d2532466d6174746865772d6d6361746565722532465079537966742e7376673f747970653d736d616c6c)](https://app.fossa.io/projects/git%2Bgithub.com%2Fmatthew-mcateer%2FPySyft?ref=badge_small)

PyGrid is a peer-to-peer network of data owners and data scientists who can collectively train AI models using [PySyft](https://github.com/OpenMined/PySyft/).


## Overview
- [Overview](#overview)
- [How to install](#how-to-install)
    - [PyGrid library](#pygrid-library)
  - [Common Installation Issues:](#common-installation-issues)
- [Getting started](#getting-started)
    - [Build images](#build-images)
    - [Let's put all together](#lets-put-all-together)
- [Try out the Tutorials](#try-out-the-tutorials)
- [Start Contributing](#start-contributing)
- [High-level Architecture](#high-level-architecture)
- [Disclaimer](#disclaimer)
- [License](#license)

## How to install

#### PyGrid library
Make PyGrid library importable in python:
```
$ pip install .
```

### Common Installation Issues:
- On macOS, you might get ```ld: library not found for -lssl```. It happens when openssl is missing. Kindly install openSSL, add it to you path and try again. You can also fix the issue by installing the appropriate Xcode Command line tools from [here](https://developer.apple.com/download/more/).

## Getting started
To boot the entire PyGrid platform locally, we will use docker containers.  
To install docker the dependencies, just follow [docker documentation](https://docs.docker.com/install/).


#### Build images
```
$ docker build -t node ./app/websocket/  # Build PyGrid node image
$ docker build -t gateway ./gateway/  # Build gateway image
```

#### Let's put all together
**PS:** Fell free to increase/decrease the number of initial PyGrid nodes ***(you can do this by changing the docker-compose.yml file)***.
```
$ docker-compose up
```
Done! now we have a gateway and three nodes (by default) running locally.

## Try out the Tutorials
A comprehensive list of tutorials can be found [here](https://github.com/OpenMined/Grid/tree/master/examples).
A list with latest experimental tutorials can be found in the dev branch [here](https://github.com/Quisher/Grid/tree/dev/examples).

These tutorials cover how to create a PyGrid node and what operations you can perform.

## Start Contributing
The guide for contributors can be found [here](https://github.com/OpenMined/PySyft/tree/master/CONTRIBUTING.md). It covers all that you need to know to start contributing code to PySyft in an easy way.

Also join the rapidly growing community of 2500+ on [Slack](http://slack.openmined.org). The slack community is very friendly and great about quickly answering questions about the use and development of PyGrid/PySyft!

We also have a Github Project page for PySyft and PyGrid [here](https://github.com/orgs/OpenMined/projects/9).


## High-level Architecture

![High-level Architecture](https://raw.githubusercontent.com/OpenMined/PyGrid/dev/art/PyGrid-Arch.png)


## Disclaimer
Do ***NOT*** use this code to protect data (private or otherwise) - at present it is very insecure.

## License

[Apache License 2.0](https://github.com/OpenMined/Grid/blob/master/LICENSE)
