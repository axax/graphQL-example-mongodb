# GraphQL-MongoDB-Example

All the important code is in `src/start.js`.

Install, build and run:

```
yarn install
yarn run build
yarn start
```

For Local Development 

You need to start Mongodb for Local development 

```
npm run startdev
```

query {
  posts {
    _id
    title
    content
  }
}

query {
  posts {
    _id
    title
    content
    comments {
      _id
      postId
      content
      post {
        _id
        title
        content
      }
    }
  }
}

mutation {
  createPost(title:"hello", content:"world") {
    _id
    title
    content
  }
}

mutation {
  createComment(postId: "5de3d87687cf8d26aed11403", content: "I like the way you say hello world.") {
    _id
    postId
    content
  }
}
