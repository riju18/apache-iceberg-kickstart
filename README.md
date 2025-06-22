# apache-iceberg-kickstart

# 🧊 Apache Iceberg Exploration

Welcome to my personal journey exploring **Apache Iceberg**, an open table format for large-scale analytics datasets. This repository tracks my experiments, findings, setup steps, and integration with other tools like `Spark, Nessie, MinIO, zeppelin and dremio`.

---

## 📚 What is Apache Iceberg?

Apache Iceberg is an open table format designed for huge analytic datasets. It brings SQL table-like features to data lakes: ACID transactions, schema evolution, time travel, partition evolution, and hidden partitioning.

[Iceberg doc](https://iceberg.apache.org/docs/nightly/spark-getting-started/)

---

## 🛠️ My Setup

### 🔧 Technologies Used

- **Apache Spark** (Data processing)
- **Apache Iceberg** (table format)
- **Project Nessie** (catalog service for versioned data)
- **MinIO** (S3-compatible object storage)
- **Docker Compose** (for local orchestration)
- **Zeppelin** (interactive notebooks)
- **dremio** (Lakehouse platform)

---

## 📁 Repo Structure

```bash
.
├── docker-compose.yml/               # Docker Compose setup
├── zeppelin_notebooks/               # JupyterLab / Zeppelin notebooks
├── zeppelin_conf/                    # zeppelin interpretor conf
├── spark/                            # spark bin
├── spark-jars/                       # necessary spark bundles
```

# ⚙️ Installation Guide

This guide sets up a local Apache Iceberg environment using Docker Compose. It includes `Spark, Nessie (for catalog/versioning), MinIO (as S3-compatible storage), dremio, zeppelin, spark with jupyter notebook`.

---

### 🧩 Prerequisites

Make sure you have the following installed:

- Docker
- Docker Compose
- Git
- Python

---

### 📁 Clone the Repository

```sh
git clone git@github.com:riju18/apache-iceberg-kickstart.git
```

```sh
cd apache-iceberg-kickstart
```

### Download spark
- download via this [link](https://drive.google.com/drive/u/0/folders/1-I2ggr-OfDk7dMFaYHy0mpFU4Kg9wqQb)
- and place it into root dir

### 🐳 Start the Docker Environment

```sh
docker compose up

or,

docker compose up -d
```

- This will start:
    
    - Zeppelin: `localhost:8090`
    - Nessie: `localhost:19120`
    - MinIO: `localhost:9001`
    - dremio: `localhost:9047`
    - jupyterlab: `localhost:8888`

### 🗃️ Initialize MinIO Buckets

- minio will come up with 4 preinitialized buckets.

    - datalake
    - datalakehouse
    - seed
    - warehouse

- Log in using:

    - Username: `admin`
    - Password: `password`

