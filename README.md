# Secure Cloud File Storage Using Amazon S3

## Project Overview

This project demonstrates how to create and manage secure cloud storage using Amazon Simple Storage Service (Amazon S3).

The goal was to gain hands-on experience with storing files, controlling access, protecting data through encryption, managing object versions, and understanding lifecycle management in AWS.

## AWS Services and Technologies

- Amazon S3
- AWS Identity and Access Management (IAM)
- S3 Bucket Policies
- S3 Versioning
- S3 Lifecycle Management
- Server-Side Encryption (SSE-S3)
- JSON

## Project Objectives

1. Create an Amazon S3 bucket.
2. Upload and download files.
3. Configure secure storage settings.
4. Enable object versioning.
5. Protect the bucket from public access.
6. Apply a bucket policy requiring HTTPS.
7. Configure an S3 Lifecycle rule.
8. Practice retrieving older object versions.

## Implementation

### 1. Creating the S3 Bucket

Created an Amazon S3 general-purpose bucket in the US East (Ohio) Region.

Configured the bucket to store documents securely and kept public access blocked.

### 2. Uploading and Downloading Objects

Uploaded a PDF document to the bucket and verified that it was stored successfully.

Downloaded the document to confirm that authorized access worked correctly.

### 3. Configuring S3 Versioning

Enabled S3 Versioning to preserve previous versions of objects.

Uploaded a document multiple times using the same object key and verified that Amazon S3 assigned unique version IDs.

Downloaded an earlier version and confirmed that it opened successfully.

### 4. Configuring Data Encryption

Verified that the bucket used server-side encryption with Amazon S3 managed keys (SSE-S3).

This protects stored objects through encryption at rest.

### 5. Configuring Bucket Security

Verified that Block Public Access was enabled.

Created a JSON bucket policy that denies requests when `aws:SecureTransport` is false.

This helps enforce HTTPS access to the bucket and its objects.

### 6. Configuring S3 Lifecycle Management

Created a lifecycle rule to transition eligible objects to S3 Standard-Infrequent Access after 30 days.

Reviewed storage transition and retrieval costs.

Disabled the lifecycle rule after configuration to avoid unnecessary automatic transitions during the learning project.

### 7. Testing and Verification

- Verified successful file uploads and downloads.
- Confirmed multiple versions of the same object.
- Successfully retrieved an older object version.
- Verified bucket encryption settings.
- Confirmed that Block Public Access was enabled.
- Saved the HTTPS-enforcement bucket policy.
- Confirmed that the lifecycle rule remained disabled.

## Security Considerations

The project follows foundational AWS security practices, including:

- Blocking public access.
- Encrypting objects at rest.
- Denying insecure transport.
- Preserving file versions for recovery.
- Reviewing possible charges before enabling lifecycle actions.

## Lessons Learned

Through this project, I gained practical experience managing Amazon S3 resources using the AWS Management Console.

I learned how bucket policies differ from IAM policies, how S3 Versioning protects against accidental overwrites, and how lifecycle rules can automate storage management.

I also gained a better understanding of securing cloud resources and considering costs when configuring AWS services.

## Project Evidence

Screenshots of the AWS configuration and successful tests will be added to the `screenshots/` folder.

Sensitive account information, private documents, and credentials will not be included.

## Future Improvements

- Explore IAM least-privilege permissions for S3 access.
- Practice additional recovery scenarios using non-sensitive test files.
- Explore S3 storage cost optimization.
- Integrate S3 with other AWS services.

## Project Status

Completed foundational Amazon S3 storage and security configuration, versioning tests, and lifecycle rule practice.

## Project Screenshots

The following screenshots show the AWS S3 configurations and hands-on exercises completed during this project.

1. [S3 Versioning](Screenshots/01-s3-versioning.png)
2. [S3 Default Encryption](Screenshots/02-s3-default-encryption.png)
3. [S3 Block Public Access](Screenshots/03-s3-block-public-access.png)
4. [S3 Bucket Policy](Screenshots/04-s3-bucket-policy.png)
5. [S3 Lifecycle Rule](Screenshots/05-s3-lifecycle-rule.png)
6. [S3 Object Version Details](Screenshots/06-s3-object-version-details.png)
