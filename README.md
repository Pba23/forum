#Forum

A comprehensive web forum allowing users to communicate, share, and interact through posts and comments.

## Description

This project is a web forum developed in Go that enables users to register, log in, publish messages, comment, and interact with content through likes and dislikes. The forum uses SQLite as a database and is containerized with Docker for easy deployment.

## Features

### Core Features
- **Authentication**
  - User registration (email, username, password)
  - Login/logout functionality
  - User session management with cookies
  
- **Communication**
  - Post creation (restricted to logged-in users)
  - Adding comments to posts (restricted to logged-in users)
  - Viewing posts and comments (open to all)
  
- **Categorization**
  - Association of one or more categories to each post
  - Filtering posts by category
  
- **Interactions**
  - Like and dislike system for posts and comments
  - Like/dislike counter visible to all users
  
- **Filtering**
  - Filter by categories
  - Filter by created posts (logged-in users only)
  - Filter by liked posts (logged-in users only)

### Supplementary Modules
This project is complemented by additional modules in separate repositories:
- **[Forum Security](https://github.com/Pba23/forum-security)**: Advanced security features
- **[Forum Advanced Features](https://github.com/Pba23/forum-advanced-features)**: Additional functionality
- **[Forum Image Upload](https://github.com/Pba23/forum-image-upload)**: Image upload management
- **[Forum Moderator](https://github.com/Pba23/forum-moderator)**: Moderation system

## Technologies Used

- **Backend**: Go
- **Database**: SQLite
- **Containerization**: Docker
- **Frontend**: HTML, CSS, Vanilla JavaScript (no frameworks)
- **Security**: bcrypt for password encryption, UUID for sessions

## Installation and Setup

### Prerequisites
- Go installed on your machine
- Docker installed on your machine

### Installation

1. Clone the repository
```bash
git clone https://github.com/your-username/forum.git
cd forum
```

2. Build the Docker image
```bash
docker build -t forum .
```

3. Launch the container
```bash
docker run -p 8080:8080 forum
```

4. Access the forum in your browser at: `http://localhost:8080`

## Database Structure

The SQLite database includes the following tables:
- Users
- Posts
- Comments
- Categories
- Post_Categories (relationship between posts and categories)
- Likes (likes on posts and comments)

## Testing

To run the unit tests:
```bash
go test ./...
```

## Contribution

Contributions are welcome! Feel free to open an issue or submit a pull request.
