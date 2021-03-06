# ReLaXed Docker

This project aims at dockerizing [ReLaXed](https://github.com/RelaxedJS/ReLaXed).

## Build

```sh
docker build -t relaxed .
```

## Usage

### Make an alias

```sh
alias relaxed="docker run -it --rm -u $(id -u):$(id -g) -v $(pwd):$(pwd) -w $(pwd) --name relaxed relaxed $@"
```

### Run

```sh
relaxed ./examples/poster/poster.pug --no-sandbox [--build-once]
```

## NB
This tool with the `--no-sandbox` option used to work until recently, and no sandbox setting seemed conclusive.  
This might be a security issue in some usecases.
