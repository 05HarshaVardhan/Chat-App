# ChatAP: A Real-Time Social Media Chat Application 👋

**ChatAP** is a modern and lightweight real-time chat application built using the **MERN** stack (MongoDB, Express.js, React.js, Node.js) and powered by **Socket.IO**. It's designed to provide a seamless and engaging chat experience, with a focus on security, performance, and user customization.

**Live Website:** [https://hellocat-0.web.app/](https://hellocat-0.web.app/)

---

## ✨ Features

Our application comes packed with a rich set of features to make chatting fun and efficient.

- **Secure Authentication:** Users can sign up, sign in, and manage their accounts with secure email verification. Forgot password functionality is also included. 🔐
- **Real-Time Messaging:** Experience instant messaging with the power of Socket.IO.
- **Conversation History:** All your chats are stored in MongoDB, so you can revisit them anytime. 💬
- **Interactive Chat UI:** Enjoy features like read receipts and typing indicators, making conversations feel more natural.
- **Media Sharing:** Effortlessly share various media types, including images. 🖼️
- **File Sharing:** Share files, code snippets, and even your location with friends. 📂
- **User Profiles:** View and update your profile details (e.g., birthday, gender, profile image). You can also view other users' profiles.
- **Friends Management:** Easily add and manage your friends list.
- **Customization:** Personalize your experience with a built-in theme editor and a dark/light mode toggle. 🎨
- **Privacy and Security:** Advanced settings to control your privacy and manage your login history.
- **Fully Responsive:** The application is fully responsive, providing a smooth experience across all devices. 📱💻

<!-- Replace with your actual GIF URL -->
<p align="center">
  <img src="https://via.placeholder.com/600x300/4F46E5/FFFFFF?text=ChatAP+Demo" alt="Chat UI Animation" width="600"/>
</p>

---

## 🛠️ Tech Stack

**Client:**
- **React.js:** A robust JavaScript library for building user interfaces.
- **Redux (or React Hooks):** For efficient state management and performance enhancement.
- **TailwindCSS (or other CSS framework):** For a clean and modern design.

**Server:**
- **Node.js & Express.js:** A fast and scalable backend for handling multiple simultaneous connections.
- **Socket.IO:** The core technology for real-time, bidirectional, event-based communication.

**Database:**
- **MongoDB:** A flexible NoSQL database for storing user data, messages, and more.

**Deployment:**
- **Frontend:** Vercel (or other similar services)
- **Backend:** Render (or other similar services)

---

## 🚀 Installation Guide

To get this project up and running on your local machine, follow these simple steps.

### Step 1: Clone the Repository

```bash
git clone https://github.com/05HarshaVardhan/Chat-App.git
cd Chat-App
```

### Step 2: Install Dependencies

Navigate to the client and server directories to install the required packages.

**Install dependencies for the client:**
```bash
cd client
npm i
```

**Navigate back and install dependencies for the server:**
```bash
cd ../server
npm i
```

### Step 3: Add Environment Variables

Create a `.env` file in both the client and server directories and add the necessary environment variables.

**For the Client:**
```env
REACT_APP_SERVER_ACCESS_BASE_URL=your_server_url_here
```

**For the Server:**
```env
MONGO_URL=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
SMTP_SERVICES=your_smtp_service
SMTP_MAIL=your_smtp_email
SMTP_PASSWORD=your_smtp_password
SMTP_HOST=your_smtp_host
SMTP_PORT=your_smtp_port
CLIENT_ACCESS_URL=your_client_url
```

### Step 4: Start the Application

Run the client and server separately.

**Start Frontend Server:**
```bash
# Move into the client directory
cd client

# Start the frontend server
npm start
```

**Start Backend Server:**
```bash
# Move into the server directory
cd ../server

# Start the backend server
npm start

# For automatic restart on changes, use:
npm run dev
```

After both servers are running, you can access the application in your browser.

---

## 📸 Screenshots

<img width="1270" height="703" alt="login" src="https://github.com/user-attachments/assets/dc5e5167-dac9-4434-bcc8-b8c7fd932960" />

### 📝 User Authentication: Sign Up

This screenshot displays the secure user authentication flow for new user registration. The interface is designed to capture essential information while ensuring data integrity.

-   **Form Fields:**
    -   `Email`: Collects the user's email address, which serves as the unique identifier for their account. This will be used for both sign-in and potential password recovery.
    -   `Password`: Accepts the user's desired password. The password input type is masked to ensure privacy.
    -   `Confirm Password`: A validation field to ensure the user has typed their password correctly, preventing common input errors.
-   **Sign Up Button:**
    -   This button initiates a POST request to the backend API (`/api/auth/signup` or similar endpoint).
    -   On the server, a user object is created, the password is hashed using a strong algorithm like bcrypt, and the user's data is stored in the MongoDB database.
-   **"Already have account? Sign In" link:**
    -   A routing link that directs the user to the `Sign In` component. This helps navigate between authentication pages without a full page reload, common in single-page applications (SPAs) built with React.

This process is a critical part of the application's security architecture, ensuring that each user has a unique and protected account before accessing the chat functionalities.

---
<img width="1384" height="785" alt="signup" src="https://github.com/user-attachments/assets/d1140e23-7e5a-43cc-9b0b-07a3556afd79" />

### 🧑‍💼 User Profile Information

This image shows the user information form, a crucial step after initial registration, where users can personalize their profile.

-   **Form Fields:**
    -   `First Name`: Captures the user's first name.
    -   `Last Name`: Captures the user's last name.
    -   `Username`: Displays a unique identifier, likely auto-generated or chosen by the user, which can be used for public display and direct messaging.
    -   `Date of Birth`: A date input field that allows the user to specify their birth date, which is stored for demographic and age-based feature access.
    -   `Gender`: A dropdown menu providing predefined options (e.g., Male, Female) for the user to select their gender.
-   **"Done" Button:**
    -   This button submits the collected profile data to the backend.
    -   Upon submission, the server-side logic updates the user's profile document in the MongoDB database, enriching their user profile with this new information.
    -   This action finalizes the registration process, typically redirecting the user to their main dashboard or chat interface.

This profile customization step is key to providing a personalized and more engaging user experience within the application.

---
<img width="1087" height="460" alt="profile" src="https://github.com/user-attachments/assets/05c64683-58b6-4bc9-93e9-f80f05102da2" />

### 👤 User Profile View

This screenshot represents a user's public profile page, which showcases key information and social metrics.

-   **Profile Header:**
    -   Displays the user's profile picture, name, and a unique `@username` (`@HK5005`), which serves as their public handle.
    -   Social metrics such as `Followers` and `Following` are also displayed here, indicating the application's social media features.
-   **User Information:**
    -   This section presents detailed profile data fetched from the database, likely from the user information form submitted earlier.
    -   `Total Posts`: Tracks the number of public posts or messages the user has made.
    -   `Birthday`: Displays the user's date of birth.
    -   `Gender`: Shows the user's specified gender.
    -   `Joined`: Indicates the date the user joined the platform, derived from the account creation timestamp.
    -   `Last Online`: A real-time indicator of the user's last known active status, managed using Socket.IO for dynamic updates.

This view provides other users with an overview of the individual's activity and personal details, fostering a sense of community within the platform.

---
<img width="1913" height="972" alt="browse-friends" src="https://github.com/user-attachments/assets/46463c3a-cffc-4a9e-9f8f-7631f7b8437f" />

### 🔍 User Search and Discovery

This screenshot illustrates the user search functionality, allowing users to find and connect with other members of the platform.

-   **Search Bar:**
    -   A prominent input field that allows users to type in a name or username.
    -   As the user types, the application performs a real-time search, likely making an API call to a `/api/users/search` endpoint.
    -   The backend query searches for matching users in the database and returns a list of results.
-   **User List:**
    -   The list displays the results of the search query in a clean, scrollable format.
    -   Each list item represents a user and includes:
        -   **Profile Picture/Avatar:** A circular icon displaying the user's initial or profile picture.
        -   **Full Name:** The user's first and last name.
        -   **Username:** The unique `@username` for easy identification.
-   **Functionality:**
    -   Clicking on any user in the list likely redirects the current user to that person's public profile page, where they can view more details and initiate a friend request or follow.

This feature is essential for a social application, as it provides a straightforward method for users to expand their network and engage with others on the platform.
---
<img width="1911" height="956" alt="Screenshot 2025-08-05 221928" src="https://github.com/user-attachments/assets/cc33a738-78a5-481f-b783-982fd5408817" />

### 👥 Friend's Profile View

This screenshot shows how a user's profile is displayed to another user, highlighting key social interaction features.

-   **Profile Header:**
    -   Displays the friend's profile picture, name, and unique `@username` (`@harsh1999`).
    -   Social metrics such as `Followers` and `Following` are also shown, providing context on their social presence.
-   **Social Interaction Buttons:**
    -   `Follow` button: Allows the user to follow the friend's public activity. This action updates the follower count on the backend.
    -   `Add Friend` button: Initiates a friend request to the user. On click, a request is sent and the button's state might change (e.g., to "Request Sent") to prevent duplicate requests.
-   **User Information:**
    -   Displays the friend's personal details, including `Total Posts`, `Birthday`, `Gender`, and `Joined` date.
    -   `Last Online`: A dynamic indicator that shows the time since the friend was last active, providing real-time presence information to the user.
-   **Friends Section:**
    -   This section visually confirms the "Friends" status, likely showing a green dot or a similar icon to indicate that the user and the profile owner are connected.

This view is specifically designed to facilitate social connections and provide a comprehensive overview of another user within the application.

---
<img width="618" height="474" alt="preview_0" src="https://github.com/user-attachments/assets/062c9de4-f64d-4dd8-a1ab-6bfcf9bee58d" />

### 💬 Real-time Chat Interface

This screenshot displays the core chat functionality, showcasing a one-on-one conversation with a user.

-   **Chat Header:**
    -   Displays the profile picture and name of the person you are chatting with, in this case, "Hime Uzaki".
    -   The 'X' icon in the top right corner is used to close the chat window, returning the user to the main interface.
-   **Conversation Area:**
    -   **Conversation Start:** Indicates when the chat was initiated, showing the date and time.
    -   **Message Bubbles:**
        -   **Received Messages:** Messages from the other user appear on the left, with their profile picture and the message content (e.g., "Hello").
        -   **Sent Messages:** Messages sent by the current user appear on the right.
    -   **Read Receipts:** A "seen" indicator confirms that the recipient has viewed the message, a key feature of real-time messaging.
    -   **Code Snippets:** The application supports sending formatted code blocks, demonstrating a feature for developers or technical discussions.
    -   **Mathematical Notation:** The ability to render mathematical expressions (e.g., $sin \frac{\pi}{2}$) indicates support for various content types, likely through a text-rendering library.
-   **Message Input Area:**
    -   **Input Box:** The main text field for typing messages.
    -   **Attachment Buttons:**
        -   An icon for attaching files (images, documents, etc.).
        -   An icon for accessing a menu of additional options (like emojis, GIFs, or other features).
    -   **Send Button:** A heart icon is used to send messages, which also suggests an option for sending reactions or specific types of messages.

This detailed chat interface is built to handle multiple message formats, ensuring a versatile and dynamic communication experience.
---


## 🧑‍💻 Authors

This project was developed by:

[@05HarshaVardhan](https://github.com/05HarshaVardhan)

---

## 💬 Feedback

If you have any feedback or suggestions, please feel free to reach out. We'd love to hear from you!

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/05HarshaVardhan/Chat-App/issues).

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
