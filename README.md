# Secure Static Website on AWS

## Project Overview
This project demonstrates the deployment of a secure, high-availability static website using **AWS S3** for object storage and **Amazon CloudFront** as a Content Delivery Network (CDN). The primary focus was implementing cloud security best practices, specifically the "Principle of Least Privilege."

## Architecture Highlights
*   **Cloud Storage:** AWS S3 (configured with "Block All Public Access").
*   **Content Delivery:** Amazon CloudFront (Edge locations for low latency).
*   **Security Configuration:**
    *   **Origin Access Control (OAC):** A sophisticated security setting that restricts S3 bucket access solely to the CloudFront distribution.
    *   **HTTPS Enforcement:** Configured Viewer Protocol Policy to redirect all HTTP traffic to HTTPS, ensuring encryption in transit.
    *   **IAM Policies:** Applied a strict S3 Bucket Policy allowing read access only from the specific CloudFront ARN.

## Technical Steps Taken
1.  **Infrastructure Setup:** Provisioned an S3 bucket and uploaded static web assets.
2.  **Security Hardening:** Enabled "Block Public Access" at the bucket level to prevent data leaks.
3.  **CDN Deployment:** Deployed a CloudFront distribution to serve content globally.
4.  **Access Management:** Configured Origin Access Control (OAC) and updated S3 Bucket Policies to create a secure "trust relationship" between the CDN and the storage.
5.  **Verification:** Validated security controls by attempting direct bucket access (Denied) versus CDN access (Allowed).

## Skills Applied
*   AWS Core Services (S3, CloudFront)
*   IAM (Identity and Access Management) Policies
*   Cloud Security Posture Management
*   Web Protocols (HTTP/HTTPS)
