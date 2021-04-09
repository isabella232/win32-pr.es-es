---
title: Elementos gráficos
description: Los elementos gráficos muestran relaciones, jerarquías y énfasis visualmente. Incluyen el fondo, los banners, el cristal, los agregadores, los separadores, las sombras y los controladores.
ms.assetid: f9e741e9-a72e-4bdb-bd95-8916c7cf344f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a452668bc1685143273df80fd144642a18019213
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104003285"
---
# <a name="graphic-elements"></a>Elementos gráficos

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

*Los elementos gráficos* muestran relaciones, jerarquías y énfasis visualmente. Incluyen el fondo, los banners, el cristal, los agregadores, los separadores, las sombras y los controladores.

![captura de pantalla del explorador de Windows con sombra, etc. ](images/vis-graphic-image1.png)

Ejemplo con varios tipos de elementos gráficos.

Los elementos gráficos no suelen ser interactivos. Sin embargo, los separadores son interactivos para contenido de tamaño ajustable y los controladores son gráficos que muestran interactividad.

**Nota:** Las instrucciones relacionadas con [cuadros de grupo](ctrl-group-boxes.md), [animaciones](vis-animations.md), [iconos](vis-icons.md)y [Personalización de marca](exper-branding.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Aunque los elementos gráficos son un medio visual seguro de indicar relaciones, si se sobreutilizan, se agrega confusión visual y se reduce el espacio disponible en una superficie. Deben usarse con moderación.

Una tendencia de diseño en Microsoft Windows es un aspecto más sencillo y limpio al eliminar gráficos y líneas innecesarios.

Para decidir si un elemento gráfico es necesario, tenga en cuenta estas preguntas:

-   **¿La presentación y la comunicación del diseño son tan claras y eficaces sin el elemento?** Si es así, quítelo.
-   **¿Puede comunicarse de forma eficaz las relaciones usando solo el diseño?** Si es así, utilice el [diseño](vis-layout.md) en su lugar. Puede colocar controles relacionados junto a otros y colocar el espaciado adicional entre los controles no relacionados. También puede utilizar la sangría para mostrar las relaciones jerárquicas.

![captura de pantalla de un diseño de cuatro iconos ](images/vis-graphic-image2.png)

En este ejemplo, el diseño solo se usa para mostrar las relaciones de control.

-   **¿La comunicación es eficaz sin texto?** Si no es así, use un [cuadro de grupo](ctrl-group-boxes.md), con la etiqueta separador u otra [etiqueta](text-ui.md).

## <a name="usage-patterns"></a>Patrones de uso

Los elementos gráficos tienen varios patrones de uso:



|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ilustraciones gráficas**<br/> Utilice para comunicar una idea visualmente. <br/>                         | Las ilustraciones gráficas son similares a los iconos, salvo que pueden tener cualquier tamaño y normalmente no son interactivas. <br/> ![gráfico del historial de uso de CPU de captura de pantalla ](images/vis-graphic-image3.png)<br/> En este ejemplo, se usa una ilustración gráfica para sugerir la naturaleza de una característica.<br/>                                                                                                                                                                                                        |
| **Fondos**<br/> Use para resaltar o anular el resaltado de diferentes tipos de contenido. <br/>           | Los trabajos en segundo plano se pueden usar para resaltar contenido importante. <br/> ![captura de pantalla del mensaje de virus en el fondo rojo ](images/vis-graphic-image4.png)<br/> en este ejemplo, se usa un fondo para resaltar una tarea importante.<br/> los trabajos en segundo plano también se pueden usar para desenfatizar el contenido secundario. <br/> ![captura de pantalla de los elementos del panel de control ](images/vis-graphic-image5.png)<br/> En este ejemplo, las tareas secundarias se desdestacan buscándolas en un panel de tareas.<br/>   |
| **Banners**<br/> se usa para indicar un estado importante. <br/>                                         | A diferencia de los terrenos, los banners resaltan principalmente una sola cadena de texto. <br/> ![captura de pantalla de banner con información de configuración ](images/vis-graphic-image6.png)<br/> En este ejemplo, se usa un banner para indicar que la configuración de la página se controla mediante directiva de grupo.<br/>                                                                                                                                                                                                       |
| **Vidrio**<br/> Use estratégicamente para reducir el peso visual de una ventana. <br/>                   | Glass puede reducir el peso de una superficie centrándose en el contenido en lugar de en la propia ventana. <br/> ![captura de pantalla de pájaro en la Galería fotográfica de Windows ](images/vis-graphic-image7.png)<br/> En este ejemplo, cristal centra la atención del usuario sobre el contenido en lugar de los controles.<br/>                                                                                                                                                                                                 |
| **Agregadores**<br/> Use para crear una relación visual entre los controles relacionados con la codificación. <br/> | ![captura de pantalla de flechas de navegación hacia atrás y hacia delante ](images/vis-graphic-image8.png)<br/> en este ejemplo, se usa un fondo del agregador para resaltar la relación entre los botones atrás y adelante del explorador.<br/> ![captura de pantalla de los controles de la Galería fotográfica de Windows ](images/vis-graphic-image7.png)<br/> En este ejemplo, se usa un agregador de límites para resaltar la relación entre los controles y hacer que se sientan como un único control en lugar de ocho.<br/> |
| **Separadores**<br/> se usa para separar controles no relacionados o débilmente relacionados. <br/>                   | Los separadores pueden ser interactivos o no interactivos. los separadores interactivos entre el contenido de tamaño variable se conocen como divisores. <br/> ![captura de pantalla del separador de separador para el botón de nombre ](images/vis-graphic-image9.png)<br/> en este ejemplo, se usa un separador interactivo para el contenido de tamaño variable.<br/> ![captura de pantalla del separador de información del explorador ](images/vis-graphic-image10.png)<br/> En este ejemplo, el separador no es interactivo.<br/>                  |
| **Shadows**<br/> Use para hacer que el contenido destaque visualmente con respecto a su fondo. <br/>             | ![captura de pantalla de cuatro fotos con sombras ](images/vis-graphic-image11.png)<br/> En este ejemplo, las sombras hacen que la ilustración destaque en el fondo.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Handles**<br/> se utiliza para indicar que un objeto puede moverse o cambiar de tamaño. <br/>                    | Los identificadores siempre son interactivos y el puntero del mouse sugiere su comportamiento al mantener el mouse. <br/> ![captura de pantalla de una esquina de ventana con el puntero de cambiar tamaño ](images/vis-graphic-image12.png)<br/> ![captura de pantalla del cuadro de selección con el puntero cambiar tamaño ](images/vis-graphic-image13.png)<br/> En estos ejemplos, los identificadores indican que se puede cambiar el tamaño de un objeto.<br/>                                                                                                                       |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **No transmita información esencial solo a través de elementos gráficos.** Al hacerlo, se presentan problemas de accesibilidad para los usuarios con discapacidades o discapacidades visuales.

### <a name="graphic-designs"></a>Diseños gráficos

-   **Los gráficos son más eficaces cuando refuerzan una sola idea sencilla.** Los gráficos complejos que requieren interpretación no funcionan bien. Hieroglyphics son los más adecuados para los dibujos de Cave.

    **Incorrecto:**

    ![captura de pantalla de advertencia con gráfico complejo ](images/vis-graphic-image14.png)

    En este ejemplo, un gráfico complejo de Windows XP intenta de manera ineficaz explicar una decisión de confianza compleja.

-   **No use flechas, comillas angulares, marcos de botones ni otras prestaciones asociadas a controles interactivos.** Al hacerlo, se invita a los usuarios a interactuar con los gráficos.
-   **Evite swaths de color rojo, amarillo y verde puro en los diseños.** Para evitar confusiones, Reserve estos colores para comunicar el estado. Si debe usar estos colores para algo que no sea el estado, utilice tonos silenciados en lugar de colores puros.
-   **Usar diseños culturalmente neutros.** Lo que puede tener un significado determinado en un país, región o referencia cultural puede no tener el mismo significado en otro.
-   **Evite el uso de personas, caras, sexos o partes del cuerpo, así como símbolos religiosos, políticos y nacionales.** Estas imágenes pueden no traducirse fácilmente o ser ofensivas.
-   **Cuando se debe representar a personas o usuarios, se describen de forma genérica.** Evite representaciones realistas.

### <a name="backgrounds-and-banners"></a>Fondo y banners

-   **Para enfatizar el contenido, use texto oscuro sobre un fondo claro.** El texto negro en un fondo gris claro o amarillo funciona bien.

    ![captura de pantalla del texto de vínculo azul en el fondo amarillo ](images/vis-graphic-image15.png)

    En este ejemplo, el vínculo obtiene la atención del usuario porque está en un fondo amarillo.

-   **Para deshacer el resaltado de contenido, use texto claro en un fondo oscuro.** El texto blanco sobre un fondo gris oscuro o azul funciona bien.

    ![captura de pantalla del vínculo de ayuda en blanco sobre fondo verde ](images/vis-graphic-image16.png)

    En este ejemplo, el fondo oscuro desenfatiza el contenido.

-   **Si se usa un degradado, asegúrese de que el color del texto tenga un buen contraste en todo el degradado.**
-   **Use siempre un icono de 16x16 píxeles para atraer la atención al banner.** En caso contrario, los banners son demasiado fáciles de pasar por alto. Para obtener más instrucciones y ejemplos, vea [iconos estándar](vis-std-icons.md).
-   **Use el fondo y los banners con precaución.** Aunque el objetivo del fondo o el banner puede ser enfatizar el contenido, a menudo los resultados son lo opuesto a un fenómeno conocido como "banner persiana".

### <a name="glass"></a>Vidrio

-   **Considere la posibilidad de usar Glass estratégicamente en regiones pequeñas que tocan el marco de la ventana sin texto.** Si lo hace, puede dar un aspecto más sencillo, más ligero y coherente haciendo que la región parezca parte del marco.
-   **No use cristal en situaciones en las que un fondo de ventana sin formato sea más atractivo o fácil de usar.**

### <a name="separators"></a>Separadores

-   **Use líneas verticales y horizontales para los separadores.** Asegúrese de tener espacio suficiente entre los separadores y el contenido que se va a separar.
-   En el caso de los separadores entre el contenido de tamaño ajustable (separadores), se muestra el puntero de cambiar tamaño al mantener el mouse.

![Captura de pantalla que muestra un divisor con el puntero de cambiar tamaño.](images/vis-graphic-image17.png)

![captura de pantalla del divisor con el puntero de cambiar tamaño ](images/vis-graphic-image18.png)

En estos ejemplos, los punteros de cambiar tamaño se muestran al mantener el mouse.

### <a name="shadows"></a>Shadows

-   **Use solo para que el contenido más significativo del programa o los objetos que se arrastran se destaquen visualmente con respecto a su fondo.** Considere la posibilidad de que las sombras tengan un desorden visual en otras circunstancias.

### <a name="high-dpi-support"></a>Compatibilidad con PPP alta

-   **Admite los modos de vídeo 96 y 120 puntos por pulgada (PPP).** Detecta el modo DPI en el inicio y controla los eventos de cambio de PPP. Windows está optimizado para 96 y 120 ppp, y utiliza de forma predeterminada 96 ppp.
-   **Es preferible proporcionar mapas de bits independientes que se representen específicamente para 96 y 120 ppp sobre el escalado de gráficos.** Proporcionar al menos 96 y 120 ppp para los mapas de bits más importantes y visibles, y para centrar o escalar los demás. Estas aplicaciones se consideran "con reconocimiento de PPP alto" y proporcionan una mejor experiencia visual general que los programas escalados automáticamente por Windows.
    -   Desarrolladores: puede declarar un programa con reconocimiento de PPP alto (y evitar el escalado automático) estableciendo la marca de reconocimiento de PPP en el manifiesto del programa o llamando a la API SetProcessDPIAware () durante la inicialización del programa. Puede usar macros para simplificar la selección de los gráficos adecuados. En el caso de los mapas de bits de Win32, puede usar SS \_ CENTERIMAGE para centrar o SS \_ REALSIZECONTROL para escalar.
-   Compruebe el programa en 96 y 120 ppp para:
    -   Gráficos demasiado pequeños o demasiado grandes.
    -   Gráficos que se van a recortar, superponer o no ajustar correctamente.
    -   Gráficos que no se ajustan correctamente ("pixelado").
    -   Texto que se recorta o no se ajusta en el fondo gráfico.

## <a name="text"></a>Texto

-   **Para la accesibilidad y la localización, no use ningún texto en los gráficos.** Haga excepciones solo para representar la [Personalización de marca](exper-branding.md) y el texto como concepto abstracto.

 

