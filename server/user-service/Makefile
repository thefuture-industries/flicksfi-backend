.PHONY: fmt lint test

fmt:
	gofmt -w .
	goimports -w .

lint:
	golangci-lint run

check: fmt lint test
	@echo "All checks passed!"

build:
	@echo "Running build..."
	@go build -o bin/user-service main.go

test:
	@go test -v ./...

run: build
	@./bin/user-service

run-to-test:
	@cmd /c "$(CURDIR)/$(BATCH_FILE_TEST)"

migrate-up:
	@echo "Running migrations..."
	@go run cmd/migrate/main.go

migrate-down:
	@go run cmd/migrate/main-down.go
