# Overview

The rationale for this is...

You want to use a 95%-compatible tailwinds utility classes, but don't
want JS to inject styles. And you can afford to
download maybe 3-400KB of CSS (or otherwise have a mechanism to strip
unused styles).

The motivation for me was working on a legacy rails app and I couldn't
figure out a clean way to integrate tailwind with no preflight (which throws
off some styles).

There's some less-commonly-used tailwind css styles that aren't carried
over. But yeah if this becomes useful we could revisit that.

# Installation

Yeah, you just include headwind.css.

And postprocess or whatever else if that's something that you're into.

# N.B.

I'm starting to see the beauty of what tailwind is doing and recommend either:

[Rails 7 + Tailwind](https://www.youtube.com/watch?v=JsNtLiph87Y) or just rewriting everything in [Svelte.js](https://www.youtube.com/watch?v=uQntFkK8Z54) ([other](https://www.youtube.com/watch?v=3TVy6GdtNuQ) [links](https://www.creative-tim.com/product/notus-svelte)).

But that's just one droplet of opinion in the web.

Note, [css-for-js.dev](https://css-for-js.dev) and [learnui.design](learnui.design) are great for writing your own design system. And [Chakra UI](https://www.reddit.com/r/nextjs/comments/jznkit/tailwindcss_vs_chakra_ui_for_fast_development/?utm_source=share&utm_medium=ios_app&utm_name=iossmf) is cool. And has a "pro" bundle of UI components, like with Tailwind UI (I surveyed the Twitters last night - both seem like cool core teams). I haven't used either.

But yeah the single reason why I might recommend Svelte in this README that has nothing to do with Svelte is what Brad Traversy mentions in his Svelte crash course. The simplicity of not writing useState but just assigning values. It appears like a pretty scalable simplicity re: overall complexity. Also the Vercel backing of Svelte.js, as mentioned in that interview with Lee Robinson, does give it a bit of inertia re: business use cases and long-term maintenance. Principal engineers are taught to design for 3 years or 5 years (depending on who you ask) - and this makes it so that Svelte will be around for at least that. Plus I trust Shawn Wang has done good investigations into things (and remember him starting a Svelte channel at work).

So if you take a demo/template where you can learn and get pretty decent styles like that Creative Tim link and get Svelte. The amount of time rewriting core functionality from a legacy app using the new stack might just be faster and more enjoyable than dealing with the rest.

As an Amazon engineer (SDM who should leave this to the team more but it's just so...fun for lack of a better word), the talk about edge functions at Vercel (which likely we won't be using because AWS has Lambda@Edge functions, etc.) is pretty cool but yeah.. solves other low-latency site requirements. We've been exploring these more in depth for the simplicity of deployment; and also there are certain low latency services that lambda hasn't been very good at. E.g., feature flag or A/B testing services/lambdas that need to run in the initial page load...

But back to the admin tool that I just got tired of looking at the styles for which is why I went through the Tailwind documentation and programmatically pulled out the most of the code to start integrating it with Rails to start to clean up the UI/layout: I'm looking forward to taking the principles from Josh Comeau and Erik Kennedy and Brad Traversy and beyond re: UI/UX design and writing this tool over winter break -- plus there's other things I should do. So we'll see.

Peace.
