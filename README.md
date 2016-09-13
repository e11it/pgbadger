# e11it/pgbadger

![](https://images.microbadger.com/badges/image/e11it/pgbadger.svg)

## Usage

```
$  docker run --rm -v $(pwd):/data e11it/pgbadger postgresql.log
```

## Enable log

```sql
psql -U postgres -c "alter system set log_statement = 'all'"
psql -U postgres -c "alter system set log_min_duration_statement = 0"
psql -U postgres -c "alter system set log_lock_waits = on"
psql -U postgres -c "alter system set log_temp_files = 0"
psql -U postgres -c "alter system set log_autovacuum_min_duration = 0"
psql -U postgres -c "alter system set log_error_verbosity = default"
psql -U postgres -c "select pg_reload_conf()"
```

## Links

- [pgbadger](https://github.com/dalibo/pgbadger)
