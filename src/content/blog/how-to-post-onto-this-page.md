---
title: "How to publish a post on this page"
description: "A how-to guide to publish a new post on this page"
published: "1735273160000"
heroImage: "https://cdn.hrsn.net/blog/2024/07/20/banner.png"
author: "akk1to.dev"
---
*This post will show you how to publish a new post on this blog, hosted by ChuyenTin Organisation. Note that you need to make a new PR on the exact post folder to publish a new post onto this page.*
*This page was made and maintained by akk1to.dev (idea from [Willam Harrison's blog](https://blog.wharrison.com.au/))*

## 1. Generate ideas & write a new post
First, generate your ideas and write a new post using Markdown format. You can use popular Markdown editors like [StackEdit](https://stackedit.io) or [Visual Studio Code](https://code.visualstudio.com) to assist you in writing. For every post, be sure to follow the specified file format to ensure that your post is clearly displayed on the page.
```md
---
title: "(your post title goes here)"
description: "(your post description goes here)"
published: "(formatted date, see how to get it below)"
heroImage: "(banner of the post, delete this line if you want to make it random)"
---
(your post content below here)
```
Our post system uses a formatted time method, called Unix timestamp in seconds. You can use online tools to encode the date to Unix timestamp in seconds format such as [EpochConverter](https://epochconverter.com/) to encode it and put inside the file.
<p align="center">
    <img src="https://i.imgur.com/mpMGO1w.png"></img>
    <i>EpochConverter homepage</i>
</p>
To put image in this post, you can upload it onto imgur and stick it in the post using these methods.

```md
![image](https://i.imgur.com/mpMGO1w.png)
```
<p align="center"><i>An example using ![image] tag in markdown</i></p>

```html
<p align="center">
    <img src="https://i.imgur.com/mpMGO1w.png"></img>
</p>
```
<p align="center"><i>An example using HTML tags to center the image</i></p>

You can check out [this link](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) to know how to write a markdown file.
Once you're ready, move to step 2 to post your blog post onto the page.

Navigate to the [`domains/`](https://wdh.gg/borLkD3) folder and then from there click the `Add file` button and selecting the `Create new file option`.

If it says you need to fork the repository, click the fork repository button and continue with the next steps on your forked repository.

![image](https://cdn.hrsn.net/blog/2024/07/20/Ll3qnqmY.png)

Next, add the file name near the top where it says `Name your file...`. Name your file the name of the subdomain you want, in my case I want `william.is-a.dev`, so I will name the file `william.json`.

Here are the naming requirements:

- It must be more than 2 characters long but less than 64 characters
- It cannot contain underscores, only dashes are permitted
- You can only use standard English characters

![image](https://cdn.hrsn.net/blog/2024/07/20/0GgRMCHy.png)

After naming your file you need to put the JSON content into it, here is an example JSON structure:

```json
{
    "owner": {
        "username": "your-github-username",
        "email": "your@email.address"
    },
    "record": {
        "RECORDTYPE": "RECORDCONTENT"
    }
}
```

- Replace `your-github-username` with your GitHub username.
- Replace `your@email.address` with your email address.
- For `RECORDTYPE` set it to what you need, is-a.dev supports `A`, `AAAA`, `CNAME`, `MX` and `TXT` records. If your website is using GitHub Pages set this to `CNAME`.
- For `RECORDCONTENT` set this to the value of the record you need, for GitHub Pages this would be `your-github-username.github.io`. (`A`, `AAAA` and `MX` records **must** be an array `[]`.)

Finally, click `Commit changes...` and then `Propose changes`.

## 2. Creating your pull request

Now you should be greeted with a screen which looks like this:

![image](https://cdn.hrsn.net/blog/2024/07/20/EXLugHC9.png)

All you need to do here is fill out the requirements and place an `x` between the `[ ]` (so it looks like `[x]`) for each requirement you meet. Please make sure you meet all the requirements before creating the pull request.

Once you have filled out the requirements you can then click the `Create pull request` button and you're done!

## 3. Waiting...

Since you have created your pull request, you will need to wait for a maintainer to merge it before you domain name becomes active. Make sure to keep an eye on your pull request incase one of the maintainers requests changes.

**_Your pull request will normally be merged with-in 12-24 hours, however in some cases it may take longer. Please be patient as the maintainers are very busy._**

Once your pull request is merged you should be good to go! [Open an issue](https://wdh.gg/r1Xw34w) if you run into any trouble.

Congratulations you have successfully setup your free is-a.dev subdomain!

_Make sure to join the is-a.dev [Discord server](https://wdh.gg/WxDO6wi) for announcements regarding the service._
