# E-Commerce Microservices Project

This project is a microservices-based e-commerce platform built using Go. It consists of three main components:

1. **Inventory Service**: Manages product inventory.
2. **Order Service**: Handles order creation, updates, and retrieval.
3. **API Gateway**: Provides a unified HTTP interface for clients to interact with the services.

## Project Structure
ecommerce/ 
├── api-gateway/ │ ├── main.go │ ├── config/ │ │ └── grpc.go │ ├── handlers/ │ │ ├── http.go │ │ ├── middleware.go │ │ └── telemetry.go ├── inventory-service/ │ ├── main.go │ ├── repository/ │ │ ├── db.go │ │ └── product.go │ ├── services/ │ │ └── product.go │ ├── handlers/ │ └── grpc.go ├── order-service/ │ ├── main.go │ ├── repository/ │ │ ├── db.go │ │ └── order.go │ ├── services/ │ │ └── order.go │ ├── handlers/ │ └── grpc.go ├── proto/ │ ├── inventory.proto │ ├── inventory.pb.go │ ├── inventory_grpc.pb.go │ ├── order.proto │ ├── order.pb.go │ └── order_grpc.pb.go ├── go.mod └── go.sum


## Requirements

- **Go**: Version 1.22 or later.
- **Protocol Buffers Compiler (`protoc`)**: Version 3.19.6 or later.
- **gRPC Plugins for Go**:
  - `protoc-gen-go`
  - `protoc-gen-go-grpc`
- **SQLite**: For database operations.

## Setup Instructions

### 1. Clone the Repository

```sh
git clone <repository-url>
cd ecommerce
