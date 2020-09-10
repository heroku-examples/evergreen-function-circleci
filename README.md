# Example of testing Evergreen functions with CircleCI

During the Functions Pilot, their continuous integration story will utilize CircleCI & GitHub. This repo is a working example to develop & test toward Pilot.

👓 For more context, see: [Functions Continuous Integration | Delivery PRD](https://salesforce.quip.com/cJASAvjPQV8k#WEBACAAqmIJ).

## How does it work?

This repo is an sfdx project, created with `sfdx force:project:create`.

The [example function](functions/ExampleFunction/) is the default created with `sfdx evergreen:function:create`.

The [CircleCI configuration](.circleci/config.yml) powers the continuous integration workflow. It may be copied and reused with another sfdx project & CircleCI.

## Setup a new project

1. configure JWT auth for a new "CircleCI" Connected App in your Salesforce DevHub
1. copy `.circleci/config.yml` into your project, commit, & push to GitHub repo
1. create the CircleCI Project for the GitHub repo
1. set JWT auth environment variables in the CircleCI project:
    - `SFDX_CONSUMER_KEY`
    - `SFDX_JWT_KEY` (base64 encoded)
    - `SFDX_USERNAME`
1. start building 🏗
