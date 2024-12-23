# Uncommon HTML Bug: innerHTML and Event Listeners

This repository demonstrates an uncommon bug related to using `innerHTML` in HTML along with event listeners. Replacing the `innerHTML` of an element that already has an event listener attached can lead to the listener being unintentionally removed.  The bug and its solution are illustrated in separate HTML files.

**Bug:** `bug.html` showcases the issue.  Clicking the div will trigger an alert. However, after the `innerHTML` is replaced, the event listener on the div is lost, and subsequent clicks will no longer work. The button's `onclick` works as expected because it's set directly in the new HTML inserted using `innerHTML`.

**Solution:** `bugSolution.html` demonstrates how to avoid this problem by detaching or re-attaching event listeners after modifying the `innerHTML`.