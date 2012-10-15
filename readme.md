##Recommended jQuery Plugin Patterns

###Introduction

So, you've tried your hand at writing jQuery plugins and you're comfortable putting together something that probably works. Awesome!. Thing is, you think there might be better ways you could be writing them - you've seen them done a number of different ways in the wild, but aren't really sure what the differences between these patterns are or how to get started with them. This project hopes to help solve this.

I began this patterns repo after seeing a number of efforts made in the past to create a one-size-fits-all jQuery plugin boilerplate. Whilst the idea of such a boilerplate is a great idea in theory, the reality is that in plugin development we <b>rarely</b> approach writing plugins in one very-fixed way using a single pattern all the time. 

Some patterns may work better for structuring solutions to a particular problem or component than others. Some developers may wish to use the widget factory. Some may not. Some might like to take advantage of nested namespacing patterns.  Some might want to use custom events or pub/sub to communicate from plugins to the rest of their app. Some may prefer using extend patterns and so on.

This project won't seek to provide solutions to every possible pattern, but will attempt to cover popular patterns developers often use in the wild.

###Patterns 

<ul>
<li><strong>A lightweight start</strong>: perfect as a generic template for beginners and above, uses a basic defaults object, simple constructor for assigning the element to work with and extending options with defaults and a lightweight wrapper around the constructor to avoid issues with multiple instantiations - jquery.basic.plugin-boilerplate.js</li>
<li><strong>Widget factory</strong>: for building complex, stateful plugins based on object-oriented principles. The majority of jQueryUI heavily relies on the widget factory as a base for components and this template covers almost all supported default methods including triggering events - jquery.widget-factory.plugin-boilerplate.js</li>
<li><strong>Widget factory + RequireJS</strong>: for wrapping jQueryUI widgets inside RequireJS compatible modules. Also demonstrates very basic widget templating - jquery.widget-factory.requirejs.boilerplate.js</li>
<li><strong>Widget factory for jQuery mobile</strong> - demonstrating best practices for building mobile widgets, includes many of the same concepts as the widget factory boilerplate, but also JQM specific usage advice/tips in the comments - jquery.widget-factory.mobile-plugin.boilerplate.js </li>
<li><strong>Namespaced pattern</strong>: to avoid collisions and improve code organization when working with components under another namespace - jquery.namespace.plugin-boilerplate.js</li>
<li><strong>Better options</strong>: globally/Per-call overridable options for greater option customization, based on Ben Almans pluginization talk - jquery.best-options.plugin-boilerplate.js</li>
<li><strong>Custom events (Pseudo Pub/Sub)</strong>: for better application decoupling. Uses the Widget factory, but could be applied to the generic template - jquery.customevents.plugin-boilerplate.js</li>
<li><strong>Extend pattern</strong> - jquery.extend-skeleton.plugin-boilerplate.js</li>
<li><strong>Non Widget-factory widget</strong>: if you wish to stay away from the widget factory. Uses Ben Alman's simplewidget including coverage for creation, instantiation and other best practices that may be helpful  - jquery.simplewidget.plugin-boilerplate.js</li>
<li><strong>Prototypal inheritance pattern</strong>: use a bridge to generate a plugin from an object (literal). Useful for code organization, readability, functionality heavily based around DOM element selection - jquery.prototypal-inheritance.plugin-boilerplate.js</li>
<li><strong>Universal Module Definition pattern</strong>: create AMD and CommonJS compatible plugin modules which are compatible with a number of different script loaders - amd+commonjs</li>
</ul>


###Further reading:

The best source of information for how to use the plugins in this repository can be found here:

[http://addyosmani.com/resources/essentialjsdesignpatterns/book/#jquerypluginpatterns](http://addyosmani.com/resources/essentialjsdesignpatterns/book/#jquerypluginpatterns)



###Contributing

If you have ideas for improvements that can be made to patterns currently in the repo, please feel free to create a new issue for discussion or send a pull request upstream. The same can be said about new patterns you wish to propose being added; for the sake of limiting confusion and complexity, I would ideally like to keep the number of overall patterns in the repo, but there are plans to separate these out into folders based on concerns. 

###Credits
Thanks to @peolanha, @ajpiano, @mathias, @cowboy, @dougneiner and others for their previous work (or tips) in this area. Some of this work is used as a basis for further improvements.

