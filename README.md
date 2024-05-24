Connectify

Connectify is a microservices-based social networking platform built using Laravel, designed for scalability and maintainability.

Microservices

- User Service: Manages user-related operations such as registration, authentication, and profile management.
- Notification Service: Handles the creation and delivery of notifications to users.
- Message Service: Manages user-to-user messaging functionality.
- Friendship Service: Handles friend requests and the management of user friendships.

Architecture

Connectify follows a microservices pattern, where each service runs independently. Communication between services is handled via RESTful APIs.

[Diagram Placeholder]

Getting Started

Prerequisites

Ensure you have the following installed:
- Docker
- Docker Compose

Installation

1. Clone the repository:
   git clone https://github.com/yourusername/connectify.git
   cd connectify

2. Build and start the services:
   docker-compose up --build

Each service will be available on the following ports:
- User Service: http://localhost:8001
- Notification Service: http://localhost:8002
- Message Service: http://localhost:8003
- Friendship Service: http://localhost:8004

Running the Services

After building the images, you can start the services using:
docker-compose up

To stop the services:
docker-compose down

API Endpoints

Each service exposes a set of RESTful endpoints. Below are examples for each service.

User Service
- GET /api/users - List all users
- POST /api/register - Register a new user
- POST /api/login - User login

Notification Service
- GET /api/notifications - List all notifications
- POST /api/notifications - Create a new notification

Message Service
- GET /api/messages - List all messages
- POST /api/messages - Send a new message

Friendship Service
- GET /api/friendships - List all friendships
- POST /api/friendships - Send a friend request

Environment Variables

Each service requires specific environment variables. Below is an example configuration for the User Service.

env

# User Service .env example
APP_NAME=UserService
APP_ENV=local
APP_KEY=base64:YOUR_APP_KEY_HERE
APP_DEBUG=true
APP_URL=http://localhost:8001

DB_CONNECTION=mysql
DB_HOST=your-database-host
DB_PORT=3306
DB_DATABASE=user_service_db
DB_USERNAME=your-database-username
DB_PASSWORD=your-database-password

Contributing

We welcome contributions! Please fork the repository and submit a pull request.

1. Fork the Project
2. Create your Feature Branch (git checkout -b feature/AmazingFeature)
3. Commit your Changes (git commit -m 'Add some AmazingFeature')
4. Push to the Branch (git push origin feature/AmazingFeature)
5. Open a Pull Request

License

Distributed under the MIT License. See LICENSE for more information.

Feel free to customize this README to better fit your project's needs. If you have any images or diagrams, such as an architecture diagram, include them to make the documentation more comprehensive.
