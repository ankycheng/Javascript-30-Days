# Notes:

### Steps
#### Step1. Adding keydown listener
Using `window.addEventListener('keydown', playSound);`
</br>

#### Step2. Build function `playSound`
1. Get audio tag and div tag by `e.keyCode`
2. See if `e.keyCode` has an audio tag, `return` if not
3. add `playing` class if the div has an audio tag
4. Set `audio.currentTime = 0`
5. Play audio
</br>

#### Step3. Add transitionend listener
Search all elements that `className='key'`, and when `transitionend`, trigger removeTransition


#### Step4. Build function `removeTransition`
See if propertyName is transform, quit if not. If the propertyName is transform, remove `playing`.
</br>
### Learnings

#### 1. `const` 

[MDN: `const` ](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)
> Constants are block-scoped, much like variables defined using the let statement. The value of a constant cannot change through re-assignment, and it can't be redeclared.

[JavaScript ES6+: var, let, or const?](https://medium.com/javascript-scene/javascript-es6-var-let-or-const-ba58b8dcde75):
> This is why I favor `const` over `let` in ES6. In JavaScript, `const` means that the identifier can’t be reassigned. (Not to be confused with immutable values. Unlike true immutable datatypes such as those produced by Immutable.js and Mori, a `const` object can have properties mutated.)

#### 2. `${expression}`

[MDN: Template_literals()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)
> Template literals are enclosed by the back-tick (` `)  (grave accent) character instead of double or single quotes. Template literals can contain placeholders.

    Ex:
    
    ``` let str = '<div data-key="' + key + '">' +
             '<button>click me</button>' +
             '</div>'; ```
    vs.
    
    ``` let str = `<div data-key="${key}">
             <button>click me</button>
             </div>`; ``` 

#### 3. [The Window Object](https://www.w3schools.com/jsref/obj_window.asp)

#### 4. [DOM Document Object](https://www.w3schools.com/jsref/dom_obj_document.asp)
* [`document.querySelector()`](https://www.w3schools.com/jsref/met_document_queryselector.asp) 找到第一個符合指定CSS selector(s)的HTML節點
* [`document.querySelectorAll()`](https://www.w3schools.com/jsref/met_document_queryselectorall.asp) 找到符合指定CSS selector(s)的HTML節點們
* querySelectorAll返回的是NodeList object 且 NodeList object 與Array不同 [ref: nodelists vs arrays](https://gomakethings.com/nodelists-vs-arrays/)

#### 5.[ DOM Element Object](https://www.w3schools.com/jsref/dom_obj_all.asp)

#### 6. [HTML DOM Node Lists](https://www.w3schools.com/js/js_htmldom_nodelist.asp)
* `NodeList.forEach()`
* querySelectorAll()出來的物件都是NodeList，它不是Array，能使用的方法不同，在此使用forEach()走訪每一個元素。 

    參考: [Array.forEach](https://www.w3schools.com/jsref/jsref_forEach.asp) & [MDN-Array.prototype.forEach()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)


#### 7. `selector.classList.add('')` &  `selector.classList/remove('')`

#### 8. `data-key`
*  data-key屬性是無法在網上搜索到的，這是一個自定義屬性，如果沒有合適的屬性可以定義該數據，就可以通過data-*的方式自定義頁面的數據。

#### 9. Arrow Function [(Lambda)](http://www.jollen.org/blog/2013/10/javascript-lambda.html)
anonymous Function

`funtion (key) {
  key.addEventListener('transitionend', removeTransition);
}`
vs.
`key => key.addEventListener('transitionend', removeTransition)`

