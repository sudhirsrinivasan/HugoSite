---
title: "How to make sure google indexes your site"
date: 2023-11-13T11:48:24+05:30
draft: false
---


## To get google to start indexing my website


I verified my ownership of site with google to make sure it starts indexing it  https://support.google.com/webmasters/answer/9008080
using directions provided here.
https://support.google.com/a/answer/6149686?hl=en


## noindex
Here is an issue I faced.
After verifying my ownership I logged into [google search console](https://search.google.com/search-console) to check on the performance. I saw this warning 
![noindex](/images/google-noindex.png)


To debug this I followed instructions [here](https://support.google.com/webmasters/answer/7440203#blocked_by_noindex_tag)

The problem was that the default ananke theme I had used was adding a noindex which I confirmed by checking the source html. 

![noindex](/images/source-noindex.png)


I fixed it by changing themes (which I was planning to do anyways). You can also simply search for the file in your themes directory which has the noindex and remove it and regenerate the html by running hugo to fix it.