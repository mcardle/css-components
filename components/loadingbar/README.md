#Loading bar

## The HTML

This is a loading bar made in raw css, with flexbox and animations. The html is very simple, so you could just create it as-is or you could include it in your project using server side.

With HTML:
```
<div class="LoadingBar">
    <div class="LoadingBar__item LoadingBar__first"></div>
    <div class="LoadingBar__item LoadingBar__second"></div>
    <div class="LoadingBar__item LoadingBar__third"></div>
    <div class="LoadingBar__item LoadingBar__forth"></div>
</div>
```

With PHP:
```
<?php include('/loadingbar/index.html'); ?>
```

With ASP:
```
<!-- #include file="/loadingbar/index.html" -->
```

With JSP:
```
<%@include file="/loadingbar/index.html" %>
```

## The CSS convention

The reason it is created with some long class names are because it is following a convention called BEM and you can read more here:
[BEM Naming](http://getbem.com/naming/ Read about the BEM convention)
 
- As a side note I follow [Jeffrey Way](https://github.com/JeffreyWay)'s naming convention with a capital letter for the blocks. 

## Including the styling 

To get it to work, include the css file LoadingBar.css in the head of your html document, like this:

```
<link href="loadingbar/LoadingBar.css" rel="stylesheet">
```

Now you can toggle the visibility by either css or js, by toggling the display none/block attribute.

## Color schemes

If you want to apply a little color on it, you could include one the schemes provided or create your own. To include a provided scheme, simply include the desired scheme like you included the LoadingBar.css
```
<link href="loadingbar/LoadingBar.css" rel="stylesheet">
<link href="loadingbar/LoadingBar--color-scheme-solid-black.css" rel="stylesheet">
```

The following schemes are available:
```
<link href="loadingbar/LoadingBar--color-scheme-solid-black.css" rel="stylesheet">
<link href="loadingbar/LoadingBar--color-scheme-solid-white.css" rel="stylesheet">
<link href="loadingbar/LoadingBar--color-scheme-solid-red.css" rel="stylesheet">
<link href="loadingbar/LoadingBar--color-scheme-solid-green.css" rel="stylesheet">
<link href="loadingbar/LoadingBar--color-scheme-solid-blue.css" rel="stylesheet">
<link href="loadingbar/LoadingBar--color-scheme-solid-google.css" rel="stylesheet">
```

If you would like to create your own, simply create a new css file or edit the LoadingBar.css (not recommended) and paste in the following:

Solid color
```
.LoadingBar__first,
.LoadingBar__second,
.LoadingBar__third,
.LoadingBar__forth{
	    background-color: #8a2be2;
}
```

or if you would like to create four different colors:
```
.LoadingBar__first{
    background-color: #b23aee;
}
.LoadingBar__second{
    background-color: #9932cd;
}
.LoadingBar__third{
    background-color: #7a378b;
}
.LoadingBar__forth{
	    background-color: #820bbb;
}
```

It is possible to set the height and width and it is still centeret.

Just open the LoadingBar.css and find the .LoadingBar class and set the with and height.
```
.LoadingBar{
  display: flex;
  align-items: center;
  width: 160px; /* REMOVE THIS */
  
  width: 500px; /* ADD THIS */
  height: 350px; /* ADD THIS */
}
```