### Postgres extension updates

The following Postgres extensions were updated to a newer version and are now supported with Postgres 16:

| Postgres extension           | Old version   | New version   |
|------------------------------|---------------|---------------|
| `pg_jsonschema`              | 0.1.4         | 0.2.0         |
| `pg_graphql`                 | 1.1.0         | 1.4.0         |
| `pgx_ulid`                   | 0.1.0         | 0.1.3         |

If you installed these extensions previously and want to upgrade to the latest version, please refer to [Update an extension version](/docs/extensions/pg-extensions#update-an-extension-version) for instructions.

Additionally, the [pg_tiktoken](/docs/extensions/pg_tiktoken) extension is now supported with Postgres 16.

For a complete list of Postgres extensions supported by Neon, see [Postgres extensions](/docs/extensions/pg-extensions).

### Fixes & improvements

- Compute: Fixed an issue that caused an invalid database state after a failed `DROP DATABASE` operation.
