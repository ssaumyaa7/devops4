# dynamiccluster
Task :
1. Create container image that’s has Linux and other basic configuration required to run Slave for Jenkins. ( example here we require kubectl to be configured )

2. When we launch the job it should automatically starts job on slave based on the label provided for dynamic approach.

3. Create a job chain of job1 & job2 using build pipeline plugin in Jenkins 

4. Job1 : Pull the Github repository automatically when some developers push repository to Github and perform the following operations as:

5. Job2 : Launch the application on the top of Kubernetes cluster performing following operations:
        If launching first time then create a deployment of the pod using the image created in the previous job. Else if deployment already exists then do rollout of the existing pod making zero downtime for the user.
        If Application created first time, then Expose the application. Else don’t expose it.
