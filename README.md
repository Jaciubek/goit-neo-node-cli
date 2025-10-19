# node_tasks

# Homework. Topic 2. Creating Console Applications



## Step 1

Create a repository named goit-node-cli, clone it, and initialise a project inside using the command npm init. Add the commander package as a project dependency.
Place the files from the src folder into the root of your project.


## Step 2

In the contacts.js file, import the fs module (the version that works with promises — fs/promises) and path for working with the file system.
Create a variable called contactsPath and assign it the path to the contacts.json file. Use methods from the path module to construct the path.
Add asynchronous functions to manage the contacts collection. In these functions, use the fs module and its methods readFile() and writeFile(). Each function should return the required data using the return statement. Console output must not be included in these functions.
Export the created functions.

```
*// contacts.js/*
 * Uncomment and assign a value
 * const contactsPath = ;
 */*async function listContacts() {
  *// ...your code. Returns an array of contacts.*
}

async function getContactById(contactId) {
  *// ...your code. Returns the contact object with the given id. Returns null if the contact with such an id is not found.*
}

async function removeContact(contactId) {
  *// ...your code. Returns the deleted contact object. Returns null if the contact with such an id is not found.*
}

async function addContact(name, email, phone) {
  *// ...your code. Returns the added contact object (with id).*
}

```


## Step 3

Import the functions from contacts.js into the index.js file.
Then use the provided invokeAction() function, which receives the type of action to perform and the necessary arguments. The function should call the corresponding method from the contacts.js file, passing the required arguments. The result of the called function should be printed to the console.


## Step 4

Run the following commands in the terminal to ensure the code works as expected:

```

*# Retrieve and display the full list of contacts as a table (console.table)*
node index.js -a list

*# Retrieve a contact by ID and display the contact object or null if no contact with such ID exists.*
node index.js -a get -i 05olLMgyVQdWRwgKfg5J6

*# Add a contact and display the newly created contact object in the console*
node index.js -a add -n Mango -e mango@gmail.com -p 322-22-22

*# Remove a contact and display the deleted contact object or null if no contact with such ID exists.*
node index.js -a remove -i qdggE76Jtbfd9eWJHrssH

```