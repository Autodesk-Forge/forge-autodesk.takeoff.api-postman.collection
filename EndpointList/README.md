# Autodesk Takeoff API List

![Platforms](https://img.shields.io/badge/Web-Windows|MacOS-lightgray.svg)
[![oAuth2](https://img.shields.io/badge/Authentication-v1-green.svg)](http://developer.autodesk.com/)
[![Data-Management](https://img.shields.io/badge/Data%20Management-v2-green.svg)](http://developer.autodesk.com/)
[![Autodesk-Takeoff](https://img.shields.io/badge/Autodesk%20Takeoff-v1-green.svg)](http://developer.autodesk.com/)

[![Postman](https://img.shields.io/badge/Postman-v8-orange.svg)](https://www.getpostman.com/)

![Beginner](https://img.shields.io/badge/Level-Beginner-green.svg)
[![License](https://img.shields.io/:license-MIT-blue.svg)](http://opensource.org/licenses/MIT)

This folder contains a Postman Collection that includes all the current Autodesk Takeoff API. The collection helps you easily test these endpoints.

![Collection](Img/collection.png)


## Instructions to run the Postman collection are as below:


### Prerequisites
- The API mainly focus on reading all the takeoff information from ACC project, before using the following APIs, user needs to activate and setup takeoff service, upload 3D models or 2D Sheets, create a couple of packages, takeoff types and takeoff items.

### Setup Postman environment and Authorization:
- Please setup the following environment vialables in **Pre-request Script** of the endpoint `Step 0: Reset the environment variables`, then run this endpoint: 
    - client_id:     Forge App Id.
    - client_secret: Forge App Secret.
    - hub_name: The name of ACC hub/account that you want to operate on.
    - project_name:  The project name that you want to operate on.

- Please add the Authorization for the collection, click **Edit Collection**, go to **Authorization** tab, make sure to use **OAuth 2.0** to get a 3 legged token of a user who has access to takeoff product, use it in the **Request Headers**.
![3leggedToken](Img/3leggedToken.png)
    - Callback URL: https://www.postman.com/oauth2/callback
    - Auth URL: https://developer.api.autodesk.com/authentication/v1/authorize 
    - Access Token URL: https://developer.api.autodesk.com/authentication/v1/gettoken

### Use the endpoints under **Run Firstly-Get Project ID** to set project id, then you can play with any Endpoint as you want.

## Tips & Tricks
- These endpoints are mainly used to quick test|verfify based on your good understanding to Autodesk Takeoff product and API, the individual endpoint may not work, you need to set up the environment variables before running the Postman request.

## License
This sample is licensed under the terms of the [MIT License](http://opensource.org/licenses/MIT). Please see the [LICENSE](../LICENSE) file for full details.

## Written by
Zhong Wu [@johnonsoftware](https://twitter.com/johnonsoftware), [Developer Advocate and Support](http://forge.autodesk.com)