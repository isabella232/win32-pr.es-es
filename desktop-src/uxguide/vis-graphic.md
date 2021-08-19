---
title: Elementos gráficos
description: Los elementos gráficos muestran las relaciones, la jerarquía y el énfasis visualmente. Incluyen fondos, banners, gafas, agregadores, separadores, sombras y identificadores.
ms.assetid: f9e741e9-a72e-4bdb-bd95-8916c7cf344f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: cc4b5ce620660e655eeee81cab869909c14b4f8290b5852da7f480da85951a5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936238"
---
# <a name="graphic-elements"></a>Elementos gráficos

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

*Los elementos gráficos* muestran las relaciones, la jerarquía y el énfasis visualmente. Incluyen fondos, banners, gafas, agregadores, separadores, sombras y identificadores.

![captura de pantalla del Explorador de Windows con sombra, etc. ](images/vis-graphic-image1.png)

Ejemplo con varios tipos de elementos gráficos.

Los elementos gráficos no suelen ser interactivos. Sin embargo, los separadores son interactivos para el contenido de tamaño ajustable y los identificadores son gráficos que muestran interactividad.

**Nota:** Las instrucciones relacionadas con [cuadros de](ctrl-group-boxes.md)grupo, [animaciones,](vis-animations.md) [iconos](vis-icons.md)y [personal](exper-branding.md) de marca se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Aunque los elementos gráficos son un medio visual sólido para indicar relaciones, su uso en exceso agrega desorden visual y reduce el espacio disponible en una superficie. Se deben usar con moderación.

Una tendencia de diseño en Microsoft Windows es una apariencia más sencilla y limpia mediante la eliminación de gráficos y líneas innecesarios.

Para decidir si un elemento gráfico es necesario, tenga en cuenta estas preguntas:

-   **¿La presentación y la comunicación del diseño son tan claras y eficaces sin el elemento?** Si es así, quítelo.
-   **¿Puede comunicar de forma eficaz las relaciones mediante el diseño por sí solo?** Si es así, use [el diseño en](vis-layout.md) su lugar. Puede colocar controles relacionados entre sí y colocar espaciado adicional entre controles no relacionados. También puede usar la sangría para mostrar relaciones jerárquicas.

![captura de pantalla de un diseño de cuatro iconos ](images/vis-graphic-image2.png)

En este ejemplo, solo el diseño se usa para mostrar las relaciones de control.

-   **¿Es eficaz la comunicación sin texto?** Si no es así, use un [cuadro de grupo](ctrl-group-boxes.md), separador etiquetado u otra [etiqueta](text-ui.md).

## <a name="usage-patterns"></a>Patrones de uso

Los elementos gráficos tienen varios patrones de uso:



| Elemento                                                                                                              |   Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ilustraciones gráficas**<br/> use para comunicar una idea visualmente. <br/>                         | Las ilustraciones gráficas son similares a los iconos, salvo que pueden tener cualquier tamaño y normalmente no son interactivas. <br/> ![gráfico del historial de uso de cpu de captura de pantalla ](images/vis-graphic-image3.png)<br/> En este ejemplo, se usa una ilustración gráfica para sugerir la naturaleza de una característica.<br/>                                                                                                                                                                                                        |
| **Fondos**<br/> use para resaltar o desacentr los distintos tipos de contenido. <br/>           | Los fondos se pueden usar para resaltar contenido importante. <br/> ![captura de pantalla de un mensaje de virus en el fondo rojo ](images/vis-graphic-image4.png)<br/> en este ejemplo, se usa un fondo para resaltar una tarea importante.<br/> los fondos también se pueden usar para desacentr el contenido secundario. <br/> ![captura de pantalla de los elementos del panel de control ](images/vis-graphic-image5.png)<br/> En este ejemplo, las tareas secundarias se desenmarcan si se encuentran en un panel de tareas.<br/>   |
| **Banners**<br/> se usa para indicar el estado importante. <br/>                                         | A diferencia de los fondos, los banners resaltan principalmente una sola cadena de texto. <br/> ![captura de pantalla del banner con información de configuración ](images/vis-graphic-image6.png)<br/> En este ejemplo, se usa un banner para indicar que la configuración de la página se controla mediante directiva de grupo.<br/>                                                                                                                                                                                                       |
| **Vidrio**<br/> use estratégicamente para reducir el peso visual de una ventana. <br/>                   | El cristal puede reducir el peso de una superficie si se centra en el contenido en lugar de en la propia ventana. <br/> ![captura de pantalla de un ave en la galería de fotos de Windows ](images/vis-graphic-image7.png)<br/> En este ejemplo, Glass centra la atención del usuario en el contenido en lugar de en los controles.<br/>                                                                                                                                                                                                 |
| **Agregadores**<br/> use para crear una relación visual entre controles fuertemente relacionados. <br/> | ![captura de pantalla de flechas de navegación hacia atrás y hacia delante ](images/vis-graphic-image8.png)<br/> En este ejemplo, se usa un fondo de agregador para resaltar la relación entre los botones atrás y hacia delante en el explorador.<br/> ![captura de pantalla de los controles de la galería de fotos de Windows ](images/vis-graphic-image7.png)<br/> En este ejemplo, se usa un agregador de límites para resaltar la relación entre los controles y hacer que se sientan como un control único en lugar de ocho.<br/> |
| **Separadores**<br/> use para separar controles débilmente relacionados o no relacionados. <br/>                   | Los separadores pueden ser interactivos o no interactivos. Los separadores interactivos entre el contenido que se puede cambiar de tamaño se conocen como separadores. <br/> ![captura de pantalla del separador divisor para el botón de nombre ](images/vis-graphic-image9.png)<br/> En este ejemplo, se usa un separador interactivo para el contenido que se puede tamaño.<br/> ![captura de pantalla del separador para la información del explorador ](images/vis-graphic-image10.png)<br/> En este ejemplo, el separador no es interactivo.<br/>                  |
| **Shadows**<br/> use para que el contenido destate visualmente en su fondo. <br/>             | ![captura de pantalla de cuatro fotos con sombras ](images/vis-graphic-image11.png)<br/> En este ejemplo, las sombras hacen que las ilustraciones desta decir sobre el fondo.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Asas**<br/> use para indicar que un objeto se puede mover o cambiar de tamaño. <br/>                    | Los identificadores siempre son interactivos y el puntero del mouse sugiere su comportamiento al mantener el puntero. <br/> ![captura de pantalla de una esquina de ventana con puntero de cambio de tamaño ](images/vis-graphic-image12.png)<br/> ![captura de pantalla del cuadro de selección con puntero de cambio de tamaño ](images/vis-graphic-image13.png)<br/> En estos ejemplos, los identificadores indican que se puede cambiar el tamaño de un objeto.<br/>                                                                                                                       |



 

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **No transmita información esencial solo a través de elementos gráficos.** Al hacerlo, se presentan problemas de accesibilidad para los usuarios con discapacidades visuales o discapacidades visuales.

### <a name="graphic-designs"></a>Diseños gráficos

-   **Los gráficos son más eficaces cuando refuerzan una sola idea sencilla.** Los gráficos complejos que requieren la reflexión para interpretar no funcionan bien. Los jeroglíacos son los mejores para los dibujos de la cueva.

    **Incorrecto:**

    ![captura de pantalla de advertencia mediante gráfico complejo ](images/vis-graphic-image14.png)

    En este ejemplo, un gráfico complejo de Windows XP intenta ineficazmente explicar una decisión de confianza compleja.

-   **No use flechas, botones de contenido adicional, marcos de botones u otras asequiciones asociadas a controles interactivos.** Al hacerlo, se invita a los usuarios a interactuar con los gráficos.
-   **Evite las franjas de rojo, amarillo y verde puros en los diseños.** Para evitar confusiones, reserve estos colores para comunicar el estado. Si debe usar estos colores para algo distinto del estado, use colores muted en lugar de colores puros.
-   **Usar diseños culturalmente neutros.** Lo que puede tener un significado determinado en un país, región o referencia cultural puede no tener el mismo significado en otro.
-   **Evite el uso de personas, caras, sexo o partes del cuerpo, así como símbolos de sentimiento, políticas y nacionales.** Es posible que estas imágenes no se traduzcan fácilmente o que puedan ser ofensivos.
-   **Cuando debe representar a personas o usuarios, representarlos genéricamente;** evite representaciones realistas.

### <a name="backgrounds-and-banners"></a>Fondos y banners

-   **Para resaltar el contenido, use texto oscuro sobre un fondo claro.** El texto negro en un fondo gris claro o amarillo funciona bien.

    ![captura de pantalla del texto del vínculo azul en el fondo amarillo ](images/vis-graphic-image15.png)

    En este ejemplo, el vínculo recibe la atención del usuario porque está en un fondo amarillo.

-   **Para desacenter el contenido, use texto claro en un fondo oscuro.** El texto blanco en un fondo gris oscuro o azul funciona bien.

    ![captura de pantalla del vínculo de ayuda blanco en el fondo verde ](images/vis-graphic-image16.png)

    En este ejemplo, el fondo oscuro desmarca el contenido.

-   **Si se usa un degradado, asegúrese de que el color del texto tiene un buen contraste en todo el degradado.**
-   **Use siempre un icono de 16 x 16 píxeles para llamar la atención sobre el banner.** De lo contrario, los banners son demasiado fáciles de pasar por alto. Para obtener más instrucciones y ejemplos, vea [Iconos estándar.](vis-std-icons.md)
-   **Use fondos y banners con precaución.** Aunque la intención del fondo o del banner puede ser resaltar el contenido, a menudo los resultados son el contrario a un fenómeno conocido como "cegura de banner".

### <a name="glass"></a>Vidrio

-   **Considere la posibilidad de usar el cristal estratégicamente en regiones pequeñas que toquen el marco de ventana sin texto.** Esto puede dar a un programa una apariencia más sencilla, más ligera y más cohesiva haciendo que la región parezca formar parte del marco.
-   **No use glass en situaciones en las que un fondo de ventana sin formato sea más atractivo o más fácil de usar.**

### <a name="separators"></a>Separadores

-   **Use líneas verticales y horizontales para los separadores.** Asegúrese de tener espacio suficiente entre los separadores y el contenido que se va a separar.
-   Para los separadores entre contenido que se puede ajustar (divisores), muestre el puntero de cambio de tamaño al mantener el puntero.

![Captura de pantalla que muestra un divisor con el puntero de cambio de tamaño.](images/vis-graphic-image17.png)

![captura de pantalla del divisor con puntero de cambio de tamaño ](images/vis-graphic-image18.png)

En estos ejemplos, los punteros de cambio de tamaño se muestran al mantener el puntero.

### <a name="shadows"></a>Shadows

-   **Use solo para que el contenido o los objetos más significativos del programa que se arrastran desta decir visualmente sobre su fondo.** Considere las sombras como desorden visual en otras circunstancias.

### <a name="high-dpi-support"></a>Compatibilidad con valores altos de ppp

-   **Admite modos de vídeo de 96 y 120 puntos por pulgada (ppp).** Detecte el modo de ppp en el inicio y controle los eventos de cambio de ppp. Windows está optimizado para 96 y 120 ppp y usa 96 ppp de forma predeterminada.
-   **Prefiere proporcionar mapas de bits independientes representados específicamente para 96 y 120 ppp en lugar de gráficos de escalado.** Proporcione al menos versiones de 96 y 120 ppp para los mapas de bits más importantes y visibles, y centrar o escalar los demás. Estas aplicaciones se consideran "con reconocimiento de valores altos de ppp" y proporcionan una mejor experiencia visual general que los programas que se escalan automáticamente mediante Windows.
    -   Desarrolladores: puede declarar un programa compatible con valores altos de ppp (e impedir el escalado automático) estableciendo la marca compatible con ppp en el manifiesto del programa o llamando a la API SetProcessDPIAware() durante la inicialización del programa. Puede usar macros para simplificar la selección de los gráficos correctos. En el caso de los mapas de bits de Win32, puede usar SS CENTERIMAGE para centrar o \_ \_ SS REALSIZECONTROL para escalar.
-   Compruebe el programa en 96 y 120 ppp para:
    -   Gráficos demasiado pequeños o demasiado grandes.
    -   Gráficos recortados, superpuestos o que no se ajusten correctamente.
    -   Gráficos mal extendidos ("con perfil").
    -   Texto recortado o no ajustado en fondos gráficos.

## <a name="text"></a>Texto

-   **Para la accesibilidad y localización, no use ningún texto en los gráficos.** Realice excepciones solo para representar [la personal de marca](exper-branding.md) y el texto como concepto abstracto.

 

