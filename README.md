# simple-dockerapp-dotnet6

This repository contains a basic asp.net core 6.0 web app created as a docker image that can be published into the DeltaV Edge Environment. Using this template, you can quickly get started with developing apps for Edge!

# Contents

## Dockerfile

This file is located in `~/EdgeGateway.HelloWorld/Dockerfile`. This file can be used to generate a docker image from a `*.csproj` visual studio project.

To learn more about docker and dockerfiles, please refer to this page: [Dockerfile reference | Docker Docs](https://docs.docker.com/engine/reference/builder/)

## NGINX Config File (nginx.conf)

This file is located in `~/EdgeGateway.HelloWorld/nginx.conf`. This configuration file is used by nginx to render the published asp.net web app.

To know more about the nginx config file, please refer to this page: [Full Example Configuration | NGINX](https://www.nginx.com/resources/wiki/start/topics/examples/full/)

## EdgeGateway.HelloWorld Project

Solution file `EdgeGateway.HelloWorld.sln` and project file `~/EdgeGateway.HelloWorld/EdgeGateway.HelloWorld.csproj`.

This is the basic asp.net project we have set up to get started with. 

# How To

## Run the ASP.Net Project

1. Open the `EdgeGateway.HelloWorld.sln`.
2. Run the project `EdgeGateway.HelloWorld`.
3. You should be able to load the hello world app without any external dependencies/configuration.

## Build Docker Image and Run as Container

1. Using VSCode, locate the `Dockerfile`, right click, and select `Open in Integrated Terminal`.
2. Execute the command `docker build . -t simple-dockerapp-dotnet6`.
3. Docker will then try to download necessary images and build the app.
4. Execute the command `docker run --rm -d -p 8011:80/tcp simple-dockerapp-dotnet6:latest`.
5. Finally, open `http://localhost:8011/` from your browser.

NOTE: If necessary, please run VSCode with Administrator privilege.
