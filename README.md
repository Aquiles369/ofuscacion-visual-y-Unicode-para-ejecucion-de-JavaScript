<h1 align="center"><img height="40" src="https://github.com/Aquiles369/iconos/blob/main/img/lobo1.gif"><img height="40" src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExNWx4YTl1dW9scXlqZDk2cTdyY2VvcXQwMG40OGoxY25rZzV0MDZhcCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/peSyJWjNTRfzaWh49M/giphy.gif">"Ofuscación visual y Unicode para ejecución de JavaScript."<img height="40" src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExNWx4YTl1dW9scXlqZDk2cTdyY2VvcXQwMG40OGoxY25rZzV0MDZhcCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/peSyJWjNTRfzaWh49M/giphy.gif"><img height="35" src="https://github.com/Aquiles369/iconos/blob/main/img/lobo1.gif"> </h1>	


<br>


<p align="center">
 <img  height="470rem" alt="GIF" src="https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExZHo0aWY5Z2I2NjZ4Z2xuOW1tdjk1aWdqdGlrbDhja3h1cHNqOXZiYSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bGgsc5mWoryfgKBx1u/giphy.gif"/>
</p>

<picture> <img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">  </picture>


### <picture> <img src = "https://media.giphy.com/media/v1.Y2lkPWVjZjA1ZTQ3NW5sZ2g4dmhnc3k4M2pjMGlubXl1Njk5eGZ1MmI1b2k5ZDVid29hOSZlcD12MV9zdGlja2Vyc19yZWxhdGVkJmN0PXM/1dPKqD8HqzmfxEUzzZ/giphy.gif" width = 75px> Ofuscación visual y Unicode para ejecución de JavaScript.  </picture> 

<br>

Catálogo técnico interactivo para analizar el uso de Unicode en ejecución real de JavaScript y su diferencia con la ofuscación visual aplicada a seguridad web. Enfocado en cómo distintos bloques Unicode se comportan bajo parsers HTML y motores ECMAScript, y cómo discrepancias entre WAF, backend y runtime pueden generar interpretaciones divergentes del mismo identificador o token.<br><br>

Incluye análisis práctico de validez sintáctica según especificación ECMAScript, comportamiento de identificadores Unicode, homoglifos funcionales vs no funcionales y diferencias entre apariencia visual y semántica real dentro del pipeline (input → WAF → backend → runtime → navegador).<br><br>

Proyecto en investigación activa. El contenido evoluciona conforme se validan nuevos escenarios de parsing y ejecución bajo distintos bloques Unicode. 
<br><br> 


<br>
<picture> <img src="https://user-images.githubusercontent.com/74038190/212284115-f47cd8ff-2ffb-4b04-b5bf-4d1c14c0247f.gif" width ="1050" > </picture>
<br>

### <picture> <img src = "https://media.giphy.com/media/v1.Y2lkPWVjZjA1ZTQ3NW5sZ2g4dmhnc3k4M2pjMGlubXl1Njk5eGZ1MmI1b2k5ZDVid29hOSZlcD12MV9zdGlja2Vyc19yZWxhdGVkJmN0PXM/2z956IUc3J0noEOXUL/giphy.gif" width = 75px>  </picture> Problema que resuelve<br><br>
**Cuando auditás aplicaciones web, muchos asumen que cualquier carácter Unicode “raro” puede ejecutar JavaScript o generar bypass.<br><br>
El problema real es otro:<br><br>
• No todos los bloques Unicode son válidos para identificadores JS.<br><br>
• No todos los caracteres visualmente equivalentes son sintácticamente válidos.<br><br>
• Parsers HTML y motores JavaScript no aceptan exactamente los mismos rangos.<br><br>
• Algunos WAF bloquean por apariencia visual aunque el runtime ejecute correctamente.<br><br>
• Ofuscación visual no implica ejecución semántica.<br><br>

Esto genera:<br><br>

• Payloads que no ejecutan.<br><br>
• Bypass teóricos sin fundamento sintáctico.<br><br>
• Confusión entre homoglyph funcional y carácter inválido.<br><br>
• Ruido innecesario en pruebas ofensivas avanzadas.<br><br>

La superficie explotable no está en “usar Unicode extraño”.
Está en conocer qué bloques ejecutan realmente y cuáles solo sirven para ofuscar.<br>

<br>

<picture> <img src="https://user-images.githubusercontent.com/74038190/212284115-f47cd8ff-2ffb-4b04-b5bf-4d1c14c0247f.gif" width ="1050" > </picture>

<br>

### <picture> <img src = "https://media.giphy.com/media/v1.Y2lkPWVjZjA1ZTQ3NW5sZ2g4dmhnc3k4M2pjMGlubXl1Njk5eGZ1MmI1b2k5ZDVid29hOSZlcD12MV9zdGlja2Vyc19yZWxhdGVkJmN0PXM/LBFPLXkgoVm80dx6sP/giphy.gif" width = 75px>  </picture> Qué aporta y cómo beneficia <br><br>

<br>

• Identificación práctica de bloques Unicode funcionales para ejecución en ECMAScript.<br><br>
• Separación clara entre ejecución real y ofuscación visual.<br><br>
• Análisis basado en comportamiento real del parser, no en teoría abstracta.<br><br>
• Aplicación directa a XSS, evasión de validaciones superficiales y análisis de filtros.<br><br>
• Optimización de payloads reduciendo ruido y falsos supuestos.<br><br>

Bloques relevantes (según contexto de identificadores y compatibilidad con parsers):<br><br>

ASCII<br>
Latin-1<br>
Latin Extended (A/B/C/D/E)<br>
Greek (subconjunto compatible)<br>
Cyrillic (subconjunto compatible)<br>
Fullwidth Latin<br>
Mathematical Alphanumeric Symbols<br>
Phonetic Extensions<br>
Combining Marks (según contexto)<br>
Letterlike Symbols<br>
Super/Subscripts (limitado por parser)<br>
Enclosed Alphanumerics (contextual)<br>
Mathematical Operators (subconjunto válido)<br>



<picture> <img src="https://user-images.githubusercontent.com/74038190/212284115-f47cd8ff-2ffb-4b04-b5bf-4d1c14c0247f.gif" width ="1050" > </picture>
<br>

### <picture> <img src = "https://media.giphy.com/media/v1.Y2lkPWVjZjA1ZTQ3MjIxNW8yMXppcWo4aXoycmZ0dTR0ajE0NXZmcnd4d2xqMnphZ2g2diZlcD12MV9zdGlja2Vyc19yZWxhdGVkJmN0PXM/H3JHrs7JC6duvenDW8/giphy.gif" width = 80px>  </picture> Resumen rápido
<br><br>

No todo Unicode ejecuta.

Solo un subconjunto reducido es válido sintácticamente para JavaScript.
El resto puede ser útil para ofuscación visual, pero no altera la semántica real del runtime.

La diferencia entre apariencia y validez sintáctica define si un payload funciona o es solo ruido.

Unicode no es solo encoding.
Es conjunto de categorías formales que el parser acepta o rechaza según reglas estrictas.

La explotación aparece cuando la validación superficial y la ejecución real no coinciden.



<br>

<picture> <img src="https://user-images.githubusercontent.com/74038190/212284115-f47cd8ff-2ffb-4b04-b5bf-4d1c14c0247f.gif" width ="1050" > </picture>
<br>

### <picture> <img src = "https://media.giphy.com/media/v1.Y2lkPWVjZjA1ZTQ3YTc5YmprbXI4aTNmcWkxbXF3OWsxaHZpOTFvaDBsMWFpdnZybmNzeSZlcD12MV9zdGlja2Vyc19yZWxhdGVkJmN0PXM/r5U5hYpabekbSj0Jn8/giphy.gif" width = 80px>  </picture> Recursos oficiales utilizados
<br><br>


• https://www.unicode.org/charts/#scripts
Tablas oficiales de sistemas de escritura Unicode. Base para analizar bloques y rangos disponibles.<br><br>

• https://www.unicode.org/versions/Unicode17.0.0/
Definiciones normativas del estándar Unicode.<br><br>

• https://www.unicode.org/Public/UCD/latest/ucd/
Unicode Character Database (propiedades formales de codepoints: categorías, combinaciones, etc.).<br><br>

• https://tc39.es/ecma262/
Especificación oficial de ECMAScript (reglas formales de identificadores Unicode y sintaxis válida).<br>

<picture> <img src="https://user-images.githubusercontent.com/74038190/212284115-f47cd8ff-2ffb-4b04-b5bf-4d1c14c0247f.gif" width ="1050" > </picture>
<br>

### <picture> <img src = "https://media.giphy.com/media/v1.Y2lkPWVjZjA1ZTQ3aHo4dGYwcHBjM2pxb2djYjF4aTcxcm1udHd6dzI2MHgzNzl6enBtZCZlcD12MV9zdGlja2Vyc19yZWxhdGVkJmN0PXM/dLD88887PfEeQnmShM/giphy.gif" width = 80px>  </picture> Enfoque
<br><br>


Investigación ofensiva con base normativa, centrada en:<br>

• Reglas formales de identificadores en ECMAScript.<br><br>
• Categorías Unicode aceptadas por motores JS reales.<br><br>
• Diferencia entre apariencia visual y validez sintáctica.<br><br>
• Comportamiento práctico de parsers HTML y motores JavaScript.<br><br>
• Unicode como herramienta quirúrgica, no decorativa.<br><br>

“Analiza qué bloques Unicode son realmente válidos para ejecución en ECMAScript, identifica cómo los parsers interpretan identificadores y distingue entre ofuscación visual y ejecución semántica antes de asumir un bypass.”
 
 <br>

<picture> <img src="https://user-images.githubusercontent.com/74038190/212284115-f47cd8ff-2ffb-4b04-b5bf-4d1c14c0247f.gif" width ="1050" > </picture>
<br>

### <picture> <img src = "https://media.giphy.com/media/v1.Y2lkPWVjZjA1ZTQ3ZWViN240bnB1YnowdDU4cmRyY2dqZ2Z2YWxsMWc5YXIwYTQzdHhrYyZlcD12MV9zdGlja2Vyc19yZWxhdGVkJmN0PXM/yB0WDQ9gO20szljPbB/giphy.gif" width = 80px>  </picture> “Analiza cómo NFC, NFD, NFKC y NFKD transforman realmente el input, identifica en qué punto del pipeline se normaliza y detecta desalineaciones entre WAF, backend y runtime antes de que se conviertan en superficie explotable.”
<br>


<picture> <img src="https://user-images.githubusercontent.com/74038190/212284115-f47cd8ff-2ffb-4b04-b5bf-4d1c14c0247f.gif" width ="1050" > </picture>

