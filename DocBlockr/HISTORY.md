# DocBlockr Extended Changelog

- **v2.6.2**, *22 March 2012*
  - PHP `__destruct` functions don't get a return value *(thanks to [Alex Whitman](https://github.com/whitman))*.
- **v2.6.1**, *16 March 2012*
  - Fixes bug whereby the return values of functions which are named `set` or `add`, *etc* were not being guessed correctly.
  - `@return` tags are now given a description field *(thanks to [Nick Dowdell](https://github.com/mikulad13))*.
- **v2.6.0**, *4 March 2012*
  - Added CoffeeScript support
- **v2.5.0**, *11 February 2012*
  - Implemented DocBlock reparsing to re-enable tabstop fields. Hotkey is `Ctrl+Alt+Tab`.
- **v2.4.1**, *2 February 2012*
  - Fixed bug [#36](https://github.com/spadgos/sublime-jsdocs/issues/36) whereby docblocks were not being properly extended inside of `<script>` tags in a HTML document.
- **v2.4.0**, *29 January 2012*
  - `Enter` at the end of a comment block (ie: after the closing `*/`) will insert a newline and de-indent by one space.
- **v2.3.0**, *15 January 2012*
  - `Ctrl+Enter` on a double-slash comment will now decorate that comment.
  - Added a setting (`jsdocs_spacer_between_sections`) to add spacer lines between sections of a docblock.
- **v2.2.2**, *12 January 2012*
  - Separated JS and PHP completions files. PHP completions don't have brackets around type information any more.
  - PHP now uses `@var` (instead of `@type`) for documenting variable declarations.
  - *Both of these changes are thanks to [svenax][svenax]*
- **v2.2.1**, *11 January 2012*
  - DocBlocks can be triggered by pressing `tab` after `/**`
  - Some bugfixes due to auto-complete changes in Sublime Text.
  - Fixed bug where indenting would not work on the first line of a comment.
- **v2.2.0**, *5 January 2012*
  - A configuration option can be set so that either `@return` or `@returns` is used in your documentation. 
  - Language-specific tags now will only show for that language (eg: PHP has no `@interface` tag).
- **v2.1.3**, *31 December 2011*
  - Changed path for macro file to point to `Packages/DocBlockr`. If you are having issues, make sure that the plugin is installed in that location (**not** the previous location `Packages/JSDocs`).
- **v2.1.2**, *31 December 2011*
  - Renamed from *JSDocs* to *DocBlockr*, since it now does more than just Javascript.
- **v2.1.1**, *23 November 2011*
  - Fixed bug which broke the completions list
- **v2.1.0**, *19 November 2011*
  - Added a command to join lines inside a docblock which is smart to leading asterisks
  - Variable types are guessed from their name. `is` and `has` are assumed to be Booleans, and `callback`, `cb`, `done`, `fn` and `next` are assumed to be Functions.
  - You can now define your own patterns for mapping a variable name to a type.
  - Autocomplete works better now. `@` will also insert the "@" character, allowing you to add any tag you like, even if it isn't in the autocomplete list.
  - Added the full set of [PHPDoc][phpdoc] tags.
- **v2.0.0**, *6 November 2011*
  - PHP support added!
  - (Almost) complete rewrite to allow for any new languages to be added easily
    - *Please send feature requests or pull requests for new languages you'd like to add*
  - More options for aligning tags
- **v1.3.0**, *5 November 2011*
  - Improvements to handling of single-line comments
  - Functions beginning with `is` or `has` are assumed to return Booleans
  - Consolidated settings files into `Base File.sublime-settings`. **If you had configured your settings in `jsdocs.sublime-settings`, please move them to the Base File settings.**
  - Setting `jsdocs_extend_double_slashes` controls whether single-line comments are extended.
  - Pressing `tab` in a docblock will tab to match the description block of the previous tag. Use `jsdocs_deep_indent` to toggle this behaviour.
- **v1.2.0**, *6 October 2011*
  - Variable declarations can be documented. `Shift+enter` to make these inline
  - Double slash comments (`// like this`) are extended when `enter` is pressed
  - Class definitions detected and treated slightly differently (no return values pre-filled)
- **v1.1.0**, *3 October 2011*
  - DocBlockr parses the line following the comment to automatically prefill some documentation for you.
  - Settings available via menu
- **v1.0.0**, *28 September 2011*
  - Initial release
  - Comments are automatically closed, extended and indented.
