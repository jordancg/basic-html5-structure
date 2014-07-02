With my own research I have been building what I think is a basic HTML5 structure that includes: language, complete site info, basic open graph info, complete set of icons, stylesheets, optional responsive stylesheets, HTML5 & CSS3 support added prior IE9.

## What does `OP` means in some comments?
That is optional depending on each site project (mobile, responsive, etc.).

## Where I can download the extra files?
* [html5shiv-printshiv.js](https://github.com/aFarkas/html5shiv)
* [normalize.min.css](http://necolas.github.io/normalize.css/)
* [respond.js](https://github.com/scottjehl/Respond)

## How do you compose the `lang` attribute for the `html` tag?
You can found the information at the [W3C Language Information site](http://www.w3.org/TR/html401/struct/dirlang.html).

The code is composed by the language tag and optionally followed by a dash "-" and the country tag.
The country tag is defined when the language belongs to a specific country (writing style), for example you can write `lang="en-US"` or `lang="en-GB"` to define American English or British English style respectively.
Not always is neccesary to add the country, for example `lang="ja-JP"` is unnecessary since Japan is the only country where Japanese is the native language so it can just be `lang="ja"`.
The IANA list which contains the languages and countries tags can be found [here](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry).


## Why there are so many `html` tags?
Is to prepare the webpage for specific IE styles since not all the CSS styles works the same in IE, as explained in the [Paul Irish site](http://www.paulirish.com/2008/conditional-stylesheets-vs-css-hacks-answer-neither/).


## How the Open Graph metadatas are filled?
In the [Open Graph Protocol Site](http://ogp.me) you can find the complete list of metadatas available including it's content type and syntax. This metadata information is useful when you share a page in a social network life Facebook or Google+ all the data needed is grabbed from this metadatas as shown in the next image.

![Open Graph metadata example](http://farm6.staticflickr.com/5472/11743113915_e48c9758eb_o.png "Example")

In my opinion some info can be extracted and copied to the open graph's metadata as follow:
* `<title>` and `meta property="og:title"`
* `meta name="description"` and `meta property="og:description"`
* `<html> lang attribute"` and `meta property="og:locale"`
* `browser URL"` and `meta property="og:url"`

Another sites are using these metadatas, and some people says that Google is using them in the search engine results.


## Why there are so many icons?
Time ago as web designer you just needed one 16 x 16 favicon, but nowadays our site can be viewed from a lot of different browsers and devices such as: PC, Mac, iOS phones and tablets, Android phones and tablets, Windows 8 tablets, and more. Because of this you need to create each type of favicon and put them in your site. [RealFaviconGenerator](http://realfavicongenerator.net) generates all the pictures and HTML code you need to get all the favicons you need.


## It is necessary to include the `charset` in the CSS file?
Is optional, but is recommended. As explained in the [W3C Internationalization](http://www.w3.org/International/questions/qa-css-charset.en.php) you can declare the charset in the first line of each CSS file, but you must no longer declare it as a `link` tag attribute.