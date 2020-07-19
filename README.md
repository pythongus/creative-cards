# creative-cards-2

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### Adding the Project to Heroku

Follow the guidelines in [Vue.js documentation](https://cli.vuejs.org/guide/deployment.html#heroku)

In a nutshell:

1. Create a `static.json` file and add to Git repository

```
{
  "root": "dist",
  "clean_urls": true,
  "routes": {
     "/**": "index.html"
  }
}

```

2. Add required modules using Heroku CLI

```
heroku buildpacks:add heroku/nodejs --app <app's name> 
heroku buildpacks:add https://github.com/heroku/heroku-buildpack-static --app <app's name>
```
