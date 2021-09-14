---
title: Acerca de los controles de encabezado
description: Un control de encabezado es una ventana que normalmente se coloca encima de las columnas de texto o números. Contiene un título para cada columna y se puede dividir en partes.
ms.assetid: b464fb9a-e342-4209-ba6f-15b5388f3914
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d9beaa9dc3bd8eb94d749ec271902a480b853e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061931"
---
# <a name="about-header-controls"></a>Acerca de los controles de encabezado

Un control de encabezado es una ventana que normalmente se coloca encima de las columnas de texto o números. Contiene un título para cada columna y se puede dividir en partes. El usuario puede arrastrar los divisores que separan las partes para establecer el ancho de cada columna. En la ilustración siguiente se muestra un control de encabezado que tiene columnas etiquetadas que dan información detallada sobre los archivos de un directorio.

![captura de pantalla de un cuadro de diálogo con un control de encabezado de tres columnas](images/header.png)

Puede crear un control de encabezado mediante la función [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) especificando la clase de ventana [**\_ WC HEADER**](common-control-window-classes.md) y los estilos de control de encabezado [adecuados.](header-control-styles.md) Esta clase de ventana se registra cuando se carga el archivo DLL de control común. Para asegurarse de que se carga este archivo DLL, use la [**función InitCommonControlsEx.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) Después de crear un control de encabezado, puede dividirlo en partes, establecer el texto de cada parte y controlar la apariencia de la ventana mediante mensajes de ventana de encabezado.

Un control de encabezado se puede crear como una ventana secundaria de otro control, como un cuadro de lista. Sin embargo, el control primario no es consciente del control de encabezado y no permite el espacio ocupado por el encabezado, con el resultado de que los elementos de lista aparecerán detrás del encabezado. Si desea usar un control de encabezado en un cuadro de lista u otro control, el control primario debe dibujarse como propietario para que todos los elementos se muestren en la posición correcta.

Los controles de vista de lista ya tienen controles de encabezado. En lugar de crear un control de encabezado para un control de vista de lista, use [**LVM \_ GETHEADER**](lvm-getheader.md) o [**ListView \_ GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) para recuperar el control existente.

-   [Tamaño y posición del control de encabezado](#header-control-size-and-position)
-   [Elementos](#items)
-   [Controles de encabezado dibujados por el propietario](#owner-drawn-header-controls)
-   [Filtros de control de encabezado](#header-control-filters)
-   [Procesamiento de mensajes de control de encabezado predeterminado](#default-header-control-message-processing)

## <a name="header-control-size-and-position"></a>Tamaño y posición del control de encabezado

Normalmente, debe establecer el tamaño y la posición de un control de encabezado para que quepa dentro de los límites de un rectángulo determinado, como el área de cliente de una ventana. Mediante el mensaje [**DISEÑO \_ de HDM,**](hdm-layout.md) puede recuperar los valores de tamaño y posición adecuados del control de encabezado.

Al enviar [**HDM \_ LAYOUT**](hdm-layout.md), se especifica la dirección de una estructura [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) que contiene las coordenadas del rectángulo que va a ocupar el control de encabezado y proporciona un puntero a una [**estructura WINDOWPOS.**](/windows/win32/api/winuser/ns-winuser-windowpos) El control rellena la estructura **WINDOWPOS** con valores de tamaño y posición adecuados para colocar el control en la parte superior del rectángulo especificado. El valor de alto es la suma de las alturas de los bordes horizontales del control y el alto medio de los caracteres de la fuente seleccionada actualmente en el contexto del dispositivo del control.

Si desea usar [**HDM \_ LAYOUT**](hdm-layout.md) para establecer el tamaño inicial y la posición de un control de encabezado, establezca el estado de visibilidad inicial del control para que esté oculto. Después de **enviar HDM \_ LAYOUT** para recuperar los valores de tamaño y posición, puede usar la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para establecer el nuevo estado de tamaño, posición y visibilidad.

## <a name="items"></a>Elementos

Normalmente, un control de encabezado tiene varios elementos de encabezado que definen las columnas del control. Para agregar un elemento a un control de encabezado, envíe el [**mensaje \_ INSERTITEM**](hdm-insertitem.md) de HDM al control . El mensaje incluye la dirección de una [**estructura HDITEM.**](/windows/win32/api/commctrl/ns-commctrl-hditema) Esta estructura define las propiedades del elemento de encabezado, que puede incluir una cadena, una imagen de mapa de bits, un tamaño inicial y un valor **LPARAM** definido por la aplicación.

El **miembro fmt** de la estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) de un elemento puede incluir la marca **HDF \_ STRING** o **HDF \_ BITMAP** para indicar si el control muestra la cadena o el mapa de bits del elemento. Si desea mostrar una cadena y un mapa de bits, cree un elemento dibujado por el propietario estableciendo el **miembro fmt** para incluir la marca **\_ OWNERDRAW de HDF.** La **estructura HDITEM** también especifica marcas de formato que le indican al control si se debe centrar, alinear a la izquierda o alinear a la derecha la cadena o el mapa de bits en el rectángulo del elemento.

[**HDM \_ INSERTITEM**](hdm-insertitem.md) devuelve el índice del elemento recién agregado. Puede usar el índice en otros mensajes para establecer propiedades o recuperar información sobre el elemento. Puede eliminar un elemento mediante el mensaje [**\_ DELETEITEM de HDM,**](hdm-deleteitem.md) especificando el índice del elemento que se va a eliminar.

Puede usar el mensaje [**\_ SETITEM**](hdm-setitem.md) de HDM para establecer las propiedades de un elemento de encabezado existente y el mensaje [**\_ GETITEM**](hdm-getitem.md) de HDM para recuperar las propiedades actuales de un elemento. Para recuperar un recuento de los elementos de un control de encabezado, use el [**mensaje \_ GETITEMCOUNT de HDM.**](hdm-getitemcount.md)

## <a name="owner-drawn-header-controls"></a>Owner-Drawn de encabezado

Puede definir elementos individuales de un control de encabezado para que sean elementos dibujados por el propietario. El uso de esta técnica proporciona más control del que tendría sobre la apariencia de un elemento de encabezado.

Puede usar el mensaje [**\_ INSERTITEM**](hdm-insertitem.md) de HDM para insertar un nuevo elemento dibujado por el propietario en un control de encabezado o el mensaje [**\_ SETITEM**](hdm-setitem.md) de HDM para cambiar un elemento existente a un elemento dibujado por el propietario. Ambos mensajes incluyen la dirección de una [**estructura HDITEM,**](/windows/win32/api/commctrl/ns-commctrl-hditema) que debe tener el **miembro fmt** establecido en el **valor \_ OWNERDRAW de HDF.**

Cuando un control de encabezado debe dibujar un elemento dibujado por el propietario, envía el [**mensaje \_ DRAWITEM**](wm-drawitem.md) de WM a la ventana primaria. El *parámetro wParam* del mensaje es el identificador de ventana secundario del control de encabezado y el parámetro *lParam* es una dirección de una [**estructura DRAWITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) La ventana primaria usa la información de la estructura para dibujar el elemento. Para un elemento dibujado por el propietario en un control de encabezado, la **estructura DRAWITEMSTRUCT** contiene la siguiente información.



| Miembro         | Descripción                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | [**ODT \_ Tipo de**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) control dibujado por el propietario HEADER.                                                                                        |
| **CtlID**      | Identificador de ventana secundaria del control de encabezado.                                                                                                         |
| **Itemid**     | Índice del elemento que se va a dibujar.                                                                                                                         |
| **itemAction** | [**ODA \_ DrawENTIRE**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) marca de acción de dibujo.                                                                                         |
| **itemState**  | [**ODS \_ Marca**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) de acción de dibujo SELECCIONADA si el cursor está en el elemento y el botón del mouse está abajo. De lo contrario, este miembro es cero. |
| **hwndItem**   | Identificador del control de encabezado.                                                                                                                          |
| **Hdc**        | Identificador del contexto de dispositivo del control de encabezado.                                                                                                    |
| **rcItem**     | Coordenadas del elemento de encabezado que se va a dibujar. Las coordenadas son relativas a la esquina superior izquierda del control de encabezado.                               |
| **itemData**   | Valor de 32 bits definido por la aplicación asociado al elemento.                                                                                             |



 

## <a name="header-control-filters"></a>Filtros de control de encabezado

Al especificar el estilo de [**ventana DE HDS \_ FILTERBAR**](header-control-styles.md) para un control de encabezado, puede habilitar la colocación de los cuadros de edición de filtro debajo de los encabezados de columna. Aparece un botón de filtro junto al cuadro de edición. Puede implementar el filtrado respondiendo a los códigos de notificación [ \_ HDN BEGINFILTEREDIT,](hdn-beginfilteredit.md) [HDN \_ ENDFILTEREDIT,](hdn-endfilteredit.md) [HDN \_ FILTERBTNCLICK](hdn-filterbtnclick.md)o [HDN \_ FILTERCHANGE.](hdn-filterchange.md)

De forma predeterminada, el cuadro de edición contiene un mensaje para que el usuario escriba texto. Puede restaurar el cuadro de edición a este estado predeterminado mediante [**Header \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) o [**Header \_ ClearAllFilters.**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)

En el ejemplo de código siguiente se muestra cómo recuperar el control de encabezado de un control de vista de lista y agregar una barra de filtro.


```
// hList is the HWND of the list-view control.
HWND hHeader = ListView_GetHeader(hList);
LONG_PTR styles = GetWindowLongPtr(hHeader, GWL_STYLE);
SetWindowLongPtr(g_hHeader, GWL_STYLE, styles | HDS_FILTERBAR);
```



## <a name="default-header-control-message-processing"></a>Procesamiento de mensajes de control de encabezado predeterminado

En esta sección se describen los mensajes de ventana que controla el procedimiento de ventana para la [**clase de ventana WC \_ HEADER.**](common-control-window-classes.md)



| Message                                            | Procesamiento realizado                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                 | Inicializa el control de encabezado.                                                                                                                                                                                                                                                                               |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)               | Desinicializa el control de encabezado.                                                                                                                                                                                                                                                                             |
| [**WM \_ ERASEBNDAND**](/windows/desktop/winmsg/wm-erasebkgnd)         | Rellena el fondo del control de encabezado con el color de fondo actual del control.                                                                                                                                                                                                                      |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | Devuelve una combinación de los valores [**\_ WANTTAB y**](/windows/desktop/dlgbox/wm-getdlgcode) [**DLGC \_ WANTARROWS de DLGC.**](/windows/desktop/dlgbox/wm-getdlgcode)                                                                                                                     |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Devuelve el identificador a la fuente actual, que usa el control de encabezado para dibujar su texto.                                                                                                                                                                                                                 |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) | Captura la entrada del mouse. Si el cursor del mouse está en un divisor, el control envía el código de [notificación \_ BEGINTRACK](hdn-begintrack.md) de HDN y comienza a arrastrar el divisor. Si el cursor está en un elemento, el elemento se muestra en estado presionado.                                                            |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | Igual que el [**mensaje \_ WM LBUTTONDBLCLK.**](/windows/desktop/inputdev/wm-lbuttondblclk)                                                                                                                                                                                                                                       |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)         | Libera la captura del mouse. Si el control estaba siguiendo el movimiento del mouse, envía el código de [notificación \_ ENDTRACK](hdn-endtrack.md) de HDN y vuelve a dibujar el control de encabezado. De lo contrario, el control envía el código [de notificación \_ ITEMCLICK](hdn-itemclick.md) de HDN y vuelve a dibujar el elemento de encabezado en el que se hizo clic. |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)         | Si se arrastra un divisor, el control envía el código de notificación [ \_ HDN TRACK](hdn-track.md) y muestra el elemento en la nueva posición. Si el botón izquierdo del mouse está fuera de servicio y el cursor está en un elemento, el elemento se muestra en estado presionado.                                                      |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)             | Asigna e inicializa una estructura de datos interna.                                                                                                                                                                                                                                                         |
| [**WM \_ NCDESTROY**](/windows/desktop/winmsg/wm-ncdestroy)           | Libera los recursos asignados por el control de encabezado después de que se desinicialice el control de encabezado.                                                                                                                                                                                                                |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                      | Pinta la región no válida del control de encabezado. Si el *parámetro wParam* no es NULL, el control supone que el valor es un HDC y pinta con ese contexto de dispositivo.                                                                                                                                    |
| [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor)           | Establece la forma del cursor, en función de si el cursor está en un divisor o en un elemento de encabezado.                                                                                                                                                                                                                   |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | Selecciona un nuevo identificador de fuente en el contexto del dispositivo para el control de encabezado.                                                                                                                                                                                                                                     |



 

 

 