[![ci-cd](https://github.com/gethop-dev/database.sql.hikaricp/actions/workflows/ci-cd.yml/badge.svg)](https://github.com/gethop-dev/database.sql.hikaricp/actions/workflows/ci-cd.yml)
[![Clojars Project](https://img.shields.io/clojars/v/dev.gethop/database.sql.hikaricp.svg)](https://clojars.org/dev.gethop/database.sql.hikaricp)

# dev.gethop/database.sql.hikaricp

Temporal fork while [issue #10][] in the [original repository][] is fixed.

[Integrant][] methods for connecting to a SQL database from the
[Duct][] framework using [HikariCP][], an efficient connection pool.


[issue #10]: https://github.com/duct-framework/database.sql.hikaricp/issues/10
[original repository]: https://github.com/duct-framework/database.sql.hikaricp
[integrant]: https://github.com/weavejester/integrant
[duct]:      https://github.com/duct-framework/duct
[hikaricp]:  https://github.com/brettwooldridge/HikariCP

## Installation

To install, add the following to your project `:dependencies`:

    [duct/database.sql.hikaricp "0.4.0"]

## Usage

This library depends on [database.sql][] and provides the
`:duct.database.sql/hikaricp` key, which is derived from
`:duct.database/sql`.

The key takes the same [config options][] as the Clojure [hikari-cp][]
wrapper library, and returns a `duct.database.sql.Boundary` record
that contains a database spec.

```edn
{:duct.database.sql/hikaricp {:jdbc-url "jdbc:sqlite:db/example.sqlite"}}
```

[database.sql]:   https://github.com/duct-framework/database.sql
[config options]: https://github.com/tomekw/hikari-cp#configuration-options
[hikari-cp]:      https://github.com/tomekw/hikari-cp

## License

Copyright © 2018 James Reeves

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
