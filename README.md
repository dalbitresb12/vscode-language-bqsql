# BigQuery SQL Language Support in Visual Studio Code

Syntax highlighting and code snippets for BigQuery SQL in Visual Studio Code.

## Changes from upstream

This extension is a fork of the original extension [SQL (BigQuery)] by [Shinichi Takii].

The following changes were made:

- Renamed the language ID from `sql-bigquery` to `bqsql`.
  - This change was made to provide syntax highlight to [BigQuery Driver for SQLTools], which together with [SQLTools] provide autocompletion and integration with BigQuery.
- Added file icon to `bqsql` language.
- Applied patch for highlight of table names with hyphens ([shinichi-takii/vscode-language-sql-bigquery#49] by [@alatani]).
- Renamed the extension to `BigQuery SQL Language Support`.
- Bump to v2 due to the language ID change.

### Recommended extensions and settings

- [SQLTools] by Matheus Teixeira
- [BigQuery Driver for SQLTools] by Evidence

Adding the following to your `settings.json` file in your workspace will enable the SQLTools extension to provide autocompletion, formatting and codelens in BigQuery SQL files:

```json
{
  "sqltools.formatLanguages": [
    "sql",
    "bqsql"
  ],
  "sqltools.completionLanguages": [
    "sql",
    "bqsql"
  ],
  "sqltools.codelensLanguages": [
    "sql",
    "bqsql"
  ]
}
```

## Features

- Syntax highlighting for Google BigQuery SQL language.
- Supports [Standard SQL] and [Legacy SQL].
- Detect and highlight Legacy SQL only functions.
- Code snippets with SQL, DML, DDL, and Standard SQL functions.

## Installation

1. View > Extensions
2. Search for `BigQuery SQL Language Support`
3. Click the **Install** button

## Usage

1. View > Command Pallet > Change Language Mode (or <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>L</kbd>)
2. Select to `BigQuery SQL`

Alternatively, if you are exclusively using BigQuery SQL, you can add the following to the `settings.json` file in your workspace:

```json
{
  "files.associations": {
    "*.sql": "bqsql"
  }
}
```

## License

[MIT](LICENSE)

[SQL (BigQuery)]: https://marketplace.visualstudio.com/items?itemName=shinichi-takii.sql-bigquery
[BigQuery Driver for SQLTools]: https://marketplace.visualstudio.com/items?itemName=Evidence.sqltools-bigquery-driver
[SQLTools]: https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools
[shinichi-takii/vscode-language-sql-bigquery#49]: https://github.com/shinichi-takii/vscode-language-sql-bigquery/pull/49
[Standard SQL]: https://cloud.google.com/bigquery/docs/reference/standard-sql/
[Legacy SQL]: https://cloud.google.com/bigquery/docs/reference/legacy-sql/
[@alatani]: https://github.com/alatani
[Shinichi Takii]: https://github.com/shinichi-takii
