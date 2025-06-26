# AWS Configuration

To ensure scalable data processing and cloud-based development, we used **Amazon Web Services (AWS)** as the platform for building and running our project: **Local Weather Trends Dashboard**. The configuration steps were completed using student accounts provided via the **AWS Educate program**, which allowed us to access various AWS services without incurring additional costs.

The main goal of using AWS was to process large datasets efficiently with **Apache Spark**, store them in the cloud using **Amazon S3**, and provide interactive analysis through **SageMaker Studio notebooks**. Below is a detailed overview of the configuration process along with visual confirmation for each step.

## 1. Creation of an EMR Cluster

We configured and launched an **Amazon EMR cluster** (Elastic MapReduce) designed for distributed big data processing using Apache Spark. The cluster was successfully created with appropriate settings and ready for use.

![EMR Cluster Successfully Created](./images/my_cluster_created.png)

## 2. Setup of SageMaker Studio

To enable interactive data exploration and coding, we set up **AWS SageMaker Studio**. This Jupyter-based development environment allows direct connection to the EMR cluster and integration with the S3 bucket. After setup, the workspace was functioning correctly, with active kernels and notebook support.

![SageMaker Studio Workspace Running](./images/sagemaker_studio_workspace.png)

## 3. EC2 Instance for Auxiliary Tasks

As a support tool for potential additional tasks (e.g., file transfer, manual script execution), we created an **EC2 instance**. Although not strictly required for running Spark jobs, it provided flexibility and an alternative environment for debugging or managing files.

![EC2 Instance Created](./images/ec2_instance_created.png)

## 4. Initial Cluster Connection without Code

Before deploying any code, we verified the connection between our development environment and the Spark cluster. This ensured that job submission and remote execution would be possible later.

![Empty Spark Cluster Connected to AWS](./images/empty_spark_cluster_connected.png)

## 5. Uploading Data to S3 Bucket

The weather datasets in CSV format were uploaded to a dedicated **Amazon S3 bucket**. S3 served as the main storage for both input files and (optionally) output data. This enabled the Spark jobs to access files efficiently in a distributed manner.

![Files Uploaded to S3 Bucket](./images/files_uploaded_to_bucket.png)

## 6. Deployment of Code to the Cluster

Once the infrastructure was in place, the Python scripts for data loading, cleaning, aggregation, and visualization were uploaded and linked to the EMR cluster. These scripts were prepared to run in Spark environments and included support for visualization modules.

![Code Deployed to AWS Cluster](./images/code_deployed_to_cluster.png)

## 7. Running Jupyter Notebook with Spark Jobs

Finally, we executed the notebook from within SageMaker Studio. The notebook was connected to the EMR cluster and successfully ran all code cells, producing aggregated statistics and plots from the weather data.

![Notebook Running with Results on AWS](./images/notebook_running_results.png)

---

This setup enabled fully cloud-based processing and analysis of weather data, leveraging distributed computing and modern cloud tools for efficient and reproducible results.
