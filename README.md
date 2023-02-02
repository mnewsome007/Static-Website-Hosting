<h1>Static Website Hosting</h1>


<h2>Description</h2>
This project will guide you in hosting a static website on AWS. You will learn the steps of importing a domain name on AWS, creating a hosted zone and managing its DNS records, creating S3 buckets to host website pages, configuring Route 53 to link the domain name to the website, creating an SSL certificate for the website using AWS Certificate Manager (ACM), and creating CloudFront distributions to secure the website in HTTPS. By completing this project, you will have a comprehensive understanding of how to host a static website on AWS and the various tools and technologies involved in the process.
<br />

<h2>AWS Cloud Map</h2>
<p align="center">
<img src="https://i.imgur.com/MleqjqT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>Services Used</h2>

- <b>Route 53</b> 
- <b>CloudFront</b>
- <b>AWS Certificate Manager</b>
- <b>Amazon S3</b>

<h2>Environments Used </h2>

- <b>AWS Management Console</b>

<h2>Static Website Hosting walk-through:</h2>

- <b>Purchase a domain from AWS through Route 53 in the AWS Management Console</b>
- <b>Purchasing your domain through AWS automatically creates a hosted zone (container for your records)</b>
- <b>Within Amazon S3, create your main S3 bucket which will be named after your main URL domain; you will also choose your AWS region during this process</b>
- <b>You will now UPLOAD your own files to the S3 bucket </b>
- <b>Activate Static website hosting under the Static website hosting section in the Properties tab</b>
- <b>Verify the website by using the temporary URL of the S3 bucket</b>
- <b>Within Amazon S3, create a redirect S3 bucket, following the same process used to create the main S3 bucket. You will choose Redirect for the Hosting type and set Protocol to "None". The "Host name" should be filled with the target bucket website address(main S3 bucket domain); this redirects all traffic it recieves to the main S3 bucket previously created</b>
- <b>Now you will link the domain to the main S3 bucket using Route 53 by creating "A" DNS records inside your hosted zone </b>
- <b>You will follow the recent step to create the second DNS record for the redirect S3 bucket</b>
- <b>Create a SSL certificate for your website through AWS Certificate Manager, after the creation of the SSL certificate, validate the certificate</b>
- <b>CloudFront will no be introduced in order to deploy your website in HTTPS and allow faster access to the website for users</b>
- <b>Create the main CLoudFront distribution using the main S3 bucket URL</b>
- <b>Create the redirect CLoudFront distribution using the Origin domain for the URL of the S3 bucketL</b>
- <b>In your redirect S3 bucket, you can now change the protocol to "https"</b>
- <b>Finalize the A records in Route 53 so the web addresses route traffic created by CloudFront distributions</b>




<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
