# Skill Exchange Platform

A simple web-based platform for connecting learners and tutors. Users can create skills, request courses, chat, give feedback, and manage their accounts. Built using PHP, MySQL, and HTML/CSS

#Project Description

The Skill Exchange Platform allows tutors to post skills or courses and learners to request access to them. Once accepted, learners can chat with tutors and provide ratings and feedback. The dashboard is personalized for tutors and learners with notifications, skill management, and account management features.
#Features

# For Tutors:
- Create and delete skills.
- View connection requests from learners.
- Accept connection requests.
- Chat with connected learners.
- Notifications for new connection requests.
- Delete their account.

# For Learners:
- Search and filter available skills.
- Send connection requests to tutors.
- Chat with connected tutors.
- Give ratings and feedback for tutors.
- Notifications for accepted requests.
- Delete their account.

#Common Features:
- Secure login/logout system.
- Personalized dashboard based on role.
- Feedback system with ratings.
- Responsive and simple UI.



# Tech Stack

- Frontend: HTML, CSS, PHP forms
- Backend: PHP (server-side)
- Database: MySQL (via phpMyAdmin/XAMPP)
- Session Management: PHP sessions
- Optional UI Enhancements: Bootstrap (if needed)

> Note: JavaScript/Bootstrap is used for front-end interactivity only; backend is fully handled by PHP.



# Database Schema

**Tables:**
- `users` - Stores tutor and learner accounts
- `skill_posts` - Tutor skills/courses
- `connection_requests` - Requests from learners to tutors
- `feedback` - Learner feedback and ratings for tutors

Relationships:
- Users → Skill Posts (1-to-many)
- Users → Feedback (1-to-many)
- Skill Posts → Connection Requests (1-to-many)
- Feedback → Users and Skill Posts

---

# Setup Instructions

1. **Install XAMPP/WAMP/MAMP** and start Apache & MySQL.  
2. Open **phpMyAdmin**: `http://localhost/phpmyadmin`  
3. Create a database, e.g., `tutor_platform_db`  
4. Import the provided SQL file to create tables and relationships.  
5. Clone this repository to `htdocs` (or your web server root).  
6. Update `db.php` with your database credentials:

```php
<?php
$conn = mysqli_connect("localhost", "root", "", "tutor_platform_db");
if (!$conn) die("Database connection failed: " . mysqli_connect_error());
?>
Open the project in your browser:
http://localhost/tutor_platform/dashboard.php



