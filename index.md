---
layout: default
title: Home
nav_order: 1
description: "Face Recognition ETL API Get Started Guide."
permalink: /
---

# Face Recognition API
The API uses state of the art facial recognition technology from Azure Face 1.0 API. Our API works as a bridge between your API and the Azure to improve the performance of your app by simplifying the API, improving the quality of results, and removing unnecessary fields. It is quick and easy to integrate, the API is developed keeping business first ideology.

# Microsoft Face API Reference
[You can find original API here.](https://azure.microsoft.com/en-us/services/cognitive-services/face/)

## Getting started

### Dependencies
The API uses NodeJS and Express and is hosted over 4000 port if run on local machine.
- Node JS: 10.16.3
- Axios: 0.21.0
- Body Parser: 1.19.0
- Express: 4.17.1
- Multer: 1.4.2

### Quick start: Local Installation

1. Register and enable Microsoft Azure face API, and Azure Storage Blob
2. Set the following environment variables:
  - AZURE_ENDPOINT: It is url given by azure face api while registering. It might look like: <em>https://project_name.cognitiveservices.azure.com/face/v1.0/</em>
  - AZURE_KEY1: It is the key1 provided by the Azure Face API
  - AZURE_STORAGE_CONNECTION_STRING: It is the connection string provided by Azure Storage Blob API.
  - STATIC_FOLDER: It is the folder inside your project where you want to store images temporarily before it will uploaded to the Azure server.
  - STORAGE_CONTAINER: It is the name of storage container in azure where all the images will be uploaded.
3. Use <code>npm i</code> to install the dependencies.
4. Use <code>node index</code> to run the app.

A handy guide on how to setup environment variable into your current operating system is [here](https://www.poftut.com/how-to-set-environment-variables-for-linux-windows-bsd-and-macosx/).

## Features
- Filtered Face Detection API: You can reduce the noises and get what you really need while detecting the faces. You can filter the detection API data in order to reduce the bandwidth usage of the client. 
- Merged Face Identification and Similar API: We merged the APIs so that you can seemlessly get the results, we will find all the similar faces in the all the face list and large face list you've and we can implicitly indentify the people if you don't know which person group they belong to. It means you can concentrate more time on coding the features than finding which person list the photo belongs to. 
- Brand New Face Verification: Now you can upload images and verify if the photos have identical person or you can also provide faceIds or faceId and personId to achieve the same task.
- Train all FaceLists or LargeFaceLists in just a single request. 
- Get all the features of Azure Face API with some additional endpoints which can make tasks easier for the developers to easily integrate to the app.
- Free to use: The Azure ETL API is free to use and can be easily hosted on your personal cloud without any cost. 
- Space for customization: You can scale the usage of API by sending your Azure API key which is optinal parameter of the ETL API which can basically allow you to make user concentric content with a room for scalability.

### API Basics

- [Get Started with API Basics]({{ site.baseurl }}{% link docs/basics.md %})

---

## About the Author

[Prashant Pandey](https://prashant-pandey.github.io).

##### About the Jekyll Theme

Just the Docs: [GitHub repo](https://github.com/pmarsceill/just-the-docs).
Thanks to the author Patrick Marsceill for this jump start.