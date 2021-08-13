---
title: Barras de herramientas
description: Las barras de herramientas son una manera de agrupar comandos para un acceso eficaz.
ms.assetid: 8f36307c-54fc-493d-a2ff-57db29e3508d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8015e1dec17ad524645b474b21d42af9269ffbc8d24279c56612620f0e4bb615
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450202"
---
# <a name="toolbars"></a>Barras de herramientas

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Las barras de herramientas son una manera de agrupar comandos para un acceso eficaz.

![captura de pantalla de dos barras de herramientas con elementos etiquetados ](images/cmd-toolbars-image1.png)

Algunas barras de herramientas típicas.

**Use barras de herramientas además de o en lugar de barras de menús.** Las barras de herramientas pueden ser más eficaces que las barras de menú porque son directas (siempre se muestran en lugar de mostrarse al hacer clic con el mouse), inmediatas (en lugar de requerir entrada adicional) y contienen los comandos usados con más frecuencia (en lugar de una lista completa). A diferencia de las barras de menús, las barras de herramientas no tienen que ser completas ni explicativas simplemente rápidas, cómodas y eficaces.

Algunas barras de herramientas son personalizables, lo que permite a los usuarios agregar o quitar barras de herramientas, cambiar su tamaño y ubicación e incluso cambiar su contenido. Algunos tipos de barras de herramientas se pueden desacoplar, lo que da lugar a una ventana de paleta. Para obtener más información sobre las variedades de barras de herramientas, vea [Patrones de uso](#usage-patterns) en este artículo.

> [!Note]  
> Las instrucciones relacionadas con [los menús,](cmd-menus.md) [los botones de](ctrl-command-buttons.md)comando y los [iconos](vis-icons.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirte, intenta responder a estas preguntas:

-   **¿La ventana es una ventana principal?** Las barras de herramientas funcionan bien para las ventanas principales, pero suelen ser abrumadoras para las ventanas secundarias. Para las ventanas secundarias, use [botones de comando,](ctrl-command-buttons.md) [botones de menú](ctrl-command-buttons.md)y [vínculos en su](ctrl-command-links.md) lugar.
-   **¿Hay un pequeño número de comandos usados con frecuencia?** Las barras de herramientas no pueden controlar tantos comandos como barras de menús, por lo que funcionan mejor como una manera de acceder eficazmente a un pequeño número de comandos usados con frecuencia.
-   **¿La mayoría de los comandos son inmediatos?** Es decir, ¿son principalmente comandos que no requieren entrada adicional? Para ser eficientes, las barras de herramientas deben tener una sensación directa e inmediata. Si no es así, las barras de menús son más adecuadas para los comandos que requieren entrada adicional.
-   **¿Se pueden presentar la mayoría de los comandos directamente?** Es decir, ¿los usuarios interactúan con ellos con un solo clic? Aunque algunos comandos se pueden presentar mediante botones de menú, la presentación de la mayoría de los comandos de esta manera vulnera la eficacia de la barra de herramientas, lo que hace que una barra de menús sea una mejor opción.
-   **¿Los comandos están bien representados por iconos?** Los botones de la barra de herramientas normalmente se representan mediante iconos en lugar de etiquetas de texto (aunque algunos botones de barra de herramientas usan ambos), mientras que los comandos de menú se representan mediante su texto. Si los iconos de comandos no son de alta calidad y no se explican por sí solos, una barra de menús puede ser una mejor opción.

Si el programa tiene una barra de herramientas sin barra de menús y la mayoría de los comandos son accesibles indirectamente a través de botones de menú y botones de [división,](ctrl-command-buttons.md)esta barra de herramientas es básicamente una barra de menús. En su [lugar, aplique el](cmd-menus.md) patrón de menús de la barra de herramientas en las directrices de menús.

## <a name="design-concepts"></a>Conceptos de diseño

Una buena barra de menús es un catálogo completo de todos los comandos de nivel superior disponibles, mientras que una buena barra de herramientas proporciona acceso rápido y cómodo a los comandos usados con frecuencia. Una barra de herramientas no intenta entrenar a los usuarios simplemente para que sean productivos. Una vez que los usuarios aprendan a acceder a un comando en una barra de herramientas, rara vez siguen teniendo acceso al comando desde la barra de menús. Por estos motivos, no es necesario que la barra de menús de un programa y su barra de herramientas se correspondan directamente.

### <a name="toolbars-vs-menu-bars"></a>Barras de herramientas frente a barras de menús

Tradicionalmente, las barras de herramientas son diferentes de las barras de menús de las maneras siguientes:

-   **Frecuencia.** Las barras de herramientas solo presentan los comandos usados con más frecuencia, mientras que las barras de menús cataloga todos los comandos de nivel superior disponibles dentro de un programa.
-   **Inmediatez.** Al hacer clic en un comando de barra de herramientas, se hace efecto inmediatamente, mientras que un comando de menú puede requerir una entrada adicional. Por ejemplo, un comando Imprimir de una barra de menús muestra primero el cuadro de diálogo Imprimir, mientras que un botón de la barra de herramientas Imprimir imprime inmediatamente una sola copia de un documento en la impresora predeterminada.

    ![captura de pantalla del botón de impresora de la barra de herramientas seleccionado ](images/cmd-toolbars-image2.png)

    En este ejemplo, al hacer clic en el botón imprimir de la barra de herramientas, se imprime inmediatamente una sola copia de un documento en la impresora predeterminada.

-   **Franqueza.** Los comandos de la barra de herramientas se invocan con un solo clic, mientras que los comandos de la barra de menús requieren navegar por el menú.
-   **Número y densidad.** El espacio de pantalla requerido por una barra de herramientas es proporcional al número de sus comandos y ese espacio siempre se usa, aunque los comandos no lo sean. Por lo tanto, las barras de herramientas deben usar su espacio de forma eficaz. Por el contrario, los comandos de la barra de menús normalmente se ocultan de la vista y su estructura jerárquica permite cualquier número de comandos.
-   **Tamaño y presentación.** Para empaquetar muchos comandos en un espacio pequeño, las barras de herramientas suelen usar comandos basados en iconos (con etiquetas basadas en información sobre herramientas), mientras que las barras de menús usan comandos basados en texto (con iconos opcionales). Aunque los botones de la barra de herramientas pueden tener etiquetas de texto estándar, usan mucho más espacio.

    ![captura de pantalla de la barra de herramientas con etiqueta de envío/recepción ](images/cmd-toolbars-image3.png)

    Los botones de la barra de herramientas etiquetados toman al menos tres veces más espacio que los sin etiquetar.

-   **se explica por sí solo.** Las barras de herramientas bien diseñadas necesitan iconos que se explican principalmente por sí solos, ya que los usuarios no pueden encontrar comandos de forma eficaz simplemente con información sobre herramientas. Sin embargo, las barras de herramientas siguen funcionando bien si algunos comandos usados con menos frecuencia no se explican por sí solos.

    ![captura de pantalla de la barra de herramientas con iconos conocidos ](images/cmd-toolbars-image4.png)

    En este ejemplo, los iconos usados con más frecuencia se explican por sí solos.

-   **Reconocible y distintivo.** En el caso de los comandos usados con frecuencia, los usuarios recuerden los atributos del botón de la barra de herramientas, como la ubicación, la forma y el color. Con las barras de herramientas bien diseñadas, los usuarios pueden encontrar los comandos rápidamente aunque no recuerden el símbolo de icono exacto. Por el contrario, los usuarios recuerden las ubicaciones de comandos de la barra de menús que se usan con frecuencia, pero se basan en las etiquetas de comando para realizar selecciones.

    ![captura de pantalla del cuadro de diálogo opciones de la herramienta de captura de pantalla ](images/cmd-toolbars-image5.png)

    Para los comandos de la barra de herramientas, la ubicación, la forma y el color distintivos ayudan a que los iconos se puedan reconocer y distinguir.

    ![captura de pantalla de la barra de menús con el comando de archivo seleccionado ](images/cmd-toolbars-image6.png)

    En el caso de los comandos de la barra de menús, los usuarios dependen en última instancia de sus etiquetas.

### <a name="efficiency"></a>Eficacia

Dadas sus características, las barras de herramientas deben diseñarse principalmente para mejorar la eficacia. Una barra de herramientas ineficaz no tiene sentido.

**Si solo hace una cosa...**

Asegúrese de que las barras de herramientas están diseñadas principalmente para mejorar la eficacia. Centre las barras de herramientas en los comandos que se usan con frecuencia, inmediatos, directos y que se pueden reconocer rápidamente.

### <a name="hiding-menu-bars"></a>Ocultar barras de menús

Por lo general, las barras de herramientas funcionan muy bien junto con las barras de menús: las barras de herramientas correctas proporcionan eficacia y las barras de menús correctas proporcionan integridad. **Tener barras de menús y barras de herramientas permite que cada una de ellas se centre en sus puntos fuertes sin poner en peligro.**

Sorprendentemente, este modelo se divide con programas sencillos. Para los programas con solo unos pocos comandos, tener una barra de menús y una barra de herramientas no tiene sentido porque la barra de menús termina siendo una versión redundante e ineficaz de la barra de herramientas.

Para eliminar esta redundancia, muchos programas sencillos de Windows Vista se centran en proporcionar comandos únicamente a través de la barra de herramientas y ocultar la barra de menús de forma predeterminada. Estos programas incluyen Windows Explorer, Windows Internet Explorer, Reproductor de Windows Media y Windows Galería de fotos.

No se trata de un pequeño cambio. La eliminación de la barra de menús cambia fundamentalmente la naturaleza de las barras de herramientas, ya que estas deben ser completas y cambiar de las maneras siguientes:

-   **Frecuencia.** Quitar la barra de menús significa que todos los comandos que no están disponibles directamente desde una ventana o sus menús contextuales deben ser accesibles desde la barra de herramientas, independientemente de su frecuencia de uso.
-   **Inmediatez.** Al quitar la barra de menús, la barra de herramientas es el único punto de acceso visible para los comandos, lo que requiere que la barra de herramientas tenga las versiones totalmente funcionales. Por ejemplo, si no hay ninguna barra de menús, un comando Imprimir de una barra de herramientas debe mostrar el cuadro de diálogo Imprimir en lugar de imprimir inmediatamente. (Aunque el uso de un botón de división es un riesgo excelente en este caso. Consulte [Menú estándar y botones de división](#standard-menu-and-split-buttons) para el botón Imprimir división estándar).

    ![captura de pantalla de las opciones de la barra de herramientas y del comando de impresión ](images/cmd-toolbars-image7.png)

    En este ejemplo, el botón imprimir de la barra de herramientas Windows Galería de fotos un comando Imprimir que muestra el cuadro de diálogo Imprimir.

-   **Franqueza.** Para ahorrar espacio y evitar el desorden, los comandos usados con menos frecuencia se pueden mover a los botones de menú, lo que los hace menos directos.

Las barras de herramientas que se usan para complementar una barra de menús se diseñan de forma diferente a las barras de herramientas diseñadas para su uso con una barra de menús oculta o quitada. Y como no se puede suponer que los usuarios mostrarán una barra de menús oculta para realizar un solo comando, ocultar una barra de menús debe tratarse igual que quitarla por completo al tomar decisiones de diseño. (Si oculta la barra de menús de forma predeterminada, no suponga que los usuarios piensen en mostrar la barra de menús para buscar un comando o incluso averiguar cómo mostrarla).

El diseño de una barra de herramientas para que funcione sin una barra de menús suele implicar algunos compromisos. Pero para mejorar la eficacia, no se comprometa demasiado. Si ocultar la barra de menús da como resultado una barra de herramientas ineficaz, no oculte la barra de menús.

### <a name="keyboard-accessibility"></a>Accesibilidad de teclado

Desde el teclado, el acceso a las barras de herramientas es bastante diferente del acceso a las barras de menús. Las barras de menús reciben el foco de entrada cuando los usuarios presionan la tecla Alt y pierden el foco de entrada con la tecla Esc. Una vez que una barra de menús tiene el foco de entrada, se navega independientemente del resto de la ventana, controlando todas las teclas de dirección, inicio, fin y tabulación. Por el contrario, las barras de herramientas reciben el foco de entrada cuando los usuarios presionan la tecla Tab a través de todo el contenido de la ventana. Dado que las barras de herramientas son las últimas en orden de tabulación, pueden realizar un esfuerzo importante para activarlas en una página ocupada (a menos que los usuarios sepan usar Mayús+Tab para retroceder).

La accesibilidad presenta un desafío aquí: aunque las barras de herramientas son más fáciles para los usuarios del mouse, son menos accesibles para los usuarios del teclado. Esto no es un problema si hay una barra de menús y una barra de herramientas, pero es si la barra de menús se quita u oculta.

Por motivos de accesibilidad, prefiere conservar la barra de menús en lugar de quitarla por completo en favor de una barra de herramientas. Si debe elegir entre quitar la barra de menús y ocultarla simplemente, prefiere ocultarla.

## <a name="usage-patterns"></a>Patrones de uso

Las barras de herramientas tienen varios patrones de uso:



|     Uso                                                                                                                 |     Ejemplo                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barras de herramientas principales**<br/> una barra de herramientas diseñada para funcionar sin una barra de menús, ya sea oculta o quitada. <br/> | las barras de herramientas principales deben equilibrar la necesidad de eficiencia con la integridad, por lo que funcionan mejor para programas sencillos. <br/> ![captura de pantalla de la barra de herramientas del Explorador de Windows ](images/cmd-toolbars-image8.png)<br/> Una barra de herramientas principal de Windows Explorer.<br/>                                                                        |
| **Barras de herramientas complementarias**<br/> una barra de herramientas diseñada para trabajar con una barra de menús. <br/>                         | las barras de herramientas complementarias pueden centrarse en la eficacia sin poner en peligro. <br/> ![captura de pantalla de una barra de menús en una barra de herramientas ](images/cmd-toolbars-image9.png)<br/> Una barra de herramientas complementaria de Windows Movie Maker.<br/>                                                                                                                  |
| **Menús de la barra de herramientas**<br/> una barra de menús implementada como barra de herramientas. <br/>                                        | Los menús de la barra de herramientas [](ctrl-command-buttons.md) son barras de herramientas que constan principalmente de comandos en botones de menú y botones de división, con solo algunos comandos directos, si los hay. <br/> ![captura de pantalla de la barra de menús con iconos y comandos ](images/cmd-toolbars-image10.png)<br/> Menú de la barra de herramientas Windows Galería de fotos.<br/> |
| **Barras de herramientas personalizables**<br/> una barra de herramientas que los usuarios pueden personalizar. <br/>                          | Las barras de herramientas personalizables permiten a los usuarios agregar o quitar barras de herramientas, cambiar su tamaño y ubicación e incluso cambiar su contenido. <br/> ![captura de pantalla de una barra de herramientas con docenas de iconos ](images/cmd-toolbars-image11.png)<br/> Una barra de herramientas personalizable de Microsoft Visual Studio.<br/>                                             |
| **Ventanas de paleta**<br/> cuadro de diálogo no modelo que presenta una matriz de comandos. <br/>                 | las ventanas de paleta son barras de herramientas desacopladas. <br/> ![captura de pantalla de un cuadro de diálogo de colores ](images/cmd-toolbars-image12.png)<br/> ![captura de pantalla de un cuadro de diálogo de fuentes ](images/cmd-toolbars-image13.png)<br/> Ventanas de paleta de Windows Paint.<br/>                                                                             |



 

Las barras de herramientas tienen estos estilos:



|   Estilo                                                                                                                                     | Ejemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iconos sin etiquetar**<br/> una o varias filas de pequeños botones de icono sin etiquetar. <br/>                                           | use este estilo si hay demasiados botones para etiquetar o si el programa se usa con frecuencia. con este estilo, los programas con funcionalidad compleja pueden tener varias filas y, por lo tanto, este es el único estilo que debe personalizarse. con este estilo, algunos botones de comando se pueden etiquetar si se usan con frecuencia. <br/> ![captura de pantalla de la barra de herramientas con iconos pequeños sin etiquetar ](images/cmd-toolbars-image14.png)<br/> Barra de herramientas de iconos sin etiquetar de WordPad.<br/> |
| **Iconos grandes sin etiquetar**<br/> una sola fila de botones de iconos grandes sin etiquetar. <br/>                                         | use este estilo para utilidades sencillas que tienen iconos fácilmente reconocibles y que normalmente se ejecutan en ventanas pequeñas. <br/> ![captura de pantalla de la barra de herramientas con iconos grandes sin etiquetar ](images/cmd-toolbars-image15.png)<br/> ![captura de pantalla de la barra de herramientas con iconos grandes ](images/cmd-toolbars-image16.png)<br/> Barras de herramientas de iconos grandes sin etiquetar de Windows Live Messenger y el Windows Herramienta Recortes.<br/>                                                                       |
| **Iconos etiquetados**<br/> una sola fila de iconos pequeños etiquetados. <br/>                                                          | use este estilo si hay pocos comandos o el programa no se usa con frecuencia. este estilo siempre tiene una sola fila. <br/> ![captura de pantalla de la barra de herramientas con iconos etiquetados ](images/cmd-toolbars-image8.png)<br/> Una barra de herramientas de iconos etiquetados Windows Explorer.<br/>                                                                                                                                                                                                               |
| **Barras de herramientas parciales**<br/> una fila parcial de iconos pequeños que se usa para ahorrar espacio cuando no es necesaria una barra de herramientas completa. <br/>       | use este estilo para ventanas con botones de navegación, un cuadro de búsqueda o pestañas para eliminar el peso innecesario en la parte superior de la ventana. <br/> ![captura de pantalla de la barra de menús, la barra de herramientas y la barra de favoritos ](images/cmd-toolbars-image17.png)<br/> Las barras de herramientas parciales se pueden combinar con botones de navegación, un cuadro de búsqueda o pestañas.<br/>                                                                                                                                                  |
| **Barras de herramientas parciales grandes**<br/> una fila parcial de iconos grandes que se usa para ahorrar espacio cuando no es necesaria una barra de herramientas completa. <br/> | use este estilo para utilidades sencillas que tienen botones de navegación o un cuadro de búsqueda para eliminar el peso innecesario en la parte superior de la ventana. <br/> ![captura de pantalla de una barra de herramientas parcial grande ](images/cmd-toolbars-image18.png)<br/> Una barra de herramientas parcial grande de Windows Defender.<br/>                                                                                                                                                                                         |



 

Por último, los controles de la barra de herramientas tienen varios patrones de uso:



|     Uso                                                                                                                 |     Ejemplo                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Botones de icono de comando**<br/> Al hacer clic en un botón de comando se inicia una acción inmediata. <br/>                                                                                                 | ![captura de pantalla de una barra de herramientas con iconos etiquetados ](images/cmd-toolbars-image19.png)<br/> Ejemplos de botones de comandos de icono Windows fax y examen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Botones de icono de modo**<br/> Al hacer clic en un botón de modo, se entra en el modo seleccionado. <br/>                                                                                                            | ![captura de pantalla de una barra de herramientas vertical ](images/cmd-toolbars-image20.png)<br/> Ejemplos de botones de modo Windows Paint.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Botones de icono de propiedad**<br/> El estado de un botón de propiedad refleja el estado de los objetos seleccionados actualmente, si los hay. Al hacer clic en el botón, se aplica el cambio a los objetos seleccionados. <br/> | ![captura de pantalla de iconos de formato y texto seleccionado ](images/cmd-toolbars-image21.png)<br/> Ejemplos de botones de propiedad Microsoft Word.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Botones de iconos con etiqueta**<br/> un botón de comando o un botón de propiedad etiquetados con un icono y una etiqueta de texto. <br/>                                                                               | Estos botones se usan para los botones de la barra de herramientas usados con frecuencia cuyo icono no es lo suficientemente explicativo. también se usan en barras de herramientas que tienen tan pocos botones que cada botón puede tener una etiqueta de texto. <br/> ![Captura de pantalla que muestra la barra de herramientas con iconos etiquetados para los botones usados con más frecuencia. ](images/cmd-toolbars-image22.png)<br/> Una barra de herramientas con sus botones usados con más frecuencia etiquetados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Botones de menú**<br/> un botón de comando que se usa para presentar un pequeño conjunto de comandos relacionados. <br/>                                                                                                | Un único triángulo que apunta hacia abajo indica que al hacer clic en el botón se muestra un menú. <br/> ![captura de pantalla de la barra de herramientas y lista desplegable de comandos ](images/cmd-toolbars-image23.png)<br/> Botón de menú con un pequeño conjunto de comandos relacionados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Botones de división**<br/> un botón de comando que se usa para consolidar las variaciones de un comando, especialmente cuando uno de los comandos se usa la mayoría de las veces. <br/>                                     | ![captura de pantalla del botón de impresión dividida ](images/cmd-toolbars-image24.png)<br/> un botón de división en su estado normal.<br/> Al igual que un botón de menú, un único triángulo que apunta hacia abajo indica que al hacer clic en la parte más derecha del botón se muestra un menú. <br/> ![captura de pantalla de los comandos del botón de impresión dividida ](images/cmd-toolbars-image25.png)<br/> un botón de división desplegable.<br/> En este ejemplo, se usa un botón de división para consolidar todos los comandos relacionados con la impresión. El comando de impresión inmediata se usa la mayoría de las veces, por lo que los usuarios normalmente no necesitan ver los otros comandos. <br/> A diferencia de un botón de menú, al hacer clic en la parte izquierda del botón se realiza la acción directamente en la etiqueta. Los botones de división son efectivos en situaciones en las que es probable que el comando siguiente sea el mismo que el último comando. En este caso, la etiqueta se cambia al último comando, como con un selector de colores:<br/> ![captura de pantalla del icono de cubo que vierte pintura ](images/cmd-toolbars-image26.png)<br/> En este ejemplo, la etiqueta se cambia al último comando.<br/> |
| **Listas desplegables**<br/> una lista desplegable (editable o de solo lectura) que se usa para ver o cambiar una propiedad. <br/>                                                                                   | ![captura de pantalla de la lista desplegable de fuentes ](images/cmd-toolbars-image27.png)<br/> En este ejemplo, se usan listas desplegables para ver y establecer atributos de fuente.<br/> Una lista desplegable de una barra de herramientas refleja el estado del objeto seleccionado actualmente, si existe. Al cambiar la lista, se cambia el estado del objeto seleccionado. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="guidelines"></a>Directrices

### <a name="presentation"></a>Presentación

-   **Elija un estilo de barra de herramientas adecuado en función del número de comandos y su uso.** Consulte la tabla de estilo de barra de herramientas anterior para obtener instrucciones sobre cómo elegir. Evite usar una configuración de barra de herramientas que tome demasiado espacio del área de trabajo del programa.
-   **Coloque las barras de herramientas justo encima del área de contenido, debajo** de la barra de menús y la barra de direcciones, si está presente.
-   **Si el espacio está en un nivel Premium, ahorre espacio al:**

    -   Omitir las etiquetas de iconos conocidos y comandos usados con menos frecuencia.
    -   Usar solo una barra de herramientas parcial en lugar del ancho completo de la ventana.
    -   Consolidar comandos relacionados con un botón de menú o un botón de división.
    -   Usar un [botón de contenido adicional de desbordamiento](glossary.md) para mostrar comandos usados con menos frecuencia.
    -   Mostrar comandos solo cuando se aplican al contexto actual.

    ![captura de pantalla de los iconos comunes de la barra de herramientas no etiquetados ](images/cmd-toolbars-image28.png)

    La Windows Internet Explorer de herramientas de almacenamiento ahorra espacio omitiendo las etiquetas de iconos conocidos, usando una barra de herramientas parcial y usando un botón de contenido adicional de desbordamiento para los comandos usados con menos frecuencia.

-   **Para el patrón de barra de herramientas de iconos sin etiquetar, use una configuración predeterminada con no más de dos filas de barras de herramientas.** Si más de dos filas pueden ser útiles, haga que las barras de herramientas sean personalizables. A partir de más de dos filas, puede sobrecargar a los usuarios y tomar demasiado espacio del área de trabajo del programa.

    **Incorrecto:**

    ![captura de pantalla de la barra de menús y tres filas de barras de herramientas ](images/cmd-toolbars-image29.png)

    Una configuración predeterminada con más de dos filas de barras de herramientas produce demasiado desorden visual.

-   **Deshabilite los botones individuales de la barra** de herramientas que no se aplican al contexto actual, en lugar de quitarlos. Esto hace que el contenido de la barra de herramientas sea estable y fácil de encontrar.
-   **Deshabilite los botones individuales de la barra de herramientas si al hacer clic en ellos se produciría directamente un error.** Esto es necesario para mantener una sensación directa.
-   **Para el patrón de barra de herramientas de iconos sin etiquetar, quite las barras de herramientas enteras si no se aplican al contexto actual.** Mostrarlos solo en los modos aplicables.

    ![captura de pantalla de la barra de herramientas de depuración ](images/cmd-toolbars-image30.png)

    En este ejemplo, la barra de herramientas Depurar solo se muestra cuando se ejecuta el programa.

-   **Mostrar botones de la barra de herramientas alineados a la izquierda.** El icono ayuda, si está presente, está alineado a la derecha.

    ![captura de pantalla de la barra de herramientas, icono de ayuda alineado a la derecha ](images/cmd-toolbars-image31.png)

    Todos los botones de la barra de herramientas se alinean a la izquierda, excepto ayuda.

    **Excepción:** Windows barras de herramientas de estilo 7 a la izquierda alinean comandos específicos del programa, pero alinean a la derecha comandos estándar y conocidos, como Opciones, Vista y Ayuda.

-   **No cambie dinámicamente las etiquetas de los botones de la barra de herramientas.** Hacerlo es confuso e inesperado. Sin embargo, puede cambiar el icono para reflejar el estado actual.

    ![captura de pantalla del icono de cubo que vierte pintura ](images/cmd-toolbars-image26.png)

    En este ejemplo, el icono se cambia para indicar el comando predeterminado.

### <a name="controls-and-commands"></a>Controles y comandos

-   **Prefiere los comandos usados con más frecuencia.**
    -   **Para las barras de herramientas principales, proporcione comandos completos.** Las barras de herramientas principales no tienen que ser tan completas como las barras de menús, pero tienen que proporcionar todos los comandos que no se pueden detectar fácilmente en otra parte. Las barras de herramientas principales no necesitan tener comandos para:
        -   Comandos que están directamente en la propia interfaz de usuario.
        -   Normalmente se accede a los comandos a través de menús contextuales.
        -   Comandos estándar y conocidos, como Cortar, Copiar y Pegar.
    -   **En el caso de las barras de herramientas complementarias, proporcione los comandos que se usan con más frecuencia.** Los comandos de la barra de menús son un superconjunto de los comandos de la barra de herramientas, por lo que no tiene que proporcionar todo. Céntrate en el acceso rápido y cómodo a los comandos y omite el resto.
-   **Prefiere controles directos.** Use los botones de la barra de herramientas en el orden de preferencia siguiente:
    -   **Botón icono.** Directo y ocupa un espacio mínimo.
    -   **Botón icono etiquetado.** Directo, pero ocupa más espacio.
    -   **Botón Dividir.** Directo para el comando más común, pero controla las variaciones de comandos.
    -   **Botón de menú.** Indirecto, pero presenta muchos comandos.
-   **Prefiere comandos inmediatos.** Para los comandos que pueden ser inmediatos o tener entradas adicionales para la flexibilidad:
    -   Para las barras de herramientas principales, use las versiones flexibles de los comandos (por ejemplo, Imprimir...).
    -   Para las barras de herramientas complementarias, use las versiones inmediatas de la barra de herramientas (por ejemplo, Imprimir) y use versiones flexibles en la barra de menús (como Imprimir...).
-   **Proporcione etiquetas para los comandos usados con frecuencia, especialmente** si sus iconos no son iconos conocidos.

    **Aceptable:**

    ![captura de pantalla de la barra de herramientas sin iconos etiquetados ](images/cmd-toolbars-image32.png)

    **Mejor:**

    ![captura de pantalla de la barra de herramientas con algunos iconos etiquetados ](images/cmd-toolbars-image33.png)

    La Windows de herramientas Fax y Examen tiene pocos comandos, por lo que la mejor versión etiqueta las más importantes.

-   No coloque comandos en los menús de la barra de herramientas que también estén directamente en la barra de herramientas.

    **Incorrecto:**

    ![captura de pantalla del comando de impresión en la barra de herramientas y el menú ](images/cmd-toolbars-image34.png)

    En este ejemplo, Imprimir está directamente en la barra de herramientas, por lo que no es necesario que esté en el menú.

### <a name="organization-and-order"></a>Organización y pedido

-   **Organice los comandos dentro de una barra de herramientas en grupos relacionados.**
-   **Coloque primero los grupos usados con más frecuencia. Dentro de un grupo, coloque los comandos en su orden lógico.** En general, los comandos deben tener un flujo lógico para que sea fácil de encontrar, a la vez que los comandos usados con más frecuencia aparecen primero. Hacerlo es más eficaz, especialmente si hay desbordamiento.
-   **Use divisores de grupo solo si los comandos entre grupos están débilmente acoplados.** Si lo hace, las agrupaciones son obvias y los comandos son más fáciles de encontrar.

    ![Captura de pantalla que muestra una barra de herramientas con iconos bien organizados mediante divisores de grupo.](images/cmd-toolbars-image35.png)

    ![captura de pantalla de la barra de herramientas con iconos bien organizados ](images/cmd-toolbars-image36.png)

    Ejemplos de barras de herramientas agrupadas de Windows Mail.

-   **Evite colocar comandos destructivos junto a los comandos usados con frecuencia.** Use el orden o la agrupación para obtener la separación. Además, considere la posibilidad de no colocar comandos destructivos en la barra de herramientas, sino solo en la barra de menús o los menús contextuales en su lugar.

    **Aceptable:**

    ![captura de pantalla de los botones de impresión y eliminación adyacentes ](images/cmd-toolbars-image37.png)

    **Mejor:**

    ![captura de pantalla de botones de impresión y eliminación separados ](images/cmd-toolbars-image38.png)

    En el mejor ejemplo, el comando Delete está físicamente separado de Print.

-   **Use el botón de contenido adicional de desbordamiento para indicar que no se pueden mostrar todos los comandos.** Pero use el desbordamiento solo si no hay espacio suficiente para mostrar todos los comandos.

    **Incorrecto:**

    ![captura de pantalla de la barra de favoritos y comandos ocultos ](images/cmd-toolbars-image39.png)

    El botón de contenido adicional de desbordamiento indica que no se muestran todos los comandos, pero podría haber más con un mejor diseño.

-   **Asegúrese de que los comandos usados con más frecuencia son accesibles directamente desde la barra de herramientas (es decir, sin desbordamiento) en tamaños de ventana pequeños.** Si es necesario, reordene los comandos, mueva los comandos usados con menos frecuencia a los botones de menú o a los botones de división, o incluso quítelos completamente de la barra de herramientas. Si esto sigue siendo un problema, replantee su elección de estilo de barra de herramientas.

### <a name="hiding-menu-bars"></a>Ocultar barras de menús

Por lo general, las barras de herramientas funcionan muy bien junto con las barras de menús, ya que tener ambas permite que cada una de ellas se centre en sus puntos fuertes sin poner en peligro.

-   Oculte la barra de menús de forma predeterminada si el diseño de la barra de herramientas hace que tenga una barra de menús redundante.
-   Oculte la barra de menús en lugar de quitarla por completo, ya que las barras de menús son más accesibles para los usuarios del teclado.
-   Para restaurar la barra de menús, proporcione una opción de marca de verificación Barra de menús en la categoría de menú Ver (para barras de herramientas principales) o Herramientas (para barras de herramientas secundarias). Para obtener más información, vea [Menú estándar y botones de división](#standard-menu-and-split-buttons).
-   Muestre la barra de menús cuando los usuarios presionen la tecla Alt y establezca el foco de entrada en la primera categoría de menú.

### <a name="interaction"></a>Interacción

-   Al mantener el puntero, muestre la [asequibilidad del](glossary.md) botón para indicar que se puede hacer clic en el icono. Después de que se agote el tiempo de espera de la información sobre herramientas, muestre la información sobre herramientas o la información.

    ![captura de pantalla de una información sobre información que describe un botón ](images/cmd-toolbars-image40.png)

    En este ejemplo se muestran los distintos estados de presentación.

-   A la izquierda, haga clic en:
    -   Para los botones de comando, interactúe con el control de la forma habitual.
    -   Para los botones de modo, muestre el control para reflejar el modo seleccionado actualmente. Si el modo afecta al comportamiento de la interacción del mouse, cambie también el puntero.

        ![captura de pantalla de puntero con forma de cubo de pintura ](images/cmd-toolbars-image41.png)

        En este ejemplo, el puntero se cambia para mostrar el modo de interacción del mouse.

    -   En el caso de los botones de propiedad y las listas desplegables, muestre el control para reflejar el estado de los objetos seleccionados actualmente, si los hay. En la interacción, actualice el estado del control y aplique el cambio a los objetos seleccionados. Si no se selecciona nada, no haga nada.

-   En el doble clic izquierdo, realice la misma acción que un solo clic izquierdo.
    -   **Excepción:** En raras ocasiones, un comando de barra de herramientas se puede usar de forma más eficaz de forma modal. En tales casos, use el doble clic para alternar el modo.

        ![captura de pantalla de información que muestra las funciones del botón ](images/cmd-toolbars-image42.png)

        En este ejemplo, al hacer doble clic en el comando Dar formato al escritor, entra en un modo en el que todos los clics posteriores aplican el formato. Los usuarios pueden salir del modo haciendo clic con un solo clic a la izquierda.

-   Al hacer clic con el botón derecho:
    -   En el caso de las barras de herramientas personalizables, muestre el menú contextual para personalizar la barra de herramientas. Muestre el menú al hacer clic con el botón derecho en el mouse hacia abajo, no hacia arriba.
    -   Para otras barras de herramientas, no haga nada.

### <a name="icons"></a>Iconos

-   **Proporcione iconos para todos los controles de la barra de herramientas, excepto las listas desplegables.**

    ![captura de pantalla de la lista desplegable tamaño de fuente ](images/cmd-toolbars-image43.png)

    Las listas desplegables no necesitan iconos, pero sí todos los demás controles de la barra de herramientas.

    **Excepción:** Windows barras de herramientas de estilo 7 usan iconos solo para los comandos cuyos iconos son conocidos; De lo contrario, usan etiquetas de texto sin iconos. Esto mejora la claridad de las etiquetas, pero requiere más espacio.

-   **Asegúrese de que los iconos de la barra de herramientas estén claramente visibles en el color de fondo de la barra de herramientas.** Evalúe siempre los iconos de la barra de herramientas en contexto y en modo de contraste alto.
-   **Elija diseños de icono que comuniquen claramente su propósito, especialmente para los comandos usados con más frecuencia.** Las barras de herramientas bien diseñadas necesitan iconos que se explican por sí solos porque los usuarios no pueden encontrar comandos de forma eficaz con su información sobre herramientas. Sin embargo, las barras de herramientas siguen funcionando bien si los iconos de algunos comandos usados con menos frecuencia no se explican por sí solos.
-   **Elija iconos que sean reconocibles y distintivos, especialmente para los comandos usados con más frecuencia.** Asegúrese de que los iconos tienen formas y colores distintivos. Esto ayuda a los usuarios a encontrar los comandos rápidamente aunque no recuerden el símbolo de icono.
-   **Asegúrese de que los iconos de la barra de herramientas se ajustan a las directrices de los iconos de estilo aerórmico.**

Para obtener más información y ejemplos, vea [Iconos](vis-icons.md).

### <a name="standard-menu-and-split-buttons"></a>Menú estándar y botones de división

Si usa botones de menú y botones de división en una barra de herramientas, intente usar las siguientes estructuras de menú estándar y sus comandos pertinentes siempre que sea posible. A diferencia de las barras de menús, los comandos de la barra de herramientas no toman claves de acceso.

**Barras de herramientas principales**

Estos comandos reflejan los comandos que se encuentran en las barras de menú estándar, por lo que solo se deben usar para las barras de herramientas principales. Esta lista muestra las etiquetas de botón (y el tipo) con su orden y separadores, teclas de método abreviado y puntos suspensivos. **Tenga en cuenta que el comando para mostrar y ocultar la barra de menús está en el menú Ver.**

<dl> Archivo <dl> NewCtrl+N  
Abierto... Ctrl+O  
Cerrar <separator>  
GuardarCtrl+S  
Guardar como... <separator>  
Enviar a <separator>  
Impresión... Ctrl+P  
Vista previa de impresión  
Configuración de página <separator>  
ExitAlt+F4 (acceso directo normalmente no dado)
</dl> </dd> Edit(menu button) <dl> DeshacerCtrl+Z  
RedoCtrl+Y <separator>  
CutCtrl+X  
CopyCtrl+C  
PasteCtrl+V <separator>  
Seleccionar todoCtrl+A <separator>  
DeleteDel(acceso directo normalmente no dado)  
Renombrar... <separator>  
Encontrar... Ctrl+F  
Buscar nextF3(comando normalmente no dado)  
Reemplazar... Ctrl+H  
Vete a... Ctrl+G
</dl> </dd> <dd>Imprimir (botón de división) <dl> Impresión... Ctrl+P  
Vista previa de impresión <separator>  
Configurar página
</dl> </dd> Ver (botón de menú) <dl> Barra de menús (compruebe si está visible)  
Panel de detalles (compruebe si está visible)  
Panel vista previa (compruebe si está visible)  
Barra de estado (compruebe si está visible) <separator>  
Zoom  
Zoom enCtrl++  
AlejarCtrl+- <separator>  
Tamaño del texto (la configuración seleccionada tiene viñeta) <dl> Mayor  
Mayor  
Media  
Más pequeño  
Menor
</dl> </dd> <separator> Pantalla completaF11  
RefreshF5
</dl> </dd> Tools(menu button) <dl> ... <separator>  
Opciones
</dl>> </dd> Help(split button, use the Help icon) <dl> <program name> helpF1 <separator>  
acerca de <program name>  
</dl> </dd> </dl>

**Barras de herramientas complementarias**

Estos comandos complementan las barras de menú estándar. Esta lista muestra las etiquetas de botón (y el tipo) con sus separadores y orden, teclas de método abreviado y puntos suspensivos. **Tenga en cuenta que el comando para mostrar y ocultar la barra de menús está en el menú Herramientas.**

Los nombres de categoría de la barra de herramientas complementarios difieren de los nombres de categoría de menú estándar porque deben ser más abarcados. Por ejemplo, se usa la categoría Organizar en lugar de Editar porque contiene comandos que no están relacionados con la edición. **Para mantener la coherencia entre las barras de menús y las barras de herramientas, use los nombres de categoría de menú estándar si no sería engañoso.**

**Incorrecto:**

![captura de pantalla de las mismas opciones para distintos comandos ](images/cmd-toolbars-image44.png)

En este ejemplo, la barra de herramientas debe usar Editar en lugar de Organizar por coherencia porque tiene los comandos de menú Editar estándar.

### <a name="palette-windows"></a>Ventanas de paleta

-   **Las ventanas de paleta usan barras de título más cortas para minimizar su espacio de pantalla.** Coloque un botón Cerrar en la barra de título.
-   **Establezca el texto de la barra de título en el comando que muestra la ventana de la paleta.**
-   **Use mayúsculas de estilo oración sin terminar de puntuar.**
-   **Proporcione un menú contextual para los comandos de administración de ventanas.** Muestra este menú contextual cuando los usuarios hacen clic con el botón derecho en la barra de título.

    ![captura de pantalla del cuadro de herramientas con el menú contextual ](images/cmd-toolbars-image45.png)

    En este ejemplo, los usuarios pueden hacer clic con el botón derecho en la barra de título para mostrar el menú contextual.

-   **Cuando sea posible y útil, haga que las ventanas de paleta se puedan redimensionar.** Indique que la ventana se puede cambiar de tamaño mediante punteros de cambio de tamaño cuando se encuentra sobre el marco de ventana.
-   **Cuando se vuelve a mostrar una ventana de paleta, se muestra con el mismo estado al que se ha accedido por última vez.** Al cerrar, guarde el tamaño y la ubicación de la ventana. Al volver a mostrar, restaure el tamaño y la ubicación de la ventana guardados. Además, considere la posibilidad de hacer que estos atributos se persistenten en todas las instancias del programa por usuario.

### <a name="customization"></a>Personalización

-   **Proporcionar personalización para las barras de herramientas que constan de dos o más filas.** Solo el estilo de iconos sin etiquetar necesita personalización. Las barras de herramientas simples con pocos comandos no necesitan personalización.
-   **Proporcione una buena configuración predeterminada.** Los usuarios no deben tener que personalizar sus barras de herramientas para escenarios comunes. No dependa de que los usuarios personalizen su forma de salir de una configuración inicial no correcta. Suponga que la mayoría de los usuarios no personalizarán sus barras de herramientas.
-   **Proporcione un menú contextual con los siguientes comandos:**
    -   Lista de casillas para mostrar las barras de herramientas disponibles
    -   Barras de herramientas de bloqueo y desbloqueo
    -   Personalizar...
-   **Bloquee las barras de herramientas personalizables de forma** predeterminada para evitar cambios accidentales.
-   **Para el comando Personalizar, muestre un cuadro** de diálogo de opciones que proporciona la capacidad de elegir qué barras de herramientas se muestran y los comandos de cada barra de herramientas.

    ![captura de pantalla del cuadro de diálogo personalizar y las opciones ](images/cmd-toolbars-image46.png)

    En este ejemplo, Visual Studio un cuadro de diálogo de opciones para personalizar sus barras de herramientas.

-   Proporcione un comando Restablecer para volver a la configuración de la barra de herramientas original en el cuadro de diálogo Personalizar opciones.
-   **Proporcione la capacidad de personalizar las barras de herramientas mediante arrastrar y colocar de las maneras siguientes:**

    -   Establezca el orden y las posiciones de la barra de herramientas.
    -   Establezca las longitudes de la barra de herramientas, mostrando las barras de herramientas que sean demasiado pequeñas para mostrar su contenido con un botón de contenido adicional de desbordamiento.
    -   Si se admite, desacopla las barras de herramientas para que se conviertan en ventanas de paleta y viceversa.

    Cuando se muestra el cuadro de diálogo Personalizar opciones:

    -   Establezca el contenido de la barra de herramientas.
    -   Establezca el orden del contenido de la barra de herramientas.

    Esto permite a los usuarios realizar cambios de forma más directa y eficaz.

-   **Guarde todas las personalizaciones de la barra de herramientas** por usuario.

### <a name="using-ellipses"></a>Uso de puntos suspensivos

Aunque los comandos de la barra de herramientas se usan para acciones inmediatas, a veces se necesita más información para realizar la acción. Use puntos suspensivos para indicar que un comando requiere más información antes de que pueda tener efecto. Coloque los puntos suspensivos al final de la información sobre herramientas y la etiqueta, si hay alguno.

![captura de pantalla de texto de información sobre herramientas de impresión con puntos suspensivos ](images/cmd-toolbars-image47.png)

En este ejemplo, imprimir... El comando muestra un cuadro de diálogo Imprimir para recopilar más información.

Sin embargo, si un comando no puede tener efecto inmediatamente, no se requieren puntos suspensivos. Por lo tanto, por ejemplo, la configuración de uso compartido no tiene puntos suspensivos aunque necesite información adicional, ya que el comando no puede tener efecto inmediatamente.

![captura de pantalla de la barra de herramientas, el comando y la información sobre herramientas ](images/cmd-toolbars-image48.png)

El comando Configuración compartido no tiene puntos suspensivos porque no puede tener efecto inmediatamente.

Dado que las barras de herramientas se muestran constantemente y el espacio es premium, los puntos suspensivos se deben usar con **poca frecuencia.**

> [!Note]  
> Para los menús mostrados por una barra de herramientas, aplique las [directrices de puntos suspensivos del menú.](cmd-menus.md)

 

## <a name="recommended-sizing-and-spacing"></a>Tamaño y espaciado recomendados

![captura de pantalla de las barras de herramientas con información de espaciado ](images/cmd-toolbars-image49.png)

Tamaño y espaciado recomendados para las barras de herramientas estándar.

## <a name="labels"></a>Etiquetas

### <a name="general"></a>General

-   **Use mayúsculas de estilo de frase.**
    -   **Excepción:** En el caso de las aplicaciones heredadas, puede usar mayúsculas de estilo de título si es necesario para evitar mezclar estilos de mayúsculas.

### <a name="unlabeled-icon-buttons"></a>Botones de icono sin etiquetar

-   **Use una información sobre herramientas para etiquetar el comando.** Para el texto de información sobre herramientas, use cuál sería la etiqueta si se etiquetase el botón, pero incluya la tecla de método abreviado si la hay.

    ![captura de pantalla de la barra de herramientas, el icono de impresora y la información sobre herramientas ](images/cmd-toolbars-image50.png)

    Ejemplo de información sobre herramientas de un botón de icono.

### <a name="labeled-icon-buttons"></a>Botones de iconos con etiqueta

-   **Use una etiqueta concisa.** Use una sola palabra si es posible, cuatro palabras como máximo.
-   **Coloque la etiqueta a la derecha del icono.**
-   **Use una información para describir el comando.** Dado que los botones están etiquetados, el uso de una información sobre herramientas en lugar de una información sobre herramientas sería redundante.

    ![captura de pantalla del botón etiquetado con información ](images/cmd-toolbars-image51.png)

    Ejemplo de información sobre los botones de icono etiquetados.

### <a name="drop-down-lists"></a>Listas desplegables

-   **Si la lista siempre tiene un valor, use el valor actual como etiqueta.**

    ![captura de pantalla de la barra de herramientas con opciones de fuente ](images/cmd-toolbars-image52.png)

    En este ejemplo, el nombre de fuente seleccionado actualmente actúa como etiqueta.

-   Si una lista desplegable editable no tiene un valor, use un [símbolo del sistema](glossary.md).

    ![captura de pantalla de las libretas de direcciones de búsqueda de etiquetas de lista ](images/cmd-toolbars-image53.png)

    En este ejemplo, se usa un símbolo del sistema para la etiqueta de la lista desplegable.

### <a name="menu-buttons-and-split-buttons"></a>Botones de menú y botones de división

-   **Prefiere nombres de botón de menú basados en verbos.** Sin embargo, omita el verbo si es Crear, Mostrar, Ver o Administrar. Por ejemplo, **los botones** **de** menú Herramientas y Página no tienen verbos.
-   **Use una sola palabra específica que describa clara y precisamente el contenido del menú.** Aunque los nombres no tienen que ser tan generales que describan todo en el menú, deben ser lo suficientemente predecibles para que los usuarios no se sorprendan por lo que encuentran en el menú.
-   **Aunque no es necesario, proporcione descripciones de información si son útiles.**

### <a name="menu-items"></a>Elementos de menú

-   **Use nombres de elementos de menú que empiecen por un verbo, un sustantivo o una frase de sustantivo.**
-   **Prefiere nombres de menú basados en verbos.** Sin embargo, omita el verbo si es Crear, Mostrar, Ver o Administrar. Por ejemplo, los comandos siguientes no usan verbos:
    -   Acerca de
    -   Avanzado
    -   Pantalla completa
    -   New
    -   Opciones
    -   Propiedades
-   **Use verbos específicos.** Evite verbos genéricos y poco útiles, como Cambiar y administrar.
-   **Use nombres singulares para los comandos que se aplican a un único objeto;** de lo contrario, use nombres plurales.
-   **Para los pares de comandos complementarios, elija nombres claramente complementarios.** Ejemplos: Agregar, Quitar; Mostrar, Ocultar; Insertar, Eliminar.
-   **Elija los nombres de los elementos de menú en función de los objetivos y las tareas del usuario, no de la tecnología.**
-   Use los siguientes nombres de elemento de menú para el propósito indicado:
    -   **Opciones:** Para mostrar las opciones del programa.
    -   **Personalizar:** Para mostrar las opciones del programa relacionadas específicamente con la configuración mecánica de la interfaz de usuario.
    -   **Personalizar:** Para mostrar un resumen de la configuración de [personalización que se usa con](glossary.md) frecuencia.
    -   **Preferencias:** No lo use. En su lugar, use Opciones.
    -   **Propiedades:** Para mostrar la ventana de propiedades de un objeto.
    -   **Configuración:** No use como etiqueta de menú. En su lugar, use Opciones.
-   **Los elementos de menú que muestran submenús nunca tienen puntos suspensivos en su etiqueta.** La flecha del submenú indica que se requiere otra selección.

## <a name="documentation"></a>Documentación

Al hacer referencia a las barras de herramientas:

-   Si solo hay una barra de herramientas, haga referencia a ella como la barra de herramientas.
-   Si hay varias barras de herramientas, haga referencia a ellas por nombre, seguida de la palabra barra de herramientas. Consulte la barra de herramientas principal que está encendido de forma predeterminada y contiene botones para tareas básicas, como abrir e imprimir un archivo, como la barra de herramientas estándar.
-   La barra de herramientas es una sola palabra sin mayúsculas. (Por el contrario, la barra de menús es dos palabras).
-   Consulte los botones de la barra de herramientas por sus etiquetas de información sobre herramientas. Use el texto exacto de la etiqueta, incluida su mayúscula, pero no incluya puntos suspensivos.
-   Consulte los botones de menú de la barra de herramientas por sus etiquetas y el menú de palabras. Use el texto exacto de la etiqueta, incluida su mayúscula.
-   Consulte los controles de barra de herramientas generalmente como botones de barra de herramientas.
-   Para describir la interacción del usuario, use haga clic para los botones de la barra de herramientas y las listas desplegables de solo lectura y escriba para listas desplegables editables. No use choose, select ni pick.
-   No use botones de menú en cascada, desplegables, desplegables o emergentes para describir los botones de menú, excepto en la documentación de programación.
-   Consulte elementos no disponibles como no disponibles, no como atenuados, deshabilitados o atenuados. Use deshabilitado en la documentación de programación.
-   Cuando sea posible, formatee las etiquetas con texto en negrita. De lo contrario, coloque las etiquetas entre comillas solo si es necesario para evitar confusiones.

Ejemplos:

-   En el menú **Página de** la barra de herramientas, haga clic en Enviar página por **correo electrónico.**
-   En el **cuadro Fuentes** de la barra de herramientas, escriba "Segoe UI".
-   En la **barra de herramientas Formato,** seleccione **Mostrar** y, a continuación, haga clic en **Comentarios.**

 

