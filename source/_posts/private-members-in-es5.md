title: Private members in ES5
date: 2015-06-30
categories: [ software ]
tags: 
	- javascript
	- private
---

For my first post, to try out hexo, I'll succinctly show how to define a private
member in a constructor function.

In the sample code below, a consumer creates a new `C` and can only invoke `getCallCount()`
on that object. But it can never change the value of the _private_ `callCount`

```
function C() {
	
	var callCount = 0;

	this.getCallCount = function(){
		return ++callCount;
	}
}
```

A consumer can get (and effectively increment) the value of `callCount` but never modify it.