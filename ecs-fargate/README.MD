ECS FARGATE
===========

This example shows how to send ECS Fargate container logs to Coralogix using AWS FireLens with a custom Fluentd image.

The example depends on ECR to host a simple Node express dockerized app.

The example is built on top of [this blog post](https://medium.com/avmconsulting-blog/how-to-deploy-a-dockerised-node-js-application-on-aws-ecs-with-terraform-3e6bceb48785).

Quick start
1. npm install
2. aws ecr get-login-password --region eu-west-2 | docker login --username AWS --password-stdin 0..7.dkr.ecr.eu-west-2.amazonaws.com
3. docker build --platform=linux/amd64 -t my-first-ecr-repo . && docker tag my-first-ecr-repo:latest 0..7.dkr.ecr.eu-west-2.amazonaws.com/my-first-ecr-repo:latest && docker push 0..7.dkr.ecr.eu-west-2.amazonaws.com/my-first-ecr-repo:latest
4. terraform init
5. terraform apply

