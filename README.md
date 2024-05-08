# DevOps Internship Assignment Documentation

## Introduction
This documentation outlines the steps taken to complete the DevOps internship assignment, focusing on the technical implementation aspects. The assignment involved setting up a GitOps pipeline using Argo CD for continuous deployment and Argo Rollouts for advanced deployment strategies within an AWS EKS Kubernetes environment. The Tetris game was Dockerized and deployed to the cluster, showcasing the use of cloud-native technologies for automated deployment and management.

## Task 1: Setup and Configuration
### 1.1 Create a GitRepository
- Created a GitHub repository https://github.com/AreebAbdulGhani/tetris-game to host the source code for the Tetris game.

### 1.2 Install Argo CD on Your Kubernetes Cluster
- Utilized AWS EKS to create a Kubernetes cluster with the latest Kubernetes version (1.29).
- Added several IAM roles for the cluster, ensuring proper permissions for service operations.
- Created a node group in the AWS EKS cluster using EC2 t3.medium instances, meeting the resource requirements of Argo CD.
- Configured public subnets and used a load balancer for external access.

### 1.3 Install Argo Rollouts
- Installed the Argo Rollouts controller in the Kubernetes cluster, following the official guide.

## Task 2: Creating the GitOps Pipeline
### 2.1 Dockerize the Application
- Developed a Dockerfile for the Tetris game application, ensuring portability and ease of deployment.
- Built Docker images for the Tetris game and pushed them to the Docker Hub repository https://hub.docker.com/u/areeb01
### 2.2 Deploy the Application Using Argo CD
- Modified the Kubernetes manifests in the GitHub repository to use the Docker image.
- Installed Argo CD on the Kubernetes cluster and connected it to the https://github.com/AreebAbdulGhani/tetris-game
- Configured Argo CD to monitor the repository and automatically deploy changes to the Kubernetes cluster.

## Task 3: Implementing a Canary Release with Argo Rollouts
### 3.1 Define a Rollout Strategy
- Modified the application's deployment to use Argo Rollouts, specifying a canary release strategy in the rollout definition.

### 3.2 Trigger a Rollout
- Updated the Docker image to a newer version (areeb01/tetris-app-v2) and pushed it to https://hub.docker.com/u/areeb01
- Updated the rollout definition to use the new image, triggering a rollout of the newer version.

### 3.3 Monitor the Rollout
- Leveraged Argo Rollouts to monitor the deployment of the new version, ensuring the canary release successfully completed.

## Task 4: Documentation and Cleanup
### 4.1 Document the Process
- Provided a detailed summary of the technical implementation, highlighting the setup of AWS EKS, IAM roles, Dockerization, and deployment using Argo CD and Argo Rollouts.
- Addressed challenges faced during IAM policy creation and resolution steps taken.

### 4.2 Clean Up
- Described the process to cleanly remove all resources created during the assignment from the Kubernetes cluster, emphasizing proper resource management and cleanup practices.

## Conclusion
The assignment demonstrated proficiency in deploying cloud-native applications using Kubernetes, GitOps principles, and tools like Argo CD and Argo Rollouts. Despite challenges, effective problem-solving skills were employed to ensure successful completion.

## Acknowledgements
Thank you for the opportunity to complete this assignment. The experience gained will be valuable in contributing to future projects and collaborations.

---
