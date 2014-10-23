---
layout: page
title: "QueryPath: Find your way"
tagline: 
---
{% include JB/setup %}

<img src="/assets/querypath-200x333.png">
<p>QueryPath is an XML and HTML DOM manipulation tool. You can think of it as jQuery for PHP.</p>

> "an essential part of the Drupal and PHP communities"
> - [The Google Blog](http://googleblog.blogspot.com/2010/08/sixth-annual-summer-of-code-flexes-some.html)

## Install It!

Install it with [Composer](http://getcomposer.org) or grab a copy from the 
[GitHub Project Page](https://github.com/technosophos/querypath).

```json
{
  "require": {
    "querypath/QueryPath": ">=3.0.0"
  }
}
```

## Use It!

Using QueryPath is as easy as using jQuery. Give it a document and tell it
what to do.

QueryPath can handle multiple kinds of documents:

- XML, XHTML, and legacy HTML versions 2-4.
- HTML 5 with the [HTML5-PHP library](https://github.com/Masterminds/html5-php).

```php
// Parse some XML and print the contents of the third TD in the second row:
print qp($xml, '#row2>td:nth(3)')->text();

// Or kick it into legacy HTML mode and parse some old HTML
print htmlqp($old_html, '#row2>td:nth(3)')->text();

// Or use HTML5-PHP to handle the latest and greatest.
use Masterminds\HTML5;
$html5 = new HTML5();
$dom = $html5->loadHTML($html);
qp($dom, '#row2>td:nth(3)')->text();
```

## The Way-back Machine

If you're still using a version of PHP that does not support namespaces, you
will probably need to use the [2.1 version](https://github.com/technosophos/querypath/archive/2.1.2.zip).

