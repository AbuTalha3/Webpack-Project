# Webpack-Project
developing a webpack project from documentation
<a name="readme-top"></a>

  <h1 align = "center"><b>WebPack Configurations</b></h1>

</div>


### Pre-requisites

Configure <a href="#">Linters</a>
 in main Branch.
 
### Step 1 (Files):
Create Three Files inside src folder that must be inside repo folder;
<ol>
<li>index.html</li>
<li>style.css</li>
<li>index.js</li>
</ol>

### Step 2 (Create WebPack File)
Create an webpack.config.js file inside repo folder.
```sh
 const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = {
  mode: 'development',
  entry: {
    index: './src/index.js',
  },
  plugins: [
    new HtmlWebpackPlugin({
      template: './src/index.html',
    }),
  ],
  output: {
    filename: '[name].bundle.js',
    path: path.resolve(__dirname, 'dist'),
    clean: true,
  },
  module: {
    rules: [
      {
        test: /\.css$/i,
        use: ['style-loader', 'css-loader'],
      },
    ],
  },
};
```

### Step 3 (Install WebPack):

```sh
 npm install webpack webpack-cli --save-dev
```

### Step 4 (Install style-loader and css-loader):

```sh
npm install --save-dev style-loader css-loader
```

### Step 5 (Install HtmlWebpackPlugin plugin):

```sh
npm install --save-dev html-webpack-plugin
```

### Step 6 (Install Webpack-dev-server):

```sh
npm install --save-dev webpack-dev-server
```

### Step 8 (Make Changes in package.json file):
Update scripts part of package.json with these lines!
```sh
"test": "echo \"Error: no test specified\" && exit 1",
"start": "webpack serve --open",
"build": "webpack"
```
### Step 9 (Run Following Command to Generate .dist/ folder):
```sh
npm run build
```
### Step 10 (Run Following Command to Run Project by WebPack Server):
```sh
npm start
```
### Setup
Clone this repository to your desired folder:
<!--
Example commands:

```sh
  cd my-folder
  git clone git@github.com:AbuTalha3/Webpack-Project.git
```
--->

<!-- AUTHORS -->

## 👥 Authors <a name="authors"></a>


👤 **Abu Talha**

- GitHub: [@AbuTalha3](https://github.com/AbuTalha3)
- Twitter: [@AbuTalha3](https://twitter.com/AbuTalha8T)
- LinkedIn: [@AbuTalha3](https://www.linkedin.com/in/abu-talha-8203b252/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGEMENTS -->

## 🙏 Acknowledgments <a name="acknowledgements"></a>

> Give credit to everyone who inspired your codebase.

I would like to thank Microverse!

<!-- LICENSE -->

## 📝 License <a name="license"></a>

This project is [MIT](./LICENSE) licensed.

_NOTE: we recommend using the [MIT license](https://choosealicense.com/licenses/mit/) - you can set it up quickly by [using templates available on GitHub](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-license-to-a-repository). You can also use [any other license](https://choosealicense.com/licenses/) if you wish._

<p align="right">(<a href="#readme-top">back to top</a>)</p>
