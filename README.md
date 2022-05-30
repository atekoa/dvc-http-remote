# DVC remote proxy

This is a dvc http remote implementation.
It is the "clean" code that we use as a remote for DVC and with which we can reproduce the issue https://github.com/iterative/dvc/issues/7564

Can be used for local storage or azure storage (put proper credentials here->[pkg/storage/storageSiteLoader.go])

## Examples

Start with a [simple example](example_simple/../README.md) and then you can go further with [the complex one](example_complex/README.md)

dvc configuration sample

```toml
['remote "localhost"']
    url = http://localhost/remote/?repo=0
    ssl_verify = false
```

- repo: Select localhost (repo=0) or Azure (repo!=0)