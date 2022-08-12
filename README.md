# How to run the Wordcloud app:

1. Clone all the wordcloud repos into the same folder. Make sure the subfolders are named "core", "worker", and "frontend" and they are in the same folder with the docker-compose file.
2. Run "docker compose up" in the parent folder.
3. IMPORTANT: for some reason, the RabbitMQ queue creation fails. To get around this, go to http://localhost:15672/#/queues and log in with the credentials "guest", "guest". Then manually create a new queue named "core.queue" and select durability: transient. Since this error causes the worker app to fail, start that container again.
4. Go to localhost:3000 to use the app.
