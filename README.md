# Product-Review
This application allows products, users and reviews to be added to a database. It also creates associations between the three where: A product can have many users, a user has many products, and a review belongs to a user and to a product. A user of the application can also access specific information from the database:

From a review, the app user can get the user who wrote it -From a review, the app user can get the product the review is about -From a product, the app user can get all its reviews -From a product, the app user can get all the users who reviewed the product -From a user, the app user can get all the reviews that the user has written -From a user, the app user can get all the products that the user has reviewed -From a review, the app user should be able to get a sentence that shows the product name, user name, the review star rating and the review comment. -From a product, an app user should be able to add a new review to the database associated with a user -From a product the app user should be able to get a sentence that shows the product name, user name,review star rating and the review comment -From a product the app user should be able to get the average star rating for all the reviews of the product -From a user the app user should be able to get the product with the highest start rating from a user -From a user the app user should be able to remove all of a users review for that product by removing any rows from the reviews table associated with this user and the product

# Pseudo Code
Create a reviews table that has two columns star_rating that stores an integer
comment that stores a string

Create a products table that has a name column Create a users table that has a name column

add macros such that the reviews table belongs to the users table and to the products table

## For the reviews table:
create #user method that returns the review's user

create #product method that returns the review's product

seed reviews to the database to test the functionalities

## For the products table:

create #reviews method thar returns a collection of all the reviews for the product

create #users that returns a colection of all the users who reviewed the product

## For the users table:
create #reviews method that returns a collectiom of all the reviews the user has given

create #products method that returns a collection of all the products that a user has reviewed

Test the functionalities of these methods using Rake console before proceeding

For reviews table: Create #print_review method that prints tring formatted as: Review for {insert product name} by {insert user name}: {insert review star_rating}. {insert review comment}

## For products table:
Create #leave_review method that takes in an instance of the user class, a star_rating and a comment and creates a new Review associated with this Product and the User

Create #print_all_reviews method that prints all the reviews of the product in the following format: 

Review for {insert product name} by {insert user name}: {insert review star_rating}. {insert review comment}

Create #average_rating method that returns(as a float) the average start rating for all reviews of the product

## For users table:
Create #favourite_product that returns the product instance that has the highest star rating from this user

Create #remove_reviews method that takes in a product instance and removes all this user's reviews for that product by deleting any rows from the reviews table associated with this user and the product