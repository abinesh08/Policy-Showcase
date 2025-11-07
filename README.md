# Policy-Showcase

Policy-Showcase is a simple Spring Boot microservices project that displays images with descriptions and hashtags (like #Women, #Men, #Dravidian).
It uses file-based storage instead of a database and has two independent services:

Admin Service:
Handles login (from file), forgot username/password, image upload, update, delete, and manage hashtags.

Display Service:
Displays the uploaded images and allows filtering based on hashtags.

🧑‍💼 Admin Service
🔹 Features

Login (reads from file)

Forgot username

Forgot password

Reset password

Upload image and hashtags

Update or delete uploaded data

View all uploaded policies

🔹 API Endpoints
Method	Endpoint	Description
POST	/api/admin/login	Login using username and password
GET	/api/admin/forgot-username	Retrieve saved username
GET	/api/admin/forgot-password	Retrieve saved password
PUT	/api/admin/reset-password	Reset password and update file
POST	/api/admin/upload	Upload image, about text, and hashtags
PUT	/api/admin/update/{imageName}	Update existing policy info
DELETE	/api/admin/delete/{imageName}	Delete policy entry
GET	/api/admin/policies	View all uploaded policies

👁️ Display Service
🔹 Features

Show all uploaded policies

Filter by hashtags (e.g., #Women, #Dravidian, etc.)

🔹 API Endpoints
Method	Endpoint	Description
GET	/api/display/all	Get all policies
GET	/api/display/filter/{hashtag}	Filter policies by hashtag
