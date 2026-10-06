# AWS Project 1: Static Website Hosting on Amazon S3

Hey! This is my first practical cloud project where I set up and published a static website on AWS S3, then configured all the network and security settings to make it accessible online.

## 🛠️ What I Built
* **Amazon S3:** Created a bucket and enabled Static Website Hosting to serve the web pages.
* **IAM Policy:** Wrote a custom JSON Bucket Policy (`s3:GetObject`) to make the site publicly accessible to visitors.

---

## ⚙️ How I Implemented It
1. Created an S3 bucket named `lab-website-2026-ab1` in `us-east-1`.
2. Uploaded the `index.html` file to the bucket.
3. Disabled "Block Public Access" settings.
4. Added the following JSON Bucket Policy:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::lab-website-2026-ab1/*"
    }
  ]
}
Turned on Static Website Hosting under Bucket Properties and tested the live website URL.

🔍 Errors I Fixed
ARN Policy Error: I got an Action does not apply to any resource error at first because I forgot the /* at the end of the bucket ARN. Adding /* fixed object-level permissions.

Lab Permission Restrictions: Switched from a restricted lab environment to an independent AWS Free Tier account to avoid bucket policy limits.
