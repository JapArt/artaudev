---
layout: post
title:  "How to install Ruby on Rails on Windows WLS"
date:   2020-01-03 10:02:55 -0500
author: Juan Artau
---

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

## Asi es como se hace un header mas grande que le contenido del sitio ##

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
  # All Devise controllers are inherited from here.
  class DeviseController < Devise.parent_controller.constantize
    include Devise::Controllers::ScopedViews

    def cool(variable)
      variable
    end

    if respond_to?(:helper)
      helper DeviseHelper
    end

    if respond_to?(:helper_method)
      helpers = %w(resource scope_name resource_name signed_in_resource
                 resource_class resource_params devise_mapping)
      helper_method(*helpers)
    end

    prepend_before_action :assert_is_devise_resource!
    respond_to :html if mimes_for_respond_to.empty?
  end
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
