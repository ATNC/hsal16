
## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- Docker and Docker Compose installed on your machine.
- Python and pip installed on your machine.

### Setting up MySQL with Slow Query Log

1. MySQL is run as a Docker service as defined in the `docker-compose.yml` file.
2. The MySQL configuration file `my.cnf` is mounted into the MySQL container. This file should contain the necessary configuration to enable the slow query log.

### Configuring ELK to Work with MySQL Slow Query Log

1. Logstash is configured to read the slow query log file from MySQL. This is defined in the `logstash.conf` file.
2. The slow query logs are then sent to Elasticsearch for indexing and storage.
3. Kibana is used to visualize the data stored in Elasticsearch.

### Configuring Graylog2 to Work with MySQL Slow Query Log

1. Graylog2 is also run as a Docker service as defined in the `docker-compose.yml` file.
2. Graylog2 is configured to receive logs from MySQL. This is done through the Graylog2 web interface.

## Running the Project

1. Clone the repository to your local machine.
2. Navigate to the project directory.
3. Run `docker-compose up` to start all the services.

## Built With

- [Python](https://www.python.org/)
- [ELK Stack](https://www.elastic.co/what-is/elk-stack)
- [Graylog2](https://www.graylog.org/)


## Accessing the Kibana Dashboard

Once all the services are up and running, you can access the Kibana dashboard by navigating to the following URL in your web browser:

[Kibana Dashboard](http://localhost:5601)