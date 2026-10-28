# aws_server

A small Node.js + Express server written in TypeScript. The `/` endpoint returns `Hello World`, and the port is configured through `.env`.

## Requirements

- Node.js (LTS recommended)
- npm

## Run locally

1. Extract the ZIP and open the `aws_server` folder in your terminal.
2. Install dependencies:

   ```bash
   npm install
   ```

3. Check that the `.env` file contains:

   ```env
   PORT=3000
   ```

4. Start the development server:

   ```bash
   npm run dev
   ```

5. Open `http://localhost:3000` in your browser or send a GET request using Postman.

Expected response:

```json
{
  "success": true,
  "message": "Hello World"
}
```

## Build and run

```bash
npm run build
npm start
```

The compiled JavaScript is generated in `dist/`.

## Project structure

```text
aws_server/
├── src/
│   ├── app.ts       # Express app and routes
│   └── server.ts    # Loads .env and starts the server
├── .env             # Local environment variables
├── .env.example     # Example environment configuration
├── .gitignore
├── package.json
├── tsconfig.json
└── README.md
```

Do not commit `.env` if it contains secrets. The `.env` file here only sets the local port.
