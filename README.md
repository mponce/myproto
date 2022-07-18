# myproto

This repo contains protobuf definitions for a dummy RPC API

Download the Google APIs in the src/github.com/googleapis/googleapis folder then generate the golang protobuf files

## To generate the files in go-proto

```
protoc -I api/ -I${GOPATH}/src/github.com/googleapis/googleapis --go_out=. ./api/api.proto
```
