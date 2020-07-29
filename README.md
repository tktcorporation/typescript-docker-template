# typescript-base

For creating a Typescript repository.

## Tools

You can customize them easily.

- [Docker](https://www.docker.com/)
- [docker-compose](https://docs.docker.com/compose/)

### Lint
- [ESLint](https://eslint.org/)

### Format

- [Prettier](https://prettier.io/)

### Test

- [Jest](https://jestjs.io/)

### Build

- [tsc](https://www.typescriptlang.org/docs/handbook/compiler-options.html)

## Get Started

### Building Docker

```bash
$ docker-compose build
```

### Working in Docker container

```bash
$ docker-compose run app /bin/bash
```

### Installation

```bash
$ yarn
```

### Lint

```bash
# Find linting error and warnings
$ yarn lint

# Run lint fixing
$ yarn lint:fix
```

### Format

```bash
# Run format
$ yarn format

# This will return exit code 1 if all files are not formatted
$ yarn format:check
```

### Test

```bash
# unit tests
$ yarn test

# e2e tests
$ yarn test:e2e

# test coverage
$ yarn test:cov
```

### Build

```bash
# Run build
$ yarn build
```
