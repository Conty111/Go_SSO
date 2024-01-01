# SSO

## How to start

Run migrations (if you haven't done this)

    go run ./cmd/migrator --storage-path=./storage/sso.db --migrations-path=./migrations

Run the application

    go run ./cmd/sso --config=./config/config.yaml

## Tests run
Firstly, run basic migrations (if you have already done it, skip)

    go run ./cmd/migrator --storage-path=./storage/sso.db --migrations-path=./migrations

Secondly, run test migrations

    go run ./cmd/migrator --storage-path=./storage/sso.db --migrations-path=./tests/migrations --migrations-table=migrations_test

After that, run the application

    go run ./cmd/sso --config=./config/local_tests_config.yaml

Finally, run the tests

    go test ./tests -count=1 -v