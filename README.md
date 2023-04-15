![1](https://user-images.githubusercontent.com/37349912/232197004-4d8890c0-9b1c-42d6-9b0b-d72d43ded83e.png)
![2](https://user-images.githubusercontent.com/37349912/232197005-4d0f5b81-1007-4779-be72-f7fdc4a7faca.png)
![3](https://user-images.githubusercontent.com/37349912/232196985-1c765c52-2829-40e7-9749-24709ddb90f5.png)
![4](https://user-images.githubusercontent.com/37349912/232196992-b22b2e54-d8b7-4374-ba92-dd6e96150ce8.png)
![5](https://user-images.githubusercontent.com/37349912/232196994-24ae351d-dc3f-4024-ad58-f8c99c4ae78e.png)
![6](https://user-images.githubusercontent.com/37349912/232197287-731c87df-90a3-4b4b-b161-3352c51af9d9.png)
![6](https://user-images.githubusercontent.com/37349912/232196996-f0d523ce-ead5-4df2-9fe7-6e15f223ca2b.png)
![7](https://user-images.githubusercontent.com/37349912/232196998-6999cdc2-e177-4806-82cd-86149838f00b.png)
![8](https://user-images.githubusercontent.com/37349912/232197000-51020946-8129-4f0e-9bda-f3391b823e57.png)
![9](https://user-images.githubusercontent.com/37349912/232197002-35f9dd87-5236-44a1-8a8d-a483cbc4e855.png)
![10](https://user-images.githubusercontent.com/37349912/232197003-ba7aee52-cf96-4f29-bca9-abd4e5008836.png)

# ATA-Capstone-Project

Follow the instructions in the course for completing the group Capstone project.

### Fill out the environment variables
Complete `setupEnvironment.sh` with the group repo name and the github username of the team member holding the repo.
Confirm these are in lower case.
The repo owner should confirm that all team members have been added to collaborate on the repo.

### To create the Lambda Example table in DynamoDB:

You must do this for the ServiceLambda to work!

```
aws cloudformation create-stack --stack-name lambda-table --template-body file://LambdaExampleTable.yml --capabilities CAPABILITY_IAM
```

### To deploy the Development Environment

Run `./deployDev.sh`

As you are taking a break from work, use the END LAB button in Vocareum instead of removing the pipeline each time.
The End Lab button will pause the lab and resources, not allowing the budget to be used. When you're ready to start again,
click the Start Lab button to begin again with renewed AWS credentials.

To tear down the deployment then run `./cleanupDev.sh`

### To deploy the CI/CD Pipeline

Fill out `setupEnvironment.sh` with the url of the github repo and the username (in all lowercase) of the 
team member who is maintaining the repo. Confirm that the team member has added your username as a contributor to the repo.

Run `./createPipeline.sh`

As you are taking a break from work, use the END LAB button in Vocareum instead of removing the pipeline each time.
The End Lab button will pause the lab and resources, not allowing the budget to be used. When you're ready to start again,
click the Start Lab button to begin again with renewed AWS credentials.

To teardown the pipeline, run `./cleanupPipeline.sh`


