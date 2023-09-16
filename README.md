# Video Transcription Prompt Application API

This API serves as the backend for a unique and interactive application that allows users to chat with uploaded videos using predefined prompts. Below, you'll find an index and essential information about the technologies used, prerequisites, usage, and how the API works.

## Content

- [Technologies Used](#technologies-used)
- [Prerequisites](#prerequisites)
- [Usage](#usage)
- [How It Works](#how-it-works)

## Technologies Used

### Fastify

Fastify is a fast and low overhead web framework for Node.js. It's highly efficient and suitable for building APIs. In this API, Fastify is used for routing and handling HTTP requests.

### Prisma

Prisma is an open-source database toolkit that simplifies database access with a type-safe and auto-generated query builder. It's employed here for managing database operations and interactions.

### Zod

Zod is a TypeScript-first schema validation and parsing library. It ensures that incoming requests and data conform to expected schemas, providing strong type checking and validation.

### Node.js Modules

Various Node.js modules, such as `fs` (File System), `path`, and `crypto`, are used for file handling, path manipulation, and generating unique identifiers.

### `ai` Library

The `ai` library is a custom module specifically developed for managing AI interactions within the API. It encapsulates the logic for communicating with AI services, handling AI completions, and facilitating the streaming of responses to clients.

## Prerequisites

Before you can run the Video Transcription Prompt Application API, ensure you have the following in place:

- **Node.js**: Install Node.js (version 14 or higher) on your server or development environment.

- **Database**: Configure and connect the API to a database system compatible with Prisma (e.g., PostgreSQL, MySQL).

## Usage

To use the API, follow these steps:

1. **Clone the Repository**: Clone this repository to your local machine or deploy it to a server.

   ```bash
   git clone https://github.com/your-username/your-api-repo.git
   cd your-api-repo
   ```

2. **Install Dependencies**: Install the required Node.js packages using npm.

   ```bash
   npm install
   ```

3. **Database Configuration**: Configure the API to connect to your database system. Update the database connection string in the Prisma configuration file (`prisma/client/`).

4. **Start the API**: Launch the API server using the following command:

   ```bash
   npm run dev
   ```

5. **API Endpoints**: The API exposes endpoints for video upload, transcription prompt creation, and AI completion generation. You can integrate these endpoints into your frontend or client application.

6. **Customization**: Customize the API to meet your specific requirements. You can extend functionality, add authentication, or integrate additional features as needed.

## How It Works

The Video Transcription Prompt Application API enables users to interact with video content through predefined prompts. Here's how it works:

1. **Video Upload**: Users can upload video files in MP3 format to the API. The uploaded videos are stored and associated with unique identifiers in the database.

2. **Transcription Prompt**: Users create transcription prompts by providing a video ID and a text prompt. The prompts may include a special variable `{transcription}`, which will be replaced with the video's transcription during AI interactions.

3. **AI Completion Generation**: Users send requests to generate AI completions based on their prompts. The API utilizes OpenAI or a similar service to generate text-based responses to the prompts. The AI completions are streamed back to the user.

4. **Custom Responses**: Users can create custom responses by defining prompts and adjusting parameters such as temperature to influence the AI's responses.

The API combines the power of Fastify for efficient routing, Prisma for database operations, Zod for schema validation, and the custom `ai` library for AI interactions to create a robust and flexible backend for the Video Transcription Prompt Application. It allows for innovative and engaging interactions with video content while offering easy customization and extension possibilities for diverse use cases.
