# LibreCores CI Github Action with FuseSoC

This executes FuseSoC in the [LibreCores CI docker
container](https://github.com/librecores/ci-docker-image).

It is still in an early development phase, please feel free to open an issue
with your suggestion!

## Inputs

### `libraries`

Comma-separated list of libraries to add.

### `arguments`

Those are the main arguments. It can also be used to run FuseSoC without setting
any other of the inputs, despite that is discouraged.

### `run-arguments`

Arguments to be passed to the command.

### `core`

The core/system identifier to execute on.

### `core-arguments`

Arguments to be passed to the core.

### `target`

Override default target, default none.

### `tool`

Override default tool for target, default none.

### `path`

Path used by checkout. This is by default guessed from the repo, but if you are
fancy with the checkout paths, it needs to be set accordingly.

## Example usage

```yaml
uses: librecores/ci-fusesoc-action@v1
with:
  core: myorg:mylib:mycore
  target: lint
```
