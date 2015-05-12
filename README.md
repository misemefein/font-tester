# font-tester

Javascript bookmarklet to override css replace the font used on any website with your own font. It grabs whatever font(s) are used on a webpage, and replaces them with a locally installed font—namely—yours. Especially useful for testing non-latin scripts without mocking up contexts with Adobe CC.

Installation instructions. I have only tested this in Firefox and Chrome.

1: Export your .otf as usual from your font editor. It is best to keep naming convention relatively simple, ie [myFont-Regular]
2: Locate your file in Finder, and install in your favourite font management software. 
3: Using your favourite code editor, paste in the following:

**
javascript:(function(){var%20s=(document.getElementsByTagName('head')[0]||document.body).appendChild(document.createElement('style'));var%20t=document.createTextNode('*{font-family:******!important;%20line-height:%20135%;%20font-size:%201.03rem;}');s.appendChild(t);})();
**

4: Replace the ****** with your exact font name ie [myFont-Regular]
4: In the browser, show all bookmarks, then duplicate any old bookmark (alt-drag)
5: Rename the link to whatever you want the bookmarklet to display, ie FontTester. 
6: In the location (link) field, replace the link from your old bookmark with your new bookmarklet.
7: Load up a test page, and hit the bookmarklet.

The hack essentially targets the page styles, and will change the font, but also increase the font size to 1.03rem (relative em) and also the the leading to 135%. You can of course alter these parameters as you wish.

** [PostStudio_](https://twitter.com/PostStudio_)

