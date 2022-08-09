# flutter-version-number-action
[![Test](https://github.com/NiklasLehnfeld/flutter-version-number-action/actions/workflows/main.yaml/badge.svg)](https://github.com/NiklasLehnfeld/flutter-version-number-action/actions/workflows/main.yaml) 

📱 Github Action to read out version number of flutter project from pubspec.yaml

## Usage

```yaml
on:
  push:
    branches:
      - main
name: Test
jobs:
  test:
    name: test
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - id: read-version
        uses: sadi304/flutter-version-number-action@main
        with:
          file-path: example/pubspec.yaml
```

### Outputs
```
steps.read-version.outputs.full-version (1.0.1+12)
steps.read-version.outputs.version (1.0.1)
steps.read-version.outputs.build-number (12)
```
