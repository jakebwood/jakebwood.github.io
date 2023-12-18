---
layout: essay
type: essay
title: "Assignment 3 Checkpoint"
# All dates must be YYYY-MM-DD format!
date: 2023-12-11
published: true
labels:
  - ITM352
  - E5.5
---

<h2>Show what each page will look like. The pages do not have to be “functional” but the design should clear.</h2>
Please click <a href="https://www.youtube.com/watch?v=jzpWVX9lcSM">here</a> to view a short screencast outlining my formatting for Assignment 3.

<h2>Describe your design for your site’s shopping cart. That is, will it be a separate page that the user can view and edit, or will it be integrated into the product pages? If so, describe in detail how this will work on your site. Provide several examples of using the cart.</h2>
The shopping cart will be a separate page that the user can visit by clicking on the shopping cart icon atop all of the product pages. The user will be able to edit quantities on this page, as well as see their current subtotal (not including tax or shipping costs). Users do not need to be logged in to view or edit their cart; however, they will be redirected to the login page if they attempt to checkout and go to the invoice. 

<h2>Explain specifically how you will use sessions to manage your shopping cart. In particular, what shopping cart data will be stored in the session, what data format will be used (NOT what data type, but the format like with the data format used for your registration data). Use code examples showing what data structures (such as arrays and their objects) you will use to manage the shopping cart data and how they will be used in a session.</h2>
The shopping cart data that will be stored in the session will be done so in an array. Since we reformatted our products to be three separate arrays contained within one JSON object, the session will reference an individual item through their respective array format. For example, {Boxes:[1, 1, 1, 0, 0, 0], Boosters:[1, 1, 1, 1, 1, 1], Accessories:[0, 0, 0, 1, 1, 1]}. This way, I will be able to tell if the user has picked out quantities for the respective array, and the individual object in each array. Although this is the format I expect to use, if this does not work, I could always refer to the object in its entirety within the array, specifying the quantity, name, etc. From there, I could push new quantities into this stored session array/pop off the last item if removed, in order to keep an updated shopping cart.

<h2>How will you avoid access to your application when the user has not logged in or registered? What are the particular security concerns you must address?</h2>
As we did in the last lab, we are able to validate log in status through the use of cookies generated by the server and sent to the client. Our client pages are able to check and validate to ensure each visitor has received a cookie from the server, verifying their login. A security concern regarding cookies is that since they are sent to the client to be used, they can also be manipulated in order to fulfill whatever tests are being conducted using said cookie.

<h2>Upon a successful login, how do you provide personalization in your UI? Explain how you did or will do this (paste code if necessary)</h2>
Upon logging in, each product page on my website will say "username's" cart. The user will also be greeted by their name when arriving at the invoice, and will also be personally thanked after completing their purchase. In Assignment 2, I was able to complete parts of this challenge by converting the object for the users name into a string, and passing it through the query string. This query string would then be sent to following pages, where this data could be used to generate personalized messages. For this assignment, I am thinking of using sessions and pulling the name object for each user out of their individual session. I will most likely leave the shipping address in the query string, as it is submitted as a form on the confirmation page. 

<h2>If you are working with partners, how will you split up the work in your team so that you are working in parallel as effectively as possible? That is, who is doing what and when?</h2>
I am not working with a partner.

<h2>How are you approaching Assignment 3 differently than Assignment 2?</h2>
Assignment 2 built upon Assignment 1, as we were still tasked to use the query string to pass data between pages, in order to be manipulated and used; however, with Assignment 3, we are required to use cookies and sessions to accomplish similar tasks. Because of this, I expect to do much more learning on my own through online resources, since we did not practice these concepts in too great of detail both in the lab, nor previous assignments