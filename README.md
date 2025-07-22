# React Authentication Frontend

This project is a **modern frontend application** built with React and Vite, designed to interact with a Node.js/Express.js backend for user authentication, email verification, and password reset functionality. It uses Tailwind CSS for styling and implements best practices for accounts and security.

## Features

- **React SPA** built using Vite for fast development.
- Utilizes **Tailwind CSS** for rapid UI styling.
- Implements **Authentication workflows** (sign up, log in, log out).
- **Account verification** via email OTP.
- **Password reset** with email OTP flow.
- **Persistent session management** with cookies.
- Fully connected to a secure Node.js/Express backend (see backend README for details).

## Tech Stack

| Technology          | Purpose                                      |
|---------------------|----------------------------------------------|
| React + Vite        | JS framework & blazing fast bundler          |
| Tailwind CSS        | Utility-first CSS styling                    |
| React Router        | Client-side routing                          |
| Axios               | API client (handles cookies/headers)         |
| react-toastify      | User notifications                           |
| Context API         | App-wide state management                    |

## Folder Structure

```
/src
  /assets         # Static assets (images, icons, etc.)
  /context        # React Context for app-wide state (AppContext.jsx)
  /components     # Reusable UI components (Navbar, Header)
  /pages          # App pages (Home, Login, Reset, VerifyEmail)
  index.css       # Imports Tailwind CSS and fonts
  main.jsx        # App entry point with router/context
  App.jsx         # Main App component
vite.config.js    # Vite configuration
```

## Local Setup

1. **Clone the repository and install dependencies:**

   ```bash
   git clone 
   cd 
   npm install
   ```

2. **Set environment variables:**

   Create a `.env` file in the project root and add:

   ```
   VITE_BACKEND_URL=http://localhost:4000
   ```

   (Update the URL if your backend runs elsewhere.)

3. **Run the development server:**

   ```bash
   npm run dev
   ```

   Open `http://localhost:5173` in your browser.

## Usage

1. **Sign Up:**  
   Register with your name, email, and password.

2. **Log In:**  
   Enter your email and password to authenticate.

3. **Email Verification:**  
   After registration, receive an OTP on your email. Enter the OTP to verify your account.

4. **Password Reset:**  
   - Use "Forgot password?" to receive an OTP.
   - Enter OTP and your new password to reset.

5. **Logout:**  
   Securely log out—cookies/session are cleared.

## Notable Code Highlights

- **Context State (AppContext.jsx):**
  - Shares auth status, user data, and backend URL globally.
  - Handles API errors and success notifications.

- **Route Protection:**  
  - Sensitive routes/components use state from context (e.g., isLoggedIn, userData).

- **OTP Handling:**  
  - Custom logic for input focus, paste, and backspace navigation for user-friendly OTP entry.

## Scripts

| Command         | Description                      |
|-----------------|----------------------------------|
| `npm run dev`   | Start local dev server (Vite)    |
| `npm run build` | Build for production             |
| `npm run preview`| Preview production build        |

## Customization

- To change the backend URL, update the `.env` variable `VITE_BACKEND_URL`.
- Easily add new UI features by extending components or pages.

## Requirements

- Node.js v16+ and npm
- Backend API with matching endpoint contracts (provided separately)

## License

This project is open-source and available for modification and distribution under your chosen license.

## Acknowledgments

- Inspired by real-world authentication best practices.
- Built with the combined power of React, Vite, and Tailwind CSS.

**Happy coding!**

[1] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/54960530/171d1a25-ba72-4d59-a64a-228d68614c99/vite.config.js
[2] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/54960530/d01b9375-e30c-45e2-b563-64a850329ff2/VerifyEmail.jsx
[3] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/54960530/a3dc48e8-0976-43a3-9739-c31c022ed681/Reset.jsx
[4] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/54960530/2029720a-8cd4-49c9-bab1-efdd5d366902/Login.jsx
[5] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/54960530/71808b36-0887-431b-b54a-1c1527cd5515/Home.jsx
[6] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/54960530/65ddda0e-64ce-4d87-aaed-b026ac5964b3/main.jsx
[7] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/54960530/c64c16cc-36c7-4738-b95e-be3de66b5f44/index.css
[8] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/54960530/3c500d46-f2b3-4164-b690-0d716f52deff/AppContext.jsx
[9] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/54960530/d0036040-88eb-4573-b4fc-5284e0483e27/Navbar.jsx
[10] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/54960530/39a2cedb-09e3-4e11-9cbb-ea0d40836500/Header.jsx