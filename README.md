# OTJS - Social Media Platform

## Overview

The Social Media Web platform, **OTJS**, is a scalable application that allows users to interact through posts, likes, and real-time updates. Built with **React**, **TypeScript**, **Tailwind CSS**, and **Appwrite**, OTJS provides a seamless, responsive, and modern user experience.

---

## Features

- **User Authentication:** Secure login and registration powered by Appwrite.
- **Profile Management:** Manage and customize user profiles effortlessly.
- **Posts:** Create, edit, and delete posts with ease.
- **Comments and Likes:** Engage with posts interactively.
- **Real-Time Updates:** Keep the UI synchronized with the server using React Query.
- **Responsive Design:** Tailored for desktop and mobile devices using Tailwind CSS.

---

## Design Patterns Used in OTJS

1. **Singleton Pattern:**  
   - **Usage:** Implemented in the `AppwriteConfig` class.  
   - **Purpose:** Ensures that there is only one instance of the configuration, providing a global point of access to Appwrite settings throughout the application.

2. **Factory Pattern:**  
   - **Usage:** Utilized in the `EntityFactory` class.  
   - **Purpose:** Centralizes the creation of user and post objects. Also used for creating query and mutation hooks for form fields and API interactions, maintaining clean and consistent object creation.

3. **Repository Pattern (MVC):**  
   - **Usage:** Found in the `UserRepository` and `PostRepository` classes.  
   - **Purpose:** Abstracts database operations, separating data access logic from business logic. Provides a clean API for CRUD operations on user and post data.

4. **Observer Pattern:**  
   - **Usage:** Evident in the use of `React Query`'s `queryClient.invalidateQueries()` method.  
   - **Purpose:** Notifies components to refetch data when mutations occur, ensuring the UI stays in sync with the latest state and changes.

5. **Command Pattern:**  
   - **Usage:** Used in the `createMutationHook` setup.  
   - **Purpose:** Encapsulates actions (e.g., signing in, creating a post) with their side effects, allowing these operations to be executed flexibly and consistently.

6. **Strategy Pattern:**  
   - **Usage:** Implemented in the `PostSorter` class.  
   - **Purpose:** Enables the use of different sorting strategies (e.g., `ChronologicalSort`, `PopularitySort`) for posts. This allows the sorting logic to be extended or modified without altering the clients that use it.

7. **Builder Pattern:**  
   - **Usage:** Applied in methods like `updatePost()` and `createPost()` in `PostRepository`.  
   - **Purpose:** Gradually builds objects (e.g., `newPost` or `updatedPost`) by adding properties and modifying them step by step, ensuring flexibility and clarity.

---

## Tech Stack

### Frontend
- **React JS**: For building the user interface.
- **TypeScript**: For type safety and robust development.
- **Tailwind CSS**: For modern, responsive styling.
- **React Query**: For server-state management and API integration.

### Backend
- **Appwrite**: A self-hosted backend server providing APIs for authentication, database, storage, and more.

---

## Installation

Follow these steps to run OTJS locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/asef-sami/OTJS-Social-Web.git
