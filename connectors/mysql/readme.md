---
title: 'MySQL'
---

MySQL connector allows querying MySQL/MariaDB databases.

## Config Schema

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| type | string | yes | constant: `mysql`  |
| host | string | yes | Database host address |
| database | string | yes | Database name |
| user | string | yes | Username |
| password | string | yes | Password |
| port | integer | yes | TCP port (default 3306) |
| tlsConfig | string | no | TLS configuration name from MySQL server |
| proxy | string | no | SOCKS5 proxy address (e.g. `127.0.0.1:7890`) |
| conn_string | string | no | Direct connection string (DSN format) |

## Config example:

```yaml
type: mysql
host: localhost
database: mydb
user: root
password: secret
port: 3306
tlsConfig: ""       # Optional TLS configuration name from MySQL server 
proxy: ""           # Optional SOCKS5 proxy address (e.g. 127.0.0.1:7890)
```

Or as alternative with direct connection string:

```yaml
type: mysql
conn_string: root:secret@tcp(localhost:3306)/mydb
```
