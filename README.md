# React training program. 
## Practice

## Main goal:
Create web application that will give end-user ability to read books (stored online).
Application should have next parts:
* main screen with recent user's activity
* login & logout control
* screen with list of all available books
* screen with book that is currently read

## Stage 1. React
Main goal - implement 'book reading' screen with static content (loremipsum).
This screen should look like:
![Book View](/resources/book-view.jpg)
### Header should contain next info:
* book title
* current chapter title
* components to increase / decrease font size, change color schema, change font family

### Footer should contain next info:
* number of current page
* number of total pages in current chapter

### Left & right panels should be invisible areas that help user navigate backward / forward through the book

Book content should be placed in these panels at the middle of the screen

### List of requirements that application should fulfil prior moving to next stage:
* user are able to open application and read book with static content
* user cannot navigate out of selected book (so there are only one route in app)
* user can see current page and number of all pages
* user can see book title / chapter title
* user can change font size / font family and pages are recalculated
* app should work correctly on Chrome with screen size limited to 480 * 320

### Structure of book object
* Book
** id
** title
** chapters (Array)
*** id
*** title
*** html_content

There are no info about pages on any level of book object.

## Stage 2. Redux
Main goal - implement home screen (recent activity) / list of all books / login & logout control

### Tech details
* add redux-store
* add routing
* add AJAX requests to get books / recently viewed books / books by id with mocked data as response
* add logout button on top of the home screen
* add login modal

### List of requirements that application should fulfil prior moving to next stage:
* user is able to see list of books (limited to 4) that were recently viewed
* user is able to see list of all books (with paging, 8 books per page)
* user is able to open any book and move to part that was already developed under *Stage 1*
* user is able to open *recently viewed* book and this book will be opened on last read page
* user is able to logout
* user is able to login (if user is not looged in after app is opened - app should show modal with login / password input fields)

## Stage 3. Redux Advanced
Main goal - finalize application

### Tech details
* add middleware to handle AJAX requests
* add logging of response errors (use in AJAX middleware or as separate middleware)
* add saving of storage on user log-out
* add restoring of storage on user log-in
