# Lakehouse Labs

![Python](https://img.shields.io/badge/Python-3.12_|_3.11-4B8BBE.svg?style=flat&logo=python&logoColor=FFD43B&labelColor=306998)
![Delta](https://img.shields.io/badge/Delta_Lake-3.2-00ACD4?style=flat&logo=delta&logoColor=00ACD4&labelColor=262A30)
![Iceberg](https://img.shields.io/badge/Iceberg-1.7-CEEBF6?style=flat&logo=apachespark&logoColor=CEEBF6&labelColor=2C7BBF)
![Hudi](https://img.shields.io/badge/Hudi-1.0-10B0F9?style=flat&logo=apachespark&logoColor=CEEBF6&labelColor=084D86)

![Metastore](https://img.shields.io/badge/Metastore-3.1-FDEE21?style=flat&logo=apachehive&logoColor=000000&labelColor=FDEE21)
![Trino](https://img.shields.io/badge/Presto-262A38?style=flat&logo=trino&logoColor=E8F5F5&labelColor=262A38)
![MinIO](https://img.shields.io/badge/MinIO-00091B?style=flat&logo=minio&logoColor=CF163D&labelColor=00091B)
![Docker](https://img.shields.io/badge/Docker-329DEE?style=flat&logo=docker&logoColor=white&labelColor=329DEE)

Experimentations with Delta, Iceberg, Hive, and other Big Data tools


## Tech Stack
- [PySpark](https://spark.apache.org/docs/latest/api/python/user_guide)
- [Delta.io](https://docs.delta.io/latest/quick-start.html)
- [Iceberg](https://iceberg.apache.org/spark-quickstart/)
- [Hudi](https://hudi.apache.org/docs/quick-start-guide/)
- [uv](https://docs.astral.sh/uv/concepts/projects/dependencies/)
- [Docker](https://docs.docker.com/get-docker/)

## Up and Running

### Developer Setup

**1.** Install `JDK` 11 or 17, Spark 3.5.x, and Hadoop:
```shell
sdk i java 17.0.13-librca
sdk i spark 3.5.3
sdk i hadoop 3.3.6
```

**2.** Install the dependencies on `pyproject.toml`:
```shell
uv sync
```

**3.** Activate the virtualenv created by `uv`:
```shell
source .venv/bin/activate
```

**4.** Spin up Minio (Object Storage), and Hive Metastore on Docker compose
```shell
docker compose up -d
```

## TODO
- [x] PEP-517: Packaging and dependency management with `uv`
- [x] Setup the infrastructure for an S3-compliant Object Storage ([Minio](https://github.com/minio/minio))
- [x] Setup the infrastructure for Hive Metastore
- [x] Write Delta Tables to MinIO/S3 with Hive Metastore
- [x] Write Iceberg Tables to MinIO/S3 with Hive Metastore
- [x] Write Hudi Tables to MinIO/S3 with Hive Metastore
- [x] Detect row-level changes to Delta Tables
- [ ] Detect row-level changes to Iceberg Tables
- [ ] Detect row-level changes to Hudi Tables

