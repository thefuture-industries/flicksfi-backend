BATCH_FILE_TEST := tests/main.start.test.bat

build:
	@go build -o bin/flicksfi main.go

test:
	@go test -v ./...

run: build
	@./bin/flicksfi

run-to-test:
	@cmd /c "$(CURDIR)/$(BATCH_FILE_TEST)"

migration:
	@migrate create -ext sql -dir cmd/migrate/migrations $(filter-out $@,$(MAKECMDGOALS))

migrate-up:
	@go run cmd/migrate/main.go up

migrate-down:
	@go run cmd/migrate/main.go down
