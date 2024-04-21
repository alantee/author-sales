
# Author Sales API

Author sales API project for Kirkey AI.

## Prerequisites

Before you begin, ensure you have met the following requirements:
- Node.js installed
- Redis installed on your machine

## Installing author-sales

To install author-sales, follow these steps:

### Backend Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/alantee/author-sales.git
   cd author-sales/backend
   ```

2. **Install Dependencies:**
   ```bash
   npm install
   ```

3. **Setting up Redis:**

   **Download and install Redis** (if not already installed):
   - Refer to [Redis's official documentation](https://redis.io/download) for installation instructions specific to your operating system.

   **Start Redis server**:
   - **Windows**:
     - Open your command prompt and run:
       ```bash
       redis-server
       ```
   - **macOS and Linux**:
     - Open your terminal and execute:
       ```bash
       redis-server
       ```
   This will start the Redis server using the default configuration file.

Ensure that Redis is running properly before proceeding with the next steps of the application setup.

4. **Run the application:**
   ```bash
   node app.js
   ```

### Frontend Setup

1. **Navigate to the frontend directory:**
   ```bash
   cd ../frontend
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Run the frontend application:**
   ```bash
   npm start
   ```
