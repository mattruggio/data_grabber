# Data Grabber

[![CI](https://github.com/mattruggio/data_grabber/actions/workflows/ci.yaml/badge.svg)](https://github.com/mattruggio/data_grabber/actions/workflows/ci.yaml) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Public collection of Ruby scripts that I have been personally building up throughout the years to call external data sources and export data I am interested in evaluating further and/or preserve.

## Installation

To use:

1. Pour some coffee into your favorite mug, take a few sips
1. Clone this repository: `git clone git@github.com:mattruggio/data_grabber.git`
1. Change to project root directory: `cd data_grabber`
1. Bundle dependencies: `bundle`
1. Copy configuration file: `cp .env.example .env`
1. Fill out configuration file (`.env`) as required per script (each script may have its own specific entries)

## Scripts

### YouTube Public Channel Export

This script will attempt to create a JSON export based on the inputted channel ID. This script should be able to export **any** public channel and its public data and is not designed to grab private channels and/or private data for public channels.

#### Configuration Requirements

KEY             | DESCRIPTION
--------------- | -----------
YOUTUBE_API_KEY | Get developer API Key in [Google's developer console](https://console.cloud.google.com/apis/credentials).

#### Running

The general CLI specification is:

`exe/youtube/public/channel CHANNEL_ID <JSON_FILE_DESTINATION>`

Example(s):

* Output to shell: `exe/youtube/public/channel abc123zyx`
* Output to file: `exe/youtube/public/channel abc123zyx tmp/channel_export.json`

## Development

This is very much in the state of a personal-use project and will be missing key structures, most notably:

* Extraction of code into Ruby classes
* Tests
* Proper options parsing
* Long-running process feedback via shell

Any and all contributions are welcome.

### Linting

```zsh
bin/rubocop
```

### Dependency Auditing

```zsh
bin/bundler-audit check --update
```

## Code of Conduct

Everyone interacting in this codebase, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/mattruggio/data_grabber/blob/main/CODE_OF_CONDUCT.md).

## License

This project is MIT Licensed.
