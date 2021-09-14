---
title: Acerca de los controles de barra de herramientas
description: Una barra de herramientas es un control que contiene uno o varios botones.
ms.assetid: b5a00a81-8d23-4844-8b0a-776e7cceced8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f615da972f14bb88c4915504c089dd6b40d9aca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166014"
---
# <a name="about-toolbar-controls"></a>Acerca de los controles de barra de herramientas

Una barra de herramientas es un control que contiene uno o varios botones. Cada botón, cuando un usuario hace clic en él, envía un mensaje de comando a la ventana primaria. Normalmente, los botones de una barra de herramientas corresponden a los elementos del menú de la aplicación, lo que proporciona una manera más directa y adicional para que el usuario acceda a los comandos de una aplicación.

En la siguiente captura de pantalla se muestra una ventana que contiene una barra de herramientas sencilla para las operaciones de archivo. La aplicación tiene habilitados los estilos visuales. El botón Guardar está "en caliente" porque el cursor estaba sobre él cuando se tomó la captura de pantalla. La apariencia real del control varía según el sistema operativo y el tema seleccionado por el usuario.

![captura de pantalla de una ventana con una barra de herramientas de tres botones; un botón está encendido](images/tb-withstyles.png)

En la siguiente captura de pantalla se muestra el mismo control en una aplicación compilada sin estilos visuales habilitados.

![captura de pantalla de una ventana sin estilos visuales: ninguno de los botones parece activa](images/tb-wostyles.png)

En los temas siguientes se tratan las características que se deben tener en cuenta al planear una barra de herramientas. Para obtener información específica sobre la implementación y el código de ejemplo, vea [Usar controles de barra de herramientas](using-toolbar-controls.md).

-   [Especificar el tamaño y la posición de la barra de herramientas](#specifying-toolbar-size-and-position)
-   [Barras de herramientas transparentes](#transparent-toolbars)
-   [Barras de herramientas de estilo de lista](#list-style-toolbars)
-   [Definir imágenes de botón](#defining-button-images)
    -   [Definir imágenes de botón mediante mapas de bits](#defining-button-images-by-using-bitmaps)
    -   [Definir imágenes de botón mediante listas de imágenes](#defining-button-images-by-using-image-lists)
-   [Definir texto para botones](#defining-text-for-buttons)
-   [Agregar botones de la barra de herramientas](#adding-toolbar-buttons)
    -   [Estilos de botón de barra de herramientas](#toolbar-button-styles)
    -   [Estados del botón Barra de herramientas](#toolbar-button-states)
    -   [Identificador de comando](#command-identifier)
    -   [Tamaño y posición del botón](#button-size-and-position)
-   [Habilitación de la personalización](#enabling-customization)
-   [Habilitación del seguimiento en caliente](#enabling-hot-tracking)

## <a name="specifying-toolbar-size-and-position"></a>Especificar el tamaño y la posición de la barra de herramientas

Si crea una barra de herramientas mediante [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), la función le permite especificar en píxeles el alto y el ancho de la barra de herramientas.

> [!Note]  
> No [**se recomienda usar CreateToolbarEx,**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) ya que no admite nuevas características de las barras de herramientas, incluidas las listas de imágenes. Para obtener más información sobre cómo crear barras de herramientas, vea [Usar controles de barra de herramientas](using-toolbar-controls.md).

 

La [**función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) no tiene parámetros para especificar el tamaño de la barra de herramientas. El procedimiento de ventana de la barra de herramientas establece automáticamente el tamaño y la posición de la ventana de la barra de herramientas. El alto se basa en el alto de los botones de la barra de herramientas. El ancho es el mismo que el ancho del área de cliente de la ventana primaria. Para cambiar la configuración de tamaño automático, envíe un [**mensaje \_ SETBUTTONSIZE de TB.**](tb-setbuttonsize.md) Los estilos de control comunes [**\_ CCS TOP**](common-control-styles.md) y [**CCS \_ BOTTOM**](common-control-styles.md) determinan si la barra de herramientas se coloca en la parte superior o inferior del área cliente. De forma predeterminada, una barra de herramientas tiene **el estilo CCS \_ TOP.**

Además, el procedimiento de ventana de la barra de herramientas ajusta automáticamente el tamaño de la barra de herramientas cada vez que recibe un [**mensaje WM \_ SIZE**](/windows/desktop/winmsg/wm-size) o [**TB \_ AUTOSIZE.**](tb-autosize.md) Una aplicación debe enviar cualquiera de estos mensajes siempre que cambie el tamaño de la ventana primaria o después de enviar un mensaje que requiera ajustar el tamaño de la barra de herramientas, por ejemplo, un mensaje [**\_ SETBUTTONSIZE de TB.**](tb-setbuttonsize.md)

Los comportamientos de ajuste de tamaño y posición predeterminados de la barra de herramientas se pueden desactivar estableciendo los estilos de control comunes [**CCS \_ NORESIZE**](common-control-styles.md) y [**CCS \_ NOPARENTALIGN.**](common-control-styles.md) Los controles de barra de herramientas hospedados por controles de barra de cambios deben establecer estos estilos porque el control rebar tiene tamaños y posiciones en la barra de herramientas.

## <a name="transparent-toolbars"></a>Barras de herramientas transparentes

Los controles de barra de herramientas admiten un aspecto transparente que permite que el área de cliente de la barra de herramientas se muestre. Hay dos tipos de barras de herramientas transparentes, unas con botones planos y otras con botones tridimensionales. Si desea que la aplicación coincida con la interfaz Windows, use la barra de herramientas de estilo transparente plano.

En la captura de pantalla siguiente se muestran los dos tipos de barras de herramientas transparentes, sin usar estilos visuales.

![captura de pantalla de dos ventanas con diferentes estilos de barras de herramientas, pero ambas barras de herramientas son transparentes](images/toolbartrans.jpg)

En la captura de pantalla siguiente se muestra una barra de herramientas transparente como podría aparecer en Windows Vista, con estilos visuales habilitados. El color de fondo del cuadro de diálogo se ha cambiado para que la transparencia sea más obvia.

![captura de pantalla de una ventana en Windows Vista con una barra de herramientas transparente](images/tb-transparent.png)

Para crear una barra de herramientas transparente, lo único que debe hacer es agregar [**TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) o [**TBSTYLE \_ TRANSPARENT**](toolbar-control-and-button-styles.md) al parámetro de estilo de ventana [**de CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Si no desea que aparezca una línea para indicar la parte inferior de la barra de herramientas, no use el estilo de [**ventana \_ WS BORDER.**](/windows/desktop/winmsg/window-styles)

> [!Note]  
> Cuando se usan estilos visuales, las barras de herramientas pueden ser planas de forma predeterminada.

 

## <a name="list-style-toolbars"></a>Barras de herramientas de estilo de lista

Los botones de la barra de herramientas permiten mostrar texto y mapas de bits. Los botones de una barra de herramientas creada con el [**estilo TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) coloca el texto a la derecha del mapa de bits en lugar de debajo de él.

En la captura de pantalla siguiente se muestra una barra de herramientas con el estilo de lista.

![captura de pantalla de una barra de herramientas con texto a la derecha de cada icono](images/tb-liststyle.png)

Puede usar el estilo de barra de [**herramientas TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) en combinación con el estilo [**TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) para crear una barra de herramientas con botones planos.

## <a name="defining-button-images"></a>Definir imágenes de botón

Hay dos maneras de especificar las imágenes para los botones: por mapas de bits o por listas de imágenes. Una aplicación debe elegir qué método usar. No puede usar ambos métodos con el mismo control de barra de herramientas. Tenga en cuenta que [**la función CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) usa el método de mapa de bits. Las aplicaciones que desean usar el método image list deben usar la [**función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear el control de barra de herramientas.

### <a name="defining-button-images-by-using-bitmaps"></a>Definir imágenes de botón mediante mapas de bits

Cada botón de una barra de herramientas puede incluir una imagen de mapa de bits. Una barra de herramientas usa una lista interna para almacenar la información que necesita para dibujar las imágenes. Cuando se llama a la función [**CreateToolbarEx,**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) se especifica un mapa de bits monocromático o de color que contiene las imágenes iniciales y la barra de herramientas agrega la información a la lista interna de imágenes. Puede agregar imágenes adicionales más adelante mediante el mensaje [**\_ ADDBITMAP de TB.**](tb-addbitmap.md)

Cada imagen tiene un índice de base cero. La primera imagen agregada a la lista interna tiene un índice de 0, la segunda imagen tiene un índice de 1, y así sucesivamente. [**TB \_ ADDBITMAP**](tb-addbitmap.md) agrega imágenes al final de la lista y devuelve el índice de la primera imagen nueva que agregó. Para asociar la imagen a un botón, debe enviar un mensaje [**\_ ADDBUTTONS**](tb-addbuttons.md) de TB y especificar el índice de la imagen después de agregar mapas de bits a la lista de imágenes interna.

Windows supone que todas las imágenes de mapa de bits de una barra de herramientas tienen el mismo tamaño. El tamaño se especifica al crear la barra de herramientas mediante [**CreateToolbarEx.**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) Si usa la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear una barra de herramientas, el tamaño de las imágenes se establece en las dimensiones predeterminadas de 16 por 15 píxeles. Puede usar el mensaje [**\_ SETBITMAPSIZE**](tb-setbitmapsize.md) de TB para cambiar las dimensiones de las imágenes de mapa de bits, pero debe hacerlo antes de agregar cualquier imagen a la lista interna.

### <a name="defining-button-images-by-using-image-lists"></a>Definir imágenes de botón mediante listas de imágenes

También puede almacenar imágenes de botón en un conjunto de [listas de imágenes](image-lists.md). Una lista de imágenes es una colección de imágenes del mismo tamaño, a las que su índice puede hacer referencia a cada una de ellas. Las listas de imágenes se usan para administrar grandes conjuntos de iconos o mapas de bits. Puede usar hasta tres listas de imágenes diferentes para mostrar botones en varios estados, como se muestra en la tabla siguiente.



|  Estado        |  Descripción                                                                                                                                                                                            |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Normal   | Botones en su estado predeterminado.                                                                                                                                                              |
| Acceso frecuente      | Botones que están bajo el puntero o presionados. Los elementos de acceso rápido solo se admiten en los controles de barra de herramientas que tienen [**el estilo TBSTYLE \_ FLAT.**](toolbar-control-and-button-styles.md) |
| Disabled | Botones que están deshabilitados.                                                                                                                                                                   |



 

Una vez que se destruye la barra de herramientas, las aplicaciones deben liberar las listas de imágenes que han creado.

## <a name="defining-text-for-buttons"></a>Definir texto para botones

Cada botón puede mostrar una cadena además o en lugar de una imagen. Una barra de herramientas mantiene una lista interna que contiene todas las cadenas disponibles para los botones de la barra de herramientas. Las cadenas se agregan a la lista interna mediante el mensaje [**\_ ADDSTRING de TB,**](tb-addstring.md) especificando la dirección del búfer que contiene las cadenas que se agregarán. Cada cadena debe terminar en null y la última cadena debe terminarse con dos caracteres NULL.

Cada cadena tiene un índice de base cero. La primera cadena agregada a la lista interna de cadenas tiene un índice de 0, la segunda cadena tiene un índice de 1, y así sucesivamente. [**TB \_ ADDSTRING**](tb-addstring.md) agrega cadenas al final de la lista y devuelve el índice de la primera cadena nueva. El índice de una cadena se usa para asociar la cadena a un botón.

El [**uso de TB \_ ADDSTRING**](tb-addstring.md) no es la única manera de agregar cadenas a una barra de herramientas. Puede mostrar una cadena en un botón pasando un puntero de cadena en el miembro **iString** de la [**estructura TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que se pasa a [**TB \_ ADDBUTTONS**](tb-addbuttons.md). Además, puede usar [**TB \_ SETBUTTONINFO para**](tb-setbuttoninfo.md) asignar texto a un botón de la barra de herramientas.

## <a name="adding-toolbar-buttons"></a>Agregar botones de la barra de herramientas

Si usa la función [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) para crear una barra de herramientas, puede agregar botones a la barra de herramientas rellenando una matriz de estructuras [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) y especificando la dirección de la matriz en la llamada de función. Sin embargo, [**la función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) no tiene un parámetro para pasar una **estructura TBBUTTON.** **CreateWindowEx crea** una barra de herramientas vacía que se rellena mediante el envío de un mensaje [**\_ ADDBUTTONS**](tb-addbuttons.md) de TB, especificando la dirección de una **estructura TBBUTTON.**

Después de crear una barra de herramientas, puede agregar botones enviando un mensaje [**\_ INSERTBUTTON o**](tb-insertbutton.md) [**TB \_ ADDBUTTONS de TB.**](tb-addbuttons.md) Cada botón se describe mediante una estructura [**TBBUTTON,**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que define los atributos del botón, incluidos los índices de su cadena y mapa de bits, así como su estilo, estado, identificador de comando y valor de 32 bits definido por la aplicación.

> [!Note]  
> Si usa la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear una barra de herramientas, debe enviar el mensaje [**\_ BUTTONSTRUCTSIZE de TB**](tb-buttonstructsize.md) antes de agregar los botones. El mensaje pasa el tamaño de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) a la barra de herramientas.

 

### <a name="toolbar-button-styles"></a>Estilos de botón de barra de herramientas

El estilo de un botón determina cómo aparece el botón y cómo responde a la entrada del usuario. Por ejemplo, el [**estilo BTNS \_ BUTTON**](toolbar-control-and-button-styles.md) crea un botón de barra de herramientas que se comporta como un botón de inserción estándar. Un botón con el estilo CHECK de [**BTNS \_**](toolbar-control-and-button-styles.md) es similar a un botón de inserción estándar, salvo que alterna entre los estados presionado y no presionado cada vez que el usuario hace clic en él.

Puede crear grupos de botones de barra de herramientas que actúen como botones de radio mediante el estilo [**BTNS \_ GROUP**](toolbar-control-and-button-styles.md) o [**\_ BTNS CHECKGROUP.**](toolbar-control-and-button-styles.md) Esto hace que un botón permanezca presionado hasta que el usuario elija otro botón del grupo. Un grupo se define como una colección contigua de botones, todo ello con el estilo **BTNS \_ GROUP** o **\_ BTNS CHECKGROUP.**

El [**estilo \_ BTNS SEP**](toolbar-control-and-button-styles.md) crea una pequeña brecha entre los botones o dibuja un etch entre los botones de las barras de herramientas planas. Un botón con el **estilo \_ BTNS SEP** no recibe la entrada del usuario.

La versión 5.80 de los controles comunes introdujo algunos estilos de botón de barra de herramientas nuevos y cambió el nombre de algunos de los estilos anteriores. Todas las marcas de estilo de botón ahora comienzan por BTNS \_ XXX en lugar de TBSTYLE \_ XXX. Para obtener una lista y una explicación de los estilos de botón, vea Control de barra de herramientas [y Estilos de botón](toolbar-control-and-button-styles.md).

### <a name="toolbar-button-states"></a>Estados del botón Barra de herramientas

Cada botón de una barra de herramientas tiene un estado . La barra de herramientas actualiza el estado de un botón para reflejar las acciones del usuario, como hacer clic en el botón. El estado indica si el botón está presionado o no presionado, habilitado o deshabilitado, oculto o visible. Aunque una aplicación establece el estado inicial de un botón al agregar el botón a la barra de herramientas, puede cambiar y recuperar el estado mediante el envío de mensajes [**DE TB \_ GETSTATE**](tb-getstate.md) y [**TB \_ SETSTATE**](tb-setstate.md) a la barra de herramientas. Para obtener una lista de los estados de los botones de la barra de herramientas, vea [Estados de la barra de herramientas.](toolbar-button-states.md)

### <a name="command-identifier"></a>Identificador de comando

Cada botón tiene asociado un identificador de comando definido por la aplicación. Los identificadores de botón normalmente se definen en un archivo de encabezado de aplicación. Por ejemplo, un botón Pegar se puede definir como:


```
#define ID_PASTE 100
```



Cuando el usuario selecciona un botón, la barra de herramientas envía a la ventana primaria un mensaje [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) o [**WM \_ NOTIFY**](wm-notify.md) que incluye el identificador de comando del botón. La ventana primaria examina el identificador de comando y lleva a cabo el comando asociado al botón. Para obtener información sobre cuándo los controles envían **mensajes \_ WM COMMAND** y cuándo envían WM **\_ NOTIFY**, vea la sección Comentarios de la [**documentación de WM \_ NOTIFY.**](wm-notify.md)

### <a name="button-size-and-position"></a>Tamaño y posición del botón

Una barra de herramientas realiza un seguimiento de sus botones asignando a cada botón un índice de posición. El índice es de base cero; Es decir, el botón situado más a la izquierda tiene un índice de 0, el botón siguiente a la derecha tiene un índice de 1, y así sucesivamente. Una aplicación debe especificar el índice de un botón al enviar mensajes para recuperar información sobre el botón o para establecer los atributos del botón.

Una barra de herramientas actualiza los índices de posición a medida que se insertan y quitan botones. Una aplicación puede recuperar el índice de posición actual de un botón mediante el mensaje [**\_ COMMANDTOINDEX de TB.**](tb-commandtoindex.md) El mensaje especifica el identificador de comando de un botón y la ventana de la barra de herramientas usa el identificador para buscar el botón y devolver su índice de posición.

Todos los botones de una barra de herramientas tienen el mismo tamaño. La [**función CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) requiere que se establezca el tamaño inicial de los botones al crear la barra de herramientas. Cuando se usa la [**función CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) el tamaño inicial se establece en las dimensiones predeterminadas de 24 por 22 píxeles. Puede usar el mensaje [**\_ SETBUTTONSIZE**](tb-setbuttonsize.md) de TB para cambiar el tamaño del botón, pero debe hacerlo antes de agregar cualquier botón a la barra de herramientas. El [**mensaje \_ TB GETITEMRECT**](tb-getitemrect.md) recupera las dimensiones actuales de los botones.

Cuando se agrega una cadena que es más larga que cualquier cadena actualmente en la barra de herramientas, la barra de herramientas restablece automáticamente el ancho de sus botones. El ancho se establece para dar cabida a la cadena más larga de la barra de herramientas.

## <a name="enabling-customization"></a>Habilitación de la personalización

Una barra de herramientas tiene características de personalización integradas que puede hacer que esté disponible para el usuario al dar a la barra de herramientas el estilo de control común [**CCS \_ ADJUSTABLE.**](common-control-styles.md) Las características de personalización permiten al usuario arrastrar un botón a una nueva posición o quitar un botón arrastrándolo fuera de la barra de herramientas. Además, el usuario puede hacer doble clic en la barra de herramientas para mostrar el cuadro de diálogo Personalizar barra de herramientas, que permite al usuario agregar, eliminar y reorganizar botones de la barra de herramientas. Para mostrar el cuadro de diálogo, use el [**mensaje \_ PERSONALIZACIÓN de TB.**](tb-customize.md) Una aplicación determina si las características de personalización están disponibles para el usuario y controla la medida en que el usuario puede personalizar la barra de herramientas.

Como parte del proceso de personalización, las aplicaciones a menudo necesitan guardar y restaurar el estado de una barra de herramientas. Por ejemplo, muchas aplicaciones almacenan el estado de la barra de herramientas antes de que el usuario comience a personalizar la barra de herramientas en caso de que el usuario quiera restaurar la barra de herramientas a su estado original. El control de barra de herramientas no mantiene automáticamente un registro de su estado de prepersonalización. La aplicación debe guardar el estado de la barra de herramientas para restaurarlo. Para obtener más información, vea [Usar controles de barra de herramientas](using-toolbar-controls.md).

## <a name="enabling-hot-tracking"></a>Habilitación del seguimiento en caliente

El seguimiento en caliente significa que cuando el puntero se mueve sobre un elemento, cambia la apariencia del botón. Cuando los estilos visuales están habilitados, las barras de herramientas admiten el seguimiento en caliente de forma predeterminada. De lo contrario, solo los controles de barra de herramientas creados [**con el estilo TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) admiten el seguimiento en caliente. Puede usar otros estilos de ventana en combinación con **TBSTYLE \_ FLAT** para generar barras de herramientas que permiten el seguimiento en caliente, pero tienen una apariencia diferente de una barra de herramientas plana. Para obtener más información, vea [Usar controles de barra de herramientas](using-toolbar-controls.md).

 

 