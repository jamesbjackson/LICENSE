# `LICENSE`

`LICENSE` is a collection of useful `LICENSE` templates inspired by [GitHub's `.gitignore`](https://github.com/github/gitignore).

`LICENSE` templates are stored in the `licenses` directory and end in `.license`. They contain some or none of the parameters listed below.

## Why?
To make writing software that generates licenses easier. `LICENSE` serves as a stable public API for `LICENSE` templates that anyone can contribute to. If a license your application requires isn't here, send a pull request!

## Usage
1. Make a request to `https://raw.githubusercontent.com/qw3rtman/LICENSE/master/licenses/{license}.license` where `license` is a `LICENSE` from the table below.
2. Replace all instances of the parameters below with its value (using `sed`, `awk`, etc.). Different licenses require different bits of information; some don't require any. (*ex: Replace* `{{{full_name}}}` *with* `Nimit Kalra`).
3. Done!

Alternatively, you can clone this repository to use `LICENSE` tempaltes offline.

## Parameters
Most licenses require some parameters, which are enclosed in triple braces `{{{parameter}}}` in the LICENSE templates. Below is a list of parameters and their meanings. ("Project" refers to the software being licensed).

`year`: Current year in `YYYY` format (*i.e: 2016*) (`date +"%Y"`)  
`full_name`: Project owner's full name (*i.e: Nimit Kalra*)  
`project_name`: Project's name (*i.e: LICENSE*)  
`description`: Project's description (*i.e: A Collection of Useful LICENSE Templates*)

| Identifier | `year` | `full_name` | `project_name` | `description` |
| ----------:|:------:|:-----------:|:--------------:|:-------------:|
| `agpl-3.0` | ✓ | ✓ | ✓ | ✓ |
| `apache-2.0` | ✓ | ✓ | ✖ | ✖ |
| `artistic-2.0` | ✓ | ✓ | ✖ | ✖ |
| `bsd-2-clause` | ✓ | ✓ | ✖ | ✖ |
| `bsd-3-clause` | ✓ | ✓ | ✓ | ✖ |
| `cc0-1.0` | ✖ | ✖ | ✖ | ✖ |
| `epl-1.0` | ✖ | ✖ | ✖ | ✖ |
| `gpl-2.0` | ✓ | ✓ | ✖ | ✓ |
| `gpl-3.0` | ✓ | ✓ | ✓ | ✓ |
| `isc` | ✓ | ✓ | ✖ | ✖ |
| `lgpl-2.1` | ✓ | ✓ | ✖ | ✓ |
| `lgpl-3.0` | ✖ | ✖ | ✖ | ✖ |
| `mit` | ✓ | ✓ | ✖ | ✖ |
| `mpl-2.0` | ✖ | ✖ | ✖ | ✖ |
| `unlicense` | ✖ | ✖ | ✖ | ✖ |

## `LICENSE` Identifiers
| Identifier | License name |
| ----------:|:------------ |
| `agpl-3.0` | GNU Affero General Public License v3.0|
| `apache-2.0` | Apache License 2.0|
| `artistic-2` | Artistic License 2.0|
| `bsd-2-clause` | BSD 2-clause "Simplified" License|
| `bsd-3-clause` | BSD 3-clause "New" or "Revised" License|
| `cc0-1.0` | Creative Commons Zero v1.0 Universal|
| `epl-1.0` | Eclipse Public License 1.0|
| `gpl-2.0` | GNU General Public License v2.0|
| `gpl-3.0` | GNU General Public License v3.0|
| `isc` | ISC License|
| `lgpl-2.1` | GNU Lesser General Public License v2.1|
| `lgpl-3.0` | GNU Lesser General Public License v3.0|
| `mit` | MIT License|
| `mpl-2.0` | Mozilla Public License 2.0|
| `unlicense` | The Unlicense|

## Contributing
If you catch an error in any of the templates, send in a pull request describing what the error is, why it is an error, and a source (if applicable).

If you'd like to submit a new template, follow the steps below.
1. Fork this repository.
2. Create a new branch (*i.e:* `add-IDENTIFIER-license`), where `IDENTIFIER` is its common identifier and lowercase. If there is no common identifier, create one following the guidelines set by the existing identifiers listed above.
3. Create a file with the contents of the license in the `licenses` directory with the format `IDENTIFIER.license`.
4. Use the parameters listed above where necessary.
5. Add the license to the two tables above (parameters and identifiers).
6. Add the license's name and `IDENTIFIER` to `licenses.json`, `licenses.yaml`, and `licenses.txt`.
7. Send in a pull request. The more information you provide about the license, the better (especially if it is not a well-known license).

If the license you wish to add requires a new parameter, first make an issue about it for discussion. Include why the parameters needs to be added (which license(s) would benefit from it). Adding a new parameter introduces a change in the API that applications may not be expecting or ready for.
