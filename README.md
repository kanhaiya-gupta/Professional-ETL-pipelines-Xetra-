# Xetra ETL Pipeline

This project implements a production-ready ETL (Extract, Transform, Load) pipeline in Python to process the Xetra dataset from Deutsche Börse Group. Xetra stands for Exchange Electronic Trading and it is the trading platform of the Deutsche Börse Group. The pipeline extracts trading data from a public AWS S3 bucket, applies transformations to generate a report, and loads the results into a target AWS S3 bucket.

## Project Overview

### Tools & Technologies
- **Python 3.9**: Core language for the pipeline.
- **Jupyter Notebook**: Used for development and testing.
- **Git & GitHub**: Version control and repository hosting.
- **Visual Studio Code**: Recommended editor for development.
- **Docker & Docker Hub**: Containerization and image distribution.
- **Python Packages**:
  - `pandas`: Data manipulation and transformation.
  - `boto3`: AWS S3 interaction.
  - `pyyaml`: Configuration file parsing.
  - `awscli`: AWS command-line tools.
  - `jupyter`: Notebook support.
  - `pylint`: Code linting.
  - `moto`: Mocking AWS services for testing.
  - `coverage`: Test coverage reporting.
  - `memory-profiler`: Performance profiling.

### Programming Approaches
- **Functional Programming**: Modular functions for data processing.
- **Object-Oriented Programming**: Structured classes for pipeline components.

### Features & Best Practices
- Clean, modular code adhering to design principles.
- Virtual environment setup for dependency isolation.
- Organized project structure.
- YAML-based configuration management.
- Comprehensive logging.
- Robust exception handling.
- Linting with `pylint` for code quality.
- Dependency management with `requirements.txt`.
- Performance optimization using `memory-profiler`.
- Unit and integration tests with `moto` and `coverage`.
- Dockerized application for easy deployment.

## Project Goal
The pipeline:
- Extracts the Xetra dataset (minute-by-minute trading data) from a public AWS S3 source bucket.
- Transforms the data to create a report.
- Loads the transformed data into a target AWS S3 bucket.
- Is designed for deployment in containerized environments like Kubernetes, with orchestration via tools such as Argo Workflows or Apache Airflow.

## Repository Contents
- **Source Code**: Python scripts and modules for the ETL pipeline.
- **Dockerfile**: For building the container image.
- **Requirements**: List of dependencies in `requirements.txt`.
- **Tests**: Unit and integration tests.
- **Configuration**: Sample YAML config files.
- **Notebooks**: Jupyter notebooks for development and exploration.

## Setup & Usage
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/kanhaiya-gupta/Professional-ETL-pipelines-Xetra-.git
   cd Professional-ETL-pipelines-Xetra-
   ```
2. **Set Up Virtual Environment**:
   ```bash
   python3.9 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```
3. **Configure**:
   - Update the `config.yaml` file with your AWS credentials and S3 bucket details.
4. **Run Locally**:
   ```bash
   python etl_pipeline.py
   ```
5. **Build Docker Image**:
   ```bash
   docker build -t xetra-etl-pipeline .
   ```
6. **Run with Docker**:
   ```bash
   docker run -e AWS_ACCESS_KEY_ID=<key> -e AWS_SECRET_ACCESS_KEY=<secret> xetra-etl-pipeline
   ```

## Deployment
- **GitHub**: Code is hosted at [https://github.com/kanhaiya-gupta/Professional-ETL-pipelines-Xetra-](https://github.com/kanhaiya-gupta/Professional-ETL-pipelines-Xetra-).
- **Docker Hub**: Pre-built image available (replace with actual Docker Hub link once published).
- **Production**: Deploy to Kubernetes or similar platforms with orchestration tools like Argo Workflows or Apache Airflow.

## About the Xetra Dataset
Xetra (Exchange Electronic Trading) is a trading platform by Deutsche Börse Group. This project uses its publicly available dataset, updated near real-time on a minute-by-minute basis, stored in an AWS S3 bucket.

## Contributing
Feel free to fork the repository, submit issues, or create pull requests to enhance the pipeline.
