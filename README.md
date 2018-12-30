# Deploy Static Web App in Google App Engine
You can use Google App Engine to host a static website. Static web pages can contain client-side technologies such as HTML, CSS, and JavaScript.

## Before you begin
1. Create a new GCP [Console project](https://console.cloud.google.com/project)
2. Install and then initialize the Google Cloud SDK: [Click Here](https://cloud.google.com/sdk/docs/)


## Creating a website to host on Google App Engine
### Basic structure for the project
This guide uses the following structure for the project:
.
 * app.yaml
 * www/
   * css/
   * js/
   * img/
   * index.html

#### Details
1. <b>`app.yaml`</b>: Configure the settings of your App Engine application.
1. <b>`www/`</b>: Directory to store all of your static files, such as HTML, CSS, images, and JavaScript.
1. <b>`css/`</b>: Directory to store stylesheets.
1. <b>`style.css`</b>: Basic stylesheet that formats the look and feel of your site.
1. <b>`img/`</b>: Optional directory to store images.
1. <b>`index.html`</b>: An HTML file that displays content for your website.
1. <b>`js/`</b>: Optional directory to store JavaScript files.
1. Other asset directories.


### Creating the app.yaml file
The `app.yaml` file is a configuration file that tells App Engine how to map URLs to your static files. In the following steps, you will add handlers that will load `www/index.html` when someone visits your website, and all static files will be stored in and called from the `www` directory. 

`app.yaml` file 

```js
runtime: python27
api_version: 1
threadsafe: true

handlers:
- url: /
  static_files: www/index.html
  upload: www/index.html

- url: /(.*)
  static_files: www/\1
  upload: www/(.*)
```

### Creating the index.html file
  Create an `HTML` file that will be served when someone navigates to the root page of your website. Store this file in your `www`   directory.

  `index.html` file

  ```html
  <html>
    <head>
      <title>Hello, world!</title>
      <link rel="stylesheet" type="text/css" href="/css/style.css">
    </head>
    <body>
      <h1>Hello, world!</h1>
      <p>
        This is a simple static HTML file that will be served from Google App
        Engine.
      </p>
    </body>
  </html>
  ```
  
### Deploying your application to App Engine
Use command in GCP SDK with the dir
`gcloud app deploy`

### View the Web Application
`gcloud app browser`

