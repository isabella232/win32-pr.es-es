---
title: Color
description: El color es un elemento visual importante de la mayoría de las interfaces de usuario.
ms.assetid: 30a60e9e-ebb4-40f2-8535-a9b58dc668a8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 9ade1c87606aa14831220e501a5f39f5d2ce2d1ebb4016ad04822634b7735c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936819"
---
# <a name="color"></a>Color

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

El color es un elemento visual importante de la mayoría de las interfaces de usuario. Más allá de la física pura, el color tiene significados asociados y provoca respuestas emocionales. Para evitar confusiones en el significado, el color debe usarse de forma coherente. Para obtener las respuestas emocionales deseadas, el color debe usarse correctamente.

El color se suele pensar en términos de un espacio de colores, donde RGB (rojo, verde, azul), HSL (matiz, saturación, luminosidad) y HSV (matiz, saturación, valor) son los espacios de color más usados.

![figura de un cubo que muestra las relaciones de color ](images/vis-color-image1.png)

El espacio de colores RGB se puede visualizar como un cubo.

Aunque la tecnología de visualización usa valores RGB y, por tanto, los desarrolladores suelen pensar en colores en términos de RGB, el espacio de colores RGB no se corresponde con la forma en que las personas perciben el color. Por ejemplo, si agrega rojo a oscuro, el resultado no se percibe como más rojo, sino como más ligero.

![ilustración de cuadrados cian oscuros y claros ](images/vis-color-image2.png)

En este ejemplo, agregar rojo a oscuro hace que sea más claro, no más rojo. El espacio de color RGB no se corresponde con la forma en que las personas perciben el color.

Los espacios de color HSL/HSV constan de tres componentes: matiz, saturación y luminosidad o valor. Estos espacios de color se usan a menudo en lugar de RGB porque coinciden mejor con la forma en que las personas perciben el color.

El espacio de color HSL forma un cono doble que es blanco en la parte superior, negro en la parte inferior y neutro en el medio:

-   **Hue:** Color básico en la rueda de colores, que va de 0 a 360 grados, donde 0 y 360 grados son rojos.

    ![figura de un círculo que muestra las relaciones de color ](images/vis-color-image3.png)

    La rueda de color, donde el rojo es 0 grados, el amarillo es 60 grados, el verde es de 120 grados, el de 180 grados, el azul es de 240 grados y el decoloro es de 300 grados.

-   **Saturación:** Qué puro es el color (frente a la desardenada), que va de 0 a 100, donde 100 está totalmente saturado y 0 es gris.
-   **Luminosidad:** La luz del color, que va de 0 a 100, donde 100 es lo más claro posible (blanco, independientemente del matiz y saturación) y 0 es lo más oscuro posible (negro).

    ![ilustración que ilustra el espacio de colores hsl ](images/vis-color-image4.png)

    El espacio de color HSL se puede visualizar como un cono doble.

El espacio de color HSV es similar, salvo que su espacio forma un solo cono:

-   **Hue:** Color básico en la rueda de colores, que va de 0 a 360 grados, donde 0 y 360 grados son rojos.
-   **Saturación:** Qué puro es el color (frente a la desardenada), que va de 0 a 100, donde 100 está totalmente saturado y 0 es gris.
-   **Valor:** Qué brillante es el color, que va de 0 a 100, donde 100 es lo más brillante posible (que es la mitad de luminosidad en el espacio HSL) y 0 es lo más oscuro posible (negro).

    ![ilustración que ilustra el espacio de colores hsv ](images/vis-color-image5.png)

    El espacio de color HSV se puede visualizar como un solo cono.

En los espacios HSL y HSV, si la saturación es 0, la luminosidad especifica un tono gris. En Windows, los espacios HSL y HSV se suelen volver a asociar a una escala entre 0 y 240 para que los colores se puedan representar con un valor de 32 bits.

**Nota:** Las directrices relacionadas [con las](vis-fonts.md) fuentes [y la accesibilidad](inter-accessibility.md) se presentan en artículos independientes.

## <a name="design-concepts"></a>Conceptos de diseño

El uso eficaz del color puede hacer que la interfaz de usuario (UI) del programa sea más eficaz. El color puede ayudar a los usuarios a comprender ciertos significados de un vistazo. El color también puede hacer que el producto parezca más atractivo y refinado desde el punto de vista visual.

Desafortunadamente, es muy fácil usar el color de forma ineficaz, especialmente si no está entrenado en el diseño visual. Un uso deficiente del color da como resultado diseños que parecen poco profesionales, con fecha, confusos o simplemente insocuos. Un uso deficiente del color puede ser peor que no usar color en absoluto.

En esta sección se explica lo que necesita saber para usar el color de forma eficaz.

### <a name="how-color-is-used"></a>Cómo se usa el color

El color se usa normalmente en la interfaz de usuario para comunicarse:

-   **Significado.** El significado de un mensaje se puede resumir a través del color. Por ejemplo, el color se usa a menudo para comunicar el estado en el que el rojo es un problema o un error, el amarillo es precaución o advertencia, y el verde es bueno.
-   **Estado.** El estado de un objeto se puede indicar a través del color. Por ejemplo, Windows color para indicar los estados de selección y de desplazamiento. Los vínculos de las páginas web usan el azul para los elementos novistidos y púrpura para los que se visitan.
-   **Diferenciación.** Los usuarios suponen que hay una relación entre los elementos del mismo color, por lo que la codificación de colores es una manera eficaz de diferenciar entre objetos. Por ejemplo, en un elemento del panel de control, los paneles de tareas usan un fondo verde para separarlos visualmente del contenido principal. Además, Microsoft Outlook permite a los usuarios asignar diferentes marcas de color a los mensajes.
-   **Énfasis.** El color se puede usar para llamar la atención de los usuarios. Por ejemplo, Windows instrucciones principales [azules](text-ui.md) para ayudarles a destacarse del otro texto.

Por supuesto, el color se usa a menudo en gráficos por motivos puramente éticos. Aunque la decoración es importante, debe elegir los colores de los elementos de la interfaz de usuario principalmente en función de lo que significan, no de su aspecto.

### <a name="color-interpretation"></a>Interpretación del color

**La interpretación del color de los usuarios suele depender culturalmente.** Por ejemplo, en la Estados Unidos, la ropa de la campana está asociada en gran medida al color blanco, mientras que el negro está asociado a las paletas. Sin embargo, hace mucho tiempo, en Japón, el simbolismo de color era justo lo contrario: el blanco era el color predominante en los azules y el negro se consideraba un color que aportaba buena suerte para los toros.

Dicho esto, **la interpretación de rojo, amarillo y verde para el estado es coherente globalmente.** Esto se debe a la Convención de tránsito de LA HAYA sobre señales y señales de carretera, que define la convención mundial para los semáforos (donde rojo significa detenerse, verde significa continuar y los medios [amarillos](https://www.unece.org/trans/conventn/signalse.pdf)proceden con precaución). Puede usar estos colores de estado sin preocuparse por las interpretaciones dependientes de la cultura.

Más allá de los colores de estado, Windows asigna significados a los colores en función de la convención, como se muestra en la sección Directrices de este artículo. Asegúrese de que el uso de color del programa es compatible con estas convenciones de color.

### <a name="color-accessibility"></a>Accesibilidad de color

El uso del color afecta a la accesibilidad del software a la audiencia más amplia posible. Es posible que los usuarios con cevidencia o visión baja no puedan ver bien los colores, en caso de que sea necesario. Aproximadamente el 8 por ciento de los hombres adultos tienen algún tipo de confusión de color (a menudo se conoce incorrectamente como "davidez de color"), de la que la confusión de color rojo-verde es la más común.

![ilustración que muestra los colores primarios como se ve normalmente ](images/vis-color-image6.png)

Los colores principales, como se ve con la visión de color normal.

![ilustración que muestra los mismos colores que se ven con la profetía ](images/vis-color-image7.png)

Los colores primarios, como se ve con Propia (1 % de la población de hombres).

![ilustración que muestra los mismos colores vistos con deuteranopia ](images/vis-color-image8.png)

Los colores principales, como se ve con Deuteranopia (6 % de la población de hombres).

![ilustración que muestra los mismos colores que se ven con tripia ](images/vis-color-image9.png)

Los colores primarios, como se ve con Tripia (1 % de la población de hombres).

Para obtener más información, consulte [¿Color-Blind usuarios pueden ver su sitio?](/previous-versions/windows/internet-explorer/ie-developer/)

### <a name="use-color-to-reinforce-visually"></a>Uso del color para reforzar visualmente

La mejor solución a los problemas de accesibilidad y interpretación del color es usar el color para reforzar visualmente el significado de uno de estos métodos principales de comunicación:

-   **Text.** El texto conciso suele ser la comunicación principal más eficaz directamente en la interfaz de usuario o a través de una información sobre herramientas.

![captura de pantalla de pequeño icono rojo con información sobre herramientas ](images/vis-color-image10.png)

En este ejemplo, el texto de la información sobre herramientas se usa para comunicar el significado de un icono.

-   **Diseño.** Los iconos se distinguen fácilmente por los diseños, especialmente su forma de contorno.

![captura de pantalla de iconos en tonalidades de gris (escala de grises) ](images/vis-color-image11.png)

En este ejemplo, los iconos estándar se distinguen fácilmente en función de sus diseños.

-   **Ubicación.** También se puede usar la ubicación relativa, pero este enfoque es más débil que las alternativas. Para que sea eficaz, la ubicación debe ser estándar y conocida, al igual que con los semáforos.

Aunque el color es el atributo más obvio de muchos diseños, siempre debe ser redundante.

### <a name="designing-with-color"></a>Diseño con color

Irónicamente, la mejor manera de diseñar para el color es empezar por diseñar sin color, mediante [tramas](glossary.md) de conexión o monocromáticas y, a continuación, agregar color más adelante. Esto ayuda a garantizar que la información no se comunica solo con el color. También ayuda a garantizar que las copias impresas tienen un aspecto excelente en impresoras monocromáticas.

### <a name="use-theme-or-system-colors"></a>Uso de colores del tema o del sistema

Aunque hay muchos factores complejos en el uso eficaz del color, en la interfaz de usuario de Windows la elección del color suele reducirse para simplemente elegir el [color](glossary.md) del tema o el [color](glossary.md) del sistema adecuados según algunas reglas sencillas. A continuación, los usuarios pueden seleccionar y personalizar estas esquemas de color a medida que lo eligen.

Al hacerlo, no solo se adapta a las preferencias de color de todos los usuarios, sino que se elimina la carga de elegir la combinación de colores perfecta que funciona para todos los idiomas, estilos y culturas (lo que, por supuesto, es imposible).

**Si solo hace una cosa...**

Elija los colores seleccionando el color del tema o el color del sistema adecuados. Nunca use el color como método principal de comunicación, sino como método secundario para reforzar el significado visualmente. Diseñe mediante wireframes o monocromáticas para ayudar a garantizar que el color es secundario.

### <a name="use-theme-or-system-colors-correctly"></a>Usar los colores del tema o del sistema correctamente

Supongamos que los usuarios eligen los colores del tema o del sistema en función de sus necesidades personales y que los colores del tema o del sistema se construyen correctamente. En función de esta suposición, si siempre elige los colores del tema o del sistema en función de su propósito previsto y empareja los primeros planos con sus fondos asociados, se garantiza que los colores son legibles y respetan los deseo de los usuarios en todos los modos de vídeo, incluido el modo de contraste [alto.](glossary.md) Por ejemplo, se garantiza que el color del sistema de texto de la ventana es legible en el color del sistema de fondo de la ventana.

En concreto, siempre:

-   **Elija colores en función de su propósito.** No elija colores en función de su apariencia actual, ya que el usuario o las versiones futuras de la Windows.
-   **Coincide con los colores de primer plano con los colores de fondo asociados.** Se garantiza que los colores de primer plano son legibles solo con respecto a los colores de fondo asociados. No mezcle ni haga coincidir los colores de primer plano con otros colores de fondo, o peor aún, otros colores de primer plano.
-   **No mezcle tipos de color.** Es decir, haga coincidir siempre los colores del tema con sus colores de tema asociados, los colores del sistema con los colores del sistema asociados y los colores de los cables duros con otros colores de cableado. Por ejemplo, no se garantiza que un color de texto del tema sea legible en un fondo cableado.
-   **Si debe usar colores de cable duro, controle el modo de contraste alto como un caso especial.**

**Si solo hace una cosa...**

Elija siempre los colores del tema o del sistema en función de su propósito previsto y emparere los primeros planos con sus fondos asociados.

### <a name="using-other-colors"></a>Uso de otros colores

Aunque el Windows define un conjunto completo de elementos de tema, es posible que el programa necesite colores que no están definidos en el archivo de tema. Aunque podría dar forma a estos colores, un mejor enfoque es derivar colores del tema o los colores del sistema. El uso estratégico de este enfoque ofrece todas las ventajas de usar colores del tema y del sistema, pero con mucha más flexibilidad.

Por ejemplo, supongamos que necesita un fondo de ventana más oscuro que el color de fondo de la ventana de tema. En el espacio de colores HSL, tener un color más oscuro significa un color con una luminosidad inferior. Por lo tanto, puede derivar un color de fondo de ventana más oscuro mediante los pasos siguientes:

-   Obtenga el color rgb del tema de fondo de la ventana.
-   Convierta RGB en su valor HSL.
-   Reduzca el valor de luminosidad (por decir, un 20 %).
-   Vuelva a convertir a valores RGB.

Con este enfoque, se garantiza que el color derivado se percibe como un tono más oscuro del color original (a menos que el color original fuera muy oscuro para empezar).

![ilustración que muestra los efectos de la luminosidad reducida ](images/vis-color-image12.png)

En este ejemplo, un color de fondo de ventana más oscuro se deriva del color de tema.

### <a name="testing-colors"></a>Prueba de colores

Para determinar si el uso del color del programa es accesible y no se usa como método principal de comunicación, se recomienda usar las utilidades [ColorDoctor](https://www.fujitsu.com/global/about/businesspolicy/tech/design/) o [Vischeck](https://www.vischeck.com/) para comprobar:

-   Dependencia general del color mediante el filtro escala gris.
-   Problemas específicos de confusión de color mediante los filtros Propia, Deuteranopia y Tripia.

Para determinar si el uso de color del programa está programado correctamente, pruebe el programa de los modos siguientes:

-   Temas habilitados mediante el tema Windows predeterminado.
-   Temas habilitados mediante un tema no predeterminado.
-   Temas deshabilitados ("Windows clásico" en la sección Tema Configuración el elemento Personalization Panel de control).
-   contraste alto negro (texto blanco sobre un fondo negro).
-   contraste alto blanco (texto negro sobre un fondo blanco).

Todos los elementos de la pantalla deben ser legibles y aparecer según lo previsto, incluso inmediatamente después de que cambie el modo.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Nunca use el color como método principal de comunicación, sino** como método secundario para reforzar el significado visualmente.

### <a name="using-theme-and-system-colors"></a>Uso de colores del tema y del sistema

-   Siempre que sea **posible, elija los colores seleccionando el color del tema o el color del sistema adecuados.** Al hacerlo, siempre puede respetar las preferencias de color de los usuarios.
-   **Elija los colores del tema y del sistema en función de su propósito.** No elija colores en función de su apariencia actual, ya que el usuario o las versiones futuras de la Windows.
-   **Coincide con los colores de primer plano con los colores de fondo asociados.** Se garantiza que los colores de primer plano son legibles solo con respecto a los colores de fondo asociados. No mezcle ni haga coincidir los colores de primer plano con otros colores de fondo, o peor aún, otros colores de primer plano.
-   **No mezcle tipos de color.** Es decir, haga coincidir siempre los colores del tema con sus colores de tema asociados, los colores del sistema con los colores del sistema asociados y los colores de los cables duros con otros colores de cableado. Por ejemplo, no se garantiza que un color de texto del tema sea legible en un fondo cableado.
-   **Si debe usar un color que no sea un tema o un color del sistema:**
    -   **Prefiere derivar el color de un tema o color del sistema en lugar de cambiar su valor.** Use el proceso descrito anteriormente en este artículo, en Uso de otros colores.
    -   **Controle el modo de contraste alto como un caso especial.**
-   **Controle los cambios de tema.** Los cambios de tema se controlan automáticamente mediante ventanas con marcos de ventana estándar y controles comunes. Windows con marcos de ventana personalizados, controles personalizados o de dibujo del propietario, y otro uso de color debe controlar los cambios de tema explícitamente.
    -   **Desarrolladores:** Puede responder a eventos de cambio de tema controlando el mensaje WM \_ THEMECHANGED.

### <a name="color-meaning"></a>Significado del color

-   Aunque debe usar colores del tema y del sistema (o colores derivados) siempre que pueda, asegúrese de que cualquier otro uso de color sea compatible con el siguiente uso de color dentro de Windows.



| Matiz | Significado | Uso en Windows  |
|--------------------------------------|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| azul/verde<br/>                | Windows marca<br/>                                                      | Fondo: Windows personal de marca.<br/>                                                                                                                        |
| glass, black, gray, white<br/> | neutral<br/>                                                            | Fondo: marcos de ventana estándar, menú Inicio, barra de tareas, barra lateral.<br/> Primer plano: texto normal.<br/>                                                |
| blue<br/>                      | start, commit<br/>                                                      | Fondo: botones de comando predeterminados, búsqueda e inicio de sesión.<br/> Iconos: información, Ayuda.<br/> Primer plano: instrucciones principales, vínculos.<br/>           |
| rojo<br/>                       | error, stop, vulnerable, critical, immediate attention, restricted<br/> | Fondo: estado, progreso detenido (barras de progreso).<br/> Iconos: error, detenerse, cerrar ventana, eliminar, entrada necesaria, falta, no disponible.<br/>     |
| yellow<br/>                    | advertencia, precaución, preguntable<br/>                                     | Fondo: estado, progreso en pausa (barras de progreso).<br/> Iconos: advertencia<br/>                                                                       |
| green<br/>                     | go, proceed, progress, safe<br/>                                        | Fondo: estado, progreso normal (barras de progreso).<br/> Iconos: go, done, refresh.<br/> Primer plano: rutas de acceso y direcciones URL (en los resultados de la búsqueda).<br/> |
| purple<br/>                    | Visitado<br/>                                                            | Primer plano: vínculos visitados (para vínculos dentro Windows Internet Explorer y documentos).<br/>                                                                |



 

-   **Para evitar comunicar los significados anteriores, elija los colores que tengan una saturación de media a baja alta y una luminosidad alta o baja.** Los usuarios asocian los significados anteriores a los colores que tienen saturación completa o alta y luminosidad de nivel medio, por lo que puede evitar estas asociaciones eligiendo diferentes tonos.

![ilustración que muestra cómo afecta la luminosidad al color ](images/vis-color-image13.png)

En este ejemplo, hay tres tonalidades diferentes de amarillo, pero solo el tono de luminosidad de nivel medio altamente saturado comunica la advertencia. El icono de carpeta amarilla no parece una advertencia.

### <a name="using-color-with-data"></a>Uso del color con datos

-   Cuando sea útil, **asigne color a los datos para ayudar a los usuarios a diferenciarlos.** Tenga en cuenta que los usuarios asumirán que los datos con colores similares tienen significados similares.
-   **Asigne colores de forma predeterminada que sean fáciles de distinguir.** Por lo general, los colores son fáciles de distinguir si están separados entre sí en los espacios de colores HSL/HSV, al tiempo que mantienen un contraste alto con su fondo:
    -   Al elegir colores, se prefieren las tonalidades de tríada o los matiz complementarios, pero no los matiz adyacentes.

        ![ilustración que muestra cómo elegir colores de contraste ](images/vis-color-image14.png)

        En este ejemplo, si la primera asignación de color es de color rojo, el color siguiente debe ser azul, verde o cian, pero no el rojo, el púrpura, el naranja o el amarillo.

    -   Los colores tienen un contraste alto si hay una gran diferencia en su matiz, saturación o luminosidad.

        ![ilustración que muestra un color en fondos diferentes ](images/vis-color-image15.png)

        En este ejemplo, el color base azul claro contrasta con los fondos con grandes diferencias en el matiz, la saturación o la luminosidad.

    -   El uso de un fondo blanco o muy claro facilita la distinción de los colores de primer plano en contraste.

        ![ilustración que ilustra el contraste bueno y deficiente ](images/vis-color-image16.png)

        En este ejemplo, los colores de fondo blanco y claro facilitan la distinción del color de primer plano.

-   **Permitir a los usuarios personalizar estas asignaciones de** colores porque la elección de color es subjetiva y una preferencia personal. Si hay muchos colores coordinados, permita a los usuarios cambiarlos como un grupo mediante esquemas de color.
-   **Permitir a los usuarios etiquetar estas asignaciones de colores.** Esto ayuda a que sean más fáciles de identificar y buscar.
-   **A diferencia de los colores de la interfaz de usuario, los datos no deben cambiar cuando cambian los colores del sistema.**

## <a name="documentation"></a>Documentación

-   **Consulte los elementos de la interfaz de usuario por sus nombres, no por sus colores.** Estas referencias no son accesibles y los colores del sistema pueden cambiar. Si el nombre de un elemento de interfaz de usuario no es lo suficientemente conocido o no es lo suficientemente descriptivo, muestre una captura de pantalla para aclararlo.

**Correcto:**

![captura de pantalla del mensaje que contiene la barra de información ](images/vis-color-image17.png)

**Incorrecto:**

![captura de pantalla del mensaje que contiene "barra dorada" ](images/vis-color-image18.png)

En el ejemplo incorrecto, el mensaje hace referencia a la Windows Internet Explorer de información por su color en lugar de por su nombre.

