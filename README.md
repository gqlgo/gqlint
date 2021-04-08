# gqlint

`gqlint` is a linter for GraphQL's schemas and queries.

## Install

`gqlint` can be installed by `go install` command.

```sh
$ go install github.com/gqlgo/gqlint@latest
```

The `gqlint` command has two flags, `schema` and `query` which will be parsed and analyzed by analyzers.

```sh
$ gqlint -schema="server/graphql/schema/**/*.graphql" -query="client/**/*.graphql"
```

The default value of `schema` is "schema/*/**.graphql" and `query` is `query/*/**.graphql`.

`schema` flag accepts URL for a endpoint of GraphQL server.
`lackid` will get schemas by an introspection query via the endpoint.

```sh
$ gqlint -schema="https://example.com" -query="client/**/*.graphql"
```

## Analyzers

`gqlint` is a collection of below analyzers.

* [gqlgo/lackid](https://github.com/gqlgo/lackid) - Detect lack of id in GraphQL query

## Author

[![Appify Technologies, Inc.](appify-logo.png)](http://github.com/appify-technologies)
