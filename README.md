# docker-introduction

- Docker definition (GSP055) - https://www.cloudskillsboost.google/focuses/1029?parent=catalog
Docker is an open platform for developing, shipping, and running applications. With Docker, you can separate your applications from your infrastructure and treat your infrastructure like a managed application. Docker helps you ship code faster, test faster, deploy faster, and shorten the cycle between writing code and running code.

Docker does this by combining kernel containerization features with workflows and tooling that helps you manage and deploy your applications.

Dockerfile explanation : 
- The initial line specifies the base parent image, which in this case is the official Docker image for node version long term support (lts).
- In the second, is set the working (current) directory of the container.
- In the third, define to add the current directory's contents (indicated by the "." ) into the container.
- Then expose the container's port so it can accept connections on that port and finally run the 'node' command to start the application.


-- Build the container using this command :
docker build -t node-app:0.1 .

-- run the container using this command :
docker run -p 4000:80 --name my-app node-app:0.1

"The --name flag allows you to name the container if you like. The -p instructs Docker to map the host's port 4000 to the container's port 80. Now you can reach the server at http://localhost:4000. Without port mapping, you would not be able to reach the container at localhost."