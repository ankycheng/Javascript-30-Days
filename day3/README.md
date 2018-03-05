# 30 Days Javascript - Day3 CSS Variable


### Goals:
1. Set CSS Variables
2. Change CSS Variables through `change` & `mouseover` events.


### Notes:
1. [`:root`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:root)

   ```
   <style>
        :root {
         --base: #ffc600;
         --spacing: 10px;
         --blur: 10px;
       }
   ``` 

2. [CSS3 :root Selector](https://www.w3schools.com/cssref/sel_root.asp)
    
    ```
    <style>
    :root {
     --base: #ff6c00;
     --spacing: 10px;
     --blur: 10px;
    }
    </style>
    
    <script>
        document.documentElement.style.setProperty(`--${this.name}`, this.value);
    </script>
    ```


3. `var(--xxx)`：CSS 变量（[CSS Variables](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Using_CSS_variables)）
    
    ```
    <style>
    element {
        --main-bg-color: brown;
    }
    element {
      --main-bg-color: brown;
    }
    </style>
    
    <script>
        element.style.setProperty('--main-bg-color', 'brown');
    </script>
    ```
    
3. [`filter: blur()`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/filter)
4. `change`、`mousemove` events
5. Difference between `NodeList` and `Array`
  
#### Reference:
[Flat Clock on Codepen](https://codepen.io/josephshambrook/pen/FlhcJ?q=flat+clock&limit=all&type=type-pens) : Better CSS positioning
[Momentjs](https://momentjs.com/)

