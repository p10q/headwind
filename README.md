# Overview

The rationale for this is...

You want to use a 95% compatible tailwinds utility classes, but don't
want JS to be the one the injects tailwind styles. And you can afford to
download make 3-400kb of CSS (or otherwise have a mechanism to strip
unused styles).

The motivation for me was working on a legacy rails app and I couldn't
figure out a clean way to integrate tailwind with no preflight.

There's some less-commonly-used tailwind css styles that aren't carried
over. But yeah if this becomes useful we could revisit that.

# Installation

Yeah, you just include headwind.css.

And postprocess or whatever else if that's something that you're into.
