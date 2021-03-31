---
title: Acerca de los controles de encabezado
description: Un control de encabezado es una ventana que normalmente se coloca encima de las columnas de texto o de números. Contiene un título para cada columna y puede dividirse en partes.
ms.assetid: b464fb9a-e342-4209-ba6f-15b5388f3914
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d9beaa9dc3bd8eb94d749ec271902a480b853e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793953"
---
# <a name="about-header-controls"></a>Acerca de los controles de encabezado

Un control de encabezado es una ventana que normalmente se coloca encima de las columnas de texto o de números. Contiene un título para cada columna y puede dividirse en partes. El usuario puede arrastrar los divisores que separan los elementos para establecer el ancho de cada columna. En la ilustración siguiente se muestra un control de encabezado que tiene columnas con etiqueta que proporcionan información detallada acerca de los archivos de un directorio.

![captura de pantalla de un cuadro de diálogo con un control de encabezado de tres columnas](images/header.png)

Puede crear un control de encabezado mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando la clase de ventana de [**\_ encabezado WC**](common-control-window-classes.md) y los [estilos de control de encabezado](header-control-styles.md)adecuados. Esta clase de ventana se registra cuando se carga el archivo DLL de control común. Para asegurarse de que se carga este archivo DLL, utilice la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) . Después de crear un control de encabezado, puede dividirlo en elementos, establecer el texto de cada parte y controlar la apariencia de la ventana mediante mensajes de la ventana de encabezado.

Un control de encabezado se puede crear como una ventana secundaria de otro control, como un cuadro de lista. Sin embargo, el control primario no es consciente del control de encabezado y no permite el espacio ocupado por el encabezado, con el resultado de que los elementos de lista aparecerán detrás del encabezado. Si desea utilizar un control de encabezado en un cuadro de lista o en otro control, el control primario debe dibujarse en el propietario para que todos los elementos se muestren en la posición correcta.

Los controles de vista de lista ya tienen controles de encabezado. En lugar de crear un control de encabezado para un control de vista de lista, use [**LVM \_ getheader**](lvm-getheader.md) o [**ListView \_ getheader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) para recuperar el control existente.

-   [Tamaño y posición del control de encabezado](#header-control-size-and-position)
-   [Elementos](#items)
-   [Controles de encabezado dibujados por el propietario](#owner-drawn-header-controls)
-   [Filtros de control de encabezado](#header-control-filters)
-   [Procesamiento de mensajes de control de encabezado predeterminado](#default-header-control-message-processing)

## <a name="header-control-size-and-position"></a>Tamaño y posición del control de encabezado

Normalmente, debe establecer el tamaño y la posición de un control de encabezado para ajustarse a los límites de un rectángulo determinado, como el área de cliente de una ventana. Mediante el mensaje [**de \_ diseño HDM**](hdm-layout.md) , puede recuperar los valores de tamaño y posición adecuados del control de encabezado.

Al enviar [**el \_ diseño HDM**](hdm-layout.md), se especifica la dirección de una estructura [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) que contiene las coordenadas del rectángulo que el control de encabezado va a ocupar y proporciona un puntero a una estructura [**windowpos (**](/windows/win32/api/winuser/ns-winuser-windowpos) . El control rellena la estructura **windowpos (** con los valores de tamaño y posición adecuados para colocar el control a lo largo de la parte superior del rectángulo especificado. El valor de alto es la suma de los altos de los bordes horizontales del control y el alto medio de los caracteres de la fuente actualmente seleccionada en el contexto del dispositivo del control.

Si desea usar el [**\_ diseño de HDM**](hdm-layout.md) para establecer el tamaño y la posición iniciales de un control de encabezado, establezca el estado de visibilidad inicial del control para que esté oculto. Después de enviar el **\_ diseño de HDM** para recuperar los valores de tamaño y posición, puede usar la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para establecer el nuevo tamaño, la posición y el estado de visibilidad.

## <a name="items"></a>Elementos

Normalmente, un control de encabezado tiene varios elementos de encabezado que definen las columnas del control. Para agregar un elemento a un control de encabezado, envíe el mensaje [**\_ INSERTITEM HDM**](hdm-insertitem.md) al control. El mensaje incluye la dirección de una estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) . Esta estructura define las propiedades del elemento de encabezado, que puede incluir una cadena, una imagen de mapa de bits, un tamaño inicial y un valor **lParam** definido por la aplicación.

El miembro **FMT** de la estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) de un elemento puede incluir la marca de **mapa de \_ bits** **HDF \_ String** o HDF para indicar si el control muestra la cadena o el mapa de bits del elemento. Si desea mostrar una cadena y un mapa de bits, cree un elemento dibujado por el propietario. para ello, establezca el miembro **FMT** para que incluya la marca de **\_ OWNERDRAW HDF** . La estructura **HDITEM** también especifica marcas de formato que indican al control si centrar, alinear a la izquierda o alinear a la derecha la cadena o el mapa de bits en el rectángulo del elemento.

[**HDM \_ INSERTITEM**](hdm-insertitem.md) devuelve el índice del elemento recién agregado. Puede usar el índice en otros mensajes para establecer las propiedades o recuperar información sobre el elemento. Puede eliminar un elemento mediante el mensaje [**HDM \_ DELETEITEM**](hdm-deleteitem.md) , especificando el índice del elemento que se va a eliminar.

Puede usar el mensaje [**\_ SETITEM de HDM**](hdm-setitem.md) para establecer las propiedades de un elemento de encabezado existente y el mensaje de [**HDM \_ GETITEM**](hdm-getitem.md) para recuperar las propiedades actuales de un elemento. Para recuperar un recuento de los elementos de un control de encabezado, use el mensaje [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md) .

## <a name="owner-drawn-header-controls"></a>Owner-Drawn controles de encabezado

Puede definir elementos individuales de un control de encabezado para que sean elementos dibujados por el propietario. El uso de esta técnica le proporciona más control de lo que tendría en la apariencia de un elemento de encabezado.

Puede usar el mensaje [**HDM \_ INSERTITEM**](hdm-insertitem.md) para insertar un nuevo elemento dibujado por el propietario en un control de encabezado o el mensaje [**HDM \_ SETITEM**](hdm-setitem.md) para cambiar un elemento existente a un elemento dibujado por el propietario. Ambos mensajes incluyen la dirección de una estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) , que debe tener el miembro **FMT** establecido en el **valor \_ OWNERDRAW HDF** .

Cuando un control de encabezado debe dibujar un elemento dibujado por el propietario, envía el mensaje de Windows de [**WM \_**](wm-drawitem.md) a la ventana primaria. El parámetro *wParam* del mensaje es el identificador de la ventana secundaria del control de encabezado y el parámetro *lParam* es una dirección de una estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . La ventana primaria usa la información de la estructura para dibujar el elemento. Para un elemento dibujado por el propietario en un control de encabezado, la estructura **drawitemstruct (** contiene la información siguiente.



| Miembro         | Descripción                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | [**ODT \_**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Tipo de control dibujado por el propietario del encabezado.                                                                                        |
| **CtlID**      | Identificador de la ventana secundaria del control de encabezado.                                                                                                         |
| **ID**     | Índice del elemento que se va a dibujar.                                                                                                                         |
| **Del itemaction** | [**Oda \_**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Marca de acción de dibujo DRAWENTIRE.                                                                                         |
| **itemState**  | [**ODS \_**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Marca de acción de dibujo seleccionada si el cursor está en el elemento y el botón del mouse está presionado. De lo contrario, este miembro es cero. |
| **hwndItem**   | Identificador del control de encabezado.                                                                                                                          |
| **Cámaras**        | Identificador del contexto de dispositivo del control de encabezado.                                                                                                    |
| **rcItem**     | Coordenadas del elemento de encabezado que se va a dibujar. Las coordenadas son relativas a la esquina superior izquierda del control de encabezado.                               |
| **itemData**   | Valor de 32 bits definido por la aplicación asociado al elemento.                                                                                             |



 

## <a name="header-control-filters"></a>Filtros de control de encabezado

Al especificar el estilo de ventana [**\_ FILTERBAR de HDS**](header-control-styles.md) para un control de encabezado, puede habilitar la colocación de los cuadros de edición de filtro debajo de los encabezados de columna. Aparece un botón de filtro junto al cuadro de edición. Puede implementar el filtrado respondiendo a los códigos de notificación [HDN \_ BEGINFILTEREDIT](hdn-beginfilteredit.md), [HDN \_ ENDFILTEREDIT](hdn-endfilteredit.md), [HDN \_ FILTERBTNCLICK](hdn-filterbtnclick.md)o [HDN \_ FILTERCHANGE](hdn-filterchange.md) .

De forma predeterminada, el cuadro de edición contiene un mensaje para que el usuario escriba texto. Puede restaurar el cuadro de edición a este estado predeterminado mediante el [**encabezado \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) o el [**encabezado \_ ClearAllFilters**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters).

En el ejemplo de código siguiente se muestra cómo recuperar el control de encabezado de un control de vista de lista y cómo agregar una barra de filtros.


```
// hList is the HWND of the list-view control.
HWND hHeader = ListView_GetHeader(hList);
LONG_PTR styles = GetWindowLongPtr(hHeader, GWL_STYLE);
SetWindowLongPtr(g_hHeader, GWL_STYLE, styles | HDS_FILTERBAR);
```



## <a name="default-header-control-message-processing"></a>Procesamiento de mensajes de control de encabezado predeterminado

En esta sección se describen los mensajes de ventana que se controlan mediante el procedimiento de ventana para la clase de ventana de [**\_ encabezado CT**](common-control-window-classes.md) .



| Message                                            | Procesamiento realizado                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**creación de WM \_**](/windows/desktop/winmsg/wm-create)                 | Inicializa el control de encabezado.                                                                                                                                                                                                                                                                               |
| [**destrucción de WM \_**](/windows/desktop/winmsg/wm-destroy)               | Desinicializa el control de encabezado.                                                                                                                                                                                                                                                                             |
| [**ERASEBKGND de WM \_**](/windows/desktop/winmsg/wm-erasebkgnd)         | Rellena el fondo del control de encabezado usando el color de fondo actual del control.                                                                                                                                                                                                                      |
| [**GETDLGCODE de WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)         | Devuelve una combinación de los valores de [**DLGC \_ WANTTAB**](/windows/desktop/dlgbox/wm-getdlgcode) y [**DLGC \_ WANTARROWS**](/windows/desktop/dlgbox/wm-getdlgcode) .                                                                                                                     |
| [**GETFONT de WM \_**](/windows/desktop/winmsg/wm-getfont)               | Devuelve el identificador de la fuente actual, que usa el control de encabezado para dibujar su texto.                                                                                                                                                                                                                 |
| [**LBUTTONDBLCLK de WM \_**](/windows/desktop/inputdev/wm-lbuttondblclk) | Captura la entrada del mouse. Si el cursor del mouse está en un divisor, el control envía el código de notificación [ \_ BEGINTRACK de HDN](hdn-begintrack.md) y comienza a arrastrar el divisor. Si el cursor está en un elemento, el elemento se muestra en estado presionado.                                                            |
| [**LBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-lbuttondown)     | Igual que el mensaje de [**\_ LBUTTONDBLCLK de WM**](/windows/desktop/inputdev/wm-lbuttondblclk) .                                                                                                                                                                                                                                       |
| [**LBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-lbuttonup)         | Libera la captura del mouse. Si el control estaba realizando el seguimiento del movimiento del mouse, envía el código de notificación [HDN \_ ENDTRACK](hdn-endtrack.md) y vuelve a dibujar el control de encabezado. De lo contrario, el control envía el código de notificación [HDN \_ ITEMCLICK](hdn-itemclick.md) y vuelve a dibujar el elemento de encabezado en el que se hizo clic. |
| [**MOUSEMOVE de WM \_**](/windows/desktop/inputdev/wm-mousemove)         | Si se está arrastrando un divisor, el control envía el código de notificación de [ \_ seguimiento de HDN](hdn-track.md) y muestra el elemento en la nueva posición. Si el botón primario del mouse está presionado y el cursor está en un elemento, el elemento se muestra en estado presionado.                                                      |
| [**NCCREATE de WM \_**](/windows/desktop/winmsg/wm-nccreate)             | Asigna e inicializa una estructura de datos interna.                                                                                                                                                                                                                                                         |
| [**NCDESTROY de WM \_**](/windows/desktop/winmsg/wm-ncdestroy)           | Libera los recursos asignados por el control de encabezado una vez que no se ha inicializado el control de encabezado.                                                                                                                                                                                                                |
| [**pintura de WM \_**](/windows/desktop/gdi/wm-paint)                      | Dibuja la región no válida del control de encabezado. Si el parámetro *wParam* no es null, el control supone que el valor es HDC y pinta usando ese contexto de dispositivo.                                                                                                                                    |
| [**SETCURSOR de WM \_**](/windows/desktop/menurc/wm-setcursor)           | Establece la forma del cursor, en función de si el cursor está en un divisor o en un elemento de encabezado.                                                                                                                                                                                                                   |
| [**WM \_**](/windows/desktop/winmsg/wm-setfont)               | Selecciona un nuevo identificador de fuente en el contexto del dispositivo para el control de encabezado.                                                                                                                                                                                                                                     |



 

 

 