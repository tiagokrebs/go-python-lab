NPY_INC = $(shell python -c 'import numpy; print(numpy.get_include())')

test:
	PYTHONPATH=$(PWD) CGO_CFLAGS="-I $(NPY_INC)" \
		go test -v

bench:
	PYTHONPATH=$(PWD) CGO_CFLAGS="-I $(NPY_INC)" \
	       go test -run NONE -bench .
