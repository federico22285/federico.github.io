---
layout: post
title: "Documentation - Configuration & First Steps"
---

### Configuration
All configuration options are in the <code>_config.yml</code> file.

<figure>
    <img src="https://cdn.dribbble.com/users/1073937/screenshots/5036567/waterfall.png" />
    <figcaption>Created by <a href="https://dribbble.com/HannahLizSharp" target="_blank_">Hannah Sharp</a></figcaption>
</figure>

##### General Settings
* **name**: Your name.
* **description**: Describe yourself with a couple of words.
* **know_as**: Everyone calls me by this name.
* **what_do_as**: About what you do.
* **live**: About where you live.
* **certificate**: Add about certificate.
* **team**: Add your team details.
* **github**: Add your Twitter links
* **linkedin**: Add your Twitter links
* **twitter**: Add your Twitter links
* **google_analytics**: Add your Google Analytics Tracking ID. Example ID: *UA-XXXXXXX-2*.

##### Serving
These options are pretty important, so take a closer look. If you experience any problems with your paths you should check them here.

* **url**: Enter your domain! Example: <code>https://mysite.com</code>
* **baseurl**: The baseurl can remain empty if you’re not going to host your site in a subfolder. But if you want your site to be something like <code>htttp://mysite.com/blog</code> you should write down <code>/blog</code> here.

##### Includes

* **include**: Force the inclusion of the pages directory. (Posts are by default inclusion)

##### Outputting

* **permalink**: By default your links will look like this <code>http://mysite.com/categories/post-name.html</code>. If you want a different permalink check [Jekyll documentation](https://jekyllrb.com/docs/permalinks/){:target="_blank"}.

##### Pagination
* **paginate_path**: The default path is <code>/page:num/</code>, so for example if you go to second page you will see something like this <code>http://mysite.com/page2/</code>.

**Important Note:** Pagination is currently working only on home page due to Jekyll limitations.

##### Conversion
* **markdown**: Choose your Markdown renderer. Different Markdown renderers supported by Jekyll sometimes have extra options available. I suggest to stick with the default.
* **excerpt_separator**: By default when you're writing a post, you should add <code>&lt;!--more--&gt;</code> to define excerpt. You have three options - to leave it as is, to change the tag or to completely remove it but in this case you'll always see the full content.

##### Assets Settings
* **sass**: Choose the path to all of yours SCSS partials and the compression method for the final file.

If you need extra help, just check out the [official Jekyll documentation](https://jekyllrb.com/docs/home/){:target="_blank"}.


### Adding Post

The next thing after you are done with the configuration file is to add your first post. You will need to have at least basic knowledge of HTML or Markdown.

All you need to do is to create a new file with name <code>YYYY-MM-DD-my-first-post</code> and <code>.markdown</code> or <code>.md</code> extension. Create it in the <code>_posts</code> folder. By default the name of the file is composed by date and title but you can overwrite these in the post's front matter.

In the beginning of the every post you have a so called [front matter](https://jekyllrb.com/docs/frontmatter/){:target="_blank"} block which contains some data about the post. Here is the short description of the options.

**layout**: The post layout.

**date**: Exact date when the post is published. The date is actually pretty important and I suggest you never change it. Specific date helps Jekyll to order correctly all the posts. Also, the date is used to generate a unique ID, so Disqus can always get the right comments for the right post, even when you change the title.

**title**: Post's title.

**description**: Meta description used for better SEO.

**author**: Adding Author for the post. By default "Federico" is set.

That's it! Do not hesitate to ask if you have any questions. Happy blogging!