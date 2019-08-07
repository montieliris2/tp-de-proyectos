<!DOCTYPE html>
<html>
<meta charset="utf-8">
<head>

    <style>

        h1 {
            font-size: 40px;
            color: #000;
            font-family: 'Open Sans';
        }
        ul {
            padding:0px;
        }
       
        li {
            list-style-type: none;
            position: relative;
            margin: 3.5px;
            padding: 0.5em 0.5em 0.5em 2em;
            background: #C0C0C0;
            font-family: sans-serif;
        }
 
        li div {
            display:none;
            float:right;
        }
 
        li div span {
            margin-left:10px;
            background-color:#808080;
            padding:3px 8px;
            border-radius: 8px;
            color:#fff;
            cursor:pointer;
        }
 
        li:hover div {display:inline;}
 
        li.ok {
            background: #CCFF99;
        }

        li.ok::before {
            content: '';
            position: absolute;
            border-color: #009933;
            border-style: solid;
            border-width: 0 0.3em 0.25em 0;
            height: 1em;
            top: 1.3em;
            left: 0.6em;
            margin-top: -1em;
            transform: rotate(45deg);
            width: 0.5em;
        }
 
        li.ko {
            background: #FF9999;
        }

        li.ko::before {
            content: 'X';
            position: absolute;
            font-size:1.3em;
            font-weight:bold;
            color: #990000;
            height: 1em;
            top: 1.3em;
            left: 0.4em;
            margin-top: -1em;
            width: 0.5em;
        }
    </style>

</head>
<body>

<h1>Lista de tareas</h1>
<ul>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
  <li> <input type="text" size="35" maxlength="50" value="Agregar tarea" name="caja de texto"> <div><span class="ok">Seleccionar</span><span class="ko">Eliminar</span></div></li>
</ul>
<script>
var list = document.querySelector('ul');
 
list.addEventListener('click', function(ev) {
    if(ev.target.className == 'ok')
    {
        ev.target.parentNode.parentNode.classList.remove('ko');
        ev.target.parentNode.parentNode.classList.toggle('ok');
    }else if(ev.target.className == 'ko'){
        ev.target.parentNode.parentNode.classList.remove('ok');
        ev.target.parentNode.parentNode.classList.toggle('ko');
    }
}, false);
 
</script>
</body>
</html>
