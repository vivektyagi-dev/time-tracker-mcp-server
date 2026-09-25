## Database storage

The app uses SQLite. Set `TIMETRACK_DB_PATH` to a writable, persistent location
in the deployment environment, for example:

```text
TIMETRACK_DB_PATH=/data/timetrack.db
```

When this variable is not set and the bundled project directory is read-only,
the app falls back to the operating system temporary directory. That allows
entries to be logged, but temporary storage may be cleared when the server
restarts, so a persistent Horizon volume is recommended for production data.
