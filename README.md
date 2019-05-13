# couchbasedemo-ios
This is a simple project of a demo app to show how integrate couchbase lite in an iOS app.

## App
The app is a Contacts app that allows user to list his contacts, add a new contact, edit or delete one.
The app has three screens:
* Main screen: show the list of all contacts. The user can create a new contact by clicking on a plus button. He also can go to detail view by clicking on a contact of the list and delete one contact doing a left-swipe on a cell of the list.
* New contact screen: show a simple form to input contact data and save it.
* Detail/edit contact screen: show the contact detail data and allows user to edit data and save changes.

The *Contact* model has the below fields:
* id
* name
* surname
* phoneNumber
* email

All fields are optional except the id.

## Project
The project is based on the *MVVM design pattern*. Due to academic purposes the project was kept simple. The view controllers contain only UI and navigation logic. The view models contain all the application logic. They contain all the CRUD methods and are the only allowed to access the database.
In a real application, is strongly recommended to split the project in more than one layer, to keep ui logic, domain logic and data logic separated.

There are three groups of viewcontroller-viewmodel:
* ContactsViewController/ContactsViewModel: list of all contacts
* NewContactViewController/NewContactViewModel: new contact creation
* ContactDetailViewController/ContactDetailViewModel: contact detail / edit contact

## How to use
The project contains fortyeight steps to guide the user step by step through the development process. It's enough to uncomment each step, build and run the demo app to test the app functionalities. To test the sync functionality a url should be properly configured in the Constants class instead of the actual placeholder url.
