# Basic Go gRPC Server and Client

This is a basic gRPC server and client written in Go which supports bidirectional streaming RPC.

```

Steps for Installing the gRPC Go plugin

```bash
go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28

go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2

export PATH="$PATH:$(go env GOPATH)/bin"
```

* Create the proto file with the required services and messages in the proto directory


* Generate .pb.go files from the proto file
  
depending on what path you mention in your greet.proto file, you will either run this - 

```bash
protoc --go_out=. --go-grpc_out=. proto/greet.proto
```
OR this -

```bash
protoc --go_out=. --go_opt=module=github.com/akhil/basic-go-grpc --go-grpc_out=. --go-grpc_opt=module=githu
b.com/akhil/basic-go-grpc proto/greet.proto
```


# Running the application

1. Install the dependencies

```bash
go mod tidy
```

2. Run the server

```bash
go run server/main.go
```

3. Run the client

```bash
go run client/main.go
```# GO-Grpc
