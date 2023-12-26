Booking_Rest_API_Postman
##Title and Description

Booking REST API Documentation
Introduction
This document provides information on how to use the Booking REST API using Postman. The API allows you to manage bookings for a variety of purposes.

API Base URL
The base URL for the Booking API is: https://api.example.com/bookings

Authentication
All requests to the API must be authenticated using an API key. Include the API key in the Authorization header of your requests.

Example header:

Authorization: Bearer YOUR_API_KEY
Positive Endpoints

Test Case :

##1. Create a Booking
Create a new booking.

Endpoint: /create
Method: POST
Request Body:
{ "firstname": "{{fname}}", "lastname": "{{lname}}", "totalprice": 1000, "depositpaid": true, "bookingdates": { "checkin": "2018-01-01", "checkout": "2019-01-01" }, "additionalneeds": "Breakfast" }

Success Response:
{ "bookingid": 4875, "booking": { "firstname": "testers", "lastname": "talk", "totalprice": 1000, "depositpaid": true, "bookingdates": { "checkin": "2018-01-01", "checkout": "2019-01-01" }, "additionalneeds": "Breakfast" } }

##2. Get Booking Details
Retrieve a list of all bookings.

Endpoint: /list
Method: GET
Success Response:
{ "firstname": "testers", "lastname": "talk", "totalprice": 1000, "depositpaid": true, "bookingdates": { "checkin": "2018-01-01", "checkout": "2019-01-01" }, "additionalneeds": "Breakfast" }

##3.Post Token Generator
Endpoint: /{booking_id}

Method: POST

{ "username":"admin",
"password":"password123"

}

Success Response:
{ "token": "72e7ea739eef644" }

##4.PUT Update Booking
{
  "firstname": "Spaceflow",
  "lastname": "Selenium c#",
  "totalprice": 111,
  "depositpaid": true,
  "bookingdates": {
      "checkin": "2018-01-01",
      "checkout": "2019-01-01"
  },
  "additionalneeds": "Breakfast"
}

## **Success Response:**

    ```json
{
  "firstname": "Spaceflow",
  "lastname": "Selenium c#",
  "totalprice": 111,
  "depositpaid": true,
  "bookingdates": {
      "checkin": "2018-01-01",
      "checkout": "2019-01-01"
  },
  "additionalneeds": "Breakfast"
}

## 5.PATCH Partial Update Booking
  ```json

{
  "firstname": "API Testing"
}

## **Success Response:**
```json

{
  "firstname": "API Testing",
  "lastname": "Selenium c#",
  "totalprice": 111,
  "depositpaid": true,
  "bookingdates": {
      "checkin": "2018-01-01",
      "checkout": "2019-01-01"
  },
  "additionalneeds": "Breakfast"
}

## 6.POST Curl Command Import

```json
{
  "firstname": "testers",
  "lastname": "talk",
  "totalprice": 1000,
  "depositpaid": true,
  "bookingdates": {
      "checkin": "2018-01-01",
      "checkout": "2019-01-01"
  },
  "additionalneeds": "Breakfast"
}


## **Success Response:**
```json

{
  "bookingid": 3784,
  "booking": {
      "firstname": "testers",
      "lastname": "talk",
      "totalprice": 1000,
      "depositpaid": true,
      "bookingdates": {
          "checkin": "2018-01-01",
          "checkout": "2019-01-01"
      },
      "additionalneeds": "Breakfast"
  }
}

## Negetive Scenarios
GET Booking Details Invalid Id

## **Success Response:**
Not Found
API Documentation:
https://documenter.getpostman.com/view/28551467/2s9XxwvtRM

Prerequisite:

Jdk
Node Js
Newman
Html Report Library

Newman and Report Installation Process:

Newman Install Command:
npm install -g newman-reporter-htmlextra

Newman Html Report Install Command:
npm install -g newman-reporter-htmlextra


How to run this project

Clone this project

Open with Postman 

Run Command:
newman run StudentDetails.postman_collection.json -e StudentDetails.postman_environment.json 

Run Command for Report:
newman run StudentDetails.postman_collection.json -e StudentDetails.postman_environment.json -r cli,htmlextra

Technology used:
Postman
Newman

Newman Report Summary:

https://drive.google.com/drive/folders/17DuBYyyRYoU5RRBSF_LxavWk5x-d2yNz?q=parent:17DuBYyyRYoU5RRBSF_LxavWk5x-d2yNz%20owner:me