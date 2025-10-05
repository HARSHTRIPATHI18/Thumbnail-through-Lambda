
#  Serverless Thumbnail Generator using AWS

A serverless image thumbnail generator built with AWS services. Automatically resizes images uploaded to S3 using AWS Lambda and stores the thumbnails in a separate bucket.

## 🚀 Features

- 📥 Upload original images to S3
- ⚙️ Automatically triggered by S3 events
- 🖼️ Generates 128x128 pixel thumbnails using Python (Pillow)
- 💾 Stores thumbnails in a separate S3 bucket
- 📊 Logs processing to CloudWatch
- 🔒 Follows least-privilege IAM practices

---

## 🧱 Architecture

```mermaid
graph TD
    A[User Uploads Image to S3 (Bucket A)] --> B(Lambda Triggered by S3 Event)
    B --> C[Lambda Resizes Image]
    C --> D[Thumbnail Stored in S3 (Bucket B)]
    B --> E[Logs to CloudWatch]
