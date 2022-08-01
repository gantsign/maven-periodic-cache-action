maven-periodic-cache-action
===========================

[![Tests](https://github.com/gantsign/maven-periodic-cache-action/actions/workflows/tests.yml/badge.svg)](https://github.com/gantsign/maven-periodic-cache-action/actions/workflows/tests.yml)

GitHub Action that caches the Maven repository periodically by date.

Usage
-----

```yaml
jobs:
  release:
    name: Release
    runs-on: ubuntu-20.04
    steps:
      - name: Cache the local Maven repository
        uses: gantsign/maven-periodic-cache-action@v1
        with:
           cache-period-days: 30
           additional-path: '!~/.m2/repository/com/example'
           key-suffix: '-deploy-site'
```

License
-------

The Unlicense

Author Information
------------------

John Freeman

GantSign Ltd.
Company No. 06109112 (registered in England)
