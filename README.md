# Blogger
[Example](http://morganmart.in/blog/)

Blogger is a simple blog generator written in ruby. It uses erb templates to display blog content supplied by the user (you!) in a stylish and simple way. It is meant to be quick and easy to setup and start using.

## How to use it

First, clone the repo. [Ruby](https://www.ruby-lang.org/en/) and [Less](http://lesscss.org/) are required to use it. Also, if code highlighting is required ([like this](https://camo.githubusercontent.com/a946613f77ac8eb7987446b5f4ef325844817480/68747470733a2f2f646c2e64726f70626f7875736572636f6e74656e742e636f6d2f732f6f707062373572356c35726762376d2f73637265656e73686f742e706e67)) then you should install the [pygments](http://pygments.org/) highlighter. This would require [python](https://www.python.org/) and [pip](https://pypi.python.org/pypi/pip) as well.

Once you've got everything set up and the repo cloned you're ready to give it some content. You'll notice that there is some sample content provided in the `posts` folder. Consider leaving it as a reference until you understand how to format your post files correctly.

First, run `chmod + x generate` to add execution permissions to the `generate` file. Now you're ready to add your content to the `posts` folder. Your content must be in a "lazy html" format. Here's a list of the different tags.

* Wrap headers in `<h1></h1>` tags.
* Wrap paragraphs in `<p></p>` tags.
* If you would like your post to be labeled with a date at the top, you may supply one wrapped in a `<p class="date"></p>` tag.
* Sub headers should be wrapped in `<h2></h2>` tags.
* Quote blocks should be wrapped in `<p class="quote"></p>` tags.
* Highlighted code blocks (pygments-styling) should be wrapped in` <p class="code"></p>` tags.

There is no need to add other sorts of html to the file, the rest is taken care of automatically.

Note that the generated html files will be named the same as the corresponding files that you supply in the posts folder. This means that your supplied files should end with a `.html` extension.

Next you should fill out your defaults in the `defaults.yml` file. It requires things like your name and links to your social media.

Once you've supplied some posts and defaults, you're ready to run it. Since you should have already supplied it with execution permissions, you can run the application by calling generate like so: `./generate`

A few moments later, you should have your generated html content.

If you decide to later change some information whether it be a default setting or supplied post content, the application will automatically overwrite the old content. Running the generate file will cause the old generated files to be deleted.

NOTE: When `generate` is run, it writes over any files in the `blog/` directory not included with the application. If you need to add extra files to the directory, you can add the filename to the defaults in the `lib/cleanup.rb` file or you can disable the cleanup functionality by removing the lines containing `clean_up` in the `generate` file.

## Customization

If you'd like you may customize the css/less to your liking. Of particular note are the default colors in `variables.less`. These control the color scheme including the accent bar at the top of the page.

If there is interest I may add extra themes in the future, or easy theme customization.

## Get in touch

If you like the project and want to know a little more about where it came from, you can stop by my website at [morganmart.in](www.morganmart.in) where I post weekly about my current coding escapades.

Have a nice day!
