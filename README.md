
# PageMirror build by Kuoll #
This repository is buildable and working version of PageMirror extension.

This build is created by Dmitry Kaigorodov, founder of Kuoll. Kuoll is a web platform that make programming better.
http://www.kuoll.com/

PageMirror is one of examples of usage of mutation-summary library. 
Original version of mutation-summary library is here: https://github.com/rafaelw/mutation-summary
Video about about DOM Mutations and the library is https://www.youtube.com/watch?v=eRZ4pO0gVWw


## Install ##
You can install PageMirror extension from https://chrome.google.com/webstore/detail/pagemirror-build-by-kuoll/kefndlndbcgpbimijjjefolmglodjoda

Alternatively, load unpacked extension from current directory as described here
https://developer.chrome.com/extensions/getstarted#unpacked

## Usage ##

1. Now try navigating to a web page which is highly dynamic. http://www.google.com is a good example.
2. Click the Spock button and move aside the tab which is opened.
3. Make changes in the original google.com window and watch the changes be mirrored in the tab which opened.


### Note ###

Web sites that use iframes (like Gmail) won't work correctly because this example doesn't attempt to recursively mirror the contents of iframes.

The "mirror" won't be functional (interacting with it won't behave like the source page). The reason is that no attempt is made to mirror the javascript state of the source page.


## Techincal Note ##

In this example, the mechanism by which DOM structures are serialized is relatively naive and no attempt is made to minimize the size of the serialized structures (compressing the messages, for example).

However, because this example uses the MutationSummary, the number of DOM structures which must be serialized IS minimized. This is a very good thing, as network bandwidth and latency are nearly always more "expensive" than DOM operations. I.e. Most applications would prefer to do lots of work in the DOM and avoid having to read from or write to the network.


## Uninstallation ##

1. Click the 'Remove' button in PageMirror row on the chrome://extensions page.
