---
title: Acerca de los controles de ficha
description: Un control de ficha es análogo a los divisores de un bloc de notas o las etiquetas de un archivador. Mediante el uso de un control de ficha, una aplicación puede definir varias páginas para la misma área de un cuadro de diálogo o de una ventana.
ms.assetid: 55ed2863-7f8d-43ce-a0f9-6f6d41e3f947
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c45ac7caa05c73e1dcf22a8e6f0eb4d031ca079
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149664"
---
# <a name="about-tab-controls"></a>Acerca de los controles de ficha

Un control de ficha es análogo a los divisores de un bloc de notas o las etiquetas de un archivador. Mediante el uso de un control de ficha, una aplicación puede definir varias páginas para la misma área de un cuadro de diálogo o de una ventana. Cada página está formada por un tipo determinado de información o un grupo de controles que la aplicación muestra cuando el usuario selecciona la pestaña correspondiente.

En la captura de pantalla siguiente se muestra un control de ficha simple que contiene las pestañas de los días de la semana. Se ha seleccionado la pestaña martes.

![captura de pantalla de una hoja de propiedades con cinco pestañas, una para cada día de la semana](images/tab-simple.png)

En este tema se incluyen las secciones siguientes.

-   [Crear controles de ficha](#creating-tab-controls)
-   [Estilos de control de pestaña](#tab-control-styles)
-   [Pestañas y atributos de pestaña](#tabs-and-tab-attributes)
-   [Área de visualización](#display-area)
-   [Selección de pestañas](#tab-selection)
-   [Listas de imágenes del control de pestañas](#tab-control-image-lists)
-   [Tamaño y posición de tabulación](#tab-size-and-position)
-   [Pestañas dibujadas por el propietario](#owner-drawn-tabs)
-   [Información sobre herramientas del control de pestaña](#tab-control-tooltips)
-   [Procesamiento de mensajes de control de pestaña predeterminado](#default-tab-control-message-processing)

## <a name="creating-tab-controls"></a>Crear controles de ficha

Puede crear un control de ficha mediante una llamada a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando la clase de ventana [**\_ TABCONTROL de CT**](common-control-window-classes.md) . Esta clase de ventana se registra cuando se carga el archivo DLL de controles comunes. Para asegurarse de que se carga el archivo DLL, utilice la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .

En Microsoft Visual Studio, puede crear un control de ficha mediante el cuadro de herramientas.

Los mensajes se envían a un control de ficha para agregar pestañas y, de lo contrario, afectar a la apariencia y el comportamiento del control. Cada mensaje tiene una macro correspondiente que puede usar en lugar de enviar el mensaje explícitamente. No se puede deshabilitar una pestaña individual en un control de ficha. Sin embargo, puede deshabilitar un control de ficha en una hoja de propiedades deshabilitando la página correspondiente.

## <a name="tab-control-styles"></a>Estilos de control de pestaña

Puede aplicar ciertas características a los controles de ficha si especifica los estilos de control de pestañas al crear el control. Por ejemplo, puede especificar la alineación y la apariencia general de las fichas de un control de ficha.

Puede hacer que las pestañas se parezcan a los botones especificando el estilo de [**\_ botones de TCS**](tab-control-styles.md) . Las pestañas de este tipo de control de pestaña deben servir la misma función que los controles de botón; es decir, al hacer clic en una pestaña, se debe ejecutar un comando en lugar de mostrar una página. Dado que el área de presentación de un control de ficha de botón normalmente no se utiliza, no se dibuja ningún borde alrededor.

Puede hacer que una pestaña reciba el foco de entrada al hacer clic especificando el estilo [**de \_ FOCUSONBUTTONDOWN de TCS**](tab-control-styles.md) . Este estilo se usa normalmente solo con el [**estilo \_ botones de TCS**](tab-control-styles.md) . Puede especificar que una pestaña no reciba el foco de entrada cuando se haga clic en él con el estilo [**TCS \_ FOCUSNEVER**](tab-control-styles.md) .

De forma predeterminada, un control de ficha muestra solo una fila de pestañas. Si no se pueden mostrar todas las pestañas a la vez, el control de pestaña muestra un control de flechas para que el usuario pueda desplazarse por las pestañas adicionales a la vista. Puede hacer que un control de ficha muestre varias filas de pestañas, si es necesario, especificando el estilo de [**\_ varias líneas de TCS**](tab-control-styles.md) . Con este estilo, todas las pestañas se pueden mostrar a la vez. Las pestañas se alinean a la izquierda dentro de cada fila, a menos que especifique el estilo [**TCS \_ RIGHTJUSTIFY**](tab-control-styles.md) . En este caso, el ancho de cada pestaña aumenta para que cada fila de pestañas ocupe todo el ancho del control de ficha.

Un control de pestaña dimensiona automáticamente cada pestaña para ajustarse a su icono, si existe, y a su etiqueta. Para dar el mismo ancho a todas las pestañas, puede especificar el estilo [**TCS \_ FIXEDWIDTH**](tab-control-styles.md) . El control ajusta el tamaño de todas las pestañas a la etiqueta más ancha, o bien puede asignar un ancho y un alto específicos mediante el mensaje [**\_ SETITEMSIZE de TCM**](tcm-setitemsize.md) . Dentro de cada pestaña, el control centra el icono y la etiqueta, colocando el icono a la izquierda de la etiqueta. Puede forzar el icono a la izquierda, y dejar la etiqueta centrada, especificando el estilo de [**\_ FORCEICONLEFT de TCS**](tab-control-styles.md) . Puede alinear a la izquierda el icono y la etiqueta mediante el [**estilo \_ FORCELABELLEFT de TCS**](tab-control-styles.md) . No puede usar el estilo **TCS \_ FIXEDWIDTH** con el estilo [**\_ RIGHTJUSTIFY de TCS**](tab-control-styles.md) .

Puede especificar que la ventana primaria dibuje las fichas en el control mediante el estilo [**\_ OWNERDRAWFIXED de TCS**](tab-control-styles.md) . Para obtener más información, consulte [pestañas dibujadas por el propietario](#owner-drawn-tabs).

Puede especificar que un control de ficha creará un control de información sobre herramientas mediante el estilo de [**\_ información sobre herramientas de TCS**](tab-control-styles.md) . Para obtener más información, vea [información sobre herramientas del control de pestañas](#tab-control-tooltips).

## <a name="tabs-and-tab-attributes"></a>Pestañas y atributos de pestaña

Cada pestaña de un control de pestaña se compone de un icono, una etiqueta y datos definidos por la aplicación. Esta información se especifica mediante una estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . Puede Agregar pestañas a un control de ficha, recuperar el número de pestañas, recuperar y establecer el contenido de una pestaña y eliminar pestañas. Las pestañas se identifican por su índice basado en cero.

Para agregar pestañas a un control de ficha, use el mensaje [**\_ INSERTITEM TCM**](tcm-insertitem.md) , especificando la posición del elemento y la dirección de una estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . Puede recuperar y establecer el contenido de una pestaña existente mediante los mensajes [**TCM \_**](tcm-getitem.md) [**\_ SETITEM y TCM**](tcm-setitem.md) . En cada pestaña, puede especificar un icono, una etiqueta o ambos. También puede especificar los datos definidos por la aplicación que se van a asociar a la pestaña.

Puede recuperar el número actual de pestañas mediante el mensaje [**TCM \_ GETITEMCOUNT**](tcm-getitemcount.md) , eliminar una pestaña mediante el mensaje de [**TCM \_ DELETEITEM**](tcm-deleteitem.md) y eliminar todas las pestañas de un control de ficha mediante el [**mensaje \_ DELETEALLITEMS de TCM**](tcm-deleteallitems.md) .

Puede asociar los datos definidos por la aplicación a cada pestaña. Por ejemplo, puede guardar información sobre cada página con su correspondiente pestaña. De forma predeterminada, un control de ficha asigna cuatro bytes adicionales por pestaña para los datos definidos por la aplicación. Puede cambiar el número de bytes adicionales por pestaña mediante el mensaje [**\_ SETITEMEXTRA de TCM**](tcm-setitemextra.md) . Este mensaje solo se puede usar cuando el control de pestaña está vacío.

Los datos definidos por la aplicación se especifican mediante el miembro **lParam** de la estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . Si usa más de 4 bytes de datos definidos por la aplicación, deberá definir su propia estructura y usarla en lugar de **TCITEM**. Puede recuperar y establecer los datos definidos por la aplicación de la misma manera que recupera y establece otra información acerca de una pestaña, mediante el uso de los mensajes de [**\_ SETITEM**](tcm-setitem.md) TCM y TCM de TCM. [**\_**](tcm-getitem.md)

El primer miembro de la estructura debe ser una estructura [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) y los miembros restantes deben especificar los datos definidos por la aplicación. **TCITEMHEADER** es idéntico a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema), salvo que no tiene el miembro **lParam** . La diferencia entre el tamaño de la estructura y el tamaño de **TCITEMHEADER** debe ser igual al número de bytes adicionales por pestaña.

## <a name="display-area"></a>Área de visualización

El área de presentación de un control de ficha es el área en la que una aplicación muestra la página actual. Normalmente, una aplicación crea un cuadro de diálogo o ventana secundaria, estableciendo el tamaño y la posición de la ventana para ajustarse al área de presentación. Dado el rectángulo de ventana de un control de ficha, puede calcular el rectángulo delimitador del área de presentación mediante el mensaje [**\_ ADJUSTRECT de TCM**](tcm-adjustrect.md) .

A veces, el área de presentación debe tener un tamaño determinado (por ejemplo, el tamaño de un cuadro de diálogo secundario no modal). Dado el rectángulo delimitador del área de visualización, puede usar [**TCM \_ ADJUSTRECT**](tcm-adjustrect.md) para calcular el rectángulo de ventana correspondiente para el control de ficha.

## <a name="tab-selection"></a>Selección de pestañas

Cuando el usuario selecciona una pestaña, un control de ficha envía los códigos de notificación de la ventana primaria en forma de mensajes de notificación de [**WM \_**](wm-notify.md) . El código de notificación de [ \_ SELCHANGING de TCN](tcn-selchanging.md) se envía antes de que cambie la selección y se envía el código de notificación de [TCN \_ SELCHANGE](tcn-selchange.md) después de que cambie la selección.

Puede procesar [TCN \_ SELCHANGING](tcn-selchanging.md) para guardar el estado de la página de salida. Puede devolver **true** para evitar que la selección cambie. Por ejemplo, es posible que no desee cambiar de un cuadro de diálogo secundario en el que un control tiene un valor no válido.

Debe procesar [TCN \_ SELCHANGE](tcn-selchange.md) para mostrar la página entrante en el área de visualización. Esto puede implicar simplemente cambiar la información que se muestra en una ventana secundaria. Con mayor frecuencia, cada página se compone de una ventana o un cuadro de diálogo secundarios. En este caso, una aplicación puede procesar esta notificación destruyendo u ocultando el cuadro de diálogo o la ventana secundaria saliente y creando o mostrando el cuadro de diálogo o la ventana secundaria entrante.

Puede recuperar y establecer la selección actual mediante los mensajes [**TCM \_ GETCURSEL**](tcm-getcursel.md) y [**TCM \_ SETCURSEL**](tcm-setcursel.md) .

## <a name="tab-control-image-lists"></a>Listas de imágenes del control de pestañas

Cada pestaña puede tener un icono asociado, que se especifica mediante un índice en la lista de imágenes del control de pestaña. Cuando se crea un control de ficha, no tiene ninguna lista de imágenes asociada. Una aplicación puede crear una lista de imágenes mediante la función de [**\_ creación ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) y, a continuación, asignarla a un control de ficha mediante el mensaje [**\_ SETIMAGELIST de TCM**](tcm-setimagelist.md) .

Puede Agregar imágenes a la lista de imágenes de un control de pestaña tal como lo haría con cualquier otra lista de imágenes. Sin embargo, una aplicación debe quitar las imágenes mediante el mensaje [**\_ REMOVEIMAGE de TCM**](tcm-removeimage.md) en lugar de la función [**ImageList \_ Remove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) . Este mensaje garantiza que cada pestaña permanece asociada a la misma imagen que antes.

La destrucción de un control de ficha no destruye una lista de imágenes asociada a ella. Debe destruir la lista de imágenes por separado. Esto resulta útil si desea asignar la misma lista de imágenes a varios controles de ficha.

Para recuperar el identificador de la lista de imágenes asociada actualmente a un control de ficha, puede usar el mensaje [**\_ GETIMAGELIST de TCM**](tcm-getimagelist.md) .

## <a name="tab-size-and-position"></a>Tamaño y posición de tabulación

Cada pestaña de un control de ficha tiene un tamaño y una posición. Puede establecer el tamaño de las fichas, recuperar el rectángulo delimitador de una pestaña o determinar qué pestaña está en una posición especificada.

En el caso de los controles de pestaña de ancho fijo y dibujado por el propietario, puede establecer el ancho y el alto exactos de las pestañas mediante el mensaje [**\_ SETITEMSIZE de TCM**](tcm-setitemsize.md) . En otros controles de ficha, el tamaño de cada pestaña se calcula en función del icono y la etiqueta de la pestaña. El control de pestaña incluye espacio para un borde y un margen adicional. Puede establecer el grosor del margen mediante el mensaje SETPADDING de [**TCM \_**](tcm-setpadding.md) .

Puede determinar el rectángulo delimitador actual para una pestaña mediante el mensaje [**\_ GETITEMRECT de TCM**](tcm-getitemrect.md) . Puede determinar qué ficha, si la hay, está en una ubicación especificada mediante el mensaje [**\_ HITTEST de TCM**](tcm-hittest.md) .

En un control de ficha con el estilo de [**\_ varias líneas de TCS**](tab-control-styles.md) , puede determinar el número actual de filas de pestañas mediante el mensaje [**\_ GETROWCOUNT de TCM**](tcm-getrowcount.md) .

## <a name="owner-drawn-tabs"></a>Owner-Drawn pestañas

Si un control de ficha tiene el estilo [**\_ OWNERDRAWFIXED de TCS**](tab-control-styles.md) , la ventana primaria debe pintar las pestañas procesando el mensaje de [**\_ DRAWITEM de WM**](wm-drawitem.md) . El control de pestaña envía este mensaje cada vez que es necesario pintar una tabulación. El parámetro *lParam* especifica la dirección de una estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , que contiene el índice de la pestaña, su rectángulo delimitador y el contexto de dispositivo (DC) en el que se va a dibujar.

De forma predeterminada, el miembro **itemData** de [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contiene el valor del miembro **lParam** de la estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . Sin embargo, si cambia la cantidad de datos definidos por la aplicación por pestaña, **itemData** contendrá la dirección de los datos en su lugar. Puede cambiar la cantidad de datos definidos por la aplicación por pestaña mediante el mensaje [**\_ SETITEMEXTRA de TCM**](tcm-setitemextra.md) .

Para especificar el tamaño de los elementos de un control de ficha, la ventana primaria debe procesar el mensaje de [**\_ MEASUREITEM de WM**](wm-measureitem.md) . Dado que todas las pestañas de un control de pestaña dibujado por el propietario tienen el mismo tamaño, este mensaje se envía solo una vez. No hay ningún estilo de control de pestaña para las pestañas dibujadas por el propietario de tamaño variable. También puede establecer el ancho y el alto de las pestañas mediante el mensaje [**\_ SETITEMSIZE de TCM**](tcm-setitemsize.md) .

## <a name="tab-control-tooltips"></a>Información sobre herramientas del control de pestaña

Puede utilizar un control de información sobre herramientas para proporcionar una breve descripción de cada pestaña de un control de ficha. Un control de ficha que tiene el estilo [**\_ información sobre herramientas de TCS**](tab-control-styles.md) crea un control ToolTip cuando se crea y destruye el control ToolTip cuando se destruye. También puede crear un control ToolTip y asignarlo a un control de ficha.

Si usa un control de información sobre herramientas con un control de pestaña, la ventana primaria debe procesar el código de notificación [TTN \_ GETDISPINFO](ttn-getdispinfo.md) para proporcionar una descripción de cada pestaña a solicitud.

Para usar el mismo control de información sobre herramientas con más de un control de pestaña, cree el control ToolTip y asígnelo al control de pestañas mediante el mensaje [**\_ SETTOOLTIPS de TCM**](tcm-settooltips.md) . Puede recuperar el identificador del control de información sobre herramientas actual de un control de pestaña mediante el mensaje [**\_ GETTOOLTIPS de TCM**](tcm-gettooltips.md) . Si crea su propio control de información sobre herramientas, no debe usar el estilo [**\_ información sobre herramientas de TCS**](tab-control-styles.md) .

## <a name="default-tab-control-message-processing"></a>Procesamiento de mensajes de control de pestaña predeterminado

En esta sección se describe el procesamiento de mensajes realizado por un control de ficha. Los mensajes específicos de los controles de ficha se describen en otras secciones de esta documentación.



| Message                                                  | Procesamiento realizado                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAPTURECHANGED de WM \_**](/windows/desktop/inputdev/wm-capturechanged) | No hace nada si el control de pestaña liberó la propia captura del mouse. Si otra ventana ha capturado el mouse y se mantiene presionado un botón, el comando libera el botón.                                                                                                                                                                                                                                                                                                                |
| [**creación de WM \_**](/windows/desktop/winmsg/wm-create)                 | Asigna e inicializa una estructura de datos interna. El control crea un control de información sobre herramientas si se especifica el estilo de [**\_ información sobre herramientas de TCS**](tab-control-styles.md) .                                                                                                                                                                                                                                                                                                    |
| [**destrucción de WM \_**](/windows/desktop/winmsg/wm-destroy)               | Libera los recursos asignados durante el procesamiento de la [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) .                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**GETDLGCODE de WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)         | Devuelve una combinación de los valores de DLGC \_ WANTARROWS y DLGC \_ WANTCHARS.                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**GETFONT de WM \_**](/windows/desktop/winmsg/wm-getfont)               | Devuelve el identificador de la fuente utilizada para las etiquetas.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**KEYDOWN de WM \_**](/windows/desktop/inputdev/wm-keydown)               | Procesa las teclas de dirección y cambia la selección, si procede.                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**KILLFOCUS de WM \_**](/windows/desktop/inputdev/wm-killfocus)           | Invalida la pestaña que tiene el foco para que se vuelva a dibujar de modo que refleje un estado sin foco.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**LBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-lbuttondown)       | Reenvía el mensaje al control ToolTip, si existe, y cambia la selección si el usuario hace clic en una pestaña. Si el usuario hace clic en un botón, el control vuelve a dibujar el botón para dar una apariencia hundida y capturar el mouse. Si el usuario hace clic en una pestaña o botón y se especifica el estilo [**TCS \_ FOCUSONBUTTONDOWN**](tab-control-styles.md) , el control establece el foco en sí mismo.                                                     |
| [**LBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-lbuttonup)           | Suelta el mouse si se presionó un botón. Si el cursor está sobre el botón y se mantiene presionado, el control cambia la selección en consecuencia y vuelve a dibujar el botón.                                                                                                                                                                                                                                                                                                         |
| [**MOUSEMOVE de WM \_**](/windows/desktop/inputdev/wm-mousemove)           | Reenvía el mensaje al control ToolTip, si existe. Si se especifica el estilo de [**\_ botones de TCS**](tab-control-styles.md) y se mantiene presionado el botón del mouse después de hacer clic, el control también puede volver a dibujar el botón afectado para darle un aspecto elevado o hundido.                                                                                                                                                                                            |
| [**\_notificaciones de WM**](wm-notify.md)                          | Reenvía los códigos de notificación enviados por el control ToolTip.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**pintura de WM \_**](/windows/desktop/gdi/wm-paint)                            | Dibuja un borde alrededor del área de presentación (a menos que se especifique el estilo de [**\_ botones de TCS**](tab-control-styles.md) ) y pinta cualquier pestaña que intersecte con el rectángulo no válido. En cada pestaña, se dibuja el cuerpo de la pestaña (o se envía un mensaje de Windows de [**WM \_**](wm-drawitem.md) a la ventana primaria) y, a continuación, se dibuja un borde alrededor de la pestaña. Si el parámetro *wParam* no es null, el control supone que el valor es HDC y pinta usando ese contexto de dispositivo. |
| [**RBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-rbuttondown)       | Envía un código de notificación de [nm \_ RCLICK](nm-rclick-tab.md) a la ventana primaria.                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**SETFOCUS de WM \_**](/windows/desktop/inputdev/wm-setfocus)             | Invalida la pestaña que tiene el foco para que se vuelva a dibujar de modo que refleje un estado enfocado.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_**](/windows/desktop/winmsg/wm-setfont)               | Establece la fuente utilizada para las etiquetas.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SETREDRAW de WM \_**](/windows/desktop/gdi/wm-setredraw)                    | Establece el estado de una marca interna que determina si el control se vuelve a dibujar cuando se insertan y eliminan elementos, cuando se cambia la fuente, etc.                                                                                                                                                                                                                                                                                                                      |
| [**tamaño de WM \_**](/windows/desktop/winmsg/wm-size)                     | Vuelve a calcular las posiciones de las fichas y puede invalidar parte del control de pestaña para forzar el repintado de algunas pestañas o de todas ellas.                                                                                                                                                                                                                                                                                                                                                             |



 

 

 