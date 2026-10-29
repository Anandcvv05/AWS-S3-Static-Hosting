# AWS S3 Static Website Hosting

## Project Overview

This project demonstrates how to host a static website using **Amazon Simple Storage Service (Amazon S3)**. The website is built using HTML and CSS and is accessible through the S3 static website endpoint.

The project demonstrates the fundamentals of AWS cloud storage, static website hosting, bucket permissions, and public access configuration.

## Objectives

- Host a static website using Amazon S3.
- Upload HTML and CSS files to an S3 bucket.
- Configure static website hosting.
- Understand S3 bucket policies and public access settings.
- Access the website through its S3 website endpoint.

## Technologies Used

- **Amazon S3** – Stores and hosts the website files.
- **HTML5** – Structures the website content.
- **CSS3** – Styles the website.
- **AWS IAM and bucket policies** – Control access to AWS resources.
- **GitHub** – Stores project source code and documentation.

## Project Architecture

```text
                 User / Web Browser
                         |
                         v
                 S3 Website Endpoint
                         |
                         v
                  Amazon S3 Bucket
                         |
                +--------+--------+
                |                 |
                v                 v
             index.html        style.css
```

## Project Structure

```text
aws-s3-static-hosting/
├── index.html
├── style.css
└── README.md
```

## Implementation Steps

### 1. Create an S3 Bucket

1. Sign in to the [AWS Management Console](https://console.aws.amazon.com/).
2. Open Amazon S3.
3. Create a bucket with a globally unique name.
4. Select an AWS Region.
5. Keep the bucket dedicated to the public website.

### 2. Create the Website Files

Create an `index.html` file containing the website structure and a `style.css` file containing the design and layout.

### 3. Upload Files to S3

1. Open the S3 bucket.
2. Select **Upload**.
3. Upload `index.html` and `style.css`.
4. Confirm that both files appear in the bucket's Objects tab.

### 4. Enable Static Website Hosting

1. Open the bucket's **Properties** tab.
2. Find **Static website hosting**.
3. Click **Edit** and enable website hosting.
4. Select **Host a static website**.
5. Set the index document to `index.html`.
6. Save the configuration.

### 5. Configure Public Access

For this demonstration, configure public read access only for the dedicated website bucket.

1. Open the bucket's Permissions tab.
2. Adjust the Block Public Access settings if necessary.
3. Add an S3 bucket policy that permits `s3:GetObject` on the website objects.
4. Save the policy.

Public access should be enabled only for files intended to be publicly available. Never upload confidential information or credentials.

### 6. Test the Website

Open the **Bucket website endpoint** from the Static website hosting section.

Verify that:
- The homepage loads successfully.
- The CSS styles are applied.
- The page content and links display correctly.

## Website Preview

The website includes:

- A welcome heading for the AWS project.
- A description of the cloud hosting implementation.
- A link to Amazon S3.
- A footer identifying the project author.

## Live Website

**S3 Website URL:** [Replace this text with your actual S3 website endpoint](http://aws-s3-static-cvv.s3-website-us-east-1.amazonaws.com).

## Key Learnings

- Understanding Amazon S3 buckets and objects.
- Hosting static websites without managing an EC2 server.
- Configuring static website hosting properties.
- Working with S3 bucket policies and public access controls.
- Deploying and testing a website on AWS.
- Documenting a cloud project using GitHub.

## Security Considerations

- Use a dedicated bucket for publicly accessible website content.
- Never store AWS access keys, passwords, or private files in the website bucket.
- Understand that S3 website endpoints use HTTP rather than HTTPS.
- For production websites, consider Amazon CloudFront with HTTPS and Origin Access Control to keep the S3 bucket private.

## Future Enhancements

- Configure Amazon CloudFront for HTTPS delivery.
- Add a custom domain using Amazon Route 53.
- Configure automated deployment from GitHub.
- Improve the website's responsive design.
- Add monitoring and logging where appropriate.

## Author

**CVV ANAND**

B.Tech Student – Artificial Intelligence and Machine Learning

GitHub: [Anandcvv05](https://github.com/Anandcvv05)

---

*This project was developed for learning and demonstrating AWS cloud hosting fundamentals.*
