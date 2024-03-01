# Internal notes

The following are quick notes as I attempt the broken-navigator challenges.

> If you haven't finished the challenges yet I suggest not reading the section for that challenge until afterwards as it may give insights on solutions.

## space-navigator/1

-   Tauri identifies different file paths with a common name regardless of the platform (such as `$RESOURCE`) even though the file paths may differ for each OS.
-   Don't allow passwords to be found in logs in production applications.

## space-navigator/2

-   Custom commands do not need to be restricted by the allowlist (for example making a Rust command with [#tauri::command])

