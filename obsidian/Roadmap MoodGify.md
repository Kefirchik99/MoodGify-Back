
### Phase 1: Planning & Setup (5 Days)

#### Column 1: To Do

1. Task: Set up GitHub Repositories (Front-end & Back-end)
   - Priority: High
   - Assignee: Developer 1 & Developer 2
   - Description: 
     - Create repositories for both the front-end (React.js) and back-end (Node.js + Express).
     - Set up .gitignore files and define branch naming conventions.
     - Create initial readme files.
   - Due Date: Day 1
   - [x] Status : Done | `Yaro`

2. Task: Initialize Front-End React.js Project
   - Priority: High
   - Assignee: Developer 1
   - Description:
     - Use Create React App or Vite to bootstrap the front-end project.
     - Set up folder structure (src/, components/, services/, styles/).
     - Install dependencies: React Router, Axios/Fetch, Redux/Context API, SCSS.
   - Due Date: Day 1-2
   - [x] Status : Done | `Yaro`

3. Task: Initialize Back-End Node.js Project
   - Priority: High
   - Assignee: Developer 2
   - Description:
     - Initialize Node.js project using npm init.
     - Set up Express, Mongoose/Firebase SDK, JWT, and basic project structure (routes/, controllers/, models/).
   - Due Date: Day 1-2
   - [ ] Status : | `Yaro` | `Dima`

4. Task: Define API Contract
   - Priority: Medium
   - Assignee: Developer 1 & Developer 2
   - Description:
     - Draft the API contract for user authentication, mood logging, and GIF retrieval endpoints.
     - Document in Google Docs or Notion.
   - Due Date: Day 2
   - [ ] Status : | `Yaro` | `Dima`

5. Task: Set up Environment Variables
   - Priority: Medium
   - Assignee: Developer 1 & Developer 2
   - Description:
     - Create .env files for storing sensitive data (GIF API keys, database URIs).
     - Add .env to .gitignore.
     - Set up front-end environment variables (REACT_APP_API_URL, REACT_APP_GIPHY_API_KEY).
     - Set up back-end environment variables (MONGODB_URI, JWT_SECRET, GIPHY_API_KEY).
   - Due Date: Day 3

6. Task: Integrate GIF API (Back-End)
   - Priority: High
   - Assignee: Developer 1 & Developer 2
   - Description:
     - Configure the GIF API (Giphy/Tenor) and integrate it with the back-end to fetch relevant GIFs based on mood.
     - Implement /api/gif route with a placeholder GIF for testing.
     - Add error handling for API failures.
   - Due Date: Day 3

7. Task: Set up OAuth Authentication (Optional)
   - Priority: Low (optional if using OAuth)
   - Assignee: Developer 2
   - Description:
     - Set up Google/Facebook OAuth using Passport.js or Firebase Authentication.
     - Implement /api/auth/google and /api/auth/facebook routes for login.
     - Test user authentication with OAuth.
   - Due Date: Day 3

8. Task: Create Header & Footer Components (Front-End)
   - Priority: Medium
   - Assignee: Developer 1 & Developer 2
   - Description:
     - Develop the Header and Footer components for basic navigation and layout.
     - Add navigation links (Home, Profile, Login) in the header.
   - Due Date: Day 4

9. Task: Create Login Page (Front-End)
   - Priority: High
   - Assignee: Developer 1
   - Description:
     - Build a basic login page with email/password inputs and Google/Facebook login buttons (if OAuth is implemented).
     - Add form validation (basic email/password checks).
   - Due Date: Day 4

10. Task: Create Mood Selector Component (Front-End)
    - Priority: High
    - Assignee: Developer 1
    - Description:
      - Create a mood selector component where users can choose their mood (happy, sad, etc.).
      - Display a placeholder GIF section when a mood is selected.
    - Due Date: Day 4-5

11. Task: Set Up Basic Routing (Front-End)
    - Priority: Medium
    - Assignee: Developer 1 & Developer 2
    - Description:
      - Implement React Router for navigation between pages (e.g., "/login", "/home", "/profile").
      - Test routing to ensure all components are properly displayed.
    - Due Date: Day 4-5

12. Task: Set up MongoDB/Firebase Database
    - Priority: High
    - Assignee: Developer 2
    - Description:
      - Set up MongoDB Atlas or Firebase for storing user data and mood history.
      - Create User and Mood models/collections for storing data.
    - Due Date: Day 5

13. Task: Create User Authentication (Back-End)
    - Priority: High
    - Assignee: Developer 2
    - Description:
      - Implement JWT-based authentication or OAuth flow for Google/Facebook login.
      - Test sign-up and login routes (/api/auth/signup, /api/auth/login).
    - Due Date: Day 5

14. Task: Implement Mood Logging API (Back-End)
    - Priority: High
    - Assignee: Developer 2
    - Description:
      - Implement POST /api/moods for logging user moods (mood type, timestamp, GIF URL).
      - Test API using Postman to verify mood data is being stored.
    - Due Date: Day 5

15. Task: Implement Mood Retrieval API (Back-End)
    - Priority: High
    - Assignee: Developer 2
    - Description:
      - Implement GET /api/moods to retrieve mood history for a user.
      - Test API with Postman to confirm mood retrieval functionality.
    - Due Date: Day 5

---

### Column 2: In Progress

Developers move tasks from "To Do" to "In Progress" as they start working on them.

---

### Column 3: Done

Once tasks are completed, they will be moved here with a checked label.

---

### Other Notes:
- Tasks can be prioritized based on urgency, ensuring critical items (authentication, GIF API integration, mood logging) are completed first.
- Both developers should hold daily check-ins to discuss progress and any roadblocks.
- Each task should be reviewed before marking it as "Done" to ensure quality and accuracy.

This task-based view provides clarity and allows developers to track their progress while ensuring that all critical elements of Phase 1 are addressed efficiently.


---


- Front-End:
     - Set up Axios or Fetch services in services/api.js for calling the GIF API via the back-end.
     - Create a placeholder service function getGifByMood(moodType) that interacts with the back-end to fetch GIFs based on mood.

3. Set Up OAuth for Authentication (if applicable):
   - Back-End:
     - Set up OAuth flow using Passport.js (Google/Facebook) or Firebase Authentication.
     - Create login routes /api/auth/google and /api/auth/facebook.
     - Test user authentication with the OAuth provider and ensure valid user profiles are created/stored in the database.
   - Front-End:
     - Add Google/Facebook buttons on the login page (UI) with a call to the back-end for authentication.

---

### Day 4: Basic User Interface & Skeleton Pages

#### Developer 1 and Developer 2 (Front-End Focus)

1. Create Basic UI Components:
   - Header & Footer Components:
     - Create simple, reusable components that will serve as the layout for all pages.
     - Include navigation links (Home, Profile, Login) in the header.
   - Login Page:
     - Design a simple form for login/sign-up with Google/Facebook buttons.
     - Set up initial form validation (basic checks for email/password fields).
   - Mood Selector Component:
     - Create a form that allows users to choose their mood (happy, sad, angry, etc.).
     - Display a placeholder GIF section for when the user selects a mood.

2. Set Up Basic Routing:
   - Configure React Router:
     - Define routes for "/login", "/home", and "/profile".
     - Add navigation links in the header and test the routing functionality.
   - Create empty page components (e.g., HomePage, ProfilePage) as placeholders.

---

### Day 5: Back-End API & Database Setup

#### Developer 1 and Developer 2 (Back-End Focus)

1. Set Up MongoDB/Firebase Database:
   - MongoDB:
     - If using MongoDB, set up a MongoDB Atlas cluster or local MongoDB server.
     - Define a User model with basic fields (name, email, mood history).
     - Define a Mood model for storing mood data (userID, moodType, timestamp, GIF URL).
   - Firebase:
     - If using Firebase, set up Firestore collections: users and moods.
     - Implement Firebase authentication logic (if not using OAuth) and database rules for access control.

2. Create Initial User Authentication Logic:
   - JWT Authentication:
     - Implement JWT authentication in Express. Create middleware for protected routes (e.g., mood logging and profile access).
     - Test signup/login routes and verify token-based authentication is working.
   - OAuth Authentication:
     - Test OAuth flow end-to-end to ensure that users can log in with Google/Facebook and that their data is stored correctly in MongoDB/Firebase.

3. Create Basic Mood Logging API:
   - Implement POST /api/moods:
     - Accept user mood type, timestamp, and return the relevant GIF URL from the GIF API.
     - Test this API using Postman/Insomnia to verify that moods are being stored in the database and that the GIF API is working.
   - Implement GET /api/moods:
     - Return all mood entries for a specific user (for later integration with the front-end).

---

### Deliverables by the End of Phase 1

- Front-End:
  - Basic routing and layout are in place with initial components (Header, Footer, Login Page, Mood Selector).
  - GIF API integration is set up with placeholder services ready to fetch GIFs based on mood.
  - OAuth buttons are in place (with back-end integration completed).
  
- Back-End:
  - Basic Express server is running with routes for authentication and mood logging.
  - MongoDB/Firebase database is connected, and user/mood models are set up.
  - Initial API endpoints (user auth, mood logging, and GIF retrieval) are functioning and tested.
  
- General:
  - Project structure is finalized, and the API contract is agreed upon.
  - Developers are aligned on workflows, Git conventions, and testing protocols.

---