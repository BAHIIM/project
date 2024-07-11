GitHub Profile Analyzer

Table of Contents
Project Overview
Features
Technologies
Setup and Installation
Usage
API Endpoints
Data Model
Challenges
Progress
Contributing
License
Authors
Screenshot

Project Overview
GitHub Profile Analyzer is a web application designed to help developers analyze and visualize their GitHub activity. By integrating with the GitHub API, users can authenticate via GitHub OAuth, fetch their repository and commit data, and view interactive visualizations of their activity.

Features
GitHub OAuth Authentication: Securely log in using your GitHub account.
Profile Data Visualization: View your GitHub profile information, including repositories and commit history.
Interactive Charts: Analyze your coding patterns and contribution frequency through interactive visualizations.
Customizable Reports: Generate reports based on your activity data.

Technologies
Frontend: HTML, CSS, JavaScript
Backend: PHP
Database: MySQL
API Gateway: GitHub API
Deployment: AWS
Alternative Technologies and Trade-offs
Frontend:
Alternative: React.js
Trade-off: React.js offers a component-based architecture and state management, but HTML, CSS, and JavaScript were chosen for their simplicity and wide browser compatibility.
Database:
Alternative: MongoDB
Trade-off: MongoDB provides flexible schema design, but MySQL was chosen for its strong relational database capabilities and support for complex queries.

Setup and Installation
Prerequisites
PHP
MySQL
Apache or Nginx server
Installation
Clone the repository:
bash
Copier le code
git clone https://github.com/bahiim/github-profile-analyzer.git
cd github-profile-analyzer


Set up environment variables: Create a .env file in the root directory and add the following:
bash
Copier le code
GITHUB_CLIENT_ID=your_github_client_id
GITHUB_CLIENT_SECRET=your_github_client_secret
DB_HOST=your_database_host
DB_NAME=your_database_name
DB_USER=your_database_user
DB_PASS=your_database_password


Import the database: Import the database.sql file into your MySQL database.
Run the application: Start your web server and navigate to the application.

Usage
Log in with GitHub: Navigate to the application and click on the "Log in with GitHub" button.
View Profile Data: After logging in, view your profile data, including repositories and commit history.
Analyze Data: Use the interactive charts to analyze your coding patterns and contribution frequency.
Generate Reports: Create customizable reports based on your activity data.

API Endpoints
Authentication
GET /api/auth: Initiates GitHub OAuth process.
POST /api/auth/callback: Handles callback from GitHub OAuth and retrieves access token.
User Data
GET /api/user: Returns authenticated user’s profile data from GitHub.
GET /api/repos: Fetches the list of repositories for the authenticated user.
GET /api/commits: Retrieves commit history for a specified repository.
GET /api/analysis: Returns analyzed data and visualizations based on user activity.

Data Model
Tables
Users
id: Unique identifier
username: GitHub username
profile_data: JSON object containing user profile information
access_token: OAuth access token
Repositories
id: Unique identifier
user_id: Reference to Users table
repo_name: Name of the repository
repo_data: JSON object containing repository information
Commits
id: Unique identifier
repo_id: Reference to Repositories table
commit_data: JSON object containing commit information

Challenges
Technical Challenge
One of the major technical challenges was linking the site to the database and ensuring proper data persistence. Initially, the backend server failed to establish a connection with the MySQL database, causing errors during data storage and retrieval. The challenge required in-depth debugging, reconfiguring database connection settings, and collaborating with the database administration team to adjust network and access permissions.
Non-Technical Challenge
Coordinating the project timeline and managing team morale was a significant non-technical challenge. The database integration issue led to delays, which frustrated the team. We addressed this by reassessing our timeline, redistributing tasks, and improving communication and documentation practices. This helped in maintaining team morale and ensuring continued progress despite setbacks.

Progress
Progress Rating: 7/10
Explanation of Progress Assessment:
Completed Parts: UI development, initial backend setup, partial OAuth integration.
Incomplete Aspects: Full database integration, data persistence, advanced features.
Challenges Faced:
Technical: Database connection issues.
Non-Technical: Project timeline management and team coordination.

Contributing
We welcome contributions from the community. To contribute:
Fork the repository
Create a new branch: git checkout -b feature-branch
Commit your changes: git commit -m 'Add new feature'
Push to the branch: git push origin feature-branch
Create a Pull Request

License
This project is licensed under the Team Bahiim|khalid|amine. See the LICENSE file for details.

Authors
Abderrahim Oulmaamer
LinkedIn : https://www.linkedin.com/in/abderrahim-oulmaamer/
GitHub : https://github.com/Bahiim
Khalid Benhamou
LinkedIn : https://www.linkedin.com/in/khalid-benhamou/
GitHub : https://github.com/5alidev
Amine Bifden
LinkedIn : https://www.linkedin.com/in/bifden-amine/
GitHub : https://github.com/GoAmine

Screenshot

For any questions or support, please contact [oulmaamerabderrahim@gmail.com].

