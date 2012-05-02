#Literate Code

A responsive front-end toolkit for laying out programming essays.
Look <a href="http://jamesabbottdd.com/literate-code.html">here for a demo</a>.

##How to get started with LC in the shortest time possible

How you end up integrating LC on your site will depend on your CMS or blog engine,
but here are some key points to keep in mind:

1. Sandbox the CSS in LC from the rest of your site. LC is self-contained in terms of design and if your global 
   stylesheets aren't isolated from the page(s) that use LC your LC styles will get affected via the CSS cascade
   mechanism.
2. Open content-template.html (included in this repo), view source, read the comments. It's got all you need.
   Then, just fill in your content.
3. The two main HTML classes that LC uses on are <code>text</code> and <code>code</code>. Use these to tag 
    <code>div</code>, <code>section</code>, or <code>p</code> elements to achieve the desired layout. Nest both
    of these elements at the same level.
4. Marking up code snippets: <code>code</code> tags for inline, <code>pre code</code> for multi-line examples.
5. As technical essays often draw on quotes from other sources, LC supports nicely formatted block quotations.
   Mark them up like this:

<code>
<blockquote>
	<p>
     	Literate Programming results in better digestion.
   </p>
   <footer>&mdash;Anonymous on <a href="http://internet.com">The Internet</a></footer>
</blockquote>
</code>

6. A Table of Contents is a <code>div</code> tagged with the class <code>toc"</code>. A good place for it is right after the main essay 		  				title.
7. LC uses <a href="http://code.google.com/p/google-code-prettify/">google-code-prettify</a>
   for syntax highlighting. For it to work, remember to load it in the <code>body</code> element:
	
  <code><body onload="prettyPrint()"></code>

  and, to tag the pre / code elements:

  <pre class="prettyprint">

That's all, really. Happy blogging. Oh, and don't forget to modify the title and meta tags to suit your site.

###TODO:

- In-document links don't work in WebKit browsers. Is this fixable?
- More headline tags ( < h2 )
- Support for responsive images (screenshots) as alternative to HTML code listings
- HTML5 video & audio support for screencasts & podcasts
- Line numbering on code listings
- Stronger semantic metadata (itemprop, property, author) for cutting-edge SEO
- More skins with other good color schemes

