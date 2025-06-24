# CampusBurn

CampusBurn is an anonymous social platform built dedicatedly for college students who want to help upcoming generations with correct knowledge and guidance about anything related to their college and university.

## 🔥 Introduction

Have you ever felt that you should provide a good review of your college but are afraid that your college might take some actions against you? Well, what if you could do this anonymously and also in this process, make some anonymous friends of a similar age group? That's what CAMPUSBURN is.

## ✨ Features

- **Anonymous Posting**: Share your thoughts, experiences, and reviews without revealing your identity
- **User Authentication**: Secure login and registration system
- **Post Interaction**: Like, dislike, and comment on posts
- **Profile Management**: Customize your anonymous profile
- **Email Verification**: Ensure user authenticity through email verification
- **Image Upload**: Share images using Cloudinary integration

## 🛠️ Tech Stack

### Frontend
- **Next.js**: React framework for building the client-side application
- **TypeScript**: For type-safe code
- **Tailwind CSS**: For styling the UI components

### Backend
- **Go (Golang)**: For building the server-side application
- **Fiber**: Web framework for Go
- **GORM**: ORM library for database interactions
- **PostgreSQL**: Database for storing application data
- **JWT**: For authentication and authorization

### Third-party Services
- **Cloudinary**: For image storage and management
- **Resend**: For email services

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or later)
- Go (v1.16 or later)
- PostgreSQL
- Cloudinary account
- Resend account

### Setting up the Frontend

1. Navigate to the client directory:
   ```bash
   cd client/campusburn
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file based on `.env.example`:
   ```
   NEXT_PUBLIC_RESEND_API_KEY=your-resend-api-key
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

5. Open [http://localhost:3000](http://localhost:3000) in your browser

### Setting up the Backend

1. Navigate to the server directory:
   ```bash
   cd server
   ```

2. Create a `.env` file based on `.env.example`:
   ```
   DATABASE_URL=your-postgres-db-url
   JWT_SECRET=your-jwt-secret
   CLOUDINARY_API_KEY=your-cloudinary-api-key
   CLOUDINARY_API_SECRET=your-cloudinary-api-secret
   CLOUDINARY_CLOUD_NAME=your-cloudinary-cloud-name
   RESEND_API_KEY=your-resend-api-key
   ```

3. Run the database migrations:
   ```bash
   go run dbMigrate/migrate.go
   ```

4. Start the server:
   ```bash
   go run main.go
   ```

5. The server will start on port 4200

## 📝 API Endpoints

### Authentication
- `POST /auth/sign-up`: Register a new user
- `POST /auth/sign-in`: Login a user
- `POST /auth/sign-out`: Logout a user
- `DELETE /auth/deleteUser/:userId`: Delete a user account
- `POST /updateUser`: Update user profile
- `POST /sendEmail`: Send verification email
- `POST /verifyEmail`: Verify email with OTP

### Posts
- `POST /createPost`: Create a new post
- `POST /deletePost`: Delete a post
- `PUT /updatePost`: Update a post
- `POST /likePost`: Like a post
- `POST /dislikePost`: Dislike a post
- `GET /getAllPosts`: Get all posts
- `GET /getTopPosts`: Get top-rated posts

### Comments
- `POST /addComment`: Add a comment to a post
- `PUT /editComment`: Edit a comment
- `POST /deleteComment`: Delete a comment
- `POST /likeComment`: Like a comment
- `POST /dislikeComment`: Dislike a comment
- `POST /allComments`: Get all comments for a post

### Media
- `POST /uploadImage`: Upload an image to Cloudinary
- `GET /getImage`: Fetch an image from Cloudinary

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Contact

For any questions or suggestions, please open an issue in the repository.
