# EMMARKET
A web application for supermarkets to manage products and carts, including the ability to handle multiple carts and calculate the total amount for each order. Each cart can be added a description for more details.

---
Table Of Content
- [EMMARKET](#emmarket)
  - [Features](#features)
  - [Installation](#installation)
    - [Run](#run)
    - [Backend \& API](#backend--api)
      - [Backend Installation](#backend-installation)
      - [Backend Run](#backend-run)
  - [Usage](#usage)
    - [POS Page (home page)](#pos-page-home-page)
    - [Products Filteration and Searching](#products-filteration-and-searching)
    - [Change the display way](#change-the-display-way)
      - [Display as Cards](#display-as-cards)
      - [Display as List](#display-as-list)
    - [Carts \& Filterations \& Sorting](#carts--filterations--sorting)
    - [Single Cart Manpluation](#single-cart-manpluation)

---
## Features
> Product Manpluation page
>
> Muli-Cart Manpluation or POS page
> 
> Search & Filteration system
> 
> Category Manpluation page
> 
> Unit of measure Manpluation page
> 
> Dashbaord for Users
> 
> Authentication System
> 
> User Authorization 
>
> Switch Between Themes 

## Installation

The application built in node environment in react.js. To install the project you can clone it or install it as Zip file. After downloading project, You have to install the dependencies by this command:
```bash
npm i
```
### Run
```bash
npm start
```
### Backend & API 
The system are connected with backend that i build **Without the backend the system fail or even you cant use its own features**. Now lets installing and setup the backed to use the API's. Through this Link 
**[POS-BACKEND](https://github.com/AhmadEleiwa/POS-Backend)**.
The backend also built in node environment with express api. To install the backend you should follow the same steps witch we discover before.

> **NOTE:** The system database is MongoDB and the uri of the database connection is hidden in .env file. To Setup mongodb configuration correctly you have add .env file with line below
>
> MONGOPATH = "mongodb+srv://(username):ixrwZDUrxf6qcTei@cluster0.tubw4as.mongodb.net/(collection name)?retryWrites=true&w=majority"
#### Backend Installation 
```bash
npm i
```
#### Backend Run
```bash
npm start
```

## Usage
After installing and configure our app. The main page once we starting the page at localhost at port 3000 the page run this url [https::/localhost:3000](http://localhost:3000/) will shown as the figure below

<img src='assets/loginpage.png' />

Noway to navigate to any page without login to the page.There's no users yet. excpt only the admin. 
> Note: That once you configure MongoDB the system will not create the admin user. you have to Create one manually.
```ts
interface User{
    username:string;
    password:string;
    admin:boolean;
}
```
### POS Page (home page)
<img src='assets/pospage.png' />
A page for the cashier to manage customer's carts. This includes the ability to create and manage multiple carts and add descriptions to them for additional information. This page can handle these functionlites:

### Products Filteration and Searching 
The Search bar and select inputs used for apply the filteration on the list of products

<img src='assets/filterproducts.png' />

### Change the display way
Also You can change the display way of products list from Cards to list as shown


#### Display as Cards
<img src='assets/cardshow.png' />

#### Display as List
<img src='assets/listshow.png' />


### Carts & Filterations & Sorting
By Clicking on the headers of the tables, the sort will be applied on the entire list. With Search you can search about the cart description.

<img src='assets/carttabel.png' width='100%' />

### Single Cart Manpluation
After choosing to any cart from the list. It navigate you to this cart as shown below. For each cart you can change the description or the QTY for the single product or Deleting Product from the list or adding new product by clicking on producin porduct list. Also, There's Tax and discount for each cart
```ts
interface Cart {
  cartId: string;
  description: string;
  tax: number;
  discount: number;
  products: Product[];
}
```

<img src='assets/singelcart.png' />