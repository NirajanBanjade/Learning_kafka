📌 Project Overview
Built a real-time review analytics pipeline using Confluent Cloud (Kafka), Kaggle (Python), and Elastic Cloud (Elasticsearch/Kibana).

Pipeline

Producer (kafka-producer.ipynb): stream Yelp reviews → Confluent Kafka.

Consumer (kafka-spark.ipynb / elasticsearch-stream.ipynb): read from Kafka, do sentiment, send to Elasticsearch.

Elasticsearch Enrichment: join reviews with businesses index via enrich policy + ingest pipeline.

Kibana Dashboards: visualize by sentiment, location, category.

🛠 Tech Stack
Confluent Cloud (Kafka)

Kaggle Notebooks (producer/consumer)

Elastic Cloud (Elasticsearch + Kibana)

Python (ingest, transform, ES API)

🔁 What each notebook/file does
kafka-producer.ipynb — reads Yelp JSONL and produces to Kafka topic (e.g., raw_reviews).

kafka-spark.ipynb — consumes from Kafka, runs sentiment, and writes to ES (or back to Kafka as enriched_reviews).

elasticsearch-stream.ipynb — bulk loads businesses data into ES and/or streams reviews to ES.

updatemongo.ipynb — reads MongoDB, computes sentiment, updates docs in place.

enrichment.txt — ES API calls for mapping + enrich policy + pipeline.

Dashboard.png, New-orleans.png, Phily.png — Kibana snapshots.