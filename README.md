Welcome to api-js.
===================


Hey! I'm Josh. This is the github repo for my latest project **api-js**. **Api-js** is a javascript library built for people who want to access apis without writing complex scripts for days.

I designed **api-js** to save people time, and allow all developers to access the fantastic json apis out there. I first started building **api-js** for my own use whilst building a Reddit web application.

What is it? How does it work?
-------------

**api-js** provides you with a set of javascript functions to easily, and quickly use apis in your code.

> **Note:**

> - **api-js** is still in development.
> - Not All Planned Functions Have Been Implemented Yet. Please Check Here Lately for New Updates
> - Currently Only Supports JSON apis.

#### The Code Explained
##### GET-ting JSON Apis. (Such as Reddit and Github)
  To get a basic JSON Api you use this syntax:
  ```
   getJSON(url, successfunction);
   ```
  Where URL is the URl of the Api (eg. http://api.reddit.com/r/aww/top)
  And Where Succesfunction is the function to be called with the Returned JSON
#### <i class="icon-file"></i> How To Add it To Your Code?

```
// Its Easy! Set Up a Normal HTML Document.
<html>
  <head>
    // And Add:
    <script src = "api.js"></script>
    // Inside Your Header
  </head>
  <body>
    ...
```

### A Basic Demo

GitHub's fenced code blocks are also supported with **Highlight.js** syntax highlighting:

```
<body>
    <h1> Demo A. </h1>
    <div id="Container"></div>
    <script>
        //Get JSON Function - Part of my API JS Library - Gets the JSON Data from the Reddit Api with the Current Top Posts In /r/aww.

        getJSON('http://api.reddit.com/r/aww/top', success);
                //URL                             //Function To Be Called With Response
        function success(data) {
            console.log("hi");
            redditLinks = data;
            redditPosts = redditLinks.data.children;

            for (i = 0; i < redditPosts.length; i++) {
                Post = redditPosts[i].data;
                document.getElementById("Container").innerHTML += "<a href = '" + Post.url + "'>" + Post.title + "</a><br>";
            }
        }
    </script>
</body>
```
What Really Shows How Useful **api.js** can be is this demo:
  Using a question on stackoverflow (http://stackoverflow.com/questions/10341135/example-of-using-github-api-from-javascript) asking for help using the github api the simple solution required 8 lines of code, mine required 2 and produces perfectly readable code.
```
 getJSON('https://api.github.com/users/funchal', function myfunction(data) {
            console.log(data.name + " has " + data.public_repos + " public repositories!"); });
```
> **Tip:** To use **Prettify** instead of **Highlight.js**, just configure the **Markdown Extra** extension in the <i class="icon-cog"></i> **Settings** dialog.

> **Note:** You can find more information:

> - about **Prettify** syntax highlighting [here][5],
> - about **Highlight.js** syntax highlighting [here][6].


### Support My Library

Please Support My Project By Using it!

