# Pseudocode Description of a CI/CD pipeline for a Serverless Function

Contents

- [CI](#ci.yml)
- [CD](#cd.yml)
- [Real World Examples](#real-world-examples)

## CI.yml

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


## CD.yml

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


## Real World Examples
Please also see some projects I have implemented CI/CD Pipelines for Servless.

[Victoria Security](https://github.com/glasswall-sre/victoria-security)

[Serverless YAML](https://github.com/glasswall-sre/victoria-security/blob/master/serverless.yml)

[CI/CD Pipelines](https://github.com/glasswall-sre/victoria-security/tree/master/.github/workflows)

***

[Deadletter Watcher](https://github.com/glasswall-sre/dead-letter-watcher)

[Deadletter Listener Servlerless YAML](https://github.com/glasswall-sre/dead-letter-watcher/blob/master/deadletter_listener/serverless.yml)

[Deadletter Resolver Serverless YAML](https://github.com/glasswall-sre/dead-letter-watcher/blob/master/deadletter_resolver/serverless.yml)

[Deadletter Event Trigger Pulumi](https://github.com/glasswall-sre/dead-letter-watcher/tree/master/event_trigger)

[CI/CD Pipelines](https://github.com/glasswall-sre/dead-letter-watcher/tree/master/.github/workflows)
