# search-app

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

axios({
  url: 'https://1jzxrj179.lp.gql.zone/graphql',
  method: 'post',
  data: {
    query: `
      query PostsForAuthor {
        author(id: 1) {
          firstName
            posts {
              title
              votes
            }
          }
        }
      `
  }
}).then((result) => {
  console.log(result.data)
});