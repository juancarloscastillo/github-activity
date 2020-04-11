# GitHub Activity Stream Widget

This is a small Javascript plugin that creates a stream of your recent GitHub activity.
It is a slightly modified and simplified version of this plugin from [Casey Scarborough](https://caseyscarborough.github.io/github-activity).

An example of how it looks like is [here](https://juancarloscastillo.github.io/jc-castillo/documents/github-activity/probwidgetgithub.html)

To add it to your webpage:

1. Just copy and paste this to the head of your html file. Replace below the username and repository you want to show:

```html
<link rel="stylesheet" href="//cdnjs.cloudflare.com/ajax/libs/octicons/2.0.2/octicons.min.css">
<link rel="stylesheet" href="https://raw.githubusercontent.com/juancarloscastillo/github-activity/master/github-activity-0.1.5.min.css">

<script src="//code.jquery.com/jquery-1.11.0.js"></script>
<script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/mustache.js/0.7.2/mustache.min.js"></script>
<script type="text/javascript" src="https://raw.githubusercontent.com/juancarloscastillo/github-activity/master/github-activity-0.1.5.min.js"></script>

<script>
GitHubActivity.feed({
	username: "juancarloscastillo",
	repository: "cienciasocialabierta", // optional
	selector: "#feed",
	limit: 20 // optional
});
</script>

```

... **or**, if you are working with Rmarkdown, download [this html file](https://raw.githubusercontent.com/juancarloscastillo/github-activity/master/demo-Rmarkdown/head_github-activity.html), replace the username and repository, and include it in the YAML header:

```
---
title: "Demo Rmarkdown GitHub Activity Widget"
output:
  html_document:
    includes:
      in_header: head_github-activity.html
---

```


2. In the body of your html (or in your Rmarkdown file) add the following where you want the plugin:

```html
<div id="feed"></div>
```
