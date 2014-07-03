With my own research I have been building what I think is a basic HTML5 structure that includes: language, complete site info, basic open graph info, complete set of icons, stylesheets, optional responsive stylesheets, HTML5 & CSS3 support added prior IE9. Below you will find a good explanation of everything. With the time I will keep adding or changing it. The whole purpose is _to make the web a standard and perfect site._


## What does `OP` means in some comments?
That is optional depending on each site project (mobile, responsive, etc.).


## Why you use Normalize.css instead of a Reset stylesheet?
You can find a good explanation from the creator on these sites:
* [What is the difference between Normalize.css and Reset CSS?](http://stackoverflow.com/questions/6887336/what-is-the-difference-between-normalize-css-and-reset-css#answers)
* [About normalize.css](http://nicolasgallagher.com/about-normalize-css/#normalize-vs-reset)

But if you feel better with a [reset stylesheet](http://www.cssreset.com/) then use it, just for anything you use remember: 

> The reset styles given here are intentionally very generic. There isn't any default color or background set for the body element, for example. I don't particularly recommend that you just use this in its unaltered state in your own projects. It should be tweaked, edited, extended, and otherwise tuned to match your specific reset baseline. Fill in your preferred colors for the page, links, and so on. In other words, this is a starting point, not a self-contained black box of no-touchiness. &mdash; **_[Eric Meyer](http://meyerweb.com/eric/tools/css/reset/)_**

And this also apply for Normalize.css, for example if the reset file is already setting the header size to 16px is a waste of compute time and space if you in another file set the header size to 20px. Also is unnecessary in the reset file to set the default for the `audio` and `video` elements if you don't use them in your project, so just change the reset file for **your defaults**.

## Where I can download the extra files?
* [html5shiv-printshiv.js](https://github.com/aFarkas/html5shiv) to support HTML5 elements on IE 6, 7 and 8.
* [normalize.min.css](http://necolas.github.io/normalize.css/) provides cross-browser consistency in the default CSS.
* [respond.js](https://github.com/scottjehl/Respond) polyfill for min/max-width CSS3 Media Queries on IE 6, 7 and 8.

With these files you can code safely what you may need in every project. To check the support of another CSS3 selectors or attributes check [this site](http://caniuse.com). Another great tool is [Modernizr](http://modernizr.com/) to check what the browser support and use fallbacks in case of failure.


## How do you compose the `lang` attribute for the `html` tag?
You can found the information at the [W3C Language Information site](http://www.w3.org/TR/html401/struct/dirlang.html).

The code is composed by the language tag and optionally followed by a dash "-" and the country tag.
The country tag is defined when the language belongs to a specific country (writing style), for example you can write `lang="en-US"` or `lang="en-GB"` to define American English or British English style respectively.
Not always is necessary to add the country, for example `lang="ja-JP"` is unnecessary since Japan is the only country where Japanese is the native language so it can just be `lang="ja"`.
The IANA list which contains the languages and countries tags can be found [here](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry).


## Why there are so many `html` tags?
Is to prepare the webpage for specific IE styles since not all the CSS styles works the same in every IE version, as explained in the [Paul Irish site](http://www.paulirish.com/2008/conditional-stylesheets-vs-css-hacks-answer-neither/).
But if your site is not targeted to older versions of IE you can safely remove some lines. For example, if nobody from your target audience is using IE7 you can remove the line `<!--[if lt IE 7]> <html class="lt-ie9 lt-ie8 lt-ie7"> <![endif]-->`.


## How the Open Graph metadata are filled?
In the [Open Graph Protocol Site](http://ogp.me) you can find the complete list of metadata available including its content type and syntax. This metadata information is useful when you share a page in a social network life Facebook or Google+. All the data needed is grabbed from this metadata as shown in the next image.

![Open Graph metadata example](http://farm6.staticflickr.com/5472/11743113915_e48c9758eb_o.png "Example")

In my opinion some information can be copied from the normal metadata to the open graph's metadata as follow:
* `<title>` to `meta property="og:title"`
* `meta name="description` to `meta property="og:description"`
* `<html> lang attribute` to `meta property="og:locale"`
* `browser URL` to `meta property="og:url"`

Another sites are using these metadata to read your site information, and you can find that [Google is using them in the search engine results](http://www.marketing-mojo.com/blog/open-graph-tagging-does-it-really-work/).


## Why there are so many icons?
Time ago as web designer you just needed one 16 x 16 favicon, but nowadays our site can be viewed from a lot of different browsers and devices such as: PC, Mac, iOS phones and tablets, Android phones and tablets, Windows 8 tablets, and more. Because of this you need to create each type of favicon and put them in your site. [RealFaviconGenerator](http://realfavicongenerator.net) generates all the pictures and HTML code you need to get all the favicons you need.


## It is necessary to include the `charset` in the CSS file?
Is optional, but is recommended. As explained in the [W3C Internationalization](http://www.w3.org/International/questions/qa-css-charset.en.php) you can declare the charset in the first line of each CSS file, but you must no longer declare it as a `link` tag attribute because is currently obsoleted by the HTML5 specification.


## A good example to structure my stylesheets?
Yeah, you can check this [website](http://thesassway.com/beginner/how-to-structure-a-sass-project), is a [SMACSS](http://smacss.com/) style (which I prefer).


## Any other good advice?
* Yes, please use a template system, whether the [Django template system](https://docs.djangoproject.com/en/dev/topics/templates/) or the [PHP's Twig template system](http://twig.sensiolabs.org/). **Do not repeat yourself**.
* Grid systems are useful to maintain order in your site, is can get messy behind so use them wisely. Here is a [good one](http://webdesign.tutsplus.com/tutorials/a-simple-responsive-grid-made-even-better-with-sass--cms-21540).

## License
Just use it. This is licenced under the [MIT license](http://opensource.org/licenses/MIT). Please read LICENSE for information on the software availability and distribution.