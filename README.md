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
#### [Sarah Parmenter](https://twitter.com/sazzy)

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
#### [Luke Wroblewski](https://twitter.com/lukew)

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

### Prototyping: The Scientific Method of Business
#### [Daniel Burka](https://twitter.com/dburka)

- "What keeps you up at night?" - A good question to ask other people in your business org.
- Designers are not working on solving internal issues (e.g., procurement, hiring). Where is design really effective?
- Design done right can be the scientific method for business.
- "Inklings": Rough-edged ideas that are not well formed, things that we argue about in meetings.
- How do we test hypotheses? We argue about them, and guessing about what customers want.
- Test several ideas and measure them, we'll at least get directional feedback on what ideas hold merit.
- Basement lab: Help your team see their own inklings.
- If a picture is worth a thousand words, a prototype is worth a thousand meetings.
- All you need is you to get started in the basement lab.
- Start prototyping, and when you have a prototype, bring it back to the meeting. It's something you can _show_ people.
- Prototypes are throwaway interfaces. They're a starting point, or something to invalidate what you once _thought_ was a good idea.
- High school science lab: Prototyping level 2, instead now you test with real customers.
- Industrial grade science lab: Prototyping level 3, a master class is creating a prototype with intention as a group.
- Day 1: Gather a sprint team, create time pressure, find the right challenge.
- Day 2: Find more than one solution. No group brainstorms: Group brainstorms are resolved by the loudest voice in the group.
- Day 3: Make good, quick decisions. No design-by-committee. Entertain risky ideas.
- Day 4: Prototype.
- Day 5: Research.
- Gather the right team, create time pressure, and conduct quick, credible research.
- Step by step instructions: http://gv.com/sprint

### Story First: Crafting Products That Engage
#### [Donna Lichaw](https://twitter.com/dlichaw)

- If you want to engage your audience, you have to have an engaging story.
- Story 101: Beginning, middle, end. This timeline has a narrative arc, dotted with plot points.
- Exposition: The beginning, where the main players are introduced. Possibly foreshadowing of something on the horizon (the problem).
- Rising action: Things get exciting, working toward a climax.
- Crisis: The point of no return. Will the crisis be averted?
- The Climax/Resolution: Crisis has been averted. The problem has been solved.
- The Denouement: Calming down, and everything is normal. The main players have grown and developed. Or a chance to continue the story (a serial narrative).
- The same narrative parsing we use to understand movies/series is the same as the narrative we used to understand the photograph.
- Life is a story. You are the hero.
- Who is your user and their big goal? What is their problem? What is your product name and market category? What is the competition? Why might they not want to adopt your product? Promise value/competitive advantage. What is the takeaway we want people to think or feel about our product? And again, what is their big goal? Has that goal been met?
- Unboxing is exciting, and is part of the product narrative arc.
- App sign-up flows are great examples of narrative arcs for users.
- The climax just needs to be nearest towards the end of any user flow. (I purchased the socks.) The resolution? (I got the socks.)
- The product narrative arc: Goal -> Problem Incentive CTA -> Flow -> Impediment (Sign up, payment, funnel drop-off, mental hurdles, boredom, lack of value, usability) -> Solve Problem/Experience Value -> Finish the flow/wrap it up. -> Goal met!
- Arcs give us a sense of time, and the ability to project what might happen.
- Our brains are activated when we recognize the narrative arc happening before us.
- Once you have a story, you can start developing it and testing it.
- Visualize the narrative arc by prototyping. Sketch it out. Illustrate the arc and all its plot points, and that will help you realize if the story is worth telling.

### The Last Ten Percent: When and Where to Add Polish That Matters
#### [Cassie McDaniel](https://twitter.com/cassiemc)

- 1. Why would we polish product?
- 2. How do we add that polish?
- 3. Does it matter if we add the polish?
- "The details are not the details. They make the design."
- We're in search of work that reflects the beauty we want to see in the world.
- Polish not only takes time, but a willingness to iterate and change what you did before. It means you've got to _stick with something_.
- If you're just copying something, you're not learning anything new. Start with the original idea and iterate on that to get something original.
- It's hard to get to the simple and obvious, but it's worth the journey.
- Critique is one of the most crucial tools as a designer.
- Surround yourself with people who will challenge your best work.
- We can collaborate with specialists to create really valuable work.
- Don't let perfection be the enemy of done.
- Iterate -> Balance -> Simplify -> Apply -> Work in a team.
- We will always be needed to make something more bespoke or human. It's the details that humans add that give an impression of something being, well, human.

### The Joy of Optimizing Images
#### [Una Kravets](https://twitter.com/Una)

- Images on the web affect all of us.
- Performance is a user experience problem. We need to take responsibility on every level.
- The average single JPG is 2.5x than the average JS file.
- The average iPhone 6 photograph is 2.5 MB. Waaaay too big.
- We take images without thinking about the cost: Irresponsible images! It becomes a problem when we cram these down the pipe to users.
- 19 seconds is the average load time for sites over 3G.
- Mobile site loading within 5 seconds had sessions lasting 70% longer.
- 53% of visits to mobile sites are abandoned after 3 seconds.
- People don't have patience for slow sites anymore.
- Most emerging markets/developing nations have yet to join the web.
- Most developing nations have poor infrastructure and slower devices.
- Access to information should be a basic human right. Performance addresses this.
- You can't be a web performance expert without being an image expert.
- Different formats are suitable for different types of content.
- Guetzli compression for JPEGs, which is a psychovisual optimization.
- General guidelines: 80% is a good maximum.
- WebP is a promising "new" format (it's been around for a while, but is gaining prominence).
- You can convert to WebPs using ImageMagick.
- Use the `<picture>` element to fall back to WebP.
- Use the `<video>` element to fall back to WebM.
- FLIF for responsive imagery sends multiple encodings in one file.
- Automate image optimization.
- ImageOptim is a great GUI program.
- SVGOMG, a web GUI for SVGO.
- Manually blur out unimportant parts of the image to save data.
- Use blurry placeholders for lazily loaded images ("blur up").
- Greyscaling reduces image size.
- CSS blend modes can liven up images and save data.
- Reducing contrast to reduce color space, which reduces file size: Start with image, remove image contrast, add contrast back in as a CSS filter.
- Manually tune GIFs in Photoshop to squeeze more bytes.
- Alternatives to GIFs: Videos.
- Leverage cache to keep media in caches longer.
- Inspect the `Accept` header to send WebPs on the server side.
- Compress SVGs using gzip/Brotli.
- Challenge the idea that 2x for Retina is always the "right" way to go.
- Consider your image format, and use `<source>` `media` attributes to send properly sized images.
- Find balance for users. It's all about user experience.
