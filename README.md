# Book Management MongoDB Shell

This project involves working with MongoDB using the MongoDB shell (`mongosh`). The instructions below detail how to start the MongoDB shell, execute various commands, and manage a sample database.

---

## Prerequisites

Ensure the following are installed and set up on your system:

- **MongoDB**: Ensure the database server is running.
- **MongoDB Shell (`mongosh`)**: The CLI tool for interacting with MongoDB.

---

## Starting the MongoDB Shell

1. Open a terminal (or command prompt).
2. Start the MongoDB server (if not already running):
   ```bash
   mongod
 3. Open a new terminal window or tab, and start the MongoDB shell:
mongosh
test>
This indicates the shell is ready for commands.

## MongoDB Shell Commands
1. Switching to a Database
 ### use LibraryDB;

2. Inserting Data
db.Books.insertMany([{
  _id: 1,
  title: "1984",
  author: "George Orwell",
  genres: ["Dystopian", "Political Fiction"],
  published_year: 1949,
  available: true
}]);
3. Insert multiple documents:

db.Patrons.insertMany([
  { _id: 1, name: "Alice Johnson", email: "alice@example.com", borrowed_books: [] },
  { _id: 2, name: "Bob Smith", email: "bob@example.com", borrowed_books: [1, 2] }
]);
4. Querying Data
Retrieve all documents in a collection:

javascript
Copy code
db.Books.find();
Find documents matching specific criteria:

javascript
Copy code
db.Books.find({ author: "George Orwell" });
5. Updating Data
## a single document:
db.Books.updateOne(
  { _id: 1 },
  { $set: { available: false } }
);
## update multiple documents:

db.Books.updateMany(
  { available: true },
  { $set: { available: false } }
);
6. Deleting Data
## Drop a collection:

db.Books.drop();
Delete a single document:

db.Patrons.deleteOne({ _id: 1 });
## Delete multiple documents:


db.Books.deleteMany({ available: false });
7. Listing Collections
## View all collections in the current database:

show collections;
8. Viewing All Databases
List all databases:
show dbs;

### screen short
### 1. MongoDB Shell Connection
![MongoDB ](/dase.pretty.png)

### 2. Database Creation
![Database Creation](/fra.png)
### 3. MongoDB Shell Connection
![MongoDB](/image1.png)

### 4. Database Creation
![Database Creation](/preety.png)

![Database Creation](/show.png)

