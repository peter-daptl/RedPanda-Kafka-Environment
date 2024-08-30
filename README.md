## RedPandas Kafka Environment

This repository provides a Docker Compose setup for a RedPanda Kafka environment.

**Features:**

* Based on the RedPandas Quickstart guide: [https://docs.redpanda.com/current/get-started/quick-start/](https://docs.redpanda.com/current/get-started/quick-start/)
* Modified to include PLAINTEXT protocols for connection from other Docker containers using `host.docker.internal`.

**Intended Use:**

* This repository is designed to be used with two projects:
    * `airflow-demo` (Kafka branch): [https://github.com/peter-daptl/airflow-demo](https://github.com/peter-daptl/airflow-demo)
    * (Future) Kafka consumer demo (details to come)
* A separate `.sh` script includes `docker-compose exec` commands to create topics used by these applications.

**Getting Started:**

1. Clone this repository.
2. Run `docker-compose up -d` to start the RedPanda container.
3. Use the provided `.sh` script to create topics for your applications.

**Connecting from Other Containers:**

This setup uses the PLAINTEXT protocol, allowing other Docker containers to connect to RedPanda using the hostname `host.docker.internal:29097`.

**Note:**

* This README provides a basic overview. Please refer to the RedPanda documentation for detailed configuration options.

**Additional Resources:**

* RedPanda documentation: [https://docs.redpanda.com/current/](https://docs.redpanda.com/current/)
