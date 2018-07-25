# bank-app

>  Ruby on Rails 5 Application with haml and API

## Table of contents
* [General info](#general-info)
* [Screenshots](#screenshots)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)
* [Inspiration](#inspiration)
* [Contact](#contact)

## General info
Simple banking application written in Rails 5 where a user can perform withdrawals and deposit transactions. The purpose is to document the current practices in terms of organizing javascript, api code (Rails) and command patterns for business rules.

Bank account belongs to a client, a client can have many bank accounts.

## Screenshots
![Example screenshot](https://raw.githubusercontent.com/lapinskap/bank-app/master/img/scr%20-%20Copy.jpg)
![Example screenshot](https://raw.githubusercontent.com/lapinskap/bank-app/master/img/scr.jpg)

## Technologies
* Ruby on Rails 5
* HAML
* jQuery
* Sqlite

## Setup

 ```
 $ git clone https://github.com/lapinskap/bank-app
 $ cd bank-app
 $ bundle install
 $ rails s
 ```
 ### Operations in terminal
 
 #### Add a client:
 ```
 $ rails console
 $ Client.create!(first_name: "Juan", middle_name: "Pablo", last_name: "Fernandez", client_number: "42034823") 
 $ client = Client.last
 $ exit
 ```
 > Rails model will change clients name to uppercase letters
 
 #### Create Bank Account:
 ```
 $ rails console
 $ BankAccount.create!(client: client, account_number: "000000001")
 $ exit
 ```
> `client: client` <- client name defined while creating a client

> default balance is $0.00

#### Delete history of transactions: 
```
$ rails console
$ AccountTransaction.destroy_all
```
or delete last transaction:

```
$ AccountTransaction.last.destroy!
$ exit

$ rails s
```

## Code Examples
#### HAML example
```html
<div class="container">
 <div class="row">
  <div class="col-md-12"></div>
 </div>
</div>

%div.container
 %div.row
  %div.col-md-12

.container
 .row
  .col-md-12
```

## Features
List of features ready and TODOs for future development
* HAML files
* Ajax calls 

To-do list:
* Add styles!
* Fix ajax bugs!

## Status
Project is: _in progress_

## Inspiration
An idea for an application that I liked very much - Inspired by devlogs youtube videos - I decided that I want to do my own version of "simple banking app". It seems easy for me to expand in the future. 

## Contact
Created by [@lapinskap](https://www.facebook.com/paulina.lapinska99) - feel free to contact me!
