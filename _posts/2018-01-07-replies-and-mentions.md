---
title: "Replies and @-mentions"
date: 2018-01-07
description: Referencing users in a post.
order: 5
categories: getting-started
---
Because Micro.blog is based on blogs, replying and mentioning other users does not work the same way as other social networks you may be used to. We've tried to build a system that is flexible enough to work with Micro.blog-hosted sites and external blogs.

There are several rules for processing replies and mentions:

* If you click or tap "Reply" on a post with Micro.blog, it stores the reply separately from your blog. We do this because you may not want replies to show up on your web site alongside other regular blog posts. Micro.blog includes the reply in the timeline and Mentions section for any user referenced in the post.

* When replying to a post that is on an external blog, Micro.blog will attempt to send a Webmention to that blog post. We've documented [more about Webmention support here](/2017/webmention/).

* If you post to your Micro.blog-hosted blog and include `@username` somewhere in the post, Micro.blog automatically converts that into a Markdown link to the Micro.blog user. Micro.blog also includes that mention in the user's timeline and Mentions section.

* For blogs hosted externally to Micro.blog, such as with WordPress, you are responsible for linking usernames for Micro.blog users you want to mention. Just including `@username` without a link will have no effect. It should be something like `<a href="https://micro.blog/username">@username</a>` to indicate to Micro.blog that a specific user should be notified. Micro.blog does not automatically link any text in external blog posts. (By adding links yourself, posts will show up correctly not just on Micro.blog but also on your web site and in feed readers.)

* For an external blog post that is a reply to a specific Micro.blog post, the external blog can send a Webmention to Micro.blog. As long as the sending blog is associated with a Micro.blog user, that post will be copied to Micro.blog as a reply and threaded into the conversation. Micro.blog's Webmention endpoint is: `https://micro.blog/webmention`

If you're signed in to Micro.blog, you can [export your replies here](https://micro.blog/account/export/replies) in JSON Feed format. Any @-mentions for hosted blogs (where the text does not start with a username) can be found in your microblog archive.
