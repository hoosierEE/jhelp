# jhelp
Beginnings of a J addon to provide interactive documentation

Inspiration is from Matlab's `help()` function, which returns documentation for things.

e.g. typing into the prompt the phrase: `help(serial)` would return something like a UNIX manual page for Matlab's `serial`-related functions, directly into the REPL.  Matlab's REPL also allows hyperlinking to other documentation, which is a nice feature for newbies, but perhaps not practical for something that runs in the terminal.

Nice-to-have features would be a way to resolve ambiguous queries, in an interactive manner such as:

    There are 2 results for 'foobar', did you mean one of these?
    1) foobar_jwplot_
    2) foobarbaz_jregex_
    Type 1 or 2 to view documentation for that name.

Also nice would be if the `help` function searched not only the loaded locales, but also the user's `~addons/` folder, or other paths that make sense.

The idea would be that users could add a line to `load'jhelp'` to their config file if desired.