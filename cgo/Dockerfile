FROM python:3.10-slim
RUN apt-get update && apt-get install -y curl gcc make pkg-config
RUN curl -LO https://golang.org/dl/go1.19.7.linux-amd64.tar.gz
RUN tar xz -C /opt -f go1.19.7.linux-amd64.tar.gz
ENV PATH="/opt/go/bin:${PATH}"
RUN python -m pip install --upgrade pip
RUN python -m pip install numpy~=1.24
WORKDIR /cgo
COPY . .
RUN go mod init github.com/tiagokrebs/go-python-lab/cgo
RUN make test
