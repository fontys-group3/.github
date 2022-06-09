# Restaurant Order System

## Table of contents
 - [What is Restaurant Order System?](#what-is-restaurant-order-system)
   - [Menu](#menu)
   - [Kitchen and Bar Interfaces](#kitchen-and-bar-interfaces) 
 - [Architecture](#architecture)
   - [Structure](#structure)
   - [Coding Languages](#coding-languages)
   - [Database](#database)
   - [Model](#model)
 - [Project Managment](#project-managment)
   - [Scrum](#scrum)

# What is Restaurant Order System
Restaurant Order Sytem is an web application that exists of 2 smaller applications.

## Menu
The menu is made for the customers. Customers can go to the menu by scanning a QR code that's located at every table. Let's say our customer scans the QR code on table 7. The QR code will bring the customer to our menu, important to note here is that the website knows the QR code on table 7 has been scanned. The customeer can now order his desired food and drinks. After it has been ordered our other application comes in action.

*Our Menu*
![image](https://user-images.githubusercontent.com/74303221/172864452-5ee0885e-45eb-4e2a-9f08-27bbe8002aab.png)

## Kitchen and Bar Interface
After a order has been ordered. It enters the Kitchen and Bar Interface. Here employees can claim orders. When a employee claims an order he can choose what color it should be. A color represents an employee. Also can they drag orders to In Progress and Done. If an order is done a waiter should bring the food to the table.

*Kitchen and Bar Interface*
(image)

# Architecture
In this section we explain all our technical decisions.

## Structure
We have chosen to work with microservices. We made this choice because our application is easier to expand this way. For example, if the customer wants a new and specific functionality, a new microservice can be created for that. For example, a monolithic application may require you to redesign it. A microservice design also makes it easier to detect errors/crashes. (If one microservice fails, the others will probably still run). In our case, for example, the menu might work, but you can't order. In addition, we can divide the services within the group, which increases our productivity compared to a monolithic application.

## Coding Languages
We used different languages for our front-end and back-end.

### Back-end
For our back-end we had the choice between many different languages, in the end we landed on the choice between Java and C#. In the end, we made the decision to choose Java as the back-end, because we all like to learn a new language and we had to work with C# already in semester 2. Another reason we chose Java is because we don't want to spend too much time learning a new language. Since Java appears to be easy to learn and resembles C#, we thought this was a good choice. Java also has the advantage that it is Multi platform, which means that it works on any machine.

### Front-end
We have chosen Javascript 'framework' for the front-end, because that is a learning outcome.

We chose React as our front-end library. We made this choice because there is a lot of documentation available about React, there are many successful companies that use React, examples are Netflix, Uber, Airbnb and in the group we already have experience with React which ensures that we can work more efficient.

In addition, we think it is advantageous to use Typescript in the front-end. Typescript is a superset of Javascript. Compared to JS, TS is an object oriented programming language that matches our back-end. It provides more structure in your project through the data annotation. In addition, TS is also a compiler language, which ensures that you can recognize bugs before you start the program. This can quickly fix simple mistakes and save us time.

## Database
For our database decision we did a small research.

### Relational or Non-Relational
The advantage of a non-relational database is that the data does not have to be entered in a specific format. In a relational database, data is stored in tables with rows and columns. All data to be stored in a table must conform to the rows and columns specified in that table. The advantage of this is that you can avoid duplicate data, since you can create a separate table in case of duplicate data. But suppose your dataset changes a lot, for example the structure of your tables changes continuously, then it is useful to use a non-relational database as changing a table structure can lead to data loss. Another disadvantage of a non-relational database is that you can't perform certain queries, such as queries that depend on relations on other tables. That is because a non-relational database does not have the necessary relationships.

We want nothing to be stored in a database during an order. Only when the order has been confirmed we want to store it in our database.

It is convenient for us to choose SQL over NoSQL. That is because we can prevent duplicate data by means of linking tables. Think of 10 customers making the same order. This would be very cumbersome and inconvenient in NoSQL, since you would then have completely written out the same piece of data 10 times. NoSQL also has no matching tables, so the concept of linking a customer to a product isn't possible. 

## Model
We have 2 frontends, one for the customer and one for the employees. The one for the employee has an extra tab for the manager. You do need an account to access it.

![image](https://user-images.githubusercontent.com/74303221/172874475-510f9253-d910-47f8-b4ae-709fdcc3b4b5.png)
 
# Project Managment

## Case
To start it all off, we got a case form our stakeholders.

blank v
[Case - InfoSupport](#blank)

## User Stories
Using this case we created user stories for the stakeholders. We showed them the user stories, tweaked them here and there, and started choosing user stories for sprint 1. When we had our set of user stories we started to play some story point poker, and started working on them.

## Sprint Release
After each sprint we had a sprint release. Here we showed everything we made in the sprint. The stakeholders give us feedback, and we use the feedback in the next sprint.
