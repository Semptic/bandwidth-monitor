[![test](https://github.com/Semptic/bandwidth-monitor/actions/workflows/test.yml/badge.svg)](https://github.com/Semptic/bandwidth-monitor/actions/workflows/test.yml)
[![GitHub](https://img.shields.io/github/license/Semptic/bandwidth-monitor)](https://github.com/Semptic/bandwidth-monitor/blob/main/LICENSE)
![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/Semptic/bandwidth-monitor)


# bandwidth-monitor

This uses Ookla to run speed tests and store the results in a google sheet

## Install

You need to install [speedtest-cli from ookla](https://www.speedtest.net/de/apps/cli) first. You also 
need to run it once and accept the eula manually.

Download the binary from [github](https://github.com/Semptic/bandwidth-monitor/releases).

E.g. you could use curl to download it:
```bash
curl -L -o bandwidth-monitor.zip https://github.com/Semptic/bandwidth-monitor/releases/download/v0.2.0/bandwidth-monitor-v0.2.0-x86_64-unknown-linux-musl.zip
```

## Google Credentials

Follow [this](/credentials.md) to setup an service account and to get the key. (This is based on https://github.com/juampynr/google-spreadsheet-reader who did a great job in documenting it.)

## Usage

You can run it like
```bash
./bandwith-monitor <spreadsheet_id>
```

You get your sheet id from the URL: `https://docs.google.com/spreadsheets/d/1WOIazmVG9vr2-GcdLi6Yz4sCHjAkgnlqSTvetiUM1oE/edit#gid=1042246224`. The id is the part after `/d/` so in this example it would be `1WOIIzmVG9vr2-GcdLi6Yz4sCHjAkgnlqSTvetiUM1iE`.

## Development

### Prerequisite

* Install [cargo-make](https://github.com/sagiegurari/cargo-make). 

### Test

To test this project run

```bash
cargo make test
```
