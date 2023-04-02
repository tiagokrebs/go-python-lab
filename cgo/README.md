# CPython and Go

```
export CGO_CFLAGS="-I $(python -c 'import numpy; print(numpy.get_include())')"
go build

make test

make bench
```
