---
title: "How This Works"
date: 2023-11-01T19:39:18+05:30
draft: false
---

## Introduction

This is a post on how this website is built. I am back to building software in my spare time and I wanted to start documenting the progress. I considered various blog/email software like medium and substack but decided to build my own since I will own the data and I enjoy the building process.  

## Site Generator
After years of working in the software industry I have come to appreciate the simplicity of generating html content. My goal is to see how much I can retain the core of a site that is generated html content but try to add dynamic components to it. I will be hosting it on AWS using amplify. 

## Choice of Site Generator
After looking at a few I decided to go with [Hugo](https://gohugo.io) 


## Setup of mac 

Installed brew
Installed hugo 
Created a github account
Created an AWS account 

## Setup SSH to access github
Used https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

ed25519
https://www.youtube.com/watch?v=jkXIzjiF72g&list=PL7slAxcLWlcAqykFVFaBj_B2HEoJ4E1TH&index=2 good video but uses rsa vs ed25519

## Getting started with Hugo 
I followed this https://gohugo.io/getting-started/quick-start/
But with one difference. I created a repository on github. Then git cloned it git clone git@github.com:sudhirsrinivasan/HugoSite.git
Then I ran hugo new site HugoSite --force 
Also after making the changes 
git add --all
git push 



## Hosting on Amplify

I followed this website - https://gohugo.io/hosting-and-deployment/hosting-on-aws-amplify/  
But one key point here. I had to do the force amplify to use the newer version https://gohugo.io/hosting-and-deployment/hosting-on-aws-amplify/#using-a-newer-version-of-hugo 
Also I edited the build file on amplify to add hugo as a command and public directory 











