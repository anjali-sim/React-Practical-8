# React-Practical-8

I have deployed my Practical-7 using AWS S3 in this.

### What is AWS?
- The full form of AWS is Amazon Web Services. It is a platform that offers flexible, reliable, scalable, easy-to-use and, cost-effective cloud computing solutions.
AWS is a comprehensive, easy to use computing platform offered Amazon. 
- The platform is developed with a combination of infrastructure as a service (IaaS), platform as a service (PaaS) and packaged software as a service (SaaS) offerings.

### What is S3?
- It stands for Simple Storage Service. Amazon S3 is an object storage service that stores data as objects within buckets. 
- A bucket is a container for objects stored in Amazon S3. You can store any number of objects in a bucket. Every object is contained in a bucket. 
- An object is a file and any metadata that describes the file. It enables you to store and retrieve any amount of data at any toime or place, giving developers access to highly scalable, reliable, fast and inexpensive data storage.

### What is CloudFront?
- Amazon CloudFront is a web service that speeds up distribution of your static and dynamic web content, such as .html, .css, .js, and image files, to your users. CloudFront delivers your content through a worldwide network of data centers called edge locations. 
- It is a globally-distributed network, which securely transfers content such as software, SDK's, videos, etc. to the clients with high transfer speed.

## :sparkles: Steps to deploy react application using S3
1. Create S3 Bucket in AWS.
![Screenshot from 2023-06-05 16-37-42](https://github.com/anjali-sim/React-Practical-8/assets/122269010/2508feea-f866-404a-affe-0843c9f8c8ac)

![Screenshot from 2023-06-05 16-39-25](https://github.com/anjali-sim/React-Practical-8/assets/122269010/f89bdcc0-cd6a-42bf-b44f-97880b390ada)
2. Configure S3 bucket to host a Static Website.
- Enable Static Website Hosting  
- Select Host a Static Website and use index.html as the Index Document and the Error Document
![Screenshot from 2023-06-05 17-03-43](https://github.com/anjali-sim/React-Practical-8/assets/122269010/08230e8e-c635-4bf6-9184-a5d99d264586)
![Screenshot from 2023-06-05 17-05-53](https://github.com/anjali-sim/React-Practical-8/assets/122269010/dcfc3f78-ec1c-491c-baf4-6e6de065c320)
3. Configure settings and permissions.
- Disable BLOCK PUBLIC ACCESS permissions
- Give access to the world to read the contents of your S3 bucket
- Go to your S3 Bucket, under Permissions, and find Bucket Policy and edit it.
![Screenshot from 2023-06-05 17-05-09](https://github.com/anjali-sim/React-Practical-8/assets/122269010/cf363a44-dd22-4ab6-b107-206176eb4b91)
4. Manually publish React App to S3 then access it with a public link.
- Create a Production build for your React App — you could use the npm run build
- Now you could upload ONLY the CONTENTS of your build folder into the S3 bucket, manually
- Then use the public link to access your React App found under Properties all the way at the bottom
![Screenshot from 2023-06-05 18-34-40](https://github.com/anjali-sim/React-Practical-8/assets/122269010/bca8c2ef-fe88-4314-b705-e61926f5fd62)
![Screenshot from 2023-06-05 18-34-49](https://github.com/anjali-sim/React-Practical-8/assets/122269010/4c54101d-24da-478c-8a1e-4adb13170c3e)

## :sparkles: Steps to deploy react application using CloudFront
1. Go to CloudFront Service and click on Create Distribution.
![Screenshot from 2023-06-06 19-35-59](https://github.com/anjali-sim/React-Practical-8/assets/122269010/e8165df8-45fa-4cb2-9945-2c13f9c9fe13)
2. Then, click the bucket as the Origin Domain from the dropdown. And specify the Default root object to index.html and specify other configurations if you want any.
3. After configuring all the options, finally click on Create Distribution and wait for a while and the deployed link is provided.
![Screenshot from 2023-06-06 19-39-11](https://github.com/anjali-sim/React-Practical-8/assets/122269010/0b32a5e5-a3b1-4bcc-b9da-ddc2a5218a70)

## :rocket: Deployed Link
- <b>Using S3</b>: http://practical-8.s3-website.ap-south-1.amazonaws.com/
- <b>Using CloudFront</b>: https://d9lppe5zpyt2c.cloudfront.net/
