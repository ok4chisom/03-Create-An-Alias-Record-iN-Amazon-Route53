<h1>Creating An Alias Record in Amazon Rout 53</h1>
<!--
 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)
--!>
<h2>Description</h2>
A new startup business in North America has recruited you to help with the launch of a quick-access, low-cost static website. You've decided to complete this contract by hosting and deploying their website utilizing AWS S3
<br />


<h2>Solution Overview</h2>

- <b>Register a domain name (if you don't have one)
- Create an S3 bucket to host your website
- Link the S3 website to the domain name



<h2>Detailed Steps:</h2>

<p align="center">

Open Route 53

If you don't have a domain name registered, register a domain name using these steps https://aws.amazon.com/getting-started/hands-on/get-a-domain/ (Note that this cost $12 per year in the US). If you have a Domain name registered, skip to step 3.

Use the previous article "link" to create an s3 bucket configured to host a static website.
- Note that the bucket name must be the same as your domain or subdomain name. For example, if your domain name is test.example.com, your S3 bucket name should be "test.example.com"

Navigate back to Route 53

Select "Hosted zones": <br/>
<img src="https://i.imgur.com/kzea1kK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select your created "Hosted zone name" and select "Create record":  <br/>
<img src="hhttps://i.imgur.com/iusXmTn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Choose your record name (should be same the as your S3 bucket)

Toggle on Alias

Select Alias to S3 website Endpoint

Select your S3 bucket

Select your routing policy (in this case I used the Simple routing policy):  <br/>
<img src="https://i.imgur.com/ezN9iyq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Select create record

Now type in your domain name into the browser and you should be routed to your website <br/>
<img src="https://i.imgur.com/Ou1J7rp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
