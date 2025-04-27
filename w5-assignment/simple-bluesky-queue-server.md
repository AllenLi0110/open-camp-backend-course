# Simple Bluesky With Queue Server

Last week, we talked about queues. I found this topic interesting, and it motivated me to explore backend technologies more deeply. It also gave me a better understanding of system design.

## Implementing the queue server:

I used RabbitMQ to set up a queue server for message bridging and notification consumption. This helps manage the process when a user signs in to Simple Bluesky and sends a notification to Slack.
When there's a backlog of events, the queue server stores them and processes them sequentially, following the FIFO(First In, First Out) principle.

![RabbitMQ](/images/rabbitmq-demo.gif)
