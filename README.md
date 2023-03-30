# TiddlyWiki_tutorial
The companion repo for my TiddlyWiki tutorial. The commit history shows the progress from blank TiddlyWiki template to the final version.


<!doctype html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html;charset=utf-8" />
<meta name="generator" content="TiddlyWiki" />
<meta name="tiddlywiki-version" content="5.2.3" />
<meta name="format-detection" content="telephone=no">
<link id="faviconLink" rel="shortcut icon" href="favicon.ico">
<title>Klarna — My notes on working at Klarna</title>
<div id="styleArea">
<style data-tiddler-title="$:/boot/boot.css" data-tiddler-type="text/css" type="text/css">/*
Basic styles used before we boot up the parsing engine
*/

/*
Error message and password prompt
*/

.tc-error-form {
	font-family: sans-serif;
	color: #fff;
	z-index: 20000;
	position: fixed;
	background-color: rgb(255, 75, 75);
	border: 8px solid rgb(255, 0, 0);
	border-radius: 8px;
	width: 50%;
	margin-left: 25%;
	margin-top: 4em;
	padding: 0 2em 1em 2em;
}

.tc-error-form h1 {
	text-align: center;
}

.tc-error-prompt {
	text-align: center;
	color: #000;
}

.tc-error-message {
	overflow: auto;
	max-height: 40em;
	padding-right: 1em;
	margin: 1em 0;
	white-space: pre-line;
}

.tc-password-wrapper {
    font-family: sans-serif;
	z-index: 20000;
	position: fixed;
	text-align: center;
	width: 200px;
	top: 4em;
	left: 50%;
	margin-left: -144px; /* - width/2 - paddingHorz/2 - border */
	padding: 16px 16px 16px 16px;
	border-radius: 8px;
}

.tc-password-wrapper {
	color: #000;
	text-shadow: 0 1px 0 rgba(255, 255, 255, 0.5);
	background-color: rgb(197, 235, 183);
	border: 8px solid rgb(164, 197, 152);
}

.tc-password-wrapper form {
	text-align: left;
}

.tc-password-wrapper h1 {
	font-size: 16px;
	line-height: 20px;
	padding-bottom: 16px;
}

.tc-password-wrapper input {
	width: 100%;
}
</style>
</div>
<style type="text/css">
.tc-sidebar-header {
	text-shadow: 0 1px 0 transparent;
}.tc-tiddler-info {
	
  -webkit-box-shadow: inset 1px 2px 3px rgba(0,0,0,0.1);
     -moz-box-shadow: inset 1px 2px 3px rgba(0,0,0,0.1);
          box-shadow: inset 1px 2px 3px rgba(0,0,0,0.1);

}@media screen {
	.tc-tiddler-frame {
		
  -webkit-box-shadow: 1px 1px 5px rgba(0, 0, 0, 0.3);
     -moz-box-shadow: 1px 1px 5px rgba(0, 0, 0, 0.3);
          box-shadow: 1px 1px 5px rgba(0, 0, 0, 0.3);

	}
}@media (max-width: 959px) {
	.tc-tiddler-frame {
		
  -webkit-box-shadow: none;
     -moz-box-shadow: none;
          box-shadow: none;

	}
}.tc-page-controls button svg, .tc-tiddler-controls button svg, .tc-topbar button svg {
	
  -webkit-transition: fill 150ms ease-in-out;
     -moz-transition: fill 150ms ease-in-out;
          transition: fill 150ms ease-in-out;

}.tc-tiddler-controls button.tc-selected,
.tc-page-controls button.tc-selected {
	
  -webkit-filter: drop-shadow(0px -1px 2px rgba(0,0,0,0.25));
     -moz-filter: drop-shadow(0px -1px 2px rgba(0,0,0,0.25));
          filter: drop-shadow(0px -1px 2px rgba(0,0,0,0.25));

}.tc-tiddler-frame input.tc-edit-texteditor,
.tc-tiddler-frame select.tc-edit-texteditor {
	
  -webkit-box-shadow: inset 0 1px 8px rgba(0, 0, 0, 0.15);
     -moz-box-shadow: inset 0 1px 8px rgba(0, 0, 0, 0.15);
          box-shadow: inset 0 1px 8px rgba(0, 0, 0, 0.15);

}.tc-edit-tags {
	
  -webkit-box-shadow: inset 0 1px 8px rgba(0, 0, 0, 0.15);
     -moz-box-shadow: inset 0 1px 8px rgba(0, 0, 0, 0.15);
          box-shadow: inset 0 1px 8px rgba(0, 0, 0, 0.15);

}.tc-tiddler-frame .tc-edit-tags input.tc-edit-texteditor {
	
  -webkit-box-shadow: none;
     -moz-box-shadow: none;
          box-shadow: none;

	border: none;
	outline: none;
}textarea.tc-edit-texteditor {
	font-family: ;
}canvas.tc-edit-bitmapeditor  {
	
  -webkit-box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
     -moz-box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
          box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);

}.tc-drop-down {
	border-radius: 4px;
	
  -webkit-box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);
     -moz-box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);
          box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);

}.tc-block-dropdown {
	border-radius: 4px;
	
  -webkit-box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);
     -moz-box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);
          box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);

}.tc-modal {
	border-radius: 6px;
	
  -webkit-box-shadow: 0 3px 7px rgba(0,0,0,0.3);
     -moz-box-shadow: 0 3px 7px rgba(0,0,0,0.3);
          box-shadow: 0 3px 7px rgba(0,0,0,0.3);

}.tc-modal-footer {
	border-radius: 0 0 6px 6px;
	
  -webkit-box-shadow: inset 0 1px 0 #fff;
     -moz-box-shadow: inset 0 1px 0 #fff;
          box-shadow: inset 0 1px 0 #fff;
;
}.tc-alert {
	border-radius: 6px;
	
  -webkit-box-shadow: 0 3px 7px rgba(0,0,0,0.6);
     -moz-box-shadow: 0 3px 7px rgba(0,0,0,0.6);
          box-shadow: 0 3px 7px rgba(0,0,0,0.6);

}.tc-notification {
	border-radius: 6px;
	
  -webkit-box-shadow: 0 3px 7px rgba(0,0,0,0.3);
     -moz-box-shadow: 0 3px 7px rgba(0,0,0,0.3);
          box-shadow: 0 3px 7px rgba(0,0,0,0.3);

	text-shadow: 0 1px 0 rgba(255,255,255, 0.8);
}.tc-sidebar-lists .tc-tab-set .tc-tab-divider {
	border-top: none;
	height: 1px;
	
background-image: linear-gradient(left, rgba(0,0,0,0.15) 0%, rgba(0,0,0,0.0) 100%);
background-image: -o-linear-gradient(left, rgba(0,0,0,0.15) 0%, rgba(0,0,0,0.0) 100%);
background-image: -moz-linear-gradient(left, rgba(0,0,0,0.15) 0%, rgba(0,0,0,0.0) 100%);
background-image: -webkit-linear-gradient(left, rgba(0,0,0,0.15) 0%, rgba(0,0,0,0.0) 100%);
background-image: -ms-linear-gradient(left, rgba(0,0,0,0.15) 0%, rgba(0,0,0,0.0) 100%);

}.tc-more-sidebar > .tc-tab-set > .tc-tab-buttons > button {
	
background-image: linear-gradient(left, rgba(0,0,0,0.01) 0%, rgba(0,0,0,0.1) 100%);
background-image: -o-linear-gradient(left, rgba(0,0,0,0.01) 0%, rgba(0,0,0,0.1) 100%);
background-image: -moz-linear-gradient(left, rgba(0,0,0,0.01) 0%, rgba(0,0,0,0.1) 100%);
background-image: -webkit-linear-gradient(left, rgba(0,0,0,0.01) 0%, rgba(0,0,0,0.1) 100%);
background-image: -ms-linear-gradient(left, rgba(0,0,0,0.01) 0%, rgba(0,0,0,0.1) 100%);

}.tc-more-sidebar > .tc-tab-set > .tc-tab-buttons > button.tc-tab-selected {
	
background-image: linear-gradient(left, rgba(0,0,0,0.05) 0%, rgba(255,255,255,0.05) 100%);
background-image: -o-linear-gradient(left, rgba(0,0,0,0.05) 0%, rgba(255,255,255,0.05) 100%);
background-image: -moz-linear-gradient(left, rgba(0,0,0,0.05) 0%, rgba(255,255,255,0.05) 100%);
background-image: -webkit-linear-gradient(left, rgba(0,0,0,0.05) 0%, rgba(255,255,255,0.05) 100%);
background-image: -ms-linear-gradient(left, rgba(0,0,0,0.05) 0%, rgba(255,255,255,0.05) 100%);

}.tc-message-box img {
	
  -webkit-box-shadow: 1px 1px 3px rgba(0,0,0,0.5);
     -moz-box-shadow: 1px 1px 3px rgba(0,0,0,0.5);
          box-shadow: 1px 1px 3px rgba(0,0,0,0.5);

}.tc-plugin-info {
	
  -webkit-box-shadow: 1px 1px 3px rgba(0,0,0,0.5);
     -moz-box-shadow: 1px 1px 3px rgba(0,0,0,0.5);
          box-shadow: 1px 1px 3px rgba(0,0,0,0.5);

}
/*
** Start with the normalize CSS reset, and then belay some of its effects
*//*! modern-normalize v1.0.0 | MIT License | https://github.com/sindresorhus/modern-normalize */

/*
Document
========
*/

/**
Use a better box model (opinionated).
*/

*,
*::before,
*::after {
  box-sizing: border-box;
}

/**
Use a more readable tab size (opinionated).
*/

:root {
  -moz-tab-size: 4;
  tab-size: 4;
}

/**
1. Correct the line height in all browsers.
2. Prevent adjustments of font size after orientation changes in iOS.
*/

html {
  line-height: 1.15; /* 1 */
  -webkit-text-size-adjust: 100%; /* 2 */
}

/*
Sections
========
*/

/**
Remove the margin in all browsers.
*/

body {
  margin: 0;
}

/**
Improve consistency of default fonts in all browsers. (https://github.com/sindresorhus/modern-normalize/issues/3)
*/

body {
  font-family:
    system-ui,
    -apple-system, /* Firefox supports this but not yet `system-ui` */
    'Segoe UI',
    Roboto,
    Helvetica,
    Arial,
    sans-serif,
    'Apple Color Emoji',
    'Segoe UI Emoji';
}

/*
Grouping content
================
*/

/**
1. Add the correct height in Firefox.
2. Correct the inheritance of border color in Firefox. (https://bugzilla.mozilla.org/show_bug.cgi?id=190655)
*/

hr {
  height: 0; /* 1 */
  color: inherit; /* 2 */
}

/*
Text-level semantics
====================
*/

/**
Add the correct text decoration in Chrome, Edge, and Safari.
*/

abbr[title] {
  text-decoration: underline dotted;
}

/**
Add the correct font weight in Edge and Safari.
*/

b,
strong {
  font-weight: bolder;
}

/**
1. Improve consistency of default fonts in all browsers. (https://github.com/sindresorhus/modern-normalize/issues/3)
2. Correct the odd 'em' font sizing in all browsers.
*/

code,
kbd,
samp,
pre {
  font-family:
    ui-monospace,
    SFMono-Regular,
    Consolas,
    'Liberation Mono',
    Menlo,
    monospace; /* 1 */
  font-size: 1em; /* 2 */
}

/**
Add the correct font size in all browsers.
*/

small {
  font-size: 80%;
}

/**
Prevent 'sub' and 'sup' elements from affecting the line height in all browsers.
*/

sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}

sub {
  bottom: -0.25em;
}

sup {
  top: -0.5em;
}

/*
Tabular data
============
*/

/**
1. Remove text indentation from table contents in Chrome and Safari. (https://bugs.chromium.org/p/chromium/issues/detail?id=999088, https://bugs.webkit.org/show_bug.cgi?id=201297)
2. Correct table border color inheritance in all Chrome and Safari. (https://bugs.chromium.org/p/chromium/issues/detail?id=935729, https://bugs.webkit.org/show_bug.cgi?id=195016)
*/

table {
  text-indent: 0; /* 1 */
  border-color: inherit; /* 2 */
}

/*
Forms
=====
*/

/**
1. Change the font styles in all browsers.
2. Remove the margin in Firefox and Safari.
*/

button,
input,
optgroup,
select,
textarea {
  font-family: inherit; /* 1 */
  font-size: 100%; /* 1 */
  line-height: 1.15; /* 1 */
  margin: 0; /* 2 */
}

/**
Remove the inheritance of text transform in Edge and Firefox.
1. Remove the inheritance of text transform in Firefox.
*/

button,
select { /* 1 */
  text-transform: none;
}

/**
Correct the inability to style clickable types in iOS and Safari.
*/

button,
[type='button'],
[type='reset'],
[type='submit'] {
  -webkit-appearance: button;
}

/**
Remove the inner border and padding in Firefox.
*/

::-moz-focus-inner {
  border-style: none;
  padding: 0;
}

/**
Restore the focus styles unset by the previous rule.
*/

:-moz-focusring {
  outline: 1px dotted ButtonText;
}

/**
Remove the additional ':invalid' styles in Firefox.
See: https://github.com/mozilla/gecko-dev/blob/2f9eacd9d3d995c937b4251a5557d95d494c9be1/layout/style/res/forms.css#L728-L737
*/

:-moz-ui-invalid {
  box-shadow: none;
}

/**
Remove the padding so developers are not caught out when they zero out 'fieldset' elements in all browsers.
*/

legend {
  padding: 0;
}

/**
Add the correct vertical alignment in Chrome and Firefox.
*/

progress {
  vertical-align: baseline;
}

/**
Correct the cursor style of increment and decrement buttons in Safari.
*/

::-webkit-inner-spin-button,
::-webkit-outer-spin-button {
  height: auto;
}

/**
1. Correct the odd appearance in Chrome and Safari.
2. Correct the outline style in Safari.
*/

[type='search'] {
  -webkit-appearance: textfield; /* 1 */
  outline-offset: -2px; /* 2 */
}

/**
Remove the inner padding in Chrome and Safari on macOS.
*/

::-webkit-search-decoration {
  -webkit-appearance: none;
}

/**
1. Correct the inability to style clickable types in iOS and Safari.
2. Change font properties to 'inherit' in Safari.
*/

::-webkit-file-upload-button {
  -webkit-appearance: button; /* 1 */
  font: inherit; /* 2 */
}

/*
Interactive
===========
*/

/*
Add the correct display in Chrome and Safari.
*/

summary {
  display: list-item;
}
*, input[type="search"] {
	box-sizing: border-box;
	-moz-box-sizing: border-box;
	-webkit-box-sizing: border-box;
}input[type="search"] {
	outline-offset: initial;
}html button {
	line-height: 1.2;
	color: inherit;
	fill: inherit;
	background: transparent;
	border-color: #ec6;
}button:disabled svg {
	fill: rgba(0, 0, 0, 0.54);
}/*
** Basic element styles
*/html, body {
	font-family: -apple-system,BlinkMacSystemFont,Segoe UI,Helvetica,Arial,sans-serif,Apple Color Emoji,Segoe UI Emoji;;
	text-rendering: optimizeLegibility; /* Enables kerning and ligatures etc. */
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
}html:-webkit-full-screen {
	background-color: #f4f4f4;
}body.tc-body {
	font-size: 14px;
	line-height: 20px;
	word-wrap: break-word;
	


	color: rgba(0, 0, 0, 0.87);
	background-color: #f4f4f4;
	fill: rgba(0, 0, 0, 0.87);
}/**
 * Correct the font size and margin on `h1` elements within `section` and
 * `article` contexts in Chrome, Firefox, and Safari.
 */h1 {
	font-size: 2em;
}h1, h2, h3, h4, h5, h6 {
	line-height: 1.2;
	font-weight: normal;
}pre {
	display: block;
	margin-top: 1em;
	margin-bottom: 1em;
	word-break: normal;
	word-wrap: break-word;
	white-space: pre-wrap;
	background-color: #ececec;
	border: 1px solid #ececec;
	padding: 0 3px 2px;
	border-radius: 3px;
	font-family: "SFMono-Regular",Consolas,"Liberation Mono",Menlo,Courier,monospace;
}code {
	color: ;
	background-color: #ececec;
	border: 1px solid #ececec;
	white-space: pre-wrap;
	padding: 0 3px 2px;
	border-radius: 3px;
	font-family: "SFMono-Regular",Consolas,"Liberation Mono",Menlo,Courier,monospace;
}blockquote {
	border-left: 5px solid #f4f4f4;
	margin-left: 25px;
	padding-left: 10px;
	quotes: "\201C""\201D""\2018""\2019";
}blockquote > div {
	margin-top: 1em;
	margin-bottom: 1em;
}blockquote.tc-big-quote {
	font-family: Georgia, serif;
	position: relative;
	background: #ececec;
	border-left: none;
	margin-left: 50px;
	margin-right: 50px;
	padding: 10px;
	border-radius: 8px;
}blockquote.tc-big-quote cite:before {
	content: "\2014 \2009";
}blockquote.tc-big-quote:before {
	font-family: Georgia, serif;
	color: #f4f4f4;
	content: open-quote;
	font-size: 8em;
	line-height: 0.1em;
	margin-right: 0.25em;
	vertical-align: -0.4em;
	position: absolute;
	left: -50px;
	top: 42px;
}blockquote.tc-big-quote:after {
	font-family: Georgia, serif;
	color: #f4f4f4;
	content: close-quote;
	font-size: 8em;
	line-height: 0.1em;
	margin-right: 0.25em;
	vertical-align: -0.4em;
	position: absolute;
	right: -80px;
	bottom: -20px;
}dl dt {
	font-weight: bold;
	margin-top: 6px;
}button, textarea, input, select {
	outline-color: #3949ab;
}textarea,
input[type=text],
input[type=search],
input[type=""],
input:not([type]) {
	color: rgba(0, 0, 0, 0.87);
	background: #FAFAFA;
}input[type="checkbox"] {
	vertical-align: middle;
}input[type="search"]::-webkit-search-decoration,
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-results-button,
input[type="search"]::-webkit-search-results-decoration {
	-webkit-appearance:none;
}.tc-muted {
	color: rgba(0, 0, 0, 0.54);
}svg.tc-image-button {
	padding: 0px 1px 1px 0px;
}.tc-icon-wrapper > svg {
	width: 1em;
	height: 1em;
}kbd {
	display: inline-block;
	padding: 3px 5px;
	font-size: 0.8em;
	line-height: 1.2;
	color: rgba(0, 0, 0, 0.87);
	vertical-align: middle;
	background-color: #FAFAFA;
	border: solid 1px rgba(0, 0, 0, 0.54);
	border-bottom-color: rgba(0, 0, 0, 0.54);
	border-radius: 3px;
	box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.54);
}::selection {
	background-color: Highlight;
	color: HighlightText;
	background-color: ;
	color: ;
}form.tc-form-inline {
	display: inline;
}/*
Markdown likes putting code elements inside pre elements
*/
pre > code {
	padding: 0;
	border: none;
	background-color: inherit;
	color: inherit;
}table {
	border: 1px solid #d8d8d8;
	width: auto;
	max-width: 100%;
	caption-side: bottom;
	margin-top: 1em;
	margin-bottom: 1em;
	/* next 2 elements needed, since normalize 8.0.1 */
	border-collapse: collapse;
	border-spacing: 0;
}table th, table td {
	padding: 0 7px 0 7px;
	border-top: 1px solid #d8d8d8;
	border-left: 1px solid #d8d8d8;
}table thead tr td, table th {
	background-color: rgba(0, 0, 0, 0.1);
	font-weight: bold;
}table tfoot tr td {
	background-color: rgba(0, 0, 0, 0.04);
}.tc-csv-table {
	white-space: nowrap;
}.tc-tiddler-frame img,
.tc-tiddler-frame svg,
.tc-tiddler-frame canvas,
.tc-tiddler-frame embed,
.tc-tiddler-frame iframe {
	max-width: 100%;
}.tc-tiddler-body > embed,
.tc-tiddler-body > iframe {
	width: 100%;
	height: 600px;
}:root {
	color-scheme: light;
}/*
** Links
*/button.tc-tiddlylink,
a.tc-tiddlylink {
	text-decoration: none;
	font-weight: 500;
	color: #3949ab;
	-webkit-user-select: inherit; /* Otherwise the draggable attribute makes links impossible to select */
}.tc-sidebar-lists a.tc-tiddlylink {
	color: rgba(0, 0, 0, 0.54);
}.tc-sidebar-lists a.tc-tiddlylink:hover {
	color: rgba(0, 0, 0, 0.87);
}button.tc-tiddlylink:hover,
a.tc-tiddlylink:hover {
	text-decoration: underline;
}a.tc-tiddlylink-resolves {
}a.tc-tiddlylink-shadow {
	font-weight: bold;
}a.tc-tiddlylink-shadow.tc-tiddlylink-resolves {
	font-weight: normal;
}a.tc-tiddlylink-missing {
	font-style: italic;
}a.tc-tiddlylink-external {
	text-decoration: underline;
	color: ;
	background-color: transparent;
}a.tc-tiddlylink-external:visited {
	color: ;
	background-color: transparent;
}a.tc-tiddlylink-external:hover {
	color: ;
	background-color: transparent;
}.tc-drop-down a.tc-tiddlylink:hover {
	color: #FAFAFA;
}/*
** Drag and drop styles
*/.tc-tiddler-dragger {
	position: relative;
	z-index: -10000;
}.tc-tiddler-dragger-inner {
	position: absolute;
	top: -1000px;
	left: -1000px;
	display: inline-block;
	padding: 8px 20px;
	font-size: 16.9px;
	font-weight: bold;
	line-height: 20px;
	color: #FAFAFA;
	text-shadow: 0 1px 0 rgba(0, 0, 0, 1);
	white-space: nowrap;
	vertical-align: baseline;
	background-color: rgba(0, 0, 0, 0.87);
	border-radius: 20px;
}.tc-tiddler-dragger-cover {
	position: absolute;
	background-color: #f4f4f4;
}.tc-page-container > .tc-dropzone {
	min-height: 100vh;
}.tc-dropzone {
	position: relative;
}.tc-dropzone.tc-dragover:before {
	z-index: 10000;
	display: block;
	position: fixed;
	top: 0;
	left: 0;
	right: 0;
	background: #ec6;
	text-align: center;
	content: "Drop now (or use the 'Escape' key to cancel)";
}.tc-droppable > .tc-droppable-placeholder {
	display: none;
}.tc-droppable.tc-dragover > .tc-droppable-placeholder {
	display: block;
	border: 2px dashed #ec6;
}.tc-draggable {
	cursor: move;
}.tc-sidebar-tab-open .tc-droppable-placeholder, .tc-tagged-draggable-list .tc-droppable-placeholder,
.tc-links-draggable-list .tc-droppable-placeholder {
	line-height: 2em;
	height: 2em;
}.tc-sidebar-tab-open-item {
	position: relative;
}.tc-sidebar-tab-open .tc-btn-invisible.tc-btn-mini svg {
	font-size: 0.7em;
	fill: rgba(0, 0, 0, 0.54);
}/*
** Plugin reload warning
*/.tc-plugin-reload-warning {
	z-index: 1000;
	display: block;
	position: fixed;
	top: 0;
	left: 0;
	right: 0;
	background: #FAFAFA;
	text-align: center;
}/*
** Buttons
*/button svg, button img, label svg, label img {
	vertical-align: middle;
}.tc-btn-invisible {
	padding: 0;
	margin: 0;
	background: none;
	border: none;
	cursor: pointer;
	color: rgba(0, 0, 0, 0.87);
	fill: rgba(0, 0, 0, 0.87);
}button:disabled.tc-btn-invisible  {
	cursor: default; 
	color: rgba(0, 0, 0, 0.54);
}.tc-btn-boxed {
	font-size: 0.6em;
	padding: 0.2em;
	margin: 1px;
	background: none;
	border: 1px solid #c6c6c6;
	border-radius: 0.25em;
}html body.tc-body .tc-btn-boxed svg {
	font-size: 1.6666em;
}.tc-btn-boxed:hover {
	background: rgba(0, 0, 0, 0.54);
	color: #FAFAFA;
}html body.tc-body .tc-btn-boxed:hover svg {
	fill: #FAFAFA;
}.tc-btn-rounded {
	font-size: 0.5em;
	line-height: 2;
	padding: 0em 0.3em 0.2em 0.4em;
	margin: 1px;
	border: 1px solid rgba(0, 0, 0, 0.54);
	background: rgba(0, 0, 0, 0.54);
	color: #FAFAFA;
	border-radius: 2em;
}html body.tc-body .tc-btn-rounded svg {
	font-size: 1.6666em;
	fill: #FAFAFA;
}.tc-btn-rounded:hover {
	border: 1px solid rgba(0, 0, 0, 0.54);
	background: #FAFAFA;
	color: rgba(0, 0, 0, 0.54);
}html body.tc-body .tc-btn-rounded:hover svg {
	fill: rgba(0, 0, 0, 0.54);
}.tc-btn-icon svg {
	height: 1em;
	width: 1em;
	fill: rgba(0, 0, 0, 0.54);
}.tc-btn-text {
	margin-left: 7px;
}/* used for documentation "fake" buttons */
.tc-btn-standard {
	line-height: 1.8;
	color: #667;
	background-color: #e0e0e0;
	border: 1px solid #888;
	padding: 2px 1px 2px 1px;
	margin: 1px 4px 1px 4px;
}.tc-btn-big-green {
	display: inline-block;
	padding: 8px;
	margin: 4px 8px 4px 8px;
	background: #3949ab;
	color: #FAFAFA;
	fill: #FAFAFA;
	border: none;
	border-radius: 2px;
	font-size: 1.2em;
	line-height: 1.4em;
	text-decoration: none;
}.tc-btn-big-green svg,
.tc-btn-big-green img {
	height: 2em;
	width: 2em;
	vertical-align: middle;
	fill: #FAFAFA;
}.tc-primary-btn {
	background: #3949ab;
}.tc-sidebar-lists input {
	color: rgba(0, 0, 0, 0.87);
}.tc-sidebar-lists button {
	color: rgba(0, 0, 0, 0.87);
	fill: rgba(0, 0, 0, 0.87);
}.tc-sidebar-lists button.tc-btn-mini {
	color: rgba(0, 0, 0, 0.38);
}.tc-sidebar-lists button.tc-btn-mini:hover {
	color: rgba(0, 0, 0, 0.54);
}.tc-sidebar-lists button small {
	color: rgba(0, 0, 0, 0.87);
}button svg.tc-image-button, button .tc-image-button img {
	height: 1em;
	width: 1em;
}.tc-unfold-banner {
	position: absolute;
	padding: 0;
	margin: 0;
	background: none;
	border: none;
	width: 100%;
	width: calc(100% + 2px);
	margin-left: -43px;
	text-align: center;
	border-top: 2px solid #F5F5F5;
	margin-top: 4px;
}.tc-unfold-banner:hover {
	background: #F5F5F5;
	border-top: 2px solid #F5F5F5;
}.tc-unfold-banner svg, .tc-fold-banner svg {
	height: 0.75em;
	fill: #c6c6c6;
}.tc-unfold-banner:hover svg, .tc-fold-banner:hover svg {
	fill: #aeaeae;
}.tc-fold-banner {
	position: absolute;
	padding: 0;
	margin: 0;
	background: none;
	border: none;
	width: 23px;
	text-align: center;
	margin-left: -35px;
	top: 6px;
	bottom: 6px;
}.tc-fold-banner:hover {
	background: #F5F5F5;
}@media (max-width: 959px) {.tc-unfold-banner {
		position: static;
		width: calc(100% + 59px);
	}.tc-fold-banner {
		width: 16px;
		margin-left: -16px;
		font-size: 0.75em;
	}}/*
** Tags and missing tiddlers
*/.tc-tag-list-item {
	position: relative;
	display: inline-block;
}.tc-tags-wrapper {
	margin: 4px 0 14px 0;
}.tc-tags-wrapper .tc-tag-list-item {
	margin-right: 7px;
}.tc-missing-tiddler-label {
	font-style: italic;
	font-weight: normal;
	display: inline-block;
	font-size: 11.844px;
	line-height: 14px;
	white-space: nowrap;
	vertical-align: baseline;
}.tc-block-tags-dropdown > .tc-btn-invisible:hover {
	background-color: #3949ab;
}button.tc-tag-label, span.tc-tag-label {
	display: inline-block;
	padding: 0.16em 0.7em;
	font-size: 0.9em;
	font-weight: normal;
	line-height: 1.2em;
	color: inherit;
	white-space: break-spaces;
	vertical-align: baseline;
	background-color: #ec6;
	border-radius: 1em;
}.tc-sidebar-scrollable .tc-tag-label {
	text-shadow: none;
}.tc-untagged-separator {
	width: 10em;
	left: 0;
	margin-left: 0;
	border: 0;
	height: 1px;
	background: #d8d8d8;
}button.tc-untagged-label {
	background-color: rgba(0, 0, 0, 0.12);
}.tc-tag-label svg, .tc-tag-label img {
	height: 1em;
	width: 1em;
	margin-right: 3px;
	margin-bottom: 1px;
	vertical-align: bottom;
}.tc-edit-tags button.tc-remove-tag-button svg {
	font-size: 0.7em;
	vertical-align: middle;
}.tc-tag-manager-table .tc-tag-label {
}.tc-tag-manager-tag {
	width: 100%;
}button.tc-btn-invisible.tc-remove-tag-button {
	outline: none;
}.tc-tag-button-selected,
.tc-list-item-selected a.tc-tiddlylink, a.tc-list-item-selected {
	background-color: #3949ab;
	color: #FAFAFA;
}/*
** Page layout
*/.tc-topbar {
	position: fixed;
	z-index: 1200;
}.tc-topbar-left {
	left: 29px;
	top: 5px;
}.tc-topbar-right {
	top: 5px;
	right: 29px;
}@media (max-width: 959px) {.tc-topbar-right {
		right: 10px;
	}}.tc-topbar button {
	padding: 8px;
}.tc-topbar svg {
	fill: rgba(0, 0, 0, 0.54);
}.tc-topbar button:hover svg {
	fill: rgba(0, 0, 0, 0.87);
}@media (max-width: 959px) {.tc-show-sidebar-btn svg.tc-image-chevron-left, .tc-hide-sidebar-btn svg.tc-image-chevron-right {
		transform: rotate(-90deg);
	}}.tc-sidebar-header {
	color: rgba(0, 0, 0, 0.54);
	fill: rgba(0, 0, 0, 0.54);
}.tc-sidebar-header .tc-title a.tc-tiddlylink-resolves {
	font-weight: normal;
}.tc-sidebar-header .tc-sidebar-lists p {
	margin-top: 3px;
	margin-bottom: 3px;
}.tc-sidebar-header .tc-missing-tiddler-label {
	color: rgba(0, 0, 0, 0.54);
}.tc-advanced-search input {
	width: 60%;
}.tc-search a svg {
	width: 1.2em;
	height: 1.2em;
	vertical-align: middle;
}.tc-page-controls {
	margin-top: 14px;
	font-size: 1.5em;
}.tc-page-controls .tc-drop-down {
	font-size: 1rem;
}.tc-page-controls button {
	margin-right: 0.5em;
}.tc-page-controls a.tc-tiddlylink:hover {
	text-decoration: none;
}.tc-page-controls img {
	width: 1em;
}.tc-page-controls svg {
	fill: #c6c6c6;
}.tc-page-controls button:hover svg, .tc-page-controls a:hover svg {
	fill: #aeaeae;
}.tc-sidebar-lists .tc-menu-list-item {
	white-space: nowrap;
}.tc-menu-list-count {
	font-weight: bold;
}.tc-menu-list-subitem {
	padding-left: 7px;
}.tc-story-river {
	position: relative;
}@media (max-width: 959px) {.tc-sidebar-header {
		padding: 14px;
		min-height: 32px;
		margin-top: 0px;
		transition:  min-height 200ms ease-in-out, padding-top 200ms ease-in-out, padding-bottom 200ms ease-in-out;
	}
	
	.tc-story-river {
		position: relative;
		padding: 0;
	}
}@media (min-width: 960px) {.tc-message-box {
		margin: 21px -21px 21px -21px;
	}.tc-sidebar-scrollable {
		position: fixed;
		top: 0px;
		left: 770px;
		bottom: 0;
		right: 0;
		overflow-y: auto;
		overflow-x: auto;
		-webkit-overflow-scrolling: touch;
		margin: 0 0 0 -42px;
		padding: 71px 0 28px 42px;
	}html[dir="rtl"] .tc-sidebar-scrollable {
		left: auto;
		right: 770px;
	}.tc-story-river {
		position: relative;
		left: 0px;
		top: 0px;
		width: 770px;
		padding: 42px 42px 42px 42px;
	}.tc-story-river.tc-static-story-river {
		margin-right: 0;
		padding-right: 42px;
	}}@media print {body.tc-body {
		background-color: transparent;
	}.tc-sidebar-header, .tc-topbar {
		display: none;
	}.tc-story-river {
		margin: 0;
		padding: 0;
	}.tc-story-river .tc-tiddler-frame {
		margin: 0;
		border: none;
		padding: 0;
	}
}/*
** Tiddler styles
*/.tc-tiddler-frame {
	position: relative;
	margin-bottom: 28px;
	background-color: #FAFAFA;
	border: 1px solid #f9f9f9;
}

.tc-tiddler-title {
	position: -webkit-sticky;
	position: -moz-sticky;
	position: -o-sticky;
	position: -ms-sticky;
	position: sticky;
	top: 0px;
	background: #FAFAFA;
	z-index: 500;
}



.tc-story-river .tc-tiddler-frame:nth-child(100n+1) {
z-index: 199;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+2) {
z-index: 198;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+3) {
z-index: 197;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+4) {
z-index: 196;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+5) {
z-index: 195;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+6) {
z-index: 194;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+7) {
z-index: 193;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+8) {
z-index: 192;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+9) {
z-index: 191;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+10) {
z-index: 190;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+11) {
z-index: 189;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+12) {
z-index: 188;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+13) {
z-index: 187;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+14) {
z-index: 186;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+15) {
z-index: 185;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+16) {
z-index: 184;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+17) {
z-index: 183;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+18) {
z-index: 182;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+19) {
z-index: 181;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+20) {
z-index: 180;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+21) {
z-index: 179;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+22) {
z-index: 178;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+23) {
z-index: 177;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+24) {
z-index: 176;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+25) {
z-index: 175;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+26) {
z-index: 174;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+27) {
z-index: 173;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+28) {
z-index: 172;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+29) {
z-index: 171;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+30) {
z-index: 170;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+31) {
z-index: 169;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+32) {
z-index: 168;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+33) {
z-index: 167;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+34) {
z-index: 166;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+35) {
z-index: 165;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+36) {
z-index: 164;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+37) {
z-index: 163;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+38) {
z-index: 162;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+39) {
z-index: 161;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+40) {
z-index: 160;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+41) {
z-index: 159;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+42) {
z-index: 158;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+43) {
z-index: 157;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+44) {
z-index: 156;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+45) {
z-index: 155;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+46) {
z-index: 154;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+47) {
z-index: 153;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+48) {
z-index: 152;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+49) {
z-index: 151;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+50) {
z-index: 150;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+51) {
z-index: 149;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+52) {
z-index: 148;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+53) {
z-index: 147;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+54) {
z-index: 146;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+55) {
z-index: 145;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+56) {
z-index: 144;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+57) {
z-index: 143;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+58) {
z-index: 142;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+59) {
z-index: 141;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+60) {
z-index: 140;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+61) {
z-index: 139;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+62) {
z-index: 138;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+63) {
z-index: 137;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+64) {
z-index: 136;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+65) {
z-index: 135;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+66) {
z-index: 134;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+67) {
z-index: 133;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+68) {
z-index: 132;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+69) {
z-index: 131;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+70) {
z-index: 130;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+71) {
z-index: 129;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+72) {
z-index: 128;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+73) {
z-index: 127;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+74) {
z-index: 126;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+75) {
z-index: 125;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+76) {
z-index: 124;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+77) {
z-index: 123;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+78) {
z-index: 122;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+79) {
z-index: 121;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+80) {
z-index: 120;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+81) {
z-index: 119;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+82) {
z-index: 118;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+83) {
z-index: 117;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+84) {
z-index: 116;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+85) {
z-index: 115;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+86) {
z-index: 114;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+87) {
z-index: 113;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+88) {
z-index: 112;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+89) {
z-index: 111;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+90) {
z-index: 110;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+91) {
z-index: 109;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+92) {
z-index: 108;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+93) {
z-index: 107;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+94) {
z-index: 106;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+95) {
z-index: 105;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+96) {
z-index: 104;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+97) {
z-index: 103;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+98) {
z-index: 102;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+99) {
z-index: 101;
}


.tc-story-river .tc-tiddler-frame:nth-child(100n+100) {
z-index: 100;
}



.tc-tiddler-info {
	overflow: hidden;
	padding: 14px 42px 14px 42px;
	background-color: #F5F5F5;
	border-top: 1px solid #F5F5F5;
	border-bottom: 1px solid #F5F5F5;
}.tc-tiddler-info p {
	margin-top: 3px;
	margin-bottom: 3px;
}.tc-tiddler-info .tc-tab-buttons button.tc-tab-selected {
	background-color: rgba(0, 0, 0, 0.04);
	border-bottom: 1px solid rgba(0, 0, 0, 0.04);
}@media (max-width: 959px) {.tc-tiddler-info {
		padding: 14px 14px 14px 14px;
	}}.tc-view-field-table {
	width: 100%;
}.tc-view-field-name {
	width: 1%; /* Makes this column be as narrow as possible */
	white-space: nowrap;
	vertical-align: top;
	text-align: right;
	font-style: italic;
	font-weight: normal;
}.tc-view-field-value {
	word-break: break-all;
}@media (max-width: 959px) {
	.tc-tiddler-frame {
		padding: 14px 14px 14px 14px;
		margin-bottom: .5em;
	}.tc-tiddler-info {
		margin: 0 -14px 0 -14px;
	}
}@media (min-width: 960px) {
	.tc-tiddler-frame {
		padding: 28px 42px 42px 42px;
		width: 686px;
		border-radius: 2px;
	}.tc-tiddler-info {
		margin: 0 -42px 0 -42px;
	}
}.tc-site-title,
.tc-titlebar {
	font-weight: normal;
	font-size: 2.35em;
	line-height: 1.35em;
	color: #000000;
	margin: 0;
}.tc-site-title {
	color: rgba(0, 0, 0, 0.87);
}.tc-tiddler-title-icon {
	vertical-align: middle;
	margin-right: .1em;
}.tc-system-title-prefix {
	color: rgba(0, 0, 0, 0.54);
}.tc-titlebar h2 {
	font-size: 1em;
	display: inline;
}.tc-titlebar img {
	height: 1em;
}.tc-subtitle {
	font-size: 0.9em;
	color: rgba(0, 0, 0, 0.54);
	font-weight: normal;
}.tc-subtitle .tc-tiddlylink {
	margin-right: .3em;
}.tc-tiddler-missing .tc-title {
	font-style: italic;
	font-weight: normal;
}.tc-tiddler-frame .tc-tiddler-controls {
	float: right;
}.tc-tiddler-controls .tc-drop-down {
	font-size: 0.6em;
}.tc-tiddler-controls .tc-drop-down .tc-drop-down {
	font-size: 1em;
}.tc-tiddler-controls > span > button,
.tc-tiddler-controls > span > span > button,
.tc-tiddler-controls > span > span > span > button {
	vertical-align: baseline;
	margin-left:5px;
}.tc-tiddler-controls button svg, .tc-tiddler-controls button img,
.tc-search button svg, .tc-search a svg {
	fill: #c6c6c6;
}.tc-tiddler-controls button svg, .tc-tiddler-controls button img {
	height: 0.75em;
}.tc-search button svg, .tc-search a svg {
	height: 1.2em;
	width: 1.2em;
	margin: 0 0.25em;
}.tc-tiddler-controls button.tc-selected svg,
.tc-page-controls button.tc-selected svg  {
	fill: #aeaeae;
}.tc-tiddler-controls button.tc-btn-invisible:hover svg,
.tc-search button:hover svg, .tc-search a:hover svg {
	fill: #aeaeae;
}@media print {
	.tc-tiddler-controls {
		display: none;
	}
}.tc-tiddler-help { /* Help prompts within tiddler template */
	color: rgba(0, 0, 0, 0.54);
	margin-top: 14px;
}.tc-tiddler-help a.tc-tiddlylink {
	color: rgba(0, 0, 0, 0.12);
}.tc-tiddler-frame .tc-edit-texteditor {
	width: 100%;
	margin: 4px 0 4px 0;
}.tc-tiddler-frame input.tc-edit-texteditor,
.tc-tiddler-frame textarea.tc-edit-texteditor,
.tc-tiddler-frame iframe.tc-edit-texteditor,
.tc-tiddler-frame select.tc-edit-texteditor {
	padding: 3px 3px 3px 3px;
	border: 1px solid #e8e7e7;
	line-height: 1.3em;
	font-family: ;
}.tc-tiddler-frame input.tc-edit-texteditor,
.tc-tiddler-frame textarea.tc-edit-texteditor,
.tc-tiddler-frame iframe.tc-edit-texteditor {
	-webkit-appearance: none;
}.tc-tiddler-frame input.tc-edit-texteditor,
.tc-tiddler-frame select.tc-edit-texteditor,
.tc-tiddler-frame textarea.tc-edit-texteditor {
	background-color: transparent;
}.tc-tiddler-frame iframe.tc-edit-texteditor {
	background-color: #FAFAFA;
}.tc-tiddler-frame .tc-edit-fields input.tc-edit-fieldeditor,
.tc-tiddler-frame .tc-edit-fields select.tc-edit-fieldeditor,
.tc-tiddler-frame .tc-edit-fields textarea.tc-edit-fieldeditor {
	margin: 0;
	padding: 2px 3px;
}.tc-tiddler-frame .tc-binary-warning {
	width: 100%;
	height: 5em;
	text-align: center;
	padding: 3em 3em 6em 3em;
	background: #FAFAFA;
	border: 1px solid rgba(0, 0, 0, 0.12);
}canvas.tc-edit-bitmapeditor  {
	border: 6px solid ;
	cursor: crosshair;
	-moz-user-select: none;
	-webkit-user-select: none;
	-ms-user-select: none;
	margin-top: 6px;
	margin-bottom: 6px;
}.tc-edit-bitmapeditor-width {
	display: block;
}.tc-edit-bitmapeditor-height {
	display: block;
}.tc-tiddler-body {
	clear: both;
}.tc-tiddler-frame .tc-tiddler-body {
	font-size: 15px;
	line-height: 22px;
}.tc-titlebar, .tc-tiddler-edit-title {
	overflow: hidden; /* https://github.com/Jermolene/TiddlyWiki5/issues/282 */
}html body.tc-body.tc-single-tiddler-window {
	margin: 1em;
	background: #FAFAFA;
}.tc-single-tiddler-window img,
.tc-single-tiddler-window svg,
.tc-single-tiddler-window canvas,
.tc-single-tiddler-window embed,
.tc-single-tiddler-window iframe {
	max-width: 100%;
}/*
** Editor
*/.tc-editor-toolbar {
	margin-top: 8px;
}.tc-editor-toolbar button {
	vertical-align: middle;
	background-color: #c6c6c6;
	color: #aeaeae;
	fill: #aeaeae;
	border-radius: 4px;
	padding: 3px;
	margin: 2px 0 2px 4px;
}.tc-editor-toolbar button.tc-text-editor-toolbar-item-adjunct {
	margin-left: 1px;
	width: 1em;
	border-radius: 8px;
}.tc-editor-toolbar button.tc-text-editor-toolbar-item-start-group {
	margin-left: 11px;
}.tc-editor-toolbar button.tc-selected {
	background-color: #3949ab;
}.tc-editor-toolbar button svg {
	width: 1.6em;
	height: 1.2em;
}.tc-editor-toolbar button:hover {
	background-color: #aeaeae;
	fill: #FAFAFA;
	color: #FAFAFA;
}.tc-editor-toolbar .tc-text-editor-toolbar-more {
	white-space: normal;
}.tc-editor-toolbar .tc-text-editor-toolbar-more button {
	display: inline-block;
	padding: 3px;
	width: auto;
}.tc-editor-toolbar .tc-search-results {
	padding: 0;
}.tc-editor-toolbar button.tc-editortoolbar-stamp-button + .tc-popup .tc-drop-down > p {
	margin: 0;
	padding: 0;
}.tc-editor-toolbar button.tc-editortoolbar-stamp-button + .tc-popup .tc-drop-down a.tc-tiddlylink {
	font-weight: normal;
}/*
** Adjustments for fluid-fixed mode
*/@media (min-width: 960px) {.tc-story-river {
		padding-right: 0;
		position: relative;
		width: auto;
		left: 0;
		margin-left: 0px;
		margin-right: 350px;
	}.tc-tiddler-frame {
		width: 100%;
	}.tc-sidebar-scrollable {
		left: auto;
		bottom: 0;
		right: 0;
		width: 350px;
	}body.tc-body .tc-storyview-zoomin-tiddler {
		width: 100%;
		width: calc(100% - 42px);
	}}/*
** Toolbar buttons
*/.tc-page-controls svg.tc-image-new-button {
	fill: ;
}.tc-page-controls svg.tc-image-options-button {
	fill: ;
}.tc-page-controls svg.tc-image-save-button {
	fill: ;
}.tc-tiddler-controls button svg.tc-image-info-button {
	fill: ;
}.tc-tiddler-controls button svg.tc-image-edit-button {
	fill: ;
}.tc-tiddler-controls button svg.tc-image-close-button {
	fill: ;
}.tc-tiddler-controls button svg.tc-image-delete-button {
	fill: ;
}.tc-tiddler-controls button svg.tc-image-cancel-button {
	fill: ;
}.tc-tiddler-controls button svg.tc-image-done-button {
	fill: ;
}/*
** Tiddler edit mode
*/.tc-tiddler-edit-frame em.tc-edit {
	color: rgba(0, 0, 0, 0.54);
	font-style: normal;
}.tc-edit-type-dropdown a.tc-tiddlylink-missing {
	font-style: normal;
}.tc-type-selector .tc-edit-typeeditor {
	width: auto;
}.tc-type-selector-dropdown-wrapper {
	display: inline-block;
}.tc-type-selector-dropdown-wrapper {
		min-width: calc(32ch + 4em);
	}.tc-type-selector-dropdown-wrapper input.tc-edit-typeeditor {
		min-width: 32ch;
	}.tc-edit-tags {
	border: 1px solid #e8e7e7;
	padding: 4px 8px 4px 8px;
}.tc-edit-add-tag {
	display: inline-block;
}.tc-edit-add-tag .tc-add-tag-name input {
	width: 50%;
}.tc-edit-add-tag .tc-keyboard {
	display:inline;
}.tc-edit-tags .tc-tag-label {
	display: inline-block;
}.tc-edit-tags-list {
	margin: 14px 0 14px 0;
}.tc-remove-tag-button {
	padding-left: 4px;
}.tc-tiddler-preview {
	overflow: auto;
}.tc-tiddler-preview-preview {
	float: right;
	width: 49%;
	border: 1px solid #e8e7e7;
	margin: 4px 0 3px 3px;
	padding: 3px 3px 3px 3px;
}.tc-tiddler-preview-preview {
	overflow-y: scroll;
	height: 600px;
}.tc-tiddler-frame .tc-tiddler-preview .tc-edit-texteditor {
	width: 49%;
}.tc-tiddler-frame .tc-tiddler-preview canvas.tc-edit-bitmapeditor {
	max-width: 49%;
}.tc-edit-fields {
	width: 100%;
}.tc-edit-fields.tc-edit-fields-small {
	margin-top: 0;
	margin-bottom: 0;
}.tc-edit-fields table, .tc-edit-fields tr, .tc-edit-fields td {
	border: none;
	padding: 4px;
}.tc-edit-fields > tbody > .tc-edit-field:nth-child(odd) {
	background-color: rgba(0, 0, 0, 0.04);
}.tc-edit-fields > tbody > .tc-edit-field:nth-child(even) {
	background-color: rgba(0, 0, 0, 0.1);
}.tc-edit-field-name {
	text-align: right;
}.tc-edit-field-value input {
	width: 100%;
}.tc-edit-field-remove {
}.tc-edit-field-remove svg {
	height: 1em;
	width: 1em;
	fill: rgba(0, 0, 0, 0.54);
	vertical-align: middle;
}.tc-edit-field-add-name-wrapper input.tc-edit-texteditor {
	width: auto;
}.tc-edit-field-add-name-wrapper {
	display: inline-block;
}.tc-edit-field-add-value {
	display: inline-block;
}@media (min-width: 960px) {.tc-edit-field-add-value {
		width: 35%;
	}}.tc-edit-field-add-button {
	display: inline-block;
	width: 10%;
}/*
** Tiddler editor dropzone
*/.tc-dropzone-editor {
	position:relative;
}.tc-dropzone-editor.tc-dragover .tc-editor-toolbar::after{
	z-index: 10000;
	top:0;
	left:0;
	right:0;
	height: 100%;
	background: #ec6;
	content: "Drop now (or use the 'Escape' key to cancel)";
	pointer-events: none;
	position: absolute;
	display: flex;
	align-items: center;
	justify-content: center;
	background-color: #FAFAFA;
	border: 4px dashed rgba(0, 0, 0, 0.12);
	font-weight: bold;
	font-size: 150%;
	opacity: 0.8;
	color: rgba(0, 0, 0, 0.87);
}.tc-editor-importpopup {
	width: 100%;
	height: 100%;
}.tc-editor-import {
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	background: #ececec;
	box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.87);
	padding: 10px;
	width: 96%;
	border: 1px solid #c6c6c6;
	text-align:center;
}.tc-editor-import img {
	max-height: 500px;
}/*
** Storyview Classes
*/.tc-viewswitcher .tc-image-button {
	margin-right: .3em;
}.tc-storyview-zoomin-tiddler {
	position: absolute;
	display: block;
	width: 100%;
}@media (min-width: 960px) {.tc-storyview-zoomin-tiddler {
		width: calc(100% - 84px);
	}}/*
** Dropdowns
*/.tc-btn-dropdown {
	text-align: left;
}.tc-btn-dropdown svg, .tc-btn-dropdown img {
	height: 1em;
	width: 1em;
	fill: rgba(0, 0, 0, 0.54);
}.tc-drop-down-wrapper {
	position: relative;
}.tc-drop-down {
	min-width: 380px;
	border: 1px solid #FFFFFF;
	background-color: #FFFFFF;
	padding: 7px 0 7px 0;
	margin: 4px 0 0 0;
	white-space: nowrap;
	text-shadow: none;
	line-height: 1.4;
}.tc-drop-down .tc-drop-down {
	margin-left: 14px;
}.tc-drop-down button svg, .tc-drop-down a svg  {
	fill: rgba(0, 0, 0, 0.87);
}.tc-drop-down button:disabled svg {
	fill: rgba(0, 0, 0, 0.54);
}.tc-drop-down button.tc-btn-invisible:hover svg {
	fill: #FAFAFA;
}.tc-drop-down .tc-drop-down-info {
	padding-left: 14px;
}.tc-drop-down p {
	padding: 0 14px 0 14px;
}.tc-drop-down svg {
	width: 1em;
	height: 1em;
}.tc-drop-down img {
	width: 1em;
}.tc-drop-down a, .tc-drop-down button {
	display: block;
	padding: 0 14px 0 14px;
	width: 100%;
	text-align: left;
	color: rgba(0, 0, 0, 0.87);
	line-height: 1.4;
}.tc-drop-down .tc-tab-set .tc-tab-buttons button {
	display: inline-block;
	width: auto;
	margin-bottom: 0px;
	border-bottom-left-radius: 0;
	border-bottom-right-radius: 0;
}.tc-drop-down .tc-prompt {
	padding: 0 14px;
}.tc-drop-down .tc-chooser {
	border: none;
}.tc-drop-down .tc-chooser .tc-swatches-horiz {
	font-size: 0.4em;
	padding-left: 1.2em;
}.tc-drop-down .tc-file-input-wrapper {
	width: 100%;
}.tc-drop-down .tc-file-input-wrapper button {
	color: rgba(0, 0, 0, 0.87);
}.tc-drop-down a:hover, .tc-drop-down button:hover, .tc-drop-down .tc-file-input-wrapper:hover button {
	color: #FAFAFA;
	background-color: #3949ab;
	text-decoration: none;
}.tc-drop-down .tc-tab-buttons button {
	background-color: #F5F5F5;
}.tc-drop-down .tc-tab-buttons button.tc-tab-selected {
	background-color: #FFFFFF;
	border-bottom: 1px solid #FFFFFF;
}.tc-drop-down-bullet {
	display: inline-block;
	width: 0.5em;
}.tc-drop-down .tc-tab-contents a {
	padding: 0 0.5em 0 0.5em;
}.tc-block-dropdown-wrapper {
	position: relative;
}.tc-block-dropdown {
	position: absolute;
	min-width: 220px;
	border: 1px solid #FFFFFF;
	background-color: #FFFFFF;
	padding: 7px 0;
	margin: 4px 0 0 0;
	white-space: nowrap;
	z-index: 1000;
	text-shadow: none;
}.tc-block-dropdown.tc-search-drop-down {
	margin-left: -12px;
}.tc-block-dropdown a {
	display: block;
	padding: 4px 14px 4px 14px;
}.tc-block-dropdown.tc-search-drop-down a {
	display: block;
	padding: 0px 10px 0px 10px;
}.tc-drop-down .tc-dropdown-item-plain,
.tc-block-dropdown .tc-dropdown-item-plain {
	padding: 4px 14px 4px 7px;
}.tc-drop-down .tc-dropdown-item,
.tc-block-dropdown .tc-dropdown-item {
	padding: 4px 14px 4px 7px;
	color: rgba(0, 0, 0, 0.54);
}.tc-block-dropdown a.tc-tiddlylink:hover {
	color: #FAFAFA;
	background-color: #3949ab;
	text-decoration: none;
}.tc-search-results {
	padding: 0 7px 0 7px;
}.tc-image-chooser, .tc-colour-chooser {
	white-space: normal;
}.tc-image-chooser a,
.tc-colour-chooser a {
	display: inline-block;
	vertical-align: top;
	text-align: center;
	position: relative;
}.tc-image-chooser a {
	border: 1px solid rgba(0, 0, 0, 0.54);
	padding: 2px;
	margin: 2px;
	width: 4em;
	height: 4em;
}.tc-colour-chooser a {
	padding: 3px;
	width: 2em;
	height: 2em;
	vertical-align: middle;
}.tc-image-chooser a:hover,
.tc-colour-chooser a:hover {
	background: #3949ab;
	padding: 0px;
	border: 3px solid #3949ab;
}.tc-image-chooser a svg,
.tc-image-chooser a img {
	display: inline-block;
	width: auto;
	height: auto;
	max-width: 3.5em;
	max-height: 3.5em;
	position: absolute;
	top: 0;
	bottom: 0;
	left: 0;
	right: 0;
	margin: auto;
}/*
** Modals
*/.tc-modal-wrapper {
	position: fixed;
	overflow: auto;
	overflow-y: scroll;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	z-index: 900;
}.tc-modal-backdrop {
	position: fixed;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	z-index: 1000;
	background-color: rgba(0, 0, 0, 0.87);
}.tc-modal {
	z-index: 1100;
	background-color: #FAFAFA;
	border: 1px solid rgba(0, 0, 0, 0.12);
}@media (max-width: 55em) {
	.tc-modal {
		position: fixed;
		top: 1em;
		left: 1em;
		right: 1em;
	}.tc-modal-body {
		overflow-y: auto;
		max-height: 400px;
		max-height: 60vh;
	}
}@media (min-width: 55em) {
	.tc-modal {
		position: fixed;
		top: 2em;
		left: 25%;
		width: 50%;
	}.tc-modal-body {
		overflow-y: auto;
		max-height: 400px;
		max-height: 60vh;
	}
}.tc-modal-header {
	padding: 9px 15px;
	border-bottom: 1px solid rgba(0, 0, 0, 0.12);
}.tc-modal-header h3 {
	margin: 0;
	line-height: 30px;
}.tc-modal-header img, .tc-modal-header svg {
	width: 1em;
	height: 1em;
}.tc-modal-body {
	padding: 15px;
}.tc-modal-footer {
	padding: 14px 15px 15px;
	margin-bottom: 0;
	text-align: right;
	background-color: #FAFAFA;
	border-top: 1px solid rgba(0, 0, 0, 0.12);
}.tc-modal-prevent-scroll {
	overflow: hidden;
}/*
** Centered modals
*/
.tc-modal-centered .tc-modal {
	width: auto;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%) !important;
}/*
** Notifications
*/.tc-notification {
	position: fixed;
	top: 14px;
	right: 42px;
	z-index: 1300;
	max-width: 280px;
	padding: 0 14px 0 14px;
	background-color: #FFFFFF;
	border: 1px solid #FFFFFF;
}/*
** Tabs
*/.tc-tab-set.tc-vertical {
	display: -webkit-flex;
	display: flex;
}.tc-tab-buttons {
	font-size: 0.85em;
	padding-top: 1em;
	margin-bottom: -2px;
}.tc-tab-buttons.tc-vertical  {
	z-index: 100;
	display: block;
	padding-top: 14px;
	vertical-align: top;
	text-align: right;
	margin-bottom: inherit;
	margin-right: -1px;
	max-width: 33%;
	-webkit-flex: 0 0 auto;
	flex: 0 0 auto;
}.tc-tab-buttons button.tc-tab-selected {
	color: rgba(0, 0, 0, 0.87);
	background-color: #FAFAFA;
	border-left: 1px solid #d8d8d8;
	border-top: 1px solid #d8d8d8;
	border-right: 1px solid #d8d8d8;
}.tc-tab-buttons button {
	color: rgba(0, 0, 0, 0.54);
	padding: 3px 5px 3px 5px;
	margin-right: 0.3em;
	font-weight: normal;
	border: none;
	background: inherit;
	background-color: transparent;
	border-left: 1px solid transparent;
	border-top: 1px solid transparent;
	border-right: 1px solid transparent;
	border-top-left-radius: 2px;
	border-top-right-radius: 2px;
	border-bottom-left-radius: 0;
	border-bottom-right-radius: 0;
}.tc-tab-buttons.tc-vertical button {
	display: block;
	width: 100%;
	margin-top: 3px;
	margin-right: 0;
	text-align: right;
	background-color: transparent;
	border-left: 1px solid transparent;
	border-bottom: 1px solid transparent;
	border-right: none;
	border-top-left-radius: 2px;
	border-bottom-left-radius: 2px;
	border-top-right-radius: 0;
	border-bottom-right-radius: 0;
}.tc-tab-buttons.tc-vertical button.tc-tab-selected {
	background-color: #FAFAFA;
	border-right: 1px solid #FAFAFA;
}.tc-tab-divider {
	border-top: 1px solid #d8d8d8;
}.tc-tab-divider.tc-vertical  {
	display: none;
}.tc-tab-content {
	margin-top: 14px;
}.tc-tab-content.tc-vertical  {
	display: inline-block;
	vertical-align: top;
	padding-top: 0;
	padding-left: 14px;
	border-left: 1px solid transparent;
	-webkit-flex: 1 0 70%;
	flex: 1 0 70%;
	overflow: auto;
}.tc-sidebar-lists .tc-tab-buttons {
	margin-bottom: -1px;
}.tc-sidebar-lists .tc-tab-buttons button.tc-tab-selected {
	background-color: #f4f4f4;
	color: rgba(0, 0, 0, 0.87);
	border-left: 1px solid #d8d8d8;
	border-top: 1px solid #d8d8d8;
	border-right: 1px solid #d8d8d8;
}.tc-sidebar-lists .tc-tab-buttons button {
	background-color: transparent;
	color: rgba(0, 0, 0, 0.54);
	border-left: 1px solid transparent;
	border-top: 1px solid transparent;
	border-right: 1px solid transparent;
}.tc-sidebar-lists .tc-tab-divider {
	border-top: 1px solid #d8d8d8;
}.tc-more-sidebar > .tc-tab-set > .tc-tab-buttons > button {
	display: block;
	width: 100%;
	background-color: transparent;
	border-top: none;
	border-left: none;
	border-bottom: none;
	border-right: 1px solid #ccc;
	margin-bottom: inherit;
}.tc-more-sidebar > .tc-tab-set > .tc-tab-buttons > button.tc-tab-selected {
	background-color: #f4f4f4;
	border: none;
}/*
** Manager
*/.tc-manager-wrapper {
	
}.tc-manager-controls {
	
}.tc-manager-control {
	margin: 0.5em 0;
}.tc-manager-control select {
	max-width: 100%;
}.tc-manager-list {
	width: 100%;
	border-top: 1px solid rgba(0, 0, 0, 0.54);
	border-left: 1px solid rgba(0, 0, 0, 0.54);
	border-right: 1px solid rgba(0, 0, 0, 0.54);
}.tc-manager-list-item {}.tc-manager-list-item-heading {
	display: block;
	width: 100%;
	text-align: left;
	border-bottom: 1px solid rgba(0, 0, 0, 0.54);
	padding: 3px;
}.tc-manager-list-item-heading-selected {
	font-weight: bold;
	color: #FAFAFA;
	fill: #FAFAFA;
	background-color: rgba(0, 0, 0, 0.87);
}.tc-manager-list-item-heading:hover {
	background: #3949ab;
	color: #FAFAFA;
}.tc-manager-list-item-content {
	display: flex;
}.tc-manager-list-item-content-sidebar {
	flex: 1 0;
	background: transparent;
	border-right: 0.5em solid rgba(0, 0, 0, 0.54);
	border-bottom: 0.5em solid rgba(0, 0, 0, 0.54);
	white-space: nowrap;
}.tc-manager-list-item-content-item-heading {
	display: block;
	width: 100%;
	text-align: left;
	background: rgba(0, 0, 0, 0.54);
	text-transform: uppercase;
	font-size: 0.6em;
	font-weight: bold;
	padding: 0.5em 0 0.5em 0;
}.tc-manager-list-item-content-item-body {
	padding: 0 0.5em 0 0.5em;
}.tc-manager-list-item-content-item-body > pre {
	margin: 0.5em 0 0.5em 0;
	border: none;
	background: inherit;
}.tc-manager-list-item-content-tiddler {
	flex: 3 1;
	border-left: 0.5em solid rgba(0, 0, 0, 0.54);
	border-right: 0.5em solid rgba(0, 0, 0, 0.54);
	border-bottom: 0.5em solid rgba(0, 0, 0, 0.54);
}.tc-manager-list-item-content-item-body > table {
	border: none;
	padding: 0;
	margin: 0;
}.tc-manager-list-item-content-item-body > table td {
	border: none;
}.tc-manager-icon-editor > button {
	width: 100%;
}.tc-manager-icon-editor > button > svg,
.tc-manager-icon-editor > button > button {
	width: 100%;
	height: auto;
}/*
** Import table
*/.tc-import-table {
	width: 100%;
}.tc-import-table svg.tc-image-edit-button {
	max-width: unset;
}.tc-import-table th:first-of-type {
	width: 10%;
}.tc-import-table th:last-of-type {
	width: 30%;
}.tc-import-table .tc-row-disabled {
	background: rgba(0, 0, 0, 0.12)10;
	opacity: 0.8;
}.tc-import-table .tc-row-warning {
	background: #ffc9c950;
}/*
** Alerts
*/.tc-alerts {
	position: fixed;
	top: 28px;
	left: 0;
	right: 0;
	max-width: 50%;
	z-index: 20000;
}.tc-alert {
	position: relative;
	margin: 14px;
	padding: 7px;
	border: 1px solid rgba(0, 0, 0, 0.12);
	background-color: #FAFAFA;
}.tc-alert-toolbar {
	position: absolute;
	top: 7px;
	right: 7px;
	line-height: 0;
}.tc-alert-toolbar svg {
	fill: rgba(0, 0, 0, 0.54);
}.tc-alert-subtitle {
	color: rgba(0, 0, 0, 0.54);
	font-weight: bold;
	font-size: 0.8em;
	margin-bottom: 0.5em;
}.tc-alert-body > p {
	margin: 0;
}.tc-alert-highlight {
	color: rgba(0, 0, 0, 0.12);
}@media (min-width: 960px) {.tc-static-alert {
		position: relative;
	}.tc-static-alert-inner {
		position: absolute;
		z-index: 100;
	}}.tc-static-alert-inner {
	padding: 0 2px 2px 42px;
	color: #aaaaaa;
}/*
** Floating drafts list
*/.tc-drafts-list {
	z-index: 2000;
	position: fixed;
	font-size: 0.8em;
	left: 0;
	bottom: 0;
}.tc-drafts-list a {
	margin: 0 0.5em;
	padding: 4px 4px;
	border-top-left-radius: 4px;
	border-top-right-radius: 4px;
	border: 1px solid #FAFAFA;
	border-bottom: none;
	background: #c80000;
	color: #FAFAFA;
	fill: #FAFAFA;
}.tc-drafts-list a:hover {
	text-decoration: none;
	background: rgba(0, 0, 0, 0.87);
	color: #FAFAFA;
	fill: #FAFAFA;
}.tc-drafts-list a svg {
	width: 1em;
	height: 1em;
	vertical-align: text-bottom;
}/*
** Control panel
*/.tc-control-panel td {
	padding: 4px;
}.tc-control-panel table, .tc-control-panel table input, .tc-control-panel table textarea {
	width: 100%;
}.tc-plugin-info {
	display: flex;
	text-shadow: none;
	border: 1px solid rgba(0, 0, 0, 0.54);
	fill: rgba(0, 0, 0, 0.54);
	background-color: #FAFAFA;
	margin: 0.5em 0 0.5em 0;
	padding: 4px;
	align-items: center;
}.tc-sidebar-lists a.tc-tiddlylink.tc-plugin-info {
	color: #3949ab;
}.tc-plugin-info-sub-plugins .tc-plugin-info {
	margin: 0.5em;
	background: #FAFAFA;
}.tc-plugin-info-sub-plugin-indicator {
	margin: -16px 1em 0 2em;
}.tc-plugin-info-sub-plugin-indicator button {
	color: #FAFAFA;
	background: rgba(0, 0, 0, 0.87);
	border-radius: 8px;
	padding: 2px 7px;
	font-size: 0.75em;
}.tc-plugin-info-sub-plugins .tc-plugin-info-dropdown {
	margin-left: 1em;
	margin-right: 1em;
}.tc-plugin-info-disabled {
	background: -webkit-repeating-linear-gradient(45deg, #ff0, #ff0 10px, #eee 10px, #eee 20px);
	background: repeating-linear-gradient(45deg, #ff0, #ff0 10px, #eee 10px, #eee 20px);
}.tc-plugin-info-disabled:hover {
	background: -webkit-repeating-linear-gradient(45deg, #aa0, #aa0 10px, #888 10px, #888 20px);
	background: repeating-linear-gradient(45deg, #aa0, #aa0 10px, #888 10px, #888 20px);
}a.tc-tiddlylink.tc-plugin-info:hover {
	text-decoration: none;
	background-color: #3949ab;
	color: #FAFAFA;
	fill: rgba(0, 0, 0, 0.87);
}a.tc-tiddlylink.tc-plugin-info:hover > .tc-plugin-info-chunk > svg {
	fill: #FAFAFA;
}.tc-plugin-info-chunk {
	margin: 2px;
}.tc-plugin-info-chunk.tc-plugin-info-toggle {
	flex-grow: 0;
	flex-shrink: 0;
	line-height: 1;
}.tc-plugin-info-chunk.tc-plugin-info-icon {
	flex-grow: 0;
	flex-shrink: 0;
	line-height: 1;
}.tc-plugin-info-chunk.tc-plugin-info-description {
	flex-grow: 1;
}.tc-plugin-info-chunk.tc-plugin-info-buttons {
	font-size: 0.8em;
	line-height: 1.2;
	flex-grow: 0;
	flex-shrink: 0;
	text-align: right;
}.tc-plugin-info-chunk.tc-plugin-info-description h1 {
	font-size: 1em;
	line-height: 1.2;
	margin: 2px 0 2px 0;
}.tc-plugin-info-chunk.tc-plugin-info-description h2 {
	font-size: 0.8em;
	line-height: 1.2;
	margin: 2px 0 2px 0;
}.tc-plugin-info-chunk.tc-plugin-info-description div {
	font-size: 0.7em;
	line-height: 1.2;
	margin: 2px 0 2px 0;
}.tc-plugin-info-chunk.tc-plugin-info-toggle img, .tc-plugin-info-chunk.tc-plugin-info-toggle svg {
	width: 1em;
	height: 1em;
}.tc-plugin-info-chunk.tc-plugin-info-icon img, .tc-plugin-info-chunk.tc-plugin-info-icon svg {
	width: 2em;
	height: 2em;
}.tc-plugin-info-dropdown {
	border: 1px solid rgba(0, 0, 0, 0.54);
	background: #FAFAFA;
	margin-top: -8px;
}.tc-plugin-info-dropdown-message {
	background: #FAFAFA;
	padding: 0.5em 1em 0.5em 1em;
	font-weight: bold;
	font-size: 0.8em;
}.tc-plugin-info-dropdown-body {
	padding: 1em 1em 0 1em;
	background: #FAFAFA;
}.tc-plugin-info-sub-plugins {
	padding: 0.5em;
	margin: 0 1em 1em 1em;
	background: #FFFFFF;
}.tc-install-plugin {
	font-weight: bold;
	background: green;
	color: white;
	fill: white;
	border-radius: 4px;
	padding: 3px;
}.tc-install-plugin.tc-reinstall-downgrade {
	background: red;
}.tc-install-plugin.tc-reinstall {
	background: blue;
}.tc-install-plugin.tc-reinstall-upgrade {
	background: orange;
}.tc-check-list {
	line-height: 2em;
}.tc-check-list .tc-image-button {
	height: 1.5em;
}/*
** Message boxes
*/.tc-message-box {
	border: 1px solid rgba(0, 0, 0, 0.12);
	background: #FAFAFA;
	padding: 0px 21px 0px 21px;
	font-size: 12px;
	line-height: 18px;
	color: rgba(0, 0, 0, 0.54);
}.tc-message-box svg {
	width: 1em;
	height: 1em;
	vertical-align: text-bottom;
}/*
** Pictures
*/.tc-bordered-image {
	border: 1px solid rgba(0, 0, 0, 0.54);
	padding: 5px;
	margin: 5px;
}/*
** Floats
*/.tc-float-right {
	float: right;
}/*
** Chooser
*/.tc-chooser {
	border-right: 1px solid rgba(0, 0, 0, 0.1);
	border-left: 1px solid rgba(0, 0, 0, 0.1);
}.tc-chooser-item {
	border-bottom: 1px solid rgba(0, 0, 0, 0.1);
	border-top: 1px solid rgba(0, 0, 0, 0.1);
	padding: 2px 4px 2px 14px;
}.tc-drop-down .tc-chooser-item {
	padding: 2px;
}.tc-chosen,
.tc-chooser-item:hover {
	background-color: rgba(0, 0, 0, 0.1);
	border-color: rgba(0, 0, 0, 0.04);
}.tc-chosen .tc-tiddlylink {
	cursor:default;
}.tc-chooser-item .tc-tiddlylink {
	display: block;
	text-decoration: none;
	background-color: transparent;
}.tc-chooser-item:hover .tc-tiddlylink:hover {
	text-decoration: none;
}.tc-drop-down .tc-chosen .tc-tiddlylink,
.tc-drop-down .tc-chooser-item .tc-tiddlylink:hover {
	color: rgba(0, 0, 0, 0.87);
}.tc-chosen > .tc-tiddlylink:before {
	margin-left: -10px;
	position: relative;
	content: "» ";
}.tc-chooser-item svg,
.tc-chooser-item img{
	width: 1em;
	height: 1em;
	vertical-align: middle;
}.tc-language-chooser .tc-image-button img {
	width: 2em;
	vertical-align: -0.15em;
}/*
** Palette swatches
*/.tc-swatches-horiz {
}.tc-swatches-horiz .tc-swatch {
	display: inline-block;
}.tc-swatch {
	width: 2em;
	height: 2em;
	margin: 0.4em;
	border: 1px solid #888;
}input.tc-palette-manager-colour-input {
	width: 100%;
	padding: 0;
}/*
** Table of contents
*/.tc-sidebar-lists .tc-table-of-contents {
	white-space: nowrap;
}.tc-table-of-contents button {
	color: rgba(0, 0, 0, 0.54);
}.tc-table-of-contents svg {
	width: 0.7em;
	height: 0.7em;
	vertical-align: middle;
	fill: rgba(0, 0, 0, 0.54);
}.tc-table-of-contents ol {
	list-style-type: none;
	padding-left: 0;
}.tc-table-of-contents ol ol {
	padding-left: 1em;
}.tc-table-of-contents li {
	font-size: 1.0em;
	font-weight: bold;
}.tc-table-of-contents li a {
	font-weight: bold;
}.tc-table-of-contents li li {
	font-size: 0.95em;
	font-weight: normal;
	line-height: 1.4;
}.tc-table-of-contents li li a {
	font-weight: normal;
}.tc-table-of-contents li li li {
	font-size: 0.95em;
	font-weight: normal;
	line-height: 1.5;
}.tc-table-of-contents li li li li {
	font-size: 0.95em;
	font-weight: normal;
}.tc-tabbed-table-of-contents {
	display: -webkit-flex;
	display: flex;
}.tc-tabbed-table-of-contents .tc-table-of-contents {
	z-index: 100;
	display: inline-block;
	padding-left: 1em;
	max-width: 50%;
	-webkit-flex: 0 0 auto;
	flex: 0 0 auto;
	background: transparent;
	border-left: 1px solid transparent;
	border-top: 1px solid transparent;
	border-bottom: 1px solid transparent;
}.tc-tabbed-table-of-contents .tc-table-of-contents .toc-item > a,
.tc-tabbed-table-of-contents .tc-table-of-contents .toc-item-selected > a {
	display: block;
	padding: 0.12em 1em 0.12em 0.25em;
}.tc-tabbed-table-of-contents .tc-table-of-contents .toc-item > a {
	border-top: 1px solid transparent;
	border-left: 1px solid transparent;
	border-bottom: 1px solid transparent;
}.tc-tabbed-table-of-contents .tc-table-of-contents .toc-item > a:hover {
	text-decoration: none;
	border-top: 1px solid transparent;
	border-left: 1px solid transparent;
	border-bottom: 1px solid transparent;
	background: transparent;
}.tc-tabbed-table-of-contents .tc-table-of-contents .toc-item-selected > a {
	border-top: 1px solid transparent;
	border-left: 1px solid transparent;
	border-bottom: 1px solid transparent;
	background: #FAFAFA;
	margin-right: -1px;
}.tc-tabbed-table-of-contents .tc-table-of-contents .toc-item-selected > a:hover {
	text-decoration: none;
}.tc-tabbed-table-of-contents .tc-tabbed-table-of-contents-content {
	display: inline-block;
	vertical-align: top;
	padding-left: 1.5em;
	padding-right: 1.5em;
	border: 1px solid transparent;
	-webkit-flex: 1 0 50%;
	flex: 1 0 50%;
}/*
** Dirty indicator
*/html body.tc-dirty span.tc-dirty-indicator, html body.tc-dirty span.tc-dirty-indicator svg {
	fill: #c80000;
	color: #c80000;
}/*
** File inputs
*/.tc-file-input-wrapper {
	position: relative;
	overflow: hidden;
	display: inline-block;
	vertical-align: middle;
}.tc-file-input-wrapper input[type=file] {
	position: absolute;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	font-size: 999px;
	max-width: 100%;
	max-height: 100%;
	filter: alpha(opacity=0);
	opacity: 0;
	outline: none;
	background: white;
	cursor: pointer;
	display: inline-block;
}::-webkit-file-upload-button {
	cursor:pointer;
}/*
** Thumbnail macros
*/.tc-thumbnail-wrapper {
	position: relative;
	display: inline-block;
	margin: 6px;
	vertical-align: top;
}.tc-thumbnail-right-wrapper {
	float:right;
	margin: 0.5em 0 0.5em 0.5em;
}.tc-thumbnail-image {
	text-align: center;
	overflow: hidden;
	border-radius: 3px;
}.tc-thumbnail-image svg,
.tc-thumbnail-image img {
	filter: alpha(opacity=1);
	opacity: 1;
	min-width: 100%;
	min-height: 100%;
	max-width: 100%;
}.tc-thumbnail-wrapper:hover .tc-thumbnail-image svg,
.tc-thumbnail-wrapper:hover .tc-thumbnail-image img {
	filter: alpha(opacity=0.8);
	opacity: 0.8;
}.tc-thumbnail-background {
	position: absolute;
	border-radius: 3px;
}.tc-thumbnail-icon svg,
.tc-thumbnail-icon img {
	width: 3em;
	height: 3em;
	
  -webkit-filter: drop-shadow(2px 2px 4px rgba(0,0,0,0.3));
     -moz-filter: drop-shadow(2px 2px 4px rgba(0,0,0,0.3));
          filter: drop-shadow(2px 2px 4px rgba(0,0,0,0.3));

}.tc-thumbnail-wrapper:hover .tc-thumbnail-icon svg,
.tc-thumbnail-wrapper:hover .tc-thumbnail-icon img {
	fill: #fff;
	
  -webkit-filter: drop-shadow(3px 3px 4px rgba(0,0,0,0.6));
     -moz-filter: drop-shadow(3px 3px 4px rgba(0,0,0,0.6));
          filter: drop-shadow(3px 3px 4px rgba(0,0,0,0.6));

}.tc-thumbnail-icon {
	position: absolute;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	display: -webkit-flex;
	-webkit-align-items: center;
	-webkit-justify-content: center;
	display: flex;
	align-items: center;
	justify-content: center;
}.tc-thumbnail-caption {
	position: absolute;
	background-color: #777;
	color: #fff;
	text-align: center;
	bottom: 0;
	width: 100%;
	filter: alpha(opacity=0.9);
	opacity: 0.9;
	line-height: 1.4;
	border-bottom-left-radius: 3px;
	border-bottom-right-radius: 3px;
}.tc-thumbnail-wrapper:hover .tc-thumbnail-caption {
	filter: alpha(opacity=1);
	opacity: 1;
}/*
** Diffs
*/.tc-diff-equal {
	background-color: ;
	color: rgba(0, 0, 0, 0.87);
}.tc-diff-insert {
	background-color: #aaefad;
	color: rgba(0, 0, 0, 0.87);
}.tc-diff-delete {
	background-color: #ffc9c9;
	color: rgba(0, 0, 0, 0.87);
}.tc-diff-invisible {
	background-color: ;
	color: rgba(0, 0, 0, 0.54);
}.tc-diff-tiddlers th {
	text-align: right;
	background: #FAFAFA;
	font-weight: normal;
	font-style: italic;
}.tc-diff-tiddlers pre {
	margin: 0;
	padding: 0;
	border: none;
	background: none;
}/*
** Errors
*/.tc-error {
	background: #f00;
	color: #fff;
}/*
** Tree macro
*/.tc-tree div {
	padding-left: 14px;
}.tc-tree ol {
	list-style-type: none;
	padding-left: 0;
	margin-top: 0;
}.tc-tree ol ol {
	padding-left: 1em;
}.tc-tree button {
	color: #acacac;
}.tc-tree svg {
	fill: #acacac;
}.tc-tree span svg {
	width: 1em;
	height: 1em;
	vertical-align: baseline;
}.tc-tree li span {
	color: lightgray;
}select {
	color: rgba(0, 0, 0, 0.87);
	background: #FAFAFA;
}/*
** Utility classes for SVG icons
*/.tc-fill-background {
	fill: #FAFAFA;
}/*
** Flexbox utility classes
*/.tc-flex {
	display: -webkit-flex;
	display: flex;
}.tc-flex-column {
	flex-direction: column;
}.tc-flex-row {
	flex-direction: row;
}.tc-flex-grow-1 {
	flex-grow: 1;
}.tc-flex-grow-2 {
	flex-grow: 2;
}/*
** Other utility classes
*/.tc-tiny-gap {
	margin-left: .25em;
	margin-right: .25em;
}.tc-tiny-gap-left {
	margin-left: .25em;
}.tc-tiny-gap-right {
	margin-right: .25em;
}.tc-small-gap {
	margin-left: .5em;
	margin-right: .5em;
}.tc-small-gap-left {
	margin-left: .5em;
}.tc-small-gap-right {
	margin-right: .5em;
}.tc-big-gap {
	margin-left: 1em;
	margin-right: 1em;
}.tc-big-gap-left {
	margin-left: 1em;
}.tc-big-gap-right {
	margin-right: 1em;
}.tc-word-break {
	word-break: break-all;
}
/*  drag and drop elements */
.kk-todolist-placeholder { 
	position:relative; 
	height:0; 	
	border:0 !important; 
	border-bottom:1px dotted grey !important; 
}

.kk-todolist-draggable-list .tc-draggable  { cursor: default !important; }
/* Todolist main ui dynamic props which follow palette colors*/.kk-todolist-ui svg{
	fill:#aaaaaa;
}.kk-todolist-ui button:hover svg {
	fill: #888888; 
}.kk-todolist-row:hover {
	/* background-color: #f6f6f6;*/
	background-color: rgba(0, 0, 0, 0.1);
}.kk-todolist-row .kk-todolist-delete {
	opacity: 0.3;
}.kk-todolist-row:hover .kk-todolist-delete {
	opacity: 1;
}
/* Todolist main ui */
.kk-todolist-ui{
	min-width:320px; /* controls the minimum width of whole ui */
}


/* Todolist header ui */

.kk-todolist-header-ui{
	display: flex;
	width: 100%;
}
.kk-todolist-header-ui > div{
	margin: 2px;
	flex-grow:0;	
}
.kk-todolist-header-ui .kk-todolist-header-textbox{
	flex-grow:1;	
}

/* Todolist items ui */
.kk-todolist-row{
	display: flex;	
	width: 100%; /* for larg screen width> 960px*/
	flex-wrap: nowrap;
}

.kk-todolist-row .kk-todolist-done,
.kk-todolist-row .kk-todolist-priority,
.kk-todolist-row .kk-todolist-delete {
	flex-grow:0; width:15px;
}

.kk-todolist-row .kk-todolist-desc{
	flex-grow:1; 
	width: calc(100% - 50px); 
	padding-left: 10px;
	padding-right: 10px;
}

.kk-todolist-row .kk-todolist-priority{
	margin-right:5px;
}/* completed item */

.kk-todolist-item-done {
	text-decoration: red line-through;
	font-style: italic;
}

/* inputbox for add-task */
.kk-todolist-input-textbox {
	width:100%;
	padding-left: 5px;
	border: none;
	border-bottom: 1px dotted grey;
}

.kk-todolist-input-textbox:focus {
	outline: none;
	border-bottom: 1px solid #5778d8;
	background: transparent;
}

/* item timestamp */
.kk-todolist-date {
	font-size:0.8em;
	color:#c0c0c0;
}

/* Item categories */
.kk-todolist-category-c1,
.kk-todolist-category-c2 {
	padding-right:3px;
}

.kk-todolist-category-c1 svg, 
.kk-todolist-category-c2 svg  {
	opacity:0.70;
	vertical-align: middle;
	width: 1em;
	height: 1em;
}

.kk-todolist-category-c1 svg{
	fill:#8B0000;
}

.kk-todolist-category-c2 svg{
	fill:#006400;
}/*!
* reveal.js 4.0.2
* https://revealjs.com
* MIT licensed
*
* Copyright (C) 2020 Hakim El Hattab, https://hakim.se
*/
.reveal .r-stretch,.reveal .stretch{max-width:none;max-height:none}.reveal pre.r-stretch code,.reveal pre.stretch code{height:100%;max-height:100%;box-sizing:border-box}.reveal .r-stack{display:grid}.reveal .r-stack>*{grid-area:1/1;margin:auto}.reveal .r-hstack,.reveal .r-vstack{display:flex}.reveal .r-vstack{flex-direction:column;align-items:center;justify-content:center}.reveal .r-hstack{flex-direction:row;align-items:center;justify-content:center}.reveal .items-stretch{align-items:stretch}.reveal .items-start{align-items:flex-start}.reveal .items-center{align-items:center}.reveal .items-end{align-items:flex-end}.reveal .justify-between{justify-content:space-between}.reveal .justify-around{justify-content:space-around}.reveal .justify-start{justify-content:flex-start}.reveal .justify-center{justify-content:center}.reveal .justify-end{justify-content:flex-end}html.reveal-full-page{width:100%;height:100%;height:100vh;height:calc(var(--vh,1vh) * 100);overflow:hidden}.reveal-viewport{height:100%;overflow:hidden;position:relative;line-height:1;margin:0;background-color:#fff;color:#000}.reveal .slides section .fragment{opacity:0;visibility:hidden;transition:all .2s ease;will-change:opacity}.reveal .slides section .fragment.visible{opacity:1;visibility:inherit}.reveal .slides section .fragment.disabled{transition:none}.reveal .slides section .fragment.grow{opacity:1;visibility:inherit}.reveal .slides section .fragment.grow.visible{transform:scale(1.3)}.reveal .slides section .fragment.shrink{opacity:1;visibility:inherit}.reveal .slides section .fragment.shrink.visible{transform:scale(.7)}.reveal .slides section .fragment.zoom-in{transform:scale(.1)}.reveal .slides section .fragment.zoom-in.visible{transform:none}.reveal .slides section .fragment.fade-out{opacity:1;visibility:inherit}.reveal .slides section .fragment.fade-out.visible{opacity:0;visibility:hidden}.reveal .slides section .fragment.semi-fade-out{opacity:1;visibility:inherit}.reveal .slides section .fragment.semi-fade-out.visible{opacity:.5;visibility:inherit}.reveal .slides section .fragment.strike{opacity:1;visibility:inherit}.reveal .slides section .fragment.strike.visible{text-decoration:line-through}.reveal .slides section .fragment.fade-up{transform:translate(0,40px)}.reveal .slides section .fragment.fade-up.visible{transform:translate(0,0)}.reveal .slides section .fragment.fade-down{transform:translate(0,-40px)}.reveal .slides section .fragment.fade-down.visible{transform:translate(0,0)}.reveal .slides section .fragment.fade-right{transform:translate(-40px,0)}.reveal .slides section .fragment.fade-right.visible{transform:translate(0,0)}.reveal .slides section .fragment.fade-left{transform:translate(40px,0)}.reveal .slides section .fragment.fade-left.visible{transform:translate(0,0)}.reveal .slides section .fragment.current-visible,.reveal .slides section .fragment.fade-in-then-out{opacity:0;visibility:hidden}.reveal .slides section .fragment.current-visible.current-fragment,.reveal .slides section .fragment.fade-in-then-out.current-fragment{opacity:1;visibility:inherit}.reveal .slides section .fragment.fade-in-then-semi-out{opacity:0;visibility:hidden}.reveal .slides section .fragment.fade-in-then-semi-out.visible{opacity:.5;visibility:inherit}.reveal .slides section .fragment.fade-in-then-semi-out.current-fragment{opacity:1;visibility:inherit}.reveal .slides section .fragment.highlight-blue,.reveal .slides section .fragment.highlight-current-blue,.reveal .slides section .fragment.highlight-current-green,.reveal .slides section .fragment.highlight-current-red,.reveal .slides section .fragment.highlight-green,.reveal .slides section .fragment.highlight-red{opacity:1;visibility:inherit}.reveal .slides section .fragment.highlight-red.visible{color:#ff2c2d}.reveal .slides section .fragment.highlight-green.visible{color:#17ff2e}.reveal .slides section .fragment.highlight-blue.visible{color:#1b91ff}.reveal .slides section .fragment.highlight-current-red.current-fragment{color:#ff2c2d}.reveal .slides section .fragment.highlight-current-green.current-fragment{color:#17ff2e}.reveal .slides section .fragment.highlight-current-blue.current-fragment{color:#1b91ff}.reveal:after{content:'';font-style:italic}.reveal iframe{z-index:1}.reveal a{position:relative}@keyframes bounce-right{0%,10%,25%,40%,50%{transform:translateX(0)}20%{transform:translateX(10px)}30%{transform:translateX(-5px)}}@keyframes bounce-left{0%,10%,25%,40%,50%{transform:translateX(0)}20%{transform:translateX(-10px)}30%{transform:translateX(5px)}}@keyframes bounce-down{0%,10%,25%,40%,50%{transform:translateY(0)}20%{transform:translateY(10px)}30%{transform:translateY(-5px)}}.reveal .controls{display:none;position:absolute;top:auto;bottom:12px;right:12px;left:auto;z-index:11;color:#000;pointer-events:none;font-size:10px}.reveal .controls button{position:absolute;padding:0;background-color:transparent;border:0;outline:0;cursor:pointer;color:currentColor;transform:scale(.9999);transition:color .2s ease,opacity .2s ease,transform .2s ease;z-index:2;pointer-events:auto;font-size:inherit;visibility:hidden;opacity:0;-webkit-appearance:none;-webkit-tap-highlight-color:transparent}.reveal .controls .controls-arrow:after,.reveal .controls .controls-arrow:before{content:'';position:absolute;top:0;left:0;width:2.6em;height:.5em;border-radius:.25em;background-color:currentColor;transition:all .15s ease,background-color .8s ease;transform-origin:.2em 50%;will-change:transform}.reveal .controls .controls-arrow{position:relative;width:3.6em;height:3.6em}.reveal .controls .controls-arrow:before{transform:translateX(.5em) translateY(1.55em) rotate(45deg)}.reveal .controls .controls-arrow:after{transform:translateX(.5em) translateY(1.55em) rotate(-45deg)}.reveal .controls .controls-arrow:hover:before{transform:translateX(.5em) translateY(1.55em) rotate(40deg)}.reveal .controls .controls-arrow:hover:after{transform:translateX(.5em) translateY(1.55em) rotate(-40deg)}.reveal .controls .controls-arrow:active:before{transform:translateX(.5em) translateY(1.55em) rotate(36deg)}.reveal .controls .controls-arrow:active:after{transform:translateX(.5em) translateY(1.55em) rotate(-36deg)}.reveal .controls .navigate-left{right:6.4em;bottom:3.2em;transform:translateX(-10px)}.reveal .controls .navigate-left.highlight{animation:bounce-left 2s 50 both ease-out}.reveal .controls .navigate-right{right:0;bottom:3.2em;transform:translateX(10px)}.reveal .controls .navigate-right .controls-arrow{transform:rotate(180deg)}.reveal .controls .navigate-right.highlight{animation:bounce-right 2s 50 both ease-out}.reveal .controls .navigate-up{right:3.2em;bottom:6.4em;transform:translateY(-10px)}.reveal .controls .navigate-up .controls-arrow{transform:rotate(90deg)}.reveal .controls .navigate-down{right:3.2em;bottom:-1.4em;padding-bottom:1.4em;transform:translateY(10px)}.reveal .controls .navigate-down .controls-arrow{transform:rotate(-90deg)}.reveal .controls .navigate-down.highlight{animation:bounce-down 2s 50 both ease-out}.reveal .controls[data-controls-back-arrows=faded] .navigate-up.enabled{opacity:.3}.reveal .controls[data-controls-back-arrows=faded] .navigate-up.enabled:hover{opacity:1}.reveal .controls[data-controls-back-arrows=hidden] .navigate-up.enabled{opacity:0;visibility:hidden}.reveal .controls .enabled{visibility:visible;opacity:.9;cursor:pointer;transform:none}.reveal .controls .enabled.fragmented{opacity:.5}.reveal .controls .enabled.fragmented:hover,.reveal .controls .enabled:hover{opacity:1}.reveal:not(.rtl) .controls[data-controls-back-arrows=faded] .navigate-left.enabled{opacity:.3}.reveal:not(.rtl) .controls[data-controls-back-arrows=faded] .navigate-left.enabled:hover{opacity:1}.reveal:not(.rtl) .controls[data-controls-back-arrows=hidden] .navigate-left.enabled{opacity:0;visibility:hidden}.reveal.rtl .controls[data-controls-back-arrows=faded] .navigate-right.enabled{opacity:.3}.reveal.rtl .controls[data-controls-back-arrows=faded] .navigate-right.enabled:hover{opacity:1}.reveal.rtl .controls[data-controls-back-arrows=hidden] .navigate-right.enabled{opacity:0;visibility:hidden}.reveal[data-navigation-mode=linear].has-horizontal-slides .navigate-down,.reveal[data-navigation-mode=linear].has-horizontal-slides .navigate-up{display:none}.reveal:not(.has-vertical-slides) .controls .navigate-left,.reveal[data-navigation-mode=linear].has-horizontal-slides .navigate-left{bottom:1.4em;right:5.5em}.reveal:not(.has-vertical-slides) .controls .navigate-right,.reveal[data-navigation-mode=linear].has-horizontal-slides .navigate-right{bottom:1.4em;right:.5em}.reveal:not(.has-horizontal-slides) .controls .navigate-up{right:1.4em;bottom:5em}.reveal:not(.has-horizontal-slides) .controls .navigate-down{right:1.4em;bottom:.5em}.reveal.has-dark-background .controls{color:#fff}.reveal.has-light-background .controls{color:#000}.reveal.no-hover .controls .controls-arrow:active:before,.reveal.no-hover .controls .controls-arrow:hover:before{transform:translateX(.5em) translateY(1.55em) rotate(45deg)}.reveal.no-hover .controls .controls-arrow:active:after,.reveal.no-hover .controls .controls-arrow:hover:after{transform:translateX(.5em) translateY(1.55em) rotate(-45deg)}@media screen and (min-width:500px){.reveal .controls[data-controls-layout=edges]{top:0;right:0;bottom:0;left:0}.reveal .controls[data-controls-layout=edges] .navigate-down,.reveal .controls[data-controls-layout=edges] .navigate-left,.reveal .controls[data-controls-layout=edges] .navigate-right,.reveal .controls[data-controls-layout=edges] .navigate-up{bottom:auto;right:auto}.reveal .controls[data-controls-layout=edges] .navigate-left{top:50%;left:.8em;margin-top:-1.8em}.reveal .controls[data-controls-layout=edges] .navigate-right{top:50%;right:.8em;margin-top:-1.8em}.reveal .controls[data-controls-layout=edges] .navigate-up{top:.8em;left:50%;margin-left:-1.8em}.reveal .controls[data-controls-layout=edges] .navigate-down{bottom:-.3em;left:50%;margin-left:-1.8em}}.reveal .progress{position:absolute;display:none;height:3px;width:100%;bottom:0;left:0;z-index:10;background-color:rgba(0,0,0,.2);color:#fff}.reveal .progress:after{content:'';display:block;position:absolute;height:10px;width:100%;top:-10px}.reveal .progress span{display:block;height:100%;width:100%;background-color:currentColor;transition:transform .8s cubic-bezier(.26,.86,.44,.985);transform-origin:0 0;transform:scaleX(0)}.reveal .slide-number{position:absolute;display:block;right:8px;bottom:8px;z-index:31;font-family:Helvetica,sans-serif;font-size:12px;line-height:1;color:#fff;background-color:rgba(0,0,0,.4);padding:5px}.reveal .slide-number a{color:currentColor}.reveal .slide-number-delimiter{margin:0 3px}.reveal{position:relative;width:100%;height:100%;overflow:hidden;touch-action:pinch-zoom}.reveal.embedded{touch-action:pan-y}.reveal .slides{position:absolute;width:100%;height:100%;top:0;right:0;bottom:0;left:0;margin:auto;pointer-events:none;overflow:visible;z-index:1;text-align:center;perspective:600px;perspective-origin:50% 40%}.reveal .slides>section{perspective:600px}.reveal .slides>section,.reveal .slides>section>section{display:none;position:absolute;width:100%;padding:20px 0;pointer-events:auto;z-index:10;transform-style:flat;transition:transform-origin .8s cubic-bezier(.26,.86,.44,.985),transform .8s cubic-bezier(.26,.86,.44,.985),visibility .8s cubic-bezier(.26,.86,.44,.985),opacity .8s cubic-bezier(.26,.86,.44,.985)}.reveal[data-transition-speed=fast] .slides section{transition-duration:.4s}.reveal[data-transition-speed=slow] .slides section{transition-duration:1.2s}.reveal .slides section[data-transition-speed=fast]{transition-duration:.4s}.reveal .slides section[data-transition-speed=slow]{transition-duration:1.2s}.reveal .slides>section.stack{padding-top:0;padding-bottom:0;pointer-events:none;height:100%}.reveal .slides>section.present,.reveal .slides>section>section.present{display:block;z-index:11;opacity:1}.reveal .slides>section:empty,.reveal .slides>section>section:empty,.reveal .slides>section>section[data-background-interactive],.reveal .slides>section[data-background-interactive]{pointer-events:none}.reveal.center,.reveal.center .slides,.reveal.center .slides section{min-height:0!important}.reveal .slides>section:not(.present),.reveal .slides>section>section:not(.present){pointer-events:none}.reveal.overview .slides>section,.reveal.overview .slides>section>section{pointer-events:auto}.reveal .slides>section.future,.reveal .slides>section.past,.reveal .slides>section>section.future,.reveal .slides>section>section.past{opacity:0}.reveal.slide section{-webkit-backface-visibility:hidden;backface-visibility:hidden}.reveal .slides>section[data-transition=slide].past,.reveal .slides>section[data-transition~=slide-out].past,.reveal.slide .slides>section:not([data-transition]).past{transform:translate(-150%,0)}.reveal .slides>section[data-transition=slide].future,.reveal .slides>section[data-transition~=slide-in].future,.reveal.slide .slides>section:not([data-transition]).future{transform:translate(150%,0)}.reveal .slides>section>section[data-transition=slide].past,.reveal .slides>section>section[data-transition~=slide-out].past,.reveal.slide .slides>section>section:not([data-transition]).past{transform:translate(0,-150%)}.reveal .slides>section>section[data-transition=slide].future,.reveal .slides>section>section[data-transition~=slide-in].future,.reveal.slide .slides>section>section:not([data-transition]).future{transform:translate(0,150%)}.reveal.linear section{-webkit-backface-visibility:hidden;backface-visibility:hidden}.reveal .slides>section[data-transition=linear].past,.reveal .slides>section[data-transition~=linear-out].past,.reveal.linear .slides>section:not([data-transition]).past{transform:translate(-150%,0)}.reveal .slides>section[data-transition=linear].future,.reveal .slides>section[data-transition~=linear-in].future,.reveal.linear .slides>section:not([data-transition]).future{transform:translate(150%,0)}.reveal .slides>section>section[data-transition=linear].past,.reveal .slides>section>section[data-transition~=linear-out].past,.reveal.linear .slides>section>section:not([data-transition]).past{transform:translate(0,-150%)}.reveal .slides>section>section[data-transition=linear].future,.reveal .slides>section>section[data-transition~=linear-in].future,.reveal.linear .slides>section>section:not([data-transition]).future{transform:translate(0,150%)}.reveal .slides section[data-transition=default].stack,.reveal.default .slides section.stack{transform-style:preserve-3d}.reveal .slides>section[data-transition=default].past,.reveal .slides>section[data-transition~=default-out].past,.reveal.default .slides>section:not([data-transition]).past{transform:translate3d(-100%,0,0) rotateY(-90deg) translate3d(-100%,0,0)}.reveal .slides>section[data-transition=default].future,.reveal .slides>section[data-transition~=default-in].future,.reveal.default .slides>section:not([data-transition]).future{transform:translate3d(100%,0,0) rotateY(90deg) translate3d(100%,0,0)}.reveal .slides>section>section[data-transition=default].past,.reveal .slides>section>section[data-transition~=default-out].past,.reveal.default .slides>section>section:not([data-transition]).past{transform:translate3d(0,-300px,0) rotateX(70deg) translate3d(0,-300px,0)}.reveal .slides>section>section[data-transition=default].future,.reveal .slides>section>section[data-transition~=default-in].future,.reveal.default .slides>section>section:not([data-transition]).future{transform:translate3d(0,300px,0) rotateX(-70deg) translate3d(0,300px,0)}.reveal .slides section[data-transition=convex].stack,.reveal.convex .slides section.stack{transform-style:preserve-3d}.reveal .slides>section[data-transition=convex].past,.reveal .slides>section[data-transition~=convex-out].past,.reveal.convex .slides>section:not([data-transition]).past{transform:translate3d(-100%,0,0) rotateY(-90deg) translate3d(-100%,0,0)}.reveal .slides>section[data-transition=convex].future,.reveal .slides>section[data-transition~=convex-in].future,.reveal.convex .slides>section:not([data-transition]).future{transform:translate3d(100%,0,0) rotateY(90deg) translate3d(100%,0,0)}.reveal .slides>section>section[data-transition=convex].past,.reveal .slides>section>section[data-transition~=convex-out].past,.reveal.convex .slides>section>section:not([data-transition]).past{transform:translate3d(0,-300px,0) rotateX(70deg) translate3d(0,-300px,0)}.reveal .slides>section>section[data-transition=convex].future,.reveal .slides>section>section[data-transition~=convex-in].future,.reveal.convex .slides>section>section:not([data-transition]).future{transform:translate3d(0,300px,0) rotateX(-70deg) translate3d(0,300px,0)}.reveal .slides section[data-transition=concave].stack,.reveal.concave .slides section.stack{transform-style:preserve-3d}.reveal .slides>section[data-transition=concave].past,.reveal .slides>section[data-transition~=concave-out].past,.reveal.concave .slides>section:not([data-transition]).past{transform:translate3d(-100%,0,0) rotateY(90deg) translate3d(-100%,0,0)}.reveal .slides>section[data-transition=concave].future,.reveal .slides>section[data-transition~=concave-in].future,.reveal.concave .slides>section:not([data-transition]).future{transform:translate3d(100%,0,0) rotateY(-90deg) translate3d(100%,0,0)}.reveal .slides>section>section[data-transition=concave].past,.reveal .slides>section>section[data-transition~=concave-out].past,.reveal.concave .slides>section>section:not([data-transition]).past{transform:translate3d(0,-80%,0) rotateX(-70deg) translate3d(0,-80%,0)}.reveal .slides>section>section[data-transition=concave].future,.reveal .slides>section>section[data-transition~=concave-in].future,.reveal.concave .slides>section>section:not([data-transition]).future{transform:translate3d(0,80%,0) rotateX(70deg) translate3d(0,80%,0)}.reveal .slides section[data-transition=zoom],.reveal.zoom .slides section:not([data-transition]){transition-timing-function:ease}.reveal .slides>section[data-transition=zoom].past,.reveal .slides>section[data-transition~=zoom-out].past,.reveal.zoom .slides>section:not([data-transition]).past{visibility:hidden;transform:scale(16)}.reveal .slides>section[data-transition=zoom].future,.reveal .slides>section[data-transition~=zoom-in].future,.reveal.zoom .slides>section:not([data-transition]).future{visibility:hidden;transform:scale(.2)}.reveal .slides>section>section[data-transition=zoom].past,.reveal .slides>section>section[data-transition~=zoom-out].past,.reveal.zoom .slides>section>section:not([data-transition]).past{transform:scale(16)}.reveal .slides>section>section[data-transition=zoom].future,.reveal .slides>section>section[data-transition~=zoom-in].future,.reveal.zoom .slides>section>section:not([data-transition]).future{transform:scale(.2)}.reveal.cube .slides{perspective:1300px}.reveal.cube .slides section{padding:30px;min-height:700px;-webkit-backface-visibility:hidden;backface-visibility:hidden;box-sizing:border-box;transform-style:preserve-3d}.reveal.center.cube .slides section{min-height:0}.reveal.cube .slides section:not(.stack):before{content:'';position:absolute;display:block;width:100%;height:100%;left:0;top:0;background:rgba(0,0,0,.1);border-radius:4px;transform:translateZ(-20px)}.reveal.cube .slides section:not(.stack):after{content:'';position:absolute;display:block;width:90%;height:30px;left:5%;bottom:0;background:0 0;z-index:1;border-radius:4px;box-shadow:0 95px 25px rgba(0,0,0,.2);transform:translateZ(-90px) rotateX(65deg)}.reveal.cube .slides>section.stack{padding:0;background:0 0}.reveal.cube .slides>section.past{transform-origin:100% 0;transform:translate3d(-100%,0,0) rotateY(-90deg)}.reveal.cube .slides>section.future{transform-origin:0 0;transform:translate3d(100%,0,0) rotateY(90deg)}.reveal.cube .slides>section>section.past{transform-origin:0 100%;transform:translate3d(0,-100%,0) rotateX(90deg)}.reveal.cube .slides>section>section.future{transform-origin:0 0;transform:translate3d(0,100%,0) rotateX(-90deg)}.reveal.page .slides{perspective-origin:0 50%;perspective:3000px}.reveal.page .slides section{padding:30px;min-height:700px;box-sizing:border-box;transform-style:preserve-3d}.reveal.page .slides section.past{z-index:12}.reveal.page .slides section:not(.stack):before{content:'';position:absolute;display:block;width:100%;height:100%;left:0;top:0;background:rgba(0,0,0,.1);transform:translateZ(-20px)}.reveal.page .slides section:not(.stack):after{content:'';position:absolute;display:block;width:90%;height:30px;left:5%;bottom:0;background:0 0;z-index:1;border-radius:4px;box-shadow:0 95px 25px rgba(0,0,0,.2);-webkit-transform:translateZ(-90px) rotateX(65deg)}.reveal.page .slides>section.stack{padding:0;background:0 0}.reveal.page .slides>section.past{transform-origin:0 0;transform:translate3d(-40%,0,0) rotateY(-80deg)}.reveal.page .slides>section.future{transform-origin:100% 0;transform:translate3d(0,0,0)}.reveal.page .slides>section>section.past{transform-origin:0 0;transform:translate3d(0,-40%,0) rotateX(80deg)}.reveal.page .slides>section>section.future{transform-origin:0 100%;transform:translate3d(0,0,0)}.reveal .slides section[data-transition=fade],.reveal.fade .slides section:not([data-transition]),.reveal.fade .slides>section>section:not([data-transition]){transform:none;transition:opacity .5s}.reveal.fade.overview .slides section,.reveal.fade.overview .slides>section>section{transition:none}.reveal .slides section[data-transition=none],.reveal.none .slides section:not([data-transition]){transform:none;transition:none}.reveal .pause-overlay{position:absolute;top:0;left:0;width:100%;height:100%;background:#000;visibility:hidden;opacity:0;z-index:100;transition:all 1s ease}.reveal .pause-overlay .resume-button{position:absolute;bottom:20px;right:20px;color:#ccc;border-radius:2px;padding:6px 14px;border:2px solid #ccc;font-size:16px;background:0 0;cursor:pointer}.reveal .pause-overlay .resume-button:hover{color:#fff;border-color:#fff}.reveal.paused .pause-overlay{visibility:visible;opacity:1}.reveal .no-transition,.reveal .no-transition *,.reveal .slides.disable-slide-transitions section{transition:none!important}.reveal .slides.disable-slide-transitions section{transform:none!important}.reveal .backgrounds{position:absolute;width:100%;height:100%;top:0;left:0;perspective:600px}.reveal .slide-background{display:none;position:absolute;width:100%;height:100%;opacity:0;visibility:hidden;overflow:hidden;background-color:rgba(0,0,0,0);transition:all .8s cubic-bezier(.26,.86,.44,.985)}.reveal .slide-background-content{position:absolute;width:100%;height:100%;background-position:50% 50%;background-repeat:no-repeat;background-size:cover}.reveal .slide-background.stack{display:block}.reveal .slide-background.present{opacity:1;visibility:visible;z-index:2}.print-pdf .reveal .slide-background{opacity:1!important;visibility:visible!important}.reveal .slide-background video{position:absolute;width:100%;height:100%;max-width:none;max-height:none;top:0;left:0;-o-object-fit:cover;object-fit:cover}.reveal .slide-background[data-background-size=contain] video{-o-object-fit:contain;object-fit:contain}.reveal>.backgrounds .slide-background[data-background-transition=none],.reveal[data-background-transition=none]>.backgrounds .slide-background{transition:none}.reveal>.backgrounds .slide-background[data-background-transition=slide],.reveal[data-background-transition=slide]>.backgrounds .slide-background{opacity:1;-webkit-backface-visibility:hidden;backface-visibility:hidden}.reveal>.backgrounds .slide-background.past[data-background-transition=slide],.reveal[data-background-transition=slide]>.backgrounds .slide-background.past{transform:translate(-100%,0)}.reveal>.backgrounds .slide-background.future[data-background-transition=slide],.reveal[data-background-transition=slide]>.backgrounds .slide-background.future{transform:translate(100%,0)}.reveal>.backgrounds .slide-background>.slide-background.past[data-background-transition=slide],.reveal[data-background-transition=slide]>.backgrounds .slide-background>.slide-background.past{transform:translate(0,-100%)}.reveal>.backgrounds .slide-background>.slide-background.future[data-background-transition=slide],.reveal[data-background-transition=slide]>.backgrounds .slide-background>.slide-background.future{transform:translate(0,100%)}.reveal>.backgrounds .slide-background.past[data-background-transition=convex],.reveal[data-background-transition=convex]>.backgrounds .slide-background.past{opacity:0;transform:translate3d(-100%,0,0) rotateY(-90deg) translate3d(-100%,0,0)}.reveal>.backgrounds .slide-background.future[data-background-transition=convex],.reveal[data-background-transition=convex]>.backgrounds .slide-background.future{opacity:0;transform:translate3d(100%,0,0) rotateY(90deg) translate3d(100%,0,0)}.reveal>.backgrounds .slide-background>.slide-background.past[data-background-transition=convex],.reveal[data-background-transition=convex]>.backgrounds .slide-background>.slide-background.past{opacity:0;transform:translate3d(0,-100%,0) rotateX(90deg) translate3d(0,-100%,0)}.reveal>.backgrounds .slide-background>.slide-background.future[data-background-transition=convex],.reveal[data-background-transition=convex]>.backgrounds .slide-background>.slide-background.future{opacity:0;transform:translate3d(0,100%,0) rotateX(-90deg) translate3d(0,100%,0)}.reveal>.backgrounds .slide-background.past[data-background-transition=concave],.reveal[data-background-transition=concave]>.backgrounds .slide-background.past{opacity:0;transform:translate3d(-100%,0,0) rotateY(90deg) translate3d(-100%,0,0)}.reveal>.backgrounds .slide-background.future[data-background-transition=concave],.reveal[data-background-transition=concave]>.backgrounds .slide-background.future{opacity:0;transform:translate3d(100%,0,0) rotateY(-90deg) translate3d(100%,0,0)}.reveal>.backgrounds .slide-background>.slide-background.past[data-background-transition=concave],.reveal[data-background-transition=concave]>.backgrounds .slide-background>.slide-background.past{opacity:0;transform:translate3d(0,-100%,0) rotateX(-90deg) translate3d(0,-100%,0)}.reveal>.backgrounds .slide-background>.slide-background.future[data-background-transition=concave],.reveal[data-background-transition=concave]>.backgrounds .slide-background>.slide-background.future{opacity:0;transform:translate3d(0,100%,0) rotateX(90deg) translate3d(0,100%,0)}.reveal>.backgrounds .slide-background[data-background-transition=zoom],.reveal[data-background-transition=zoom]>.backgrounds .slide-background{transition-timing-function:ease}.reveal>.backgrounds .slide-background.past[data-background-transition=zoom],.reveal[data-background-transition=zoom]>.backgrounds .slide-background.past{opacity:0;visibility:hidden;transform:scale(16)}.reveal>.backgrounds .slide-background.future[data-background-transition=zoom],.reveal[data-background-transition=zoom]>.backgrounds .slide-background.future{opacity:0;visibility:hidden;transform:scale(.2)}.reveal>.backgrounds .slide-background>.slide-background.past[data-background-transition=zoom],.reveal[data-background-transition=zoom]>.backgrounds .slide-background>.slide-background.past{opacity:0;visibility:hidden;transform:scale(16)}.reveal>.backgrounds .slide-background>.slide-background.future[data-background-transition=zoom],.reveal[data-background-transition=zoom]>.backgrounds .slide-background>.slide-background.future{opacity:0;visibility:hidden;transform:scale(.2)}.reveal[data-transition-speed=fast]>.backgrounds .slide-background{transition-duration:.4s}.reveal[data-transition-speed=slow]>.backgrounds .slide-background{transition-duration:1.2s}.reveal [data-auto-animate-target^=unmatched]{will-change:opacity}.reveal section[data-auto-animate]:not(.stack):not([data-auto-animate=running]) [data-auto-animate-target^=unmatched]{opacity:0}.reveal.overview{perspective-origin:50% 50%;perspective:700px}.reveal.overview .slides{-moz-transform-style:preserve-3d}.reveal.overview .slides section{height:100%;top:0!important;opacity:1!important;overflow:hidden;visibility:visible!important;cursor:pointer;box-sizing:border-box}.reveal.overview .slides section.present,.reveal.overview .slides section:hover{outline:10px solid rgba(150,150,150,.4);outline-offset:10px}.reveal.overview .slides section .fragment{opacity:1;transition:none}.reveal.overview .slides section:after,.reveal.overview .slides section:before{display:none!important}.reveal.overview .slides>section.stack{padding:0;top:0!important;background:0 0;outline:0;overflow:visible}.reveal.overview .backgrounds{perspective:inherit;-moz-transform-style:preserve-3d}.reveal.overview .backgrounds .slide-background{opacity:1;visibility:visible;outline:10px solid rgba(150,150,150,.1);outline-offset:10px}.reveal.overview .backgrounds .slide-background.stack{overflow:visible}.reveal.overview .slides section,.reveal.overview-deactivating .slides section{transition:none}.reveal.overview .backgrounds .slide-background,.reveal.overview-deactivating .backgrounds .slide-background{transition:none}.reveal.rtl .slides,.reveal.rtl .slides h1,.reveal.rtl .slides h2,.reveal.rtl .slides h3,.reveal.rtl .slides h4,.reveal.rtl .slides h5,.reveal.rtl .slides h6{direction:rtl;font-family:sans-serif}.reveal.rtl code,.reveal.rtl pre{direction:ltr}.reveal.rtl ol,.reveal.rtl ul{text-align:right}.reveal.rtl .progress span{transform-origin:100% 0}.reveal.has-parallax-background .backgrounds{transition:all .8s ease}.reveal.has-parallax-background[data-transition-speed=fast] .backgrounds{transition-duration:.4s}.reveal.has-parallax-background[data-transition-speed=slow] .backgrounds{transition-duration:1.2s}.reveal>.overlay{position:absolute;top:0;left:0;width:100%;height:100%;z-index:1000;background:rgba(0,0,0,.9);transition:all .3s ease}.reveal>.overlay .spinner{position:absolute;display:block;top:50%;left:50%;width:32px;height:32px;margin:-16px 0 0 -16px;z-index:10;background-image:url(data:image/gif;base64,R0lGODlhIAAgAPMAAJmZmf%2F%2F%2F6%2Bvr8nJybW1tcDAwOjo6Nvb26ioqKOjo7Ozs%2FLy8vz8%2FAAAAAAAAAAAACH%2FC05FVFNDQVBFMi4wAwEAAAAh%2FhpDcmVhdGVkIHdpdGggYWpheGxvYWQuaW5mbwAh%2BQQJCgAAACwAAAAAIAAgAAAE5xDISWlhperN52JLhSSdRgwVo1ICQZRUsiwHpTJT4iowNS8vyW2icCF6k8HMMBkCEDskxTBDAZwuAkkqIfxIQyhBQBFvAQSDITM5VDW6XNE4KagNh6Bgwe60smQUB3d4Rz1ZBApnFASDd0hihh12BkE9kjAJVlycXIg7CQIFA6SlnJ87paqbSKiKoqusnbMdmDC2tXQlkUhziYtyWTxIfy6BE8WJt5YJvpJivxNaGmLHT0VnOgSYf0dZXS7APdpB309RnHOG5gDqXGLDaC457D1zZ%2FV%2FnmOM82XiHRLYKhKP1oZmADdEAAAh%2BQQJCgAAACwAAAAAIAAgAAAE6hDISWlZpOrNp1lGNRSdRpDUolIGw5RUYhhHukqFu8DsrEyqnWThGvAmhVlteBvojpTDDBUEIFwMFBRAmBkSgOrBFZogCASwBDEY%2FCZSg7GSE0gSCjQBMVG023xWBhklAnoEdhQEfyNqMIcKjhRsjEdnezB%2BA4k8gTwJhFuiW4dokXiloUepBAp5qaKpp6%2BHo7aWW54wl7obvEe0kRuoplCGepwSx2jJvqHEmGt6whJpGpfJCHmOoNHKaHx61WiSR92E4lbFoq%2BB6QDtuetcaBPnW6%2BO7wDHpIiK9SaVK5GgV543tzjgGcghAgAh%2BQQJCgAAACwAAAAAIAAgAAAE7hDISSkxpOrN5zFHNWRdhSiVoVLHspRUMoyUakyEe8PTPCATW9A14E0UvuAKMNAZKYUZCiBMuBakSQKG8G2FzUWox2AUtAQFcBKlVQoLgQReZhQlCIJesQXI5B0CBnUMOxMCenoCfTCEWBsJColTMANldx15BGs8B5wlCZ9Po6OJkwmRpnqkqnuSrayqfKmqpLajoiW5HJq7FL1Gr2mMMcKUMIiJgIemy7xZtJsTmsM4xHiKv5KMCXqfyUCJEonXPN2rAOIAmsfB3uPoAK%2B%2BG%2Bw48edZPK%2BM6hLJpQg484enXIdQFSS1u6UhksENEQAAIfkECQoAAAAsAAAAACAAIAAABOcQyEmpGKLqzWcZRVUQnZYg1aBSh2GUVEIQ2aQOE%2BG%2BcD4ntpWkZQj1JIiZIogDFFyHI0UxQwFugMSOFIPJftfVAEoZLBbcLEFhlQiqGp1Vd140AUklUN3eCA51C1EWMzMCezCBBmkxVIVHBWd3HHl9JQOIJSdSnJ0TDKChCwUJjoWMPaGqDKannasMo6WnM562R5YluZRwur0wpgqZE7NKUm%2BFNRPIhjBJxKZteWuIBMN4zRMIVIhffcgojwCF117i4nlLnY5ztRLsnOk%2BaV%2BoJY7V7m76PdkS4trKcdg0Zc0tTcKkRAAAIfkECQoAAAAsAAAAACAAIAAABO4QyEkpKqjqzScpRaVkXZWQEximw1BSCUEIlDohrft6cpKCk5xid5MNJTaAIkekKGQkWyKHkvhKsR7ARmitkAYDYRIbUQRQjWBwJRzChi9CRlBcY1UN4g0%2FVNB0AlcvcAYHRyZPdEQFYV8ccwR5HWxEJ02YmRMLnJ1xCYp0Y5idpQuhopmmC2KgojKasUQDk5BNAwwMOh2RtRq5uQuPZKGIJQIGwAwGf6I0JXMpC8C7kXWDBINFMxS4DKMAWVWAGYsAdNqW5uaRxkSKJOZKaU3tPOBZ4DuK2LATgJhkPJMgTwKCdFjyPHEnKxFCDhEAACH5BAkKAAAALAAAAAAgACAAAATzEMhJaVKp6s2nIkolIJ2WkBShpkVRWqqQrhLSEu9MZJKK9y1ZrqYK9WiClmvoUaF8gIQSNeF1Er4MNFn4SRSDARWroAIETg1iVwuHjYB1kYc1mwruwXKC9gmsJXliGxc%2BXiUCby9ydh1sOSdMkpMTBpaXBzsfhoc5l58Gm5yToAaZhaOUqjkDgCWNHAULCwOLaTmzswadEqggQwgHuQsHIoZCHQMMQgQGubVEcxOPFAcMDAYUA85eWARmfSRQCdcMe0zeP1AAygwLlJtPNAAL19DARdPzBOWSm1brJBi45soRAWQAAkrQIykShQ9wVhHCwCQCACH5BAkKAAAALAAAAAAgACAAAATrEMhJaVKp6s2nIkqFZF2VIBWhUsJaTokqUCoBq%2BE71SRQeyqUToLA7VxF0JDyIQh%2FMVVPMt1ECZlfcjZJ9mIKoaTl1MRIl5o4CUKXOwmyrCInCKqcWtvadL2SYhyASyNDJ0uIiRMDjI0Fd30%2FiI2UA5GSS5UDj2l6NoqgOgN4gksEBgYFf0FDqKgHnyZ9OX8HrgYHdHpcHQULXAS2qKpENRg7eAMLC7kTBaixUYFkKAzWAAnLC7FLVxLWDBLKCwaKTULgEwbLA4hJtOkSBNqITT3xEgfLpBtzE%2FjiuL04RGEBgwWhShRgQExHBAAh%2BQQJCgAAACwAAAAAIAAgAAAE7xDISWlSqerNpyJKhWRdlSAVoVLCWk6JKlAqAavhO9UkUHsqlE6CwO1cRdCQ8iEIfzFVTzLdRAmZX3I2SfZiCqGk5dTESJeaOAlClzsJsqwiJwiqnFrb2nS9kmIcgEsjQydLiIlHehhpejaIjzh9eomSjZR%2BipslWIRLAgMDOR2DOqKogTB9pCUJBagDBXR6XB0EBkIIsaRsGGMMAxoDBgYHTKJiUYEGDAzHC9EACcUGkIgFzgwZ0QsSBcXHiQvOwgDdEwfFs0sDzt4S6BK4xYjkDOzn0unFeBzOBijIm1Dgmg5YFQwsCMjp1oJ8LyIAACH5BAkKAAAALAAAAAAgACAAAATwEMhJaVKp6s2nIkqFZF2VIBWhUsJaTokqUCoBq%2BE71SRQeyqUToLA7VxF0JDyIQh%2FMVVPMt1ECZlfcjZJ9mIKoaTl1MRIl5o4CUKXOwmyrCInCKqcWtvadL2SYhyASyNDJ0uIiUd6GGl6NoiPOH16iZKNlH6KmyWFOggHhEEvAwwMA0N9GBsEC6amhnVcEwavDAazGwIDaH1ipaYLBUTCGgQDA8NdHz0FpqgTBwsLqAbWAAnIA4FWKdMLGdYGEgraigbT0OITBcg5QwPT4xLrROZL6AuQAPUS7bxLpoWidY0JtxLHKhwwMJBTHgPKdEQAACH5BAkKAAAALAAAAAAgACAAAATrEMhJaVKp6s2nIkqFZF2VIBWhUsJaTokqUCoBq%2BE71SRQeyqUToLA7VxF0JDyIQh%2FMVVPMt1ECZlfcjZJ9mIKoaTl1MRIl5o4CUKXOwmyrCInCKqcWtvadL2SYhyASyNDJ0uIiUd6GAULDJCRiXo1CpGXDJOUjY%2BYip9DhToJA4RBLwMLCwVDfRgbBAaqqoZ1XBMHswsHtxtFaH1iqaoGNgAIxRpbFAgfPQSqpbgGBqUD1wBXeCYp1AYZ19JJOYgH1KwA4UBvQwXUBxPqVD9L3sbp2BNk2xvvFPJd%2BMFCN6HAAIKgNggY0KtEBAAh%2BQQJCgAAACwAAAAAIAAgAAAE6BDISWlSqerNpyJKhWRdlSAVoVLCWk6JKlAqAavhO9UkUHsqlE6CwO1cRdCQ8iEIfzFVTzLdRAmZX3I2SfYIDMaAFdTESJeaEDAIMxYFqrOUaNW4E4ObYcCXaiBVEgULe0NJaxxtYksjh2NLkZISgDgJhHthkpU4mW6blRiYmZOlh4JWkDqILwUGBnE6TYEbCgevr0N1gH4At7gHiRpFaLNrrq8HNgAJA70AWxQIH1%2BvsYMDAzZQPC9VCNkDWUhGkuE5PxJNwiUK4UfLzOlD4WvzAHaoG9nxPi5d%2BjYUqfAhhykOFwJWiAAAIfkECQoAAAAsAAAAACAAIAAABPAQyElpUqnqzaciSoVkXVUMFaFSwlpOCcMYlErAavhOMnNLNo8KsZsMZItJEIDIFSkLGQoQTNhIsFehRww2CQLKF0tYGKYSg%2BygsZIuNqJksKgbfgIGepNo2cIUB3V1B3IvNiBYNQaDSTtfhhx0CwVPI0UJe0%2Bbm4g5VgcGoqOcnjmjqDSdnhgEoamcsZuXO1aWQy8KAwOAuTYYGwi7w5h%2BKr0SJ8MFihpNbx%2B4Erq7BYBuzsdiH1jCAzoSfl0rVirNbRXlBBlLX%2BBP0XJLAPGzTkAuAOqb0WT5AH7OcdCm5B8TgRwSRKIHQtaLCwg1RAAAOwAAAAAAAAAAAA%3D%3D);visibility:visible;opacity:.6;transition:all .3s ease}.reveal>.overlay header{position:absolute;left:0;top:0;width:100%;padding:5px;z-index:2;box-sizing:border-box}.reveal>.overlay header a{display:inline-block;width:40px;height:40px;line-height:36px;padding:0 10px;float:right;opacity:.6;box-sizing:border-box}.reveal>.overlay header a:hover{opacity:1}.reveal>.overlay header a .icon{display:inline-block;width:20px;height:20px;background-position:50% 50%;background-size:100%;background-repeat:no-repeat}.reveal>.overlay header a.close .icon{background-image:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAABkklEQVRYR8WX4VHDMAxG6wnoJrABZQPYBCaBTWAD2g1gE5gg6OOsXuxIlr40d81dfrSJ9V4c2VLK7spHuTJ/5wpM07QXuXc5X0opX2tEJcadjHuV80li/FgxTIEK/5QBCICBD6xEhSMGHgQPgBgLiYVAB1dpSqKDawxTohFw4JSEA3clzgIBPCURwE2JucBR7rhPJJv5OpJwDX+SfDjgx1wACQeJG1aChP9K/IMmdZ8DtESV1WyP3Bt4MwM6sj4NMxMYiqUWHQu4KYA/SYkIjOsm3BXYWMKFDwU2khjCQ4ELJUJ4SmClRArOCmSXGuKma0fYD5CbzHxFpCSGAhfAVSSUGDUk2BWZaff2g6GE15BsBQ9nwmpIGDiyHQddwNTMKkbZaf9fajXQca1EX44puJZUsnY0ObGmITE3GVLCbEhQUjGVt146j6oasWN+49Vph2w1pZ5EansNZqKBm1txbU57iRRcZ86RWMDdWtBJUHBHwoQPi1GV+JCbntmvok7iTX4/Up9mgyTc/FJYDTcndgH/AA5A/CHsyEkVAAAAAElFTkSuQmCC)}.reveal>.overlay header a.external .icon{background-image:url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAAcElEQVRYR+2WSQoAIQwEzf8f7XiOMkUQxUPlGkM3hVmiQfQR9GYnH1SsAQlI4DiBqkCMoNb9y2e90IAEJPAcgdznU9+engMaeJ7Azh5Y1U67gAho4DqBqmB1buAf0MB1AlVBek83ZPkmJMGc1wAR+AAqod/B97TRpQAAAABJRU5ErkJggg==)}.reveal>.overlay .viewport{position:absolute;display:flex;top:50px;right:0;bottom:0;left:0}.reveal>.overlay.overlay-preview .viewport iframe{width:100%;height:100%;max-width:100%;max-height:100%;border:0;opacity:0;visibility:hidden;transition:all .3s ease}.reveal>.overlay.overlay-preview.loaded .viewport iframe{opacity:1;visibility:visible}.reveal>.overlay.overlay-preview.loaded .viewport-inner{position:absolute;z-index:-1;left:0;top:45%;width:100%;text-align:center;letter-spacing:normal}.reveal>.overlay.overlay-preview .x-frame-error{opacity:0;transition:opacity .3s ease .3s}.reveal>.overlay.overlay-preview.loaded .x-frame-error{opacity:1}.reveal>.overlay.overlay-preview.loaded .spinner{opacity:0;visibility:hidden;transform:scale(.2)}.reveal>.overlay.overlay-help .viewport{overflow:auto;color:#fff}.reveal>.overlay.overlay-help .viewport .viewport-inner{width:600px;margin:auto;padding:20px 20px 80px 20px;text-align:center;letter-spacing:normal}.reveal>.overlay.overlay-help .viewport .viewport-inner .title{font-size:20px}.reveal>.overlay.overlay-help .viewport .viewport-inner table{border:1px solid #fff;border-collapse:collapse;font-size:16px}.reveal>.overlay.overlay-help .viewport .viewport-inner table td,.reveal>.overlay.overlay-help .viewport .viewport-inner table th{width:200px;padding:14px;border:1px solid #fff;vertical-align:middle}.reveal>.overlay.overlay-help .viewport .viewport-inner table th{padding-top:20px;padding-bottom:20px}.reveal .playback{position:absolute;left:15px;bottom:20px;z-index:30;cursor:pointer;transition:all .4s ease;-webkit-tap-highlight-color:transparent}.reveal.overview .playback{opacity:0;visibility:hidden}.reveal .hljs{min-height:100%}.reveal .hljs table{margin:initial}.reveal .hljs-ln-code,.reveal .hljs-ln-numbers{padding:0;border:0}.reveal .hljs-ln-numbers{opacity:.6;padding-right:.75em;text-align:right;vertical-align:top}.reveal .hljs.has-highlights tr:not(.highlight-line){opacity:.4}.reveal .hljs:not(:first-child).fragment{position:absolute;top:0;left:0;width:100%;box-sizing:border-box}.reveal pre[data-auto-animate-target]{overflow:hidden}.reveal pre[data-auto-animate-target] code{height:100%}.reveal .roll{display:inline-block;line-height:1.2;overflow:hidden;vertical-align:top;perspective:400px;perspective-origin:50% 50%}.reveal .roll:hover{background:0 0;text-shadow:none}.reveal .roll span{display:block;position:relative;padding:0 2px;pointer-events:none;transition:all .4s ease;transform-origin:50% 0;transform-style:preserve-3d;-webkit-backface-visibility:hidden;backface-visibility:hidden}.reveal .roll:hover span{background:rgba(0,0,0,.5);transform:translate3d(0,0,-45px) rotateX(90deg)}.reveal .roll span:after{content:attr(data-title);display:block;position:absolute;left:0;top:0;padding:0 2px;-webkit-backface-visibility:hidden;backface-visibility:hidden;transform-origin:50% 0;transform:translate3d(0,110%,0) rotateX(-90deg)}.reveal aside.notes{display:none}.reveal .speaker-notes{display:none;position:absolute;width:33.33333%;height:100%;top:0;left:100%;padding:14px 18px 14px 18px;z-index:1;font-size:18px;line-height:1.4;border:1px solid rgba(0,0,0,.05);color:#222;background-color:#f5f5f5;overflow:auto;box-sizing:border-box;text-align:left;font-family:Helvetica,sans-serif;-webkit-overflow-scrolling:touch}.reveal .speaker-notes .notes-placeholder{color:#ccc;font-style:italic}.reveal .speaker-notes:focus{outline:0}.reveal .speaker-notes:before{content:'Speaker notes';display:block;margin-bottom:10px;opacity:.5}.reveal.show-notes{max-width:75%;overflow:visible}.reveal.show-notes .speaker-notes{display:block}@media screen and (min-width:1600px){.reveal .speaker-notes{font-size:20px}}@media screen and (max-width:1024px){.reveal.show-notes{border-left:0;max-width:none;max-height:70%;max-height:70vh;overflow:visible}.reveal.show-notes .speaker-notes{top:100%;left:0;width:100%;height:42.85714%;height:30vh;border:0}}@media screen and (max-width:600px){.reveal.show-notes{max-height:60%;max-height:60vh}.reveal.show-notes .speaker-notes{top:100%;height:66.66667%;height:40vh}.reveal .speaker-notes{font-size:14px}}.zoomed .reveal *,.zoomed .reveal :after,.zoomed .reveal :before{-webkit-backface-visibility:visible!important;backface-visibility:visible!important}.zoomed .reveal .controls,.zoomed .reveal .progress{opacity:0}.zoomed .reveal .roll span{background:0 0}.zoomed .reveal .roll span:after{visibility:hidden}html.print-pdf *{-webkit-print-color-adjust:exact}html.print-pdf{width:100%;height:100%;overflow:visible}html.print-pdf body{margin:0 auto!important;border:0;padding:0;float:none!important;overflow:visible}html.print-pdf .nestedarrow,html.print-pdf .reveal .controls,html.print-pdf .reveal .playback,html.print-pdf .reveal .progress,html.print-pdf .reveal.overview,html.print-pdf .state-background{display:none!important}html.print-pdf .reveal pre code{overflow:hidden!important;font-family:Courier,'Courier New',monospace!important}html.print-pdf .reveal{width:auto!important;height:auto!important;overflow:hidden!important}html.print-pdf .reveal .slides{position:static;width:100%!important;height:auto!important;zoom:1!important;pointer-events:initial;left:auto;top:auto;margin:0!important;padding:0!important;overflow:visible;display:block;perspective:none;perspective-origin:50% 50%}html.print-pdf .reveal .slides .pdf-page{position:relative;overflow:hidden;z-index:1;page-break-after:always}html.print-pdf .reveal .slides section{visibility:visible!important;display:block!important;position:absolute!important;margin:0!important;padding:0!important;box-sizing:border-box!important;min-height:1px;opacity:1!important;transform-style:flat!important;transform:none!important}html.print-pdf .reveal section.stack{position:relative!important;margin:0!important;padding:0!important;page-break-after:avoid!important;height:auto!important;min-height:auto!important}html.print-pdf .reveal img{box-shadow:none}html.print-pdf .reveal .backgrounds{display:none}html.print-pdf .reveal .slide-background{display:block!important;position:absolute;top:0;left:0;width:100%;height:100%;z-index:auto!important}html.print-pdf .reveal.show-notes{max-width:none;max-height:none}html.print-pdf .reveal .speaker-notes-pdf{display:block;width:100%;height:auto;max-height:none;top:auto;right:auto;bottom:auto;left:auto;z-index:100}html.print-pdf .reveal .speaker-notes-pdf[data-layout=separate-page]{position:relative;color:inherit;background-color:transparent;padding:20px;page-break-after:always;border:0}html.print-pdf .reveal .slide-number-pdf{display:block;position:absolute;font-size:14px}html.print-pdf .aria-status{display:none}@media print{html:not(.print-pdf){background:#fff;width:auto;height:auto;overflow:visible}html:not(.print-pdf) body{background:#fff;font-size:20pt;width:auto;height:auto;border:0;margin:0 5%;padding:0;overflow:visible;float:none!important}html:not(.print-pdf) .controls,html:not(.print-pdf) .fork-reveal,html:not(.print-pdf) .nestedarrow,html:not(.print-pdf) .reveal .backgrounds,html:not(.print-pdf) .reveal .progress,html:not(.print-pdf) .reveal .slide-number,html:not(.print-pdf) .share-reveal,html:not(.print-pdf) .state-background{display:none!important}html:not(.print-pdf) body,html:not(.print-pdf) li,html:not(.print-pdf) p,html:not(.print-pdf) td{font-size:20pt!important;color:#000}html:not(.print-pdf) h1,html:not(.print-pdf) h2,html:not(.print-pdf) h3,html:not(.print-pdf) h4,html:not(.print-pdf) h5,html:not(.print-pdf) h6{color:#000!important;height:auto;line-height:normal;text-align:left;letter-spacing:normal}html:not(.print-pdf) h1{font-size:28pt!important}html:not(.print-pdf) h2{font-size:24pt!important}html:not(.print-pdf) h3{font-size:22pt!important}html:not(.print-pdf) h4{font-size:22pt!important;font-variant:small-caps}html:not(.print-pdf) h5{font-size:21pt!important}html:not(.print-pdf) h6{font-size:20pt!important;font-style:italic}html:not(.print-pdf) a:link,html:not(.print-pdf) a:visited{color:#000!important;font-weight:700;text-decoration:underline}html:not(.print-pdf) div,html:not(.print-pdf) ol,html:not(.print-pdf) p,html:not(.print-pdf) ul{visibility:visible;position:static;width:auto;height:auto;display:block;overflow:visible;margin:0;text-align:left!important}html:not(.print-pdf) .reveal pre,html:not(.print-pdf) .reveal table{margin-left:0;margin-right:0}html:not(.print-pdf) .reveal pre code{padding:20px}html:not(.print-pdf) .reveal blockquote{margin:20px 0}html:not(.print-pdf) .reveal .slides{position:static!important;width:auto!important;height:auto!important;left:0!important;top:0!important;margin-left:0!important;margin-top:0!important;padding:0!important;zoom:1!important;transform:none!important;overflow:visible!important;display:block!important;text-align:left!important;perspective:none;perspective-origin:50% 50%}html:not(.print-pdf) .reveal .slides section{visibility:visible!important;position:static!important;width:auto!important;height:auto!important;display:block!important;overflow:visible!important;left:0!important;top:0!important;margin-left:0!important;margin-top:0!important;padding:60px 20px!important;z-index:auto!important;opacity:1!important;page-break-after:always!important;transform-style:flat!important;transform:none!important;transition:none!important}html:not(.print-pdf) .reveal .slides section.stack{padding:0!important}html:not(.print-pdf) .reveal section:last-of-type{page-break-after:avoid!important}html:not(.print-pdf) .reveal section .fragment{opacity:1!important;visibility:visible!important;transform:none!important}html:not(.print-pdf) .reveal section img{display:block;margin:15px 0;background:#fff;border:1px solid #666;box-shadow:none}html:not(.print-pdf) .reveal section small{font-size:.8em}html:not(.print-pdf) .reveal .hljs{max-height:100%;white-space:pre-wrap;word-wrap:break-word;word-break:break-word;font-size:15pt}html:not(.print-pdf) .reveal .hljs .hljs-ln-numbers{white-space:nowrap}html:not(.print-pdf) .reveal .hljs td{font-size:inherit!important;color:inherit!important}}/**
 * A simple theme for reveal.js presentations, similar
 * to the default theme. The accent color is darkblue.
 *
 * This theme is Copyright (C) 2012 Owen Versteeg, https://github.com/StereotypicalApps. It is MIT licensed.
 * reveal.js is Copyright (C) 2011-2012 Hakim El Hattab, http://hakim.se
 */
@import url(https://fonts.googleapis.com/css?family=News+Cycle:400,700);
@import url(https://fonts.googleapis.com/css?family=Lato:400,700,400italic,700italic);
section.has-dark-background, section.has-dark-background h1, section.has-dark-background h2, section.has-dark-background h3, section.has-dark-background h4, section.has-dark-background h5, section.has-dark-background h6 {
  color: #fff; }

/*********************************************
 * GLOBAL STYLES
 *********************************************/
:root {
  --background-color: #fff;
  --main-font: Lato, sans-serif;
  --main-font-size: 40px;
  --main-color: #000;
  --block-margin: 20px;
  --heading-margin: 0 0 20px 0;
  --heading-font: News Cycle, Impact, sans-serif;
  --heading-color: #000;
  --heading-line-height: 1.2;
  --heading-letter-spacing: normal;
  --heading-text-transform: none;
  --heading-text-shadow: none;
  --heading-font-weight: normal;
  --heading1-text-shadow: none;
  --heading1-size: 3.77em;
  --heading2-size: 2.11em;
  --heading3-size: 1.55em;
  --heading4-size: 1em;
  --code-font: monospace;
  --link-color: #00008B;
  --link-color-hover: #0000f1;
  --selection-background-color: rgba(0, 0, 0, 0.99);
  --selection-color: #fff; }

.reveal-viewport {
  background: #fff;
  background-color: #fff; }

.reveal {
  font-family: "Lato", sans-serif;
  font-size: 40px;
  font-weight: normal;
  color: #000; }

.reveal ::selection {
  color: #fff;
  background: rgba(0, 0, 0, 0.99);
  text-shadow: none; }

.reveal ::-moz-selection {
  color: #fff;
  background: rgba(0, 0, 0, 0.99);
  text-shadow: none; }

.reveal .slides section,
.reveal .slides section > section {
  line-height: 1.3;
  font-weight: inherit; }

/*********************************************
 * HEADERS
 *********************************************/
.reveal h1,
.reveal h2,
.reveal h3,
.reveal h4,
.reveal h5,
.reveal h6 {
  margin: 0 0 20px 0;
  color: #000;
  font-family: "News Cycle", Impact, sans-serif;
  font-weight: normal;
  line-height: 1.2;
  letter-spacing: normal;
  text-transform: none;
  text-shadow: none;
  word-wrap: break-word; }

.reveal h1 {
  font-size: 3.77em; }

.reveal h2 {
  font-size: 2.11em; }

.reveal h3 {
  font-size: 1.55em; }

.reveal h4 {
  font-size: 1em; }

.reveal h1 {
  text-shadow: none; }

/*********************************************
 * OTHER
 *********************************************/
.reveal p {
  margin: 20px 0;
  line-height: 1.3; }

/* Ensure certain elements are never larger than the slide itself */
.reveal img,
.reveal video,
.reveal iframe {
  max-width: 95%;
  max-height: 95%; }

.reveal strong,
.reveal b {
  font-weight: bold; }

.reveal em {
  font-style: italic; }

.reveal ol,
.reveal dl,
.reveal ul {
  display: inline-block;
  text-align: left;
  margin: 0 0 0 1em; }

.reveal ol {
  list-style-type: decimal; }

.reveal ul {
  list-style-type: disc; }

.reveal ul ul {
  list-style-type: square; }

.reveal ul ul ul {
  list-style-type: circle; }

.reveal ul ul,
.reveal ul ol,
.reveal ol ol,
.reveal ol ul {
  display: block;
  margin-left: 40px; }

.reveal dt {
  font-weight: bold; }

.reveal dd {
  margin-left: 40px; }

.reveal blockquote {
  display: block;
  position: relative;
  width: 70%;
  margin: 20px auto;
  padding: 5px;
  font-style: italic;
  background: rgba(255, 255, 255, 0.05);
  box-shadow: 0px 0px 2px rgba(0, 0, 0, 0.2); }

.reveal blockquote p:first-child,
.reveal blockquote p:last-child {
  display: inline-block; }

.reveal q {
  font-style: italic; }

.reveal pre {
  display: block;
  position: relative;
  width: 90%;
  margin: 20px auto;
  text-align: left;
  font-size: 0.55em;
  font-family: monospace;
  line-height: 1.2em;
  word-wrap: break-word;
  box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.15); }

.reveal code {
  font-family: monospace;
  text-transform: none; }

.reveal pre code {
  display: block;
  padding: 5px;
  overflow: auto;
  max-height: 400px;
  word-wrap: normal; }

.reveal table {
  margin: auto;
  border-collapse: collapse;
  border-spacing: 0; }

.reveal table th {
  font-weight: bold; }

.reveal table th,
.reveal table td {
  text-align: left;
  padding: 0.2em 0.5em 0.2em 0.5em;
  border-bottom: 1px solid; }

.reveal table th[align="center"],
.reveal table td[align="center"] {
  text-align: center; }

.reveal table th[align="right"],
.reveal table td[align="right"] {
  text-align: right; }

.reveal table tbody tr:last-child th,
.reveal table tbody tr:last-child td {
  border-bottom: none; }

.reveal sup {
  vertical-align: super;
  font-size: smaller; }

.reveal sub {
  vertical-align: sub;
  font-size: smaller; }

.reveal small {
  display: inline-block;
  font-size: 0.6em;
  line-height: 1.2em;
  vertical-align: top; }

.reveal small * {
  vertical-align: top; }

.reveal img {
  margin: 20px 0; }

/*********************************************
 * LINKS
 *********************************************/
.reveal a {
  color: #00008B;
  text-decoration: none;
  transition: color .15s ease; }

.reveal a:hover {
  color: #0000f1;
  text-shadow: none;
  border: none; }

.reveal .roll span:after {
  color: #fff;
  background: #00003f; }

/*********************************************
 * Frame helper
 *********************************************/
.reveal .r-frame {
  border: 4px solid #000;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.15); }

.reveal a .r-frame {
  transition: all .15s linear; }

.reveal a:hover .r-frame {
  border-color: #00008B;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.55); }

/*********************************************
 * NAVIGATION CONTROLS
 *********************************************/
.reveal .controls {
  color: #00008B; }

/*********************************************
 * PROGRESS BAR
 *********************************************/
.reveal .progress {
  background: rgba(0, 0, 0, 0.2);
  color: #00008B; }

/*********************************************
 * PRINT BACKGROUND
 *********************************************/
@media print {
  .backgrounds {
    background-color: #fff; } }
pre table { border: none; }
/*!
  Theme: Default
  Description: Original highlight.js style
  Author: (c) Ivan Sagalaev <maniac@softwaremaniacs.org>
  Maintainer: @highlightjs/core-team
  Website: https://highlightjs.org/
  License: see project LICENSE
  Touched: 2021
*/pre code.hljs{display:block;overflow-x:auto;padding:1em}code.hljs{padding:3px 5px}.hljs{background:#f3f3f3;color:#444}.hljs-comment{color:#697070}.hljs-punctuation,.hljs-tag{color:#444a}.hljs-tag .hljs-attr,.hljs-tag .hljs-name{color:#444}.hljs-attribute,.hljs-doctag,.hljs-keyword,.hljs-meta .hljs-keyword,.hljs-name,.hljs-selector-tag{font-weight:700}.hljs-deletion,.hljs-number,.hljs-quote,.hljs-selector-class,.hljs-selector-id,.hljs-string,.hljs-template-tag,.hljs-type{color:#800}.hljs-section,.hljs-title{color:#800;font-weight:700}.hljs-link,.hljs-operator,.hljs-regexp,.hljs-selector-attr,.hljs-selector-pseudo,.hljs-symbol,.hljs-template-variable,.hljs-variable{color:#ab5656}.hljs-literal{color:#695}.hljs-addition,.hljs-built_in,.hljs-bullet,.hljs-code{color:#397300}.hljs-meta{color:#1f7199}.hljs-meta .hljs-string{color:#38a}.hljs-emphasis{font-style:italic}.hljs-strong{font-weight:700}pre.hljs {
  padding: 0;
}pre code.hljs {
  padding: 0.5em;
}.hljs {
  background: transparent;
  color: rgba(0, 0, 0, 0.87);
  -webkit-text-size-adjust:none;
}.hljs-comment,
.hljs-quote {
  color: #93a1a1;
}/* Solarized Green */
.hljs-keyword,
.hljs-selector-tag,
.hljs-addition {
  color: #859900;
}/* Solarized Cyan */
.hljs-number,
.hljs-string,
.hljs-meta .hljs-string,
.hljs-literal,
.hljs-doctag,
.hljs-regexp {
  color: #2aa198;
}/* Solarized Blue */
.hljs-title,
.hljs-section,
.hljs-name,
.hljs-selector-id,
.hljs-selector-class {
  color: #268bd2;
}/* Solarized Yellow */
.hljs-attribute,
.hljs-attr,
.hljs-variable,
.hljs-template-variable,
.hljs-class .hljs-title,
.hljs-type {
  color: #b58900;
}/* Solarized Orange */
.hljs-symbol,
.hljs-bullet,
.hljs-subst,
.hljs-meta,
.hljs-meta .hljs-keyword,
.hljs-selector-attr,
.hljs-selector-pseudo,
.hljs-link {
  color: #cb4b16;
}/* Solarized Red */
.hljs-built_in,
.hljs-deletion {
  color: #dc322f;
}.hljs-formula {
  background: #eee8d5;
}.hljs-emphasis {
  font-style: italic;
}.hljs-strong {
  font-weight: bold;
}
.tc-drop-down .tc-qrcode-drop-down img {
	width: 100%;
	height: 100%;
}

</style>
</head>
<body class="tc-body">

<section class="tc-story-river tc-static-story-river">
<a name="TiddlyWiki Practice">
<div class="tc-tiddler-frame tc-tiddler-view-frame tc-tiddler-exists  tc-tagged-TiddlyWiki%20Talk%20Script" data-tags="[[TiddlyWiki Talk Script]]" data-tiddler-title="TiddlyWiki Practice Revised" role="article"><div class="tc-tiddler-title"><div class="tc-titlebar"><span class="tc-tiddler-controls"><button aria-expanded="false" aria-label="more" class="tc-btn-invisible tc-btn-%24%3A%2Fcore%2Fui%2FButtons%2Fmore-tiddler-actions" title="More actions"></button><div class=" tc-reveal" hidden="true"></div><span class=" tc-reveal"><button aria-label="fold tiddler" class="tc-btn-invisible tc-btn-%24%3A%2Fcore%2Fui%2FButtons%2Ffold" title="Fold the body of this tiddler"></button></span><span class=" tc-reveal" hidden="true"></span><button aria-label="edit" class="tc-btn-invisible tc-btn-%24%3A%2Fcore%2Fui%2FButtons%2Fedit" title="Edit this tiddler"></button><button aria-label="close" class="tc-btn-invisible tc-btn-%24%3A%2Fcore%2Fui%2FButtons%2Fclose" title="Close this tiddler"></button></span><span><h2 class="tc-title">TiddlyWiki Practice Revised</h2></span></div><div class="tc-tiddler-info tc-popup-handle tc-reveal" hidden="true"></div></div><div class=" tc-reveal"><div class=" tc-reveal"><button aria-label="fold tiddler" class="tc-fold-banner" title="Fold the body of this tiddler"><svg class="tc-image-chevron-up tc-image-button" height="22pt" viewBox="0 0 128 128" width="22pt"><g fill-rule="evenodd"><path d="M63.947 44.544c2.027 0 4.054.77 5.6 2.316l55.98 55.98a7.92 7.92 0 010 11.196c-3.086 3.085-8.105 3.092-11.196 0L63.95 63.656l-50.382 50.382a7.92 7.92 0 01-11.195 0c-3.085-3.086-3.092-8.105 0-11.196l55.98-55.98a7.892 7.892 0 015.595-2.317z"></path><path d="M63.947 5.931c2.027 0 4.054.77 5.6 2.316l55.98 55.98a7.92 7.92 0 010 11.196c-3.086 3.085-8.105 3.092-11.196 0L63.95 25.041 13.567 75.423a7.92 7.92 0 01-11.195 0c-3.085-3.086-3.092-8.104 0-11.196l55.98-55.98a7.892 7.892 0 015.595-2.316z"></path></g></svg></button></div><div class=" tc-reveal" hidden="true"></div></div><div class=" tc-reveal"><div class="tc-subtitle"><a class="tc-tiddlylink tc-tiddlylink-missing" href="#"></a> March 30, 2023 at 11:57 pm</div></div><div class=" tc-reveal"><div class="tc-tags-wrapper"><span class="tc-tag-list-item" data-tag-title="TiddlyWiki Talk Script"><span aria-expanded="false" class="tc-tag-label tc-btn-invisible" draggable="true" style="background-color:;
fill:rgba(0, 0, 0, 0.87);
color:rgba(0, 0, 0, 0.87);">TiddlyWiki Talk Script</span><span class="tc-drop-down tc-reveal" hidden="true"></span></span></div></div><div class="tc-tiddler-body tc-reveal"><p>The practical part is structured in a "make it work, make it right, make it beautiful" progression. First we get the bare essentials, then we automate the repetitive tasks, and finally add a cherry or two on top.</p><h1 class="">Make it Work</h1><h2 class="">Download the Template</h2><p>We start off with downloading a blank template from the TiddlyWiki home page.</p><ul><li>Open <a class="tc-tiddlylink-external" href="https://tiddlywiki.com/" rel="noopener noreferrer" target="_blank">TiddlyWiki</a>.</li><li>Scroll and find the big green "Download" button.</li></ul><h2 class="">Install the File Saver</h2><ul><li>Open the downloaded <code>empty.html</code> in your browser.</li></ul><p>Before we start adding content, let's install a plugin that automatically saves changes to the disk.</p><ul><li>Open <a class="tc-tiddlylink-external" href="https://slaymaker1907.github.io/tiddlywiki/plugin-library.html" rel="noopener noreferrer" target="_blank">File Saver</a> in a separate tab.</li><li>Click <code>close</code> on the welcoming screen.</li><li>Drag-and-drop the plugin box to the tab with <code>empty.html</code>. </li><li>Click <code>import</code>.</li><li>Click the red target icon.</li><li>Close all tabs.</li><li>Rename the downloaded file to <code>my_notes.html</code>.</li><li>Open <code>my_notes.html</code> in the browser.</li><li>Click <code>Save</code> and choose <code>my_notes.html</code> confirming the "File already exists. Do you want to replace it?" dialog.</li></ul><p>Great, now any changes that we do to the wiki will be saved on your computer.</p><h2 class="">Create the first Tiddler</h2><p>For our first record we will create a journal entry for yesterday.</p><ul><li>Close <code>GettingStarted</code> tiddler with the cross icon.</li><li>Press on <code>+</code> icon in the sidebar.</li><li>Change the title to yesterday's date, e.g. <code>2023-03-29</code>.</li><li>Add text <code>09:00 I met Alice and she is helping me to setup System X.</code></li><li>Click checkmark to save the tiddler.</li></ul><h2 class="">Apply Formatting</h2><p>All the regular formatting shenanigans work. TiddlyWiki uses WikiText markup to format the text. Start with buttons and soon you will learn the symbols used for the markup.</p><ul><li>Click edit button and use the editor buttons to apply format:<ul><li>Select <code>09:00</code> and click Bold.</li><li>Select <code>helping</code> and click italics.</li></ul></li><li>Click the eye icon to see the preview.</li><li>Hide the sidebar by clicking the double right chevron button.</li><li>add the following bullet list.</li></ul><pre><code>09:30 Daily Standup

* Alice
** Reviewing ABC-123.
* Bob
** Testing System Y.</code></pre><ul><li>Click save.</li></ul><h2 class="">Create Links</h2><p>What makes any wiki useful is the ability to link its content. Let's see how to link tiddlers with one another.</p><ul><li>Press <code>+</code> to create a second tiddler.</li><li>Name it <code>System X</code>.</li></ul><p>A picture is worth a thousand words</p><ul><li>download <code>Image</code> in the channel bookmarks to your computer and drag-and-drop the file into the open Tiddler editor.</li><li>Click <code>Import</code>.</li><li>To adjust the image change change <code>[img[dumpster_fire.png]]</code> to <code>[img width=64 [dumpster_fire.png]]</code></li><li>Open the first journal tiddler and change <code>SystemX</code> to <code>[[System X]]</code>.</li><li>Click on <code>System X</code> link, you will be taken to that tiddler in the story river. </li><li>Close the <code>System X</code> tiddler and you will see that it gets reopened when you click the link.</li><li>(By default the tiddler open at the bottom of the story river, we can change this behavior in the settings to changed to<ul><li>At the top of the story river</li><li>Above the linking tiddler</li><li>Below the linking tiddler)</li></ul></li></ul><p>Now let's see what happens if we create a link to non-existing tiddler.</p><ul><li>Change <code>System Y</code> to <code>[[System Y]]</code>.</li></ul><p>In the preview it appears in <em>italics</em> to show that the page does not exist yet. I found it a good idea to create links to missing tiddlers if I think that a concept is important but not enough to get a full blown tiddler.</p><ul><li>Open the sidebar -&gt; <code>More</code> -&gt; <code>Missing</code>.</li><li>Click on <code>System Y</code>, it shows all the tiddlers mentioning it.</li></ul><p>I made it a weekly routine to go over missing tiddlers and see if any of them needs to be created.</p><p>Finally, let's see how to link to an external resource.</p><ul><li>Open the first tiddler.</li><li>Replace <code>ABC-123</code> with <code>[[ABC-123|jira.corp.net/jira/browse/ABC-123]]</code></li></ul><h2 class="">Tag the Tiddlers</h2><p>When adding more tiddlers you will see that some of them will be related to each other and this is where tagging becomes helpful.</p><p>Let's create a few more tiddlers.</p><ul><li>Change <code>Alice</code> to <code>[[Alice|Alice Bishop]]</code>.</li><li>Change <code>Bob</code> to <code>[[Bob|Bob Dobbs]]</code>.</li><li>Create empty tiddlers for <code>Alice Bishop</code>, <code>Bob Dobbs</code>, and <code>System Y</code> by clicking on the links and populating the tiddlers.</li></ul><p>Now the story river becomes a little crowded. Sidebar to the rescue.</p><ul><li>Open sidebar -&gt; <code>Open</code> tab.</li><li>Rearrange the order of tiddlers with drag and drop.</li><li>Show how to close tiddlers.</li></ul><p>If the river still feels crowded, you can fold some of the tiddlers to show only the title.</p><ul><li>Click on the <code>more actions</code> button on the journal tiddler and choose <code>fold tiddler</code>.</li></ul><p>Now with all the tiddlers in on column we see that there are 3 categories emerging:</p><ul><li>Journal</li><li>People</li><li>Systems</li></ul><p>Let's group the tiddlers into these categories.</p><ul><li>Open <code>System X</code></li><li>Write <code>System</code> in tags field.</li><li>Repeat for <code>System Y</code>.</li><li>Add label <code>Person</code> to <code>Alice Bishop</code> and <code>Bob Dobbs</code>.</li><li>And <code>Journal</code> to the first tiddler.</li></ul><p>The tags create a shortcut to all other tiddlers with the same tag.</p><p>Now we are done with the bare essentials and can start automating repetitive parts.</p><h1 class="">Make it Right</h1><h2 class="">Create a Shortcut for Journal Tiddlers</h2><p>If you are serious about keeping daily notes, then there will be a journal tiddler for every day at work. Although it is not difficult to create tiddlers with the current date and tagged with <code>Journal</code>, there is a shortcut for this.</p><ul><li>Open sidebar -&gt; <code>Tools</code></li><li>Check <code>new journal</code>, observe a new button appearing on the sidebar.</li><li>Click it.</li></ul><p>The created journal tiddler has the right tag, however the format is <code>30th March 2023</code>. It looks nice, but a bit impractical if you need to link to Journal tiddlers or sort them alphabetically, so let's change the journal title format to ISO-8601 as we did in the very first tiddler.</p><ul><li>delete the draft of <code>30th March 2023</code>.</li><li>Open control panel by clicking on the cog icon on the sidebar.</li><li>Change the value of <code>Title of new journal tiddlers</code> from <code>DDth MMM YYYY</code> to <code>YYYY-0MM-0DD</code>, zeroes are needed to add leading zeroes.</li><li>Close the <code>Control Panel</code> tiddler.</li><li>Click the <code>create new journal tiddler</code> button again.  Much better!</li></ul><h2 class="">Create a Snippet for Daily Standups</h2><p>Standups repeat every day, so it makes sense to automate adding notes on them with a template or as it's called in TiddlyWiki, a snippet.</p><ul><li>Close all tiddlers and open the two journal tiddlers.</li><li>Click on the stamp icon and select <code>Add your own</code>. </li><li>Call the new tiddler "StandupSnippet", the title does not matter, as it will be referred by a caption, observe the system tag, TiddlyWIki uses internally to find snippets.</li><li>Paste the tiddler text.</li></ul><pre><code>09:30 Daily Standup

* [[Alice|Alice Bishop]]
* [[Bob|Bob Dobbs]]</code></pre><ul><li>add caption <code>09:30 Daily Standup</code></li><li>Close the StandupSnippet tiddler.</li><li>Open the newest Journal and add the snippet.</li></ul><h2 class="">Create a Macro for Jira Tickets</h2><p>One more frequent thing that we should automate is adding Jira links, so instead of typing <code> [[ABC-123|https://jira.corp.net/ABC-123]]</code> we can type <code>&lt;&lt;jira ABC-123&gt;&gt;</code> and get the same result.</p><ul><li>add <code>** Merged &lt;&lt;jira ABC-123&gt;&gt;.</code> to today's journal tiddler for Alice.</li><li>Create a new tiddler called <code>JiraMacro</code>.</li><li>Add <code>$:/tags/Macro</code> system tag.</li><li>Use the snippets button to insert <code>Macro definition</code></li><li>Change</li></ul><pre><code>\define macroName(param1:"default value",param2)
Text of the macro
\end</code></pre><p>to</p><pre><code>\define jira(id)
[[$id$|https://jira.corp.net/$id$]]
\end</code></pre><ul><li>Save <code>JiraMacro</code> tiddler, observe that the journal tiddler shows the correct link.</li></ul><h2 class="">Backups</h2><p>The final point in the "Make it Right" part is backups. Please do them regularly. Since the whole wiki is just a single file choose a way that works for you. I keep my backups as a private snippet on Stash, but any other solution will work as well.</p><h1 class="">Make it Beautiful</h1><p>Ok, for the final part of the practice we will add a couple of bells and whistles to our TiddlyWiki.</p><h2 class="">Add Visual Tweaks</h2><p>Now that we don't have to worry about losing our data, we can go nuts on customizing the wiki.</p><ul><li>Open <code>ControlPannel</code> (cog icon)</li></ul><h3 class="">Info</h3><ul><li>Navigate to <code>Info</code></li><li>Change the <code>Title of this TiddlyWiki</code> and <code>Subtitle</code>, observe changes in the sidebar.</li><li>Change the animation duration from default <code>400</code> to <code>200</code> milliseconds for a snappier feel.</li><li>Change <code>Default tiddlers</code> to "retain story ordering", to see the same tiddlers when you re-open the wiki.</li></ul><p>If you feel curious, after the tutorial, you can explore the <code>Advanced</code> tab, it has some nerdy diagnostic information.</p><h3 class="">Appearance</h3><ul><li>Navigate to <code>Appearance</code>.</li><li>Navigate to <code>Palette</code></li><li>Choose a theme that suites your mood.</li></ul><p>Later you can press <code>show editor</code> button at the bottom and create the official "kitsch pink" theme if that's what you like.</p><h3 class="">Toolbars</h3><ul><li>Navigate to <code>Toolbars</code></li></ul><h4 class="">Page Toolbars</h4><ul><li>Navigate to <code>Page Toolbars</code></li><li>Uncheck <code>save changes</code> with the plugin we installed saving happens automatically and is indicated with a small hover.</li><li>add <code>more</code> button to have access to less used buttons.</li></ul><p>There are a few other useful buttons:</p><ul><li>Check <code>palette</code> if you are feeling trendy and want the notes to match your day's outfit.</li><li>If you are a tinfoil-cap paranoid type select the <code>encrypt</code> button, but be aware that password-protecting your wiki will make it useless if you forget the password.</li><li><code>full screen</code> is for the mythical focus-mode we all desire.</li><li><code>print</code> is a great button if you need to quickly make a PDF or a paper version of the currently open tiddlers.</li></ul><p>Observe that icons can be rearranged by dragging.</p><h4 class="">View Toolbars</h4><p>Finally, let's customize View Toolbars. I think it's alright by default, just check <code>fold tiddler</code> button, so that you can leave only the title while focusing on other open tiddlers.</p><ul><li>Navigate to <code>View Toolbars</code></li><li>Select <code>Fold Bar</code> to quickly fold/unfold tiddlers.</li></ul><h4 class="">Theme Tweaks</h4><ul><li>Navigate to <code>Theme Tweaks</code></li><li>In <code>Options</code> change <code>Sidebar layout</code> to <code>Fluid story, fixed sidebar</code> to get move screen space to the story river.</li><li>Enable sticky titles, they are nice.</li></ul><blockquote><div>"One designer played with the fonts and lost."</div></blockquote><p>so let's not touch those, the defaults are a-ok.</p><ul><li>Navigate to <code>Settings</code> tab</li><li>Uncheck <code>Enable automatic CamelCase linking</code> otherwise TiddlyWiki will consider any CamelCased word as a link to new Tiddler.</li><li>Close <code>ControlPannel</code> tiddler.</li></ul><p>Phew. That concludes the tweaking part.</p><h2 class="">Sharing Your Work</h2><p>At some point you may want to share the notes with other people and there are several options for that.</p><h3 class="">Sharing a single tiddler:</h3><ul><li>Open some tiddler.</li><li>Click on <code>more menu</code> on a tiddler, choose <code>Export tiddler</code> -&gt; <code>Static HTML</code>, examine the downloaded file.</li><li>Can also be exported as <code>.tid</code> file and imported by drag-and-drop into another TiddlyWiki.</li></ul><h3 class="">Sharing the whole TiddlyWiki</h3><ul><li>Open <code>more</code> menu in the sidebar.</li><li>Click on <code>export all</code>, you will see the same choices, but for the whole wiki.</li></ul><h3 class="">As a printed PDF using Print button.</h3><p>A quick and easy way to share a subset of tiddlers is to unfold them, hide the sidebar and click on the printer icon and print to a PDF.</p><h2 class="">Enhance Tags</h2><ul><li>Navigate to Sidebar -&gt; <code>More</code> -&gt; <code>Tags</code>.</li><li>Open tag manager system tiddler, add an appropriate icon and a fancy color.</li><li>Show that the tag appears, click on it to see all tag-mates and a tiddler, representing tag, * Write info about <code>System</code>, some common info.</li></ul><pre><code>Common information about systems at Corp.

* [[The global repository for system accesses|https://corp.net/systems]]
* [[Rules for creating a new system|https://corp.net/new_system]]</code></pre><ul><li>Use "List of tiddlers by tag" to enrich the <code>Journal</code> tiddler. </li></ul><h2 class="">Plugins</h2><p>How many of you use</p><ul><li>Browser plugins?</li><li>Jenkins plugins?</li><li>Vim plugins?</li><li>Winamp plugins? Anyone? Ah well!</li></ul><p>Then you know the first rule of plugins. Don't overdo it! Understand the limitations of vanilla before installing a bunch. It is very easy to install, it's just drag-and-dropping the plugin into an open tab.</p><p>Here is the top list of plugins that I use:</p><ol><li>Filesystem saver (already installed)</li><li><a class="tc-tiddlylink-external" href="https://kookma.github.io/TW-Todolist/" rel="noopener noreferrer" target="_blank">TODO plugin</a><ul><li><code>&lt;&lt;todolist-ui caption:"!!" base:"Simple" width:60%&gt;&gt;</code></li><li>Keep TODO widget-page alway open, unloads your focus, production line with occasional gremlins analogy.</li></ul></li><li><a class="tc-tiddlylink-external" href="https://tiddlywiki.com/plugins/tiddlywiki/highlight/" rel="noopener noreferrer" target="_blank">Highlight.js</a><ul><li>invaluable for storing pieces of code.</li></ul></li><li><a class="tc-tiddlylink-external" href="https://efurlanm.github.io/mermaid-tw5#%24%3A%2Fplugins%2Forange%2Fmermaid-tw5" rel="noopener noreferrer" target="_blank">Mermaid</a><ul><li>Great for generating diagrams</li><li>Btw, everyone's darling, ChatGPT, is amazingly good at generating the mermaid diagrams given enough context.</li></ul></li><li><a class="tc-tiddlylink-external" href="https://sukima.github.io/tiddlywiki-reveal-js/#%24%3A%2Fplugins%2Fsukima%2Freveal-js:%24%3A%2Fplugins%2Fsukima%2Freveal-js%20Introduction%20Install%20Documentation%20License" rel="noopener noreferrer" target="_blank">Reveal-js</a><ul><li>I made the slides in it.</li></ul></li><li><a class="tc-tiddlylink-external" href="https://tiddlywiki.com/editions/full/#%24%3A%2Fplugins%2Ftiddlywiki%2Fqrcode" rel="noopener noreferrer" target="_blank">QR Code</a></li></ol><p>There are also plugins that I haven't installed but see they could be fun:</p><ul><li><a class="tc-tiddlylink-external" href="http://tiddlymap.org/" rel="noopener noreferrer" target="_blank">TiddlyMap</a> if you feel like searching for Pepe Silva</li><li><a class="tc-tiddlylink-external" href="https://giffmex.org/stroll/stroll.html" rel="noopener noreferrer" target="_blank">Stroll</a> for two-column view</li><li><a class="tc-tiddlylink-external" href="https://tiddlywiki.com/editions/full/#%24%3A%2Fplugins%2Ftiddlywiki%2Fkatex" rel="noopener noreferrer" target="_blank">KaTeX</a> plugin if you write in LaTeX</li><li><a class="tc-tiddlylink-external" href="https://tiddlywiki.com/editions/full/#%24%3A%2Fplugins%2Ftiddlywiki%2Fmarkdown" rel="noopener noreferrer" target="_blank">markdown</a> to allow writing tiddlers in Markdown.</li></ul><h2 class="">Add Custom favicon</h2><p>This wiki, your wiki, is almost perfect. Now let's add a final touch and add a favicon, so that you can easily find it among other open browser tabs.</p><ul><li>Navigate to <a class="tc-tiddlylink-external" href="http://www.faviconer.com/" rel="noopener noreferrer" target="_blank">http://www.faviconer.com/</a></li><li>Draw a cool 32-pixel icon, give it a name and description and download.</li><li>Drag-and-drop to import into wiki</li><li>rename the tiddler to <code>$:/favicon.ico</code>.</li><li>Now if you pin it it will be easy to find.</li></ul><p>Setting a favicon is an equivalent of naming a pet, so this TiddlyWiki is with you to stay.
</p></div>
</div>
</a>
</section>
</body>
</html>
