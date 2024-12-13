# Meteor Up ![GitHub Workflow Status (branch)](https://img.shields.io/github/workflow/status/zodern/meteor-up/Test/master?style=flat-square) [![Gitter](https://img.shields.io/gitter/room/meteor-up/Lobby.svg?style=flat-square)](https://gitter.im/meteor-up/Lobby) [![Backers on Open Collective](https://opencollective.com/meteor-up/backers/badge.svg)](#backers) [![Sponsors on Open Collective](https://opencollective.com/meteor-up/sponsors/badge.svg)](#sponsors)

## This Fork

***@cunneen/mup***
This is a fork of [meteor-up](https://github.com/zodern/meteor-up) to add ARM support, for Meteor >= 2.3 (including Meteor 3.x). Once I've tested its stability it'll be submitted as a PR to zodern/meteor-up. These changes depend on the following forks:

- zodern/meteor-docker (forked as [cunneen/meteor-docker - feature/arm-support branch](https://github.com/cunneen/meteor-docker/tree/feature/arm-support))
- meteor/meteor (forked as [cunneen/meteor - release-2.17.arm-support branch](https://github.com/cunneen/meteor/tree/release-2.17.arm-support))
- meteor/node-v14-esm (forked as [cunneen/node-v14-esm - release-v14.x-ARM branch](https://github.com/cunneen/node-v14-esm/tree/release-v14.x-ARM)) -
  There are no significant changes to this, I simply compiled it for ARM.

***Changes***

- Added the following `buildOptions` :
  - `aarch64`: boolean, set to `true` to set `--architecture os.linux.aarch64` for the `meteor build` command (
    uses `--architecture os.linux.x86_64` otherwise)
  - `nodeHeaders`: string, set to the absolute path of a local copy of the node_headers TGZ file for the version of node you wish to use. This is required by native node packages, in particular `fibers` on Meteor v2.x.
    - You can download the v14.21.4 ESM Node headers from here:
      - [https://public.juto.com.au/node/v14.21.4/node-v14.21.4-headers.tar.gz](https://public.juto.com.au/node/v14.21.4/node-v14.21.4-headers.tar.gz)
    - You'll only need this for Meteor 2.x on ARM (using node v14.21.4 ESM)
    - Other versions will be automatically installed from nodejs.org e.g. [https://nodejs.org/download/release/v14.21.3/node-v14.21.3-headers.tar.gz](https://nodejs.org/download/release/v14.21.3/node-v14.21.3-headers.tar.gz)

---

#### Production Quality Meteor Deployments

Meteor Up is a command line tool that allows you to deploy any [Meteor](http://meteor.com) app to your own server.

You can install and use Meteor Up on Linux, Mac and Windows. It can deploy to servers running Ubuntu 14 or newer.

This version of Meteor Up is powered by [Docker](http://www.docker.com/), making deployment easy to manage and reducing server specific errors.

Read the [getting started tutorial](http://meteor-up.com/getting-started.html).

### Features

* Single command server setup
* Single command deployment
* Deploy to multiple servers, with optional load balancing and sticky sessions
* Environment Variable management
* Support for [`settings.json`](http://docs.meteor.com/#meteor_settings)
* Password or Private Key (pem) based server authentication
* Access logs from the terminal (supports log tailing)
* Support for custom docker images
* Support for Let's Encrypt and custom SSL certificates

[Roadmap](ROADMAP.md)

### Server Configuration

* Auto-restart if the app crashes
* Auto-start after server reboot
* Runs with docker for better security and isolation
* Reverts to the previous version if the deployment failed

### Installation

Meteor Up requires Node v8 or newer. It runs on Windows, Mac, and Linux.

```bash
npm install -g mup
```

`mup` should be installed on the computer you are deploying from.

### Using Mup
- [Getting Started](http://meteor-up.com/getting-started.html)
- [Docs](http://meteor-up.com/docs.html)

## Meteor compatibility

Mup supports Meteor 1.2 and newer.
To use Meteor 1.4 and newer, you will need to change the docker image. A list of docker images is available [here](http://meteor-up.com/docs#meteor-support).

### Support

First, look at the [troubleshooting](http://meteor-up.com/docs.html#troubleshooting) and [common problems](http://meteor-up.com/docs.html#common-problems) sections of the docs. You can also search the [github issues](https://github.com/zodern/meteor-up/issues).

If that doesn't solve the problem, you can:

- [Create a Github issue](https://github.com/zodern/meteor-up/issues/new)
- [Chat on Gitter](https://gitter.im/meteor-up/Lobby)

## Contributors

This project exists thanks to all the people who contribute. [[Contribute]](CONTRIBUTING.md).
<a href="graphs/contributors"><img src="https://opencollective.com/meteor-up/contributors.svg?width=890" /></a>


## Backers

Thank you to all our backers! 🙏 [[Become a backer](https://opencollective.com/meteor-up#backer)]

<a href="https://opencollective.com/meteor-up#backers" target="_blank"><img src="https://opencollective.com/meteor-up/backers.svg?width=890"></a>


## Sponsors

Support this project by becoming a sponsor. Your logo will show up here with a link to your website. [[Become a sponsor](https://opencollective.com/meteor-up#sponsor)]

<a href="https://opencollective.com/meteor-up/sponsor/0/website" target="_blank"><img src="https://opencollective.com/meteor-up/sponsor/0/avatar.svg"></a>
<a href="https://opencollective.com/meteor-up/sponsor/1/website" target="_blank"><img src="https://opencollective.com/meteor-up/sponsor/1/avatar.svg"></a>
<a href="https://opencollective.com/meteor-up/sponsor/2/website" target="_blank"><img src="https://opencollective.com/meteor-up/sponsor/2/avatar.svg"></a>
<a href="https://opencollective.com/meteor-up/sponsor/3/website" target="_blank"><img src="https://opencollective.com/meteor-up/sponsor/3/avatar.svg"></a>
<a href="https://opencollective.com/meteor-up/sponsor/4/website" target="_blank"><img src="https://opencollective.com/meteor-up/sponsor/4/avatar.svg"></a>
<a href="https://opencollective.com/meteor-up/sponsor/5/website" target="_blank"><img src="https://opencollective.com/meteor-up/sponsor/5/avatar.svg"></a>
<a href="https://opencollective.com/meteor-up/sponsor/6/website" target="_blank"><img src="https://opencollective.com/meteor-up/sponsor/6/avatar.svg"></a>
<a href="https://opencollective.com/meteor-up/sponsor/7/website" target="_blank"><img src="https://opencollective.com/meteor-up/sponsor/7/avatar.svg"></a>
<a href="https://opencollective.com/meteor-up/sponsor/8/website" target="_blank"><img src="https://opencollective.com/meteor-up/sponsor/8/avatar.svg"></a>
<a href="https://opencollective.com/meteor-up/sponsor/9/website" target="_blank"><img src="https://opencollective.com/meteor-up/sponsor/9/avatar.svg"></a>
