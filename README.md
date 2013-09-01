## MDitor 1.0

MDtior is a web markdown editor with preview that is extremely easy to use. :)~

## Useage

Few code works. you can use just like below :
    
### 1. simple [[demo]](http://github.pw/MDitor/demo.html)

* HTML:
    
    ```html
    <textarea id="editor" name="content"></textarea>
    ```

* Javascript:
    
    ```javascript
    <script type="text/javascript" src="mditor.min.js"></script>
    <script type="text/javascript">
        var editor = new MDitor( "#editor" ) // "#editor" is the selector of your origin textarea
    </script>
    ```

### 2. with highlight [[demo]](http://github.pw/MDitor/demo.highlight.html)

* HTML:
    
    ```html
    <link rel="stylesheet" type="text/css" href="highlight.css" />
    <textarea id="editor" name="content"></textarea>
    ```

* Javascript:
    
    ```javascript
    <script type="text/javascript" src="mditor.min.js"></script>
    <script type="text/javascript">

        var editor = new MDitor( "#editor" );
        
        editor.onPreviewMode = function( input, preview ) {
            var codes = preview.querySelectorAll("pre code");
            for (var i = codes.length - 1; i >= 0; i--) {
                hljs.highlightBlock(codes[i])
            }
        }

    </script>
    ```

### 3. custom editor style [[demo]](http://github.pw/MDitor/demo.custom.html)

* HTML:

    ```html
    <link rel="stylesheet" type="text/css" href="custom.css" />
    <textarea id="editor" name="content"></textarea>
    ```

* Javascript:

    ```javascript
    <script type="text/javascript" src="mditor.min.js"></script>
    <script type="text/javascript">
        var editor = new MDitor( "#editor" , { 
            useCustomStyle : true
        });
    </script>
    ```

### 4. custom preview markdown style [[demo]](http://github.pw/MDitor/demo.markdown.html)

just add your custom markdown style. remeber add prefix ".wmd-preview" before you style.

* HTML:

    ```html
    <link rel="stylesheet" type="text/css" href="solarized.css" />
    ```

##Don't forget 

the buttons style based on the [bootstrap2](http://getbootstrap.com/2.3.2/), so you'd better keep bootstrap's style in your html 
or you can custom them yourself by customizing editor style , this [[demo]](http://github.pw/MDitor/demo.custom.html).
