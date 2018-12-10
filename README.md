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
1. <b>app.yaml</b>: Configure the settings of your App Engine application.
1. <b>www/</b>: Directory to store all of your static files, such as HTML, CSS, images, and JavaScript.
1. <b>css/</b>: Directory to store stylesheets.
1. <b>style.css</b>: Basic stylesheet that formats the look and feel of your site.
1. <b>images/</b>: Optional directory to store images.
1. <b>index.html</b>: An HTML file that displays content for your website.
1. <b>js/</b>: Optional directory to store JavaScript files.
1. Other asset directories.


