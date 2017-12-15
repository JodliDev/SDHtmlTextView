# SDHtmlTextView
Inspired by:
* HTMLTextView https://github.com/PrivacyApps/html-textview.
* HTMLSpanner https://github.com/NightWhistler/HtmlSpanner.

SDHtmlTextView use HTMLSpanner to display properly in TextViews an html page, overriding Html.fromHtml() and handling some CSS style inline properties.

### HTML Tags supported 

* ``<i>``
* ``<em>``
* ``<cite>``
* ``<dfn>``
* ``<b>``
* ``<strong>``
* ``<blockquote>``
* ``<ul>``
* ``<ol>``
* ``<tt>``
* ``<code>``
* ``<style>``
* ``<br>``
* ``<p>``
* ``<div>``
* ``<span>``
* ``<big>``
* ``<small>``
* ``<pre>``
* ``<sub>``
* ``<sup>``
* ``<center>``
* ``<li>``
* ``<font size="..." color="..." face="...">``
* ``<h1>``, ``<h2>``, ``<h3>``, ``<h4>``, ``<h5>``, ``<h6>``
* ``<a href="...">``
* ``<img src="...">``
* ``<table>``

### CSS Tags supported 

* ``color``
* ``background-color``
* ``align``
* ``text-align``
* ``font-weight``
* ``font-style``
* ``font-family``
* ``font-size``
* ``line-height`` only with measures in px 
* ``margin-bottom``
* ``margin-top``
* ``margin-left``
* ``margin-right``
* ``margin``
* ``text-indent``
* ``display``
* ``border-style``
* ``border-color``
* ``border-width``
* ``border``

## Usage
In the xml layout file define a simple TextView then in the Activity do

```java
        String html=loadStringFromAssetFile(this,"example.html");
        TextView tv = (TextView) findViewById(R.id.text);
        tv.setText((new HtmlSpanner()).fromHtml(html));
```
If you want to handle href you need to add
```java
        tv.setMovementMethod(LinkMovementMethod.getInstance());
```



## License
Copyright (C) 2017 Sysdata S.p.A.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.


