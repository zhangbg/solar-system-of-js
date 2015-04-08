[![title](title.png)](http://shaunlebron.github.io/solar-system-of-js/)
[![preview](preview.gif)](http://shaunlebron.github.io/solar-system-of-js/)

__[>> View Presentation](http://shaunlebron.github.io/solar-system-of-js/)__

#### What and Why?

I made this to visualize the __current state of languages on the JS platform__,
because I am frankly overwhelmed by all the different activity happening in
this space.  It was originally motivated by a desire to bring ClojureScript
into this view, as a language that I think has simple, fundamental solutions to
a lot of the problems that are fragmenting JS.

#### Implementation

The presentation is made with <img
src="http://shaunlebron.github.io/solar-system-of-js/cljs.svg" height="32px">
ClojureScript.  Some details:

- frames are drawn to a Canvas using the 2D api
- all animations tap a `core.async` channel to receive a delta-time `dt` value every frame.
- slide transitions are driven by an [actions spec] to animate [state data]
- the incremental actions spec allows us to jump ahead to specific slides (for URL routing)
- the [drawing] is a pure function of the application state (basically)

###### File Descriptions:

- `core.cljs` - entry point
- `actions.cljs` - slide transition state actions
- `animate.cljs` - animation utility (using core.async)
- `canvas.cljs` - canvas initialization and api wrapper
- `caption.cljs` - caption setter in markdown
- `control.cljs` - touch/key controls
- `draw.cljs` - all drawing functions
- `math.cljs` - math aliases
- `nav.cljs` - slide navigation and routing
- `state.cljs` - state of the application

#### Development Setup

1. Install [leiningen]
2. Run this to get a live-reload compiler, http server, and REPL:

    ```
    $ lein figwheel dev
    ```

3. Open <http://localhost:3449>

#### ClojureScript has a logo?

The [logo] is part of a branding effort for a proper ClojureScript
website that we are building this year, with docs pages and tutorials.

#### Contact

- email: <shaun.e.williams@gmail.com>
- twitter: [@shaunlebron](http://twitter.com/shaunlebron)

#### License

MIT

----

![sketch](sketch.jpg)

[actions spec]:https://github.com/shaunlebron/solar-system-of-js/blob/master/src/solar_system_of_js/actions.cljs#L160
[state data]:https://github.com/shaunlebron/solar-system-of-js/blob/master/src/solar_system_of_js/state.cljs#L5
[drawing]:https://github.com/shaunlebron/solar-system-of-js/blob/master/src/solar_system_of_js/draw.cljs#L459
[leiningen]:http://leiningen.org/
[logo]:https://github.com/oakmac/cljs.info/blob/master/00-scrap/cljs_logo-01.svg

