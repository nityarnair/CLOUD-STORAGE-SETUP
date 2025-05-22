# CLOUD-STORAGE-SETUP

**COMPANY** : CODTECH IT SOLUTIONS

**NAME** : NITYA R NAIR

**INTERN ID** : CT04DK556

**DOMAIN** :  CLOUD COMPUTING

**DURATION** : 4 WEEKS 

**MENTOR** : NEELA SANTOSH

#DESCRIPTION :
For my first internship task, I learned how to set up and configure cloud storage on AWS. The goal was simple: create a storage bucket, upload a file, and make it publicly accessible. I chose Amazon S3 (Simple Storage Service) because it’s one of the most popular and easy-to-use cloud storage options.

1. Creating the S3 Bucket
I started by logging into the AWS Management Console and navigating to the S3 service. In S3, data is stored in containers called buckets. I clicked “Create bucket,” entered a unique name (S3 bucket names must be globally unique), selected my preferred AWS region, and left all other settings at their defaults. Versioning and encryption were turned off to keep things straightforward for this introductory task.

2. Uploading the File
Once the bucket was ready, I uploaded a two .jpg images. I opened the bucket, clicked “Upload,” selected the image from my local computer, and hit “Upload.” A progress bar appeared briefly, and then the file showed up in the bucket’s file list. This step confirmed that the bucket was working correctly.

3. Editing the Bucket Policy for Public Access
By default, new buckets and their contents are private. To share my image with anyone, I needed to change the bucket’s access policy. Instead of making the object public one by one, I edited the bucket policy so that all objects in the bucket became readable by anyone on the internet. Under the bucket’s Permissions tab, I pasted this simple JSON policy:
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicRead",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::codtechawsbucket/*"
    }
  ]
}
4. Verifying Public Access
After applying the bucket policy, I tested the public URL of my image. I copied the Object URL from the AWS console and opened it in an incognito browser window. The image displayed instantly, proving that anyone could now view or download the file without logging into AWS.

5. What I Learned

Bucket Creation: How to set up an S3 bucket with the correct naming and region.

File Upload: Using the S3 console to upload files easily.

Bucket Policies: Writing and applying a JSON policy to control access at the bucket level.

Testing Access: Verifying public permissions by using the object’s URL.

6. Why It Matters
Cloud storage is a fundamental skill for modern software development. Whether you need to host images for a website, store backup files, or share documents, understanding how to configure buckets, upload files, and manage access is essential. By practicing with a single image and a simple policy, I built a solid foundation to tackle more advanced scenarios—like private data, role-based access, and automated uploads.

Overall, this task gave me hands-on experience with AWS S3 and taught me how to manage cloud-based file storage securely and efficiently. I’m now ready to apply these skills to real-world projects that require reliable, scalable, and shareable file storage.

##OUTPUT

![Image](https://github.com/user-attachments/assets/1c88648a-e41e-4577-acd7-94eff8972e06)

![Image](https://github.com/user-attachments/assets/aad45cd5-02e4-4e7b-8f24-4d4e91790436)
