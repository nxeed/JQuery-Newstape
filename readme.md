JQuery Newstape
===================
Плагин для создания бегущей новостной ленты. Прост в использовании, поддерживает mousewheel и event.drag.

Установка
-------------
Подключение скриптов
``` html
<script src="путь к jquery"></script>
<!-- Если используете -->
<script src="путь к jquery.mousewheel"></script>
<!-- Если используете -->
<script src="путь к jquery.event.drag"></script>

<script src="путь к jquery.newstape"></script>
```
Пример разметки
``` html
<div class="newstape">
    <div class="newstape-content">
        Содержимое новостной ленты
    </div>
</div>
```
Пример стилей
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
Инициализация
``` html
<script>
    $(function() {
        var newstapes = $('.newstape').newstape();
    });
</script>
```
Настройка
-------------
``` html
<script>
    $(function() {
        var newstapes = $('.newstape').newstape({
            // период срабатывания таймера
            period: 30, 
            // на сколько пикселей смещается лента
            offset: 1, 
            // разрешить прокрутку колёсиком
            mousewheel: true, 
            // разрешить "таскать" ленту
            dragable: true, 
            // на сколько пикселей происходит смещение при прокрутке колёсиком
            mousewheelRate: 30, 
            // разрешить отслеживать изменение высоты контента
            // (пригождается, если у вас на сайте изменяется размер шрифта)
            heightSpy: true
        });
    });
</script>
```
