---
title: Iconos (conceptos básicos de diseño)
description: Los iconos son representaciones gráficas de objetos, importantes no solo por motivos éticos como parte de la identidad visual de un programa, sino también por motivos utilitarios como abreviatura para transmitir el significado que los usuarios perciben casi de forma instantánea.
ms.assetid: 6f88cb32-ecfe-4e6e-a41b-31891cf510cf
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ad788338adc81bd9bc796412eebf4bef87ceca2b7a3855e024702a3e1bb23e49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841939"
---
# <a name="icons-design-basics"></a>Iconos (conceptos básicos de diseño)

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Los iconos son representaciones gráficas de objetos, importantes no solo por motivos éticos como parte de la identidad visual de un programa, sino también por motivos utilitarios como abreviatura para transmitir el significado que los usuarios perciben casi de forma instantánea. Windows Vista presenta un nuevo estilo de iconografía que aporta un mayor nivel de detalle y sofisticación a Windows.

**Nota:** Las directrices relacionadas [con los iconos estándar](vis-std-icons.md) se presentan en un artículo independiente.

## <a name="design-concepts"></a>Conceptos de diseño

Aero es el nombre de la experiencia del usuario de Windows Vista, que representa los valores representados en el diseño de la apariencia, así como la visión detrás de la interfaz de usuario (UI). Aero significa: autenticación, ambiente, reflexión y apertura. El objetivo de Aero es establecer un diseño profesional y atractivo. La decoración de Aero crea una experiencia elegante y de alta calidad que facilita la productividad del usuario e incluso impulsa una respuesta emocional.

Windows Los iconos de Vista difieren Windows iconos de estilo XP de las maneras siguientes:

-   El estilo es más realista que ilustrativo, pero no muy fotorealista. Los iconos son imágenes simbólicas que deberían ser mejores que las fotorealistas.
-   Los iconos tienen un tamaño máximo de 256 x 256 píxeles, lo que los hace adecuados para pantallas de valores altos de ppp (puntos por pulgada). Estos iconos de alta resolución permiten una alta calidad visual en las vistas de lista con iconos grandes.
-   Siempre que sea práctico, los iconos de documentos fijos se reemplazan por miniaturas del contenido, lo que facilita la identificación y la búsqueda de documentos.
-   Los iconos de la barra de herramientas tienen menos detalles y ninguna perspectiva, para optimizar los tamaños más pequeños y la distinción visual.

Iconos bien diseñados:

-   Mejore la comunicación visual del programa.
-   Afecta en gran medida a la impresión general de los usuarios del diseño visual del programa y a la satisfacción por su ajuste y terminación.
-   Mejore la facilidad de uso al facilitar la identificación, el aprendizaje y la búsqueda de programas, objetos y acciones.

En las imágenes siguientes se muestra lo que hace que el estilo de iconografía de Aero en Windows Vista sea diferente del usado en Windows XP.

![imágenes de iconos de bloqueo y clave](images/vis-icons-image1.png)

Los Windows vista (el bloqueo y la clave de la izquierda) son auténticos, nítidos y detallados. Se representan en lugar de dibujarse, pero no son completamente fotorealistas.

![imágenes de iconos de cuadernos de globos y cuadernos de cuadernos](images/vis-icons-image2.png)

Los iconos Windows Vista (los dos de la izquierda) son profesionales y de gran calidad, con atención a los detalles que mejoran la calidad de producción de los iconos.

![imágenes de cuaderno, bloqueo, monitor y papel](images/vis-icons-image3.png)

Estos Windows Vista muestran el equilibrio óptico y la precisión percibida en perspectiva y detalles. Esto les permite tener un aspecto grande o pequeño, de cerca o desde una distancia. Además, este estilo de iconografía funciona para pantallas de alta resolución.

![imagen de un icono de enrutador inalámbrico](images/vis-icons-image4.png)![imagen de un icono de hoja de papel](images/vis-icons-image5.png)![imagen de un icono de flecha derecha grande y verde](images/vis-icons-image6.png)

En estos ejemplos se muestran diferentes tipos de iconos, incluido un objeto tridimensional en perspectiva, un icono frontal (plano) y un icono de barra de herramientas.

## <a name="guidelines"></a>Directrices

### <a name="perspective"></a>Perspectiva

-   **Los iconos de Windows Vista son tridimensionales y se muestran en perspectiva como objetos sólidos, o bien objetos bidimensionales que se muestran directamente.** Use iconos planos para archivos y para objetos que son realmente planos, como documentos o fragmentos de papel.

    ![imágenes de un equipo 3d y papel 2d plano ](images/vis-icons-image7.png)

    Iconos 3D y planos típicos.

-   **Los objetos tridimensionales se representan en perspectiva como objetos sólidos, vistos desde una vista baja de los ojos con dos puntos de desvaneciendo.**

    ![imagen de cuaderno con líneas que muestran perspectiva](images/vis-icons-image8.png)

    En este ejemplo se muestran los puntos de perspectiva y de desvanección típicos de los iconos 3D.

-   **En los tamaños más pequeños, el mismo icono puede cambiar de perspectiva a directo.** Con un tamaño de 16 x 16 píxeles y más pequeño, represente iconos directamente (orientados hacia delante). Para iconos más grandes, use perspectiva.

    -   **Excepción:** Los iconos de la barra de herramientas siempre son frontales, incluso en tamaños mayores.

    ![imagen de un equipo 3d grande y un equipo 2D pequeño ](images/vis-icons-image9.png)

    En este ejemplo se muestra cómo se trata el mismo icono de forma diferente, en función del tamaño.

### <a name="light-source"></a>Fuente de luz

-   **La fuente de luz de los objetos dentro de la cuadrícula de perspectiva está por encima, ligeramente delante de y ligeramente a la izquierda del objeto.**
-   **La fuente de luz proyecta sombras ligeramente hacia la parte posterior y derecha de la base del objeto.**
-   **Todos los rayos de luz son paralelos y toan el objeto en el mismo ángulo (como el sol).** El objetivo es tener una apariencia de iluminación uniforme en todos los iconos y efectos de foco. Los rayos de luz paralelos generan sombras que tienen la misma longitud y densidad, lo que proporciona más unidad entre varios iconos.

### <a name="shadows"></a>Shadows

**General**

-   **Use sombras para elevar objetos visualmente desde el fondo y hacer que los objetos 3D aparezcan en tierra, en lugar de flotar de forma incomodada en el espacio.**
-   **Use un intervalo de opacidad del 30 al 50 por ciento para las sombras.** A veces se debe usar un nivel diferente de sombra, en función de la forma o el color de un icono.
-   **Desplágala o acorte la sombra si es necesario para evitar que el tamaño del cuadro de icono la recorte.**
-   **No use sombras en iconos de 24 x 24 o tamaños más pequeños.**

    ![imágenes de iconos 3d con sombras ](images/vis-icons-image10.png)

    Sombras de icono típicas.

**Iconos planos**

-   **Los iconos planos se usan generalmente para iconos de** archivo y objetos planos del mundo real, como un documento o un fragmento de papel.
-   **La iluminación de iconos planos procede de la parte superior izquierda a 130 grados.**
-   **Los iconos más pequeños (por ejemplo, 16 x 16 y 32 x 32) se simplifican para mejorar la legibilidad.** Sin embargo, si contienen una reflexión dentro del icono (a menudo simplificada), es posible que tengan una sombra paralela estrecha. Las sombras paralelas tienen una opacidad del 30 al 50 por ciento.
-   **Los efectos de capa se pueden usar para iconos planos, pero se deben comparar con otros iconos planos.** Las sombras de los objetos variarán ligeramente, según lo que se vea mejor y sea más coherente dentro del conjunto de tamaño y con los demás iconos de Windows Vista. En algunas ocasiones, incluso puede ser necesario modificar las sombras. Esto será especialmente cierto cuando los objetos estén colocados sobre otros.
-   **Se puede usar una gama sutil de colores para lograr el resultado deseado.** Las sombras ayudan a los objetos a quedarse en el espacio. El color afecta al peso percibido de la sombra y puede distorsionar la imagen si es demasiado pesada.

![captura de pantalla del cuadro de diálogo con la sombra paralela activada ](images/vis-icons-image11.png)![captura de pantalla del icono de papel con sombra paralela estrecha ](images/vis-icons-image12.png)

La opción Sombra paralela del cuadro de diálogo Estilo de capa y una sombra típica para un icono plano.

**Rangos de sombras de icono plano básico**



| Característica                              | Intervalo                                                         |
|-------------------------------|----------------------------------------------------------|
| Color<br/>              | Negro<br/>                                         |
| Modo blend<br/>         | Multiplicar<br/>                                      |
| Opacidad<br/>            | Del 22 al 50 por ciento, según el color del elemento<br/> |
| Ángulo<br/>              | 120-130 (usar luz global)<br/>                    |
| Distancia<br/>           | 3 para 256 x 256, que van hasta 1 para 32 x 32<br/>    |
| Propagación:<br/>             | 0<br/>                                             |
| Size<br/>               | 7 para 256 x 256, que van hasta 2 para 32 x 32<br/>    |



 

**Iconos tridimensionales**

-   Cree sombras para iconos 3D en función de cada caso, con el esfuerzo de ajustarse a un intervalo de distancia de conversión y de empujo a totalmente transparente. Cree las imágenes en un tamaño un poco menor que el tamaño total del icono que exige para permitir el espacio para una sombra paralela (para esos tamaños que requerirán uno). Asegúrese de que la sombra no termina repentinamente en el borde del icono.

![Ilustración de la creación de sombras en Photoshop](images/vis_icons_image13.jpeg)

![Ilustración de cuatro objetos con sombras variables](images/vis_icons_image14.jpeg)

Estos ejemplos ayudan a mostrar las variaciones creadas en función de la forma y la posición del propio objeto. En ocasiones, la sombra debe ser aplumada o abreviada para evitar que se recorte por el tamaño del cuadro de icono.

### <a name="color-and-saturation"></a>Color y saturación

-   **Por lo general, los colores están menos saturados que Windows XP.**
-   **Use degradados para crear una imagen de aspecto más realista.**
-   **Aunque no hay ninguna paleta de colores específica para los iconos estándar, recuerde que deben funcionar bien juntos en muchos contextos y temas.** Prefiere el conjunto estándar de colores; no vuelva a colorear los iconos estándar, como los iconos de advertencia, porque esto interrumpe la capacidad de los usuarios para interpretar el significado. Para obtener más instrucciones, vea [Color](vis-color.md).
-   **Los archivos de icono también** requieren versiones de paleta de 8 y 4 bits para admitir la configuración predeterminada en un escritorio remoto. Estos archivos se pueden crear a través de un proceso por lotes, pero deben revisarse, ya que algunos requerirán retoque para mejorar la legibilidad.

    ![captura de pantalla del cuadro de diálogo selector de colores ](images/vis-icons-image15.png)

    No hay ninguna restricción de paleta de colores estricta. Solo se evita la saturación completa (parte superior derecha).

-   Niveles de bits: diseño de ICO para 32 bits (alfa incluido) + 8 bits + 4 bits (se ditrae automáticamente el píxel más crítico). Solo se debe incluir una copia de 32 bits de la imagen de 256 x 256 píxeles y solo se debe comprimir la imagen de 256 x 256 píxeles para mantener el tamaño del archivo reducido. Varias herramientas de iconos ofrecen compresión para Windows Vista.
-   Niveles de bits: barras de herramientas de 24 bits + alfa (máscara de 1 bit), 8 bits y 4 bits.
-   Barras de herramientas o archivos AVI: use el color de transparencia de fondo (R255 G0 B255).

### <a name="size-requirements"></a>Requisitos de tamaño

**General**

-   **Preste especial atención** a los iconos de alta visibilidad, como los iconos de aplicación principales, los iconos de archivo que pueden aparecer en el Explorador de Windows y los iconos que aparecen en el menú Inicio o en el escritorio.
    -   **Iconos de aplicación y Panel de control elementos:** El conjunto completo incluye 16x16, 32x32, 48x48 y 256x256 (el código se escala entre 32 y 256). Se requiere el formato de archivo .ico. Para el modo clásico, el conjunto completo es 16x16, 24x24, 32x32, 48x48 y 64x64.
    -   **Opciones de icono de elemento de lista:** Use miniaturas en directo o iconos de archivo del tipo de archivo (por ejemplo, .doc); conjunto completo.
    -   **Iconos de la barra de herramientas:** 16x16, 24x24, 32x32. Tenga en cuenta que los iconos de la barra de herramientas siempre son planos, no 3D, incluso con un tamaño de 32 x 32.
    -   **Iconos de cuadro de diálogo y asistente:** 32x32 y 48x48.
    -   **Superposiciones:** Código de shell principal (por ejemplo, un acceso directo) 10x10 (para 16x16), 16x16 (para 32 x 32), 24x24 (para 48x48), 128x128 (para 256 x 256). Tenga en cuenta que algunos de ellos son ligeramente más pequeños, pero están cerca de este tamaño, en función de la forma y el equilibrio óptico.
    -   **inicio rápido área de trabajo:** Los iconos se reducirán verticalmente de 48 x 48 en superposiciones dinámicas alt+tab, pero para una versión más nítida, agregue un archivo 40x40 a .ico.
    -   **Iconos de globo:** 32 x 32 y 40 x 40.
    -   **Tamaños adicionales:** Son útiles como recursos para crear otros archivos (por ejemplo, anotaciones, franjas de barra de herramientas, superposiciones, valores altos de ppp y casos especiales): 128x128, 96x96, 64x64, 40x40, 24x24, 22x22, 14x14, 10x10 y 8x8. Puede usar .ico, .png, .bmp u otros formatos de archivo, según el código de esa área.

**Para valores altos de ppp**

-   Windows Vista tiene como destino 96 ppp y 120 ppp.

En las tablas siguientes se muestran ejemplos de relaciones de escalado aplicadas a dos tamaños de icono comunes. Tenga en cuenta que no todos estos tamaños deben incluirse en el archivo .ico. El código escalará los más grandes hacia abajo.



| ppp                   | Tamaño de icono                         | Factor de escala                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 16x16<br/>         | 1.0 (100%)<br/>       |
| 120<br/>     | 20x20<br/>         | 1.25 (125%)<br/>      |
| 144<br/>     | 24x24<br/>         | 1.5 (150%)<br/>       |
| 192<br/>     | 32x32<br/>         | 2.0 (200%)<br/>       |



 



| ppp                   | Tamaño de icono                         | Factor de escala                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 32x32<br/>         | 1.0 (100%)<br/>       |
| 120<br/>     | 40x40<br/>         | 1.25 (125%)<br/>      |
| 144<br/>     | 48x48<br/>         | 1.5 (150%)<br/>       |
| 192<br/>     | 64x64<br/>         | 2.0 (200%)<br/>       |



 

**Tamaños de archivo .ico (estándar)**

![Diagrama que muestra diferentes iconos de enrutador de tamaño estándar.](images/vis-icons-image16.png)

**Tamaños de archivo .ico (casos especiales)**

![ilustración de iconos de enrutador de diferentes tamaños ](images/vis-icons-image17.png)

**Anotaciones y superposiciones**

-   Las anotaciones van en la esquina inferior derecha del icono y deben rellenar el 25 por ciento del área de iconos.
    -   **Excepción:** los iconos de 16 x 16 toman anotaciones de 10 x 10.
-   No use más de una anotación sobre un icono.
-   Las superposiciones van en la esquina inferior izquierda del icono y deben rellenar el 25 % del área de iconos.
    -   **Excepción:** los iconos de 16 x 16 toman superposiciones de 10 x 10.

### <a name="level-of-detail"></a>Nivel de detalle

-   El tamaño de 16 x 16 de muchos de estos iconos se sigue utilizando ampliamente y, por tanto, es importante.
-   Los detalles de un icono de este tamaño deben mostrar claramente el punto clave del icono.
-   A medida que un icono se vuelve más pequeño, la transparencia y algunos detalles especiales que se encuentran en tamaños más grandes deben sacrificarse para simplificar y llegar al punto.
-   Los atributos y los colores se deben enfatizar y usar para resaltar las formas clave.

    ![ilustración de un dispositivo grande y dos pequeños ](images/vis-icons-image18.png)

    A las 16 x 16, el icono del dispositivo de audio portátil podría confundirse fácilmente con un teléfono móvil, por lo que la pieza de los oídos es un detalle visual clave para mostrar.

-   El simple escalado vertical del tamaño de 256 x 256 no funciona.
-   Todos los tamaños necesitan un nivel de detalle pertinente; cuanto menor sea el icono, más necesita para sobresalar los detalles de definición.

    ![ilustración de teléfonos móviles con detalles claros ](images/vis-icons-image19.png)

    ![ilustración de teléfonos móviles con detalles desenfocados ](images/vis-icons-image20.png)

### <a name="icon-development"></a>Desarrollo de iconos

**Diseño y generación de iconos**

-   **Contratación de un diseñador gráfico experimentado.** Para obtener gráficos excelentes, las imágenes y los iconos funcionan con expertos. Se recomienda la experiencia en las ilustraciones con vector art o programas 3D.
-   **Planee** realizar series de iteraciones, desde bocetos de concepto iniciales hasta simulaciones en contexto, hasta revisión final de producción y ajuste y fin de iconos en el producto de trabajo.
-   **La creación de iconos con anticipación puede ser costosa.** Recopila todos los detalles y requisitos existentes, como: el conjunto completo de iconos necesarios; la función principal y el significado de cada una de ellas; familias o clústeres del conjunto que desea que sean evidentes; requisitos de marca; los nombres de archivo exactos; formatos de imagen usados en el código; y los requisitos de tamaño. Asegúrese por adelantado de que puede hacer todo el tiempo con el diseñador.
-   **Recuerde que es posible que el diseñador no esté familiarizado con el producto, por lo que debe proporcionar información funcional, capturas de pantalla y secciones de especificación, según corresponda.**
-   **Planee revisiones geopolíticas y legales según corresponda.**
-   **Asignar un período de tiempo y tener comunicación regular.**

**Del boceto de concepto al producto final**

![ilustración del desarrollo de bocetos de teléfonos móviles ](images/vis-icons-image21.png)

-   Crear bocetos de concepto.
-   Pruebe el concepto en distintos tamaños.
-   Se representa en 3D si es necesario.
-   Tamaños de prueba en diferentes colores de fondo.
-   Evalúe los iconos en el contexto de la interfaz de usuario real.
-   Generar el archivo .ico final u otros formatos de recursos gráficos.

**Herramientas**

-   **Lápiz y papel:** Ideas de concepto iniciales, enumeradas y esbozadas.
-   **3D Studio Max:** Representar objetos 3D en perspectiva.
-   **Adobe Adobe Adobe:** Esboce e itera, se simula en contexto y se finalizarán los detalles.
-   **Adobe Adobe Adobe/Macromedia Freehand:** Esboce e itera y finalizará los detalles.
-   **Gamani Gif Movie Gear:** Generar archivo .ico (con compresión si es necesario).
-   **Taller de iconos de Kpi:** Generar archivo .ico (con compresión si es necesario).
-   Microsoft Visual Studio no admite iconos Windows Vista (no hay compatibilidad con el canal alfa ni más de 256 colores).

**Producción**

> [!TIP]
> Siga estos pasos para crear un único archivo .ico que contenga varios tamaños de imagen y profundidades de color.

**Paso 1: Conceptualizar**

-   Use los conceptos establecidos siempre que sea posible para garantizar la coherencia de los significados del icono y su relevancia para otros usos.
-   Tenga en cuenta cómo aparecerá el icono en el contexto de la interfaz de usuario y cómo podría funcionar como parte de un conjunto de iconos.
-   Si revisa un icono existente, considere si se puede reducir la complejidad.
-   Tenga en cuenta el impacto cultural de los gráficos. Evite usar letras, palabras, manos o caras en iconos. Represente las representaciones de personas o usuarios de la forma más genérica posible, si es necesario.
-   Si combina varios objetos en una sola imagen en un icono, tenga en cuenta cómo se escalará la imagen a tamaños más pequeños. No use más de tres objetos en un icono (se prefiere dos). Para el tamaño de 16 x 16, considere la posibilidad de quitar objetos o simplificar la imagen para mejorar el reconocimiento.
-   No use la marca Windows en los iconos.

**Paso 2: Ilustrar**

-   Para ilustrar Windows de estilo Aero, use una herramienta de vector como Macromedia Freehand o Adobe Illustrate. Use la paleta y las características de estilo como se ha descrito anteriormente en este artículo.
-   Ilustrar la imagen mediante Freehand o Illustrate. Copie y pegue las imágenes vectoriales en Adobe Adobe Adobe.
-   Crear y usar una capa de plantilla en Photoshop para asegurarse de que el trabajo se realiza dentro de regiones cuadradas de los tamaños regulados.
-   Cree las imágenes con un tamaño un poco menor que el tamaño total del icono que exige para permitir el espacio para una sombra paralela (para los tamaños que requieren una).
-   Coloque las imágenes en la parte inferior de los cuadrados para que todos los iconos de un directorio se coloquen de forma coherente. Evite cortar sombras.
-   Si va a agregar otro objeto a una imagen o una serie, mantenga el objeto principal en una posición fija y coloque las imágenes planas de menor tamaño en una posición fija, como la parte inferior izquierda o superior derecha, en función del caso.

**Paso 3: Creación de imágenes de 24 bits**

-   Una vez que haya pegado tamaños en Photoshop, compruebe la legibilidad de las imágenes, especialmente en tamaños de 16 x 16 y más pequeños. Es posible que se requiera la aplicación de píxeles mediante porcentajes de colores. También puede ser necesaria una reducción de la transparencia. Es habitual resalte aspectos en tamaños más pequeños y eliminar también aspectos, con el fin de centrarse en el punto clave.
-   Los iconos de 8 bits se mostrarán en cualquier modo de color inferior a 32 bits y no tendrán el canal alfa de 8 bits, por lo que es posible que tengan que limpiar sus bordes o más porque no hay suavizado de contorno (los bordes pueden ser irregulares y la imagen puede ser difícil de leer).
-   En Photoshop, duplique la capa de imagen de 24 bits y cambie el nombre de la capa a imágenes de 4 bits. Indexe imágenes de 4 bits a la paleta Windows 16 colores.
-   Limpie las imágenes con solo los colores de la paleta de 16 colores. Los contornos realizados a partir de versiones más oscuras o más claras de los colores del objeto suelen ser preferibles a gris o negro.
-   Si trabaja en un mapa de bits, asegúrese de que el color de fondo no se usa en la propia imagen, ya que ese color será el color transparente. A menudo se usa El color de trasparencia de fondo(R255 G0 B255) como color de transparencia de fondo.

**Paso 4: Creación de imágenes de 8 y 4 bits**

-   Ahora que las imágenes de 24 bits están listas para convertirse en iconos de 32 bits, es necesario crear versiones de 8 bits.
-   Este es un buen momento para probar las capturas de pantalla contextuales. Es increíble lo que se puede detectar mediante la visualización de otros iconos o una familia de iconos en contexto. Este paso puede ahorrar tiempo y dinero. Es mucho mejor detectar problemas antes de que los archivos pasen a producción y se entreguen.
-   Agregue la sombra paralela a las imágenes en tamaños que las requieran.
-   Combine la sombra paralela y las imágenes de 24 bits.
-   Cree un nuevo archivo de Photoshop para cada tamaño. Copie y pegue la imagen adecuada. Guarde cada archivo como un .psd archivo.
-   No combine la capa de imagen con la capa de fondo. Resulta útil incluir el tamaño y la profundidad de color en el nombre de archivo mientras se trabaja, pero es posible que en última instancia sea necesario cambiar el nombre del archivo.

**Paso 5: Creación del archivo .ico**

-   Elija la aplicación que mejor se adapte a las necesidades y aptitudes de los intérpretes. Recuerde que los iconos que se usarán en un producto de envío deben crearse en una herramienta adquirida o con licencia. Esto significa que no se pueden usar versiones de prueba.
-   Los diseñadores que han generado iconos para Windows Vista han usado ambos productos enumerados a continuación y cada uno ofrece la capacidad de exportar a Adobe Adobe Adobe CS.
    -   Gamani Gif Movie Gear: Produce el archivo .ico
    -   Taller de iconos de Kpis: Generación de un archivo .ico
-   Visual Studio no admite iconos Windows Vista (no hay compatibilidad con el canal alfa o más de 256 colores), por lo que no se recomienda su uso.
-   Los archivos de icono (formato .ico) deben contener las versiones de 4 y 8 bits, así como las versiones de 24 bits + alfa.
-   Guarde los archivos como un "icono Windows (.ico)" independientemente del programa de creación de iconos que elija usar.
-   Algunos recursos iconográficos pueden ser realmente franjas de mapa de bits, que también requieren un canal alfa (por ejemplo, para las barras de herramientas) o archivos .png guardados con transparencia. No todos tienen necesariamente el formato .ico; compruebe qué formato se admite en el código.

**Paso 6: Evaluar**

-   Mire todos los tamaños.
-   Mire la familia juntos para evaluar el parecido de la familia, el equilibrio óptico y la distinción.
-   Mire en contexto para evaluar los pesos relativos y la visibilidad (asegúrese de que no domina).
-   Considere los casos que no se pueden usar ahora, pero que podrían estar en un futuro próximo. ¿Podría anotarse este icono o tener una superposición?
-   Mire en el código.

### <a name="icons-in-the-context-of-list-views-toolbars-and-tree-views"></a>Iconos en el contexto de vistas de lista, barras de herramientas y vistas de árbol

**Vistas de lista**

-   Para Windows Vista, use miniaturas para los archivos que mantienen contenido que es visualmente distinto a pequeña escala, de modo que los usuarios puedan reconocer directamente el archivo que buscan. (Use la interfaz Windows programación de aplicaciones de miniaturas).

    ![captura de pantalla del Explorador de Windows con iconos de carpeta ](images/vis-icons-image22.png)

-   Las superposiciones del icono de aplicación (no se muestran aquí) en las miniaturas ayudan a la asociación con la aplicación para el tipo de archivo, además de mostrar la vista previa del archivo.

**Nota:** En el caso de los archivos sin contenido visualmente distinto, no use miniaturas. En su lugar, use iconos de archivo simbólico tradicionales que muestren la representación de objetos y la aplicación o el tipo asociados.

**Barras de herramientas**

-   Los iconos que aparecen en una barra de herramientas deben tener un equilibrio óptico en tamaño, color y complejidad.
-   Pruebe los iconos potenciales en una captura de pantalla contextual para evitar cualquier dominación o desequilibrio no deseado.
-   Las pruebas en capturas de pantalla ayudan a evitar fácilmente iteraciones costosas en el código.
-   Revise también los iconos del código. El movimiento y otros factores pueden afectar al éxito de un icono. En algunos casos, pueden ser necesarias más iteraciones.

![captura de pantalla de la barra de herramientas con iconos y etiquetas pequeños ](images/vis-icons-image23.png)

En el ejemplo anterior, aún no se ha logrado el equilibrio óptico.

![ilustración de iconos en distintos fondos ](images/vis-icons-image24.png)

Pruebe iteraciones en contexto.

**Vistas de árbol**

-   Se necesita un equilibrio óptico para conservar la jerarquía en un control de vista de árbol.
-   Por lo tanto, los iconos que se usan normalmente en este contexto se deben evaluar allí. A veces, un icono determinado de 16 x 16 se debe hacer más pequeño porque su forma tiene una dominación óptica sobre otras.
-   La compensación de desequilibrios ópticos es una parte importante de la generación de iconos de alta calidad.

![ilustración de dos conjuntos de carpetas en la vista de árbol ](images/vis-icons-image25.png)

 

