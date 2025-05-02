I was going to write a [franz-go](https://github.com/twmb/franz-go) mock similar to [pgxmock](https://github.com/pashagolub/pgxmock/tree/master) or [sqlmock](https://github.com/DATA-DOG/go-sqlmock) but you should just use [kfake](https://github.com/twmb/franz-go/tree/master/pkg/kfake).

kfake [examples](https://grep.app/search?q=franz-go%2Fpkg%2Fkfake). If you're looking to mock simple consumer/producer messages then this [example](https://github.com/redpanda-data/console/blob/master/backend/pkg/console/list_messages_integration_test.go#L306) from RedPanda is probably what you're looking for.

Here's the [issue](https://github.com/twmb/franz-go/issues/58#issuecomment-896368502) where I learned about kfake. 