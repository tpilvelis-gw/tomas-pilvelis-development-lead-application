# Pseudocode Description of a CI/CD pipeline for a Serverless Function


```
name: CI

on:
  pull_request:
    branches: [ dev ]

jobs:

  static-code-analysis:
    runs-on: ubuntu-latest

    - uses: actions/checkout@v2

    ################################
    # Run linter against code base #
    ################################

    ################################
    # Run Static Analyser          #
    ################################

  build:
    runs-on: ubuntu-latest

    - uses: actions/checkout@v2

    ################################
    # Install Dependencies         #
    ################################

    ################################
    # Build Codebase               #
    ################################

  test:
    runs-on: ubuntu-latest

    - uses: actions/checkout@v2

    ################################
    # Run Unit Tests               #
    ################################
  
    ################################
    # Run Integration Tests        #
    ################################
```

```
name: CD

on:
  pull_request:
    branches: [ master ]

jobs:

  static-code-analysis:
    runs-on: ubuntu-latest

    - uses: actions/checkout@v2

    ################################
    # Run linter against code base #
    ################################

    ################################
    # Run Static Analyser          #
    ################################

  build:
    runs-on: ubuntu-latest

    - uses: actions/checkout@v2

    ################################
    # Install Serverless           #
    ################################

    ################################
    # Install Serverless Plugins   #
    ################################

    ################################
    # Build Project                #
    ################################

  test:
    runs-on: ubuntu-latest

    - uses: actions/checkout@v2

    ################################
    # Run Unit Tests               #
    ################################
  
    ################################
    # Run Integration Tests        #
    ################################

  deploy:
    runs-on: ubuntu-latest

    - uses: actions/checkout@v2

    ################################
    # Install Serverless           #
    ################################

    ################################
    # Install Serverless Plugins(o)#
    ################################

    ################################
    # Build Project                #
    ################################
```

Please also see some projects I have implemented CI/CD Pipelines for.

[Victoria Security](https://github.com/glasswall-sre/victoria-security/tree/master/.github/workflows)

[Deadletter Watcher](https://github.com/glasswall-sre/dead-letter-watcher/tree/master/.github/workflows)
