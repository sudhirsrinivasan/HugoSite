---
title: "How This Works"
date: 2023-11-01T19:39:18+05:30
draft: false
---

# Introduction

This is my first  post on how this website is built. I am planning to  documenting the progress of how I am setting things up. I am writing this so my kids can use this :) so hoping the explanations are detailed enough. 


# Choices I made
## Build/host my website vs use blogging software
I considered various blog/email software like medium and substack but decided to build my own site rather than use blog/email sites like [Medium](https://medium.com/)   or [Substack](https://substack.com/). 
<!--- TODO - Potential Post here --->

## Site Generator
After years of working in the software industry I have come to appreciate the simplicity of generating html content as opposed to having a backend. My goal is to see how much I can retain the core of a site that is generated html content but try to add dynamic components to it. 
<!--- TODO - Potential Post here --->

## Choice of Site Generator
After evaluating a few I decided to go with [Hugo](https://gohugo.io) 
<!--- TODO - Potential Post here --->

## Hosting 
I will be hosting it on AWS and for a start I plan to use AWS Amplify amongst other services.  


# How I built it 
Here is a rough picture of the pieces involved. With this setup you can create html and view it on your laptop/desktop using hugo and then publish the html to a github repository which is then picked up using AWS Amplify to publish it so everyone can see it. 

![Setup](/HugoMacSetup.svg)



## Setup your local desktop/laptiop Mac
1. For Mac  [Install brew](https://brew.sh/) and [Install hugo](https://gohugo.io/installation/) 
1. PC ->  [Instructions for windows](https://www.techielass.com/how-to-install-hugo-on-windows-10/)



## Githup and access to github account from Mac
1. Create a github account
1. Follow instructions to setup ssh access to your github account [here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) to setup my access of github from mac. This [video](https://www.youtube.com/watch?v=jkXIzjiF72g&list=PL7slAxcLWlcAqykFVFaBj_B2HEoJ4E1TH&index=2) also describes the same process but is a bit dated. It uses rsa instead of the newer ed25519 algorithm


## Getting started with Hugo 

I created a repository on github called HugoSite. Then git cloned it and ran ran hugo new site with a --force option since the directory already existed

1. git clone git@github.com:sudhirsrinivasan/HugoSite.git
1. cd HugoSite
1. hugo new site . --force 


After that followed directions from [here](https://gohugo.io/getting-started/quick-start/) except for the steps above so I did not have to git init. Also if you see this warning "found no layout file for" follow directions from [here](https://stackoverflow.com/questions/60269683/how-to-fix-the-error-found-no-layout-file-for-html-for-page-in-hugo-cms)

Once you follow above instructions and are able to see your website on your local you can push changes to github using the commands below 
1. git add --all
1. git push 



## Hosting on Amplify
1. Create an AWS account 
1. Followed these [directions](https://gohugo.io/hosting-and-deployment/hosting-on-aws-amplify/) except for two things  

    1. I had to do the force amplify  to use the newer version of hugo and to do that I followed [these directions](https://gohugo.io/hosting-and-deployment/hosting-on-aws-amplify/#using-a-newer-version-of-hugo) 
    1. Also I edited the build file on amplify to add hugo as a command and public directory. 
    1. Amplify will give you a URL but you can also register your DNS using route 53 and then assign use that. 

## Purchasing a DNS using Route 53 
I then purchased a [domain name using Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/domain-register.html) 
There were cheaper options than route 53 but I did not want to maintain one more account. 
Then I added the Domain to the amplify app using [directions here](https://docs.aws.amazon.com/amplify/latest/userguide/to-add-a-custom-domain-managed-by-amazon-route-53.html).


## Tada

[sudhirsrinivasan.net](http://sudhirsrinivasan.net)

## To get google to start indexing my website

I verified my ownership of site with google to make sure it starts indexing it  https://support.google.com/webmasters/answer/9008080
using directions provided here.
https://support.google.com/a/answer/6149686?hl=en













