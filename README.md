# kubecolor completion for fish shell

## Install

```fish
$ mkdir -p ~/.config/fish/completions
$ cd ~/.config/fish
$ git clone https://github.com/awinecki/fish-kubecolor-completions
$ ln -s ../fish-kubecolor-completions/completions/kubecolor.fish completions/
```

### Install using [Fisher](https://github.com/jorgebucaran/fisher)

`fisher install evanlucas/fish-kubecolor-completions`

## Building

This was tested using go 1.15.7 on macOS 11.1 "Big Sur".

```console
$ make build
```

## Environment Variables

### `FISH_KUBECOLOR_COMPLETION_TIMEOUT`

This is used to pass the `--request-timeout` flag to the `kubecolor` command.
It defaults to `5s`.

> Non-zero values should contain a corresponding time unit (e.g. 1s, 2m, 3h).
> A value of zero means don't timeout requests.

### `FISH_KUBECOLOR_COMPLETION_COMPLETE_CRDS`

This can be used to prevent completing CRDs. Some users may have limited access
to resources.
It defaults to `1`. To disable, set to anything other than `1`.

## Author

Forked by: Andrzej Winecki

Original credit goes to Evan Lucas (https://github.com/evanlucas/fish-kubectl-completions).

## License

MIT
