SCSS demo
=========

Tutorial for SCSS.

##Prerequisites

Install Compass or Sass for pre-processing the stylesheets.

* [Install Compass] (http://compass-style.org/install/)
* [Install Sass] (http://sass-lang.com/install)

To make Compass watch the file and update the CSS every time the Sass file changes run the following from terminal:

```
compass watch --sass-dir src/ --css-dir build/
```

To make Sass do the same:

```
sass --watch src/:build/
```

We assume that _src_ and _build_ are the code and output directory.

##Intro
SCSS provides the following features that makes writing CSS fun.

###Variables
Variables are declared using the __$__ sign in front of the variable name.

```scss
$color: #ccc;
```

###Nesting

  We can nest declaration like HTML and SCSS will automatically process and generate the correct CSS for us.

```scss
div {
  background: #ccc;
  font-size: 1em;
  
  div.foo {
    font-size: 0.5em;
    
    ul.bar {
      background: #ddd;
    }
    
  }
}
```

###Partials

  Partials are like the include files.
  These are used to modularize the CSS code.
  Partials must be created in files with names starting with an underscore for example; _reset.scss
  
  SCSS uses the underscore _ to determine if the file is a partial.

  We use the __@import__ directive to import partials.

  For example,

  import 'filename';

###Mixins

Mixin is created when we combine the properties of two or more objects.

A good use of mixin in CSS would be to use it for the new CSS3 vendor prefixes.

Mixins are declared using the _@mixin_ declarative.
Mixins can be called using the _@include_ declarative.

###Extend/Inheritance

Works just like classical inheritance.

* Create a base css selector with a base set of properties.
* Use the "@extend" declarative Extend/Inherit the base class to create the Sub class/Child class.

###Mathematical Operators

Sass allows us to do simple mathematical operations like +, -, /, *, % etc.

### Misc

* SASS website http://sass-lang.com/.
* Compass Installation http://compass-style.org/install/

