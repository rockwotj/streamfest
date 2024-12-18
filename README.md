# Streamfest 2024 - Redpanda Connect AI Demo

This is a demo from my streamfest presentation on Redpanda's Sovereign AI functionality.


It's an AI data pipeline that can run entirely local in your network. It showcases an ecommerce flow of sending personalized emails
of relevant products when a user creates a transaction. It uses llama3.2 and llamaguard3 to create an email and ensure it's generating
safe content. It features Clickhouse to use as a database and vector search engine.

## To run

* Download the latest Redpanda Connect: https://docs.redpanda.com/redpanda-connect/get-started/quickstarts/rpk/
* Download Clickhouse: https://clickhouse.com/docs/en/install
* Start Clickhouse in the background: `./clickhouse server`
* Run the ingestion pipeline to seed initial data: `rpk connect run ./ingest.yaml`
* Run the demo AI pipeline that I ran in my presentation: `rpk connect run -e .env ./connect.yaml`

The last step will require an API key with https://www.mailslurp.com/
