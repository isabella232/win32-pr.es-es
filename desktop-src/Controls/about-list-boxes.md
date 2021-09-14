---
title: Acerca de los cuadros de lista
description: En esta sección se describen las características del cuadro de lista.
ms.assetid: 359bb363-5b97-4e0c-bdc4-bfa6a6504a76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674712226a79960e44ab99ed8e59c88b27984efb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061413"
---
# <a name="about-list-boxes"></a>Acerca de los cuadros de lista

Un control de cuadro de lista contiene una lista simple de la que el usuario generalmente puede seleccionar uno o varios elementos. Los cuadros de lista proporcionan una flexibilidad limitada en comparación con los [controles de vista de](list-view-control-reference.md) lista.

Los elementos de cuadro de lista se pueden representar mediante cadenas de texto, mapas de bits o ambos. Si el cuadro de lista no es lo suficientemente grande como para mostrar todos los elementos del cuadro de lista a la vez, el cuadro de lista proporciona una barra de desplazamiento. El usuario se desplaza por los elementos del cuadro de lista y aplica o quita el estado de selección según sea necesario. Al seleccionar un elemento de cuadro de lista se cambia su apariencia visual, normalmente cambiando el texto y los colores de fondo a los especificados por las métricas pertinentes del sistema operativo. Cuando el usuario selecciona o anula la selección de un elemento, el sistema envía un mensaje de notificación a la ventana primaria del cuadro de lista.

Para una aplicación ANSI, el sistema convierte el texto de un cuadro de lista en Unicode mediante la **página de códigos CP \_ ACP.** Esto puede causar problemas. Por ejemplo, los caracteres latinos acentuados en un cuadro de lista no Unicode de Windows, la versión japonesa aparecerá desconsolada. Para solucionar este problema, compile la aplicación como Unicode o use un cuadro de lista dibujado por el propietario.

En esta sección se de tratan los temas siguientes:

-   [Crear un cuadro de lista](#creating-a-list-box)
-   [Estilos y tipos de cuadro de lista](#list-box-types-and-styles)
-   [Funciones de cuadro de lista](#list-box-functions)
-   [Mensajes de notificación de cuadros de lista](#notification-messages-from-list-boxes)
-   [Mensajes a cuadros de lista](#notification-messages-from-list-boxes)
-   [Procesamiento de mensajes de ventana predeterminado](#default-window-message-processing)
-   [Cuadros de lista dibujados por el propietario](#owner-drawn-list-boxes)
-   [Arrastrar cuadros de lista](#drag-list-boxes)
    -   [Crear cuadros de lista de arrastre](#creating-drag-list-boxes)
    -   [Arrastrar mensajes de cuadro de lista](#drag-list-box-messages)
    -   [Códigos de notificación de cuadro de lista de arrastre](#drag-list-box-notification-codes)

## <a name="creating-a-list-box"></a>Crear un cuadro de lista

La manera más fácil de crear un cuadro de lista en un cuadro de diálogo es arrastrarlo desde el cuadro de herramientas Microsoft Visual Studio al recurso de diálogo. Para crear un cuadro de lista dinámicamente o para crear un cuadro de lista en una ventana que no sea [](list-box-styles.md)un cuadro de diálogo, use la función [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) especificando la clase de ventana WC [**\_ LISTBOX**](common-control-window-classes.md) y los estilos de cuadro de lista adecuados.

## <a name="list-box-types-and-styles"></a>Estilos y tipos de cuadro de lista

Hay dos tipos de cuadros de lista: selección única (valor predeterminado) y selección múltiple. En un cuadro de lista de selección única, el usuario solo puede seleccionar un elemento a la vez. En un cuadro de lista de selección múltiple, el usuario puede seleccionar más de un elemento a la vez. Para crear un cuadro de lista de selección múltiple, especifique [**el estilo LBS \_ MULTIPLESEL**](list-box-styles.md) o [**LBS \_ EXTENDEDSEL.**](list-box-styles.md)

La apariencia y el funcionamiento de un cuadro de lista se controlan mediante estilos [de cuadro de](list-box-styles.md) lista y estilos de ventana. Estos estilos indican si la lista está ordenada, organizada en varias columnas, dibujada por la aplicación, y así sucesivamente. Las dimensiones y estilos de un cuadro de lista normalmente se definen en una plantilla de cuadro de diálogo que se incluye en los recursos de una aplicación.

> [!Note]  
> Para usar estilos visuales con estos controles, una aplicación debe incluir un manifiesto y debe llamar a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) al principio del programa. Para obtener información sobre los estilos visuales, vea [Estilos visuales.](themes-overview.md) Para obtener información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="list-box-functions"></a>Funciones de cuadro de lista

La [**función DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) reemplaza el contenido de un cuadro de lista por los nombres de unidades, directorios y archivos que coinciden con un conjunto de criterios especificado. La [**función DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) recupera la selección actual en un cuadro de lista inicializado por **DlgDirList**. Estas funciones hacen posible que el usuario seleccione una unidad, un directorio o un archivo en un cuadro de lista sin escribir la ubicación y el nombre del archivo.

Además, la [**función GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) devuelve el número de elementos por columna en un cuadro de lista especificado.

## <a name="notification-messages-from-list-boxes"></a>Mensajes de notificación de cuadros de lista

Cuando se produce un evento en un cuadro de lista, el cuadro de lista envía un código de notificación, en forma de mensaje [**WM \_ COMMAND,**](/windows/desktop/menurc/wm-command) al procedimiento de cuadro de diálogo de la ventana de propietario. Los códigos de notificación de cuadro de lista se envían cuando un usuario selecciona, hace doble clic o cancela un elemento del cuadro de lista. cuando el cuadro de lista recibe o pierde el foco del teclado; y cuando el sistema no puede asignar suficiente memoria para una solicitud de cuadro de lista. Un **mensaje \_ WM COMMAND** contiene el identificador del cuadro de lista en la palabra de orden bajo del parámetro *wParam* y el código de notificación en la palabra de orden superior. El *parámetro lParam* contiene el identificador de la ventana de control.

No es necesario un procedimiento de cuadro de diálogo para procesar estos mensajes; el procedimiento de ventana predeterminado los procesa.

Una aplicación debe supervisar y procesar los siguientes códigos de notificación de cuadro de lista.



| Código de notificación                   | Descripción                                                      |
|-------------------------------------|------------------------------------------------------------------|
| [\_DBLCLK de LBN](lbn-dblclk.md)       | El usuario hace doble clic en un elemento del cuadro de lista.                  |
| [LBN \_ ERRSPACE](lbn-errspace.md)   | El cuadro de lista no puede asignar suficiente memoria para satisfacer una solicitud. |
| [LBN \_ KILLFOCUS](lbn-killfocus.md) | El cuadro de lista pierde el foco del teclado.                           |
| [LBN \_ SELCANCEL](lbn-selcancel.md) | El usuario cancela la selección de un elemento en el cuadro de lista.       |
| [LBN \_ SELCHANGE](lbn-selchange.md) | La selección de un cuadro de lista está a punto de cambiar.                  |
| [LBN \_ SETFOCUS](lbn-setfocus.md)   | El cuadro de lista recibe el foco del teclado.                        |



 

## <a name="messages-to-list-boxes"></a>Mensajes a cuadros de lista

Un procedimiento de cuadro de diálogo puede enviar mensajes a un cuadro de lista para agregar, eliminar, examinar y cambiar elementos del cuadro de lista. Por ejemplo, un procedimiento de cuadro de diálogo podría enviar un mensaje [**\_ ADDSTRING**](lb-addstring.md) de LB a un cuadro de lista para agregar un elemento y un mensaje [**\_ LB GETSEL**](lb-getsel.md) para determinar si el elemento está seleccionado. Otros mensajes establecen y recuperan información sobre el tamaño, la apariencia y el comportamiento del cuadro de lista. Por ejemplo, el [**mensaje \_ LB SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) establece el ancho desplazable de un cuadro de lista. Un procedimiento de cuadro de diálogo puede enviar cualquier mensaje a un cuadro de lista mediante la [**función SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o [**SendDlgItemMessage.**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea)

A menudo se hace referencia a un elemento de cuadro de lista por su *índice*, un entero que representa la posición del elemento en el cuadro de lista. El índice del primer elemento de un cuadro de lista es 0, el índice del segundo elemento es 1, y así sucesivamente.

En la tabla siguiente se describe cómo responde el procedimiento predefinido del cuadro de lista a los mensajes del cuadro de lista.



| Message                                                   | Response                                                                                                                                                                                                                         |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LB \_ ADDFILE**](lb-addfile.md)                         | Inserta un archivo en un cuadro de lista de directorios rellenado por la función [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) y recupera el índice del cuadro de lista del elemento insertado.                                                                  |
| [**LB \_ ADDSTRING**](lb-addstring.md)                     | Agrega una cadena a un cuadro de lista y devuelve su índice.                                                                                                                                                                               |
| [**LB \_ DELETESTRING**](lb-deletestring.md)               | Quita una cadena de un cuadro de lista y devuelve el número de cadenas que permanecen en la lista.                                                                                                                                      |
| [**LB \_ DIR**](lb-dir.md)                                 | Agrega una lista de nombres de archivo a un cuadro de lista y devuelve el índice del último nombre de archivo agregado.                                                                                                                                       |
| [**LB \_ FINDSTRING**](lb-findstring.md)                   | Devuelve el índice de la primera cadena del cuadro de lista que comienza con una cadena especificada.                                                                                                                                       |
| [**LB \_ FINDSTRINGEXACT**](lb-findstringexact.md)         | Devuelve el índice de la cadena del cuadro de lista que es igual a una cadena especificada.                                                                                                                                             |
| [**LB \_ GETANCHORINDEX**](lb-getanchorindex.md)           | Devuelve el índice del elemento que el mouse seleccionó por última vez.                                                                                                                                                                      |
| [**LB \_ GETCARETINDEX**](lb-getcaretindex.md)             | Devuelve el índice del elemento que tiene el rectángulo de foco.                                                                                                                                                                      |
| [**LB \_ GETCOUNT**](lb-getcount.md)                       | Devuelve el número de elementos del cuadro de lista.                                                                                                                                                                                     |
| [**LB \_ GETCURSEL**](lb-getcursel.md)                     | Devuelve el índice del elemento seleccionado actualmente.                                                                                                                                                                                |
| [**LB \_ GETHORIZONTALEXTENT**](lb-gethorizontalextent.md) | Devuelve el ancho desplazable, en píxeles, de un cuadro de lista.                                                                                                                                                                          |
| [**LB \_ GETITEMDATA**](lb-getitemdata.md)                 | Devuelve el valor asociado al elemento especificado.                                                                                                                                                                    |
| [**LB \_ GETITEMHEIGHT**](lb-getitemheight.md)             | Devuelve el alto, en píxeles, de un elemento en un cuadro de lista.                                                                                                                                                                         |
| [**LB \_ GETITEMRECT**](lb-getitemrect.md)                 | Recupera las coordenadas de cliente del elemento de cuadro de lista especificado.                                                                                                                                                                 |
| [**LB \_ GETLOCALE**](lb-getlocale.md)                     | Recupera la configuración regional del cuadro de lista. La palabra de orden superior contiene el código de país o región y la palabra de orden bajo contiene el identificador de idioma.                                                                              |
| [**LB \_ GETSEL**](lb-getsel.md)                           | Devuelve el estado de selección de un elemento de cuadro de lista.                                                                                                                                                                                  |
| [**LB \_ GETSELCOUNT**](lb-getselcount.md)                 | Devuelve el número de elementos seleccionados en un cuadro de lista de selección múltiple.                                                                                                                                                           |
| [**LB \_ GETSELITEMS**](lb-getselitems.md)                 | Crea una matriz de los índices de todos los elementos seleccionados en un cuadro de lista de selección múltiple y devuelve el número total de elementos seleccionados.                                                                                           |
| [**LB \_ GETTEXT**](lb-gettext.md)                         | Recupera la cadena asociada a un elemento especificado y la longitud de la cadena.                                                                                                                                              |
| [**LB \_ GETTEXTLEN**](lb-gettextlen.md)                   | Devuelve la longitud, en caracteres, de la cadena asociada a un elemento especificado.                                                                                                                                               |
| [**LB \_ GETTOPINDEX**](lb-gettopindex.md)                 | Devuelve el índice del primer elemento visible en un cuadro de lista.                                                                                                                                                                       |
| [**LB \_ INITSTORAGE**](lb-initstorage.md)                 | Asigna memoria para el número especificado de elementos y sus cadenas asociadas.                                                                                                                                                 |
| [**LB \_ INSERTSTRING**](lb-insertstring.md)               | Inserta una cadena en un índice especificado en un cuadro de lista.                                                                                                                                                                             |
| [**LB \_ ITEMFROMPOINT**](lb-itemfrompoint.md)             | Recupera el índice de base cero del elemento más cercano al punto especificado en un cuadro de lista.                                                                                                                                            |
| [**LB \_ RESETCONTENT**](lb-resetcontent.md)               | Quita todos los elementos de un cuadro de lista.                                                                                                                                                                                               |
| [**LB \_ SELECTSTRING**](lb-selectstring.md)               | Selecciona la primera cadena que encuentra que coincide con un prefijo especificado.                                                                                                                                                               |
| [**LB \_ SELITEMRANGE**](lb-selitemrange.md)               | Selecciona un intervalo especificado de elementos en un cuadro de lista.                                                                                                                                                                                |
| [**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md)           | Selecciona un intervalo de elementos especificado si el índice del primer elemento del intervalo es menor que el índice del último elemento del intervalo. Cancela la selección en el intervalo si el índice del primer elemento es mayor que el último. |
| [**LB \_ SETANCHORINDEX**](lb-setanchorindex.md)           | Establece el elemento que el mouse seleccionó por última vez en un elemento especificado.                                                                                                                                                                  |
| [**LB \_ SETCARETINDEX**](lb-setcaretindex.md)             | Establece el rectángulo de foco en un elemento de cuadro de lista especificado.                                                                                                                                                                           |
| [**LB \_ SETCOLUMNWIDTH**](lb-setcolumnwidth.md)           | Establece el ancho, en píxeles, de todas las columnas de un cuadro de lista.                                                                                                                                                                         |
| [**LB \_ SETCOUNT**](lb-setcount.md)                       | Establece el número de elementos de un cuadro de lista.                                                                                                                                                                                          |
| [**LB \_ SETCURSEL**](lb-setcursel.md)                     | Selecciona un elemento de cuadro de lista especificado.                                                                                                                                                                                               |
| [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) | Establece el ancho desplazable, en píxeles, de un cuadro de lista.                                                                                                                                                                             |
| [**LB \_ SETITEMDATA**](lb-setitemdata.md)                 | Asocia un valor a un elemento de cuadro de lista.                                                                                                                                                                                         |
| [**LB \_ SETITEMHEIGHT**](lb-setitemheight.md)             | Establece el alto, en píxeles, de un elemento o elementos de un cuadro de lista.                                                                                                                                                                   |
| [**LB \_ SETLOCALE**](lb-setlocale.md)                     | Establece la configuración regional de un cuadro de lista y devuelve el identificador de configuración regional anterior.                                                                                                                                                        |
| [**LB \_ SETSEL**](lb-setsel.md)                           | Selecciona un elemento en un cuadro de lista de selección múltiple.                                                                                                                                                                                |
| [**LB \_ SETTABSTOPS**](lb-settabstops.md)                 | Establece que la pestaña se detiene en las especificadas en una matriz especificada.                                                                                                                                                                      |
| [**LB \_ SETTOPINDEX**](lb-settopindex.md)                 | Desplaza el cuadro de lista para que el elemento especificado esté en la parte superior del intervalo visible.                                                                                                                                                   |



 

## <a name="default-window-message-processing"></a>Procesamiento de mensajes de ventana predeterminado

El procedimiento de ventana para la clase predefinida de ventana de cuadro de lista lleva a cabo el procesamiento predeterminado para todos los mensajes que el cuadro de lista no procesa. Cuando el procedimiento del cuadro de lista devuelve **FALSE** para un mensaje, el procedimiento de ventana predefinido comprueba el mensaje y realiza acciones predeterminadas, como se muestra en la tabla siguiente.



| Message                                            | Acción predeterminada                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)                   | Mueve la selección al primer elemento que comienza con el carácter que el usuario ha especificado. Si el cuadro de lista tiene el estilo [**L BS \_ OWNERDRAW,**](button-styles.md) no se produce ninguna acción. Varios caracteres que se escriben dentro de un intervalo corto se tratan como un grupo y se selecciona el primer elemento que comienza con esa serie de caracteres.<br/> |
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                 | Crea un cuadro de lista vacío.                                                                                                                                                                                                                                                                                                                                               |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)               | Destruye el cuadro de lista y libera los recursos que usa.                                                                                                                                                                                                                                                                                                              |
|                                                    | Pasa el mensaje al procedimiento del cuadro de diálogo o al proceso de ventana primaria.                                                                                                                                                                                                                                                                                                 |
| [**WM \_ ENABLE**](/windows/desktop/winmsg/wm-enable)                 | Si el control está visible, invalida el rectángulo para que las cadenas se puedan pintar en gris.                                                                                                                                                                                                                                                                                 |
| [**WM \_ ERASEBNDAND**](/windows/desktop/winmsg/wm-erasebkgnd)         | Borra el fondo de un cuadro de lista. Si el cuadro de lista tiene el estilo L [**BS \_ OWNERDRAW,**](button-styles.md) el fondo no se borra.                                                                                                                                                                                                                   |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | Devuelve DLGC \_ WANTARROWS \| DLGC \_ WANTCHARS, [**\_**](/windows/desktop/inputdev/wm-char) lo que indica que el procedimiento del cuadro de lista predeterminado procesa las teclas de dirección y los mensajes CHAR de WM.                                                                                                                                                                                                      |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Devuelve un identificador a la fuente actual del cuadro de lista.                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ HSCROLL**](wm-hscroll.md)                  | Desplaza horizontalmente el cuadro de lista.                                                                                                                                                                                                                                                                                                                                       |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)             | Procesa las claves virtuales para el desplazamiento. La clave virtual es el índice del elemento al que se va a mover el elemento de referencia. La selección no cambia.                                                                                                                                                                                                                                       |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)         | Desactiva el caret y lo destruye. Envía un código de notificación KILLFOCUS de [ \_ LBN](lbn-killfocus.md) al propietario del cuadro de lista.                                                                                                                                                                                                                                        |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) | Realiza un seguimiento del mouse en el área de cliente del cuadro de lista. Esto permite al usuario cancelar una selección si el botón del mouse se libera fuera del área de cliente del cuadro de lista.                                                                                                                                                                                                              |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | Realiza un seguimiento del mouse en el área de cliente del cuadro de lista. Esto permite al usuario cancelar una selección si el botón del mouse se libera fuera del área de cliente del cuadro de lista.                                                                                                                                                                                                              |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)         | Realiza un seguimiento del mouse en el área de cliente del cuadro de lista. Esto permite al usuario cancelar una selección si el botón del mouse se libera fuera del área de cliente del cuadro de lista.                                                                                                                                                                                                              |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)         | Realiza un seguimiento del mouse en el área de cliente del cuadro de lista. Esto permite al usuario cancelar una selección si el botón del mouse se libera fuera del área de cliente del cuadro de lista.                                                                                                                                                                                                              |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                      | Realiza una operación de pintura con subclases mediante el identificador del cuadro de lista para el contexto del dispositivo (DC).                                                                                                                                                                                                                                                                           |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)           | Activa el icono de inserción y envía un código [de notificación \_ SETFOCUS](lbn-setfocus.md) de LBN al propietario del cuadro de lista.                                                                                                                                                                                                                                                        |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | Establece una nueva fuente para el cuadro de lista.                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw)              | Establece o borra la marca de volver a dibujar según el valor *de wParam*.                                                                                                                                                                                                                                                                                                           |
| [**TAMAÑO \_ DE WM**](/windows/desktop/winmsg/wm-size)                     | Cambia el tamaño del cuadro de lista a un número entero de elementos.                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ VSCROLL**](wm-vscroll.md)                  | Desplaza el cuadro de lista verticalmente.                                                                                                                                                                                                                                                                                                                                         |



 

El procedimiento del cuadro de lista predefinido pasa todos los demás mensajes [**a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para su procesamiento predeterminado.

## <a name="owner-drawn-list-boxes"></a>Owner-Drawn cuadros de lista

Una aplicación puede crear un cuadro *de lista dibujado* por el propietario para asumir la responsabilidad de pintar elementos de lista. La ventana primaria o el cuadro de diálogo de un cuadro de lista dibujado por el propietario (su *propietario)* recibe mensajes [**\_ DRAWITEM**](wm-drawitem.md) de WM cuando es necesario pintar una parte del cuadro de lista. Un cuadro de lista dibujado por el propietario puede enumerar información que no sea cadenas de texto o además de estas.

El propietario de un cuadro de lista dibujado por el propietario debe procesar el [**mensaje \_ DRAWITEM de WM.**](wm-drawitem.md) Este mensaje se envía siempre que se debe volver a dibujar una parte del cuadro de lista. Es posible que el propietario tenga que procesar otros mensajes, en función de los estilos especificados para el cuadro de lista.

Una aplicación puede crear un cuadro de lista dibujado por el propietario especificando el estilo [**LBS \_ OWNERDRAWFIXED**](list-box-styles.md) [**o LBS \_ OWNERDRAWVARIABLE.**](list-box-styles.md) Si todos los elementos de lista del cuadro de lista tienen el mismo alto, como cadenas o iconos, una aplicación puede usar el estilo **\_ LBS OWNERDRAWFIXED.** Si los elementos de lista tienen un alto variable (por ejemplo, mapas de bits de diferente tamaño), una aplicación puede usar el estilo **\_ LBS OWNERDRAWVARIABLE.**

El propietario de un cuadro de lista dibujado por el propietario puede procesar un [**mensaje \_ MEASUREITEM**](wm-measureitem.md) de WM para especificar las dimensiones de los elementos de lista. Si la aplicación crea el cuadro de lista con el estilo [**LBS \_ OWNERDRAWFIXED,**](list-box-styles.md) el sistema envía el **mensaje \_ MEASUREITEM de WM** solo una vez. Las dimensiones especificadas por el propietario se usan para todos los elementos de lista. Si se [**usa el estilo LBS \_ OWNERDRAWVARIABLE,**](list-box-styles.md) el sistema envía un mensaje **WM \_ MEASUREITEM** para cada elemento de lista que se agrega al cuadro de lista. El propietario puede determinar o establecer el alto de un elemento de lista en cualquier momento mediante los mensajes [**\_ LB GETITEMHEIGHT**](lb-getitemheight.md) y [**LB \_ SETITEMHEIGHT,**](lb-setitemheight.md) respectivamente.

Si la información mostrada en un cuadro de lista dibujado por el propietario incluye texto, una aplicación puede realizar un seguimiento del texto de cada elemento de lista especificando el estilo [**\_ HASSTRINGS de LBS.**](list-box-styles.md) Los cuadros de lista con [**el estilo SORT \_ de LBS**](list-box-styles.md) se ordenan en función de este texto. Si un cuadro de lista está ordenado, pero no es del estilo **\_ HASSTRINGS de LBS,** el propietario debe procesar el [**mensaje \_ COMPAREITEM de WM.**](wm-compareitem.md)

En un cuadro de lista dibujado por el propietario, el propietario debe realizar un seguimiento de los elementos de lista que contienen información que no sea o además del texto. Una manera cómoda de hacerlo es guardar el identificador en la información como datos de elemento mediante el mensaje [**\_ LB SETITEMDATA.**](lb-setitemdata.md) Para liberar objetos de datos asociados a elementos de un cuadro de lista, el propietario puede procesar el [**mensaje \_ DELETEITEM de WM.**](wm-deleteitem.md)

Para obtener un ejemplo de un cuadro de lista dibujado por el propietario, vea [How to Create an Owner-Drawn List Box](create-an-owner-drawn-list-box.md).

## <a name="drag-list-boxes"></a>Arrastrar cuadros de lista

Un cuadro de lista de arrastre es un tipo especial de cuadro de lista que permite al usuario arrastrar elementos de una posición a otra. Una aplicación puede usar un cuadro de lista de arrastrar para mostrar cadenas en una secuencia determinada y permitir que el usuario cambie la secuencia arrastrando los elementos a su posición.

### <a name="creating-drag-list-boxes"></a>Crear cuadros de lista de arrastre

Los cuadros de lista de arrastre tienen los mismos estilos de ventana y procesan los mismos mensajes que los cuadros de lista estándar. Para crear un cuadro de lista de arrastre, cree primero un cuadro de lista estándar y, a continuación, llame a la [**función MakeDragList.**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) Para convertir un cuadro de lista de un cuadro de diálogo en un cuadro de lista de arrastre, puede llamar a **MakeDragList** cuando se procese el mensaje WM \_ INITDIALOG.

### <a name="drag-list-box-messages"></a>Arrastrar mensajes de cuadro de lista

Un cuadro de lista de arrastre notifica a la ventana primaria los eventos de arrastre enviándole un mensaje de lista de arrastre. La ventana primaria debe procesar el mensaje de la lista de arrastre.

El cuadro de lista de arrastre registra este mensaje cuando se llama a la función [**MakeDragList.**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) Para recuperar el identificador de mensaje (valor numérico) del mensaje de la lista de arrastre, llame a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) y especifique el valor DRAGLISTMSGSTRING.

El *parámetro wParam* del mensaje de la lista de arrastre es el identificador de control del cuadro de lista de arrastre. El *parámetro lParam* es la dirección de una estructura [**DRAGLISTINFO,**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contiene el código de notificación para el evento de arrastre y otra información. El valor devuelto del mensaje depende de la notificación.

### <a name="drag-list-box-notification-codes"></a>Códigos de notificación de cuadro de lista de arrastre

El código de notificación de la lista de arrastre, identificado por el miembro **uNotification** de la estructura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) incluida con el mensaje de la lista de arrastre, puede ser [DL \_ BEGINDRAG,](dl-begindrag.md) [DL \_ DRAGGING,](dl-dragging.md) [DL \_ CANCELDRAG](dl-canceldrag.md)o [DL \_ DROPPED.](dl-dropped.md)

El [código de notificación \_ BEGINDRAG](dl-begindrag.md) de DL se envía cuando el cursor está en un elemento de lista y el usuario hace clic en el botón izquierdo del mouse. La ventana primaria puede devolver **TRUE para** iniciar la operación de arrastre o **FALSE** para no permitir el arrastre. De esta manera, la ventana primaria puede habilitar el arrastre para algunos elementos de lista y deshabilitarlo para otros. Puede determinar qué elemento de lista se encuentra en la ubicación especificada mediante la [**función LBItemFromPt.**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt)

Si el arrastre está en vigor, el código de notificación [ \_ DL DRAGGING](dl-dragging.md) se envía cada vez que se mueve el mouse, o a intervalos regulares si no se mueve el mouse. La ventana primaria debe determinar primero el elemento de lista bajo el cursor mediante [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) y, a continuación, dibujar el icono de inserción mediante la [**función DrawInsert.**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) Al especificar **TRUE para** el parámetro *bAutoScroll* de **LBItemFromPt**, puede hacer que el cuadro de lista se desplace por una línea si el cursor está por encima o debajo de su área de cliente. El valor devuelto para esta notificación especifica el tipo de cursor del mouse que debe establecer el cuadro de lista de arrastre.

El [código de notificación \_ CANCELDRAG de DL](dl-canceldrag.md) se envía si el usuario cancela una operación de arrastrar haciendo clic en el botón derecho del mouse o presionando la tecla ESC. El código de notificación [ \_ DL DROPPED](dl-dropped.md) se envía si el usuario completa una operación de arrastre al soltar el botón izquierdo del mouse, incluso si el cursor no está sobre un elemento de lista. El cuadro de lista de arrastre libera la captura del mouse antes de enviar una notificación. Se omite el valor devuelto de estas dos notificaciones. Arrastrar lista

 

