# contentful-asset-auditor

`contentful-asset-auditor` is a CLI tool to facilitate the management of media Assets in Contentful.

## Installation

1. Download the source code for the [latest release](https://github.com/kstrongholte/contentful-cleanup/releases/latest).
2. Install the package and dependencies globally with `npm i -g .`.

## Usage
```bash
$ contentful-asset-auditor <command> [options]

Commands:
  get-assets         Get list of assets from Contentful space
  get-asset-details  Get detailed information about assets

Options:
      --version  Show version number                                   [boolean]
  -h, --help     Show help                                             [boolean]
```

### Get a list of Assets and save to JSON file
```bash
$ contentful-asset-auditor get-assets [-o <file_path>]

Options:
      --version      Show version number                               [boolean]
  -o, --output-file  Output file you want to save data to (JSON format)
                                                                      [required]
  -h, --help         Show help                                         [boolean]

Examples:
  contentful-asset-auditor get-assets -o assets.json
```

### Get detailed information about Assets and save to CSV file
```bash
$ contentful-asset-auditor get-asset-details [-i <file_path> | -o <file_path>]

Options:
      --version      Show version number                               [boolean]
  -i, --input-file   Input file you want to read data from (JSON format)
                                                                      [required]
  -o, --output-file  Output file you want to write data to (CSV format)
                                                                      [required]
  -m, --max          Maximum number of assets to analyze
  -h, --help         Show help                                         [boolean]

Examples:
  contentful-asset-auditor get-asset-details -i assets.json -o asset_details.json
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)
