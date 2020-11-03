# Emmet Abbreviations <!-- omit in toc -->

[Find Me Here](https://www.linkedin.com/in/kaustavthakur/)

Emmet Abbreviations provide shorthand syntax for writing html code at super fast speed. Abbreviations are the heart of the Emmet toolkit: these special expressions are parsed in runtime and transformed into structured code block, HTML for example. 

The abbreviation’s syntax looks like CSS selectors with a few extensions specific to code generation. The following document showcases important examples for practical uses. I have used VS Code as the IDE for this.  


### Table of Contents <!-- omit in toc -->
- [Boilerplate Generation](#boilerplate-generation)
- [CSS ID](#css-id)
- [CSS Class](#css-class)
- [Concatenating CSS Classes](#concatenating-css-classes)
- [Nesting Child](#nesting-child)
- [Siblings](#siblings)
- [Combining Child & Siblings](#combining-child--siblings)
- [Multiplying Elements](#multiplying-elements)
- [Text inside Elements](#text-inside-elements)
- [Auto Numbering](#auto-numbering)
- [Grouping Elements](#grouping-elements)
- [Dummy Text](#dummy-text)

## Boilerplate Generation
Pressing ```!``` generates html boilerplate code
```html 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html> 
```
## CSS ID
Typing ``` div#id ``` and pressing ```Enter``` generates the following code.
```html
<div id="id"></div>
```
## CSS Class
Typing ``` div.single-class ``` and pressing ```Enter``` generates the following code.
```html
<div class="single-class"></div>
```
## Concatenating CSS Classes
Multiple CSS classes are joined using the ```.``` operator.Typing ``` div.multiple.classes.concatenated ``` and pressing ```Enter``` generates the following code.
```html
<div class="multiple classes concatenated"></div>
```

## Nesting Child
Child classes are nested using the ```>``` operator. To generate the following code:
```html
<div class="child">
    <ul class="nesting">
        <li></li>
    </ul>
</div>
```
Type ``` div.child>ul.nesting>li ``` and press ```Enter```

## Siblings
Siblings are generated using the ```+``` operator. To generate the following code:
```html
<div id="sibling"></div>
<h2 class="heading"></h2>
<h3></h3>
```
Type ``` div#sibling+h2.heading+h3 ``` and press ```Enter```.

## Combining Child & Siblings
To generate the following code:
```html
<div></div>
<div>
    <p><span></span><strong></strong></p>
</div>
```
Type ``` div+div>p>span+strong ``` and press ```Enter```.

## Multiplying Elements
To generate similar multiple elements, use the ``` * ``` operator followed by the number of elements. To generate the following code:
```html
<div>
    <ul>
        <li><a href=""><strong></strong></a></li>
        <li><a href=""><strong></strong></a></li>
    </ul>
</div>
```
Type ``` div>ul>li*2>a>strong ``` and press ```Enter```. Note that any element after the multiplied element also gets multiplied. Here ```a href``` and ```strong``` got multiplied.

## Text inside Elements
To add text inside elements, use the ``` {} ``` braces operator with the text placed inside. To generate the following code:
```html
<h4>Text Inside</h4>
<h4>Text Inside</h4>
```
Type ``` h4{Text Inside}*2 ``` and press ```Enter```.

## Auto Numbering
To add auto numbering to class names & text, use the ``` $ ``` operator before or after the text. To generate the following code:
```html
<div>
    <ul>
        <li class="item1"></li>
        <li class="item2"></li>
        <li class="item3"></li>
    </ul>
</div>
```
Type ``` div>ul>li.item$*3 ``` and press ```Enter```. To continue numbering, use the ```$@``` operator followed by the number. To generate the following code:
```html
<div>
    <ul>
        <li class="item4"></li>
        <li class="item5"></li>
    </ul>
</div>
```
Type ``` div>ul>li.item$@4*2 ``` and press ```Enter```. Let us combine the above and also auto increment text inside elements. To generate the following code:
```html
<div>
    <ul>
        <li><a href=""><strong>Click Me 1</strong></a></li>
        <li><a href=""><strong>Click Me 2</strong></a></li>
    </ul>
</div>
```
Type ``` div>ul>li*2>a>strong{Click Me $} ``` and press ```Enter```.

## Grouping Elements
To group elements of different hierarchy, use the ``` () ``` braces operator. To generate the following code:
```html
<div>
    <ul>
        <li class="item1"><a href="">Text 1</a></li>
        <li class="item2"><a href="">Text 2</a></li>
    </ul>
</div>
<div>
    <p><span><em></em></span></p>
</div>
<blockquote></blockquote>
<div></div>
```
Type ``` (div>ul>li.item$*2>a{Text $})+(div>p>span>em)+bq+div ``` and press ```Enter```.

## Dummy Text
To generate dummy lorem ipsum text, use the ``` lorem<number of words> ``` keyword. To generate the following code:
```html
<p>Lorem ipsum dolor sit amet.</p>
<p>Aperiam harum suscipit quis voluptatibus.</p>
```
Type ``` p*2>lorem5 ``` and press ```Enter```. To generate dummy text inside lists:
```html
<ul class="hello">
    <li class="world">Lorem, ipsum.</li>
    <li class="world">Nisi, sit.</li>
</ul>
```
Type ```  ul.hello>li.world*2>lorem2 ``` and press ```Enter```.