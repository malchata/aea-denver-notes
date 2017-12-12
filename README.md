# AEA Denver Notes (December 11th-13th)

These are notes for all the sessions I attended at AEA Denver. If you see typos or errors, feel free to put in a PR!

## 11 DECEMBER

### From Research to Redesign: An Unexpected Journey
#### [Jeffrey Zeldman](https://twitter.com/zeldman)

- "There's always something the web site can do for your customers."
- Design is not about chasing trends, but engaging with the customer.
- Research is good for giving you a plan down the road.
- Pixel-perfect should never have been our goal, and it shouldn't be now.
- Better to spend a few weeks figuring out what you need to make rather than losing years building the wrong thing.
- Research exposes blind spots and biases by involving outside perspectives.
- Long tail conversion: Small commitments begetting larger commitments.
- Don't ask for too much information. Good UX == low friction.
- If you need to ask for information, tell the user _why_ you're asking for it.
- Every website needs to answer the question "What's the call to action? What are users here for?"
- An embarrassment of riches without research is useless.
- "Where's the fold?" "The CEO's laptop!"
- Let customers know whether they're anticipating customer needs accurately.
- Stakeholder interviews reveal knowledge and build consensus.

### Digital Marketing Strategies for the Busy “Web Master”
#### Sarah Parmenter

- We are still in the first 10,000 days of the web.
- We are still in the first 3,000 days of social media.
- 33% of jobs don't exist right now that will in 2020.
- We're not asking what we can do for people, we're saying "look at what I've got!"
- Are we chasing vanity metrics? (e.g., 20,000 more followers, posts per day, et cetera.) Case in point: Hit counters!
- We have to check out our personal bias in social networks.
- Check up and coming social media apps, and market early to those audiences.
- Video is the fastest way to build engagement.
- Use HTTPs.
- Mobile ready and performance.
- Starting January 10th: Google is going to penalize sites that have popovers.
- How do we bring people back? Discount codes on the spot, perchance?
- Marketers who use video grow revenue 49% faster than those that don't.
- Most video content is viewed on mobile, and the vast majority watch it without sound.
- To caption video easily: SRT Edit Pro-Make and Edit in the Mac App Store.
- Posts with hashtags performance ~12% better than those without.
- Most people will put their trust into peer recommendations rather than advertising.
- Free trial for https://lefty.io for influencers.
- Some networks don't make sense for every business.

### Obvious Always Wins
#### Luke Wroblewski

- Some design changes seem obvious in retrospect, but aren't so obvious at the time.
- Apple's Maps app's small iterative changes took time, research.
- Don't overwhelm new users with tons of features. Build sensible, usable interaction paths.
- Get close to the customer, and find out how they use the product.
- You can't listen to what people tell you, you have to get the whole story: You should _see_ people using products.
- Qualitative metrics are very different from quantitative metrics.
- Conduct survival analysis: 1) What did users do? 2) What of those actions correlated with them being around later? (surviving)
- Look for design "band-aids", i.e., unintuitive design features.
- Have confidence in the decisions you're making. Have the courage to experiment.
- "I cannot give you the formula for success, but I can give you the formula for failure - which is: Try to please everybody."
- Not "Data-driven decisions", but rather "Data-_informed_ decisions".

### Choose Your Animation Adventure
#### [Val Head](https://twitter.com/vlh)

- CSS is best for animations that have well defined state transitions. Loading/looping, interaction animations, loading states/repeating.
- CSS pros:
  - No external library.
  - Good performance without much effort.
  - Keyframes are reusable.
  - Adjust properties in media queries easily.
- CSS cons:
  - Access to a limited set of events.
  - You have to define animations entirely ahead of time.
  - You can't separate transform properties (currently).
- CSS + JS = 🙌
  - Helps to orchestrate transitions and animations.
- Rules of thumb for moving past CSS to JS:
  - Chaining more than three animations together.
  - If the animation needs to change dynamically at runtime.
  - Need to animate transform properties separately.
  - Physics or other complex structures are required.
- JS is great at:
  - More complex animated interactions.
  - Narrative or immersive animation.
  - Dynamic state transitions.
  - Great for drag and drop interactions.
- Vanilla JS or a Library?
  - Vanilla: requestAnimationFrame
  - A Library: Makes vanilla animations much more manageable.
  - Libraries:
    - GSAP (29 KB) IE8+, SVG, morphSVG, Draggable, $$
    - Velocity (14.4 KB) IE8+, Drop-in for jQuery, MIT/Free
    - Anime (4.7 KB) IE10+, Very lightweight, MIT/Free
- SVG is good at
  - Animated illustrations/icons/logos
  - Animated infographics and data visualization
  - Fluidly scaling, responsive animation
  - Mushy/malleable stuff!
- SVG can be animated in three ways:
  - SMIL (on the outs)
  - CSS
  - JS
- Performance
  - Render flow: Style -> Layout -> Paint -> Composite
  - csstriggers.com (determines how each property hits the render pipeline).
  - Paint flashing in Chrome can reveal non-performant animations.
  - Firefox will tell you if certain animations are/are not hardware accelerated.
  - CSS isn't impacted by the main thread.
  - JS is imperative, and only aware of the current frame.
  - Hardware acceleration isn't a given with JS.
  - SVG is not hardware accelerated.

### Graduating to Grid
#### Rachel Andrew

- Grid is shipped in all major production browsers (~75-80% global support).
- CSS fundamentals: Cascade and Inheritance on MDN.
- You're faking a grid when you use floats and flexbox.
- `max-content`/`min-content` properties upcoming for dictating element size based on content.
- Flexbox is starting from `max-content` and taking space away. Grid starts at `min-content` and adding space.
- `fit-content` puts limits on `max-content`.
- `minmax` means you can specify a minimum and maximum. `auto` for maximums restricts track size.
- Everyone wants everything to be simple, but incredibly powerful. Grid is complex, but is highly capable. And you don't need to learn all of it at once, but rather incrementally.
- Names can be designated for grid tracks in the `grid` declaration in bracket notation e.g., `[content-start]`.
- `grid-area` is a shorthand for four other properties.
- Old CSS in your project doesn't stop you from using the shiny and new. You can take baby steps into using the new stuff.
- Don't forget that the older stuff has its uses.
- Off-the-shelf frameworks are designed to solve _generic_ problems.
- Come up with layout utilities that solve _your_ problems.
- Many browsers without support for grid are mobile browsers, often used by countries with poor infrastructure.
- Stop looking for polyfills and shims. Don't push JS on low-end devices in emerging markets.
- Use a feature query (`@supports`) to ask if the browser supports a feature before using it.
- Don't create cools things just for rich people. Make the web available to everyone.

### Designing with Grid
#### Jen Simmons

- Our medium is not done. Layout on the web is _evolving_.
- A lot of layout on the web is very symmetrical and predictable. It keeps happening that way because we download some framework that prescribes layouts for us.
- Design layout palettes in addition to other design elements (e.g., color and typography palettes).
- We're leaving the age of framework layouts in the next few years.
- Grid won't kill other stuff like flexbox and floats. We're going to keep using them when we need them.
- Explicit vs. implict layout in grid.
- Explicit: Defining the number of columns/Place items specifically.
- Implicit: Leaving it up to the browser
- Grid: We have ROWS, something we haven't had in CSS.
- Tracks don't have to all be the same size.
- Content can be sized by the size of a track, _and_ vice versa.
- We can mix and match units for grid track sizes.
- You can use grid to line things up. Or not.
- Great book: Graphic Design the New Basics.
- Asymmetry is really rare and effective on the web.
- Overlap: We see it all the time in print media. Grid makes it way easier to overlap elements.
- Firefox Nightly has a bunch of awesome new tools!
- The viewport: We can build complex stuff that is unveiled as the viewport reveals it. It's a long, skinny (or wide) vertical space.
- Storyboards: We can design parts of the page, and storyboard what the viewport will reveal as the user scrolls.
- We have the tools to design for all four edges of the screen, not just the top and left edges.
- Framing: Is there a language specific to the web that helps us talk about how we frame layouts?
- We can leave space in our layouts! The most important tool of layout management is _white space_.
- Verticality: We're going to be able to accommodate vertical layouts, especially useful for cultures with languages that lay out text vertically. What _does_ it mean to design in a vertical space?
- The web is a bunch of boxes in vertical spaces.
- `fr` unit = fraction. `fr`s are great for letting CSS decide what to do with the space that remains in a given track.
- `minmax` can be used to establish layouts that will size tracks to minimum and maximum bounds with _any_ kind of units (`ch` driven tracks, anyone?).
- "Pixel perfect" is out the window.
- We are programming the flexibility model.
- Creativity: Grid allows us to be creative and break away from boring frameworks that prescribe layouts.
- Time to play. Time to learn.

---

## 12 DECEMBER