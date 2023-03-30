# TiddlyWiki_tutorial
The companion repo for my TiddlyWiki tutorial. The commit history shows the progress from blank TiddlyWiki template to the final version.

# TiddlyWiki Practice Revised

The practical part is structured in a "make it work, make it right, make it beautiful" progression. First we get the bare essentials, then we automate the repetitive tasks, and finally add a cherry or two on top.

# Make it Work

## Download the Template

We start off with downloading a blank template from the TiddlyWiki home page.

* Open [TiddlyWiki](https://tiddlywiki.com/).
* Scroll and find the big green "Download" button.

## Install the File Saver

* Open the downloaded `empty.html` in your browser.

Before we start adding content, let's install a plugin that automatically saves changes to the disk.

* Open [File Saver](https://slaymaker1907.github.io/tiddlywiki/plugin-library.html) in a separate tab.
* Click `close` on the welcoming screen.
* Drag-and-drop the plugin box to the tab with `empty.html`.
* Click `import`.
* Click the red target icon.
* Close all tabs.
* Rename the downloaded file to `my_notes.html`.
* Open `my_notes.html` in the browser.
* Click `Save` and choose `my_notes.html` confirming the "File already exists. Do you want to replace it?" dialog.

Great, now any changes that we do to the wiki will be saved on your computer.

## Create the first Tiddler

For our first record we will create a journal entry for yesterday.

* Close `GettingStarted` tiddler with the cross icon.
* Press on `+` icon in the sidebar.
* Change the title to yesterday's date, e.g. `2023-03-29`.
* Add text `09:00 I met Alice and she is helping me to setup System X.`
* Click checkmark to save the tiddler.

## Apply Formatting

All the regular formatting shenanigans work. TiddlyWiki uses WikiText markup to format the text. Start with buttons and soon you will learn the symbols used for the markup.

* Click edit button and use the editor buttons to apply format:
    * Select `09:00` and click Bold.
    * Select `helping` and click italics.
* Click the eye icon to see the preview.
* Hide the sidebar by clicking the double right chevron button.
* add the following bullet list.

```
09:30 Daily Standup

* Alice
** Reviewing ABC-123.
* Bob
** Testing System Y.
```

* Click save.

## Create Links

What makes any wiki useful is the ability to link its content. Let's see how to link tiddlers with one another.

* Press `+` to create a second tiddler.
* Name it `System X`.

A picture is worth a thousand words

* download `Image` in the channel bookmarks to your computer and drag-and-drop the file into the open Tiddler editor.
* Click `Import`.
* To adjust the image change change `[img[dumpster_fire.png]]` to `[img width=64 [dumpster_fire.png]]`
* Open the first journal tiddler and change `SystemX` to `[[System X]]`.
* Click on `System X` link, you will be taken to that tiddler in the story river.
* Close the `System X` tiddler and you will see that it gets reopened when you click the link.
* (By default the tiddler open at the bottom of the story river, we can change this behavior in the settings to changed to
    * At the top of the story river
    * Above the linking tiddler
    * Below the linking tiddler)

Now let's see what happens if we create a link to non-existing tiddler.

* Change `System Y` to `[[System Y]]`.

In the preview it appears in *italics* to show that the page does not exist yet. I found it a good idea to create links to missing tiddlers if I think that a concept is important but not enough to get a full blown tiddler.

* Open the sidebar -> `More` -> `Missing`.
* Click on `System Y`, it shows all the tiddlers mentioning it.

I made it a weekly routine to go over missing tiddlers and see if any of them needs to be created.

Finally, let's see how to link to an external resource.

* Open the first tiddler.
* Replace `ABC-123` with `[[ABC-123|jira.corp.net/jira/browse/ABC-123]]`

## Tag the Tiddlers

When adding more tiddlers you will see that some of them will be related to each other and this is where tagging becomes helpful.

Let's create a few more tiddlers.

* Change `Alice` to `[[Alice|Alice Bishop]]`.
* Change `Bob` to `[[Bob|Bob Dobbs]]`.
* Create empty tiddlers for `Alice Bishop`, `Bob Dobbs`, and `System Y` by clicking on the links and populating the tiddlers.

Now the story river becomes a little crowded. Sidebar to the rescue.

* Open sidebar -> `Open` tab.
* Rearrange the order of tiddlers with drag and drop.
* Show how to close tiddlers.

If the river still feels crowded, you can fold some of the tiddlers to show only the title.

* Click on the `more actions` button on the journal tiddler and choose `fold tiddler`.

Now with all the tiddlers in on column we see that there are 3 categories emerging:

* Journal
* People
* Systems

Let's group the tiddlers into these categories.

* Open `System X`
* Write `System` in tags field.
* Repeat for `System Y`.
* Add label `Person` to `Alice Bishop` and `Bob Dobbs`.
* And `Journal` to the first tiddler.

The tags create a shortcut to all other tiddlers with the same tag.

Now we are done with the bare essentials and can start automating repetitive parts.

# Make it Right

## Create a Shortcut for Journal Tiddlers

If you are serious about keeping daily notes, then there will be a journal tiddler for every day at work. Although it is not difficult to create tiddlers with the current date and tagged with `Journal`, there is a shortcut for this.

* Open sidebar -> `Tools`
* Check `new journal`, observe a new button appearing on the sidebar.
* Click it.

The created journal tiddler has the right tag, however the format is `30th March 2023`. It looks nice, but a bit impractical if you need to link to Journal tiddlers or sort them alphabetically, so let's change the journal title format to ISO-8601 as we did in the very first tiddler.

* delete the draft of `30th March 2023`.
* Open control panel by clicking on the cog icon on the sidebar.
* Change the value of `Title of new journal tiddlers` from `DDth MMM YYYY` to `YYYY-0MM-0DD`, zeroes are needed to add leading zeroes.
* Close the `Control Panel` tiddler.
* Click the `create new journal tiddler` button again.  Much better!

## Create a Snippet for Daily Standups

Standups repeat every day, so it makes sense to automate adding notes on them with a template or as it's called in TiddlyWiki, a snippet.

* Close all tiddlers and open the two journal tiddlers.
* Click on the stamp icon and select `Add your own`.
* Call the new tiddler "StandupSnippet", the title does not matter, as it will be referred by a caption, observe the system tag, TiddlyWIki uses internally to find snippets.
* Paste the tiddler text.

```
09:30 Daily Standup

* [[Alice|Alice Bishop]]
* [[Bob|Bob Dobbs]]
```

* add caption `09:30 Daily Standup`
* Close the StandupSnippet tiddler.
* Open the newest Journal and add the snippet.

## Create a Macro for Jira Tickets

One more frequent thing that we should automate is adding Jira links, so instead of typing ` [[ABC-123|https://jira.corp.net/ABC-123]]` we can type `<<jira ABC-123>>` and get the same result.

* add `** Merged <<jira ABC-123>>.` to today's journal tiddler for Alice.
* Create a new tiddler called `JiraMacro`.
* Add `$:/tags/Macro` system tag.
* Use the snippets button to insert `Macro definition`
* Change

```
\define macroName(param1:"default value",param2)
Text of the macro
\end
```

to

```
\define jira(id)
[[$id$|https://jira.corp.net/$id$]]
\end
```

* Save `JiraMacro` tiddler, observe that the journal tiddler shows the correct link.

## Backups

The final point in the "Make it Right" part is backups. Please do them regularly. Since the whole wiki is just a single file choose a way that works for you. I keep my backups as a private snippet on Stash, but any other solution will work as well.

# Make it Beautiful

Ok, for the final part of the practice we will add a couple of bells and whistles to our TiddlyWiki.

## Add Visual Tweaks

Now that we don't have to worry about losing our data, we can go nuts on customizing the wiki.

* Open `ControlPannel` (cog icon)

### Info

* Navigate to `Info`
* Change the `Title of this TiddlyWiki` and `Subtitle`, observe changes in the sidebar.
* Change the animation duration from default `400` to `200` milliseconds for a snappier feel.
* Change `Default tiddlers` to "retain story ordering", to see the same tiddlers when you re-open the wiki.

If you feel curious, after the tutorial, you can explore the `Advanced` tab, it has some nerdy diagnostic information.

### Appearance

* Navigate to `Appearance`.
* Navigate to `Palette`
* Choose a theme that suites your mood.

Later you can press `show editor` button at the bottom and create the official "kitsch pink" theme if that's what you like.

### Toolbars

* Navigate to `Toolbars`

#### Page Toolbars

* Navigate to `Page Toolbars`
* Uncheck `save changes` with the plugin we installed saving happens automatically and is indicated with a small hover.
* add `more` button to have access to less used buttons.

There are a few other useful buttons:

* Check `palette` if you are feeling trendy and want the notes to match your day's outfit.
* If you are a tinfoil-cap paranoid type select the `encrypt` button, but be aware that password-protecting your wiki will make it useless if you forget the password.
* `full screen` is for the mythical focus-mode we all desire.
* `print` is a great button if you need to quickly make a PDF or a paper version of the currently open tiddlers.

Observe that icons can be rearranged by dragging.

#### View Toolbars

Finally, let's customize View Toolbars. I think it's alright by default, just check `fold tiddler` button, so that you can leave only the title while focusing on other open tiddlers.

* Navigate to `View Toolbars`
* Select `Fold Bar` to quickly fold/unfold tiddlers.

#### Theme Tweaks

* Navigate to `Theme Tweaks`
* In `Options` change `Sidebar layout` to `Fluid story, fixed sidebar` to get move screen space to the story river.
* Enable sticky titles, they are nice.

> "One designer played with the fonts and lost."

so let's not touch those, the defaults are a-ok.

* Navigate to `Settings` tab
* Uncheck `Enable automatic CamelCase linking` otherwise TiddlyWiki will consider any CamelCased word as a link to new Tiddler.
* Close `ControlPannel` tiddler.

Phew. That concludes the tweaking part.

## Sharing Your Work

At some point you may want to share the notes with other people and there are several options for that.

### Sharing a single tiddler:

* Open some tiddler.
* Click on `more menu` on a tiddler, choose `Export tiddler` -> `Static HTML`, examine the downloaded file.
* Can also be exported as `.tid` file and imported by drag-and-drop into another TiddlyWiki.

### Sharing the whole TiddlyWiki

* Open `more` menu in the sidebar.
* Click on `export all`, you will see the same choices, but for the whole wiki.

### As a printed PDF using Print button.

A quick and easy way to share a subset of tiddlers is to unfold them, hide the sidebar and click on the printer icon and print to a PDF.

## Enhance Tags

* Navigate to Sidebar -> `More` -> `Tags`.
* Open tag manager system tiddler, add an appropriate icon and a fancy color.
* Show that the tag appears, click on it to see all tag-mates and a tiddler, representing tag, * Write info about `System`, some common info.

```
Common information about systems at Corp.

* [[The global repository for system accesses|https://corp.net/systems]]
* [[Rules for creating a new system|https://corp.net/new_system]]
```

* Use "List of tiddlers by tag" to enrich the `Journal` tiddler.

## Plugins

How many of you use

* Browser plugins?
* Jenkins plugins?
* Vim plugins?
* Winamp plugins? Anyone? Ah well!

Then you know the first rule of plugins. Don't overdo it! Understand the limitations of vanilla before installing a bunch. It is very easy to install, it's just drag-and-dropping the plugin into an open tab.

Here is the top list of plugins that I use:

1. Filesystem saver (already installed)
1. [TODO plugin](https://kookma.github.io/TW-Todolist/)
    * `<<todolist-ui caption:"!!" base:"Simple" width:60%>>`
    * Keep TODO widget-page alway open, unloads your focus, production line with occasional gremlins analogy.
1. [Highlight.js](https://tiddlywiki.com/plugins/tiddlywiki/highlight/)
    * invaluable for storing pieces of code.
1. [Mermaid](https://efurlanm.github.io/mermaid-tw5#%24%3A%2Fplugins%2Forange%2Fmermaid-tw5)
    * Great for generating diagrams
    * Btw, everyone's darling, ChatGPT, is amazingly good at generating the mermaid diagrams given enough context.
1. [Reveal-js](https://sukima.github.io/tiddlywiki-reveal-js/#%24%3A%2Fplugins%2Fsukima%2Freveal-js:%24%3A%2Fplugins%2Fsukima%2Freveal-js%20Introduction%20Install%20Documentation%20License)
    * I made the slides in it.
1. [QR Code](https://tiddlywiki.com/editions/full/#%24%3A%2Fplugins%2Ftiddlywiki%2Fqrcode)

There are also plugins that I haven't installed but see they could be fun:

* [TiddlyMap](http://tiddlymap.org/) if you feel like searching for Pepe Silva
* [Stroll](https://giffmex.org/stroll/stroll.html) for two-column view
* [KaTeX](https://tiddlywiki.com/editions/full/#%24%3A%2Fplugins%2Ftiddlywiki%2Fkatex) plugin if you write in LaTeX
* [markdown](https://tiddlywiki.com/editions/full/#%24%3A%2Fplugins%2Ftiddlywiki%2Fmarkdown) to allow writing tiddlers in Markdown.

## Add Custom favicon

This wiki, your wiki, is almost perfect. Now let's add a final touch and add a favicon, so that you can easily find it among other open browser tabs.

* Navigate to <http://www.faviconer.com/>
* Draw a cool 32-pixel icon, give it a name and description and download.
* Drag-and-drop to import into wiki
* rename the tiddler to `$:/favicon.ico`.
* Now if you pin it it will be easy to find.

Setting a favicon is an equivalent of naming a pet, so this TiddlyWiki is with you to stay.
