This is a list of new fixes and other changes made to SOUP during its continued development.

SOUP version numbering generally follows the _major.minor.patch_ scheme.  Odd minor versions (1.1.x, 1.3.x, 1.5.x, etc.) are reserved for unstable development versions ("devel" branch on [GitHub][github]), while even ones denote stable releases ("master" branch on [GitHub][github]).  The change log below thus only includes even version numbers, as changes between development versions are too numerous to list.

1.8
===

**Changes in 1.8.1:**

* The fix for [mso212372](http://meta.stackoverflow.com/q/219740) is no longer needed, and has been removed.
* The fix for [mso104184](http://meta.stackoverflow.com/q/104184) is no longer applied in the mobile view; see [this feature request](http://meta.stackoverflow.com/q/213709) for details.
* The README Markdown has been simplified for better compatibility between GitHub, StackApps and UserScripts.org.

**New fixes in 1.8.0:**

* [mso60390: Inconsistent padding of inline code](http://meta.stackoverflow.com/q/60390) ([CSS][CSS])
* [mso219740: Add spacing / padding to “Protected By…” and “Not the answer you're looking for”](http://meta.stackoverflow.com/q/219740) ([CSS][CSS])
* [mso212372: Top bar should be consistent on all sites… but it's not](http://meta.stackoverflow.com/q/212372) ([CSS][CSS])
* [mso222509: Getting Red Line under tags](http://meta.stackoverflow.com/q/222509) ([CSS][CSS], [chat][chat]) (partial fix)
* [mso220470: CSS for daily site access calendar on profile page fails to load over HTTPS](http://meta.stackoverflow.com/q/220470)
* [mso220337: Election comments have no permalink link](http://meta.stackoverflow.com/q/220337)

**Other changes:**

* The code has been reorganized into self-contained modules, each corresponding to one bugfix / workaround.  Currently, this has little effect on functionality, but it could be used e.g. to allow toggling individual fixes on/off.
* Utility functions like <code>hookAjax()</code> are now contained in a page-global <code>SOUP</code> object.
* A new <code>SOUP.hookEditPreview()</code> utility function has been added to allow easier editing fixes.
* CSS fixes are now injected before the document is loaded, reducing the risk of "flickering".  As a side effect, a few selectors had to be adjusted to increase their specificity over conflicting SE default styles.
* Added a change log, with retroactive logging for earlier releases.

1.6
===

**Changes in 1.6.1:**

* The fix for [mso216760](http://meta.stackoverflow.com/q/216760) caused a [regression](http://meta.stackoverflow.com/q/221733) in the chat transcript view.  This has been fixed.

**New fixes in 1.6.0:**

* [mso136589: The monospace formatting in a spoiler quote on a beta site is evil](http://meta.stackoverflow.com/q/136589) ([CSS][CSS])
* [mso112305: Code samples inside of spoilers are still visible on some sites](http://meta.stackoverflow.com/q/112305) ([CSS][CSS])
* [mso110566: Does the spoiler markdown work on images?](http://meta.stackoverflow.com/q/110566) ([CSS][CSS])
* [mso217779: The CSS for spoilers is a mess. Let's fix it!](http://meta.stackoverflow.com/q/217779) (*not* CSS only, supersedes above three fixes)
* [mso58760: &lt;kbd&gt; (yes, still &lt;kbd&gt;) doesn't play nice with lists](http://meta.stackoverflow.com/q/58760) ([CSS][CSS])
* [mso160338: Allow moderators to reply to a flag](http://meta.stackoverflow.com/q/160338) ([mod][mod])
* [cs537: Missing MathJaX in the duplicate subtab of the close review queue](http://meta.cs.stackexchange.com/q/537) ([math][math])

1.4
===

**New fixes in 1.4.0:**

* [mso143973: Images can be pushed outside the boundaries of a post by using nested lists](http://meta.stackoverflow.com/q/143973) ([CSS][CSS])
* [mso217120: Ugly overflows when editing a deleted answer inline](http://meta.stackoverflow.com/q/217120) ([CSS][CSS])
* [mso145819: &lt;hr/&gt;'s do not get rendered in deleted answers](http://meta.stackoverflow.com/q/145819) ([CSS][CSS])
* [mso108046: Mouse cursor doesn't change to pointer when hovering “full site” on mobile](http://meta.stackoverflow.com/q/108046) ([CSS][CSS])
* [mso216760: The reply buttons in chat shouldn't reposition themselves on pinged messages](http://meta.stackoverflow.com/q/216760) ([CSS][CSS], [chat][chat])
* [mso134268: U+0008 inserted into chat @-pings](http://meta.stackoverflow.com/q/134268) ([chat][chat])
* [mso78989: Clicking on tags broken?](http://meta.stackoverflow.com/q/78989)
* [mso214706: The branch prediction answer is overflowing](http://meta.stackoverflow.com/q/214706)
* [mso66646: Confirming context menu entries via Enter triggers comment to be posted](http://meta.stackoverflow.com/q/66646)
* [mso210132: New top bar should render avatar with a transparent background](http://meta.stackoverflow.com/q/210132)
* [mso150069: Can we have the "50 more" link return items of the same type, please?](http://meta.stackoverflow.com/q/150069) 
* [math11392: MathJax preview broken when equations contain `\label`s](http://meta.math.stackexchange.com/q/11392) ([math][math])

1.2
===

**New fixes in 1.2.0:**

* [math4130: The scope of \newcommand is the entire page](http://meta.math.stackexchange.com/q/4130) ([math][math])
* [mso114109: Background in OP's user name can obscure text in multiline comments](http://meta.stackoverflow.com/q/114109) ([CSS][CSS])
* [math11036: Can we have the suggested questions' titles parsed by default?](http://meta.math.stackexchange.com/q/11036) ([math][math])

1.0
===

**Fixes included in the 1.0.x branch:**

* [mso114636: All Stack Exchange sites in a small window causing display problems?](http://meta.stackoverflow.com/q/114636) ([CSS][CSS])
* [mso215473: Add a non-breaking space to “reopen (1)” and its ilk](http://meta.stackoverflow.com/q/215473) ([CSS][CSS])
* [mso155308: Ignoring somebody screws up the avatar list](http://meta.stackoverflow.com/q/155308) ([CSS][CSS], [chat][chat])
* [mso138685: Layout fix for Firefox in “Zoom text only” mode](http://meta.stackoverflow.com/q/138685) ([CSS][CSS])
* [mso207526: Cannot navigate into the multicollider with keyboard](http://meta.stackoverflow.com/q/207526)
* [mso129593: Un-fade low-score answers on rollover or click](http://meta.stackoverflow.com/q/129593)
* [mso104184: Allow flagging a comment after upvoting it](http://meta.stackoverflow.com/q/104184)
* [mso215450: SSL breaks TeX rendering](http://meta.stackoverflow.com/q/215450)
* [mso150069: Can we have the "50 more" link return items of the same type, please?](http://meta.stackoverflow.com/q/150069) ([10k][10k])
* [mso209393: Render MathJax in the 10k tools](http://meta.stackoverflow.com/q/209393) ([10k][10k])

----

Notes:

* <b id="note-css">CSS</b>: This is a pure CSS fix.  It will be applied even if site JavaScript is disabled.
* <b id="note-chat">chat</b>: This fix applies to the [Stack Exchange Network chat](http://chat.stackexchange.com "Stack Exchange Network chat").
* <b id="note-10k">10k</b>: This fix applies to the "moderator tools" interface available to users with 10,000+ rep (3,000+ on beta sites).
* <b id="note-mod">mod</b>: This fix applies to the full moderator interface available only to ♦ moderators.
* <b id="note-math">math</b>: This fix applies only to sites using MathJax for LaTeX math rendering.

   [CSS]: #note-css "This is a pure CSS fix.  It will be applied even if site JavaScript is disabled."
   [chat]: #note-chat "This fix applies to the Stack Exchange Network chat (chat.stackexchange.com)."
   [math]: #note-math "This fix applies only to sites using MathJax for LaTeX math rendering."
   [10k]: #note-10k " This fix applies to the "moderator tools" interface available to users with 10,000+ rep (3,000+ on beta sites)."
   [mod]: #note-mod "This fix applies to the full moderator interface available only to ♦ moderators."
   [github]: https://github.com/vyznev/soup "SOUP repository on GitHub"