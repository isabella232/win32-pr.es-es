---
title: Acerca de los cuadros de lista
description: En esta sección se describen las características del cuadro de lista.
ms.assetid: 359bb363-5b97-4e0c-bdc4-bfa6a6504a76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674712226a79960e44ab99ed8e59c88b27984efb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488326"
---
# <a name="about-list-boxes"></a>Acerca de los cuadros de lista

Un control de cuadro de lista contiene una lista simple en la que el usuario puede seleccionar normalmente uno o varios elementos. Los cuadros de lista proporcionan una flexibilidad limitada en comparación con los controles de [vista de lista](list-view-control-reference.md) .

Los elementos de cuadro de lista se pueden representar mediante cadenas de texto, mapas de bits o ambos. Si el cuadro de lista no es lo suficientemente grande como para mostrar todos los elementos del cuadro de lista a la vez, el cuadro de lista proporciona una barra de desplazamiento. El usuario se desplaza por los elementos del cuadro de lista y aplica o quita el estado de selección según sea necesario. Al seleccionar un elemento de cuadro de lista, se cambia su apariencia visual, normalmente cambiando el texto y los colores de fondo a los especificados por las métricas del sistema operativo pertinentes. Cuando el usuario selecciona o anula la selección de un elemento, el sistema envía un mensaje de notificación a la ventana primaria del cuadro de lista.

En el caso de una aplicación ANSI, el sistema convierte el texto de un cuadro de lista en Unicode mediante la página de códigos **CP \_ ACP** . Esto puede causar problemas. Por ejemplo, los caracteres romanos acentuados en un cuadro de lista no Unicode de Windows, la versión en japonés se verá distorsionada. Para solucionar este error, compile la aplicación como Unicode o use un cuadro de lista dibujado por el propietario.

En esta sección se tratan los temas siguientes:

-   [Crear un cuadro de lista](#creating-a-list-box)
-   [Tipos y estilos de cuadros de lista](#list-box-types-and-styles)
-   [Funciones de cuadro de lista](#list-box-functions)
-   [Mensajes de notificación de cuadros de lista](#notification-messages-from-list-boxes)
-   [Mensajes a cuadros de lista](#notification-messages-from-list-boxes)
-   [Procesamiento de mensajes de ventana predeterminado](#default-window-message-processing)
-   [Cuadros de lista dibujados por el propietario](#owner-drawn-list-boxes)
-   [Arrastrar cuadros de lista](#drag-list-boxes)
    -   [Crear cuadros de lista de arrastre](#creating-drag-list-boxes)
    -   [Arrastrar mensajes de cuadro de lista](#drag-list-box-messages)
    -   [Arrastrar códigos de notificación de cuadro de lista](#drag-list-box-notification-codes)

## <a name="creating-a-list-box"></a>Crear un cuadro de lista

La forma más fácil de crear un cuadro de lista en un cuadro de diálogo es arrastrarlo desde el cuadro de herramientas en Microsoft Visual Studio hasta el recurso del cuadro de diálogo. Para crear dinámicamente un cuadro de lista o para crear un cuadro de lista en una ventana que no sea un cuadro de diálogo, use la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando la clase de ventana de cuadro de lista [**CT \_**](common-control-window-classes.md) y los estilos de cuadro de [lista](list-box-styles.md)adecuados.

## <a name="list-box-types-and-styles"></a>Tipos y estilos de cuadros de lista

Hay dos tipos de cuadros de lista: selección única (valor predeterminado) y selección múltiple. En un cuadro de lista de selección única, el usuario solo puede seleccionar un elemento cada vez. En un cuadro de lista de selección múltiple, el usuario puede seleccionar más de un elemento a la vez. Para crear un cuadro de lista de selección múltiple, especifique el estilo [**lbs \_ MULTIPLESEL**](list-box-styles.md) o [**lb \_ EXTENDEDSEL**](list-box-styles.md) .

La apariencia y el funcionamiento de un cuadro de lista se controlan mediante [estilos de cuadro de lista](list-box-styles.md) y estilos de ventana. Estos estilos indican si la lista está ordenada, organizada en varias columnas, dibujada por la aplicación, etc. Las dimensiones y los estilos de un cuadro de lista se definen normalmente en una plantilla de cuadro de diálogo que se incluye en los recursos de una aplicación.

> [!Note]  
> Para usar estilos visuales con estos controles, una aplicación debe incluir un manifiesto y debe llamar a [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) al principio del programa. Para obtener información sobre los estilos visuales, vea [estilos visuales](themes-overview.md). Para obtener información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="list-box-functions"></a>Funciones de cuadro de lista

La función [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) reemplaza el contenido de un cuadro de lista con los nombres de las unidades, directorios y archivos que coinciden con un conjunto de criterios especificado. La función [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) recupera la selección actual de un cuadro de lista que inicializa **DlgDirList**. Estas funciones permiten al usuario seleccionar una unidad, un directorio o un archivo de un cuadro de lista sin escribir la ubicación y el nombre del archivo.

Además, la función [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) devuelve el número de elementos por columna de un cuadro de lista especificado.

## <a name="notification-messages-from-list-boxes"></a>Mensajes de notificación de cuadros de lista

Cuando se produce un evento en un cuadro de lista, el cuadro de lista envía un código de notificación, en forma de mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) , al procedimiento de cuadro de diálogo de la ventana propietaria. Los códigos de notificación del cuadro de lista se envían cuando un usuario selecciona, hace doble clic o cancela un elemento del cuadro de lista. Cuando el cuadro de lista recibe o pierde el foco de teclado; y cuando el sistema no puede asignar suficiente memoria para una solicitud de cuadro de lista. Un mensaje de **\_ comando de WM** contiene el identificador del cuadro de lista en la palabra de orden inferior del parámetro *wParam* y el código de notificación en la palabra de orden superior. El parámetro *lParam* contiene el identificador de la ventana de control.

No es necesario un procedimiento de cuadro de diálogo para procesar estos mensajes; el procedimiento de ventana predeterminado los procesa.

Una aplicación debe supervisar y procesar los siguientes códigos de notificación de cuadro de lista.



| Código de notificación                   | Descripción                                                      |
|-------------------------------------|------------------------------------------------------------------|
| [LBN \_ DBLCLK](lbn-dblclk.md)       | El usuario hace doble clic en un elemento del cuadro de lista.                  |
| [LBN \_ ERRSPACE](lbn-errspace.md)   | El cuadro de lista no puede asignar suficiente memoria para satisfacer una solicitud. |
| [LBN \_ KILLFOCUS](lbn-killfocus.md) | El cuadro de lista pierde el foco de teclado.                           |
| [LBN \_ SELCANCEL](lbn-selcancel.md) | El usuario cancela la selección de un elemento en el cuadro de lista.       |
| [LBN \_ SELCHANGE](lbn-selchange.md) | La selección de un cuadro de lista está a punto de cambiar.                  |
| [LBN ( \_ SETFOCUS)](lbn-setfocus.md)   | El cuadro de lista recibe el foco de teclado.                        |



 

## <a name="messages-to-list-boxes"></a>Mensajes a cuadros de lista

Un procedimiento de cuadro de diálogo puede enviar mensajes a un cuadro de lista para agregar, eliminar, examinar y cambiar elementos del cuadro de lista. Por ejemplo, un procedimiento de cuadro de diálogo puede enviar un mensaje de [**lb \_ ADDSTRING**](lb-addstring.md) a un cuadro de lista para agregar un elemento, y un mensaje de [**lb \_ GETSEL**](lb-getsel.md) para determinar si el elemento está seleccionado. Otros mensajes establecen y recuperan información sobre el tamaño, la apariencia y el comportamiento del cuadro de lista. Por ejemplo, el mensaje [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) establece el ancho desplazable de un cuadro de lista. Un procedimiento de cuadro de diálogo puede enviar cualquier mensaje a un cuadro de lista mediante la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) .

A menudo se hace referencia a un elemento de cuadro de lista mediante su *Índice*, un entero que representa la posición del elemento en el cuadro de lista. El índice del primer elemento de un cuadro de lista es 0, el índice del segundo elemento es 1 y así sucesivamente.

En la tabla siguiente se describe cómo el procedimiento de cuadro de lista predefinido responde a los mensajes de cuadro de lista.



| Message                                                   | Response                                                                                                                                                                                                                         |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LB \_ ADDFILE**](lb-addfile.md)                         | Inserta un archivo en un cuadro de lista de directorios que está rellenado por la función [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) y recupera el índice del cuadro de lista del elemento insertado.                                                                  |
| [**LB \_ ADDSTRING**](lb-addstring.md)                     | Agrega una cadena a un cuadro de lista y devuelve su índice.                                                                                                                                                                               |
| [**LB \_ DELETESTRING**](lb-deletestring.md)               | Quita una cadena de un cuadro de lista y devuelve el número de cadenas que permanecen en la lista.                                                                                                                                      |
| [**DIR de LB \_**](lb-dir.md)                                 | Agrega una lista de nombres de archivo a un cuadro de lista y devuelve el índice del último nombre de archivo agregado.                                                                                                                                       |
| [**LB \_ FINDSTRING**](lb-findstring.md)                   | Devuelve el índice de la primera cadena del cuadro de lista que comienza con una cadena especificada.                                                                                                                                       |
| [**LB \_ FindExactString con**](lb-findstringexact.md)         | Devuelve el índice de la cadena en el cuadro de lista que es igual a una cadena especificada.                                                                                                                                             |
| [**LB \_ GETANCHORINDEX**](lb-getanchorindex.md)           | Devuelve el índice del elemento que seleccionó el mouse por última vez.                                                                                                                                                                      |
| [**LB \_ GETCARETINDEX**](lb-getcaretindex.md)             | Devuelve el índice del elemento que tiene el rectángulo de foco.                                                                                                                                                                      |
| [**LB \_ GETCOUNT**](lb-getcount.md)                       | Devuelve el número de elementos del cuadro de lista.                                                                                                                                                                                     |
| [**LB \_ GETCURSEL**](lb-getcursel.md)                     | Devuelve el índice del elemento actualmente seleccionado.                                                                                                                                                                                |
| [**LB \_ GETHORIZONTALEXTENT**](lb-gethorizontalextent.md) | Devuelve el ancho desplazable, en píxeles, de un cuadro de lista.                                                                                                                                                                          |
| [**LB \_ GETITEMDATA**](lb-getitemdata.md)                 | Devuelve el valor asociado al elemento especificado.                                                                                                                                                                    |
| [**LB \_ GETITEMHEIGHT**](lb-getitemheight.md)             | Devuelve el alto, en píxeles, de un elemento de un cuadro de lista.                                                                                                                                                                         |
| [**LB \_ GETITEMRECT**](lb-getitemrect.md)                 | Recupera las coordenadas de cliente del elemento de cuadro de lista especificado.                                                                                                                                                                 |
| [**equilibro \_ de lb**](lb-getlocale.md)                     | Recupera la configuración regional del cuadro de lista. La palabra de orden superior contiene el código de país o región y la palabra de orden inferior contiene el identificador de idioma.                                                                              |
| [**LB \_ GETSEL**](lb-getsel.md)                           | Devuelve el estado de selección de un elemento de cuadro de lista.                                                                                                                                                                                  |
| [**LB \_ GETSELCOUNT**](lb-getselcount.md)                 | Devuelve el número de elementos seleccionados en un cuadro de lista de selección múltiple.                                                                                                                                                           |
| [**LB \_ GETSELITEMS**](lb-getselitems.md)                 | Crea una matriz de los índices de todos los elementos seleccionados en un cuadro de lista de selección múltiple y devuelve el número total de elementos seleccionados.                                                                                           |
| [**\_apgettext GETTEXT**](lb-gettext.md)                         | Recupera la cadena asociada a un elemento especificado y la longitud de la cadena.                                                                                                                                              |
| [**LB \_ GETTEXTLEN**](lb-gettextlen.md)                   | Devuelve la longitud, en caracteres, de la cadena asociada a un elemento especificado.                                                                                                                                               |
| [**LB \_ GETTOPINDEX**](lb-gettopindex.md)                 | Devuelve el índice del primer elemento visible de un cuadro de lista.                                                                                                                                                                       |
| [**' LB \_ INITSTORAGE**](lb-initstorage.md)                 | Asigna memoria para el número especificado de elementos y sus cadenas asociadas.                                                                                                                                                 |
| [**LB \_ INSERTSTRING**](lb-insertstring.md)               | Inserta una cadena en el índice especificado de un cuadro de lista.                                                                                                                                                                             |
| [**LB \_ ITEMFROMPOINT**](lb-itemfrompoint.md)             | Recupera el índice de base cero del elemento más próximo al punto especificado en un cuadro de lista.                                                                                                                                            |
| [**LB \_ RESETCONTENT**](lb-resetcontent.md)               | Quita todos los elementos de un cuadro de lista.                                                                                                                                                                                               |
| [**LB \_ SELECTSTRING**](lb-selectstring.md)               | Selecciona la primera cadena que encuentra que coincide con un prefijo especificado.                                                                                                                                                               |
| [**LB \_ SELITEMRANGE**](lb-selitemrange.md)               | Selecciona un intervalo de elementos especificado en un cuadro de lista.                                                                                                                                                                                |
| [**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md)           | Selecciona un intervalo de elementos especificado si el índice del primer elemento del intervalo es menor que el índice del último elemento del intervalo. Cancela la selección del intervalo si el índice del primer elemento es mayor que el último. |
| [**LB \_ SETANCHORINDEX**](lb-setanchorindex.md)           | Establece el elemento que el mouse seleccionó por última vez en un elemento especificado.                                                                                                                                                                  |
| [**LB \_ SETCARETINDEX**](lb-setcaretindex.md)             | Establece el rectángulo de foco en un elemento de cuadro de lista especificado.                                                                                                                                                                           |
| [**LB \_ SETCOLUMNWIDTH**](lb-setcolumnwidth.md)           | Establece el ancho de todas las columnas de un cuadro de lista, en píxeles.                                                                                                                                                                         |
| [**LB \_ SETCOUNT**](lb-setcount.md)                       | Establece el número de elementos de un cuadro de lista.                                                                                                                                                                                          |
| [**LB \_ SETCURSEL**](lb-setcursel.md)                     | Selecciona un elemento de cuadro de lista especificado.                                                                                                                                                                                               |
| [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) | Establece el ancho desplazable, en píxeles, de un cuadro de lista.                                                                                                                                                                             |
| [**LB \_ SETITEMDATA**](lb-setitemdata.md)                 | Asocia un valor a un elemento del cuadro de lista.                                                                                                                                                                                         |
| [**LB \_ SETITEMHEIGHT**](lb-setitemheight.md)             | Establece el alto, en píxeles, de un elemento o elementos de un cuadro de lista.                                                                                                                                                                   |
| [**LB \_ SETLOCALE**](lb-setlocale.md)                     | Establece la configuración regional de un cuadro de lista y devuelve el identificador de configuración regional anterior.                                                                                                                                                        |
| [**LB \_ SETSEL**](lb-setsel.md)                           | Selecciona un elemento en un cuadro de lista de selección múltiple.                                                                                                                                                                                |
| [**LB \_ SETTABSTOPS**](lb-settabstops.md)                 | Establece las tabulaciones en las que se especifican en una matriz especificada.                                                                                                                                                                      |
| [**LB \_ SETTOPINDEX**](lb-settopindex.md)                 | Desplaza el cuadro de lista de modo que el elemento especificado se encuentra en la parte superior del rango visible.                                                                                                                                                   |



 

## <a name="default-window-message-processing"></a>Procesamiento de mensajes de ventana predeterminado

El procedimiento de ventana de la clase de ventana de cuadro de lista predefinido lleva a cabo el procesamiento predeterminado para todos los mensajes que el cuadro de lista no procesa. Cuando el procedimiento de cuadro de lista devuelve **false** para un mensaje, el procedimiento de ventana predefinido comprueba el mensaje y realiza las acciones predeterminadas, tal como se muestra en la tabla siguiente.



| Message                                            | Acción predeterminada                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**carácter de WM \_**](/windows/desktop/inputdev/wm-char)                   | Mueve la selección al primer elemento que comienza con el carácter escrito por el usuario. Si el cuadro de lista tiene el [**estilo \_ OWNERDRAW L BS**](button-styles.md) , no se produce ninguna acción. Varios caracteres que se escriben en un intervalo corto se tratan como un grupo y se selecciona el primer elemento que comienza con esa serie de caracteres.<br/> |
| [**creación de WM \_**](/windows/desktop/winmsg/wm-create)                 | Crea un cuadro de lista vacío.                                                                                                                                                                                                                                                                                                                                               |
| [**destrucción de WM \_**](/windows/desktop/winmsg/wm-destroy)               | Destruye el cuadro de lista y libera los recursos que utiliza.                                                                                                                                                                                                                                                                                                              |
|                                                    | Pasa el mensaje al procedimiento de cuadro de diálogo o al proceso de ventana primaria.                                                                                                                                                                                                                                                                                                 |
| [**\_habilitación de WM**](/windows/desktop/winmsg/wm-enable)                 | Si el control está visible, invalida el rectángulo para que las cadenas se puedan pintar en gris.                                                                                                                                                                                                                                                                                 |
| [**ERASEBKGND de WM \_**](/windows/desktop/winmsg/wm-erasebkgnd)         | Borra el fondo de un cuadro de lista. Si el cuadro de lista tiene el [**estilo \_ OWNERDRAW L BS**](button-styles.md) , el fondo no se borra.                                                                                                                                                                                                                   |
| [**GETDLGCODE de WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)         | Devuelve DLGC \_ WANTARROWS \| DLGC \_ WANTCHARS, lo que indica que el procedimiento de cuadro de lista predeterminado procesa las teclas de dirección y los mensajes de tipo [**\_ Char de WM**](/windows/desktop/inputdev/wm-char) .                                                                                                                                                                                                      |
| [**GETFONT de WM \_**](/windows/desktop/winmsg/wm-getfont)               | Devuelve un identificador para la fuente actual del cuadro de lista.                                                                                                                                                                                                                                                                                                                   |
| [**HSCROLL de WM \_**](wm-hscroll.md)                  | Desplaza el cuadro de lista horizontalmente.                                                                                                                                                                                                                                                                                                                                       |
| [**KEYDOWN de WM \_**](/windows/desktop/inputdev/wm-keydown)             | Procesa las teclas virtuales para el desplazamiento. La clave virtual es el índice del elemento al que se va a desplace el símbolo de intercalación. No se cambia la selección.                                                                                                                                                                                                                                       |
| [**KILLFOCUS de WM \_**](/windows/desktop/inputdev/wm-killfocus)         | Desactiva el símbolo de intercalación y lo destruye. Envía un código de notificación de [LBN \_ KILLFOCUS](lbn-killfocus.md) al propietario del cuadro de lista.                                                                                                                                                                                                                                        |
| [**LBUTTONDBLCLK de WM \_**](/windows/desktop/inputdev/wm-lbuttondblclk) | Hace un seguimiento del mouse en el área de cliente del cuadro de lista. Esto permite al usuario cancelar una selección si el botón del mouse se suelta fuera del área cliente del cuadro de lista.                                                                                                                                                                                                              |
| [**LBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-lbuttondown)     | Hace un seguimiento del mouse en el área de cliente del cuadro de lista. Esto permite al usuario cancelar una selección si el botón del mouse se suelta fuera del área cliente del cuadro de lista.                                                                                                                                                                                                              |
| [**LBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-lbuttonup)         | Hace un seguimiento del mouse en el área de cliente del cuadro de lista. Esto permite al usuario cancelar una selección si el botón del mouse se suelta fuera del área cliente del cuadro de lista.                                                                                                                                                                                                              |
| [**MOUSEMOVE de WM \_**](/windows/desktop/inputdev/wm-mousemove)         | Hace un seguimiento del mouse en el área de cliente del cuadro de lista. Esto permite al usuario cancelar una selección si el botón del mouse se suelta fuera del área cliente del cuadro de lista.                                                                                                                                                                                                              |
| [**pintura de WM \_**](/windows/desktop/gdi/wm-paint)                      | Realiza una operación de dibujo de subclases usando el identificador del cuadro de lista en el contexto de dispositivo (DC).                                                                                                                                                                                                                                                                           |
| [**SETFOCUS de WM \_**](/windows/desktop/inputdev/wm-setfocus)           | Activa el símbolo de intercalación y envía un código de notificación [ \_ SETFOCUS de LBN](lbn-setfocus.md) al propietario del cuadro de lista.                                                                                                                                                                                                                                                        |
| [**WM \_**](/windows/desktop/winmsg/wm-setfont)               | Establece una nueva fuente para el cuadro de lista.                                                                                                                                                                                                                                                                                                                                        |
| [**SETREDRAW de WM \_**](/windows/desktop/gdi/wm-setredraw)              | Establece o borra la marca de volver a dibujar basada en el valor de *wParam*.                                                                                                                                                                                                                                                                                                           |
| [**tamaño de WM \_**](/windows/desktop/winmsg/wm-size)                     | Cambia el tamaño del cuadro de lista a un número entero de elementos.                                                                                                                                                                                                                                                                                                                     |
| [**VSCROLL de WM \_**](wm-vscroll.md)                  | Desplaza el cuadro de lista verticalmente.                                                                                                                                                                                                                                                                                                                                         |



 

El procedimiento de cuadro de lista predefinido pasa el resto de mensajes a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para el procesamiento predeterminado.

## <a name="owner-drawn-list-boxes"></a>Owner-Drawn cuadros de lista

Una aplicación puede crear un cuadro *de lista dibujado por el propietario* para asumir la responsabilidad de pintar los elementos de la lista. La ventana primaria o el cuadro de diálogo de un cuadro de lista dibujado por el propietario (su *propietario*) recibe mensajes de [**WM \_ DRAWITEM**](wm-drawitem.md) cuando es necesario pintar una parte del cuadro de lista. Un cuadro de lista dibujado por el propietario puede mostrar información distinta de las cadenas de texto, o además de ellas.

El propietario de un cuadro de lista dibujado por el propietario debe procesar el mensaje de la [**\_ DRAWITEM de WM**](wm-drawitem.md) . Este mensaje se envía siempre que se debe volver a dibujar una parte del cuadro de lista. Es posible que el propietario tenga que procesar otros mensajes, en función de los estilos especificados para el cuadro de lista.

Una aplicación puede crear un cuadro de lista dibujado por el propietario especificando el estilo de la lb o el de la [**lbs \_**](list-box-styles.md) . [**\_**](list-box-styles.md) Si todos los elementos de lista del cuadro de lista tienen el mismo alto, como cadenas o iconos, una aplicación puede usar el estilo **lb \_ OWNERDRAWFIXED** . Si los elementos de lista son de alto variable (por ejemplo, mapas de bits de tamaño distinto), una aplicación puede usar el estilo **lb \_ OWNERDRAWVARIABLE** .

El propietario de un cuadro de lista dibujado por el propietario puede procesar un mensaje de [**\_ MEASUREITEM de WM**](wm-measureitem.md) para especificar las dimensiones de los elementos de la lista. Si la aplicación crea el cuadro de lista con el estilo de la [**lbs- \_ OWNERDRAWFIXED**](list-box-styles.md) , el sistema envía el mensaje de **WM \_ MEASUREITEM** una sola vez. Las dimensiones especificadas por el propietario se usan para todos los elementos de lista. Si se usa el estilo [**lb \_ OWNERDRAWVARIABLE**](list-box-styles.md) , el sistema envía un mensaje de **WM \_ MEASUREITEM** para cada elemento de lista que se agrega al cuadro de lista. El propietario puede determinar o establecer el alto de un elemento de lista en cualquier momento mediante los mensajes [**lb \_ GETITEMHEIGHT**](lb-getitemheight.md) y [**lb \_ SETITEMHEIGHT**](lb-setitemheight.md) , respectivamente.

Si la información que se muestra en un cuadro de lista dibujado por el propietario incluye texto, una aplicación puede realizar un seguimiento del texto de cada elemento de la lista especificando el estilo [**lb \_ HASSTRINGS**](list-box-styles.md) . Los cuadros de lista con el estilo de [**\_ ordenación lbs**](list-box-styles.md) se ordenan en función de este texto. Si un cuadro de lista está ordenado, pero no es del estilo **lb \_ HASSTRINGS** , el propietario debe procesar el mensaje [**de \_ COMPAREITEM de WM**](wm-compareitem.md) .

En un cuadro de lista dibujado por el propietario, el propietario debe realizar un seguimiento de los elementos de la lista que contienen información que no es o además del texto. Una manera cómoda de hacerlo es guardar el identificador de la información como datos de elemento mediante el mensaje [**lb \_ SETITEMDATA**](lb-setitemdata.md) . Para liberar los objetos de datos asociados a los elementos de un cuadro de lista, el propietario puede procesar el mensaje de [**WM \_ DELETEITEM**](wm-deleteitem.md) .

Para obtener un ejemplo de un cuadro de lista dibujado por el propietario, vea [Cómo crear un Owner-Drawn cuadro de lista](create-an-owner-drawn-list-box.md).

## <a name="drag-list-boxes"></a>Arrastrar cuadros de lista

Un cuadro de lista de arrastre es un tipo especial de cuadro de lista que permite al usuario arrastrar elementos de una posición a otra. Una aplicación puede usar un cuadro de lista de arrastre para mostrar cadenas en una secuencia determinada y permitir que el usuario cambie la secuencia arrastrando los elementos a la posición.

### <a name="creating-drag-list-boxes"></a>Crear cuadros de lista de arrastre

Los cuadros de lista de arrastre tienen los mismos estilos de ventana y procesan los mismos mensajes que los cuadros de lista estándar. Para crear un cuadro de lista de arrastre, primero cree un cuadro de lista estándar y, a continuación, llame a la función [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) . Para convertir un cuadro de lista de un cuadro de diálogo en un cuadro de lista de arrastre, puede llamar a **MakeDragList** cuando \_ se procese el mensaje de INITDIALOG de WM.

### <a name="drag-list-box-messages"></a>Arrastrar mensajes de cuadro de lista

Un cuadro de lista de arrastre notifica a la ventana primaria de los eventos de arrastre mediante el envío de un mensaje de la lista de arrastre. La ventana primaria debe procesar el mensaje de la lista de arrastre.

El cuadro de lista arrastrar registra este mensaje cuando se llama a la función [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) . Para recuperar el identificador de mensaje (valor numérico) del mensaje de la lista de arrastre, llame a la función [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) y especifique el valor DRAGLISTMSGSTRING.

El parámetro *wParam* del mensaje de la lista de arrastre es el identificador del control del cuadro de lista de arrastre. El parámetro *lParam* es la dirección de una estructura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) , que contiene el código de notificación para el evento de arrastre y otra información. El valor devuelto del mensaje depende de la notificación.

### <a name="drag-list-box-notification-codes"></a>Arrastrar códigos de notificación de cuadro de lista

El código de notificación de la lista de arrastre, identificado por el miembro **uNotification** de la estructura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que se incluye con el mensaje de la lista de arrastre, puede ser [DL \_ BEGINDRAG](dl-begindrag.md), [DL \_ arrastrar](dl-dragging.md), [DL \_ CANCELDRAG](dl-canceldrag.md)o [DL \_ quitado](dl-dropped.md).

El código de notificación [DL \_ BEGINDRAG](dl-begindrag.md) se envía cuando el cursor está en un elemento de lista y el usuario hace clic en el botón primario del mouse. La ventana primaria puede devolver **true** para comenzar la operación de arrastre o **false** para no permitir el arrastre. De esta manera, la ventana primaria puede habilitar el arrastre de algunos elementos de la lista y deshabilitarlo para otros usuarios. Puede determinar qué elemento de la lista se encuentra en la ubicación especificada mediante la función [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) .

Si el arrastre está en vigor, el código de notificación de [ \_ arrastre](dl-dragging.md) de la DL se envía cuando se mueve el mouse, o a intervalos regulares si no se mueve el mouse. La ventana primaria debe determinar primero el elemento de lista bajo el cursor mediante [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) y, a continuación, dibujar el icono de inserción mediante la función [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) . Al especificar **true** para el parámetro *bAutoScroll* de **LBItemFromPt**, puede hacer que el cuadro de lista se desplace una línea si el cursor está por encima o por debajo de su área cliente. El valor que se devuelve para esta notificación especifica el tipo de cursor del mouse que debe establecer el cuadro de lista de arrastre.

El código de notificación [DL \_ CANCELDRAG](dl-canceldrag.md) se envía si el usuario cancela una operación de arrastre haciendo clic con el botón secundario del mouse o presionando la tecla ESC. El código de notificación [DL \_ quitado](dl-dropped.md) se envía si el usuario completa una operación de arrastre soltando el botón primario del mouse, incluso si el cursor no está sobre un elemento de lista. El cuadro de lista arrastrar libera la captura del mouse antes de enviar cualquier notificación. Se omite el valor devuelto de estas dos notificaciones. Arrastrar lista

 

