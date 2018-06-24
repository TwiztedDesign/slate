---
title: Videoflow Framework API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - javascript

toc_footers:

includes:

search: true
---

# Introduction

Welcome to the Videoflow framework (or VFF ) API.

vff is a JavaScript library designed to create graphic overlays for the Videoflow Player.


# Core

## addTemplate
```javascript
var myData = {};
vff.addTemplate(myData);
```
Register the object as a template in VFF

## getPages
```javascript

vff.getPages();
```
Get all the project pages (for now, mainly used to build home screen overlays)

## onUpdate

### unused

## getQueryParams
```javascript
vff.getQueryParams();
```
Get the project query params (can’t use window.location.search because the overlay can be opened in an iframe)

## send
### unused
## request
### unused
## extend
```javascript
vff.extend(name, extension)
```
Extend the vff global object
## define
```javascript
vff.define(name, element)
```
Define a vff custom element  
Name - string - element name should be at least two words, dash separated (i.e vff-telestrator) **should consider auto “vff-” prefix

## emit
```javascript
vff.emit(payload);
```
Emit gfx event to all open players **no fully working yet
## onEvent
```javascript
vff.onEvent(template, cb, options)
vff.onEvent(cb, options)
```

# Player control

## go
```javascript
vff('pagename', timecode)
```
Go to page

* target - ***string*** - target page name
* timecode - ***int*** - ***optional*** - target time if the target page is video



## next
## previous
## home

# Visibility

## show
```javascript
vff.show(template)
```
Set “visibility” property in the template to true

* template - _string_ - the name of the template

## hide
```javascript
vff.hide(template)
```
Set “visibility” property in the template to false

* template - _string_ - the name of the template

## toggle
```javascript
vff.toggle(template)
```
Toggle “visibility” property in the template

* template - _string_ - the name of the template

# Globals

## isMobile

## isController
