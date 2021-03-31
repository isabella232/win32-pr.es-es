---
title: Acerca de los controles de barra de herramientas
description: Una barra de herramientas es un control que contiene uno o varios botones.
ms.assetid: b5a00a81-8d23-4844-8b0a-776e7cceced8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263d95b13ddee54561cf1b0bb9d003d5d34cdf8d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995653"
---
# <a name="about-toolbar-controls"></a>Acerca de los controles de barra de herramientas

Una barra de herramientas es un control que contiene uno o varios botones. Cada botón, cuando un usuario hace clic en él, envía un mensaje de comando a la ventana primaria. Normalmente, los botones de una barra de herramientas corresponden a elementos del menú de la aplicación, lo que proporciona una forma adicional y más directa para que el usuario tenga acceso a los comandos de una aplicación.

En la captura de pantalla siguiente se muestra una ventana que contiene una barra de herramientas simple para las operaciones de archivo. La aplicación ha habilitado los estilos visuales. El botón Guardar está "activo" porque el cursor se mantiene sobre él cuando se tomó la captura de pantalla. La apariencia real del control varía en función del sistema operativo y del tema seleccionado por el usuario.

![captura de pantalla de una ventana con una barra de herramientas de tres botones; un botón está activo](images/tb-withstyles.png)

En la captura de pantalla siguiente se muestra el mismo control en una aplicación que se compiló sin estilos visuales habilitados.

![captura de pantalla de una ventana sin estilos visuales: ninguno de los botones tiene un aspecto activo](images/tb-wostyles.png)

En los temas siguientes se describen las características que se deben tener en cuenta al planear una barra de herramientas. Para obtener información específica sobre la implementación de y el código de ejemplo, vea [usar controles de barra de herramientas](using-toolbar-controls.md).

-   [Especificar el tamaño y la posición de la barra de herramientas](#specifying-toolbar-size-and-position)
-   [Barras de herramientas transparentes](#transparent-toolbars)
-   [Barras de herramientas de estilo de lista](#list-style-toolbars)
-   [Definir imágenes de botón](#defining-button-images)
    -   [Definir imágenes de botón mediante mapas de bits](#defining-button-images-by-using-bitmaps)
    -   [Definir imágenes de botón mediante listas de imágenes](#defining-button-images-by-using-image-lists)
-   [Definir texto para botones](#defining-text-for-buttons)
-   [Agregar botones de barra de herramientas](#adding-toolbar-buttons)
    -   [Estilos de botón de barra de herramientas](#toolbar-button-styles)
    -   [Estados del botón de la barra de herramientas](#toolbar-button-states)
    -   [Identificador de comando](#command-identifier)
    -   [Tamaño y posición del botón](#button-size-and-position)
-   [Habilitar la personalización](#enabling-customization)
-   [Habilitación del seguimiento activo](#enabling-hot-tracking)

## <a name="specifying-toolbar-size-and-position"></a>Especificar el tamaño y la posición de la barra de herramientas

Si crea una barra de herramientas mediante [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), la función le permite especificar en píxeles el alto y el ancho de la barra de herramientas.

> [!Note]  
> No se recomienda usar [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) , ya que no es compatible con las nuevas características de las barras de herramientas, incluidas las listas de imágenes. Para obtener más información sobre la creación de barras de herramientas, vea [usar controles de barra de herramientas](using-toolbar-controls.md).

 

La función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) no tiene parámetros para especificar el tamaño de la barra de herramientas. El procedimiento de ventana barra de herramientas establece automáticamente el tamaño y la posición de la ventana de la barra de herramientas. El alto se basa en el alto de los botones de la barra de herramientas. El ancho es el mismo que el ancho del área cliente de la ventana primaria. Para cambiar la configuración de tamaño automático, envíe un mensaje de [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) . Los estilos de control comunes de los controles [**CCS \_ Top**](common-control-styles.md) y [**CCS \_ inferiores**](common-control-styles.md) determinan si la barra de herramientas se coloca a lo largo de la parte superior o inferior del área cliente. De forma predeterminada, una barra de herramientas tiene el estilo de **CCS \_ superior** .

Además, el procedimiento de ventana de la barra de herramientas ajusta automáticamente el tamaño de la barra de herramientas cada vez que recibe un mensaje de tamaño de [**WM \_**](/windows/desktop/winmsg/wm-size) o [**\_ tamaño**](tb-autosize.md) automático de TB. Una aplicación debe enviar cualquiera de estos mensajes cada vez que cambie el tamaño de la ventana primaria o después de enviar un mensaje que requiera ajustar el tamaño de la barra de herramientas, por ejemplo, un mensaje de [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) .

Los comportamientos de ajuste de tamaño y posición predeterminados de la barra de herramientas se pueden desactivar estableciendo los estilos de control comunes de [**CCS \_ NORESIZE**](common-control-styles.md) y [**CCS \_ NOPARENTALIGN**](common-control-styles.md) . Los controles de barra de herramientas hospedados por controles rebar deben establecer estos estilos porque el control rebar dimensiona y coloca la barra de herramientas.

## <a name="transparent-toolbars"></a>Barras de herramientas transparentes

Los controles de barra de herramientas admiten una apariencia transparente que permite que el área cliente de la barra de herramientas se muestre. Hay dos tipos de barras de herramientas transparentes, unas con botones planos y otras con botones tridimensionales. Si desea que la aplicación coincida con la interfaz de Windows, use la barra de herramientas estilo transparente.

En la captura de pantalla siguiente se muestran los dos tipos de barras de herramientas transparentes, no el uso de estilos visuales.

![captura de pantalla de dos ventanas con distintos estilos de barras de herramientas, pero ambas barras de herramientas son transparentes](images/toolbartrans.jpg)

En la siguiente captura de pantalla se muestra una barra de herramientas transparente como podría aparecer en Windows Vista, con los estilos visuales habilitados. El color de fondo del cuadro de diálogo se ha cambiado para que la transparencia sea más obvia.

![captura de pantalla de una ventana en Windows Vista con una barra de herramientas transparente](images/tb-transparent.png)

Para crear una barra de herramientas transparente, lo único que debe hacer es agregar [**TBSTYLE \_ plano**](toolbar-control-and-button-styles.md) o [**TBSTYLE \_ transparente**](toolbar-control-and-button-styles.md) al parámetro de estilo de ventana de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Si no desea que aparezca una línea para indicar la parte inferior de la barra de herramientas, no use el estilo de ventana de [**\_ borde de WS**](/windows/desktop/winmsg/window-styles) .

> [!Note]  
> Al usar estilos visuales, las barras de herramientas pueden ser planas de forma predeterminada.

 

## <a name="list-style-toolbars"></a>Barras de herramientas de estilo de lista

Los botones de la barra de herramientas le permiten mostrar tanto el texto como los mapas de bits. Los botones de una barra de herramientas creada con el estilo de [**\_ lista TBSTYLE**](toolbar-control-and-button-styles.md) colocan el texto a la derecha del mapa de bits en lugar de debajo de él.

En la captura de pantalla siguiente se muestra una barra de herramientas con el estilo de lista.

![captura de pantalla de una barra de herramientas con el texto a la derecha de cada icono](images/tb-liststyle.png)

Puede usar el estilo de la barra de herramientas de [**\_ lista TBSTYLE**](toolbar-control-and-button-styles.md) en combinación con el estilo [**\_ plano TBSTYLE**](toolbar-control-and-button-styles.md) para crear una barra de herramientas con botones planos.

## <a name="defining-button-images"></a>Definir imágenes de botón

Hay dos maneras de especificar las imágenes de los botones, por mapas de bits o por listas de imágenes. Una aplicación debe elegir el método que se va a usar. No puede utilizar ambos métodos con el mismo control Toolbar. Tenga en cuenta que la función [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) usa el método Bitmap. Las aplicaciones que deseen usar el método de lista de imágenes deben usar la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear el control de barra de herramientas.

### <a name="defining-button-images-by-using-bitmaps"></a>Definir imágenes de botón mediante mapas de bits

Cada botón de una barra de herramientas puede incluir una imagen de mapa de imágenes. Una barra de herramientas usa una lista interna para almacenar la información que necesita para dibujar las imágenes. Cuando se llama a la función [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) , se especifica un mapa de bits monocromo o de color que contiene las imágenes iniciales y la barra de herramientas agrega la información a la lista interna de imágenes. Puede agregar más imágenes más adelante mediante el mensaje [**TB \_ ADDBITMAP**](tb-addbitmap.md) .

Cada imagen tiene un índice basado en cero. La primera imagen agregada a la lista interna tiene un índice de 0, la segunda imagen tiene un índice de 1, y así sucesivamente. [**TB \_ ADDBITMAP**](tb-addbitmap.md) agrega imágenes al final de la lista y devuelve el índice de la primera imagen nueva que se ha agregado. Para asociar la imagen con un botón, debe enviar un mensaje [**TB \_ ADDBUTTONS**](tb-addbuttons.md) y especificar el índice de la imagen después de agregar mapas de bits a la lista de imágenes internas.

Windows supone que todas las imágenes de mapa de la barra de herramientas tienen el mismo tamaño. El tamaño se especifica al crear la barra de herramientas mediante [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex). Si usa la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear una barra de herramientas, el tamaño de las imágenes se establece en las dimensiones predeterminadas de 16 por 15 píxeles. Puede usar el mensaje de [**TB \_ SETBITMAPSIZE**](tb-setbitmapsize.md) para cambiar las dimensiones de las imágenes de mapa Dete, pero debe hacerlo antes de agregar imágenes a la lista interna.

### <a name="defining-button-images-by-using-image-lists"></a>Definir imágenes de botón mediante listas de imágenes

También puede almacenar imágenes de botón en un conjunto de [listas de imágenes](image-lists.md). Una lista de imágenes es una colección de imágenes del mismo tamaño, a las que se puede hacer referencia a través de su índice. Las listas de imágenes se utilizan para administrar grandes conjuntos de iconos o mapas de bits. Puede usar hasta tres listas de imágenes diferentes para mostrar botones en varios Estados, como se muestra en la tabla siguiente.



|          |                                                                                                                                                                                              |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Normal   | Botones en su estado predeterminado.                                                                                                                                                              |
| Acceso frecuente      | Botones que están debajo del puntero o presionados. Los elementos de acceso frecuente solo se admiten en los controles de barra de herramientas que tienen el estilo [**\_ plano TBSTYLE**](toolbar-control-and-button-styles.md) . |
| Disabled | Botones que están deshabilitados.                                                                                                                                                                   |



 

Una vez destruida la barra de herramientas, las aplicaciones deben liberar las listas de imágenes que hayan creado.

## <a name="defining-text-for-buttons"></a>Definir texto para botones

Cada botón puede mostrar una cadena además de o en lugar de una imagen. Una barra de herramientas mantiene una lista interna que contiene todas las cadenas disponibles para los botones de la barra de herramientas. Puede Agregar cadenas a la lista interna mediante el mensaje de [**TB \_ ADDSTRING**](tb-addstring.md) , especificando la dirección del búfer que contiene las cadenas que se van a agregar. Cada cadena debe terminar en NULL y la última cadena debe terminar con dos caracteres null.

Cada cadena tiene un índice basado en cero. La primera cadena agregada a la lista interna de cadenas tiene un índice de 0, la segunda cadena tiene un índice de 1, y así sucesivamente. [**TB \_ ADDSTRING**](tb-addstring.md) agrega cadenas al final de la lista y devuelve el índice de la primera cadena nueva. El índice de una cadena se usa para asociar la cadena con un botón.

El uso de [**TB \_ ADDSTRING**](tb-addstring.md) no es la única manera de agregar cadenas a una barra de herramientas. Puede mostrar una cadena en un botón pasando un puntero de cadena en el miembro **iString** de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que se pasa a [**TB \_ ADDBUTTONS**](tb-addbuttons.md). Además, puede usar [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) para asignar texto a un botón de la barra de herramientas.

## <a name="adding-toolbar-buttons"></a>Agregar botones de barra de herramientas

Si usa la función [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) para crear una barra de herramientas, puede agregar botones a la barra de herramientas rellenando una matriz de estructuras [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) y especificando la dirección de la matriz en la llamada de función. Sin embargo, la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) no tiene un parámetro para pasar una estructura **TBBUTTON** . **CreateWindowEx** crea una barra de herramientas vacía que se rellena mediante el envío de un mensaje de [**TB \_ ADDBUTTONS**](tb-addbuttons.md) , que especifica la dirección de una estructura **TBBUTTON** .

Después de crear una barra de herramientas, puede agregar botones mediante el envío de un mensaje [**TB \_ INSERTBUTTON**](tb-insertbutton.md) o [**TB \_ ADDBUTTONS**](tb-addbuttons.md) . Cada botón se describe mediante una estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) , que define los atributos del botón, incluidos los índices de su cadena y mapa de bits, así como su estilo, estado, identificador de comando y valor de 32 bits definido por la aplicación.

> [!Note]  
> Si usa la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear una barra de herramientas, debe enviar el mensaje de [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) antes de agregar cualquier botón. El mensaje pasa el tamaño de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) a la barra de herramientas.

 

### <a name="toolbar-button-styles"></a>Estilos de botón de barra de herramientas

El estilo de un botón determina cómo aparece el botón y cómo responde a los datos proporcionados por el usuario. Por ejemplo, el estilo de [**\_ botón BTNS**](toolbar-control-and-button-styles.md) crea un botón de barra de herramientas que se comporta como un botón de tecla de preinstalación estándar. Un botón que tiene el estilo de [**\_ comprobación BTNS**](toolbar-control-and-button-styles.md) es similar a un botón de comando de inserción estándar, salvo que alterna entre los Estados presionado y sin presionar cada vez que el usuario hace clic en él.

Puede crear grupos de botones de la barra de herramientas que actúen como botones de radio mediante el [**\_ Grupo BTNS**](toolbar-control-and-button-styles.md) o el estilo [**\_ CHECKGROUP BTNS**](toolbar-control-and-button-styles.md) . Esto hace que se mantenga presionado un botón hasta que el usuario elija otro botón del grupo. Un grupo se define como una colección contigua de botones, todos con el **BTNS \_** o el estilo **BTNS \_ CHECKGROUP** .

El estilo [**BTNS \_ Sep**](toolbar-control-and-button-styles.md) crea un pequeño espacio entre los botones o dibuja un grabado entre los botones de las barras de herramientas sin formato. Un botón con el estilo **BTNS \_ Sep** no recibe datos proporcionados por el usuario.

En la versión 5,80 de los controles comunes se introdujeron algunos estilos de botón de la barra de herramientas nuevos y se cambió el nombre de algunos de los estilos anteriores. Ahora, todas las marcas de estilo de botón comienzan por BTNS \_ XXX en lugar de TBSTYLE \_ xxx. Para obtener una lista y una descripción de los estilos de botón, vea [control de barra de herramientas y estilos de botón](toolbar-control-and-button-styles.md).

### <a name="toolbar-button-states"></a>Estados del botón de la barra de herramientas

Cada botón de una barra de herramientas tiene un estado. La barra de herramientas actualiza el estado de un botón para reflejar las acciones del usuario, como hacer clic en el botón. El estado indica si el botón está actualmente presionado o no presionado, habilitado o deshabilitado, oculto o visible. Aunque una aplicación establece el estado inicial de un botón al agregar el botón a la barra de herramientas, puede cambiar y recuperar el estado mediante el envío de los mensajes [**TB \_ GETSTATE**](tb-getstate.md) y [**TB \_ SETSTATE**](tb-setstate.md) a la barra de herramientas. Para obtener una lista de Estados de botones de la barra de herramientas, vea Estados de la [barra de herramientas](toolbar-button-states.md).

### <a name="command-identifier"></a>Identificador de comando

Cada botón tiene asociado un identificador de comando definido por la aplicación. Los identificadores de botón normalmente se definen en un archivo de encabezado de aplicación. Por ejemplo, un botón pegar se puede definir de la siguiente manera:


```
#define ID_PASTE 100
```



Cuando el usuario selecciona un botón, la barra de herramientas envía a la ventana primaria un [**\_ comando de WM**](/windows/desktop/menurc/wm-command) o un mensaje de [**\_ notificación de WM**](wm-notify.md) que incluye el identificador de comando del botón. La ventana primaria examina el identificador de comando y realiza el comando asociado al botón. Para obtener información acerca de cuándo los controles envían mensajes de **\_ comandos de WM** y cuándo envían la **\_ notificación de WM**, consulte la sección Comentarios de la documentación de [**\_ notificaciones de WM**](wm-notify.md) .

### <a name="button-size-and-position"></a>Tamaño y posición del botón

Una barra de herramientas realiza un seguimiento de sus botones asignando cada botón a un índice de posición. El índice es de base cero; es decir, el botón situado más a la izquierda tiene un índice de 0, el botón siguiente a la derecha tiene un índice de 1, y así sucesivamente. Una aplicación debe especificar el índice de un botón al enviar mensajes para recuperar información sobre el botón o para establecer los atributos del botón.

Una barra de herramientas actualiza los índices de posición a medida que se insertan y se quitan botones. Una aplicación puede recuperar el índice de posición actual de un botón mediante el mensaje [**TB \_ COMMANDTOINDEX**](tb-commandtoindex.md) . El mensaje especifica el identificador de comando de un botón y la ventana de la barra de herramientas usa el identificador para buscar el botón y devolver su índice de posición.

Todos los botones de una barra de herramientas tienen el mismo tamaño. La función [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) requiere que se establezca el tamaño inicial de los botones al crear la barra de herramientas. Cuando se usa la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , el tamaño inicial se establece en las dimensiones predeterminadas de 24 por 22 píxeles. Puede usar el mensaje de [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) para cambiar el tamaño del botón, pero debe hacerlo antes de agregar botones a la barra de herramientas. El mensaje [**TB \_ GETITEMRECT**](tb-getitemrect.md) recupera las dimensiones actuales de los botones.

Cuando se agrega una cadena que es más larga que cualquier cadena que se encuentre actualmente en la barra de herramientas, la barra de herramientas restablece automáticamente el ancho de sus botones. El ancho se establece para alojar la cadena más larga en la barra de herramientas.

## <a name="enabling-customization"></a>Habilitar la personalización

Una barra de herramientas tiene características de personalización integradas que puede poner a disposición del usuario. para ello, proporcione a la barra de herramientas el estilo de control común de [**CCS \_ ajustable**](common-control-styles.md) . Las características de personalización permiten al usuario arrastrar un botón a una nueva posición o quitar un botón arrastrándolo fuera de la barra de herramientas. Además, el usuario puede hacer doble clic en la barra de herramientas para mostrar el cuadro de diálogo Personalizar barra de herramientas, que permite al usuario agregar, eliminar y reorganizar botones de la barra de herramientas. Para mostrar el cuadro de diálogo, use el mensaje de [**\_ Personalización de TB**](tb-customize.md) . Una aplicación determina si las características de personalización están disponibles para el usuario y controla la medida en la que el usuario puede personalizar la barra de herramientas.

Como parte del proceso de personalización, las aplicaciones suelen necesitar guardar y restaurar el estado de una barra de herramientas. Por ejemplo, muchas aplicaciones almacenan el estado de la barra de herramientas antes de que el usuario comience a personalizar la barra de herramientas en caso de que el usuario desee restaurar la barra de herramientas a su estado original. El control de barra de herramientas no mantiene automáticamente un registro de su estado de personalización. La aplicación debe guardar el estado de la barra de herramientas para restaurarlo. Para obtener más información, vea [usar controles Toolbar](using-toolbar-controls.md).

## <a name="enabling-hot-tracking"></a>Habilitación del seguimiento activo

El seguimiento activo significa que cuando el puntero se mueve sobre un elemento, cambia la apariencia del botón. Cuando los estilos visuales están habilitados, las barras de herramientas admiten el seguimiento activo de forma predeterminada. De lo contrario, solo los controles de barra de herramientas creados con el estilo [**\_ plano TBSTYLE**](toolbar-control-and-button-styles.md) admiten el seguimiento activo. Puede usar otros estilos de ventana en combinación con **TBSTYLE \_ plano** para generar barras de herramientas que habiliten el seguimiento activo, pero que tengan una apariencia diferente a la de una barra de herramientas plana. Para obtener más información, vea [usar controles Toolbar](using-toolbar-controls.md).

 

 