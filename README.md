## How to get API Key?

Please register on [football-data.org](http://api.football-data.org/register) to get your API Key. Then run `$ football config` to add your API Key (use `sudo` if required). Requests made using API key increases your rate limit from 50 reqs per day to 50 requests per minute


## Usage

### Commands available

```shell
football <command>

Commands:
  scores     Get scores of past and live fixtures
  fixtures   Get upcoming and past fixtures of a league and team
  standings  Get standings of particular league
  lists      List of codes of various competitions
  config     Change configuration and defaults

Options:
  -h, --help  Show help                                          [boolean]

```

#### Command `scores`
Get scores of past and live fixtures



```shell
Usage: football scores [options]

Options:
  -h, --help  Show help                                          [boolean]
  -l, --live  Live scores                                        [boolean]
  -t, --team  Select team                                        [string]

Examples:
  football scores -t "Manchester United" -l

```

#### Command `fixtures`
Get upcoming and past fixtures of a league and team

```shell
Usage: football fixtures [options]

Options:
  -h, --help    Show help                                         [boolean]
  -d, --days    Number of days from today                         [number]
  -l, --league  League                                            [string]
  -t, --team    Team name or substring of it                      [string]
  -n, --next    Next or upcoming matches                          [boolean]

Examples:
  football fixtures -l PL -d 5 -t "Manchester United" -n

```



#### Command `standings`
Get standings of particular league

```shell
Usage: football standings [options]

Options:
  -h, --help    Show help                                         [boolean]
  -l, --league  League to be searched                             [required]

Examples:
  football standings -l PL

```

#### Command `lists`
List of codes of various competitions

```shell
Usage: football lists [options]

Options:
  -h, --help     Show help                                        [boolean]
  -r, --refresh  Refresh league ids                               [boolean]

Examples:
  football lists -r

```

#### Command `config`
Change configuration and defaults

```shell
Usage: football config

Options:
  -h, --help  Show help                                           [boolean]

Examples:
  football config

```



## Development

Run:

```sh
Clone the repo
$ cd football-cli
$ npm link
```

This will setup a symbolic link to the CLI. Any changes in source files will now be reflected when running the `football` command.

To lint your code, run

```sh
$ npm run lint
```
