# myproto

This repo contains protobuf definitions for a dummy RPC API

Download the Google APIs in the src/github.com/googleapis/googleapis folder then generate the golang protobuf files

## Generate the go file go-proto/api.pb.go 

From the proto files and save them in go-proto folder (defined in ./api/api.proto)

```
protoc -I api/ -I${GOPATH}/src/github.com/googleapis/googleapis --go_out=plugins=grpc:. ./api/api.proto
```

## Generate GRPC Gateway file go-proto/api.pb.gw.go

```
protoc -I api/ -I${GOPATH}/src/github.com/googleapis/googleapis --grpc-gateway_out=logtostderr=true:. ./api/api.proto
``` 
