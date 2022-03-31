$ apt install -y protobuf-compiler
$ protoc --version  # Ensure compiler version is 3+

go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest



protoc --go_out=. --go-grpc_opt=require_unimplemented_servers=false --go-grpc_out=. chat/chat.proto
or
protoc --go-grpc_out=. --go_out=. chat/chat.proto
