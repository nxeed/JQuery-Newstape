JQuery Newstape
===================
A plugin to create a running news feed. Easy to use, supports mousewheel and event.drag.

Usage
-------------
Scripts
``` html
<script src="path to jquery"></script>
<!-- If you use "mousewheel" option -->
<script src="path to jquery.mousewheel"></script>
<!-- If you use "dragable" option -->
<script src="path to jquery.event.drag"></script>

<script src="path to jquery.newstape"></script>
```
Markup
``` html
<div class="newstape">
    <div class="newstape-content">
        Content
    </div>
</div>
```
Styles
``` css
.newstape {
    height: 400px;
    overflow: hidden;
}

.newstape-content {
    position: relative;
    padding: 15px;
}

.newstape-drag {
    cursor: ns-resize;
}
```
Initialization
``` html
<script>
    $(function() {
        var newstapes = $('.newstape').newstape();
    });
</script>
```
Settings
-------------
``` html
<script>
    $(function() {
        var newstapes = $('.newstape').newstape({
            // timer period
            period: 30, 
            // offset pixel count
            offset: 1, 
            // mousewheel scroll
            mousewheel: true, 
            // mousewheel offset pixel count
            mousewheelRate: 30, 
            // dragging tape content
            dragable: true
        });
    });
</script>
```
