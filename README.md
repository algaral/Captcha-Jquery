<h5>Captcha-Jquery diseñado y desarrollado por Bianca Conde y Alfonso Garcia en Saregune </h5>

  Como todos sabéis, en ocasiones es necesario saber si lo que está interactuando con nuestra web es una persona, normalmente para el tema de recibir mails con sugerencias, opiniones o algún test, todos sabemos que a veces se mandan masivamente desde programas. Para evitar esto, he implementado lo que podriamos denominar un "captcha", el cual consiste en mover una imagen dentro de otra.

Si os fijáis en el php adjunto, el llamdao "cat_captcha.php", en la parte del estilo, están añadidas dos imágenes. Una que es la que permanecerá fija en nuestra web, en nuestro caso la casita, y otra que es la que se moverá, en nuestro caso el gato. Podríamos cambier esas imágenes por otras dos cualesquiera, teniendo en cuenta la anchura y altura de las imágenes, las cuales se pueden modificar cambiendo las propiedades width y height en la parte del estilo.

También se pueden personalizar el texto que nos aparece al principio y el cual nos indica que hay que hacer, en nuestro caso mover el gatito dentro de la casita, modificando el valor de la variable "v_txt_instrucciones"

Al pulsar en el botón "Comprobar", si el gato no está totalmente dentro de la casa nos mostrará un mensaje indicandolo. Ese mensaje se puede modificar cambiando el valor de la variable "v_txt_error". Tener en cuenta que este texto debe de ir dentro de las etiquetas de un párrafo de html.

