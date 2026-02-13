Auth APIs
POST /api/auth/register:{"name", "email", "password"}
POST /api/auth/login:{"email", "password"} - Returns a {"token": "JWT_STRING_HERE"}
GET /api/auth/me: {"id", "name", "email"}

Event APIs
GET /api/events: Returns a list of all club events.
POST /api/events: (Admin only) Creates a new event. -{"title", "description", "date"}
POST /api/events/:id/rsvp: Takes a status (YES/NO/MAYBE).
DELETE /api/events/:id	: Deleted an event by ID

RSVP APIs
POST /api/events/:id/rsvp: Create or update an RSVP status. {"status": "YES"} (or NO, MAYBE)
GET /api/events/:id/attendees:	Get a list of everyone attending a pecific event. 
GET /api/users/me/rsvps: Get a list of all events the logged-in user has joined.