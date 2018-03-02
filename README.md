# Sample for Android (Java)

[![CircleCI](https://circleci.com/gh/noboru-i/sample-android-java.svg?style=svg)](https://circleci.com/gh/noboru-i/sample-android-java)

This is the sample continuous integrated project for Android (Java).

## What is this repository?

- **Lint**: Configured lint setting with [monstar-lab/gradle-android-ci-check](https://github.com/monstar-lab/gradle-android-ci-check).
  - **CheckStyle**
  - **Findbugs**
  - **PMD/PMD-CPD**
  - **Android Lint**
- **Build**: Configured build setting. e.g. `signingConfigs`, `buildTypes`
- **CircleCI**: Lint, Test, and Build in [CircleCI](https://circleci.com/).
- **PR Comment by Danger**: [Danger](http://danger.systems/ruby/) configuration is included. Lint error comes as PR comment.


## How to setup

1. Setup CircleCI build.
    - Turn "On" "Only build pull requests".
2. Copy or refer to below files. [diff](https://github.com/noboru-i/sample-android-java/compare/ebfaaf24a68981a81e02be24a1f71bbfde0bf0e4...master)
    - `.circleci/config.yml`
    - `Dangerfile`
    - `Gemfile`
    - `Gemfile.lock` : If you want newer version, please exec `bundle update`.
    - `app/build.gradle`
    - `app/keystores/debug.keystore` : Please get from local.
    - `app/keystores/release.jks` : Please get or create.
2. Set environment variable.
    - `DANGER_GITHUB_API_TOKEN` : token for check bot
    - `ANDROID_KEYSTORE_PASSWORD` : password for release keystore
    - `ANDROID_KEYSTORE_ALIAS` : alias for release keystore
    - `ANDROID_KEYSTORE_PRIVATE_KEY_PASSWORD` : alias's password for release keystore

## Customize

This repository is targeting for very simple project.

But in real world, we need to work for complex project.

We have some advice for customizing configuration in [Wiki](https://github.com/noboru-i/sample-android-java/wiki).
Please refer to it.
