---
title: Introducción a la experiencia de 10 pies para los desarrolladores de juegos de Windows
description: En este artículo se presenta la experiencia de 10 pies y se explora la lista de cosas que debe tener en cuenta en primer lugar sobre este nuevo patrón de interacción, incluso si no está esperando que el juego se reproduzca de esta manera.
ms.assetid: 126a0aae-6a7a-8cda-5748-c364e54c304e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4814c76aeefdadbe1fd8bf9dc4c21cd84612671
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421538"
---
# <a name="introduction-to-the-10-foot-experience-for-windows-game-developers"></a>Introducción a la experiencia de 10 pies para los desarrolladores de juegos de Windows

Un número cada vez mayor de personas está usando sus equipos personales de una forma totalmente nueva. Cuando se crea una interacción típica con un equipo basado en Windows, es probable que se esté trabajando en el escritorio con un monitor, y usando un mouse y un teclado (o quizás un dispositivo de joystick). Esto se conoce como la experiencia de 2 pies y sigue siendo el escenario más común para juegos de Windows, pero hay otra tendencia en la que probablemente comenzará más sobre: la experiencia de 10 pies, que describe el uso del equipo como un dispositivo de entretenimiento con la salida a un televisor. En este artículo se presenta la experiencia de 10 pies y se explora la lista de cosas que debe tener en cuenta en primer lugar sobre este nuevo patrón de interacción, incluso si no está esperando que el juego se reproduzca de esta manera. Parte de sus clientes ejecutarán su juego basado en Windows en un equipo que ejecuta Windows Media Center, es mejor que sepa cuál será la experiencia antes de que los clientes la prueben.

-   [¿Qué es Windows Media Center?](#what-is-windows-media-center)
-   [La experiencia de 10 pies](#the-10-foot-experience)
    -   [Instalación](#installation)
    -   [Datos proporcionados por el usuario](#user-input)
    -   [Pantalla](#display)
-   [Relación de aspecto y pantalla panorámica](#aspect-ratio-and-widescreen)
-   [Región segura de título](#title-safe-region)
-   [Sugerencias NTSC](#ntsc-suggestions)
    -   [Abrazadera los valores de componente de color RGB entre 16 y 235](#clamp-the-rgb-color-component-values-between-16-and-235)
    -   [Evite colores similares que puedan parecer idénticos](#avoid-similar-colors-that-might-appear-identical)
    -   [Evitar diferencias nítidas en contraste](#avoid-sharp-differences-in-contrast)
-   [Conclusión](#conclusion)

## <a name="what-is-windows-media-center"></a>¿Qué es Windows Media Center?

Windows Media Center puede actuar como la interfaz de las capacidades multimedia del equipo host. En el sitio web de esta característica, en la [Página principal de Windows Media Center](https://windows.microsoft.com/windows/products/windows-media-center/), se ofrece una introducción detallada y se muestran todos los buenos materiales disponibles en la versión más reciente. Media Center se incluye en Windows XP Media Center Edition, Windows Vista Home Premium, Windows Vista Ultimate y la mayoría de las ediciones de Windows 7.

En el pasado, la única manera de obtener Windows Media Center era comprar un equipo con Media Center desde un fabricante del sistema de nivel 1, pero como Windows Media Center ahora se incluye con dos ediciones de Windows Vista, el posible Marketplace es ahora mucho más grande.

## <a name="the-10-foot-experience"></a>La experiencia de 10 pies

Windows Media Center se diseñó pensando en la idea de que los usuarios podían usar Windows para disfrutar de una experiencia de entretenimiento de sala de reuniones enriquecida y de que la mayoría de los usuarios prefieren interactuar de manera diferente con Windows Media Center de manera diferente que con las aplicaciones de equipos tradicionales. En el caso de una, si el cliente usa el equipo en el salón para el entretenimiento, es probable que el vídeo se muestre en algo que no sea un monitor de equipo convencional: los televisores analógicos, los televisores digitales de alta definición y cualquier número de pantallas LCD son posibles candidatos. Normalmente, estos tipos de pantallas se ven a partir de una distancia de aproximadamente 10 pies; por lo tanto, la *experiencia de 10 pies* de etiqueta.

La experiencia de 10 pies no se limita a los usuarios de Windows Media Center; en los últimos años, los usuarios pueden conectar su equipo de estación de trabajo o portátil a su sistema de TV y audio. Cada vez es más común que los dispositivos de visualización del consumidor expongan conexiones RGB o DVI, los puertos de salida de vídeo estándar en los equipos. Además, los puertos S-video son una característica típica de las tarjetas de vídeo de alta gama y ofrecen una manera sencilla de generar un dispositivo de pantalla alternativo.

Hay algunas directrices de diseño importantes que se deben tener en cuenta para una experiencia agradable de 10 pies: instalación, entrada de usuario y visualización.

### <a name="installation"></a>Instalación

Durante el promedio de la experiencia de 2 pies, el usuario se encuentra al alcance de la distancia del equipo; Si durante el inicio o el juego, el usuario debe insertar o cambiar el medio, el usuario puede permanecer colocado al menos. La experiencia media de 10 pies coloca el equipo a través de la habitación del usuario y, por lo tanto, todo lo que requiere que el usuario interactúe físicamente con el equipo obliga al usuario a ponerse en marcha y cruzar el salón. Por esta razón, los desarrolladores deben evitar obligar al usuario a cambiar los medios. considere la posibilidad de permitir una instalación completa de la aplicación en el disco duro.

### <a name="user-input"></a>Entrada del usuario

Otra característica de Windows Media Center es la compatibilidad con un control remoto estándar, que es el dispositivo de entrada preferido en general. Aunque el género del título del juego decide en gran medida si el control remoto es adecuado para proporcionar entradas de juego, es posible que desee permitir que el usuario PAUSE el juego y acceda a los menús del juego mediante el control remoto. sin embargo, asegúrese de que también permite que el usuario controle los menús mediante el dispositivo de entrada principal del juego. Para obtener más información sobre el diseño y el desarrollo de Windows Media Center y sus dispositivos, vea el [Kit de desarrollo de software de Windows Media Center](/previous-versions/msdn10/bb895967(v=msdn.10)) en MSDN.

Evite cualquier interacción física entre el usuario y el equipo o sus periféricos. Requerir que el usuario cambie los controladores de entrada durante el juego no es deseable, ya que es probable que esté cerca del dispositivo de entrada principal.

Microsoft ha creado controladores de controlador de juegos comunes para su uso con Windows y Xbox 360: la controladora Xbox 360 para Windows y la controladora inalámbrica Xbox 360 para Windows. Asegurarse de que el título se reproduzca correctamente en los controladores comunes facilitará algunos de los problemas asociados con la prueba del juego contra posibles dispositivos de entrada.

### <a name="display"></a>Pantalla

La amplia gama de posibles dispositivos de visualización ofrece consejos sobre cómo mostrar un desafío y cada tipo de dispositivo tiene advertencias especiales. Algunos de los problemas relacionados con las tecnologías de pantalla específicas se incluyen más adelante en este documento. Independientemente del dispositivo de salida de vídeo, es importante que las fuentes y los gráficos de interfaz de usuario tengan un tamaño lo suficientemente grande como para facilitar la lectura a una distancia de 10 metros. Tenga en cuenta también que las fuentes alisadas suelen ofrecer una mejor legibilidad.

También debe evitar líneas horizontales y elementos de interfaz de usuario estática con un grosor o un detalle de un solo píxel. Es posible que los televisores anteriores no muestren detalles y, incluso en los dispositivos de pantalla más recientes, el contenido parpadee cuando se ejecuta en un modo entrelazado, ya que una sola fila de píxeles solo es visible la mitad del tiempo. Como sustituto de los detalles pequeños, observe que una línea gris de 2 píxeles aparece más fina que una línea en blanco de 2 píxeles. (Esto es esencialmente lo mismo que desenfocar una línea en blanco de 1 píxel).

## <a name="aspect-ratio-and-widescreen"></a>Relación de aspecto y pantalla panorámica

Relación de aspecto describe la proporción de ancho y alto de la pantalla. Las pantallas de TV y monitor de equipo estándar tienen una relación de aspecto de 4:3, lo que significa que, para cada 4 píxeles que se ejecutan a lo largo del ancho del búfer de fotogramas, hay 3 píxeles a lo largo del alto (a veces también se representa como 1,33).

Con la llegada de HDTV, una relación de aspecto de 16:9, también conocida como pantalla ancha, se ha convertido en el estándar para el futuro de la televisión y, junto con el televisor de definición mejorada (EDTV), hay tres modos de presentación que es probable que encuentre:

<dl> <dt>

<span id="480p_EDTV"></span><span id="480p_edtv"></span><span id="480P_EDTV"></span>480p EDTV
</dt> <dd>

480 líneas de análisis que se muestran progresivamente. Este modo puede generar 4:3 (con una resolución de búfer de fotogramas de 640 × 480) o 16:9 (720 × 480).

</dd> <dt>

<span id="720p_HDTV"></span><span id="720p_hdtv"></span><span id="720P_HDTV"></span>HDTV de 720p
</dt> <dd>

720 líneas de análisis que se muestran progresivamente. Este modo siempre es 16:9 (1280 × 720).

</dd> <dt>

<span id="1080i_HDTV"></span><span id="1080i_hdtv"></span><span id="1080I_HDTV"></span>HDTV 1080i
</dt> <dd>

1080 líneas de análisis que se muestran entrelazadas. Este modo siempre es 16:9 (1920 × 1080 o 1920 × 540 si se representan los campos entrelazados por separado).

</dd> </dl>

Si el juego está codificado de forma rígida para que funcione en una relación de aspecto de 4:3, es probable que un usuario que vea el juego en una pantalla de 16:9 tenga tres opciones para mostrar la imagen, en la que no se satisfagan especialmente:

<dl> <dt>

<span id="Stretch"></span><span id="stretch"></span><span id="STRETCH"></span>Adapta
</dt> <dd>

El búfer de fotogramas 4:3 se expande para abarcar perfectamente la resolución nativa 16:9 de la pantalla, lo que da lugar a que los objetos de la escena aparezcan más anchos de lo deseado. Algunos televisores ofrecen modos elástico adicionales que intentan conservar la relación de aspecto cerca del centro de la pantalla y aumentan gradualmente el estiramiento en los lados de la imagen.

</dd> <dt>

<span id="Center"></span><span id="center"></span><span id="CENTER"></span>Centro
</dt> <dd>

El búfer de fotogramas 4:3 se muestra sin distorsionar en el centro de la pantalla, con barras de color sólido que rellenan los píxeles restantes en los lados.

</dd> <dt>

<span id="Zoom"></span><span id="zoom"></span><span id="ZOOM"></span>General
</dt> <dd>

El búfer de fotogramas 4:3 se recorta a una región 16:9, que, a continuación, rellena la resolución de pantalla nativa sin Distorsiones; Tenga en cuenta que los píxeles situados por encima y por debajo del rectángulo de recorte se descartan por completo, que son regiones comunes de los elementos de la interfaz de usuario de un juego.

</dd> </dl>

Un mejor enfoque es agregar compatibilidad con la presentación de pantalla ancha al juego. El cambio más importante es establecer la transformación de proyección de la cámara de juego para que use una relación de aspecto 16:9, lo que evita la distorsión de la ampliación. Incluso si deja el búfer de reserva en una resolución 4:3, al cambiar la transformación de proyección para que use 16:9 se mejora en gran medida la precisión percibida de la imagen representada; por supuesto, la imagen final se filtra para escalar la resolución del búfer de reserva 4:3 para cumplir con la resolución de pantalla nativa 16:9, pero se trata de un artefacto menos apreciable que la distorsión de stretch causada por una incoherencia de las proporciones de aspecto.

El costo de representar la escena a través de la cámara 16:9 puede ser mayor que una cámara 4:3 (incluso con resoluciones idénticas), porque hay más objetos de escena visibles en el frustum de vista más amplio. También debe tener en cuenta cómo el área visible ampliada puede influir en el juego; por ejemplo, una cámara de juegos con una relación 16:9 revelaría más de su mundo de juego que una cámara 4:3.

Para obtener los mejores resultados en una pantalla 16:9, debe representar en un búfer de reserva de 16:9, pero esto requerirá rellenar más píxeles. La diferencia entre 640 × 480 y 720 × 480 es casi 38.400 píxeles, una ganancia del 12,5%. Si puede permitirse el costo de rellenar este área más grande, es muy recomendable hacerlo.

## <a name="title-safe-region"></a>Title-Safe región

El búfer de fotogramas de imagen podría ocultarse parcialmente del usuario, porque algunos píxeles alrededor del borde suelen estar cubiertas por el bisel frontal de la pantalla. Para asegurarse de que los elementos críticos de la interfaz de usuario están visibles en una amplia variedad de hardware de pantalla, debe observar los requisitos de la región de título seguro para el modo de presentación de destino. En el caso de los modos que no son de HDTV, la región de título seguro es el 85 por ciento interno del búfer de fotogramas, y para los modos de HDTV, el área de título seguro es el 90 por ciento interno. Por lo tanto, para obtener la mayor compatibilidad entre el hardware de pantalla actual y el futuro, debe mantener todos los elementos críticos de la interfaz de usuario y los indicadores de visualización de los encabezados dentro del 85 por ciento interno del búfer de fotogramas.

## <a name="ntsc-suggestions"></a>Sugerencias NTSC

Dado que NTSC es el estándar de vídeo más común en el Estados Unidos para el hardware de visualización del consumidor, es importante conocer algunas de las instrucciones que debe seguir para la imagen de salida.

### <a name="clamp-the-rgb-color-component-values-between-16-and-235"></a>Abrazadera los valores de componente de color RGB entre 16 y 235

Los colores que se encuentran fuera del intervalo de 16-235 pueden enviarse a un televisor NTSC, pero es probable que estos valores fuera del intervalo se interpreten como datos de audio. Esto se suele denominar *zumbidos de audio* y sería más aparente si el contenido se presentara sobre un fondo blanco sólido. Puede implementar fácilmente la compresión del color de salida dentro de un sombreador de píxeles.

### <a name="avoid-similar-colors-that-might-appear-identical"></a>Evite colores similares que puedan parecer idénticos

La gama de colores NTSC no ofrece la misma paleta que un monitor de equipo típico, por lo que evite el uso de colores similares siempre que el juego requiera que el jugador reconozca la diferencia.

### <a name="avoid-sharp-differences-in-contrast"></a>Evitar diferencias nítidas en contraste

Aunque esta directriz no siempre es práctica de seguir, puede mitigar algunas de las molestias de sangrado de color en las pantallas NTSC (también conocido como *rastreo de croma*) seleccionando los colores adecuados para los elementos de primer plano y de fondo de la interfaz de usuario; el texto en blanco sobre un fondo de color probablemente dará mejores resultados que los colores de contraste.

## <a name="conclusion"></a>Conclusión

En este artículo se ofrece una visión general de la experiencia de 10 pies desde la perspectiva de un desarrollador de juegos de Windows, pero no se trata de una encuesta completa; debe investigar estos temas más allá si está desarrollando un título de juego de Windows (aunque no esté diseñado para su uso con Windows Media Center). La prueba verdadera es probar el juego en una variedad de pantallas de vídeo para asegurarse de que el juego ofrezca una experiencia agradable en cada uno. En función del ciclo de vida típico de un juego basado en Windows y el crecimiento previsto en el uso de Windows Media Center, se garantiza que un juego que publique hoy es parte de la experiencia de 10 pies de un tercero, tanto si los clientes pueden jugar su juego desde la comodidad de los sofá como si están obligados a sentarse en el escritorio.

 

 