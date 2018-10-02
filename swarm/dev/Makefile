.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/arokapil/go-cents/cmd/swarm
	go build -o bin/geth     github.com/arokapil/go-cents/cmd/geth
	go build -o bin/bootnode github.com/arokapil/go-cents/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/arokapil/go-cents/swarm/...
