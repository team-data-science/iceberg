
# Iceberg Data Engineering Project

This project demonstrates how to use Apache Iceberg with Spark and MinIO for modern data lake management and analytics. It provides a local environment for experimenting with Iceberg tables, Spark SQL, and S3-compatible object storage using Docker Compose.

## Project Structure

- `docker-compose.yml`: Defines the services for Spark, Iceberg REST catalog, MinIO (S3-compatible storage), and MinIO client.
- `data/`: Contains sample datasets in Parquet and CSV formats for use in the warehouse.
- `warehouse/`: The storage location for tables of the default Spark catalog (not managed by Iceberg).
- `notebooks/`: Jupyter notebooks for interactive exploration and learning.

## How to Run

1. **Start the environment:**
   Open a terminal in the project directory and run:
   
   ```sh
   docker-compose up
   ```

2. **Access Jupyter Notebook:**
   - Once the containers are running, open [http://localhost:8888](http://localhost:8888) in your browser.
   - Use the token printed in the terminal to log in.
   - Explore the notebooks in the `notebooks/` folder to learn about Iceberg and Spark operations.

3. **Interact with Spark and Iceberg:**
   - Spark is available on ports 4040, 4041 (UI), 10000, 10001 (Thrift), and 8080 (REST).
   - MinIO Console is available at [http://localhost:9001](http://localhost:9001) (user: `admin`, password: `password`).

## Explanations

- **Apache Iceberg**: An open table format for huge analytic datasets, enabling features like time travel, schema evolution, and partitioning.
- **Spark**: Used for processing and querying data stored in Iceberg tables.
- **MinIO**: Provides S3-compatible object storage for the warehouse, simulating cloud storage locally.
- **Iceberg REST Catalog**: Manages table metadata and enables Spark to interact with Iceberg tables over REST.

This setup is ideal for learning, prototyping, and testing data engineering workflows with modern open-source tools.
