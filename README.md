# git-hub-capstone-prj
This project focuses on developing a static website using HTML, CSS, and optional JavaScript, setting up GitHub Actions to automate deployment, and deploying the site to a cloud platform (AWS S3). 


## PROJECT STRUCTURE 

#### Create a new repository on GitHub - - **TechOps-Solutions**
![image](https://github.com/user-attachments/assets/01b70f20-d98d-4724-b273-9484b08e9154)


#### Clone the repository locally
![image](https://github.com/user-attachments/assets/76aa30f7-954c-47ae-89d7-88919f11627a)


#### Change directory (cd) into into the clone respository. - **cd Techops-solutions** -
![image](https://github.com/user-attachments/assets/6bbacf93-82a9-4af2-82b6-60bf134aad21)


#### Create index.html as the main page: **vim index.html** -  Add the following code into it.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TechOps Solutions</title>
  <link rel="stylesheet" href="assets/css/styles.css">
</head>
<body>
  <header>
    <h1>Welcome to TechOps Solutions</h1>
    <nav>
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="contact.html">Contact</a>
    </nav>
  </header>
  <main>
    <p>Your go-to platform for tech solutions.</p>
  </main>
  <footer>
    <p>&copy; 2024 TechOps Solutions. All rights reserved.</p>
  </footer>
  <script src="assets/js/script.js"></script>
</body>
</html>

![image](https://github.com/user-attachments/assets/04888235-773f-4bdf-b797-95984558fb35)


####  Add Styling with CSS: Create assets/css/styles.css. 
![image](https://github.com/user-attachments/assets/31900781-beea-4cea-80e8-5cae8cb40282)


#### Create assets/js/script.js: Add the following code into it 
// Example: Add a dynamic greeting to the console
console.log("Welcome to TechOps Solutions!");


## Configure AWS S3 for Deployment
#### Go to the AWS Management Console.
#### Create an S3 bucket ( techops-solutions-bucket).
#### Enable Static Website Hosting in bucket properties and provide an index document (index.html).
![image](https://github.com/user-attachments/assets/dc36b40d-4e6a-469f-bee3-f9a828651a12)
![image](https://github.com/user-attachments/assets/566fd4a8-692f-4bfa-a080-43cbadd4445c)
![image](https://github.com/user-attachments/assets/6e4555ba-bce4-4130-ac2d-158640c2516d)


#### Set Bucket Permissions: Make the bucket publicly accessible by adding a bucket policy:
![image](https://github.com/user-attachments/assets/ace843cb-5cff-4e05-bb6d-e8f33ba9c4f0)


## Generate AWS Credentials:
#### Generate an IAM user with programmatic access.
![image](https://github.com/user-attachments/assets/fd64ecf8-e844-472e-a465-f0c7350f2522)

#### Assign the AmazonS3FullAccess policy to the user.
![image](https://github.com/user-attachments/assets/3908a3de-d1ad-469d-afed-71eeec9ddd2a)


#### Save the Access Key ID and Secret Access Key.
![image](https://github.com/user-attachments/assets/2d2b7493-f480-4464-94d4-e89f62b7659b)


## Set Up GitHub Actions for CI/CD

#### Create the Workflow File: ** .github/workflows/deploy.yml: **
![image](https://github.com/user-attachments/assets/8fa2d40c-3377-4613-8473-a40d1706af42)


## Add Secrets to GitHub

#### Go to your GitHub repository.
#### Navigate to Settings > Secrets and variables > Actions.
#### Add the following secrets:
#### AWS_ACCESS_KEY_ID: Your AWS Access Key ID.
#### AWS_SECRET_ACCESS_KEY: Your AWS Secret Access Key.
![image](https://github.com/user-attachments/assets/efee9db7-0cd1-4d36-aec1-15bae3a6dc1a)


## Test the CI/CD Pipeline

#### Run the command: **git add .**  --  **git commit -m "Update static website"** -- **git push origin main**


#### Go to the Actions tab in your GitHub repository to check the workflow progress.
![image](https://github.com/user-attachments/assets/b11c7720-df02-4de8-a199-6abb2110a86d)



#### Once complete, verify the deployment by visiting the S3 bucket URL.
![image](https://github.com/user-attachments/assets/543c247a-0f8b-4c87-92b7-38a1bf4fe626)



























































































































































