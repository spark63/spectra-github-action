# Spectra Github Action


## Introduction
Spectra Github Action makes an automated audit on smart contracts.

<br>


## Inputs

### `api_key`

- Required: True
- Explanation: Spectra API key obtained from Spectra Web

### `path`

- Required: False
- Explanation: Path for audit targets. Default value is the root directory.

<br>

## Example Usage

```
name: Spectra Github Action

on:
  push:
    branches: ["main"]

jobs:
  main:
    name: Spectra audit
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
        
      - name: Spectra Github Action Step
        uses: spark63/spectra-github-action@v1
        with:
          api_key: ${{ secrets.SPECTRA_API_KEY }}
          path: "contracts"

```

<br>

## License

TBD