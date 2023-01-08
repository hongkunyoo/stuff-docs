---
hide:
  - navigation
  - toc
---
# stuffbox

<!-- ![](logo.png){ width=80px; } -->

Get your stuff out of the box.

## Motivation

I always needed some easy way to get my frequently used configurations and files in the middle of development. (NGINX conf, K8s Deployment template, etc) </br>
For example,

```bash
curl mywebsite.com/deploy-template.yaml > deploy.yaml
```

So I made stuffbox to do the work.

## How to

1. Make Github Repo named `stuffbox`. (public or private)
2. Stuff your frequently used files.
3. Run following script to get your file anywhere you want.

```bash
curl -sL stuffbox.io/$YOUR_GIT_REPO/$YOUR_FILE | sh
```

if you want to list your stuffbox, just type `$YOUR_GIT_REPO`.

```bash
curl -sL stuffbox.io/$YOUR_GIT_REPO | sh
```

## FAQ

### 1. Why do I need to use stuffbox, given that I already know how to use git?

Yes, you can use git by yourself to get your own stuff.</br>
stuffbox is just a small protocol to get your files easily on any server.
If you follow the protocol, you can get an easy access point to get your stuff.

To be honest, stuffbox was started just for me to remember the exact git repo that I have stored my stuff.
I always forgot whether I named my repo as "mystuff[s]" or "stuff[s]".

So I decided to get a DNS to remember my repo name. Now, I don't forget it.


### 2. How do I believe whether my files are safe?

Just print out the command and look for yourself!

```bash
curl -sL stuffbox.io/$YOUR_GIT_REPO/$YOUR_FILE
```

There is no such backend that intercepts your file in the middle of the request.
All execution runs on your client computer.
