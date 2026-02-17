# Ping Endpoint Monitor

Browser-only remake of the old PHP ping tool in `ref/index.php`.

## Run

Serve the folder with any static server:

```bash
python3 -m http.server 4173
```

Open:

`http://127.0.0.1:4173`

## Use

1. Set your ping endpoint URL (for example: `https://your-api.example.com/ping`).
2. Set method/interval/timeout.
3. Click **Start**.

The app continuously sends HTTP requests and shows:

- total + failed pings
- recent avg/low/high
- session low/high
- live colored latency stream
- browser connection details (`navigator.connection`, when available)

## Notes

- This measures HTTP request round-trip time from the browser (not ICMP ping).
- Cross-origin endpoints must allow CORS, or the browser will mark requests as failed.
