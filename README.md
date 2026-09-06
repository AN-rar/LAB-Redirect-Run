*Redireccionar ejecución*

Vulnerabilidad: Se filtraron datos confidenciales en el cuerpo de una respuesta de redirección intermedia.

En este laboratorio de WebVerse se uso burpsuit para mayor facilidad

Contexto: Quikpay genera URL de recibos cortos y fáciles de compartir para los comercios. 
Al visitar una de ellas, se te redirige a una página de agradecimiento por tu compra. 
Sin embargo, la redirección no es tan silenciosa como parece; 
el equipo de ingeniería olvidó eliminar algo de la respuesta intermedia.

1. Accedesmos al LAB, abrimos burpsuit.
2. En la pagina web del lab, hacemos click en link que dice: Live demo shortlink.
![Captura de pantalla 1](Captura%20de%20pantalla%202026-09-06%20175028.png)

3. Hablitamos el proxy de burpsuit y interceptamos la peticion.
![Captura de pantalla 2](Captura%20de%20pantalla%202026-09-06%20175104.png)
   
4.  La peticion la mandamos al repetear para investigarla mejor.
   
5.  Ya a en el repetear mandamos la peticion y observamos la respuesta del servidor, que nos dara la bandera.
![Captura de pantalla 3](Captura%20de%20pantalla%202026-09-06%20175138.png)

Conclusion: Lo que paso aqui es que hubo una fuga de informacion por comentarios de desarrolladores, es algo muy comun y que hasta el dia de hoy sigue pasando
