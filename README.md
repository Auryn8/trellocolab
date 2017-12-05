# TRELLO


## Maquetar el proyecto

## Crear HTML

1. Arquitectar la estructura del proyecto

2. Enlazar documentos de estilo y javascript

3. Enlazar iconos


## Estilos CSS y SASS

1. Modificar márgenes del body

2. Establecer color de background

3. Posicionar barra de búsqueda, logo, foto de perfil e íconos en header

4. Sección uno:
    4.1 Dar estilo, color y tipo de fuente a h3 y h5
    4.2 Colocar iconos

5. Sección dos:
    5.1 Posicionar y dar estilos a casilla de texto
    5.1 Posicionar y dar estilo al botón
    
    
## Desarrollo

1. Función para ocultar elementos:

    function hideElement(a, b) { 
		 a.classList.toggle('d-create');
		 b.classList.toggle('d-create');

2. Función para generar una nueva casilla:

    function newElements(element, clase, texto, container) { 
		 var div = document.createElement(element); 
		 div.classList.add(clase); 
		 div.innerHTML = texto; 
		 container.appendChild(div); 


3. Función para crear tarjetas:

    function newForm(form, clase, container, agregarTarjeta) { 
		 var form = document.createElement(form); 
		 form.classList.add(clase);
		 newElements('textarea', 'textarea', '', form); 
		 newElements('button', 'boton', 'Añadir', form); 
		 container.appendChild(form); 
     form.lastElementChild.addEventListener('click', function(event) { 
       event.preventDefault(); 
			 agregarTarjeta.classList.remove('d-create'); 
			 form.classList.add('d-create');
			 var text = form.firstElementChild.value;
			 var div = document.createElement('div'); 
			 div.classList.add('text-cards'); 
       div.innerHTML = text; 