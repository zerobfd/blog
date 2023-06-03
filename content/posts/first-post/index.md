---
title: "First Post"
date: 2023-06-03T13:46:11-07:00
---

Before anything else, I want to write a bit about how I've set things up on the
site. At some point later I'll write about why I set it up this way.

The blog is published as a git archive on GitHub. I use a static site generator
(Hugo) to publish the content from markdown files.  Each commit is signed with
a GPG key that's associated with my GitHub account, and the public key can be
found in the repo and on keyservers. After committing, I use OpenTimestamps to
generate a trusted timestamp, and then commit the resulting OTS file for
verification to the archive as well.

In this way, I think I can count on the following guarantees being held:

 * git ensures that the integrity of the blog is kept
 * signing the commits ensures that I'm actually the one making updates
 * OpenTimestamps ensures that posts are immutable once committed and published

I'm not a security expert, but I'm reasonably confident that at least after
the first few updates to the blog, it would require an unreasonable amount of
effort to fake content or rewrite history.

My intent is to have largely two types of content here: one are posts, which
are written addressing some external audience about some topic(s) that I want
to write about. The second is a Zettelkasten-style knowledge base linking
together a bunch of stuff that ends up in my head. Posts I intend to be write-
once, update never or rarely, and order chronologically. In contrast, the kb
articles may be updated, renamed, or deleted; they may make no sense to anyone
(including me); there is no natural ordering.

As of the initial writing, I don't think there's a standard a way to generate
backlinks between pieces with Hugo, so the implementation of intent may end up
diverging a bit from what's written here. We'll see.
