
# Author Sales API

Author sales API project for Kirkey AI.

## Prerequisites for local development

Before you begin, ensure you have met the following requirements:
- Node.js installed
- Redis installed on your machine
- PostfreSQL installed

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
### Database Setup

1. **Install PostgreSQL**:
   - [Download](https://www.postgresql.org/download/) and install PostgreSQL.
2. **Create your database**:
   ```bash
   createdb mydatabase
3. **Create required Tables**

   - Ensure the following tables are created in the database before adding test data:

   ```sql
   CREATE TABLE authors (
     id serial PRIMARY KEY,
     name text,
     email text,
     date_of_birth timestamp
   );

   CREATE TABLE books (
     id serial PRIMARY KEY,
     author_id integer REFERENCES authors (id),
     isbn text
   );
   
   CREATE TABLE sale_items (
     id serial PRIMARY KEY,
     book_id integer REFERENCES books (id),
     customer_name text,
     item_price money,
     quantity integer
   );

### Local Development

1. **Configuration Updates**
   - After setting up database be sure to update backend app.js with the login credentials for the PostgreSQL db.
     ```javascript
     const pool = new Pool({
       user: '<yourUserName>',
       host: 'localhost',
       database: '<yourDbName>',
       password: '<password>',
       port: 5432,});

