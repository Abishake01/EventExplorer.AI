# React Vite Project

This is a React project bootstrapped with [Vite](https://vitejs.dev/), a fast and modern build tool. The project serves as a template for building scalable and efficient React applications.

---

## Features

- ⚡ **Vite:** Super fast build and development environment.
- 🖼️ **React 18:** Modern React features with concurrent rendering.
- 🛠️ **ES Modules:** Native support for ES6+ modules.
- 🔥 **Hot Module Replacement (HMR):** Instant updates during development.
- 💅 **Customizable:** Add plugins and configurations as needed.

---

## Prerequisites

Make sure you have the following installed:

- **Node.js**: [Download here](https://nodejs.org/)
- **npm or yarn**: Comes with Node.js installation.

---

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Abishake01/EventExplorer.AI.git
   cd EventExplorer.AI

2. **Install dependencies:**
    ```bash
    npm install
    # or
    yarn install

3. **Start the development server:**
    ```bash
    npm run dev
    # or
    yarn dev

4. Open the app in your browser at http://localhost:5173

<a href="https://www.youtube.com/watch?v=EzzcEL_1o9o"> Video Tutorial</a>

## Key features and Functionalities

1. **3D Avatar Interaction:**

A 3D avatar is integrated using @react-three/fiber and @react-three/drei.
The avatar supports facial expressions, lip-syncing, and animations.
Facial expressions (e.g., smile, sad, angry) are dynamically applied based on the message context.

2. **Chat Functionality:**

A chat system is implemented using a custom useChat hook.
Messages are sent to a backend API (https://virtual-gf-py.vercel.app/chat) and responses are displayed.
Messages are processed in a queue, and the avatar speaks the responses using Speech Synthesis.

3. **Speech Synthesis:**

The avatar speaks messages using the Web Speech API.
Lip-syncing is implemented by randomly selecting visemes (mouth shapes) during speech.

4. **Voice Input:**

Users can input messages via voice using the Web Speech Recognition API.
The microphone button activates voice input, and the recognized text is sent as a message.

5. **Camera Controls:**

The camera can zoom in and out using a toggle button.
Camera positions are controlled using CameraControls from @react-three/drei.

6. **Green Screen Mode:**

A green screen mode can be toggled on/off, changing the background to green for chroma keying.

7. **Loading Indicators:**

A loading animation (dots) is displayed while waiting for a response from the backend.

## Technologies Used

1. **React:**

JavaScript library for building the user interface.
Version: React 18.

2. **Vite:**

Build tool for fast development and production builds.
Used for bundling and optimizing the project.

3. **Tailwind CSS:**

Utility-first CSS framework for styling the UI.
Provides responsive and modern design.

4. **React Three Fiber:**

React renderer for Three.js, used for 3D rendering.
Version: @react-three/fiber 8.13.3.

5. **React Three Drei:**

Helper library for React Three Fiber.
Provides components like CameraControls, Environment, and Text.
Version: @react-three/drei 9.75.0.

6. **Three.js:**

3D library for rendering and animating 3D objects.
Version: three 0.153.0.

## Challenges Faced

1. **3D Avatar Integration**

Challenge: Integrating a 3D avatar with realistic facial expressions and animations.
Solution:
Used ReadyPlayerMe for the avatar model.
Implemented morph targets for facial expressions and visemes for lip-syncing.
Leveraged @react-three/fiber and @react-three/drei for rendering and animations.

2. **Speech Synthesis and Lip-Syncing**

Challenge: Synchronizing the avatar's lip movements with speech synthesis.
Solution:
Used the Web Speech API for text-to-speech.
Implemented random viseme selection during speech to simulate lip-syncing.
Adjusted viseme intensity based on the avatar's current expression.

3. **Voice Input**

Challenge: Implementing voice input using the Web Speech Recognition API.
Solution:
Added a microphone button to activate voice input.
Processed the recognized text and sent it as a chat message.
Handled errors and unsupported browser scenarios gracefully.

4. **Camera Controls**

Challenge: Implementing smooth camera zoom and movement.
Solution:
Used CameraControls from @react-three/drei for camera manipulation.
Added a toggle button to switch between zoomed-in and zoomed-out views.

5. **Green Screen Mode**

Challenge: Implementing a green screen mode for chroma keying.
Solution:
Added a toggle button to change the background to green.
Used CSS to dynamically update the background color.

6. **Loading Indicators**

Challenge: Displaying a loading animation while waiting for backend responses.
Solution:
Created a Dots component that animates dots during loading.
Wrapped the component in Suspense to prevent flickering during asset loading.

7. **State Management**

Challenge: Managing complex state for chat messages, animations, and expressions.
Solution:
Created a custom useChat hook to centralize chat-related state and logic.
Used useState, useEffect, and useRef for managing state and side effects.

8. **Cross-Browser Compatibility**

Challenge: Ensuring compatibility across different browsers, especially for speech synthesis and recognition.
Solution:
Tested the application on multiple browsers (Chrome, Firefox, Edge).
Added fallbacks and error handling for unsupported features.

9. **Performance Optimization**

Challenge: Optimizing performance for smooth 3D rendering and animations.
Solution:
Preloaded 3D models and animations to reduce loading times.
Used useFrame for efficient frame updates in the 3D scene.

10. **Debugging and Testing**

Challenge: Debugging complex interactions between 3D rendering, chat, and speech synthesis.
Solution:
Used Leva for debugging and controlling variables.
Added logging and error handling to identify and fix issues.

11. **Backend Integration**

Challenge: Integrating with the backend API for chat functionality.
Solution:
Used the Fetch API to send and receive data.
Handled errors and loading states gracefully.

