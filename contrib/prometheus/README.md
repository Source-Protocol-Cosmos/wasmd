Enable prometheus metrics
* Edit `$HOME/config/app.toml`
```toml
[telemetry]

# Enabled enables the application telemetry functionality. When enabled,
# an in-memory sink is also enabled by default. Operators may also enabled
# other sinks such as Prometheus.
enabled =true
...

# PrometheusRetentionTime, when positive, enables a Prometheus metrics sink.
prometheus-retention-time = 15
```

`retention-time` must be >0 (see prometheus scrape config)



* Edit `$HOME/config/config.toml`
```toml
[instrumentation]

# When true, Prometheus metrics are served under /metrics on
# PrometheusListenAddr.
# Check out the documentation for the list of available metrics.
prometheus = true
```

