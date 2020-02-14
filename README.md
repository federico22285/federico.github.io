# Federico

[![Build Status](https://travis-ci.org/pages-themes/hacker.svg?branch=master)](https://travis-ci.org/pages-themes/hacker) [![Gem Version](https://badge.fury.io/rb/jekyll-theme-hacker.svg)](https://badge.fury.io/rb/jekyll-theme-hacker)

*My blog. [Preview](https://federico22285.github.io/federico.github.io/).*

## Customizing

### Configuration variables

Hacker will respect the following variables, if set in your site's `_config.yml`:

```yml
title: [The title of your site]
description: [A short description of your site's purpose]
```

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

### Stylesheet

If you'd like to add your own custom styles:

1. Create a file called `/assets/css/style.scss` in your site
2. Add the following content to the top of the file, exactly as shown:
    ```scss
    ---
    ---

    @import "{{ site.theme }}";
    ```
3. Add any custom CSS (or Sass, including imports) you'd like immediately after the `@import` line

*Note: If you'd like to change the theme's Sass variables, you must set new values before the `@import` line in your stylesheet.*

### Layouts

If you'd like to change the new theme's HTML layout:

1. Create a new file called `/_layouts/page.html` in your site
2. Customize the layout as you'd like
3. Use it in frontmatter as 
    ```yml 
    layout:page 
    ```

### Adding Post

The next thing after you are done with the configuration file is to add your first post. You will need to have at least basic knowledge of HTML or Markdown.

All you need to do is to create a new file with name <code>YYYY-MM-DD-my-first-post</code> and <code>.markdown</code> or <code>.md</code> extension. Create it in the <code>_posts</code> folder. By default the name of the file is composed by date and title but you can overwrite these in the post's front matter.

In the beginning of the every post you have a so called [front matter](https://jekyllrb.com/docs/frontmatter/){:target="_blank"} block which contains some data about the post. Here is the short description of the options.

**layout**: The post layout.

**date**: Exact date when the post is published. The date is actually pretty important and I suggest you never change it. Specific date helps Jekyll to order correctly all the posts. Also, the date is used to generate a unique ID, so Disqus can always get the right comments for the right post, even when you change the title.

**title**: Post's title.

**description**: Meta description used for better SEO.

**author**: Adding Author for the post. By default "Federico" is set.

### Previewing the theme locally

I assume you have already downloaded and installed Ruby. Here's what you need to do next:

1. Run <code>gem install jekyll bundler</code>.
2. Copy the theme in your desired folder.
3. Enter into the folder by executing <code>cd name-of-the-folder</code>.
4. Run <code>bundle install</code>.
5. If you want to access and customize the theme, use <code>bundle exec jekyll serve</code>. This way it will be accessible on <code>http://localhost:4000</code>.
6. Upload the content of the compiled <code>_site</code> folder on your host server.

## Roadmap

See the [open issues](https://github.com/pages-themes/hacker/issues) for a list of proposed features (and known issues).

## Project philosophy

The Hacker theme is intended to make it quick and easy for GitHub Pages users to create their first (or 100th) website. The theme should meet the vast majority of users' needs out of the box, erring on the side of simplicity rather than flexibility, and provide users the opportunity to opt-in to additional complexity if they have specific needs or wish to further customize their experience (such as adding custom CSS or modifying the default layout). It should also look great, but that goes without saying.
