# SimpleJSwidget
Simple JS widget

## Inicia:
``` 
npm init
``` 

## Install:
``` 
npm install --save-dev webpack webpack-dev-server webpack-cli sass-loader node-sass css-loader style-loader postcss-loader uglifyjs-webpack-plugin html-webpack-plugin cssnano autoprefixer
```
```
npm install babel-loader @babel/core @babel/preset-env --save-dev
```

## Build
```
npm run build
```

## Publicar NPM package
You can publish your package on NPM in 3 easy steps.

Crea una cuenta en npmjs.com
Logueate en npm en tu terminal con:
```
npm login
```
Publicalo con: 
```
npm publish
```
## Publícalo en un CDN:
As a link (hosted on a CDN)
To achieve this, we will use unpkg. Unpkg is a free CDN that hosts your npm packages. Once published, you can get a link to your package using their service.

All you have to do is adding the following lines to your package.json:

```
  "unpkg": "dist/plugin-name.min.js",
  "files": [
    "dist"
  ],
```
The first line tells unpkg the file to serve, and the last 3 lines tell npm to add the dist folder in the package. (if you ignored it in the .gitignore file)

## El ejemplo subido al CDN quedaría:
https://unpkg.com/simplejswidget@1.0.1/dist/simplejswidget.min.js

___________________________________
___________________________________

# El código a integrar dentro de otra web es:
```html
<todo-list>
</todo-list>
<script type="text/javascript" src="https://unpkg.com/simplejswidget@1.0.1/dist/simplejswidget.min.js"></script>
```