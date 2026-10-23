# Taller guiado: diseño de una experiencia de aprendizaje con asistentes de IA

Guía para el instructor. Las cuatro demostraciones diseñan la misma clase, en este orden. Cada herramienta recibe el resultado de la anterior.

1. ChatGPT arma el plan: objetivo, actividad y preguntas de evaluación.
2. Microsoft Copilot convierte ese plan en la ficha del estudiante y le cambia la forma.
3. Google Gemini aporta un dato con fuente, dos ejemplos y la misma actividad en otras dos edades.
4. Amazon Lex responde las preguntas frecuentes de esa clase y rechaza hacer la tarea.

## Objetivo

Al terminar, la audiencia ha visto una experiencia de aprendizaje completa, construida en vivo:

- **Clase:** El agua que usamos en casa.
- **Asignatura:** Ciencias.
- **Duración de la clase que se diseña:** 45 minutos.
- **Nivel base:** estudiantes de 12 a 14 años.
- **Meta:** cada estudiante nombra tres usos del agua en su casa y propone una acción concreta para reducir uno de ellos.

Las cuatro piezas que quedan son el plan, la ficha del estudiante, la misma actividad adaptada a 8–10 años y a 16–18 años, y un asistente para las dudas de esa clase.

Diga esto al empezar, y no vuelva a explicar el marco:

> Vamos a diseñar una sola clase de 45 minutos. Cada herramienta hace una parte. Al final queda el plan, el material, la versión para otras edades y un asistente para las dudas.

## Cómo seguir esta guía

- Siga los pasos en el orden escrito. No redacte prompts nuevos en la sala.
- Pegue cada prompt desde este documento.
- En cada demostración haga una sola corrección. No pida una segunda versión.
- Si un servicio no responde, muestre el respaldo de esa demostración y pase a la siguiente. No abra licencias ni configuración delante de la audiencia.
- En ningún prompt escriba nombres, correos ni datos de menores.

## Prerrequisitos

Compruebe todo el día anterior, con las mismas cuentas que va a proyectar.

### Personas

- **Instructor.** Conduce, pega los prompts y señala en pantalla lo que la audiencia debe mirar.
- La audiencia puede ser docente o diseñadora instruccional. No necesita cuenta propia.

### Equipo

- Un computador con Windows 10 o superior, enchufado a corriente.
- Proyector o pantalla. Resolución mínima 1920×1080. Con el navegador al 150 %, el texto se lee desde la última fila.
- Internet estable. El día anterior, abra las cuatro páginas con las cuentas de la demo.
- Navegador actualizado: Microsoft Edge o Google Chrome.
- Micrófono solo si la sala es grande. Lex se prueba por texto.

### Qué dejar abierto antes de empezar

Una ventana, con estas pestañas de izquierda a derecha, y la sesión ya iniciada:

1. ChatGPT: [https://chatgpt.com](https://chatgpt.com).
2. Word en la web, documento vacío guardado en OneDrive, de nombre `Ficha-agua`. Copilot visible dentro del documento.
3. Gemini: [https://gemini.google.com](https://gemini.google.com).
4. Consola de Amazon Lex V2, bot `AsistenteClaseAgua` en estado **Built**, panel **Test** abierto.
5. Este archivo, para copiar los prompts.
6. Un bloc de notas vacío llamado `entrega.txt`. Ahí se pega el objetivo y la actividad al cerrar ChatGPT. Copilot y Gemini parten de ese texto.

Cierre el correo, el chat del equipo y las notificaciones del sistema.

El archivo local está en el escritorio: `Ficha-agua.docx`. Súbalo a OneDrive y ábralo desde Word en la web. Debe llegar vacío. La ficha con texto es solo el respaldo en imagen. No la abra en Word durante la demo.

### Licencias y cuentas

Use cuentas de demostración, no una cuenta personal.

**ChatGPT**

- Cuenta en [https://chatgpt.com](https://chatgpt.com).
- Plan recomendado para la sala: **ChatGPT Plus, Team o Enterprise**. El plan gratuito sirve para ensayar y en la sala puede quedar limitado. El día anterior, envíe el prompt de la demostración 1 y confirme que responde.
- Deje seleccionado el modelo más capaz de la cuenta.
- Desactive la memoria temporal del chat, para que no mezcle otro tema.
- Basta el navegador. No hace falta la aplicación de escritorio.

**Microsoft Copilot**

Esta demostración transforma un material dentro de Word. El Copilot gratuito del navegador y el de Windows no sirven para este paso. Hace falta Copilot dentro de Word.

- Un plan de Microsoft 365 que Microsoft acepte como base de Copilot. Confirme el nombre del plan en el centro de administración el día anterior.
- La licencia **Microsoft 365 Copilot** asignada al usuario que va a proyectar. La asignación puede tardar horas en aparecer dentro de Word. Hágalo al menos un día antes.
- Word de Microsoft 365, de escritorio o en [https://www.office.com](https://www.office.com). El archivo tiene que estar en **OneDrive o SharePoint**. Un archivo solo en el computador puede no mostrar Copilot.
- El día anterior, abra `Ficha-agua` desde OneDrive, pida a Copilot una frase de prueba y luego borre esa frase. El documento de la sala queda vacío.
- El usuario de la demo tiene permiso de edición sobre ese archivo.
- Si la cuenta es educativa, use la licencia de educación que Microsoft indique para Copilot en Word. Lo que se muestra es lo mismo: generar la ficha y luego transformarla.

**Google Gemini**

- Cuenta de Google con sesión en [https://gemini.google.com](https://gemini.google.com).
- Basta el plan estándar. Si la cuenta es de **Google Workspace** o de **Workspace for Education**, el administrador tiene que haber habilitado Gemini para ese usuario. El día anterior, confirme que un prompt de prueba devuelve respuesta.
- **Gemini Advanced** no es obligatorio. Úselo solo si ya está activo en la cuenta.
- Si el plan permite consultar la web, déjelo activo. La demostración pide un dato con fuente. Si la búsqueda no está disponible, use el texto de respaldo.
- No conecte Gemini al Drive de la institución ni a cuentas de estudiantes.

**Amazon Lex**

En la sala se prueba un asistente ya construido. No se crea la cuenta, el permiso, el bot ni los intents delante de la audiencia.

- Cuenta de AWS del equipo de la demo, con un medio de pago vigente. Lex puede generar costo si se supera el nivel gratuito vigente. El día anterior, revise el precio actual de Amazon Lex V2. Esta demo solo escribe unas frases en el chat de prueba de la consola.
- Región fija. Use `us-east-1` salvo que el bot ya exista en otra. No cambie de región en la sala.
- Un usuario IAM, no la cuenta raíz, con permiso para abrir Lex, probar el bot y leer la definición. No hace falta permiso para borrar bots.
- Bot de Lex **V2**, idioma **es_US** o **es_ES**, el que haya compilado bien. Nombre: `AsistenteClaseAgua`. Solo texto. Voz desactivada.
- Última compilación en estado **Built**. Si está en **Building** o **Failed**, no entre a la sala así.
- Alias de prueba `TestBotAlias` asociado a esa versión. El panel **Test** debe abrir sin trámites extra.
- No publique el bot en una página, Slack ni WhatsApp para esta demo.

### Bot que debe existir antes de la sala

| Intent | Para qué | Lo que el estudiante preguntaría | Respuesta que debe decir el bot |
|---|---|---|---|
| `Materiales` | Qué llevar | ¿Qué tengo que llevar? | Trae tu cuaderno y un lápiz. La ficha te la entrega el docente. |
| `QueVamosAHacer` | La actividad | ¿Qué vamos a hacer en clase? | Vas a anotar tres usos del agua en tu casa y elegir uno para reducirlo. |
| `ComoMeEvaluan` | La evaluación | ¿Cómo me van a evaluar? | Entregas tres usos escritos y una acción concreta. El docente revisa que la acción se pueda hacer esta semana. |
| `FallbackIntent` | Lo que el bot no sabe | Cualquier otra frase | No tengo esa respuesta. Pregúntale al docente al empezar la clase. |

Formas de preguntar que cada intent debe reconocer:

- Materiales: `qué llevo`, `qué debo traer`, `necesito materiales`.
- QueVamosAHacer: `qué haremos`, `cuál es la actividad`, `qué vamos a hacer hoy`.
- ComoMeEvaluan: `cómo es la nota`, `qué tengo que entregar`, `cómo me evalúan`.

Compile, abra **Test** y confirme una frase de cada intent. La respuesta tiene que coincidir con la tabla.

### Respaldos

Si un servicio no responde, proyecte la imagen y lea el texto de respaldo de esa demostración. Las imágenes están en `\respaldo-demo\`:

- `01-chatgpt-plan.png` — objetivo, actividad y tres preguntas.
- `02-copilot-ficha.png` — ficha de una página.
- `03-gemini-niveles.png` — la misma actividad en dos edades.
- `04-lex-prueba.png` — las tres respuestas y la pregunta que el asistente rechaza.

Esas imágenes no son capturas del servicio. Están rotuladas como respaldo.

### Lista de comprobación

- [ ] ChatGPT abre y el prompt de la demostración 1 devuelve el plan.
- [ ] Word abre `Ficha-agua` desde OneDrive, Copilot responde una frase de prueba y el documento queda vacío.
- [ ] Gemini responde en la cuenta que se va a proyectar.
- [ ] Lex está en **Built** y las cuatro frases de prueba responden como en la tabla.
- [ ] Las cuatro imágenes están en `respaldo-demo`.
- [ ] Las pestañas quedaron abiertas y con sesión iniciada.
- [ ] El navegador está al 150 % y se lee desde el fondo de la sala.
- [ ] Notificaciones del sistema apagadas.
- [ ] `entrega.txt` existe y está vacío.
- [ ] Ningún prompt de este archivo contiene datos de un estudiante real.

## Demostración 1 — ChatGPT

**Objetivo.** El instructor obtiene el objetivo de la clase, la actividad y las preguntas de evaluación. Corrige una sola cosa, para que se vea que el plan lo decide la persona.

**Pantalla.** ChatGPT, conversación nueva, modelo más capaz.

### Paso 1. Diga de qué clase se trata

> La clase es de ciencias, 45 minutos, estudiantes de 12 a 14 años. El tema es el agua que usan en casa. ChatGPT arma el plan. Yo me quedo con una versión y la corrijo.

No muestre el historial de otras conversaciones. Pulse **Nuevo chat**.

### Paso 2. Pegue el prompt y envíe

```text
Actúa como docente de ciencias. Diseña una clase de 45 minutos.
Tema: El agua que usamos en casa.
Estudiantes: 12 a 14 años.
Grupo: 28 estudiantes. Aula con pupitres, sin laboratorio.

Devuelve solo estas cuatro partes, con estos títulos:
1. Objetivo. Una sola frase. El estudiante tiene que poder demostrarlo al final de la clase. Usa un verbo observable: nombrar, describir, proponer o comparar. No uses "comprender" ni "reflexionar".
2. Actividad. Pasos numerados, de la bienvenida al cierre, que sumen 45 minutos. En cada paso indica los minutos. Incluye 15 minutos de trabajo individual en el pupitre.
3. Preguntas de evaluación. Exactamente 3. Cada una se responde por escrito en la ficha. La tercera pide una acción que el estudiante pueda hacer en su casa esta semana.
4. Material del estudiante. Lista de lo que debe tener en la mano. Máximo 4 ítems.

Escribe en español, para que un docente lo lea en voz alta. No agregues introducción ni cierre.
```

Mientras genera, no hable de la herramienta. Señale el título **Objetivo** cuando aparezca.

### Paso 3. Lea el objetivo y corrija el verbo si hace falta

Lea en voz alta solo el objetivo.

Si el verbo ya es nombrar, describir, proponer o comparar, dígalo y siga. Si salió "comprender", "conocer" o "reflexionar", envíe solo esto:

```text
Reescribe solo el objetivo. Cambia el verbo por "describe" o "propone". Deja el resto de la respuesta igual. No expliques el cambio.
```

No pida otra versión de la actividad.

### Paso 4. Muestre la actividad y las preguntas

Señale en la actividad el tramo de trabajo individual. Lea las tres preguntas. Confirme en voz alta que la tercera pide una acción para esta semana.

Copie a `entrega.txt` solo estos dos bloques, con sus títulos:

- Objetivo
- Actividad

Ese archivo es la entrada de Copilot. Las preguntas se quedan en la pantalla de ChatGPT. Gemini no las necesita pegadas: el prompt de Gemini ya trae el objetivo y la actividad.

Pase a Word.

### Si ChatGPT no responde

Proyecte `01-chatgpt-plan.png`. Pegue este texto en `entrega.txt`, muéstrelo y diga que es el plan con el que siguen:

```text
Objetivo. El estudiante describe tres usos del agua en su casa y propone una acción para reducir uno de ellos durante esta semana.

Actividad.
1. 5 min. Saludo y pregunta: ¿en qué momento de ayer usaste agua?
2. 10 min. Puesta en común. El docente anota en el tablero cuatro usos que salgan del grupo.
3. 15 min. Trabajo individual. Cada estudiante escribe tres usos de su casa y elige uno.
4. 10 min. En parejas, se leen la acción y se dicen si se puede hacer esta semana.
5. 5 min. Cierre. Tres estudiantes leen su acción.
```

## Demostración 2 — Microsoft Copilot

**Objetivo.** El plan se convierte en la ficha que el estudiante tiene en el pupitre. Después cambia la forma de los pasos, sin redactar otra vez el contenido.

**Pantalla.** Word, documento `Ficha-agua` vacío, guardado en OneDrive, panel de Copilot abierto.

### Paso 1. Pase el plan al documento

Diga:

> El plan ya existe. Copilot lo pasa a la ficha que el estudiante escribe en clase. Luego le cambio la forma, no el contenido.

Pegue en el documento vacío, como texto normal, el objetivo y la actividad de `entrega.txt`. Copilot tiene que ver ese texto en la página.

Abra Copilot en Word.

### Paso 2. Pida la ficha

```text
Convierte el texto de este documento en una ficha de una página para el estudiante.
La ficha debe tener:
- El título: El agua que usamos en casa.
- El objetivo, en una frase, dirigido al estudiante ("Vas a...").
- Los pasos de la actividad, numerados, con los minutos.
- Un recuadro con tres líneas en blanco para que escriba tres usos del agua en su casa.
- Un recuadro con dos líneas para la acción que va a intentar esta semana.
- Al pie, la frase: Pon tu nombre solo si el docente te lo pide.

No agregues imágenes, rúbricas ni teoría. Mantén el español sencillo. Escríbelo en el documento.
```

Cuando aparezca la propuesta, pulse **Conservar** o el botón que inserte el texto en la página. Recorra con el cursor los dos recuadros en blanco. Diga que ahí escribe el estudiante, no la IA.

Si la ficha queda solo en el panel de Copilot, pulse insertar. No reescriba el prompt.

### Paso 3. Transforme los pasos

Sin borrar la ficha, envíe una sola transformación:

```text
Transforma los pasos numerados de la actividad en una lista de 5 verificaciones, cada una con una casilla para marcar. Conserva los minutos. No cambies el objetivo ni los recuadros en blanco. No alargues la ficha a más de una página.
```

Muestre el cambio: de instrucciones corridas a casillas. Diga:

> El mismo trabajo de 45 minutos. Cambió la forma en que el estudiante se guía.

No pida diapositivas, rúbrica ni traducción. Guarde el documento y pase a Gemini.

### Si Copilot no responde

No entre a licencias. Proyecte `02-copilot-ficha.png` y diga:

> La ficha tiene el objetivo en segunda persona, los cinco pasos, tres líneas para los usos y dos para la acción. La transformación deja esos pasos como casillas.

Pase a Gemini.

## Demostración 3 — Google Gemini

**Objetivo.** La misma actividad gana un dato que se puede citar, dos ejemplos concretos y una versión para otras dos edades, sin diseñar otra clase.

**Pantalla.** Gemini, chat nuevo.

### Paso 1. Diga qué va a hacer

> La ficha ya está. Gemini hace tres cosas con la misma actividad: un dato con fuente, dos ejemplos, y la actividad para otras dos edades.

### Paso 2. Pida el dato y los ejemplos

```text
Esta es una clase de ciencias de 45 minutos para estudiantes de 12 a 14 años.
Objetivo: el estudiante describe tres usos del agua en su casa y propone una acción para reducir uno de ellos esta semana.
Actividad: escribe tres usos, elige uno y propone cómo reducirlo.

Haz solo esto:
1. Un dato sobre el uso de agua en el hogar, en una frase, con la fuente y el año. Si no puedes citar una fuente verificable, escribe "sin fuente" y no inventes el organismo.
2. Dos ejemplos concretos de acciones que un estudiante de 12 a 14 años puede hacer en una casa esta semana. Cada ejemplo en una línea. No repitas "cerrar la llave" en los dos.

No des teoría. No rediseñes la clase. Español claro.
```

Lea el dato. Si la respuesta dice "sin fuente", dígales que el docente no pone en la ficha un número sin organismo. Lea los dos ejemplos y elija uno en voz alta. No vuelva a Word en este paso.

### Paso 3. Pida las dos edades

En el mismo chat:

```text
Adapta solo la actividad, no inventes otro tema.
Nivel A: estudiantes de 8 a 10 años. Máximo 4 pasos. Palabras cortas. La acción tiene que poder dibujarse.
Nivel B: estudiantes de 16 a 18 años. Mantén los 45 minutos. Pide que comparen dos usos y justifiquen cuál reducen, con una razón.
Para cada nivel escribe:
- el objetivo en una frase
- los pasos con minutos
No expliques las diferencias. Que se vean en el texto.
```

Lea solo el objetivo del nivel A y el del nivel B. Cierre con esta frase:

> A los 8 años dibujan la acción. A los 16 comparan dos usos y dan una razón. El tema no cambió.

No pida un tercer nivel ni una bibliografía. Pase a Lex.

### Si Gemini no responde

Proyecte `03-gemini-niveles.png`. Si falta el dato con fuente, diga:

> No se proyecta un número si la herramienta no trajo organismo y año. Dos acciones que sí se pueden decir: recoger en un balde el agua fría de la ducha mientras sale caliente, y usar un vaso para cepillarse en lugar de dejar la llave abierta.

Objetivos de respaldo:

- 8 a 10 años: el estudiante dibuja tres momentos en los que usa agua y marca uno que puede cuidar.
- 16 a 18 años: el estudiante compara dos usos del agua en su casa y justifica cuál va a reducir esta semana.

## Demostración 4 — Amazon Lex

**Objetivo.** Las dudas que se repiten en esta clase las responde un asistente. Lo que no sabe, lo devuelve al docente. En la sala no se entrena ni se publica el bot: se prueba el que ya tiene las respuestas de la clase.

**Pantalla.** Consola de Lex V2, bot `AsistenteClaseAgua`, panel **Test** abierto. No entre a crear intents.

### Paso 1. Diga qué se va a probar

> El estudiante ya tiene ficha y actividad. Antes de la clase pregunta lo mismo tres veces: qué llevo, qué vamos a hacer y cómo me evalúan. Ese asistente ya está armado con las respuestas de la clase que acabamos de diseñar. Ahora lo probamos como lo probaría el docente.

Señale el nombre del bot y el idioma. No abra precios ni IAM.

### Paso 2. Escriba las tres preguntas

En **Test**, una por una. Espere la respuesta y léala antes de escribir la siguiente.

1. `qué debo traer`
2. `qué vamos a hacer hoy`
3. `cómo me evalúan`

La respuesta esperada está en la tabla de prerrequisitos. Si una frase no cae en el intent, escríbala una sola vez más con la forma exacta de la tabla: `qué llevo`, `cuál es la actividad` o `qué tengo que entregar`.

Relacione cada respuesta con lo ya diseñado:

- La primera coincide con el material de la ficha.
- La segunda coincide con la actividad de la clase.
- La tercera coincide con la evaluación: tres usos y una acción de esta semana.

### Paso 3. Muestre lo que el asistente no hace

Escriba:

```text
¿me puedes hacer la tarea?
```

Tiene que caer en `FallbackIntent`: no tiene esa respuesta y manda a preguntarle al docente.

Cierre:

> El asistente cubre las dudas repetidas de esta clase. La tarea la sigue haciendo el estudiante. Lo que el bot no sabe, no lo inventa: se lo deja al docente.

No agregue un intent. No pulse **Build**. Cierre el panel Test.

### Si la consola no abre

Proyecte `04-lex-prueba.png` y lea las tres respuestas de la tabla y esta:

> No tengo esa respuesta. Pregúntale al docente al empezar la clase.

Diga la frase de cierre igual.

## Si la audiencia pregunta al final

Responda una cosa y deje el resto para después:

- Las cuatro cuentas son de demostración. Un colegio las contrata y las administra aparte. Los nombres de los estudiantes no se pegan en los prompts.
- Lex quedó probado en la consola. Publicarlo en la página del curso es otro trabajo.
- El documento `Ficha-agua` y los chats quedan como evidencia. Bórrelos de las cuentas de demostración si no se van a reutilizar.
