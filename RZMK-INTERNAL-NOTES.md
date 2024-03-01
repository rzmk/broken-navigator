# Internal notes

The following are quick notes as I attempt the broken-navigator challenges.

> If you haven't finished the challenges yet I suggest not reading the section for that challenge until afterwards as it may give insights on solutions.

## space-navigator/1

-   Tauri identifies different file paths with a common name regardless of the platform (such as `$RESOURCE`) even though the file paths may differ for each OS.
-   Don't allow passwords to be found in logs in production applications.

## space-navigator/2

-   Custom commands do not need to be restricted by the allowlist (for example making a Rust command with [#tauri::command])

## space-navigator/3

This one was a bit more challenging for me. I was able to use the console in DevTools for invoking a tauri command with the window object, but identifying the resource path properly was a bit confusing at first. Looking at the `options` for the Rust API code for `writeFile`, there's a `BaseDirectory` enum that can be filled into the `dir` option with the right number to use as the base directory while I write the rest of the path as indicated in the config. Finding the enum was done primarily with looking through source code, then the Tauri website as [linked in the js path API](https://tauri.app/v1/api/js/path/#basedirectory) which helped me find the right value to use.
