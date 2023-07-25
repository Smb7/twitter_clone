# twitter_clone
This is a simple Twitter clone built using Flask and SQLAlchemy. The application provides endpoints to manage users and tweets, allowing users to register, log in, post tweets, like tweets, and more.

Requirements
Python==3.11.4
Flask==2.3.2
Flask-SQLAlchemy==3.0.5

Installation
Clone the repository:
git clone https://github.com/Smb7/twitter_clone
cd flask-twitter-clone

Install the required dependencies:
pip install -r requirements.txt

Create a database:
Edit the app.py file and provide your database URI in the app.config['SQLALCHEMY_DATABASE_URI'] variable.

Initialize the database:
In your terminal, run the following commands:
python

In terminal run:
python app.py

API Endpoints
Users
GET /users: Get a list of all users.
GET /users/<int:id>: Get details of a specific user by ID.
POST /users: Register a new user. Include "username" and "password" in the JSON request body.
DELETE /users/<int:id>: Delete a user by ID.
PATCH/PUT /users/<int:id>: Update a user's details. Include "username" and/or "password" in the JSON request body.
Tweets
GET /tweets: Get a list of all tweets.
GET /tweets/<int:id>: Get details of a specific tweet by ID.
POST /tweets: Create a new tweet. Include "user_id" and "content" in the JSON request body.
DELETE /tweets/<int:id>: Delete a tweet by ID.
Likes
GET /tweets/<int:id>/liking_users: Get a list of users who liked a specific tweet.
Usage
Open your web browser and navigate to http://localhost:5000.
Register a new account or log in with your existing credentials.
You will be redirected to the home page where you can post tweets and view tweets from other users.
To like a tweet, click the heart icon next to the tweet.
Database Schema
User Table
Column	Type	Description
id	Integer	Primary key, auto-incremented
username	String(128)	Unique username for the user
password	String(128)	User's hashed password
Tweet Table
Column	Type	Description
id	Integer	Primary key, auto-incremented
content	String(280)	The content of the tweet
created_at	DateTime	Timestamp when the tweet was created
user_id	Integer	Foreign key to link to the user
Likes Table
Column	Type	Description
user_id	Integer	Foreign key to link to the user
tweet_id	Integer	Foreign key to link to the tweet
created_at	DateTime	Timestamp when the like was created
Contributing
Contributions are welcome! If you find any issues or have suggestions for improvement, feel free to open an issue or submit a pull request.

Please ensure that your code adheres to the PEP 8 style guide.

License
This project is licensed under the MIT License.


