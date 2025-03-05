# Apuntes-Tercera-Semana
Apuntes control de movimiento - Primer corte-Tercera Semana
# MOTORES, SENSORES Y DRIVERS
En esta clase, se habló de los tipos de motores existente en la industria, las diferencias entre sí y las características partículares de cada uno. Adicionalmente como desde SimScape - Matlab podemos hacer una validación de modelo del motor con el que queramos trabajar, esto desde ciertos parametros que nos entregan los fabricantes. 

## 1. MOTORES
Se veran los tipos de motores que existen en la industria.

>🔑 *Motores DC:* Los motores DC o motores de corriente continua, son dispositivos electromecánicos capaces de convertir energía eléctrica en energía mecánica.
>
>🔑 *Motores AC Asíncrono:* También conocidos como motores de inducción, son motores que funcionan con corriente alterna (AC), pero al ser asíncronos la velocidad de rotación no es igual a la velocidad del campo magnéticos del estator. 
>
>🔑 *Motores AC Síncrono:* Son motores que funcionan con corriente alterna (AC), pero al ser asíncronos la velocidad de rotación es exactamente igual a la velocidad del campo magnéticos del estator, esto hace que no haya deslizamiento, osea que el rotor gira en síncronica con el campo magnético del estator.
>
>🔑 *Servomotores:* Se asocia a un sistemas que es capaz se seguir referencias, es decir que sigue cambios en determinado tiempo, estas referencias pueden llegar a ser de posición, velocidad o torque mediante un sistema de control.

### 1.1. Motores Corriente Continua
Estos motores contienen las siguientes caracteristicas fisicas:
* Estator: El devanado inductor genera el campo magnético de excitación. Está compuesto por una corona de material ferromagnético (culata) con polos en su interior, alrededor de los cuales se enrollan los devanados de excitación que crean el campo magnético al circular corriente.
* Rotor: Está constituido por una pieza cilíndrica ranurada de material ferromagnético, donde se aloja el devanado inducido cerrado en las ranuras del rotor.
* Colector de Delgas: Es un conjunto de láminas de cobre aisladas entre sí que giran con el rotor y están conectadas eléctricamente a las bobinas del devanado inducido, permitiendo su conexión al exterior.
  
En cuestiones industriales estos tipos de motores tienen varias aplicaciones, por lo que podemos resaltas las siguientes ventajas y desventajas:

| **Ventajas**  | **Desventajas** |
|---------------|-----------------|
|• Control más simple
• Driver de potencia más simple
• Bajo precio en bajas capacidades
• Alta eficiencia en aplicaciones pequeñas      | • Requiere mantenimiento e inspección periódicas
• No se usa en entornos limpios debido a la abrasión de las escobillas
• No se puede utilizar para altos torques
• Sus imanes pueden sufrir desmagnetización con el tiempo              |

Tabla 1. Motores DC

### 1.2. Motores Corriente Alterna - Asíncronos
Estos motores contienen las siguientes caracteristicas fisicas:
* Estator: El devanado inductor genera el campo magnético de excitación. Está compuesto por una corona de material ferromagnético (culata) con polos en su interior, alrededor de los cuales se enrollan los devanados de excitación que crean el campo magnético al circular corriente.
* Rotor: Está constituido por una pieza cilíndrica ranurada de material ferromagnético, donde se aloja el devanado inducido cerrado en las ranuras del rotor.
* Colector de Delgas: Es un conjunto de láminas de cobre aisladas entre sí que giran con el rotor y están conectadas eléctricamente a las bobinas del devanado inducido, permitiendo su conexión al exterior.
  
En cuestiones industriales estos tipos de motores tienen varias aplicaciones, por lo que podemos resaltas las siguientes ventajas y desventajas:

| **Ventajas**  | **Desventajas** |
|---------------|-----------------|
|• Control más simple
• Driver de potencia más simple
• Bajo precio en bajas capacidades
• Alta eficiencia en aplicaciones pequeñas      | • Requiere mantenimiento e inspección periódicas
• No se usa en entornos limpios debido a la abrasión de las escobillas
• No se puede utilizar para altos torques
• Sus imanes pueden sufrir desmagnetización con el tiempo              |

Tabla 2. Motores AC Asíncronicos

### 1.3. Motores Corriente Alterna - Síncronos

## 2. SENSORES
Se analizarán algunos tipos de sensores que existen, especialmente los encoder u otros sensores que nos permitan hacer mediciones de pulsos de un motor.
## 3. DRIVERS
Los drivers se estudian como parte escencial

## 5. Ecuaciones
Para la edición de ecuaciones debe utilizar la etiqueta '$$' al comienzo y final de la ecuación para que la ecuación quede centrada ocupando una línea. Si se quiere que la ecuación quede integrada en el texto debe utilizar la etiqueta '$' al comienzo y final de la ecuación. Las ecuaciones pueden ser editadas utilizando el código LATEX, en el siguiente enlace encuentran un editor de ecuaciones que les genera el código. http://www.alciro.org/tools/matematicas/editor-ecuaciones.jsp . Sin embargo hay muchas otras herramientas que pueden utilizar para esto.

💡**Ejemplo 1:** si se va a representar la ecuación de la ley de Ohm se puede mostrar así $R=\frac{V}{I}$ o también,

$$R=\frac{V}{I}$$

## 6. Figuras
Todas las figuras que incluya deben ser generadas por ustedes, **no utilizar las figuras de las presentaciones**. Para incluir figuras puede seguir los siguientes pasos:
* Primero escribimos ![]().
* Después escribimos, dentro de los corchetes, el texto alternativo. Este es opcional y solo entra en acción cuando no se puede cargar la imagen correctamente.
* Después escribimos, dentro de los paréntesis, la ubicación del archivo (ya sea una url o una ubicación dentro de algun folder local). Se recomienda poner las imágenes en una carpeta que se llame imágenes dentro del repositorio github para que no tengan problemas al cargar las imágenes.

💡**Ejemplo 2:**

![Figura de prueba](images/plantilla/Captura2.PNG)

Figura 1. Figura de prueba

Incluya la respectiva etiqueta a modo de descripción de la figura y mantenga numeración consecutiva para todas las figuras de la clase.


## 9. Ejercicios
Deben agregar 2 ejercicios con su respectiva solución, referentes a los temas tratados en cada una de las clases. Para agregar estos, utilice la etiqueta #, es decir como un nuevo título dentro de la clase con la palabra 'Ejercicios'. Cada uno de los ejercicios debe estar numerado y con su respectiva solución inmediatamente despues del enunciado. Antes del subtitulo de cada ejercicio incluya el emoji 📚

## 10. Conclusiones
Agregue unas breves conclusiones sobre los temas trabajados en cada clase, puede ser a modo de resumen de lo trabajado o a indicando lo aprendido en cada clase

## 11. Referencias
Agregue un subtítulo al final donde pueda poner todas las referencias consultadas incluyendo el origen o fuente de los ejercicios planteados. Tambien dentro del texto referencie los textos o artículos consultados y las figuras y tablas dentro de la explicación de las mismas.
