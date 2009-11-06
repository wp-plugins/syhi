=== Plugin Name ===
Contributors: sole
Donate link: http://soledadpenades.com/projects/wordpress/#donate
Tags: code, highlight, syntax, preformatting, whitespace, preserve
Requires at least: 2.8.5
Tested up to: 2.8.5
Stable tag: trunk

Minimalistic Syntax Highlighter plug-in which also makes sure code can still be copied and pasted into your favourite compiler!

== Description ==

This plug-in is totally designed for developers.

You know, that sort of people who post code snippets in their blog regularly and hardly use the Visual Editor,
because they write the HTML themselves. But they don't like WordPress messing with their quotes and dashes,
so this plug-in makes sure no one touches one of their lovingly crafted lines of code.

It's also very minimalistic - less than 10k, not counting the GeSHi syntax highlighting library which is also included.

In addition, it's also lazy. It will try to avoid doing as much work as possible.
That is good, because it will not eat resources like other plug-ins out there.

== Installation ==

- Upload the full `syhi` folder to the `/wp-content/plugins/` directory
- Activate the plugin through the 'Plugins' menu in WordPress
- That's it!

**Warning:** php5 and WP2.8.5+ are required. The plug-in has not been tested with any other configuration.

== Usage ==

Whenever you want to post some syntax highlighted code, surround it with `<code lang="language"></code>`. That's it.

Example:

	<code lang="php">
	class HelloWorld()
	{
		public function __construct()
		{
			echo "This is an unnecessarily long version of Hello World";
		}
	}
	</code>

The 'lang' attribute can be entirely omitted. You will get whitespace, quotes and dashes preservation... but no highlighting.

== Frequently Asked Questions ==

= Which languages are supported? =

This plug-in can beautify snippets in pretty much every programming language you can think of, thanks to the huge language support provided by GeSHi (the highlighting library). 

These are the available languages: abap, actionscript, actionscript3, ada, apache, applescript, apt sources, asm, asp, autoit, avisynth, bash, basic4gl, bf, bibtex, blitzbasic, bnf, boo, c, caddcl, cadlisp, cfdg, cfm, cil, c_mac, cmake, cobol, cpp, cpp-qt, csharp, css, d, dcs, delphi, diff, div, dos, dot, eiffel, email, erlang, fo, fortran, freebasic, genero, gettext, glsl, gml, gnuplot, groovy, haskell, hq9plus, html4strict, idl, ini, inno, intercal, io, java, java5, javascript, kixtart, klonec, klonecpp, latex, lisp, locobasic, lolcode, lotusformulas, lotusscript, lscript, lsl2, lua, m68k, make, matlab, mirc, modula3, mpasm, mxml, mysql, nsis, oberon2, objc, ocaml, ocaml-brief, oobas, oracle8, oracle11, pascal, per, perl, php, php-brief, pic16, pixelbender, plsql, povray, powershell, progress, prolog, properties, providex, python, qbasic, rails, rebol, reg, robots, ruby, sas, scala, scheme, scilab, sdlbasic, smalltalk, smarty, sql, tcl, teraterm, text, thinbasic, tsql, typoscript, vb, vbnet, verilog, vhdl, vim, visualfoxpro, visualprolog, whitespace, whois, winbatch, xml, xorg_conf, xpp, z80.

When entering the `lang` attribute in the code blocks, make sure the value you enter is exactly one of the languages in the list, or the highlighting will resort to a simple preformatted text.

If you still require syntax highlighting for a language which is not in this list, you'll have to develop your own language file. What about submitting it to GeSHi when you're done? :-)

= Is there any configuration panel or settings for the plug-in? =

Not right now, but it's on the to-do list. However, don't expect to be able to modify tons of settings. This is all about minimalism!

= Can I use the Visual Editor to enter code? =

My tests prove otherwise. You'll need to use the HTML view. At least by now.

= Features that other plug-ins have but are entirely unsupported/missing for the time being =

* Ability to use [code][/code] tags instead of `<code></code>` tags (would solve problems with the Visual Editor and the code tags)
* Ability to show line numbers
* Ability to have nested `<code>` blocks

= Planned features =

 Add options for...

 * configuring if you want to use my css sheet, your css sheet, both, or no one at all
 * configuring if you want to use GeSHi, or are happy with just plain preformatted text
 * configuring if you want to allow commenters to post syntax highlighted code snippets

== Screenshots ==

1. Sample of code highlighted with SyHi. See how the other text is unaffected by the quote-preserving feature, and hence is fully texturized (dashes, curly quotes, you name it!)
2. Sample of code with and without highlighting, using the default kubrick theme. Notice how the first snippet is totally ruined, because it doesn't use the code tag. The second one is beatifully colored and all problematic characters are preserved. Notice also that the snippet gets a scrollbar if the lines are too wide for the column width.

== Changelog ==

= 0.0.3 =

* Fix an issue where sometimes code blocks got replaced with placeholders, never to have the beautified code back into place
* Added every language file provided by GeSHi. No more adding language files manually to the plug-in.
* Rewording of readme.txt in places to improve legibility. Also added a list with all available language files so that people know what the plug-in can really do before installing it.
* Fixed some formatting issues in the readme.txt -- now it should display fine in the WordPress.org plugin page (hopefully!)

= 0.0.2 =

* Added the mandatory readme.txt that I forgot in the first release, plus a couple of screenshots.

= 0.0.1 =

* First public release


== Uninstall ==

Just deactivate the plug-in, and remove its folder from the wp-content/plugins directory.

== Thanks ==

Big thanks to the creators of the GeSHi library. Without it, the output of this plug-in would be very boring.
Here's its homepage: http://qbnz.com/highlighter/

The following plug-ins were invaluable sources of inspiration and how-to-do-it-right:

* Preserve Code Formatting, by  Scott Reilly (http://coffee2code.com)
* Code Snippet, by Roman Roan. Now maintained by Wyatt Neal (http://blog.hackerforhire.org/code-snippet/)

You could say this plug-in is the sum of the essence of both plug-ins.

