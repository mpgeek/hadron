Towards Hadron as a Drupal base theme
=====================================

The Hadron serve app is a great prototyping tool. What we need is a matching subtheme that utilizes the same markup and front-end libraries to streamline the theming process.

It should be noted that its impossible to create a base theme that is the magic bullet for ALL projects. What we are after here is a subtheme that gives us an out-of-the box look/feel/function that mimicks what our in-browser prototypes  look like (think live wireframes).

# Requirements

What we want:

## Responsive out of the Box, Semantically
The frontend framework of choice should utilize sematic markup to construct the pages. No _.grid-N_ classes should be found in the rendered pages. This would allow grid configuration per project with SASS mixins instead of modifying the markup per project. It should also pursue a [mobile first approach](http://en.wikipedia.org/wiki/Responsive_web_design#Mobile_first.2C_unobtrusive_JavaScript.2C_and_progressive_enhancement).

## HTML 5 + IE Support
The markup should be compliant, standards based HTML5 with fallbacks for older browsers, perhaps using `html5shiv` or `Modernizer`. IE-specific support should also be a part of the out-of-the-box implementation; the depth of support would likely be project specific.

## Accessiblity
Generally speaking, we want as-close-to-perfect accessibility as possible. We want to shoot for WCAG 2.0 compliance on all markup on all pages. There is no such thing as a perfect implementation, but full compliance is a great goal.

## Performance
Obviously, the implementation should not amount to code bloat. We want fast loads for all devices. Some existing themes are known to be slow, we want to avoid this at all costs. Nod and repeat: only load necesarry resources.

## Panels Support
As a matter of best practice, we want to minimize technical debt by proliferation of tpl files. Utilizing panels in this regard, not to mention its strengths in creating reusables, is a win for development in general. By support we don't mean placing panels in a main content area, rather providing configurable pane placement so the same codebase can be used across projects.

## No UI-generated CSS
Deployment is a primary concern and we don't want theme settings generating CSS as deployments are complicated with this type of implementation. Plus we want all CSS generated by the SASS

# Exsisting Tools
There are several themes and starter kits that are good at this or that, but no single tool that serves as a good starting point for most projects. Some tangibles about exsting tools that are out there and what they are good at:

## Zen Grids
[Zen](https://drupal.org/project/zen) is one of the classics. Version 7.x-5.x is a mobile-first implementation with a mostly-semantic grid implementaiton. There is no UI-generated CSS and the grid is configured completely is SASS. There is no high-level Panels support and no claims towards how accessible the markup is. HTML5 with JS fallbacks.

## Adaptive Theme
[Adaptive Theme](https://drupal.org/project/adaptivetheme)
??

## Zentropy
??

## Omega/Delta
??

# Roadmap / TODO

The current preference is for Foundation 4 due to familiarity and current use in the hadron prototyping tool. Before deciding if that is the best route, we need to examine a few things further:

1. Decide on a frontend framework.
* Do we go with Foundation 4 and roll our own base theme?
* Or do we utilize a grid system from one of the exisitng themes?
* Assess the accessibitliy of the pure markup.

We already know foundatoin 4 is meets most of the markup requirements out of the box, its a matter of looking into its accessibility.

1. Figure out the path to go from SASS and markup to drupal theme.

