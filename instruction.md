# Access log summary

Read the access log at `/app/access.log` and write a summary report to `/app/report.json`.

The log uses the common access-log format, one request per non-empty line. The first
whitespace-separated field of each line is the client IP address, and the requested path
is the second token inside the quoted request (for example, `/index.html` in
`"GET /index.html HTTP/1.1"`).

Write `/app/report.json` as a JSON object containing exactly these keys:

- `total_requests`: the total number of requests (non-empty lines) in the log.
- `unique_ips`: the number of distinct client IP addresses.
- `top_path`: the most frequently requested path.

## Success criteria

1. `/app/report.json` exists.
2. `/app/report.json` contains valid JSON.
3. `total_requests` is correct.
4. `unique_ips` is correct.
5. `top_path` is correct.
