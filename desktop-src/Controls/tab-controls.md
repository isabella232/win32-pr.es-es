---
title: Acerca de los controles tab
description: Un control de ficha es análogo a los divisores de un bloc de notas o las etiquetas de un archivador. Mediante el uso de un control de ficha, una aplicación puede definir varias páginas para la misma área de un cuadro de diálogo o de una ventana.
ms.assetid: 55ed2863-7f8d-43ce-a0f9-6f6d41e3f947
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c45ac7caa05c73e1dcf22a8e6f0eb4d031ca079
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166926"
---
# <a name="about-tab-controls"></a>Acerca de los controles tab

Un control de ficha es análogo a los divisores de un bloc de notas o las etiquetas de un archivador. Mediante el uso de un control de ficha, una aplicación puede definir varias páginas para la misma área de un cuadro de diálogo o de una ventana. Cada página consta de un determinado tipo de información o un grupo de controles que la aplicación muestra cuando el usuario selecciona la pestaña correspondiente.

En la captura de pantalla siguiente se muestra un control de pestaña simple que contiene pestañas para los días de la semana. Se ha seleccionado la pestaña Martes.

![captura de pantalla de una hoja de propiedades con cinco pestañas, una para cada día de la semana](images/tab-simple.png)

En este tema se incluyen las secciones siguientes.

-   [Crear controles de ficha](#creating-tab-controls)
-   [Estilos de control de pestaña](#tab-control-styles)
-   [Pestañas y atributos de pestaña](#tabs-and-tab-attributes)
-   [Área de visualización](#display-area)
-   [Selección de pestañas](#tab-selection)
-   [Listas de imágenes de control de pestañas](#tab-control-image-lists)
-   [Tamaño y posición de la pestaña](#tab-size-and-position)
-   [Pestañas dibujadas por el propietario](#owner-drawn-tabs)
-   [Información sobre herramientas del control de pestañas](#tab-control-tooltips)
-   [Procesamiento de mensajes de control de tabulación predeterminado](#default-tab-control-message-processing)

## <a name="creating-tab-controls"></a>Crear controles de ficha

Puede crear un control de ficha llamando a [**la función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especificando la clase de ventana [**WC \_ TABCONTROL.**](common-control-window-classes.md) Esta clase de ventana se registra cuando se carga el archivo DLL de controles comunes. Para asegurarse de que se carga el archivo DLL, use la [**función InitCommonControlsEx.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)

En Microsoft Visual Studio, puede crear un control de ficha mediante el Cuadro de herramientas.

Los mensajes se envían a un control de pestaña para agregar pestañas y, de lo contrario, afectan a la apariencia y el comportamiento del control. Cada mensaje tiene una macro correspondiente que puede usar en lugar de enviar el mensaje explícitamente. No se puede deshabilitar una pestaña individual en un control de ficha. Sin embargo, puede deshabilitar un control de ficha en una hoja de propiedades si deshabilita la página correspondiente.

## <a name="tab-control-styles"></a>Estilos de control de pestaña

Puede aplicar determinadas características a los controles de ficha especificando estilos de control de pestaña cuando se crea el control. Por ejemplo, puede especificar la alineación y la apariencia general de las pestañas en un control de ficha.

Puede hacer que las pestañas se parezcan a los botones especificando el [**estilo TCS \_ BUTTONS.**](tab-control-styles.md) Las pestañas de este tipo de control de pestaña deben servir la misma función que los controles de botón; Es decir, al hacer clic en una pestaña se debe ejecutar un comando en lugar de mostrar una página. Dado que el área de presentación de un control de pestaña de botón no se usa normalmente, no se dibuja ningún borde alrededor de él.

Puede hacer que una pestaña reciba el foco de entrada al hacer clic especificando el [**estilo \_ TCS FOCUSONBUTTONDOWN.**](tab-control-styles.md) Este estilo se usa normalmente solo con el [**estilo TCS \_ BUTTONS.**](tab-control-styles.md) Puede especificar que una pestaña no reciba el foco de entrada al hacer clic con el [**estilo TCS \_ FOCUSNEVER.**](tab-control-styles.md)

De forma predeterminada, un control de ficha muestra solo una fila de pestañas. Si no todas las pestañas se pueden mostrar a la vez, el control de pestaña muestra un control de flechas para que el usuario pueda desplazarse por pestañas adicionales a la vista. Puede hacer que un control de ficha muestre varias filas de pestañas, si es necesario, especificando el [**estilo TCS \_ MULTILINE.**](tab-control-styles.md) Con este estilo, todas las pestañas se pueden mostrar a la vez. Las pestañas se alinean a la izquierda dentro de cada fila, a menos que especifique [**el estilo TCS \_ RIGHTJUSTIFY.**](tab-control-styles.md) En este caso, el ancho de cada pestaña aumenta para que cada fila de pestañas rellene todo el ancho del control de ficha.

Un control de pestaña ajusta automáticamente el tamaño de cada pestaña para que se ajuste a su icono, si lo hubiera, y a su etiqueta. Para dar a todas las pestañas el mismo ancho, puede especificar el [**estilo \_ FIXEDWIDTH de TCS.**](tab-control-styles.md) El control ajusta el tamaño de todas las pestañas para ajustarse a la etiqueta más ancha, o bien puede asignar un ancho y un alto específicos mediante el mensaje [**\_ SETITEMSIZE de TCM.**](tcm-setitemsize.md) Dentro de cada pestaña, el control centra el icono y la etiqueta, colocando el icono a la izquierda de la etiqueta. Puede forzar el icono a la izquierda, dejando la etiqueta centrada, especificando el [**estilo \_ FORCEICONLEFT de TCS.**](tab-control-styles.md) Puede alinear a la izquierda el icono y la etiqueta mediante el [**estilo \_ FORCELABELLEFT de TCS.**](tab-control-styles.md) No se puede usar **el estilo \_ FIXEDWIDTH** de TCS con el [**estilo \_ RIGHTJUSTIFY de TCS.**](tab-control-styles.md)

Puede especificar que la ventana primaria dibuje las pestañas del control mediante el [**estilo TCS \_ OWNERDRAWFIXED.**](tab-control-styles.md) Para obtener más información, vea [Pestañas dibujadas por el propietario](#owner-drawn-tabs).

Puede especificar que un control de pestaña creará un control de información sobre herramientas mediante el estilo [**TCS \_ TOOLTIPS.**](tab-control-styles.md) Para obtener más información sobre esto, vea [Información sobre herramientas del control de pestañas](#tab-control-tooltips).

## <a name="tabs-and-tab-attributes"></a>Pestañas y atributos de pestaña

Cada pestaña de un control de pestaña consta de un icono, una etiqueta y datos definidos por la aplicación. Esta información se especifica mediante una [**estructura TCITEM.**](/windows/win32/api/commctrl/ns-commctrl-tcitema) Puede agregar pestañas a un control de pestaña, recuperar el número de pestañas, recuperar y establecer el contenido de una pestaña y eliminar pestañas. Las pestañas se identifican por su índice de base cero.

Para agregar pestañas a un control de pestaña, use el mensaje [**\_ INSERTITEM de TCM,**](tcm-insertitem.md) especificando la posición del elemento y la dirección de una [**estructura TCITEM.**](/windows/win32/api/commctrl/ns-commctrl-tcitema) Puede recuperar y establecer el contenido de una pestaña existente mediante los mensajes [**\_ GETITEM**](tcm-getitem.md) y [**TCM \_ SETITEM de TCM.**](tcm-setitem.md) Para cada pestaña, puede especificar un icono, una etiqueta o ambos. También puede especificar los datos definidos por la aplicación que se asocian a la pestaña.

Puede recuperar el número actual de pestañas mediante el mensaje [**\_ GETITEMCOUNT de TCM,**](tcm-getitemcount.md) eliminar una pestaña mediante el mensaje [**\_ DELETEITEM**](tcm-deleteitem.md) de TCM y eliminar todas las pestañas de un control de pestaña mediante el mensaje [**\_ DELETEALLITEMS de TCM.**](tcm-deleteallitems.md)

Puede asociar datos definidos por la aplicación a cada pestaña. Por ejemplo, puede guardar información sobre cada página con su pestaña correspondiente. De forma predeterminada, un control de pestaña asigna cuatro bytes adicionales por pestaña para los datos definidos por la aplicación. Puede cambiar el número de bytes adicionales por pestaña mediante el mensaje [**\_ SETITEMEXTRA de TCM.**](tcm-setitemextra.md) Solo puede usar este mensaje cuando el control de ficha está vacío.

El miembro **lParam** de la estructura TCITEM especifica los datos [**definidos por la**](/windows/win32/api/commctrl/ns-commctrl-tcitema) aplicación. Si usa más de 4 bytes de datos definidos por la aplicación, debe definir su propia estructura y usarla en lugar de **TCITEM**. Puede recuperar y establecer datos definidos por la aplicación de la misma manera que recupera y establece otra información sobre una pestaña mediante los mensajes [**\_ TCM GETITEM**](tcm-getitem.md) y [**TCM \_ SETITEM.**](tcm-setitem.md)

El primer miembro de la estructura debe ser [**una estructura TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) y los miembros restantes deben especificar datos definidos por la aplicación. **TCITEMHEADER** es idéntico a [**TCITEM,**](/windows/win32/api/commctrl/ns-commctrl-tcitema)salvo que no tiene el **miembro lParam.** La diferencia entre el tamaño de la estructura y el tamaño de **TCITEMHEADER** debe ser igual al número de bytes adicionales por pestaña.

## <a name="display-area"></a>Área de visualización

El área de presentación de un control de pestaña es el área en la que una aplicación muestra la página actual. Normalmente, una aplicación crea una ventana secundaria o un cuadro de diálogo, estableciendo el tamaño y la posición de la ventana para ajustarse al área de presentación. Dado el rectángulo de ventana de un control de pestaña, puede calcular el rectángulo delimitador del área de presentación mediante el mensaje [**\_ ADJUSTRECT de TCM.**](tcm-adjustrect.md)

A veces, el área de presentación debe tener un tamaño determinado, por ejemplo, el tamaño de un cuadro de diálogo secundario no modelo. Dado el rectángulo delimitador para el área de presentación, puede usar [**TCM \_ ADJUSTRECT**](tcm-adjustrect.md) para calcular el rectángulo de ventana correspondiente para el control de ficha.

## <a name="tab-selection"></a>Selección de pestañas

Cuando el usuario selecciona una pestaña, un control de pestaña envía sus códigos de notificación de ventana primaria en forma de [**mensajes WM \_ NOTIFY.**](wm-notify.md) El [código de notificación DE \_ TCN SELCHANGING](tcn-selchanging.md) se envía antes de que cambie la selección y el código de [notificación DE \_ TCN SELCHANGE](tcn-selchange.md) se envía después de que cambie la selección.

Puede procesar [TCN \_ SELCHANGING](tcn-selchanging.md) para guardar el estado de la página saliente. Puede devolver **TRUE para evitar** que la selección cambie. Por ejemplo, es posible que no quiera salir de un cuadro de diálogo secundario en el que un control tiene una configuración no válida.

Debe procesar [TCN \_ SELCHANGE para](tcn-selchange.md) mostrar la página entrante en el área de presentación. Esto podría implicar simplemente cambiar la información que se muestra en una ventana secundaria. Más a menudo, cada página consta de una ventana secundaria o un cuadro de diálogo. En este caso, una aplicación podría procesar esta notificación mediante la destrucción u ocultación de la ventana o el cuadro de diálogo secundarios salientes y mediante la creación o la presentación de la ventana secundaria o el cuadro de diálogo entrantes.

Puede recuperar y establecer la selección actual mediante los mensajes [**\_ GETCURSEL**](tcm-getcursel.md) y [**TCM \_ SETCURSEL de TCM.**](tcm-setcursel.md)

## <a name="tab-control-image-lists"></a>Listas de imágenes de control de pestañas

Cada pestaña puede tener un icono asociado, que se especifica mediante un índice en la lista de imágenes para el control de ficha. Cuando se crea un control de ficha, no tiene ninguna lista de imágenes asociada. Una aplicación puede crear una lista de imágenes mediante la función [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) y, a continuación, asignarla a un control de pestaña mediante el mensaje [**\_ SETIMAGELIST de TCM.**](tcm-setimagelist.md)

Puede agregar imágenes a la lista de imágenes de un control de pestaña igual que lo haría con cualquier otra lista de imágenes. Sin embargo, una aplicación debe quitar imágenes mediante el [**mensaje \_ REMOVEIMAGE**](tcm-removeimage.md) de TCM en lugar de la [**función ImageList \_ Remove.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) Este mensaje garantiza que cada pestaña permanece asociada a la misma imagen que antes.

La destrucción de un control de ficha no destruye una lista de imágenes asociada a él. Debe destruir la lista de imágenes por separado. Esto resulta útil si desea asignar la misma lista de imágenes a varios controles de pestaña.

Para recuperar el identificador de la lista de imágenes asociada actualmente a un control de pestaña, puede usar el [**mensaje \_ GETIMAGELIST de TCM.**](tcm-getimagelist.md)

## <a name="tab-size-and-position"></a>Tamaño y posición de la pestaña

Cada pestaña de un control de pestaña tiene un tamaño y una posición. Puede establecer el tamaño de las pestañas, recuperar el rectángulo delimitador de una pestaña o determinar qué pestaña se encuentra en una posición especificada.

Para los controles de pestaña de ancho fijo y dibujado por el propietario, puede establecer el ancho y alto exactos de las pestañas mediante el mensaje [**\_ SETITEMSIZE de TCM.**](tcm-setitemsize.md) En otros controles de pestaña, el tamaño de cada pestaña se calcula en función del icono y la etiqueta de la pestaña. El control de pestaña incluye espacio para un borde y un margen adicional. Puede establecer el grosor del margen mediante el mensaje [**\_ SETPADDING de TCM.**](tcm-setpadding.md)

Puede determinar el rectángulo delimitador actual de una pestaña mediante el mensaje [**\_ GETITEMRECT de TCM.**](tcm-getitemrect.md) Puede determinar qué pestaña, si existe, está en una ubicación especificada mediante el [**mensaje \_ HITTEST de TCM.**](tcm-hittest.md)

En un control de pestaña con el estilo [**\_ MULTILINE de TCS,**](tab-control-styles.md) puede determinar el número actual de filas de pestañas mediante el mensaje [**\_ GETROWCOUNT de TCM.**](tcm-getrowcount.md)

## <a name="owner-drawn-tabs"></a>Owner-Drawn pestañas

Si un control de pestaña tiene el estilo [**TCS \_ OWNERDRAWFIXED,**](tab-control-styles.md) la ventana primaria debe pintar pestañas procesando el [**mensaje \_ DRAWITEM de WM.**](wm-drawitem.md) El control de pestaña envía este mensaje cada vez que es necesario pintar una pestaña. El *parámetro lParam* especifica la dirección de una estructura [**DRAWITEMSTRUCT,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contiene el índice de la pestaña, su rectángulo delimitador y el contexto de dispositivo (DC) en el que se va a dibujar.

De forma predeterminada, **el miembro itemData** de [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contiene el valor del **miembro lParam** de la [**estructura TCITEM.**](/windows/win32/api/commctrl/ns-commctrl-tcitema) Sin embargo, si cambia la cantidad de datos definidos por la aplicación por pestaña, **itemData** contiene la dirección de los datos en su lugar. Puede cambiar la cantidad de datos definidos por la aplicación por pestaña mediante el mensaje [**\_ SETITEMEXTRA de TCM.**](tcm-setitemextra.md)

Para especificar el tamaño de los elementos de un control de ficha, la ventana primaria debe procesar el [**mensaje \_ MEASUREITEM de WM.**](wm-measureitem.md) Dado que todas las pestañas de un control de pestaña dibujado por el propietario tienen el mismo tamaño, este mensaje se envía solo una vez. No hay ningún estilo de control de tabulación para las pestañas dibujadas por el propietario de tamaño variable. También puede establecer el ancho y el alto de las pestañas mediante el [**mensaje \_ SETITEMSIZE de TCM.**](tcm-setitemsize.md)

## <a name="tab-control-tooltips"></a>Información sobre herramientas del control de pestañas

Puede usar un control de información sobre herramientas para proporcionar una breve descripción de cada pestaña de un control de pestaña. Un control de pestaña que tiene el estilo [**TCS \_ TOOLTIPS**](tab-control-styles.md) crea un control de información sobre herramientas cuando se crea y destruye el control de información sobre herramientas cuando se destruye. También puede crear un control de información sobre herramientas y asignarlo a un control de pestaña.

Si usa un control de información sobre herramientas con un control de pestaña, la ventana primaria debe procesar el código de notificación [ \_ GETDISPINFO de TTN](ttn-getdispinfo.md) para proporcionar una descripción de cada pestaña a petición.

Para usar el mismo control de información sobre herramientas con más de un control de pestaña, cree el control de información sobre herramientas usted mismo y asígnelo al control de pestaña mediante el mensaje [**\_ SETTOOLTIPS de TCM.**](tcm-settooltips.md) Puede recuperar el identificador en el control de información sobre herramientas actual de un control de pestaña mediante el mensaje [**\_ GETTOOLTIPS de TCM.**](tcm-gettooltips.md) Si crea su propio control de información sobre herramientas, no debe usar el estilo [**TCS \_ TOOLTIPS.**](tab-control-styles.md)

## <a name="default-tab-control-message-processing"></a>Procesamiento de mensajes de control de tabulación predeterminado

En esta sección se describe el procesamiento de mensajes realizado por un control de pestaña. Los mensajes específicos de los controles de tabulación se de abordan en otras secciones de esta documentación.



| Message                                                  | Procesamiento realizado                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAPTURECHANGED**](/windows/desktop/inputdev/wm-capturechanged) | No hace nada si el control de tabulación liberó la propia captura del mouse. Si otra ventana captura el mouse y se mantiene un botón, el comando lo libera.                                                                                                                                                                                                                                                                                                                |
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                 | Asigna e inicializa una estructura de datos interna. El control crea un control de información sobre herramientas si se especifica el estilo [**TCS \_ TOOLTIPS.**](tab-control-styles.md)                                                                                                                                                                                                                                                                                                    |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)               | Libera los recursos asignados durante el [**procesamiento de WM \_ CREATE.**](/windows/desktop/winmsg/wm-create)                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | Devuelve una combinación de los valores \_ WANTARROWS y \_ DLGC WANTCHARS de DLGC.                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Devuelve el identificador a la fuente utilizada para las etiquetas.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)               | Procesa las claves de dirección y cambia la selección, si procede.                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)           | Invalida la pestaña que tiene el foco, por lo que se volverá a dibujar para reflejar un estado sin foco.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)       | Reenvía el mensaje al control de información sobre herramientas, si existe, y cambia la selección si el usuario hace clic en una pestaña. Si el usuario hace clic en un botón, el control vuelve a dibujar el botón para dar una apariencia desenfoque y captura el mouse. Si el usuario hace clic en una pestaña o un botón y se especifica el estilo [**\_ FOCUSONBUTTONDOWN de TCS,**](tab-control-styles.md) el control establece el foco en sí mismo.                                                     |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)           | Libera el mouse si se ha presionado un botón. Si el cursor está sobre el botón y se mantiene, el control cambia la selección en consecuencia y vuelve a dibujar el botón.                                                                                                                                                                                                                                                                                                         |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)           | Reenvía el mensaje al control de información sobre herramientas, si lo hubiera. Si se [**especifica el estilo \_ TCS BUTTONS**](tab-control-styles.md) y el botón del mouse se mantiene bloqueado después de hacer clic, el control también puede volver a dibujar el botón afectado para darle un aspecto elevado o bloqueado.                                                                                                                                                                                            |
| [**WM \_ NOTIFY**](wm-notify.md)                          | Reenvía los códigos de notificación enviados por el control de información sobre herramientas.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                            | Dibuja un borde alrededor del área de presentación (a menos que se especifique el estilo [**TCS \_ BUTTONS)**](tab-control-styles.md) y pinta las pestañas que intersecan con el rectángulo no válido. Para cada pestaña, dibuja el cuerpo de la pestaña (o envía un mensaje [**\_ DRAWITEM wm**](wm-drawitem.md) a la ventana primaria) y, a continuación, dibuja un borde alrededor de la pestaña. Si el *parámetro wParam* no es NULL, el control asume que el valor es un HDC y pinta con ese contexto de dispositivo. |
| [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)       | Envía un [código de notificación NM \_ RCLICK](nm-rclick-tab.md) a la ventana primaria.                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)             | Invalida la pestaña que tiene el foco para que se vuelva a dibujar para reflejar un estado enfocado.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | Establece la fuente utilizada para las etiquetas.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw)                    | Establece el estado de una marca interna que determina si el control se vuelve a dibujar cuando se insertan y eliminan elementos, cuando se cambia la fuente, y así sucesivamente.                                                                                                                                                                                                                                                                                                                      |
| [**TAMAÑO \_ WM**](/windows/desktop/winmsg/wm-size)                     | Vuelve a calcular las posiciones de las pestañas y puede invalidar parte del control de tabulación para forzar el repintado de algunas o todas las pestañas.                                                                                                                                                                                                                                                                                                                                                             |



 

 

 