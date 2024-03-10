# Node.js Application

This repository contains a Node.js application with routes for user authentication, user management, posting functionality, and more.

## Getting Started

To get started with this project, follow these steps:

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up environment variables:

   Create a `.env` file in the root directory of the project and add the following configuration variables:

   ```dotenv
   PORT=3000
   MONGO_URL=mongodb://localhost:27017/my_database
   JWT_SECRET=my_secret_key
   ```

4. Start the server:

   ```bash
   npm start
   ```

## Configuration

This application uses environment variables for configuration. Here are the available configuration options:

- `PORT`: The port on which the server will listen.
- `MONGO_URL`: The URL of the MongoDB database
- `JWT_SECRET`: The secret key used for JWT token generation and verification.

## Routes

### Authentication

- `POST /auth/register`: Register a new user.
- `POST /auth/login`: Login user.

### Users

- `GET /users/:id`: Get user information.
- `GET /users/:id/friends`: Get user's friends.
- `PATCH /users/:id/:friendId`: Add or remove friend.

### Posts

- `GET /posts`: Get feed posts.
- `GET /posts/:userId`: Get user's posts.
- `POST /posts`: Create a new post.
- `PATCH /posts/:id/like`: Like a post.

## Dependencies

- [bcrypt](https://www.npmjs.com/package/bcrypt): A library to hash passwords securely.
- [body-parser](https://www.npmjs.com/package/body-parser): Node.js body parsing middleware.
- [cors](https://www.npmjs.com/package/cors): Cross-origin resource sharing middleware.
- [dotenv](https://www.npmjs.com/package/dotenv): Loads environment variables from a `.env` file.
- [express](https://www.npmjs.com/package/express): Fast, unopinionated, minimalist web framework for Node.js.
- [gridfs-stream](https://www.npmjs.com/package/gridfs-stream): GridFS storage for Node.js streams.
- [helmet](https://www.npmjs.com/package/helmet): Helps secure your Express apps by setting various HTTP headers.
- [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken): Implementation of JSON Web Tokens (JWT) for Node.js.
- [mongoose](https://www.npmjs.com/package/mongoose): MongoDB object modeling tool designed to work in an asynchronous environment.
- [morgan](https://www.npmjs.com/package/morgan): HTTP request logger middleware for Node.js.
- [multer](https://www.npmjs.com/package/multer): Node.js middleware for handling multipart/form-data.
- [multer-gridfs-storage](https://www.npmjs.com/package/multer-gridfs-storage): GridFS storage engine for multer.

