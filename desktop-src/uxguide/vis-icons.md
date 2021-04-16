---
title: Iconos (conceptos básicos de diseño)
description: Los iconos son representaciones fotográficas de objetos, no solo son importantes por motivos estéticos como parte de la identidad visual de un programa, sino también por motivos de utilitarian como una forma abreviada de transmitir, lo que significa que los usuarios se perciben de manera casi instantánea.
ms.assetid: 6f88cb32-ecfe-4e6e-a41b-31891cf510cf
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 9dc0994aa4e7aa07709a8051f9b13b72142bcb7b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104562811"
---
# <a name="icons-design-basics"></a>Iconos (conceptos básicos de diseño)

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Los iconos son representaciones fotográficas de objetos, no solo son importantes por motivos estéticos como parte de la identidad visual de un programa, sino también por motivos de utilitarian como una forma abreviada de transmitir, lo que significa que los usuarios se perciben de manera casi instantánea. Windows Vista presenta un nuevo estilo de iconografía que ofrece un mayor nivel de detalle y sofisticación a Windows.

**Nota:** Las instrucciones relacionadas con los [iconos estándar](vis-std-icons.md) se presentan en un artículo independiente.

## <a name="design-concepts"></a>Conceptos de diseño

Aero es el nombre de la experiencia del usuario de Windows Vista, que representa tanto los valores incorporados en el diseño de la estética como la visión subyacente de la interfaz de usuario (UI). Aero representa: auténtico, enérgico, reflectante y Open. Aero pretende establecer un diseño que sea profesional y bonito. La estética de Aero crea una experiencia de alta calidad y elegante que facilita la productividad del usuario e incluso impulsa una respuesta emocional.

Los iconos de Windows Vista difieren de los iconos de estilo de Windows XP de las siguientes maneras:

-   El estilo es más realista que el ilustrativo, pero no es muy realista. Los iconos son imágenes simbólicas que deben tener un aspecto mejor que el de fotoestado.
-   Los iconos tienen un tamaño máximo de 256x256 píxeles, por lo que son adecuados para pantallas con valores altos de PPP (puntos por pulgada). Estos iconos de alta resolución permiten una calidad visual alta en las vistas de lista con iconos grandes.
-   Siempre que sea práctico, los iconos de documentos fijos se sustituyen por miniaturas del contenido, lo que facilita la identificación y la búsqueda de los documentos.
-   Los iconos de la barra de herramientas tienen menos detalles y no hay ninguna perspectiva para optimizarlos para tamaños más pequeños y distintivo visual.

Iconos bien diseñados:

-   Mejorar la comunicación visual del programa.
-   Influya totalmente en la impresión general de los usuarios del diseño visual de su programa y la apreciación de su ajuste y acabado.
-   Mejore la facilidad de uso haciendo que los programas, objetos y acciones sean más fáciles de identificar, aprender y encontrar.

En las siguientes imágenes se describe lo que hace que el estilo Aero de iconografía en Windows Vista sea diferente del que se usa en Windows XP.

![imágenes de iconos de bloqueo y clave](images/vis-icons-image1.png)

Los iconos de Windows Vista (el bloqueo y la clave a la izquierda) son auténticos, nítidos y detallados. Se representan en lugar de dibujarse, pero no son completamente fotorealistas.

![imágenes de iconos de Bloc de notas de globo terráqueo](images/vis-icons-image2.png)

Los iconos de Windows Vista (los dos a la izquierda) son profesionales y bonitos, con atención a los detalles que mejoran la calidad de la producción de iconos.

![imágenes de Notebook, Lock, monitor y Paper](images/vis-icons-image3.png)

Estos iconos de Windows Vista muestran el equilibrio óptico y la precisión percibida en la perspectiva y los detalles. Esto les permite tener un aspecto muy grande o pequeño, de arriba a abajo o desde una distancia. Además, este estilo de iconografía funciona en pantallas de alta resolución.

![imagen de un icono de enrutador inalámbrico](images/vis-icons-image4.png)![imagen de un icono de hoja de papel](images/vis-icons-image5.png)![imagen de un icono de flecha derecha grande y verde](images/vis-icons-image6.png)

En estos ejemplos se muestran distintos tipos de iconos, como un objeto tridimensional en la perspectiva, un icono plano frontal (plano) y un icono de la barra de herramientas.

## <a name="guidelines"></a>Directrices

### <a name="perspective"></a>Perspectiva

-   **Los iconos de Windows Vista son tridimensionales y se muestran en perspectiva como objetos sólidos, o bien se muestran objetos bidimensionales.** Use iconos planos para los archivos y para los objetos que realmente son planos, como documentos o piezas de papel.

    ![imágenes del equipo 3D y papel plano 2D ](images/vis-icons-image7.png)

    Iconos 3D y planos típicos.

-   **Los objetos tridimensionales se representan en perspectiva como objetos sólidos, que se muestran a partir de una vista de pájaros bajo bajo dos puntos de desvanecimiento.**

    ![imagen del cuaderno con líneas que muestran la perspectiva](images/vis-icons-image8.png)

    Este ejemplo muestra puntos de perspectiva y de desvanecimiento típicos de iconos 3D.

-   **En tamaños más pequeños, el mismo icono puede cambiar de una perspectiva a una directa.** En el tamaño de 16x16 píxeles y más pequeño, los iconos de representación se activan directamente (hacia delante). Para los iconos más grandes, use la perspectiva.

    -   **Excepción:** Los iconos de la barra de herramientas siempre están orientados al frente, incluso en tamaños mayores.

    ![imagen de equipo 3D grande y pequeño equipo en 2D ](images/vis-icons-image9.png)

    En este ejemplo se muestra cómo el mismo icono se trata de forma diferente, en función del tamaño.

### <a name="light-source"></a>Fuente de luz

-   **La fuente de luz de los objetos dentro de la cuadrícula de perspectiva es superior, ligeramente delante y ligeramente a la izquierda del objeto.**
-   **La fuente de luz proyecta sombras que son ligeramente hacia atrás y a la derecha de la base del objeto.**
-   **Todos los rayos claros son paralelos y cogolpean el objeto a lo largo del mismo ángulo (como el sol).** El objetivo es tener una apariencia de iluminación uniforme en todos los iconos y efectos destacados. Los rayos de luz paralela producen sombras que tienen la misma longitud y densidad, lo que proporciona más Unity en varios iconos.

### <a name="shadows"></a>Shadows

**General**

-   **Utilice Shadows para levantar objetos visualmente desde el fondo y para que los objetos 3D aparezcan por encima, en lugar de estar flotando de forma complicada en el espacio.**
-   **Use un intervalo de opacidad del 30-50 por ciento para las sombras.** A veces se debe usar un nivel de sombra diferente, dependiendo de la forma o el color de un icono.
-   **Desvanecer o acortar la sombra si es necesario, para evitar que se recorte por el tamaño del cuadro de icono.**
-   **No use sombras en los iconos de 24x24 o tamaños más pequeños.**

    ![imágenes de iconos 3D con sombras ](images/vis-icons-image10.png)

    Icono típico sombras.

**Iconos planos**

-   Los **iconos planos se suelen usar para los iconos de archivo y para los objetos planos del mundo real,** como un documento o una hoja de papel.
-   **La iluminación de icono plano proviene de la parte superior izquierda en 130 grados.**
-   **Los iconos más pequeños (por ejemplo, 16x16 y 32x32) se simplifican para facilitar la lectura.** Sin embargo, si contienen un reflejo dentro del icono (a menudo simplificado), pueden tener una sombra paralela estrecha. Los intervalos de sombra paralelas en la opacidad del 30-50 por ciento.
-   **Los efectos de capa se pueden usar para iconos planos, pero se deben comparar con otros iconos planos.** Las sombras de los objetos variarán en cierto modo, según lo que sea mejor y sea más coherente en el conjunto de tamaños y con los demás iconos en Windows Vista. En algunas ocasiones, incluso puede ser necesario modificar las sombras. Esto será especialmente cierto cuando los objetos se colocan sobre otros.
-   **Se puede usar una gama sutil de colores para lograr el resultado deseado.** Los objetos de ayuda Shadows se encuentran en el espacio. El color afecta al peso percibido de la sombra y puede distorsionar la imagen si es demasiado pesada.

![captura de pantalla del cuadro de diálogo con sombra paralela activada ](images/vis-icons-image11.png)![captura de pantalla del icono de papel con sombra paralela estrecha ](images/vis-icons-image12.png)

La opción sombra paralela en el cuadro de diálogo estilo de capa y una sombra típica para un icono plano.

**Intervalos de sombra de icono plano básico**



| Característica                              | Intervalo                                                         |
|-------------------------------|----------------------------------------------------------|
| Color<br/>              | Negro<br/>                                         |
| Modo de mezcla<br/>         | Multiplicar<br/>                                      |
| Opacidad<br/>            | 22-50 por ciento, dependiendo del color del elemento<br/> |
| Ángulo<br/>              | 120-130 (usar luz global)<br/>                    |
| Distancia<br/>           | 3 para 256x256, de un intervalo de hasta 1 para 32x32<br/>    |
| Propagación:<br/>             | 0<br/>                                             |
| Tamaño<br/>               | 7 para 256x256, que va hasta 2 para 32x32<br/>    |



 

**Iconos tridimensionales**

-   Crear sombras para los iconos 3D en función de cada caso, con un esfuerzo para ajustarse dentro de un intervalo de distancia de la conversión y desvanecimiento a totalmente transparente. Cree las imágenes en un tamaño un poco más pequeño que el tamaño de icono general para permitir el espacio para una sombra paralela (para los tamaños que requerirán una). Asegúrese de que la sombra no finaliza repentinamente en el borde del icono.

![Ilustración de la creación de sombras en Photoshop](images/vis_icons_image13.jpeg)

![Ilustración de cuatro objetos con sombras variables](images/vis_icons_image14.jpeg)

Estos ejemplos ayudan a mostrar las variaciones creadas en función de la forma y la posición del propio objeto. A veces es necesario desvanecer o acortar la sombra para impedir que se recorte por el tamaño del cuadro de icono.

### <a name="color-and-saturation"></a>Color y saturación

-   **Los colores suelen ser menos saturados que los de Windows XP.**
-   **Use degradados para crear una imagen de aspecto más realista.**
-   **Aunque no hay ninguna paleta de colores específica para los iconos estándar, recuerde que deben funcionar bien juntos en muchos contextos y temas.** Prefiere el conjunto estándar de colores; no vuelva a colorear iconos estándar, como iconos de advertencia, ya que esto interrumpe la capacidad de los usuarios de interpretar el significado. Para obtener más instrucciones, consulte [color](vis-color.md).
-   **Los archivos de iconos requieren también versiones de la paleta de 8 y 4** bits para admitir la configuración predeterminada en un escritorio remoto. Estos archivos se pueden crear a través de un proceso por lotes, pero deben revisarse, ya que algunos requerirán volver a tocar para mejorar la legibilidad.

    ![captura de pantalla del cuadro de diálogo Selector de colores ](images/vis-icons-image15.png)

    No hay ninguna restricción estricta de la paleta de colores. Solo se evita la saturación completa (superior derecha).

-   Niveles de bits: diseño de ICO para 32 bits (alfa incluido) + 8 bits + 4 bits (se ha desactivado automáticamente el solo lectura de píxeles). Solo se debe incluir una copia de 32 bits de la imagen de píxel de 256x256 y solo se debe comprimir la imagen de 256x256 píxeles para mantener el tamaño del archivo inactivo. Varias herramientas de iconos ofrecen compresión para Windows Vista.
-   Niveles de bits: barras de herramientas de 24 bits + alfa (máscara de 1 bit), de 8 bits y de 4 bits.
-   Barras de herramientas o archivos AVI: Use magenta (R255 G0 B255) como color de transparencia de fondo.

### <a name="size-requirements"></a>Requisitos de tamaño

**General**

-   **Preste especial atención a los iconos de alta visibilidad,** como los iconos de la aplicación principal, los iconos de archivo que pueden aparecer en el explorador de Windows y los iconos que aparecen en el menú Inicio o en el escritorio.
    -   **Iconos de aplicación y elementos del panel de control:** El conjunto completo incluye 16x16, 32x32, 48x48 y 256x256 (el código se escala entre 32 y 256). El formato de archivo. ico es obligatorio. En el modo clásico, el conjunto completo es 16x16, 24x24, 32x32, 48x48 y 64 x 64.
    -   **Opciones de icono de elemento de lista:** Usar miniaturas activas o iconos de archivo del tipo de archivo (por ejemplo,. doc); conjunto completo.
    -   **Iconos de la barra de herramientas:** 16x16, 24x24, 32x32. Tenga en cuenta que los iconos de la barra de herramientas siempre son planos, no 3D, ni siquiera en el tamaño 32x32.
    -   **Iconos de cuadro de diálogo y de asistente:** 32x32 y 48x48.
    -   **Superposiciones:** Código de Shell principal (por ejemplo, un acceso directo) 10x10 (para 16x16), 16x16 (para 32x32), 24x24 (para 48x48), 128x128 (para 256x256). Tenga en cuenta que algunas de ellas son ligeramente más pequeñas, pero están cerca de este tamaño, dependiendo de la forma y el equilibrio óptico.
    -   **Área de inicio rápido:** Los iconos se reducirán verticalmente de 48x48 en las superposiciones dinámicas Alt + Tab, pero para una versión más nítida, agregue un 40 x 40 al archivo. ico.
    -   **Iconos de globo:** 32x32 y 40 x 40.
    -   **Tamaños adicionales:** Son útiles para tener a mano los recursos para crear otros archivos (por ejemplo, anotaciones, franjas de la barra de herramientas, superposiciones, PPP alto y casos especiales): 128x128, 96x96, 64 x 64, 40 x 40, 24x24, 22x22, 14x14, 10x10 y 8 x 8. Puede usar. ico,. png,. bmp u otros formatos de archivo, en función del código de esa área.

**Para altos PPP**

-   Windows Vista tiene como destino 96 PPP y 120 ppp.

En las tablas siguientes se muestran ejemplos de relaciones de escalado que se aplican a dos tamaños de icono comunes. Tenga en cuenta que no todos estos tamaños deben incluirse en el archivo. ico. El código escalará los más grandes.



| ppp                   | Tamaño de icono                         | Factor de escala                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 16x16<br/>         | 1,0 (100%)<br/>       |
| 120<br/>     | 20x20<br/>         | 1,25 (125%)<br/>      |
| 144<br/>     | 24x24<br/>         | 1,5 (150%)<br/>       |
| 192<br/>     | 32x32<br/>         | 2,0 (200%)<br/>       |



 



| ppp                   | Tamaño de icono                         | Factor de escala                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 32x32<br/>         | 1,0 (100%)<br/>       |
| 120<br/>     | 40x40<br/>         | 1,25 (125%)<br/>      |
| 144<br/>     | 48x48<br/>         | 1,5 (150%)<br/>       |
| 192<br/>     | 64x64<br/>         | 2,0 (200%)<br/>       |



 

**tamaños de archivo. ico (estándar)**

![Diagrama que muestra distintos iconos de enrutador de tamaño estándar.](images/vis-icons-image16.png)

**tamaños de archivo. ico (casos especiales)**

![Ilustración de iconos de enrutador de tamaño distinto ](images/vis-icons-image17.png)

**Anotaciones y superposiciones**

-   Las anotaciones van en la esquina inferior derecha del icono y deben llenar el 25 por ciento del área de iconos.
    -   **Excepción:** los iconos 16x16 toman anotaciones 10x10.
-   No use más de una anotación sobre un icono.
-   Las superposiciones van en la esquina inferior izquierda del icono y deben llenar el 25 por ciento del área de iconos.
    -   **Excepción:** los iconos 16x16 toman superposiciones de 10x10.

### <a name="level-of-detail"></a>Nivel de detalle

-   el tamaño 16x16 de muchos de estos iconos sigue siendo muy utilizado y, por lo tanto, es importante.
-   Los detalles de un icono de este tamaño deben mostrar claramente el punto clave del icono.
-   A medida que se reduce el tamaño de un icono, la transparencia y algunos detalles especiales que se encuentran en tamaños mayores se deben sacrificar para simplificar y obtener el punto.
-   Los atributos y los colores se deben exagerar y usar para resaltar los formatos clave.

    ![Ilustración de un dispositivo grande y dos pequeños ](images/vis-icons-image18.png)

    En 16x16, el icono del dispositivo de audio portátil podría confundirse con facilidad para un teléfono móvil, por lo que la pieza auricular es un detalle visual clave que se debe mostrar.

-   Simplemente no funciona el escalado vertical desde el tamaño de 256x256.
-   Todos los tamaños necesitan un nivel de detalle relevante; cuanto menor sea el icono, más deberá exagerar los detalles de la definición.

    ![Ilustración de teléfonos móviles con detalles claros ](images/vis-icons-image19.png)

    ![Ilustración de teléfonos móviles con detalles borrosos ](images/vis-icons-image20.png)

### <a name="icon-development"></a>Desarrollo de iconos

**Diseñar y generar iconos**

-   **Contratar un diseñador gráfico experimentado.** Para excelentes gráficos, imágenes e iconos funcionan con expertos. Se recomienda la experiencia en ilustraciones mediante el uso de imágenes vectoriales o programas 3D.
-   **Planee realizar series de iteraciones,** desde bocetos de concepto iniciales hasta simulacros en contexto, hasta la revisión final de la producción y el ajuste y la finalización de los iconos del producto en funcionamiento.
-   **Pensar en la creación de iconos puede ser caro.** Recopile todos los detalles y requisitos existentes, como: el conjunto completo de iconos necesarios; la función principal y el significado de cada; familias o clústeres en el conjunto que desea ser aparente; requisitos de marca; los nombres de archivo exactos; formatos de imagen utilizados en el código; requisitos de tamaño y. Asegúrese por adelantado de que puede sacar el máximo partido de su tiempo con el diseñador.
-   **Recuerde que es posible que el diseñador no esté familiarizado con el producto, por lo que debe proporcionar información funcional, capturas de pantalla y secciones de especificaciones, según corresponda.**
-   **Planee las revisiones geopolíticas y legales según corresponda.**
-   **Asigne un período de tiempo y una comunicación normal.**

**De esbozo de concepto a producto final**

![Ilustración de cómo desarrollar bocetos de teléfonos móviles ](images/vis-icons-image21.png)

-   Cree bocetos de concepto.
-   Pruebe el concepto en diferentes tamaños.
-   Se representa en 3D si es necesario.
-   Tamaños de prueba en diferentes colores de fondo.
-   Evaluar iconos en el contexto de la interfaz de usuario real.
-   Generar un archivo. ico final u otros formatos de recursos gráficos.

**Herramientas**

-   **Lápiz y papel:** Ideas de concepto iniciales, enumeradas y esbozadas.
-   en **3D Studio como máximo:** Representar objetos 3D en perspectiva.
-   **Adobe Photoshop:** Esboce e iteración, simulacros en contexto y finalización de los detalles.
-   **Adobe Illustrator/Macromedia FreeHand:** Esboce y itere los detalles.
-   **Gamani de película GIF:** Cree el archivo. ico (con compresión si es necesario).
-   **Taller de icono axial:** Cree el archivo. ico (con compresión si es necesario).
-   Microsoft Visual Studio no es compatible con los iconos de Windows Vista (no hay compatibilidad con el canal alfa o con más de 256 colores).

**Producción**

> [!TIP]
> Siga estos pasos para crear un único archivo. ico que contenga varios tamaños de imagen y profundidades de color.

**Paso 1: conceptualizar**

-   Use los conceptos establecidos siempre que sea posible para garantizar la coherencia de los significados del icono y su relevancia con respecto a otros usos.
-   Tenga en cuenta cómo aparecerá el icono en el contexto de la interfaz de usuario y cómo podría funcionar como parte de un conjunto de iconos.
-   Si va a revisar un icono existente, tenga en cuenta si se puede reducir la complejidad.
-   Tenga en cuenta el impacto cultural de los gráficos. Evite el uso de letras, palabras, manos o caras en los iconos. Describir las representaciones de personas o usuarios de la forma genérica posible, si es necesario.
-   Si combina varios objetos en una sola imagen en un icono, tenga en cuenta cómo se escalará la imagen a los tamaños más pequeños. No use más de tres objetos en un icono (se prefiere dos). Para el tamaño 16x16, considere la posibilidad de quitar objetos o de simplificar la imagen para mejorar el reconocimiento.
-   No use la marca de Windows en los iconos.

**Paso 2: ilustrar**

-   Para ilustrar los iconos de estilo Aero de Windows, use una herramienta vectorial como Macromedia FreeHand o Adobe Illustrator. Use las características de la paleta y el estilo que se describen anteriormente en este artículo.
-   Ilustra la imagen mediante FreeHand o Illustrator. Copie y pegue las imágenes vectoriales en Adobe Photoshop.
-   Cree y use una capa de plantilla en Photoshop para asegurarse de que el trabajo se realiza en regiones cuadradas de los tamaños regulados.
-   Cree las imágenes en un tamaño un poco más pequeño que el tamaño de icono general para permitir el espacio para una sombra paralela (para aquellos tamaños que requieran una).
-   Coloque las imágenes en la parte inferior de los cuadrados para que todos los iconos de un directorio se coloquen de forma coherente. Evite la reducción de las sombras.
-   Si va a agregar otro objeto a una imagen o una serie, mantenga el objeto principal en una posición fija y colóquela en una posición fija, como la parte inferior izquierda o la parte superior derecha, según el caso.

**Paso 3: creación de las imágenes de 24 bits**

-   Una vez que haya pegado los tamaños en Photoshop, Compruebe la legibilidad de las imágenes, especialmente en tamaños de 16x16 y menores. Se pueden requerir píxeles-Poking con porcentajes de colores. También puede ser necesaria la reducción de la transparencia. Es habitual exagerar los aspectos en tamaños más pequeños y eliminar también los aspectos, con el fin de centrarse en el punto clave.
-   Los iconos de 8 bits se mostrarán en cualquier modo de color inferior a 32 bits y no tendrán el canal alfa de 8 bits, por lo que es posible que necesiten tener sus bordes o más limpiados porque no hay ningún suavizado de contorno (los bordes pueden ser más difíciles de leer).
-   En Photoshop, duplique la capa de imagen de 24 bits y cambie el nombre de la capa a imágenes de 4 bits. Indexar imágenes de 4 bits en la paleta de colores de Windows 16.
-   Limpie las imágenes con solo los colores de la paleta de 16 colores. Los esquemas realizados a partir de versiones más oscuras o claras de los colores del objeto suelen ser preferibles a gris o a negro.
-   Si trabaja en un mapa de bits, asegúrese de que el color de fondo no se usa en la propia imagen, ya que ese color será el color transparente. Magenta (R255 G0 B255) se utiliza a menudo como el color de transparencia de fondo.

**Paso 4: creación de las imágenes de 8 y 4 bits**

-   Ahora que las imágenes de 24 bits están listas para su realización en iconos de 32 bits, es necesario crear las versiones de 8 bits.
-   Es un buen momento para probar capturas de pantalla contextuales. Es asombroso lo que se puede detectar viendo otros iconos o una familia de iconos en contexto. Este paso puede ahorrar tiempo y dinero. Es mucho mejor detectar problemas antes de que los archivos pasen a la producción y se entreguen.
-   Agregue la sombra paralela a las imágenes en tamaños que las necesiten.
-   Combina la sombra paralela y las imágenes de 24 bits juntas.
-   Cree un nuevo archivo de Photoshop para cada tamaño. Copie y pegue la imagen adecuada. Guarde cada archivo como un archivo. psd.
-   No combine la capa de imagen con la capa de fondo. Resulta útil incluir el tamaño y la profundidad de color en el nombre de archivo mientras se trabaja, pero es posible que sea necesario cambiar el nombre del archivo en última instancia.

**Paso 5: crear el archivo. ico**

-   Elija la aplicación que mejor se adapte a sus necesidades y habilidades. Recuerde que los iconos que se van a usar en un producto de envío deben crearse en una herramienta que se haya adquirido o con licencia. Esto significa que no se pueden usar las versiones de prueba.
-   Los diseñadores que han generado iconos para Windows Vista han utilizado los dos productos que se enumeran a continuación y cada uno de ellos ofrece la capacidad de exportar a Adobe Photoshop CS.
    -   Gamani Gif Movie Gear: produce archivo. ico
    -   Icono axial: crear archivo. ico
-   Visual Studio no es compatible con los iconos de Windows Vista (no hay compatibilidad con el canal alfa o con más de 256 colores), por lo que no se recomienda su uso.
-   Los archivos de icono (formato. ico) deben contener las versiones de 4 y 8 bits, así como la versión de 24 bits + alfa.
-   Guarde los archivos como un "icono de Windows (. ico)" independientemente del programa de creación de iconos que decida usar.
-   Algunos recursos de iconographic pueden ser en realidad bandas de mapa de bits, que también requieren un canal alfa (por ejemplo, para las barras de herramientas) o archivos. png guardados con transparencia. No todos son necesariamente el formato. ico. Compruebe el formato que se admite en el código.

**Paso 6: evaluar**

-   Examine todos los tamaños.
-   Fíjese en la familia para evaluar la similitud de la familia, el equilibrio óptico y la distinción.
-   Fíjese en el contexto para evaluar los pesos y la visibilidad relativos (Asegúrese de que uno no domina).
-   Considere los casos que no se pueden usar ahora, pero que podrían estar en un futuro próximo. ¿Se puede anotar este icono o tener una superposición?
-   Vea en el código.

### <a name="icons-in-the-context-of-list-views-toolbars-and-tree-views"></a>Iconos en el contexto de vistas de lista, barras de herramientas y vistas de árbol

**Vistas de lista**

-   En Windows Vista, use vistas en miniatura para los archivos que contienen contenido que es visualmente distinto a pequeña escala, de modo que los usuarios puedan reconocer directamente el archivo que buscan. (Use la interfaz de programación de aplicaciones de miniaturas de Windows para esto).

    ![captura de pantalla del explorador de Windows con iconos de carpeta ](images/vis-icons-image22.png)

-   Las superposiciones de los iconos de aplicación (no se muestran aquí) en las miniaturas ayudan a asociar la aplicación para el tipo de archivo, además de mostrar la vista previa del archivo.

**Nota:** En el caso de los archivos sin contenido visualmente distinto, no use vistas en miniatura. En su lugar, use iconos de archivo simbólico tradicional que muestren la representación de objetos y la aplicación o el tipo asociados.

**Barras de herramientas**

-   Los iconos que aparecen en una barra de herramientas deben tener un equilibrio óptico en el tamaño, el color y la complejidad.
-   Pruebe los iconos potenciales en una captura de pantalla contextual para evitar cualquier dominio o desequilibrio no deseados.
-   Las pruebas en capturas de pantalla ayudan fácilmente a evitar iteraciones costosas en el código.
-   Revise también los iconos en el código. El movimiento y otros factores pueden afectar al éxito de un icono; en algunos casos, es posible que se necesiten más iteraciones.

![captura de pantalla de la barra de herramientas con iconos y etiquetas pequeños ](images/vis-icons-image23.png)

En el ejemplo anterior, todavía no se ha logrado el equilibrio óptico.

![Ilustración de iconos en distintos terrenos ](images/vis-icons-image24.png)

Pruebe las iteraciones en contexto.

**Vistas de árbol**

-   Se necesita equilibrio óptico para conservar la jerarquía en un control de vista de árbol.
-   Por lo tanto, los iconos que se usan normalmente en este contexto deben evaluarse ahí. A veces, un icono de 16x16 determinado debe ser más pequeño porque su forma tiene una dominación óptica sobre otros.
-   La compensación de los desequilibrios ópticos es una parte importante de la generación de iconos de alta calidad.

![figura de dos conjuntos de carpetas en la vista de árbol ](images/vis-icons-image25.png)

 

