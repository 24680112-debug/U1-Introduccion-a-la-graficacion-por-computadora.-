# U1-Introducción a la graficación por computadora.
### Apuntes de clase

# 1.1 Historia y evolución de la graficación por computadora
La graficación por computadora evolucionó desde visualizaciones básicas en osciloscopios en los años 50 hasta el fotorrealismo 3D actual, impulsada por hitos como Sketchpad (1963) de Ivan Sutherland, el desarrollo de CAD, el ratón, las tarjetas gráficas (GPU) y el cine (Pixar). Esta tecnología transformó la interacción humano-máquina, la visualización científica, los videojuegos y la animación, pasando de trazos simples a entornos virtuales complejos.

Hitos Clave en la Evolución:
* Años 50 - Los Inicios: Uso de osciloscopios para mostrar datos y el sistema Whirlwind (1951) del MIT, considerado el primer sistema gráfico 3D.
* Años 60 - Fundamentos Interactivos: Ivan Sutherland crea Sketchpad (1963), introduciendo el lápiz óptico y estructuras de datos. Aparece el primer ratón y se desarrollan técnicas de algoritmos de línea.
* Años 70 - Gráficos y Consolas: Nolan Bushnell funda Atari y populariza los videojuegos (Pong). Aparecen los primeros modelos de curvas y superficies, además de los primeros fractales.
* Años 80 - La Era PC y 3D: Lanzamiento de AutoCAD (1982) y auge del modelado 3D. Pixar comienza a producir cortometrajes y Apple populariza las interfaces gráficas.
* Años 90 - Aceleración y Fotorrealismo: Lanzamiento de las tarjetas gráficas de consumo, el estándar OpenGL (1992) y el estreno de Toy Story (1995), el primer largometraje 3D.
* Siglo XXI - Alta Definición y Tiempo Real: Las GPUs (NVIDIA GeForce 256 en 1999) permiten renderizado en tiempo real, motores gráficos avanzados (Doom 3, 2003), realidad virtual y aumento de realismo en simulaciones e inteligencia artificial.
<img width="310" height="162" alt="image" src="https://github.com/user-attachments/assets/39954283-6c26-4af4-96a9-506713182cf2" />


# 1.2. Áreas de aplicación
La graficación por computadora se aplica extensamente en el entretenimiento (videojuegos, cine 3D), diseño asistido (CAD en ingeniería y arquitectura), medicina (imágenes de diagnóstico, simulaciones), visualización científica de datos, publicidad, interfaces de usuario (GUI) y realidad virtual/aumentada, permitiendo la creación, manipulación y visualización de imágenes 2D y 3D.

Las áreas de aplicación más destacadas incluyen:
* Entretenimiento: Producción de películas, efectos visuales (VFX), videojuegos inmersivos y animaciones.
* Diseño e Ingeniería (CAD/CAM): Creación de prototipos, diseño de interiores, modelado industrial y arquitectónico.
* Medicina: Visualización de tomografías, resonancias magnéticas, planificación quirúrgica y simulaciones anatómicas.
* Visualización de Datos: Representación de información compleja, tendencias científicas, mapas geográficos y gráficos estadísticos.
* Publicidad y Arte: Diseño gráfico, edición de fotografía, artes comerciales y creación de logotipos.
* Educación y Simulación: Entrenadores de vuelo, simuladores de conducción y modelos educativos 3D.
* Interfaces Gráficas de Usuario (GUI): Diseño de interfaces para software, aplicaciones móviles y sitios web.
<img width="284" height="177" alt="image" src="https://github.com/user-attachments/assets/31e0d134-3a1a-4a4b-b842-162817eff8b3" />



# 1.3. Aspectos matemáticos de la graficación
Para que una computadora dibuje, necesita coordenadas. En los scripts, la transición de un concepto geométrico a código se basa en la Trigonometría.

* Coordenadas Polares a Cartesianas: En ambos archivos se usa el círculo unitario para posicionar elementos. La computadora entiende X y Y, pero nosotros pensamos en "ángulos".
  * Fórmula aplicada en tus scripts:
<div align="center">
x = radio*cos(θ)
</div>

<div align="center">
y = radio*sin(θ)
</div>

* Conversión de Unidades: El script Flor de vida.py usa math.radians() porque las funciones de Python trabajan en radianes, no en grados sexagesimales.

* Vectores y Puntos: En Poligono2d.py, los vértices se almacenan como tuplas (x, y, 0), representando puntos en un espacio 3D (aunque el dibujo sea 2D).
<img width="452" height="326" alt="image" src="https://github.com/user-attachments/assets/8bc36e42-5e6c-4c69-b430-8e60cfd87fd9" />


# 1.4. Modelos del color: RBG, CMYK, HSV y HSL
### ¿Qué es un modelo de color?
Un modelo de color establece un conjunto de colores primarios a partir de los que, mediante mezclas, se pueden obtener otros colores hasta cubrir todo el espectro visible, además del propio blanco, negro y grises, y aún más. Por ejemplo, hay colores, como el marrón o el magenta, que no están presentes en el espectro visible, y es nuestro cerebro el que lo interpreta a partir de la combinación de ondas con diferentes longitudes.

Los modelos de color más comunes son RGB (utilizado en monitores) y CMYK (utilizado para impresión), que veremos más adelante.

### Modelos aditivos y sustractivos
Hay dos tipos de modelos de color, los aditivos y los sustractivos. Un modelo aditivo se basa en la adición o mezcla de los colores básicos como forma para obtener el blanco.

Un modelo sustractivo se basa en la mezcla de los colores primarios de dicho modelo para «sustraer la luz», es decir, para obtener el negro, que como comentábamos en el artículo de la luz, es la ausencia de luz.

### Modelo RGB
Volviendo a los modelos de color más habituales en fotografía, el modelo RGB define como colores primarios el rojo, el verde y el azul. La combinación de los tres genera blanco. La ausencia de los tres genera negro. Las diferentes mezclas entre ellos representarían toda la gama de color. De nuevo, los grises se representarían con diferentes intensidades de cada color, pero siempre los tres con el mismo valor.

El modelo RBG se utiliza cuando se representa color mediante haces de luz (pantallas o monitores). Un pixel en un monitor se representaría mediante tres subpíxeles o células: una roja, una verde y una azul, correspondiendo cada una a un LED o diodo emisor de luz del respectivo color.

Si los tres diodos están apagados, obtendríamos el negro. Si están encendidos a diferentes intensidades, obtendríamos colores, si están todos encendidos con la misma intensidad y al máximo, tendríamos el blanco, y si la intensidad es menor pero igual en los tres diodos, obtendríamos grises.

### Modelo CMYK
Es un modelo sustractivo y se utiliza en impresión a partir de pigmentos de tres colores básicos: C – cian, M – magenta y Y – amarillo. La K viene del negro, ya que la combinación de los tres anteriores produce un negro poco puro, de ahí que se añada al modelo un pigmento negro puro. Al contrario que en RGB, donde el negro es la ausencia de luz, en CMYK el blanco se representa aquí como ausencia de pigmentos.

Los colores intermedios se producen a partir de la mezcla en distintas proporciones de los pigmentos base.

Hay una relación entre los modelos RGB y CMYK, ya que con la mezcla a igual parte de cada uno de los colores básicos de un modelo obtenemos los primarios del otro.

En RGB (rojo, verde, azul):

* Rojo y verde en iguales proporciones: obtenemos amarillo – Y de CMYK
* Rojo y azul en iguales proporciones: obtenemos el magenta – M
* Verde y azul en iguales proporciones: obtenemos el cian – C

En CMYK (cian, magenta, amarillo):

* Cian y magenta en igual proporción: obtenemos el azul
* Cian y amarillo en igual proporción: obtenemos el verde
* Magenta y amarillo en igual proporción: obtenemos el rojo

### Modelo HSV y HSL
Estos modelos incluyen otros dos parámetros adicionales al matiz o croma para obtener el color, que son la saturación (en ambos) y el valor (en HSV) o la luminosidad o tono (en HSL). De ahí sus siglas: HSL (H – hue o matiz, S – saturation o saturación, L – luminosity o luminosidad/tono), HSV (idem excepto V de value o valor).

La diferencia entre HSV y HSL es que en HSV la saturación va del color puro al blanco, y en HSL la saturación va del color puro al gris medio, y el tono, en HSV va desde el negro al color, y en HSL va desde el negro al blanco. De ahí que HSL sea el que se utiliza más comúnmente en fotografía.

Lightroom, que se basa en HSL, dispone de controles para alterar H – matiz, S – saturación y L – Tono para los siguientes colores: rojo, naranja, amarillo, verde, cian, azul, violeta y magenta.

Siguiendo con Lightroom, éste nos permite fijar la saturación entre gris y color puro para esos 8 colores. Respecto al matiz, nos permite virar los 8 colores a los adyacentes que comentaba en el artículo de luz y color, por ejemplo, para el rojo, desde magenta a naranja.

Por último, respecto al tono, Lightroom nos permite oscurecer cada uno de esos 8 colores hasta el negro, o bien aclararlo hasta llegar al blanco.
<img width="612" height="612" alt="image" src="https://github.com/user-attachments/assets/d14dd541-6c81-4fb4-9cd0-b14baf8336bf" />



# 1.5. Representación y trazo de líneas y polígonos
Este tema explica cómo la computadora "une los puntos". Los archivos muestran dos formas de representar geometría:

### A. Primitivas Geométricas (Flor de vida.py)
Blender ya tiene funciones predefinidas para crear formas básicas.

* Uso de primitive_circle_add: Es una función de alto nivel que genera automáticamente los vértices y aristas de un círculo.

* Resolución: El parámetro vertices=64 define qué tan "suave" se ve el polígono que imita al círculo.

### B. Representación de Datos de Malla (Poligono2d.py)
Este script es mucho más técnico y cercano a cómo funcionan los motores de renderizado internamente:

* Vértices (Vertices): La lista de puntos en el espacio.

* Aristas (Edges): La conexión lógica entre índices de vértices. En el código: aristas.append((i, (i + 1) % lados)).

  * Nota Pro: El uso de % lados (módulo) es un truco de programación para cerrar el polígono, uniendo el último vértice con el primero.

* Estructura de Datos: Se usa malla.from_pydata(vertices, aristas, []), que es la forma fundamental de construir objetos geométricos desde cero en sistemas computacionales.
<img width="682" height="538" alt="image" src="https://github.com/user-attachments/assets/687d72e4-9746-4680-882b-7a14ae1bb038" />
<img width="862" height="566" alt="image" src="https://github.com/user-attachments/assets/0f9b2bc9-483a-4e40-8c95-c40cbc5962b5" />


# 1.6. Formatos de imagen
Aunque los scripts se enfocan en la geometría (vectores), el paso final de la graficación es el rasterizado (convertir esos vectores en píxeles).

* Vectores vs. Bitmaps: Los archivos .py generan gráficos vectoriales (puedes hacer zoom infinito en Blender y no se pixelan). Al renderizar a un formato como .PNG (mencionado en el punto 1.5), se convierten en un mapa de bits.

* Espacio de Color: Por defecto, Blender trabaja en RGB. Si quisieras cambiar el color de "Flor de la Vida" por código, tendrías que asignar materiales con valores normalizados (0.0 a 1.0) para cada canal.

Tabla Comparativa de los Scripts
| Concepto | Flor de vida.py | Poligono2d.py |
|:----------|:------:|--------:|
| Lógica    | Bucle while por ángulos.  | Bucle for por número de lados.   |
| Abstracción | Alta (usa funciones de Blender). | Baja (define vértices manualmente). |
| Propósito | Patrones geométricos complejos. | Estructura base de polígonos. |

  * Tip de Ingeniería: En el script Flor de vida.py, asegúrarse de que el paso_angular sea divisor de 360 para que la figura cierre perfectamente. Actualmente se usa 60, lo cual es perfecto para una simetría hexagonal.
<img width="219" height="86" alt="image" src="https://github.com/user-attachments/assets/842d5ab7-f8e6-4d20-8788-7e05b0f23077" />


# 1.7. Procesamiento de mapas de bits
Un mapa de bits es una matriz de bits que especifica el color de cada píxel de una matriz rectangular de píxeles. El número de bits asignado a un píxel individual determina el número de colores que se pueden asignar a dicho píxel. Por ejemplo, si cada píxel se representa con 4 bits, a un píxel determinado se le podrá asignar uno entre los 16 colores distintos (2^4 = 16).
A las imágenes en mapa de bits se las suele definir por su altura y anchura (en píxeles) y por su profundidad de color (en bits por píxel), que determina el número de colores distintos que se pueden almacenar en cada punto individual, y por lo tanto, en gran medida, la calidad del color de la imagen.

Los gráficos en mapa de bits se distinguen de los gráficos vectoriales en que estos últimos representan una imagen a través del uso de objetos geométricos como curvas de Bézier y polígonos, no del simple almacenamiento del color de cada punto en la matriz. El formato de imagen matricial está ampliamente extendido y es el que se suele emplear para tomar fotografías digitales y realizar capturas de vídeo. Para su obtención se usan dispositivos de conversión analógica-digital, tales como escáneres y cámaras digitales.

### Color
Cada punto representado en la imagen debe contener información de color, representada en canales separados que representan los componentes primarios del color que se pretende representar, en cualquier modelo de color, bien sea RGB, CMYK, LAB o cualquier otro disponible para su representación. A esta información, se puede sumar otro canal que representa la transparencia respecto al fondo de la imagen. En algunos casos, (GIF) el canal de transparencia tiene un solo bit de información, es decir, se puede representar como totalmente opaco o como totalmente transparente; en los más avanzados (PNG, TIFF), el canal de transparencia es un canal con la misma profundidad del resto de canales de color, con lo cual se pueden obtener centenares, miles o incluso millones de niveles de transparencia distintos.

La transformación de un mapa de bits a un formato vectorial se llama vectorización. Este proceso normalmente se lleva a cabo o bien manualmente (calcando el mapa de bits con curvas de Bézier o polígonos vectoriales en programas como Adobe Illustrator) o automáticamente con Corel PowerTrace o Inkscape. El proceso inverso, convertir una imagen vectorial en una imagen de mapa de bits, es mucho más sencillo y se llama rasterización.

<img width="252" height="200" alt="image" src="https://github.com/user-attachments/assets/59d525dd-e2d0-4d5a-a3cb-c6e3017e440e" />



# Referencias bibliográficas
* Computación gráfica: Técnicas y Ejemplos | StudySmarter. (s. f.). StudySmarter ES. https://www.studysmarter.es/resumenes/estudios-de-medios/tecnologia-y-medios/computacion-grafica/#:~:text=Utiliza%20algoritmos%20y%20software%20especializado%20para%20generar,impulsando%20innovaciones%20en%20realidades%20virtuales%20y%20aumentadas.
* Hearn, D., & Baker, M. P. (2006). Gráficos por computadora con OpenGL. Pearson Educación.
* Blender Foundation. (2024). Blender Python API Documentation (Release 4.0). https://docs.blender.org/api/current/
* Hughes, J. F., van Dam, A., McGuire, M., Sklar, D. F., Foley, J. D., Feiner, S. K., & Akeley, K. (2013). Computer Graphics: Principles and Practice. Addison-Wesley Professional.
* Python Software Foundation. (2024). Mathematical functions (math module). https://docs.python.org/3/library/math.html
* Antonio. (2016d, junio 19). Modelos de color (RGB, CMYK, HSV/HSL). Antonio Herrera. https://ahenav.wordpress.com/2014/04/09/modelos-de-color/
