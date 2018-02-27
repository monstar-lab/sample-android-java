# Sample for Android (Java)

[![CircleCI](https://circleci.com/gh/noboru-i/sample-android-java.svg?style=svg)](https://circleci.com/gh/noboru-i/sample-android-java)

This is sample project for Android (Java).

## Setup

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
