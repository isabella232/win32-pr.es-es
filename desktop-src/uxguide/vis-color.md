---
title: Color
description: El color es un elemento visual importante de la mayoría de las interfaces de usuario.
ms.assetid: 30a60e9e-ebb4-40f2-8535-a9b58dc668a8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ae58ddf232a3d8311a917ea0475c7aca1bae8949
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104156977"
---
# <a name="color"></a>Color

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

El color es un elemento visual importante de la mayoría de las interfaces de usuario. Más allá de la estética pura, el color tiene significados asociados y produce respuestas emocionales. Para evitar confusiones en significado, el color debe usarse de forma coherente. Para obtener las respuestas emocionales deseadas, se debe usar el color adecuadamente.

El color se suele considerar en términos de un espacio de colores, donde RGB (rojo, verde, azul), HSL (Hue, saturación, luminosidad) y HSV (matiz, saturación, valor) son los espacios de colores más utilizados.

![figura de un cubo que muestra las relaciones de color ](images/vis-color-image1.png)

El espacio de colores RGB se puede visualizar como un cubo.

Aunque la tecnología de pantalla usa valores RGB y, por lo tanto, los desarrolladores suelen pensar en los colores en términos de RGB, el espacio de colores RGB no se corresponde con el modo en que las personas perciben el color. Por ejemplo, si agrega rojo a cian oscuro, el resultado no se percibe como rojo, sino como aguamarina más claro.

![Ilustración de los cuadrados de cian oscuro y claro ](images/vis-color-image2.png)

En este ejemplo, la adición de rojo a cian oscuro hace que sea más claro, no más rojo. El espacio de colores RGB no se corresponde con el modo en que las personas perciben el color.

Los espacios de colores HSL/HSV se componen de tres componentes: matiz, saturación y luminosidad o valor. Estos espacios de colores suelen usarse en lugar de RGB porque mejoran la forma en que las personas perciben el color.

El espacio de colores HSL forma un cono doble que está en blanco en la parte superior, negro en la parte inferior y neutro en el centro:

-   **Matiz:** Color básico de la rueda de colores, que va de 0 a 360 grados, donde los grados 0 y 360 son rojos.

    ![figura de un círculo que muestra las relaciones de color ](images/vis-color-image3.png)

    La rueda de colores, donde el color rojo es 0 grados, el amarillo es de 60 grados, el verde es de 120 grados, el aguamarina es 180 grados, el azul es 240 grados y el magenta es de 300 grados.

-   **Saturación:** Cómo es puro (frente a mate) el color, que oscila entre 0 y 100, donde 100 está totalmente saturado y 0 es gris.
-   **Luminosidad:** La luz del color, que oscila entre 0 y 100, donde 100 es lo más claro posible (blanco, independientemente del matiz y la saturación) y 0 es lo más oscuro posible (negro).

    ![Ilustración que ilustra el espacio de colores HSL ](images/vis-color-image4.png)

    El espacio de colores HSL se puede visualizar como un cono doble.

El espacio de colores HSV es similar, salvo que su espacio forma un solo cono:

-   **Matiz:** Color básico de la rueda de colores, que va de 0 a 360 grados, donde los grados 0 y 360 son rojos.
-   **Saturación:** Cómo es puro (frente a mate) el color, que oscila entre 0 y 100, donde 100 está totalmente saturado y 0 es gris.
-   **Valor:** Brillo del color, que oscila entre 0 y 100, donde 100 es lo más brillante posible (que es la mitad de la luminosidad en el espacio HSL) y 0 es lo más oscuro posible (negro).

    ![Ilustración que ilustra el espacio de colores HSV ](images/vis-color-image5.png)

    El espacio de colores HSV se puede visualizar como un solo cono.

En los espacios HSL y HSV, si la saturación es 0, la luminosidad especifica un tono de gris. En Windows, los espacios HSL y HSV normalmente se reasignan a una escala de 0 a 240, de modo que los colores se pueden representar con un valor de 32 bits.

**Nota:** Las instrucciones relacionadas con las [fuentes](vis-fonts.md) y la [accesibilidad](inter-accessibility.md) se presentan en artículos independientes.

## <a name="design-concepts"></a>Conceptos de diseño

El uso efectivo del color puede hacer que la interfaz de usuario (UI) del programa sea más eficaz. El color puede ayudar a los usuarios a comprender ciertos significados de un vistazo. El color también puede hacer que el producto parezca más agradable y refinado.

Desafortunadamente, es muy fácil usar el color de manera ineficaz, especialmente si no está entrenado en el diseño visual. Un uso deficiente de los resultados en los diseños que parecen ser no profesionales, con fecha, confusos o simplemente horribles. Un uso deficiente del color puede ser peor que no usar el color en absoluto.

En esta sección se explica lo que necesita saber para usar el color de manera eficaz.

### <a name="how-color-is-used"></a>Cómo se usa el color

El color se usa normalmente en la interfaz de usuario para comunicarse:

-   **Al.** El significado de un mensaje se puede resumir a través del color. Por ejemplo, el color se usa a menudo para comunicar el estado en el que el rojo es un problema o un error, el amarillo es precaución o advertencia, y el verde es bueno.
-   **State.** El estado de un objeto se puede indicar a través del color. Por ejemplo, Windows usa color para indicar los Estados de selección y de desplazamiento. Los vínculos de las páginas web usan el azul para los que no se visitan y púrpura para visitarlos.
-   **Aun.** Las personas suponen que hay una relación entre los elementos del mismo color, por lo que la codificación en colores es una manera eficaz de diferenciar los objetos. Por ejemplo, en un elemento del panel de control, los paneles de tareas usan un fondo verde para separarlos visualmente del contenido principal. Además, Microsoft Outlook permite a los usuarios asignar diferentes marcas de color a los mensajes.
-   **Atención.** El color se puede usar para atraer la atención de los usuarios. Por ejemplo, Windows utiliza las [instrucciones principales](text-ui.md) azules para que destaquen del resto del texto.

Por supuesto, el color se usa a menudo en los gráficos por motivos estéticos. Aunque son importantes, debe elegir los colores de los elementos de la interfaz de usuario principalmente en función de lo que significan, no de su aspecto.

### <a name="color-interpretation"></a>Interpretación de color

**La interpretación de color de los usuarios suele depender de la cultura.** Por ejemplo, en el Estados Unidos, la boda attire para el novia está asociada en gran medida al color blanco, mientras que el negro está asociado a Funerals. Sin embargo, hace mucho tiempo en Japón, el símbolo de color era simplemente el opuesto: blanco era el color predominante en Funerals y el negro se consideraba un color que pone buena suerte para bodas.

Dicho esto, **la interpretación de rojo, amarillo y verde para el estado es coherente globalmente.** Esto se debe a la [Convención de la UNESCO de la UNESCO en señales y señales de carretera](https://www.unece.org/trans/conventn/signalse.pdf), que define la Convención Mundial de las luces de tráfico (donde el rojo significa que se ha detenido, verde y amarillo). Puede usar estos colores de estado sin preocuparse por las interpretaciones dependientes de la cultura.

Más allá de los colores de estado, Windows asigna significados a los colores según la Convención, tal como se muestra en la sección directrices de este artículo. Asegúrese de que el uso de colores del programa sea compatible con estas convenciones de color.

### <a name="color-accessibility"></a>Accesibilidad de color

El uso de color afecta a la accesibilidad del software al público más amplio posible. Es posible que los usuarios con ceguera o poca visión no puedan ver los colores bien, si se desea. Aproximadamente el 8 por ciento de los hombres adultos tienen algún tipo de confusión de color (a menudo se conoce como "persiana de color"), cuya confusión de color rojo-verde es la más común.

![figura que muestra los colores primarios tal como se muestra normalmente ](images/vis-color-image6.png)

Los colores primarios tal y como se muestran con la visión de color normal.

![figura que muestra los mismos colores que se ven con Protanopia ](images/vis-color-image7.png)

Los colores primarios tal como se muestran con Protanopia (1% del llenado macho).

![figura que muestra los mismos colores que se ven con deuteranopia ](images/vis-color-image8.png)

Los colores primarios tal como se muestran con deuteranopia (6% del llenado macho).

![figura que muestra los mismos colores que se ven con tritanopia ](images/vis-color-image9.png)

Los colores primarios tal como se muestran con Tritanopia (1% del llenado macho).

Para obtener más información, consulte [¿puede Color-Blind usuarios ver su sitio?](/previous-versions/windows/internet-explorer/ie-developer/)

### <a name="use-color-to-reinforce-visually"></a>Usar el color para reforzar visualmente

La mejor solución para la interpretación de color y los problemas de accesibilidad es usar el color para reforzar visualmente el significado de uno de estos métodos de comunicación principales:

-   **Text.** El texto conciso suele ser la comunicación principal más eficaz directamente en la interfaz de usuario o a través de una información sobre herramientas.

![captura de pantalla de un pequeño icono rojo con información sobre herramientas ](images/vis-color-image10.png)

En este ejemplo, el texto de información sobre herramientas se usa para comunicar el significado de un icono.

-   **Concepción.** Los iconos distinguen fácilmente los diseños, especialmente su forma de contorno.

![captura de pantalla de iconos en tonalidades de gris (escala de grises) ](images/vis-color-image11.png)

En este ejemplo, los iconos estándar se pueden distinguir fácilmente en función de sus diseños.

-   **Cód.** También se puede utilizar la ubicación relativa, pero este enfoque es más débil que las alternativas. Para ser efectivo, la ubicación debe ser estándar y bien conocida, como con las luces de tráfico.

Aunque el color es el atributo más obvio de muchos diseños, siempre debe ser redundante.

### <a name="designing-with-color"></a>Diseñar con color

Paradójicamente, la mejor manera de diseñar para el color es empezar diseñando sin color, utilizando [tramas de alambre](glossary.md) o monocromáticas, y, a continuación, agregue el color más adelante. De este modo, se garantiza que la información no se comunica con solo color. También ayuda a garantizar que la copia impresa tenga un aspecto excelente en las impresoras monocromáticas.

### <a name="use-theme-or-system-colors"></a>Usar colores del tema o del sistema

Aunque hay muchos factores complejos al usar el color de forma eficaz, en la interfaz de usuario de Windows la elección del color a menudo se reduce a la simple elección del color del [tema](glossary.md) o [del sistema](glossary.md) apropiado según unas pocas reglas simples. Los usuarios pueden seleccionar y personalizar estas combinaciones de colores como deseen.

Al hacerlo, no solo se acomodan las preferencias de color de todos los usuarios, sino que se elimina la carga que supone elegir la combinación de colores perfecta que funciona para todos los gustos, estilos y referencias culturales (que, por supuesto, no es posible).

**Si solo hace algo...**

Elija colores seleccionando el color de tema o el color del sistema adecuados. Nunca use el color como método principal de comunicación, sino como método secundario para reforzar visualmente el significado. Diseño mediante tramas de alambre o monocromo para garantizar que el color es secundario.

### <a name="use-theme-or-system-colors-correctly"></a>Usar colores del tema o del sistema correctamente

Supongamos que los usuarios eligen los colores del tema o del sistema en función de sus necesidades personales y de que los colores del sistema o del tema se construyen adecuadamente. En función de esta suposición, si siempre elige colores del tema o del sistema en función de su finalidad prevista y emparejar en primer plano con los suyos asociados, se garantiza que los colores son legibles y respetan los deseos de los usuarios en todos los modos de vídeo, incluido [el modo de alto contraste](glossary.md). Por ejemplo, se garantiza que el color del sistema de texto de la ventana es legible en el color del sistema de fondo de la ventana.

En concreto, siempre:

-   **Elija los colores en función de su propósito.** No elija colores en función de su apariencia actual porque el usuario o versiones futuras de Windows pueden cambiar esa apariencia.
-   **Coincide con los colores de primer plano con sus colores de fondo asociados.** Se garantiza que los colores de primer plano son legibles únicamente contra sus colores de fondo asociados. No mezcle ni haga coincidir los colores de primer plano con otros colores de fondo, o peor aún, otros colores de primer plano.
-   **No mezcle tipos de colores.** Es decir, siempre coinciden los colores del tema con los colores del tema asociados, los colores del sistema con los colores del sistema asociados y los colores cableados con otros colores de cableado. Por ejemplo, no se garantiza que un color de texto del tema sea legible contra un fondo cableado.
-   **Si debe trabajar con los colores, trate el modo de alto contraste como caso especial.**

**Si solo hace algo...**

Elija siempre colores del tema o del sistema en función de su finalidad prevista y empareje los demás en primer plano con los suyos asociados.

### <a name="using-other-colors"></a>Usar otros colores

Aunque el tema de Windows define un conjunto completo de partes del tema, puede encontrar que el programa necesita colores que no están definidos en el archivo de tema. Aunque podría cableado de estos colores, un enfoque mejor es derivar los colores del tema o de los colores del sistema. El uso estratégico de este enfoque proporciona todas las ventajas del uso de los colores del tema y del sistema, pero con mucha más flexibilidad.

Por ejemplo, supongamos que necesita un fondo de ventana que sea más oscuro que el color de fondo de la ventana de tema. En el espacio de colores HSL, tener un color más oscuro significa un color con una luminosidad inferior. Por lo tanto, puede derivar un color de fondo de la ventana más oscuro mediante los pasos siguientes:

-   Obtiene el color RGB del tema de fondo de la ventana.
-   Convierta el RGB en su valor HSL.
-   Reduzca el valor de luminosidad (por ejemplo, 20 por ciento).
-   Vuelva a convertir los valores RGB.

Con este enfoque, se garantiza que el color derivado se percibe como un tono más oscuro del color original (a menos que el color original fuera muy oscuro para comenzar).

![Ilustración que muestra los efectos de la luminosidad reducida ](images/vis-color-image12.png)

En este ejemplo, el color de fondo de una ventana más oscura se deriva del color del tema.

### <a name="testing-colors"></a>Probar colores

Para determinar si el uso del programa de color es accesible y no se usa como método principal de comunicación, se recomienda usar las utilidades [Fujitsu ColorDoctor](https://www.fujitsu.com/global/about/businesspolicy/tech/design/) o [Vischeck](https://www.vischeck.com/) para comprobar lo siguiente:

-   Dependencia global en el color con el filtro de escala de grises.
-   Problemas de confusión de color específicos mediante los filtros Protanopia, deuteranopia y tritanopia.

Para determinar si el uso del programa de color está programado correctamente, pruebe el programa en los modos siguientes:

-   Se habilitan con el tema predeterminado de Windows.
-   Se habilitan con temas que no son predeterminados.
-   Se deshabilitan ("estilo clásico de Windows" en la configuración del tema en el elemento del panel de control de personalización).
-   Contraste alto negro (texto blanco sobre un fondo negro).
-   Contraste alto blanco (texto en negro sobre un fondo blanco).

Todos los elementos de la pantalla deben ser legibles y aparecer según lo esperado, incluso después de los cambios en el modo.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Nunca use el color como método principal de comunicación,** sino como método secundario para reforzar visualmente el significado.

### <a name="using-theme-and-system-colors"></a>Usar colores del tema y del sistema

-   Siempre que sea posible, **Elija colores seleccionando el color del tema o el color del sistema adecuados.** Al hacerlo, siempre puede respetar las preferencias de color de los usuarios.
-   **Elija los colores del tema y del sistema en función de su finalidad.** No elija colores en función de su apariencia actual, ya que el usuario o versiones futuras de Windows pueden cambiar esa apariencia.
-   **Coincide con los colores de primer plano con sus colores de fondo asociados.** Se garantiza que los colores de primer plano son legibles únicamente contra sus colores de fondo asociados. No mezcle ni haga coincidir los colores de primer plano con otros colores de fondo, o peor aún, otros colores de primer plano.
-   **No mezcle tipos de colores.** Es decir, siempre coinciden los colores del tema con los colores del tema asociados, los colores del sistema con los colores del sistema asociados y los colores cableados con otros colores de cableado. Por ejemplo, no se garantiza que un color de texto del tema sea legible contra un fondo cableado.
-   **Si debe usar un color que no sea un tema o un color del sistema:**
    -   **Prefiere derivar el color de un tema o de un color del sistema a través de su valor.** Use el proceso descrito anteriormente en este artículo, en uso de otros colores.
    -   **Administrar el modo de alto contraste como caso especial.**
-   **Controle los cambios de tema.** Windows administra automáticamente los cambios de tema con los marcos de ventana estándar y los controles comunes. Las ventanas con marcos de ventana personalizados, controles personalizados o dibujados por el propietario, y otro uso de color deben controlar explícitamente los cambios de tema.
    -   **Desarrolladores:** Puede responder a los eventos de cambio de tema controlando el mensaje de THEMECHANGED de WM \_ .

### <a name="color-meaning"></a>Significado del color

-   Aunque debe usar los colores del tema y del sistema (o los colores derivados) siempre que pueda, asegúrese de que cualquier otro uso de color sea compatible con el siguiente uso de color dentro de Windows.



|                                      |                                                                               |                                                                                                                                                                 |
|--------------------------------------|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hue**<br/>                   | **Significado**<br/>                                                        | **Usar en Windows**<br/>                                                                                                                                   |
| azul/verde<br/>                | Marca de Windows<br/>                                                      | Background: personalización de marca de Windows.<br/>                                                                                                                        |
| vidrio, negro, gris, blanco<br/> | neutral<br/>                                                            | Fondo: marcos de ventana estándar, menú Inicio, barra de tareas, barra lateral.<br/> Foreground: texto normal.<br/>                                                |
| blue<br/>                      | Inicio, confirmar<br/>                                                      | Background: botones de comando predeterminados, buscar, iniciar sesión.<br/> Iconos: información, ayuda.<br/> Primer plano: instrucciones principales, vínculos.<br/>           |
| rojo<br/>                       | error, detención, vulnerable, crítico, atención inmediata, restringido<br/> | Background: Estado, progreso detenido (barras de progreso).<br/> Iconos: error, detener, cerrar ventana, eliminar, entrada necesaria, falta, no disponible.<br/>     |
| yellow<br/>                    | ADVERTENCIA, precaución, cuestionable<br/>                                     | Background: Estado, progreso en pausa (barras de progreso).<br/> Iconos: ADVERTENCIA<br/>                                                                       |
| green<br/>                     | Go, Proceed, Progress, Safe<br/>                                        | Background: Estado, progreso normal (barras de progreso).<br/> Iconos: ir, listo, actualizar.<br/> Foreground: rutas de acceso y direcciones URL (en los resultados de la búsqueda).<br/> |
| purple<br/>                    | visitado<br/>                                                            | Primer plano: vínculos visitados (para vínculos en Windows Internet Explorer y documentos).<br/>                                                                |



 

-   **Para evitar la comunicación de los significados anteriores, elija los colores tienen alta saturación de media a baja y alta o baja luminosidad.** Los usuarios asocian los significados anteriores a los colores que tienen una luminosidad completa o alta y una luminosidad de nivel medio, por lo que puede evitar estas asociaciones eligiendo diferentes sombras.

![Ilustración que muestra cómo afecta la luminosidad al color ](images/vis-color-image13.png)

En este ejemplo, hay tres sombras diferentes de amarillo, pero solo el sombreado de luminosidad de nivel medio muy saturado comunica la advertencia. El icono de la carpeta amarilla no se parece a una advertencia.

### <a name="using-color-with-data"></a>Usar el color con datos

-   Cuando sea útil, **asigne color a los datos para ayudar a los usuarios a diferenciarlos.** Tenga en cuenta que los usuarios asumirán que los datos con colores similares tienen significados similares.
-   **Asigne colores de forma predeterminada que resulten fáciles de distinguir.** Por lo general, los colores son fáciles de distinguir si están alejados entre sí en los espacios de colores HSL/HSV, a la vez que se mantiene un contraste alto con su fondo:
    -   Al elegir colores, prefiere las armonías de tríada o los matices complementarios, pero no los tonos adyacentes.

        ![Ilustración que muestra cómo elegir los colores de contraste ](images/vis-color-image14.png)

        En este ejemplo, si la primera asignación de color es rojo, el color siguiente debe ser azul, verde o aguamarina, pero no magenta, púrpura, naranja o amarillo.

    -   Los colores tienen un contraste alto si hay una gran diferencia en el matiz, la saturación o la luminosidad.

        ![Ilustración en la que se muestra un color en otros terrenos ](images/vis-color-image15.png)

        En este ejemplo, el color base azul claro contrasta con el fondo con grandes diferencias de matiz, saturación o luminosidad.

    -   El uso de un fondo blanco o muy claro facilita la diferenciación de los colores de primer plano.

        ![Ilustración que ilustra el contraste bueno y deficiente ](images/vis-color-image16.png)

        En este ejemplo, los colores de fondo blanco y claro facilitan la distinción del color de primer plano.

-   **Permitir a los usuarios personalizar estas asignaciones de color** , ya que la elección de color es subjetiva y una preferencia personal. Si hay muchos colores coordinados, permita a los usuarios cambiarlos como un grupo mediante combinaciones de colores.
-   **Permitir a los usuarios etiquetar estas asignaciones de color.** De este modo, podrá facilitar su identificación y búsqueda.
-   **A diferencia de los colores de la interfaz de usuario, los datos no deben cambiar cuando cambian los colores del sistema.**

## <a name="documentation"></a>Documentación

-   **Haga referencia a los elementos de la interfaz de usuario por sus nombres, no por sus colores.** Dichas referencias no son accesibles y los colores del sistema pueden cambiar. Si el nombre de un elemento de la interfaz de usuario no es bien conocido o no es lo suficientemente descriptivo, muestre una captura de pantalla para aclararlo.

**Correcto:**

![captura de pantalla del mensaje que contiene la barra de información ](images/vis-color-image17.png)

**Incorrecto:**

![captura de pantalla del mensaje que contiene la "barra dorada" ](images/vis-color-image18.png)

En el ejemplo incorrecto, el mensaje hace referencia a la barra de información de Windows Internet Explorer por su color en lugar de su nombre.

