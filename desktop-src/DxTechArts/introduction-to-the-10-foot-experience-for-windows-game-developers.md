---
title: Introducción a la experiencia de 10 pies para desarrolladores Windows juegos
description: En este artículo se presenta la experiencia de 10 pies y se explora la lista de cosas que debe tener en cuenta primero sobre este nuevo patrón de interacción, incluso si no espera que el juego se jugará de esta manera.
ms.assetid: 126a0aae-6a7a-8cda-5748-c364e54c304e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049cbbe839509681f8f8629144511853d2984bbabafbf989611d1ed1db32e686
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963625"
---
# <a name="introduction-to-the-10-foot-experience-for-windows-game-developers"></a>Introducción a la experiencia de 10 pies para desarrolladores Windows juegos

Cada vez más personas usan sus equipos personales de una manera completamente nueva. Cuando se piensa en la interacción típica con un equipo basado en Windows, probablemente piense en estar sentado en un escritorio con un monitor y usando un mouse y un teclado (o quizás un dispositivo portátil). Esto se conoce como la experiencia de 2 pies y sigue siendo el escenario más común para juegos de Windows, pero hay otra tendencia sobre la que probablemente empezará a escuchar más: la experiencia de 10 pies, que describe el uso del equipo como un dispositivo de entretenimiento con salida a un televisor. En este artículo se presenta la experiencia de 10 pies y se explora la lista de cosas que debe tener en cuenta primero sobre este nuevo patrón de interacción, incluso si no espera que el juego se jugará de esta manera. Una parte de los clientes ejecutará el juego basado en Windows en un equipo que ejecuta Windows Media Center; es mejor que sepa cómo será esa experiencia antes de que los clientes lo prueben.

-   [¿Qué es Windows Media Center?](#what-is-windows-media-center)
-   [La experiencia de 10 pies](#the-10-foot-experience)
    -   [Instalación](#installation)
    -   [Entrada del usuario](#user-input)
    -   [Pantalla](#display)
-   [Relación de aspecto y Widescreen](#aspect-ratio-and-widescreen)
-   [Región de Caja fuerte título](#title-safe-region)
-   [Sugerencias de GESTIÓN](#ntsc-suggestions)
    -   [Fijación de los valores de los componentes de color RGB entre 16 y 235](#clamp-the-rgb-color-component-values-between-16-and-235)
    -   [Evitar colores similares que puedan parecer idénticos](#avoid-similar-colors-that-might-appear-identical)
    -   [Evitar diferencias nítibles en el contraste](#avoid-sharp-differences-in-contrast)
-   [Conclusión](#conclusion)

## <a name="what-is-windows-media-center"></a>¿Qué es Windows Media Center?

Windows Media Center puede actuar como la interfaz de las funcionalidades multimedia del equipo host. El sitio web de esta característica, Windows Inicio de [Media Center,](https://windows.microsoft.com/windows/products/windows-media-center/)ofrece una introducción exhaustiva y muestra todo lo bueno disponible en la versión más reciente. Media Center se incluye en Windows XP Media Center Edition, Windows Vista Home Premium, Windows Vista Ultimate y la mayoría de las ediciones de Windows 7.

En el pasado, la única manera de obtener Windows Media Center era comprar un equipo de Media Center a un fabricante del sistema de nivel 1, pero como Windows Media Center ahora se incluye con dos ediciones de Windows Vista, el marketplace potencial ahora es mucho mayor.

## <a name="the-10-foot-experience"></a>La experiencia de 10 pies

Windows Media Center se diseñó en torno a la idea de que las personas podían usar Windows para disfrutar de una experiencia de entretenimiento en una sala de estar enriquección, y se sigue que la mayoría de los usuarios prefieren interactuar de manera diferente con Windows Media Center de forma diferente que con las aplicaciones informáticas tradicionales. Por un lado, si el cliente usa el equipo en la sala para el entretenimiento, es probable que el vídeo se muestre en algo que no sea un monitor de equipo convencional: los televisores análogos, los televisores digitales de alta definición y cualquier número de pantallas DE LAV son candidatos probables. Estos tipos de pantallas normalmente se ven desde una distancia de aproximadamente 10 pies, de ahí la experiencia de *etiqueta de 10 pies*.

La experiencia de 10 pies no se limita a los usuarios de Windows Media Center. En los últimos años, es habitual que los usuarios conecten su estación de trabajo o equipo de cuadernos a su sistema de audio y televisión. Cada vez es más común que los dispositivos de visualización del consumidor exponían conexiones RGB o DVI, los puertos de salida de vídeo estándar en los equipos. Además, los puertos S-Video son una característica típica de las tarjetas de vídeo de gama alta y ofrecen una manera sencilla de generar salidas en un dispositivo de visualización alternativo.

Hay algunas directrices de diseño importantes que se deben tener en cuenta para una experiencia agradable de 10 pies: instalación, entrada del usuario y visualización.

### <a name="installation"></a>Instalación

Durante la experiencia media de 2 pies, el usuario está a una distancia de alcance del equipo. Si durante el inicio o el juego, el usuario tiene que insertar o cambiar de medio, el usuario puede permanecer al menos sentado. La experiencia media de 10 pies coloca el equipo a través de la habitación del usuario y, por tanto, cualquier cosa que requiera que el usuario interactúe físicamente con el equipo obliga al usuario a rse y atravesar la habitación. Por esta razón, los desarrolladores deben evitar forzar al usuario a cambiar los medios. considere la posibilidad de permitir una instalación completa de la aplicación en el disco duro.

### <a name="user-input"></a>Entrada del usuario

Otra característica de Windows Media Center es la compatibilidad con un control remoto estándar, que es el dispositivo de entrada preferido por lo general. Aunque el género del título del juego decide en gran medida si el control remoto es adecuado para proporcionar la entrada del juego, es posible que quiera permitir al usuario pausar el juego y acceder a los menús del juego mediante el control remoto. sin embargo, asegúrese de que también permite al usuario controlar los menús mediante el dispositivo de entrada del juego principal. Para obtener más información sobre el diseño y el desarrollo para Windows Media Center y sus dispositivos, vea Windows Kit de desarrollo de software de [Media Center](/previous-versions/msdn10/bb895967(v=msdn.10)) en MSDN.

Evite cualquier interacción física entre el usuario y el equipo o sus periféricos. No se desea exigir al usuario que cambie los controladores de entrada durante el juego, ya que es probable que esté cerca solo del dispositivo de entrada principal.

Microsoft ha creado controladores de controlador de juegos comunes para su uso con Windows y Xbox 360, el Mando Xbox 360 para Windows y el Mando inalámbrico Xbox 360 para Windows. Asegurarse de que el título se desempeña bien en los controladores comunes le ayudará a mitigar algunos de los problemas asociados a probar el juego con posibles dispositivos de entrada.

### <a name="display"></a>Mostrar

La amplia gama de posibles dispositivos de pantalla ofrece consejos sobre la presentación complicada y cada tipo de dispositivo tiene advertencias especiales. Algunos de los problemas relacionados con tecnologías de visualización específicas se presentan más adelante en este documento. Independientemente del dispositivo de salida de vídeo, es importante que las fuentes y los gráficos de interfaz de usuario tienen el tamaño suficiente para una legibilidad cómoda a una distancia de 10 pies. Tenga en cuenta también que las fuentes con suavizado de contorno suelen ofrecer una mejor legibilidad.

También debe evitar líneas horizontales y elementos de interfaz de usuario estáticos con grosor o detalle de un solo píxel. Es posible que los televisores más antiguos no muestren detalles detallados e incluso en los dispositivos de pantalla más recientes, el contenido parpadeará cuando se ejecute en un modo entrelazado, ya que una sola fila de píxeles solo está visible la mitad del tiempo. Como sustituto de detalles pequeños, debe tener en cuenta que una línea gris de 2 píxeles parece más fina que una línea blanca de 2 píxeles. (Esto es básicamente lo mismo que desenfocar una línea blanca de 1 píxel).

## <a name="aspect-ratio-and-widescreen"></a>Relación de aspecto y Widescreen

La relación de aspecto describe la proporción de ancho y alto de la pantalla. Las pantallas estándar de monitor de tv y equipo tienen una relación de aspecto de 4:3, lo que significa que por cada 4 píxeles que se ejecutan a lo largo del ancho del búfer de fotogramas, hay 3 píxeles a lo largo de la altura (a veces también se representan como 1,33).

Con la llegada de LAV, una relación de aspecto de 16:9(también conocida como pantalla ancha) se ha convertido en el estándar para el futuro de la televisión y, junto con la televisión de definición mejorada (EDTV), es probable que encuentre tres modos de pantalla:

<dl> <dt>

<span id="480p_EDTV"></span><span id="480p_edtv"></span><span id="480P_EDTV"></span>EDTV de 480p
</dt> <dd>

480 líneas de examen presentadas progresivamente. Este modo puede generar 4:3 (con una resolución de búfer de fotogramas de 640×480) o 16:9 (720×480).

</dd> <dt>

<span id="720p_HDTV"></span><span id="720p_hdtv"></span><span id="720P_HDTV"></span>720pPTO
</dt> <dd>

720 líneas de examen presentadas progresivamente. Este modo es siempre 16:9 (1280×720).

</dd> <dt>

<span id="1080i_HDTV"></span><span id="1080i_hdtv"></span><span id="1080I_HDTV"></span>1080i INN
</dt> <dd>

1080 líneas de examen presentadas entrelazadas. Este modo es siempre 16:9 (1920×1080 o 1920×540 si se representa los campos de intercalación por separado).

</dd> </dl>

Si el juego está codificado de forma definida para funcionar en una relación de aspecto de 4:3, es probable que un usuario que ve el juego en una pantalla de 16:9 tenga tres opciones para mostrar la imagen, ninguna de las cuales es especialmente satisfactoria:

<dl> <dt>

<span id="Stretch"></span><span id="stretch"></span><span id="STRETCH"></span>elasticidad
</dt> <dd>

El búfer de fotogramas 4:3 se ajusta para cubrir perfectamente la resolución nativa de 16:9 de la pantalla, lo que da lugar a que los objetos de escena parezcan más anchos de lo deseado. Algunos televisores ofrecen modos de stretch adicionales que intentan conservar la relación de aspecto cerca del centro de la pantalla y aumentar gradualmente el stretch en los lados de la imagen.

</dd> <dt>

<span id="Center"></span><span id="center"></span><span id="CENTER"></span>Centro
</dt> <dd>

El búfer de fotogramas 4:3 se muestra sin cambios en el centro de la pantalla, con barras de color sólidas que rellenan los píxeles restantes en los lados.

</dd> <dt>

<span id="Zoom"></span><span id="zoom"></span><span id="ZOOM"></span>Zoom
</dt> <dd>

El búfer de fotogramas 4:3 se recorta a una región 16:9, que luego rellena la resolución de pantalla nativa sin distorsión; Tenga en cuenta que los píxeles situados por encima y debajo del rectángulo de recorte se descartan completamente, que son regiones comunes para los elementos de la interfaz de usuario de un juego.

</dd> </dl>

Un enfoque mejor es agregar compatibilidad con la pantalla ancha al juego. El cambio más importante es establecer la transformación de proyección de la cámara del juego para usar una relación de aspecto de 16:9, lo que evita la distorsión del ajuste. Incluso si deja el búfer de reserva con una resolución de 4:3, cambiar la transformación de proyección para usar 16:9 mejora en gran medida la precisión percibida de la imagen representada; Por supuesto, la imagen final se filtra para ampliar la resolución del búfer de reserva 4:3 para satisfacer la resolución de pantalla nativa de 16:9, pero se trata de un artefacto menos perceptible que la distorsión de la extensión causada por una discrepancia de relaciones de aspecto.

El costo de representar la escena a través de una cámara de 16:9 puede ser mayor que una cámara de 4:3 (incluso con resoluciones idénticas), ya que más objetos de escena serán visibles en la vista más ancha. También debe tener en cuenta cómo el área visualizable ampliada puede influir en el juego; Por ejemplo, una cámara de juego con una relación de 16:9 revelaría más de su mundo del juego que una cámara de 4:3.

Para obtener los mejores resultados en una pantalla de 16:9, debe representar en un búfer de reserva de 16:9, pero esto obviamente requerirá rellenar más píxeles. La diferencia entre 640×480 y 720×480 es de casi 38 400 píxeles, una ganancia del 12,5 %. Si puede permitirse el costo de rellenar esta área más grande, se recomienda encarecidamente hacerlo.

## <a name="title-safe-region"></a>Title-Safe región

El búfer del marco de imagen podría estar parcialmente oculto del usuario, ya que algunos píxeles alrededor del borde suelen estar cubiertos por el bisel frontal de la pantalla. Para asegurarse de que los elementos críticos de la interfaz de usuario están visibles en una amplia variedad de hardware de pantalla, debe observar los requisitos de la región segura para el título del modo de presentación de destino. En el caso de los modos que no son DEN, la región segura para título es el 85 % interno del búfer de fotogramas y, para los modos DESTE, el área segura para título es el 90 % interno. Por lo tanto, para obtener la máxima compatibilidad en el hardware de visualización actual y futuro, debe mantener todos los elementos críticos de la interfaz de usuario y los indicadores de visualización de cara al 85 % interno del búfer de fotogramas.

## <a name="ntsc-suggestions"></a>Sugerencias de GESTIÓN

Puesto que el estándar de vídeo más común de Estados Unidos es el hardware de visualización del consumidor, es importante conocer algunas de las directrices que debe seguir para la imagen de salida.

### <a name="clamp-the-rgb-color-component-values-between-16-and-235"></a>Fijación de los valores de los componentes de color RGB entre 16 y 235

Los colores que están fuera del intervalo de 16 a 235 se pueden enviar sin duda a un televisor NINGUNA, pero es probable que estos valores fuera del intervalo se interpreten como datos de audio. Esto suele denominarse *sonido sonrón* y sería más evidente si el contenido se presentara sobre un fondo blanco sólido. Puede implementar fácilmente la fijación del color de salida dentro de un sombreador de píxeles.

### <a name="avoid-similar-colors-that-might-appear-identical"></a>Evitar colores similares que puedan parecer idénticos

La gama de colores GADO no ofrece la misma paleta que un monitor de equipo típico, así que evite usar colores similares siempre que el juego requiera que el jugador reconozca la diferencia.

### <a name="avoid-sharp-differences-in-contrast"></a>Evitar diferencias nítibles en el contraste

Aunque esta guía no siempre es práctica, puede mitigar algunas de las molestias de color en las pantallas de RADO (también conocidas como rastreo de *arrastre)* mediante la selección de los colores adecuados para los elementos de primer plano y fondo de la interfaz de usuario. el texto en blanco en un fondo coloreado probablemente dará mejores resultados que los colores de contraste.

## <a name="conclusion"></a>Conclusión

En este artículo se ha ofrecido un vistazo a la experiencia de 10 pies desde la perspectiva de un desarrollador de juegos de Windows, pero no es una encuesta completa. Debe investigar más estos temas si está desarrollando un título de juego Windows (incluso si no está pensado para su uso con Windows Media Center). La verdadera prueba es probar el juego en una variedad de pantallas de vídeo para asegurarse de que el juego ofrece una experiencia increíble en cada una de ellas. En función de la duración típica de un juego basado en Windows y el crecimiento previsto en el uso de Windows Media Center, está casi garantizado que un juego que se publica hoy forma parte de la experiencia de 10 pies de alguien, independientemente de si los clientes pueden jugar a su juego desde la comodidad de los diván o se ven obligados a quedarse sentados en el escritorio depende en gran medida de usted.

 

 