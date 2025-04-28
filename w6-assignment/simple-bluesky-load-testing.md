# Simple Bluesky With Load Testing

Another topic we discussed was load testing. Metrics such as total HTTP requests and request duration are essential for monitoring how the system behaves under load.

## Implementing monitoring through metrics:

I use Prometheus to collect API metrics and Grafana to visualize them. This allows me to monitor the processing time of the sign-in, sign-out, and create-post APIs, along with metrics such as HTTP request total and HTTP request duration.

![Metrics](/images/prometheus.gif)

## Implementing Log Tracking:

You can see important events, like failed logins, right on a dashboard and track the number of logs coming in over time. This is super helpful for spotting issues early and keeping things running smoothly.

![Logs](/images/grafana-loki.gif)

## Implementing traces with Grafana + Jaeger:

In this short video, you can see how a user login request is traced all the way through to the ListFeeds API call, including the time spent at each step. Using Jaeger, we’re able to visualize the entire request flow and pinpoint where time is being consumed.

![Traces](/images/grafana-jaeger.gif)
