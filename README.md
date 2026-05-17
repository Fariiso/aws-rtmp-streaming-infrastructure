# AWS Live Media Streaming Architecture

A high-performance, real-time media ingestion and streaming architecture deployed on AWS utilizing the Nginx RTMP module and Amazon S3 storage bucket lifecycle rules.

## System Architecture Diagram
[Insert your draw.io or Lucidchart architectural diagram link here]

## Infrastructure Breakdown
- **Compute Instance:** AWS EC2 Running Ubuntu Server (t3.micro)
- **Ingestion Protocol:** RTMP (Real-Time Messaging Protocol) over Port 1935
- **Media Storage:** Amazon S3 Object Storage for broadcast file archival
- **Edge Layer:** Nginx Web Server acting as the ingestion core and data processor

##  Security Configuration
- **Stateful Firewalls:** Configured AWS Security Groups to explicitly limit inbound port 1935 intake strictly to the source broadcast laptop IP address.
- **Port Management:** Standard HTTP traffic exposed on Port 80, with administrative access secured via SSH on Port 22.

## Core Configuration Files
- `rtmp_nginx_backup.conf`: Holds the core Nginx process orchestration block and live ingest directives.
