# Apuntes-Tercera-Semana
Apuntes control de movimiento - Primer corte-Tercera Semana
# MOTORES, SENSORES Y DRIVERS
En esta clase, se habló de los tipos de motores existente en la industria, las diferencias entre sí y las características partículares de cada uno. Adicionalmente como desde SimScape - Matlab podemos hacer una validación de modelo del motor con el que queramos trabajar, esto desde ciertos parametros que nos entregan los fabricantes. 

## 1. MOTORES
Son dispositivso que convierten la energía eléctrica en energía mecánica a través de la interacción de campos magnéticos, esto mediante el paso de corriente eléctrica por un devanado, generando un campo magnético que induce el movimiento de un rotor. Se utilizan ampliamente en maquinaria industrial, electrodomésticos, vehículos eléctricos y sistemas automatizados, debido a su eficiencia, precisión y facilidad de control. 

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

| **Ventajas**                                 | **Desventajas**                                                           |
|----------------------------------------------|---------------------------------------------------------------------------|
| • Control más simple                         | • Requiere mantenimiento e inspección periódicas                          |
| • Driver de potencia más simple              | • No se usa en entornos limpios debido a la abrasión de las escobillas    |
| • Bajo precio en bajas capacidades           | • No se puede utilizar para altos torques                                 |
| • Alta eficiencia en aplicaciones pequeñas   | • Sus imanes pueden sufrir desmagnetización con el tiempo                 |

Tabla 1. Motores DC

### 1.2. Motores Corriente Alterna - Asíncronos
El motor funciona mediante un campo magnético giratorio generado en el devanado inductor del estator. Al atravesar el devanado del rotor, induce fuerzas electromagnéticas que generan corrientes, provocando una reacción que hace girar el motor a una velocidad inferior a la de sincronismo.
  
En cuestiones industriales estos tipos de motores tienen varias aplicaciones, por lo que podemos resaltas las siguientes ventajas y desventajas:

| **Ventajas**                                 | **Desventajas**                                                           |
|----------------------------------------------|---------------------------------------------------------------------------|
| • Poco mantenimiento                         | • Baja eficiencia en aplicaciones pequeñas                                |
| • Excelente resistencia al entorno           |  Control más complicado que el DC por las señales de potencia             |
| • Alta velocidad y alto torque               | • Puede sufrir cambios en sus características debido a temperaturas       |
| • Alta eficiencia en aplicaciones grandes    |                                                                           |
| • Estructura robusta                         |                                                                           |

Tabla 2. Motores AC Asíncronicos

### 1.3. Motores Corriente Alterna - Síncronos
Son máquinas eléctricas cuya velocidad de rotación depende de la frecuencia de la red AC, manteniendo igual velocidad entre el rotor y el campo magnético del estator. Los imanes de campo se montan en el rotor y se excitan con corriente continua, mientras que las bobinas de armadura, divididas en tres partes, se alimentan con corriente trifásica. Estos motores contienen las siguientes caracteristicas fisicas:
* Estator:  Bobinado trifásico para producir el campo magnético giratorio.
* Rotor: Tiene unos imanes o bobinas de excitación recorridas por una corriente continua. Gira a la velocidad del campo magnético.
* Anillos Rozantes: Son anillos metálicos que sirven para alimentar de corriente continua al rotor.

Se debe tener en cuenta que para iniciar el motor síncronico se debe aplica una señal alterna trifásica al estator y una señal DC al rotor, generando un campo magnético con polaridad. El campo del estator atrae al del rotor, provocando su giro a velocidad de sincronismo.
  
En cuestiones industriales estos tipos de motores tienen varias aplicaciones, por lo que podemos resaltas las siguientes ventajas y desventajas:

| **Ventajas**                                     | **Desventajas**                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------|
| • Muy poco mantenimiento                         | • Control de dificultad intermedia                                        |
| • Excelente resistencia al entorno               | • Se requiere respuesta 1:1 entre driver motor                            |
| • Compactos y ligeros                            | • Sus imanes pueden sufrir desmagnetización con el tiempo                 |
| • Alta eficiencia en todo tipo de aplicaciones   |                                                                           |

Tabla 3. Motores AC Síncronicos

### 1.4. Servomotores
* Modelo por corriente de armadura
Parte Eléctrica:   $\upsilon a= La*Ia + Ra*Ia + Vb$
Parte Magnética:   $Tm = ( Ka*Kc*Ic )*Ia( t ) = K\tau *Ia( t )$    ,      $Vb = Ke* \omega$     ,       $Tm = Tc + Tp$
Parte Mecánica:    $J*\frac{\partial^2 \theta }{\partial t^2  } + b*\frac{\mathrm{d} \theta }{\mathrm{d} t} + R\theta = \tau ( t )$
$La * \frac{\mathrm{d} ( \frac{J \theta   + b\theta  + K\theta }{K\tau } )}{\mathrm{d} t} + Ra * ( \frac{J \theta   + b\theta  + K\theta }{K\tau } ) + Ke \theta  = \upsilon a$

## 2. SENSORES
Un sensores un dispositivo que detecta cambios en una magnitud física o química, como temperatura, presión o luz, y los convierte en señales eléctricas para su procesamiento. Se usa en diversos sistemas para monitoreo y automatización.

>🔑 *Encoder:* Un encoder es un sensor que convierte el movimiento (rotación o desplazamiento) en señales eléctricas para medir posición, velocidad o dirección en motores y sistemas automatizados.
>
>🔑 *Resolver:* Es un sensor electromecánico que mide la posición angular y la velocidad de un eje, utilizando señales eléctricas sin necesidad de componentes electrónicos en el rotor, lo que lo hace resistente y preciso. 

Los servomecanismos utilizan sensores para medir corriente (torque), posición y velocidad, asegurando el cumplimiento de las rutinas de movimiento necesarias para diversas aplicaciones. Sin estas mediciones, no se puede garantizar un control preciso.
Se analizarán algunos tipos de sensores que existen, especialmente los encoder u otros sensores que nos permitan hacer mediciones de pulsos de un motor.

### 2.1. Encoders
Generalmente son usados para medir tanto la posición como la velocidad del eje de cualquier tipo de motor.
* Encoders Absolutos: Tienen un Código digital de posición absoluta para una sola revolución y un contador de revoluciones.
* Encoders Incrementales: Generan un número específico de pulsos por unidad de longitud de movimiento lineal.

Comparandos ambos tipos de encoders, tenemos que:

| **Elemento**              | **Encoder Incremental**                 |  **Encoder Absoluto**                                                     |
|---------------------------|-----------------------------------------|---------------------------------------------------------------------------|
| Salida                    | Salida aumenta incrementalmente         | Hay posiciones absolutas en una revolución                                |
| Reinicialización          | Operación de retorno durante encendido  | No require ninguna operación de retorno ya que se sabe siempre su posición dentro de una revolución   |
| Precio                    | Bajo                                    |Alto                                                                        |
| Estructura                | ![Figura de prueba](images/plantilla/Captura2.PNG)  |  ![Figura de prueba](images/plantilla/Captura2.PNG)            |
|Adicionales                |  Solamente se detectan pulsos           | Hay un Código perforado en el encoder. El mas usado es gray                |

### 2.2. Resolver

## 3. DRIVERS
Los drivers se estudian como parte escencial


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
