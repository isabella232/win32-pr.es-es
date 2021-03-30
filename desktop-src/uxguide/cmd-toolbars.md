---
title: Barras de herramientas
description: Las barras de herramientas son una manera de agrupar comandos para obtener un acceso eficaz.
ms.assetid: 8f36307c-54fc-493d-a2ff-57db29e3508d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: bb32c84f6090bc25b985b8445fb351a478c24c2b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104553481"
---
# <a name="toolbars"></a>Barras de herramientas

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Las barras de herramientas son una manera de agrupar comandos para obtener un acceso eficaz.

![captura de pantalla de dos barras de herramientas con elementos etiquetados ](images/cmd-toolbars-image1.png)

Algunas barras de herramientas típicas.

**Usar barras de herramientas además o en lugar de barras de menús.** Las barras de herramientas pueden ser más eficaces que las barras de menús porque son directas (siempre se muestran en lugar de mostrarse al hacer clic con el mouse), inmediato (en lugar de requerir una entrada adicional) y contienen los comandos usados con mayor frecuencia (en lugar de una lista completa). A diferencia de las barras de menús, las barras de herramientas no tienen que ser exhaustivas o autoexplicativas, tan rápidas, prácticas y eficaces.

Algunas barras de herramientas son personalizables, lo que permite a los usuarios agregar o quitar barras de herramientas, cambiar su tamaño y ubicación, e incluso cambiar su contenido. Algunos tipos de barras de herramientas se pueden desacoplar, lo que resulta en una ventana de paleta. Para obtener más información sobre las variedades de barras de herramientas, consulte [patrones de uso](#usage-patterns) en este artículo.

> [!Note]  
> Las instrucciones relacionadas con los [menús](cmd-menus.md), los [botones de comando](ctrl-command-buttons.md)y los [iconos](vis-icons.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidirte, intenta responder a estas preguntas:

-   **¿La ventana es una ventana principal?** Las barras de herramientas funcionan bien para las ventanas principales, pero suelen ser abrumadoras para las ventanas secundarias. En el caso de las ventanas secundarias, use [botones de comando](ctrl-command-buttons.md), [botones de menú](ctrl-command-buttons.md)y [vínculos](ctrl-command-links.md) en su lugar.
-   **¿Hay un pequeño número de comandos usados con frecuencia?** Las barras de herramientas no pueden controlar tantos comandos como barras de menús, por lo que funcionan mejor como una manera de tener acceso eficazmente a un pequeño número de comandos usados con frecuencia.
-   **¿La mayoría de los comandos son inmediatos?** Es decir, ¿son principalmente comandos que no requieren ninguna entrada adicional? Para ser eficientes, las barras de herramientas deben tener una sensación directa e inmediata. Si no es así, las barras de menús son más adecuadas para los comandos que requieren una entrada adicional.
-   **¿Se puede presentar la mayoría de los comandos directamente?** Es decir, los usuarios interactúan con ellos mediante un solo clic? Aunque algunos comandos se pueden presentar mediante botones de menú, la mayoría de los comandos se convierten en la mayor parte de la eficacia de la barra de herramientas, lo que permite que una barra de menús sea una opción mejor.
-   **¿Los comandos se representan bien mediante iconos?** Los botones de barra de herramientas se representan normalmente mediante iconos en lugar de etiquetas de texto (aunque algunos botones de la barra de herramientas utilizan ambos), mientras que los comandos de menú se representan mediante el texto. Si los iconos de comando no son de alta calidad y no se explican por sí solos, una barra de menús puede ser una opción mejor.

Si el programa tiene una barra de herramientas sin una barra de menús, y la mayoría de los comandos son accesibles indirectamente a través de los botones de menú y los [botones de expansión](ctrl-command-buttons.md), esta barra de herramientas es básicamente una barra de menús. En su lugar, aplique el patrón de menús de la [barra de herramientas](cmd-menus.md) en las instrucciones de los menús.

## <a name="design-concepts"></a>Conceptos de diseño

Una buena barra de menús es un catálogo completo de todos los comandos de nivel superior disponibles, mientras que una buena barra de herramientas proporciona un acceso rápido y cómodo a los comandos usados con frecuencia. Una barra de herramientas no intenta entrenar a los usuarios para que sean productivos. Una vez que los usuarios obtengan información sobre cómo obtener acceso a un comando en una barra de herramientas, rara vez tienen que acceder al comando desde la barra de menús. Por estos motivos, no es necesario que la barra de menús y la barra de herramientas de un programa se correspondan directamente.

### <a name="toolbars-vs-menu-bars"></a>Barras de herramientas y barras de menús

Tradicionalmente, las barras de herramientas son diferentes de las barras de menús de las siguientes maneras:

-   **Frecuencia.** Las barras de herramientas solo presentan los comandos usados con mayor frecuencia, mientras que las barras de menús catalogan todos los comandos de nivel superior disponibles dentro de un programa.
-   **Inmediatez.** Hacer clic en un comando de la barra de herramientas surte efecto inmediatamente, mientras que un comando de menú puede requerir una entrada adicional. Por ejemplo, un comando imprimir en una barra de menús muestra primero el cuadro de diálogo Imprimir, mientras que un botón Imprimir de la barra de herramientas imprime inmediatamente una única copia de un documento en la impresora predeterminada.

    ![captura de pantalla del botón de impresora de la barra de herramientas seleccionado ](images/cmd-toolbars-image2.png)

    En este ejemplo, al hacer clic en el botón Imprimir de la barra de herramientas, se imprime inmediatamente una única copia de un documento en la impresora predeterminada.

-   **Dirección.** Los comandos de la barra de herramientas se invocan con un solo clic, mientras que los comandos de la barra de menús requieren desplazarse por el menú.
-   **Número y densidad.** El espacio de pantalla necesario para una barra de herramientas es proporcional al número de comandos y ese espacio siempre se usa, incluso si los comandos no lo son. Por lo tanto, las barras de herramientas deben usar su espacio de forma eficaz. Por el contrario, los comandos de la barra de menús suelen estar ocultos en la vista y su estructura jerárquica permite cualquier número de comandos.
-   **Tamaño y presentación.** Para empaquetar muchos comandos en un espacio pequeño, las barras de herramientas suelen usar comandos basados en iconos (con etiquetas basadas en la información sobre herramientas), mientras que las barras de menús usan comandos basados en texto (con iconos opcionales). Aunque los botones de la barra de herramientas pueden tener etiquetas de texto estándar, usan mucho más espacio.

    ![captura de pantalla de la barra de herramientas con la etiqueta de envío y recepción ](images/cmd-toolbars-image3.png)

    Los botones de barra de herramientas con etiqueta toman al menos tres veces más espacio que los no etiquetados.

-   **se explica por sí solo.** Las barras de herramientas bien diseñadas necesitan iconos que principalmente se explican por sí solos, ya que los usuarios no pueden encontrar comandos de forma eficaz simplemente mediante la información sobre herramientas. Sin embargo, las barras de herramientas siguen funcionando bien si algunos comandos menos usados no se explican por sí solos.

    ![captura de pantalla de la barra de herramientas con iconos conocidos ](images/cmd-toolbars-image4.png)

    En este ejemplo, los iconos que se usan con más frecuencia se explican por sí solos.

-   **Reconocible y distinguible.** Para los comandos usados con frecuencia, los usuarios recuerdan los atributos de botón de la barra de herramientas, como ubicación, forma y color. Con las barras de herramientas bien diseñadas, los usuarios pueden encontrar los comandos rápidamente aunque no recuerden el símbolo de icono exacto. Por el contrario, los usuarios recuerdan las ubicaciones de comandos de la barra de menús que se usan con frecuencia, pero dependen de las etiquetas de comando para efectuar selecciones.

    ![captura de pantalla del cuadro de diálogo Opciones de recortes ](images/cmd-toolbars-image5.png)

    En el caso de los comandos de la barra de herramientas, ubicación distintiva, forma y color ayudan a que los iconos sean reconocibles y distinguibles.

    ![captura de pantalla de la barra de menús con el comando de archivo seleccionado ](images/cmd-toolbars-image6.png)

    En el caso de los comandos de la barra de menús, los usuarios dependen en última instancia de sus etiquetas.

### <a name="efficiency"></a>Eficacia

Dadas sus características, las barras de herramientas deben diseñarse principalmente para mejorar la eficacia. Una barra de herramientas ineficaz no tiene sentido.

**Si solo hace algo...**

Asegúrese de que las barras de herramientas están diseñadas principalmente para mejorar la eficacia. Las barras de herramientas de foco en comandos que se usan con frecuencia, inmediato, directo y fácil de reconocer.

### <a name="hiding-menu-bars"></a>Ocultar barras de menús

Por lo general, las barras de herramientas funcionan muy bien con barras de menús: las barras de herramientas adecuadas proporcionan eficiencia y las barras de menús adecuadas proporcionan una gran exhaustividad. **Tener las barras de menús y las barras de herramientas permite que cada una de ellas se Centre en sus puntos fuertes sin poner en peligro.**

Sorprendentemente, este modelo se desglosa con programas sencillos. En el caso de los programas con pocos comandos, tener una barra de menús y una barra de herramientas no tiene sentido, ya que la barra de menús acaba siendo una versión redundante e ineficaz de la barra de herramientas.

Para eliminar esta redundancia, muchos programas sencillos de Windows Vista se centran en proporcionar comandos únicamente a través de la barra de herramientas y ocultar la barra de menús de forma predeterminada. Estos programas incluyen el explorador de Windows, Windows Internet Explorer, Windows Media Player y la Galería fotográfica de Windows.

No se trata de un cambio pequeño. Al quitar la barra de menús, se cambia fundamentalmente la naturaleza de las barras de herramientas, ya que estas barras de herramientas deben ser completas y cambiar de las siguientes maneras:

-   **Frecuencia.** Al quitar la barra de menús, todos los comandos que no estén disponibles directamente desde una ventana o sus menús contextuales deben ser accesibles desde la barra de herramientas, independientemente de su frecuencia de uso.
-   **Inmediatez.** Al quitar la barra de menús, la barra de herramientas es el único punto de acceso visible para los comandos, lo que requiere que la barra de herramientas tenga las versiones totalmente funcionales. Por ejemplo, si no hay ninguna barra de menús, un comando imprimir en una barra de herramientas debe mostrar el cuadro de diálogo Imprimir en lugar de imprimirlo inmediatamente. (Aunque el uso de un botón de expansión es un buen compromiso en este caso. Vea [botones de división y menú estándar](#standard-menu-and-split-buttons) para el botón de división de impresión estándar).

    ![captura de pantalla de las opciones del comando imprimir y la barra de herramientas ](images/cmd-toolbars-image7.png)

    En este ejemplo, el botón de la barra de herramientas imprimir de la Galería fotográfica de Windows tiene un comando imprimir que muestra el cuadro de diálogo Imprimir.

-   **Dirección.** Para ahorrar espacio y evitar la confusión, los comandos que se usan con menos frecuencia se pueden mover a botones de menú, lo que hace que sean menos directos.

Las barras de herramientas que se usan para complementar una barra de menús están diseñadas de forma distinta que las barras de herramientas diseñadas para usarse con una barra de menús que se ha quitado u oculto. Además, dado que no se puede suponer que los usuarios muestren una barra de menús oculta para ejecutar un solo comando, la ocultación de una barra de menús debe tratarse de la misma forma que al tomar decisiones de diseño. (Si oculta la barra de menús de forma predeterminada, no suponga que los usuarios piensan en Mostrar la barra de menús para buscar un comando o incluso averiguar cómo se muestra).

El diseño de una barra de herramientas para trabajar sin una barra de menús suele implicar algunos peligros. Pero para mayor eficacia, no ponga en peligro demasiado. Si ocultar la barra de menús da como resultado una barra de herramientas ineficaz, no oculte la barra de menús.

### <a name="keyboard-accessibility"></a>Accesibilidad de teclado

Desde el teclado, el acceso a las barras de herramientas es bastante diferente del acceso a las barras de menús. Las barras de menús reciben el foco de entrada cuando los usuarios presionan la tecla Alt y pierden el foco de entrada con la tecla ESC. Una vez que una barra de menús tiene el foco de entrada, se navega independientemente del resto de la ventana y controla todas las teclas de dirección, Inicio, fin y teclas de tabulación. Por el contrario, las barras de herramientas reciben el foco de entrada cuando los usuarios presionan la tecla TAB en todo el contenido de la ventana. Dado que las barras de herramientas están por última vez en el orden de tabulación, es posible que tarden algún esfuerzo en activar una página ocupada (a menos que los usuarios sepan usar Mayús + Tab para desplazarse hacia atrás).

La accesibilidad presenta un dilema aquí: mientras que las barras de herramientas son más fáciles de ver para los usuarios del mouse, son menos accesibles para los usuarios del teclado. Esto no supone un problema si hay una barra de menús y una barra de herramientas, pero es si se quita o se oculta la barra de menús.

Por motivos de accesibilidad, prefiere conservar la barra de menús en lugar de quitarla completamente en favor de una barra de herramientas. Si tiene que elegir entre quitar la barra de menús y simplemente ocultarla, prefiera ocultarla.

## <a name="usage-patterns"></a>Patrones de uso

Las barras de herramientas tienen varios patrones de uso:



|                                                                                                                      |                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barras de herramientas principales**<br/> barra de herramientas diseñada para trabajar sin una barra de menús, ya sea oculta o quitada. <br/> | las barras de herramientas principales deben equilibrar la necesidad de eficacia con la exhaustividad, por lo que funcionan mejor para programas sencillos. <br/> ![captura de pantalla de la barra de herramientas del explorador de Windows ](images/cmd-toolbars-image8.png)<br/> Barra de herramientas principal del explorador de Windows.<br/>                                                                        |
| **Barras de herramientas complementarias**<br/> una barra de herramientas diseñada para trabajar con una barra de menús. <br/>                         | las barras de herramientas complementarias pueden centrarse en la eficacia sin ningún riesgo. <br/> ![captura de pantalla de una barra de menús en una barra de herramientas ](images/cmd-toolbars-image9.png)<br/> Barra de herramientas complementaria de Windows Movie Maker.<br/>                                                                                                                  |
| **Menús de barra de herramientas**<br/> barra de menús implementada como una barra de herramientas. <br/>                                        | los menús de barra de herramientas son barras de herramientas que se componen principalmente de comandos en [botones de menú](ctrl-command-buttons.md) y botones de expansión, con solo unos pocos comandos directos, si los hay. <br/> ![captura de pantalla de la barra de menús con iconos y comandos ](images/cmd-toolbars-image10.png)<br/> Menú de la barra de herramientas de la Galería fotográfica de Windows.<br/> |
| **Barras de herramientas personalizables**<br/> barra de herramientas que pueden personalizar los usuarios. <br/>                          | las barras de herramientas personalizables permiten a los usuarios agregar o quitar barras de herramientas, cambiar su tamaño y ubicación, e incluso cambiar su contenido. <br/> ![captura de pantalla de una barra de herramientas con docenas de iconos ](images/cmd-toolbars-image11.png)<br/> Barra de herramientas personalizable de Microsoft Visual Studio.<br/>                                             |
| **Ventanas de paleta**<br/> un cuadro de diálogo no modal que presenta una matriz de comandos. <br/>                 | las ventanas de paleta son barras de herramientas desacopladas. <br/> ![captura de pantalla de un cuadro de diálogo de colores ](images/cmd-toolbars-image12.png)<br/> ![captura de pantalla de un cuadro de diálogo de fuentes ](images/cmd-toolbars-image13.png)<br/> Ventanas de paleta de Paint de Windows.<br/>                                                                             |



 

Las barras de herramientas tienen estos estilos:



|                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iconos sin etiqueta**<br/> una o más filas de botones pequeños de iconos sin etiquetar. <br/>                                           | Use este estilo si hay demasiados botones para etiquetar o si el programa se usa con frecuencia. con este estilo, los programas con funcionalidad compleja pueden tener varias filas y, por lo tanto, este es el único estilo que debe ser personalizable. con este estilo, algunos botones de comando se pueden etiquetar si se usan con frecuencia. <br/> ![captura de pantalla de la barra de herramientas con iconos pequeños sin etiquetar ](images/cmd-toolbars-image14.png)<br/> Barra de herramientas de iconos sin etiqueta de WordPad.<br/> |
| **Iconos grandes sin etiqueta**<br/> una sola fila de botones grandes de iconos sin etiqueta. <br/>                                         | Use este estilo para utilidades sencillas que tienen iconos fácilmente reconocibles y que normalmente se ejecutan en ventanas pequeñas. <br/> ![captura de pantalla de la barra de herramientas con iconos grandes y sin etiqueta ](images/cmd-toolbars-image15.png)<br/> ![captura de pantalla de la barra de herramientas con iconos grandes ](images/cmd-toolbars-image16.png)<br/> Barras de herramientas de iconos grandes sin etiquetar desde Windows Live Messenger y la herramienta recortes de Windows.<br/>                                                                       |
| **Iconos con etiqueta**<br/> una sola fila de iconos con etiqueta pequeña. <br/>                                                          | Use este estilo si hay pocos comandos o si el programa no se usa con frecuencia. Este estilo siempre tiene una sola fila. <br/> ![captura de pantalla de la barra de herramientas con iconos etiquetados ](images/cmd-toolbars-image8.png)<br/> Barra de herramientas de iconos con etiqueta del explorador de Windows.<br/>                                                                                                                                                                                                               |
| **Barras de herramientas parciales**<br/> una fila parcial de iconos pequeños que se usa para ahorrar espacio cuando no es necesaria una barra de herramientas completa. <br/>       | Use este estilo para Windows con botones de navegación, un cuadro de búsqueda o pestañas para eliminar el peso innecesario en la parte superior de la ventana. <br/> ![captura de pantalla de la barra de menús, barra de herramientas y barra de favoritos ](images/cmd-toolbars-image17.png)<br/> Las barras de herramientas parciales se pueden combinar con botones de navegación, un cuadro de búsqueda o pestañas.<br/>                                                                                                                                                  |
| **Barras de herramientas parciales grandes**<br/> una fila parcial de iconos grandes que se usa para ahorrar espacio cuando no se necesita una barra de herramientas completa. <br/> | Use este estilo para utilidades sencillas que tengan botones de navegación o un cuadro de búsqueda para eliminar el peso innecesario en la parte superior de la ventana. <br/> ![captura de pantalla de una barra de herramientas parcial grande ](images/cmd-toolbars-image18.png)<br/> Una amplia barra de herramientas parcial de Windows Defender.<br/>                                                                                                                                                                                         |



 

Por último, los controles de barra de herramientas tienen varios patrones de uso:



|                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Botones de iconos de comando**<br/> al hacer clic en un botón de comando, se inicia una acción inmediata. <br/>                                                                                                 | ![captura de pantalla de una barra de herramientas de iconos con etiqueta ](images/cmd-toolbars-image19.png)<br/> Ejemplos de botones de comando de icono desde fax y escáner de Windows.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Botones de icono de modo**<br/> al hacer clic en un botón modo, se entra en el modo seleccionado. <br/>                                                                                                            | ![captura de pantalla de una barra de herramientas vertical ](images/cmd-toolbars-image20.png)<br/> Ejemplos de botones de modo de Paint de Windows.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Botones de icono de propiedad**<br/> el estado de un botón de propiedad refleja el estado de los objetos seleccionados actualmente, si los hay. al hacer clic en el botón, se aplica el cambio a los objetos seleccionados. <br/> | ![captura de pantalla de iconos de formato y texto seleccionado ](images/cmd-toolbars-image21.png)<br/> Ejemplos de botones de propiedades de Microsoft Word.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Botones de iconos con etiqueta**<br/> botón de comando o de propiedad con la etiqueta de un icono y una etiqueta de texto. <br/>                                                                               | Estos botones se utilizan para los botones de la barra de herramientas usados con frecuencia cuyo icono no es suficientemente explicativo. también se usan en las barras de herramientas que tienen tan pocos botones en los que cada botón puede tener una etiqueta de texto. <br/> ![Captura de pantalla que muestra la barra de herramientas con iconos etiquetados para los botones usados con mayor frecuencia. ](images/cmd-toolbars-image22.png)<br/> Una barra de herramientas con los botones usados con mayor frecuencia etiquetados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Botones de menú**<br/> un botón de comando que se usa para presentar un pequeño conjunto de comandos relacionados. <br/>                                                                                                | un solo triángulo que apunta hacia abajo indica que al hacer clic en el botón se muestra un menú. <br/> ![captura de pantalla de la lista desplegable de barras de herramientas y comandos ](images/cmd-toolbars-image23.png)<br/> Botón de menú con un pequeño conjunto de comandos relacionados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Botones de expansión**<br/> un botón de comando que se usa para consolidar las variaciones de un comando, especialmente cuando uno de los comandos se usa la mayor parte del tiempo. <br/>                                     | ![captura de pantalla del botón de impresión de división ](images/cmd-toolbars-image24.png)<br/> botón de expansión en estado normal.<br/> al igual que un botón de menú, un solo triángulo que apunta hacia abajo indica que al hacer clic en la parte más a la derecha del botón se muestra un menú. <br/> ![captura de pantalla de comandos de botón de impresión dividida ](images/cmd-toolbars-image25.png)<br/> botón de expansión quitado.<br/> en este ejemplo, se usa un botón de expansión para consolidar todos los comandos relacionados con la impresión. el comando de impresión inmediato se usa la mayor parte del tiempo, por lo que los usuarios normalmente no necesitan ver los demás comandos. <br/> a diferencia de un botón de menú, al hacer clic en la parte izquierda del botón, la acción se realiza directamente en la etiqueta. los botones de expansión son eficaces en situaciones en las que es probable que el siguiente comando sea el mismo que el último comando. en este caso, la etiqueta se cambia al último comando, como sucede con un selector de colores:<br/> ![captura de pantalla del icono de cubo que vierte Paint ](images/cmd-toolbars-image26.png)<br/> En este ejemplo, la etiqueta se cambia al último comando.<br/> |
| **Listas desplegables**<br/> lista desplegable (editable o de solo lectura) utilizada para ver o cambiar una propiedad. <br/>                                                                                   | ![captura de pantalla de la lista desplegable de fuentes ](images/cmd-toolbars-image27.png)<br/> En este ejemplo, las listas desplegables se utilizan para ver y establecer los atributos de fuente.<br/> Una lista desplegable de una barra de herramientas refleja el estado del objeto seleccionado actualmente, si existe. Cambiar la lista cambia el estado del objeto seleccionado. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="guidelines"></a>Directrices

### <a name="presentation"></a>Presentación

-   **Elija un estilo de barra de herramientas adecuado en función del número de comandos y su uso.** Vea la tabla de estilos de barra de herramientas anterior para obtener instrucciones sobre cómo elegir. Evite usar una configuración de barra de herramientas que tenga demasiado espacio en el área de trabajo del programa.
-   **Coloque las barras de herramientas justo encima del área de contenido,** debajo de la barra de menús y la barra de direcciones, si está presente.
-   **Si el espacio es Premium, Ahorre espacio:**

    -   Omitir las etiquetas de iconos conocidos y comandos de uso menos frecuente.
    -   Usar solo una barra de herramientas parcial en lugar de todo el ancho de la ventana.
    -   Consolidación de comandos relacionados con un botón de menú o un botón de expansión.
    -   Usar un [botón de contenido adicional de desbordamiento](glossary.md) para mostrar los comandos usados con menos frecuencia.
    -   Mostrar comandos solo cuando se aplican al contexto actual.

    ![captura de pantalla de iconos comunes de la barra de herramientas sin etiqueta ](images/cmd-toolbars-image28.png)

    La barra de herramientas de Windows Internet Explorer ahorra espacio al omitir las etiquetas de iconos conocidos, usar una barra de herramientas parcial y usar un botón de contenido adicional de desbordamiento para los comandos usados con menos frecuencia.

-   **Para el patrón de barra de herramientas iconos sin etiquetar, use una configuración predeterminada que no contenga más de dos filas de barras de herramientas.** Si pueden ser útiles más de dos filas, haga que las barras de herramientas sean personalizables. Comenzar con más de dos filas puede sobrecargar a los usuarios y ocupar demasiado espacio en el área de trabajo del programa.

    **Incorrecto:**

    ![captura de pantalla de la barra de menús y tres filas de barras de herramientas ](images/cmd-toolbars-image29.png)

    Una configuración predeterminada con más de dos filas de barras de herramientas tiene como resultado un exceso de objetos visuales.

-   **Deshabilitar los botones de la barra de herramientas individuales que no se aplican al contexto actual,** en lugar de quitarlos. Esto hace que el contenido de la barra de herramientas sea estable y más fácil de encontrar.
-   **Deshabilitar los botones individuales de la barra de herramientas si al hacer clic en ellos se produciría directamente un error.** Esto es necesario para mantener una sensación directa.
-   **Para el patrón de barra de herramientas iconos sin etiquetar, quite todas las barras de herramientas si no se aplican al contexto actual.** Solo se muestran en los modos aplicables.

    ![captura de pantalla de la barra de herramientas de depuración ](images/cmd-toolbars-image30.png)

    En este ejemplo, la barra de herramientas de depuración solo se muestra cuando se ejecuta el programa.

-   **Mostrar botones de la barra de herramientas alineados a la izquierda.** El icono de ayuda, si está presente, está alineado a la derecha.

    ![captura de pantalla de la barra de herramientas, icono de ayuda alineado a la derecha ](images/cmd-toolbars-image31.png)

    Todos los botones de la barra de herramientas se alinean a la izquierda excepto para obtener ayuda.

    **Excepción:** Las barras de herramientas de estilo de Windows 7 alinean a la izquierda comandos específicos del programa, pero alinean a la derecha comandos conocidos y estándar, como opciones, vistas y ayuda.

-   **No cambie las etiquetas de botón de la barra de herramientas dinámicamente.** Hacerlo es confuso e inesperado. Sin embargo, puede cambiar el icono para que refleje el estado actual.

    ![captura de pantalla del icono de cubo que vierte Paint ](images/cmd-toolbars-image26.png)

    En este ejemplo, se cambia el icono para indicar el comando predeterminado.

### <a name="controls-and-commands"></a>Controles y comandos

-   **Prefiera los comandos que se usan con más frecuencia.**
    -   **En el caso de las barras de herramientas principales, proporcione comandos completos.** Las barras de herramientas principales no tienen que ser tan completas como barras de menús, pero tienen que proporcionar todos los comandos que no se pueden detectar fácilmente en otro lugar. Las barras de herramientas principales no necesitan tener comandos para:
        -   Comandos que se encuentran directamente en la propia interfaz de usuario.
        -   Comandos a los que normalmente se accede a través de menús contextuales.
        -   Comandos conocidos y estándar, como cortar, copiar y pegar.
    -   **En el caso de las barras de herramientas complementarias, proporcione comandos que se usan con más frecuencia.** Los comandos de la barra de menús son un superconjunto de los comandos de la barra de herramientas, por lo que no tiene que proporcionar todo. Céntrese en el acceso rápido y práctico del comando y omita el resto.
-   **Prefiere controles directos.** Use los botones de la barra de herramientas en el siguiente orden de preferencia:
    -   **Botón de icono.** Directo y requiere espacio mínimo.
    -   **Botón de icono con etiqueta.** Directo, pero ocupa más espacio.
    -   **Botón de expansión.** Directo para el comando más común, pero controla las variaciones de comandos.
    -   **Botón de menú.** Indirecto, pero presenta muchos comandos.
-   **Prefiere comandos inmediatos.** Para los comandos que pueden ser inmediatos o tener una entrada adicional para la flexibilidad:
    -   En el caso de las barras de herramientas principales, use las versiones flexibles de los comandos (por ejemplo, imprimir...).
    -   En el caso de las barras de herramientas complementarias, use las versiones inmediatas de la barra de herramientas (por ejemplo, imprimir) y use versiones flexibles en la barra de menús (por ejemplo, imprimir...).
-   **Proporcione etiquetas para los comandos usados con frecuencia,** especialmente si sus iconos no son iconos conocidos.

    **Aceptable:**

    ![captura de pantalla de la barra de herramientas sin iconos etiquetados ](images/cmd-toolbars-image32.png)

    **Manera**

    ![captura de pantalla de la barra de herramientas con algunos iconos etiquetados ](images/cmd-toolbars-image33.png)

    La barra de herramientas de fax y escáner de Windows tiene pocos comandos, por lo que la versión mejor etiqueta las más importantes.

-   No coloque los comandos en los menús de la barra de herramientas que también están directamente en la barra de herramientas.

    **Incorrecto:**

    ![captura de pantalla del comando imprimir en la barra de herramientas y el menú ](images/cmd-toolbars-image34.png)

    En este ejemplo, la impresión está directamente en la barra de herramientas, por lo que no es necesario que esté en el menú.

### <a name="organization-and-order"></a>Organización y pedido

-   **Organice los comandos de una barra de herramientas en grupos relacionados.**
-   **Coloque primero los grupos usados con mayor frecuencia. Dentro de un grupo, coloque los comandos en su orden lógico.** En general, los comandos deben tener un flujo lógico para que sean fáciles de encontrar y, al mismo tiempo, los comandos que se usan con más frecuencia aparecen en primer lugar. Hacerlo es más eficaz, especialmente si hay desbordamiento.
-   **Utilice los divisores de grupo solo si los comandos de los grupos están débilmente acoplados.** Esto hace que las agrupaciones sean obvias y los comandos sean más fáciles de encontrar.

    ![Captura de pantalla que muestra una barra de herramientas con iconos bien organizados mediante divisores de grupo.](images/cmd-toolbars-image35.png)

    ![captura de pantalla de la barra de herramientas con iconos bien organizados ](images/cmd-toolbars-image36.png)

    Ejemplos de barras de herramientas agrupadas de Windows Mail.

-   **Evite colocar comandos destructivos junto a los comandos usados con frecuencia.** Use el orden o la agrupación para obtener la separación. Además, considere la posibilidad de no colocar comandos destructivos en la barra de herramientas, pero solo en la barra de menús o en los menús contextuales.

    **Aceptable:**

    ![captura de pantalla de los botones de impresión y eliminación adyacentes ](images/cmd-toolbars-image37.png)

    **Manera**

    ![captura de pantalla de los botones de impresión y eliminación separados ](images/cmd-toolbars-image38.png)

    En el mejor ejemplo, el comando eliminar está físicamente separado de la impresión.

-   **Utilice el botón de contenido adicional de desbordamiento para indicar que no se pueden mostrar todos los comandos.** Pero use el desbordamiento solo si no hay espacio suficiente para mostrar todos los comandos.

    **Incorrecto:**

    ![captura de pantalla de la barra de favoritos y comandos ocultos ](images/cmd-toolbars-image39.png)

    El botón de contenido adicional de desbordamiento indica que no se muestran todos los comandos, pero que más pueden ser con un diseño mejor.

-   **Asegúrese de que los comandos usados con más frecuencia son accesibles directamente desde la barra de herramientas (es decir, no en el desbordamiento) en tamaños de ventana pequeños.** Si es necesario, reordene los comandos, mueva los comandos usados con menos frecuencia a botones de menú o botones de expansión, o incluso quítelos completamente de la barra de herramientas. Si el problema persiste, reconsidere la posibilidad de elegir el estilo de la barra de herramientas.

### <a name="hiding-menu-bars"></a>Ocultar barras de menús

Por lo general, las barras de herramientas funcionan muy bien con barras de menús, ya que tener ambos permite centrarse en sus puntos fuertes sin poner en peligro.

-   Oculte la barra de menús de forma predeterminada si el diseño de la barra de herramientas hace que una barra de menús sea redundante.
-   Oculte la barra de menús en lugar de quitarla por completo, ya que las barras de menús son más accesibles para los usuarios del teclado.
-   Para restaurar la barra de menús, proporcione una opción de marca de verificación de la barra de menús en la categoría de menú Ver (para barras de herramientas principales) o herramientas (para barras de herramientas secundarias). Para obtener más información, vea [botón de expansión y menú estándar](#standard-menu-and-split-buttons).
-   Mostrar la barra de menús cuando los usuarios presionen la tecla Alt y establecer el foco de entrada en la primera categoría del menú.

### <a name="interaction"></a>Interacción

-   Al mantener el puntero, muestra el mantenimiento [del botón para](glossary.md) indicar que se hace clic en el icono. Después del tiempo de espera de la información sobre herramientas, muestre la información sobre herramientas o el recuadro

    ![captura de pantalla de un recuadro informativo que describe un botón ](images/cmd-toolbars-image40.png)

    En este ejemplo se muestran los distintos Estados de presentación.

-   En un solo clic a la izquierda:
    -   En el caso de los botones de comando, interactúe con el control como de costumbre.
    -   En los botones de modo, muestre el control para que refleje el modo seleccionado actualmente. Si el modo afecta al comportamiento de la interacción con el mouse, cambie también el puntero.

        ![captura de pantalla de un puntero con forma de cubo de pintura ](images/cmd-toolbars-image41.png)

        En este ejemplo, el puntero se cambia para mostrar el modo de interacción con el mouse.

    -   En el caso de los botones de propiedades y listas desplegables, muestre el control para reflejar el estado de los objetos seleccionados actualmente, si los hay. En interacción, actualice el estado del control y aplique el cambio a los objetos seleccionados. Si no hay nada seleccionado, no haga nada.

-   En el doble clic a la izquierda, realice la misma acción que un solo clic a la izquierda.
    -   **Excepción:** En raras ocasiones, un comando de la barra de herramientas se puede usar de forma más eficaz. En tales casos, use el doble clic para alternar el modo.

        ![captura de pantalla de las funciones del botón de recuadro informativo ](images/cmd-toolbars-image42.png)

        En este ejemplo, al hacer doble clic en el comando Copiar formato entra en un modo en el que todos los clics posteriores aplican el formato. Los usuarios pueden dejar el modo haciendo un solo clic a la izquierda.

-   Al hacer clic con el botón derecho:
    -   En el caso de las barras de herramientas personalizables, muestre el menú contextual para personalizar la barra de herramientas. Mostrar el menú al hacer clic con el botón derecho en el mouse hacia abajo, no al subir el mouse.
    -   En el caso de otras barras de herramientas, no haga nada.

### <a name="icons"></a>Iconos

-   **Proporcionar iconos para todos los controles de barra de herramientas excepto las listas desplegables.**

    ![captura de pantalla de la lista desplegable de tamaño de fuente ](images/cmd-toolbars-image43.png)

    Las listas desplegables no necesitan iconos, pero todos los demás controles de la barra de herramientas sí lo hacen.

    **Excepción:** Las barras de herramientas de estilo Windows 7 usan iconos únicamente para comandos cuyos iconos son conocidos; en caso contrario, usan etiquetas de texto sin iconos. Al hacerlo, se mejora la claridad de las etiquetas, pero se requiere más espacio.

-   **Asegúrese de que los iconos de la barra de herramientas están claramente visibles en el color de fondo de la barra de herramientas.** Evalúe siempre los iconos de la barra de herramientas en el contexto y en el modo de alto contraste.
-   **Elija diseños de icono que comuniquen claramente su finalidad, especialmente para los comandos que se usan con más frecuencia.** Las barras de herramientas bien diseñadas necesitan iconos que se explican por sí solos porque los usuarios no pueden encontrar comandos de forma eficaz mediante su información sobre herramientas. Sin embargo, las barras de herramientas siguen funcionando bien si los iconos de algunos comandos menos usados no se explican por sí solos.
-   **Elija los iconos que sean reconocibles y distinguibles, especialmente para los comandos que se usan con más frecuencia.** Asegúrese de que los iconos tienen formas y colores distintivos. Esto ayuda a los usuarios a encontrar los comandos rápidamente aunque no recuerden el símbolo del icono.
-   **Asegúrese de que los iconos de la barra de herramientas cumplen las directrices del icono de estilo Aero.**

Para obtener más información y ejemplos, vea [iconos](vis-icons.md).

### <a name="standard-menu-and-split-buttons"></a>Botón de división y menú estándar

Si está utilizando botones de menú y botones de expansión en una barra de herramientas, intente usar las siguientes estructuras de menú estándar y sus comandos correspondientes siempre que sea posible. A diferencia de las barras de menús, los comandos de la barra de herramientas no toman teclas de acceso.

**Barras de herramientas principales**

Estos comandos reflejan los comandos que se encuentran en las barras de menús estándar, por lo que solo deben usarse para las barras de herramientas principales. En esta lista se muestran las etiquetas de botón (y tipo) con su orden y separadores, teclas de método abreviado y puntos suspensivos. **Tenga en cuenta que el comando para mostrar y ocultar la barra de menús está en el menú Ver.**

<dl> Archivo <dl> NewCtrl + N  
Abrir... Ctrl + O  
Cerrar <separator>  
SaveCtrl + S  
Guardar como... <separator>  
Enviar a <separator>  
Imprimir... Ctrl + P  
Vista previa de impresión  
Configurar página <separator>  
Exinicializar + F4 (normalmente no se proporciona el acceso directo)
</dl> </dd> Edit(menu button) <dl> UndoCtrl + Z  
RedoCtrl + Y <separator>  
CutCtrl + X  
CopyCtrl + C  
PasteCtrl + V <separator>  
Seleccionar allCtrl + A <separator>  
DeleteDel (normalmente no se proporciona el acceso directo)  
Cambiar nombre... <separator>  
Buscar... Ctrl + F  
Buscar nextF3 (no se proporciona el comando normalmente)  
Reemplazar... Ctrl + H  
Vete a... Ctrl + G
</dl> </dd> <dd>Imprimir (botón de expansión) <dl> Imprimir... Ctrl + P  
Vista previa de impresión <separator>  
Configurar página
</dl> </dd> Vista (botón de menú) <dl> Barra de menús (comprobar si está visible)  
Panel de detalles (comprobar si está visible)  
Panel de vista previa (comprobar si está visible)  
Barra de estado (comprobar si está visible) <separator>  
Zoom  
Zoom inctrl + +  
Zoom outctrl +- <separator>  
Tamaño del texto (la configuración seleccionada tiene viñeta) <dl> Valor  
Mayor  
Media  
Más pequeño  
Menor
</dl> </dd> <separator> ScreenF11 completo  
RefreshF5
</dl> </dd> Tools(menu button) <dl> ... <separator>  
Opciones
</dl>> </dd> Help(split button, use the Help icon) <dl> <program name> helpF1 <separator>  
Sobre <program name>  
</dl> </dd> </dl>

**Barras de herramientas complementarias**

Estos comandos complementan las barras de menús estándar. En esta lista se muestran las etiquetas de botón (y tipo) con su orden y separadores, teclas de método abreviado y puntos suspensivos. **Tenga en cuenta que el comando para mostrar y ocultar la barra de menús está en el menú herramientas.**

Los nombres de categoría de la barra de herramientas complementaria se diferencian de los nombres de categoría de menú estándar porque tienen que estar más englobados. Por ejemplo, la categoría organizar se usa en lugar de editar porque contiene comandos que no están relacionados con la edición. **Para mantener la coherencia entre las barras de menús y las barras de herramientas, use los nombres de categoría de menú estándar si esto no es engañoso.**

**Incorrecto:**

![captura de pantalla de las mismas opciones para distintos comandos ](images/cmd-toolbars-image44.png)

En este ejemplo, la barra de herramientas debe usar Editar en lugar de organizar por coherencia porque tiene los comandos del menú edición estándar.

### <a name="palette-windows"></a>Ventanas de paleta

-   **Las ventanas de paleta usan barras de título más cortas para minimizar el espacio de la pantalla.** Coloque un botón cerrar en la barra de título.
-   **Establezca el texto de la barra de título en el comando que muestra la ventana de paleta.**
-   **Use el uso de mayúsculas de estilo oraciones sin puntuación final.**
-   **Proporcione un menú contextual para los comandos de administración de ventanas.** Muestra este menú contextual cuando los usuarios hacen clic con el botón derecho en la barra de título.

    ![captura de pantalla del cuadro de herramientas con el menú contextual ](images/cmd-toolbars-image45.png)

    En este ejemplo, los usuarios pueden hacer clic con el botón secundario en la barra de título para mostrar el menú contextual.

-   **Cuando sea posible y útil, haga que las ventanas de la paleta sean ajustables.** Indica que se cambia el tamaño de la ventana, mediante el uso de punteros de redimensionamiento cuando se sitúa sobre el marco de la ventana.
-   **Cuando se vuelve a mostrar una ventana de paleta, se muestra con el mismo estado en el que se ha tenido acceso por última vez.** Al cerrar, guarde el tamaño y la ubicación de la ventana. Al volver a mostrar, restaure el tamaño y la ubicación de la ventana guardada. Además, considere la posibilidad de hacer que estos atributos persisten entre instancias de programa por usuario.

### <a name="customization"></a>Personalización

-   **Proporcionar personalización para las barras de herramientas que se componen de dos o más filas.** Solo el estilo de iconos sin etiqueta necesita personalización. Las barras de herramientas simples con pocos comandos no necesitan personalización.
-   **Proporcione una configuración predeterminada correcta.** Los usuarios no deben tener que personalizar las barras de herramientas para escenarios comunes. No dependa de que los usuarios personalicen su forma de una configuración inicial incorrecta. Supongamos que la mayoría de los usuarios no personalizarán sus barras de herramientas.
-   **Proporcione un menú contextual con los siguientes comandos:**
    -   Una lista de casillas para mostrar las barras de herramientas disponibles
    -   Bloquear o desbloquear barras de herramientas
    -   Personalizar...
-   **Bloquear las barras de herramientas personalizables de forma predeterminada** para evitar cambios accidentales.
-   **Para el comando personalizar, se muestra un cuadro de diálogo de opciones** que permite elegir qué barras de herramientas se muestran y los comandos de cada barra de herramientas.

    ![captura de pantalla del cuadro de diálogo y opciones de personalización ](images/cmd-toolbars-image46.png)

    En este ejemplo, Visual Studio proporciona un cuadro de diálogo Opciones para personalizar las barras de herramientas.

-   Proporcione un comando de restablecimiento para volver a la configuración original de la barra de herramientas en el cuadro de diálogo personalizar opciones.
-   **Proporcionar la capacidad de personalizar las barras de herramientas mediante arrastrar y colocar de las maneras siguientes:**

    -   Establecer el orden y las posiciones de la barra de herramientas.
    -   Establecer las longitudes de la barra de herramientas, que muestran las barras de herramientas que son demasiado pequeñas para mostrar su contenido con un cheurón de desbordamiento.
    -   Si es compatible, desacople las barras de herramientas para convertirlas en ventanas de paleta y viceversa.

    Cuando se muestra el cuadro de diálogo personalizar opciones:

    -   Establezca el contenido de la barra de herramientas.
    -   Establezca el orden del contenido de la barra de herramientas.

    Esto permite a los usuarios realizar cambios de forma más directa y eficaz.

-   **Guardar todas las personalizaciones** de la barra de herramientas por usuario.

### <a name="using-ellipses"></a>Usar puntos suspensivos

Aunque los comandos de la barra de herramientas se usan para acciones inmediatas, a veces se necesita más información para realizar la acción. Use un botón de puntos suspensivos para indicar que un comando requiere más información para poder surtir efecto. Coloque los puntos suspensivos al final de la información sobre herramientas y la etiqueta, si hay alguno.

![captura de pantalla del texto de información sobre herramientas de impresión con puntos suspensivos ](images/cmd-toolbars-image47.png)

En este ejemplo, se imprime... comando muestra un cuadro de diálogo de impresión para recopilar más información.

Sin embargo, si un comando no puede surtir efecto inmediatamente, no es necesario ningún botón de puntos suspensivos. Por lo tanto, por ejemplo, la configuración de uso compartido no tiene puntos suspensivos aunque necesite información adicional, ya que es posible que el comando no surta efecto inmediatamente.

![captura de pantalla de la barra de herramientas, el comando y la información sobre herramientas ](images/cmd-toolbars-image48.png)

El comando de configuración de uso compartido no tiene puntos suspensivos porque no puede surtir efecto inmediatamente.

Dado que las barras de herramientas se muestran constantemente y el espacio es muy **importante, las elipses deben usarse con poca frecuencia**.

> [!Note]  
> En el caso de los menús que se muestran en una barra de herramientas, aplique las [instrucciones de puntos suspensivos](cmd-menus.md).

 

## <a name="recommended-sizing-and-spacing"></a>Ajuste de tamaño y espaciado recomendados

![captura de pantalla de barras de herramientas con información de espaciado ](images/cmd-toolbars-image49.png)

Ajuste de tamaño y espaciado recomendados para las barras de herramientas estándar.

## <a name="labels"></a>Etiquetas

### <a name="general"></a>General

-   **Use mayúsculas de estilo de frase.**
    -   **Excepción:** En el caso de las aplicaciones heredadas, puede utilizar el uso de mayúsculas de estilo de título si es necesario para evitar la combinación de estilos de capitalización.

### <a name="unlabeled-icon-buttons"></a>Botones de iconos sin etiqueta

-   **Use una información sobre herramientas para etiquetar el comando.** Para el texto de información sobre herramientas, use la etiqueta si el botón tuviera la etiqueta, pero incluya la tecla de método abreviado si existe.

    ![captura de pantalla de la barra de herramientas, el icono de la impresora y la información sobre herramientas ](images/cmd-toolbars-image50.png)

    Un ejemplo de una información sobre herramientas del botón de icono.

### <a name="labeled-icon-buttons"></a>Botones de iconos con etiqueta

-   **Use una etiqueta concisa.** Use una sola palabra si es posible, con un máximo de cuatro palabras.
-   **Coloque la etiqueta a la derecha del icono.**
-   **Use un recuadro informativo para describir el comando.** Dado que se etiquetan los botones, el uso de una información sobre herramientas en lugar de un recuadro informativo sería redundante.

    ![captura de pantalla de un botón con etiqueta con recuadro informativo ](images/cmd-toolbars-image51.png)

    Ejemplo de un botón de icono recuadro informativo.

### <a name="drop-down-lists"></a>Listas desplegables

-   **Si la lista siempre tiene un valor, use el valor actual como etiqueta.**

    ![captura de pantalla de la barra de herramientas con opciones de fuente ](images/cmd-toolbars-image52.png)

    En este ejemplo, el nombre de fuente seleccionado actualmente actúa como etiqueta.

-   Si una lista desplegable editable no tiene un valor, use un [símbolo del sistema](glossary.md).

    ![captura de pantalla de las libretas de direcciones de búsqueda de etiquetas de lista ](images/cmd-toolbars-image53.png)

    En este ejemplo, se usa un símbolo del sistema para la etiqueta de la lista desplegable.

### <a name="menu-buttons-and-split-buttons"></a>Botones de menú y botones de expansión

-   **Prefiere nombres de botón de menú basados en verbos.** Sin embargo, omita el verbo si es crear, mostrar, ver o administrar. Por ejemplo, los botones **herramientas** y menú **Página** no tienen verbos.
-   **Use una sola palabra específica que describa claramente y con precisión el contenido del menú.** Aunque los nombres no tienen que ser tan generales que describan todo en el menú, deben ser suficientemente predecibles para que los usuarios no se sorprendan según lo que encuentren en el menú.
-   **Aunque no es necesario, proporcione descripciones representativas si son útiles.**

### <a name="menu-items"></a>Elementos de menú

-   **Use nombres de elementos de menú que empiecen por un verbo, un nombre o una frase.**
-   **Prefiere nombres de menú basados en verbos.** Sin embargo, omita el verbo si es crear, mostrar, ver o administrar. Por ejemplo, los siguientes comandos no utilizan verbos:
    -   Acerca de
    -   Avanzado
    -   Pantalla completa
    -   Nuevo
    -   Opciones
    -   Propiedades
-   **Usar verbos específicos.** Evite los verbos genéricos no ayudantes, como cambiar y administrar.
-   **Use nombres singulares para los comandos que se aplican a un solo objeto; de** lo contrario, use Sustantivos plurales.
-   **En el caso de los pares de comandos complementarios, elija nombres claramente complementarios.** Ejemplos: agregar, quitar; Mostrar, ocultar; Insertar, eliminar.
-   **Elija los nombres de elemento de menú en función de los objetivos y las tareas del usuario, no de la tecnología.**
-   Use los siguientes nombres de elemento de menú para el propósito indicado:
    -   **Opciones:** Para mostrar las opciones del programa.
    -   **Personalizar:** Para mostrar las opciones del programa relacionadas específicamente con la configuración mecánica de la interfaz de usuario.
    -   **Personalizar:** Para mostrar un resumen de la configuración de [Personalización](glossary.md) utilizada comúnmente.
    -   **Preferencias:** No use. En su lugar, use las opciones.
    -   **Propiedades:** Para mostrar la ventana de propiedades de un objeto.
    -   **Configuración:** No use como etiqueta de menú. En su lugar, use las opciones.
-   **Los elementos de menú que muestran submenús nunca tienen puntos suspensivos en su etiqueta.** La flecha de submenú indica que se requiere otra selección.

## <a name="documentation"></a>Documentación

Al hacer referencia a las barras de herramientas:

-   Si solo hay una barra de herramientas, haga referencia a ella como la barra de herramientas.
-   Si hay varias barras de herramientas, haga referencia a ellas por su nombre, seguido de la barra de herramientas palabra. Consulte la barra de herramientas principal que está activada de forma predeterminada y contiene botones para tareas básicas, como abrir e imprimir un archivo, como la barra de herramientas estándar.
-   La barra de herramientas es una palabra única y en mayúsculas. (Por el contrario, la barra de menús es de dos palabras).
-   Haga referencia a los botones de la barra de herramientas por sus etiquetas de información sobre herramientas. Use el texto de etiqueta exacto, incluido el uso de mayúsculas, pero no incluya ningún botón de puntos suspensivos.
-   Haga referencia a los botones del menú de la barra de herramientas por sus etiquetas y el menú de Word. Use el texto de etiqueta exacto, incluido el uso de mayúsculas.
-   Haga referencia a los controles de barra de herramientas generalmente como botones de barra de herramientas.
-   Para describir la interacción del usuario, haga clic en los botones de la barra de herramientas y en las listas desplegables de solo lectura y escriba en listas desplegables que se puedan modificar. No use elegir, seleccionar o seleccionar.
-   No utilice en cascada, desplegable, desplegable o emergente para describir botones de menú, excepto en la documentación de programación.
-   Haga referencia a los elementos no disponibles como no disponible, no como atenuado, deshabilitado o atenuado. Use deshabilitado en la documentación de programación.
-   Siempre que sea posible, dé formato a las etiquetas usando texto en negrita. De lo contrario, coloque las etiquetas entre comillas solo si es necesario para evitar confusiones.

Ejemplos:

-   En el menú **Página** de la barra de herramientas, haga clic en **Enviar página por correo electrónico**.
-   En el cuadro **fuentes** de la barra de herramientas, escriba "Segoe UI".
-   En la barra de herramientas **formato** , seleccione **Mostrar** y, a continuación, haga clic en **comentarios**.

 

