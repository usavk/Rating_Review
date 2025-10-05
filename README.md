⭐ Rating & Review System

A generic and flexible Review & Rating System that can be applied to any type of service or entity — whether it’s an event, sport, movie, or anything else!

💡 Key Idea

The system is designed to handle multiple types of entities dynamically.

entityType → Defines the type of entity (e.g., event, movie, sport, etc.)

entityId → Refers to the unique record ID within that entity type

Example:
If you pass entityType = event and entityId = 1,
it refers to Event with ID 1.

🧩 Models

User – Represents the person giving a review or rating.

Entity – Represents any service or item that can be reviewed/rated.

Review – Stores text-based feedback.

Rating – Stores numeric feedback (e.g., stars out of 5).

🚀 Controllers

ReviewController – Handles all review-related operations.

RatingController – Handles all rating-related operations.

🗣️ Reviews API
➤ Add Review

Endpoint:

POST http://localhost:8080/review/add


Parameters (x-www-form-urlencoded or query):

userId – ID of the user

entityId – ID of the entity being reviewed

entityType – Type of entity (event, movie, etc.)

reviewValue – Text review content

Example URL:

http://localhost:8080/review/add?userId=1&entityId=1&entityType=event&reviewValue=Great+event!

➤ Get Review

Endpoint:

GET http://localhost:8080/review/get


Example URL:

http://localhost:8080/review/get?userId=1&entityId=1&entityType=event

⭐ Ratings API
➤ Add Rating

Endpoint:

POST http://localhost:8080/rating/add


Parameters:

userId

entityId

entityType

ratingValue

Example URL:

http://localhost:8080/rating/add?userId=1&entityId=1&entityType=event&ratingValue=4

➤ Get Rating

Endpoint:

GET http://localhost:8080/rating/get


Example URL:

http://localhost:8080/rating/get?userId=1&entityId=1&entityType=event

🧠 Summary

This system provides a universal structure for managing reviews and ratings across different entity types.
It’s simple, scalable, and can be integrated into any platform that requires user feedback functionality.
