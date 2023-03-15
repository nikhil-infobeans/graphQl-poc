# graphQl-poc

# Setup

#### Step 1: clone git repo

```
git clone https://github.com/nikhil-infobeans/graphQl-poc.git
```

#### Step 2: Run npm install command

```
npm install
```

#### Step 6: Run application (Default port number is 5005)

```
npm run dev
```

# Execute GraphQl API - http://localhost:5005/graphql


#### 1: List All the books
```
{
  books {
    id,
    name
  }
}
```
#### 2: List All the books with Author Information
```
{
  books {
    id,
    name,
    author {
      id,
      name
    }
  }
}
```
#### 3: Get specific Book with Author Information
```
{
  book(id:1) {
    id,
    name,
    author {
      id,
      name
    }
  }
}
```
#### 4: Get specific Author with his books Information
```
{
  author(id:1) {
    id,
    name,
    books {
      id,
      name
    }
  }
}
```
#### 5: Add New Book
```
mutation {
  addBook(name: "New Book", authorId: 10) {
    id,
    name
  }
}
```
#### 5: Add New Author
```
mutation {
  addAuthor(name: "New Author") {
    id,
    name
  }
}
```



