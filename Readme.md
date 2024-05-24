**Podverse Web Application Deployment Guide**

This guide provides a step-by-step process to run the Podverse web application, including setup instructions for both client and server folders. Ensure you follow these steps meticulously for a smooth deployment experience.

### Client Folder (Frontend)

**Environment Variables (`.env` file):**
- Make sure to create a `.env` file in the client folder with the following variables:
  ```
  REACT_APP_FIREBASE_API_KEY="your-api-key"
  REACT_APP_FIREBASE_AUTH_DOMAIN="your-auth-domain"
  REACT_APP_FIREBASE_PROJECT_ID="your-project-id"
  REACT_APP_FIREBASE_STORAGE_BUCKET="your-storage-bucket"
  REACT_APP_FIREBASE_MESSAGING_ID="your-messaging-id"
  REACT_APP_FIREBASE_APP_ID="your-app-id"
  REACT_APP_FIREBASE_MEASUREMENT_ID="your-measurement-id"
  ```

**Instructions:**
1. **Change Directory to Client:**
   ```
   cd client
   ```

2. **Install Client Packages:**
   ```
   npm install
   ```

3. **Start the Client:**
   ```
   npm start
   ```

### Server Folder (Backend)

**Environment Variables (`.env` file):**
- Create a `.env` file in the server folder with the following variable:
  ```
  DB_STRING=mongodb+srv://username:password@cluster0.klhz4ln.mongodb.net/?retryWrites=true&w=majority
  ```
  Replace `username` and `password` with your MongoDB credentials.

**Firebase Configuration:**
- Place your Firebase service account key JSON file in the `config` folder of the server directory and rename it to `serverAccountKey.json`.

**Instructions:**
1. **Change Directory to Server:**
   ```
   cd server
   ```

2. **Install Server Packages:**
   ```
   npm install
   ```

3. **Start the Server:**
   ```
   nodemon app.js
   ```

### Post-Installation Steps

1. **MongoDB Configuration:**
   - After signing into the website, go to MongoDB and manually change the user database's role from `member` to `admin`. This enables access to the dashboard.

2. **Firebase Storage Setup:**
   - Create two folders in Firebase Storage named `Image` and `Audio` to store images and audio files respectively.

3. **Website Usage:**
   - After signing in as admin, access the dashboard from the top right corner to manage audio and video content.
   - Use the dashboard to upload podcasts (click on the "+" symbol) and manage user roles.

By following these steps, you can successfully deploy and run the Podverse web application. Ensure you've completed all setup steps for a seamless user experience.
