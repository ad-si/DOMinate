# DOMinate

---

**THIS PROGRAM IS DEPRECATED AND NO LONGER ACTIVELY MAINTAINED.**

**Check out its successor [Shaven](http://shaven.ad-si.com/) instead.**

---

A DOM building utility and Template engine build upon JsonML with syntax sugar.


```javascript
	DOMinate(
		[document.body,
			['h1#logo', 'Static Example', {style:'color:blue'}],
			['p','some example text'],
			['ul#list.bullets'},
				['li', 'item1'],
                ['li.active', 'item2'],
                ['li',
                    ['a', 'item3', {href: '#'}]
                ]
			]
		]
	);
```

compiles to

```html
	<body>
		<h1 id="logo" style="color:blue">Static Example</h1>
		<p>some example text</p>
		<ul id="list" class="bullets">
			<li>item1</li>
			<li class="active">item2</li>
			<li><a href="#">item3</a></li>
		</ul>
	</body>
```


## Versions
DOMinate is available in two versions, which are based on each other.

### Essential
- 242 bytes
- Contains the basic functionality
- Attempt to build the shortest JsonML parser possible
- For projects where every byte counts

### Standard
- 0.6k bytes
- Contains all the functionality
- Syntax Sugar for ids and classes
- Support for namespaces. (Lets you build SVGs and other XML based languages)
- Callback functions on elements
- Returns a Object containing the root element and the elements with an id

**Check out the examples folder for more in-depth examples**
