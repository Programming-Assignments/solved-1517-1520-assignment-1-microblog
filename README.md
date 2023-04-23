Download Link: https://assignmentchef.com/product/solved-1517-1520-assignment-1-microblog
<br>
<p class="ui header product-top-header" title="Assignment 1 – &quot;Microblog&quot; Solution"><strong>Introduction</strong>

This is an individual assignment in which you are required to develop a dynamic web application as described below using PHP, MySQL, JavaScript and CSS.Details of the weight of the assignment and due date are given in the course description.

<strong>Task Description</strong><strong>Application</strong>

For this assignment, you will create a web-based microblogging platform, similar in functionality to “Twitter”. You will have to come up with your own fancy name.

<strong>Database Structure</strong>The web application uses a relational database to create a micro-blogging platform. The database has the following structure:

User(id, name, email, password)Post(id, user_id, post_date, in_reply_to, text)Follow(user_id, follower_id)

Each record in the Post table refers to a single post made by a user. Primary keys are indicated with underlines or bold formatting, and foreign keys are italicized.The following constraints should be applied in implementing the application:

• The user_id and follower_id fields in the Follow table form a compound primary key, and both refer to the id field in the User table. The user id field should be an integer primary key, and should automatically increment.• The post_date field may be stored as either strings, or using MySQL datetime types, and must include time as well as date.CRICOS Provider No. 00103D ITECH3224 6224 Assignment 1 1517-1520.docx

• The text field in the Post table should be limited to 160 characters.

• The in_reply_to field in the Post table is a nullable foreign key that refers to the id field on the same table. If this field is null, then the post is not a reply to another post – if it is non-null then the post is a reply to the post with the matching id.

• The password field should be a VARCHAR field of at least 125 characters. The name and email fields should be VARCHAR of a length that you determine to be reasonable and sufficient.

<strong>Initial data</strong>

When the database is created it should be populated with data of your own invention. Include this data as part of your written report. Each table should have between 3 and 6 records initially.

Include yourself as a user, using your student id as the name, and your real email address. Invent other users as necessary – perhaps use characters from your favourite movie or band.

<strong>Creating the database</strong>

Create an SQL file that creates a database on the server, creates the three tables above, and populates them with your initial data.

Password data should be hashed using, at minimum, the crypt() PHP function. If available, prefer to use the PHP password_hash() function to generate password hashes. It is acceptable for all initial User records to share the same password for testing. Use of MD5 is not acceptable.

Include a user that can login as ‘tutor’ with password ‘guest’.Test your database by writing queries on the command line that display all initial data using SELECT statements, and include the queries in your report.

<strong>User accounts</strong>

Write an HTML form that allows new users to sign up. The form should request a username, email address and password. The password must be hashed before storing it in the database.Using PHP, validate that the username is unique, and the password is at least 5 characters. Write PHP code to allow users to log in and log out. This will require the use of sessions or cookies.

<strong>Global timeline</strong>Write PHP and HTML code to display a list of the last 10 posts from all users, sorted in descending date order – that is, the most recent posts are at the top. This timeline of posts should be visible to anybody without logging in.If posts are in reply to another post, include a link to the original.

<strong>Creating posts</strong>Logged-in users should be able to create new posts. Write PHP code to support this. Use both PHP and Javascript to limit the length of the post to 160 characters.<strong>Following</strong>

Write HTML and PHP code to allow logged-in users to follow other users. This should create a new entry in the Follow table. This may require you to create a way to view an individual user, or list of all users.

Users who are logged in should see posts only from users that they follow, instead of the global timeline. This list should again be limited to the last 10 posts.

<strong>Replying</strong>Create a link on each post that allows a logged-in user to reply to a post. This should allow them to create a new entry in the Post table, with the in_reply_to foreign-key field set appropriately.

<strong>Aggregate data</strong>Complete the following using SQL aggregation such as COUNT and SUM, subqueries or nested SELECT statements, inner joins and (left or right) outer joins.• Create a page that contains a list of the top 10 most-followed users, with their number of followers ordered in descending order. Similarly create a page that contains a list of the top 20 most popular posts by number of replies.• For each post in the timeline that has replies, display the number of replies with the post.• Display the number of posts that have been made in the last 24 hours at the top of the global timeline.

5/5 - (2 votes)