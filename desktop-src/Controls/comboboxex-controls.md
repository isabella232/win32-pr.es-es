---
title: Acerca de los controles ComboBoxEx
description: Los controles ComboBoxEx son controles de cuadro combinado que proporcionan compatibilidad nativa con imágenes de elementos.
ms.assetid: a4b1aa79-40c4-4eff-801c-4f308d86fb35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427abef015474047d1842d13e5fb40640d0406c5
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904859"
---
# <a name="about-comboboxex-controls"></a>Acerca de los controles ComboBoxEx

Los controles ComboBoxEx son controles de cuadro combinado que proporcionan compatibilidad nativa con imágenes de elementos. Para facilitar el acceso a las imágenes de los elementos, el control proporciona compatibilidad con la lista de imágenes. Con este control, puede proporcionar la funcionalidad de un cuadro combinado sin tener que dibujar manualmente los gráficos de los elementos.

En este tema se incluyen las siguientes secciones.

-   [Crear controles ComboBoxEx](#creating-comboboxex-controls)
-   [Estilos de control ComboBoxEx](#comboboxex-control-styles)
-   [Elementos de control ComboBoxEx](#comboboxex-control-items)
-   [Elementos de devolución de llamada](#callback-items)
-   [Listas de imágenes del control ComboBoxEx](#comboboxex-control-image-lists)
-   [Acerca de los mensajes de notificación del control ComboBoxEx](#about-comboboxex-control-notification-messages)
-   [Reenvío de mensajes del control ComboBoxEx](#comboboxex-control-message-forwarding)

## <a name="creating-comboboxex-controls"></a>Crear controles ComboBoxEx

De hecho, un control ComboBoxEx crea un cuadro combinado secundario y realiza tareas de dibujo de propietario en función de una lista de imágenes asignada. Por lo tanto, el estilo de la [**INE de CBS \_**](combo-box-styles.md) es implícito y no es necesario usarlo al crear el control. Dado que las listas de imágenes se usan para proporcionar gráficos de elementos, no se puede usar el estilo [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) .

Un control ComboBoxEx se debe inicializar mediante una llamada a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , especificando \_ \_ las clases USEREX de ICC en la estructura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) adjunta.

Puede crear un control ComboBoxEx mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especificando [**WC \_ ComboBoxEx**](common-control-window-classes.md) como clase de ventana. La clase se registra cuando se llama a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) como se explicó anteriormente.

Los controles ComboBoxEx se crean sin una lista de imágenes predeterminada. Para usar imágenes de elementos, debe crear una lista de imágenes para el control ComboBoxEx y asignarla al control mediante el mensaje [**CBEM \_ SETIMAGELIST**](cbem-setimagelist.md) . Si no asigna una lista de imágenes al control ComboBoxEx, el control solo muestra el texto del elemento.

## <a name="comboboxex-control-styles"></a>Estilos de control ComboBoxEx

Los controles de ComboBoxEx solo admiten los siguientes estilos de cuadro combinado:

-   CBS \_ simple
-   \_lista desplegable de CBS
-   DROPDOWNLIST de CBS \_
-   \_elemento secundario WS

También hay varios [estilos extendidos de control ComboBoxEx](comboboxex-control-extended-styles.md) que solo usa ComboBoxEx.

> [!Note]  
> Es posible que el estilo [**\_ simple CBS**](combo-box-styles.md) no funcione correctamente en algunos casos.

 

Dado que el control ComboBoxEx realiza tareas de dibujo de propietario en función de una lista de imágenes asignada, el estilo de la expresión [**CBS \_**](combo-box-styles.md) es implícito; no es necesario usarlo al crear el control. Dado que las listas de imágenes se usan para proporcionar gráficos de elementos, no se puede usar el estilo [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) . El control ComboBoxEx también admite los [estilos extendidos de control ComboBoxEx](comboboxex-control-extended-styles.md) que proporcionan características adicionales.

## <a name="comboboxex-control-items"></a>Elementos de control ComboBoxEx

Los controles ComboBoxEx mantienen la información de los elementos mediante una estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) . Esta estructura incluye los miembros de los índices de elementos, los índices de imagen (normal, el estado de selección y la superposición), los valores de sangría, las cadenas de texto y los valores específicos del elemento.

El control ComboBoxEx proporciona un acceso sencillo a los elementos y su manipulación mediante mensajería. Para agregar o eliminar un elemento, envíe el mensaje [**CBEM \_ INSERTITEM**](cbem-insertitem.md) o [**CBEM \_ DELETEITEM**](cbem-deleteitem.md) . Puede modificar los elementos que se encuentran actualmente en el control mediante el mensaje [**CBEM \_ SETITEM**](cbem-setitem.md) .

## <a name="callback-items"></a>Elementos de devolución de llamada

Los controles ComboBoxEx admiten atributos de elementos de devolución de llamada. Puede especificar un elemento como un elemento de devolución de llamada cuando lo agregue al control mediante [**CBEM \_ INSERTITEM**](cbem-insertitem.md). Al asignar valores a la estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) de un elemento, debe especificar los valores adecuados de la marca de devolución de llamada. A continuación se muestran los miembros de la estructura **COMBOBOXEXITEM** y sus correspondientes valores de marca de devolución de llamada.



| Miembro             | Valor de devolución de llamada      |
|--------------------|---------------------|
| **Miembros pszText**        | LPSTR \_ TEXTCALLBACK |
| **iImage**         | I \_ IMAGECALLBACK    |
| **iSelectedImage** | I \_ IMAGECALLBACK    |
| **iOverlay**       | I \_ IMAGECALLBACK    |
| **iIndent**        | I \_ INDENTCALLBACK   |



 

El control solicitará información sobre los elementos de devolución de llamada mediante el envío de códigos de notificación de [CBEN \_ GETDISPINFO](cben-getdispinfo.md) . Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) . Cuando la aplicación procesa este mensaje, debe proporcionar la información solicitada para el control. Si establece el miembro de **máscara** de la estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que lo acompaña en CBEIF \_ di \_ SETITEM, el control almacenará los datos del elemento y no volverá a solicitarlo.

## <a name="comboboxex-control-image-lists"></a>Listas de imágenes del control ComboBoxEx

Si desea que un control ComboBoxEx muestre iconos con elementos, debe proporcionar una lista de imágenes. Los controles ComboBoxEx admiten hasta tres imágenes para un elemento, una para su estado seleccionado, una para su estado no seleccionado y otra para una imagen superpuesta. Asignar una lista de imágenes existente a un control ComboBoxEx mediante el mensaje [**\_ SETIMAGELIST de CBEM**](cbem-setimagelist.md) .

La estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) contiene miembros que representan los índices de imagen de cada lista de imágenes (seleccionada, no seleccionada y superposición). Para cada elemento, establezca estos miembros para mostrar las imágenes deseadas. No es necesario especificar índices de imagen para cada tipo de imagen. Puede mezclar y hacer coincidir los tipos de imagen como desee, pero siempre establezca el miembro de **máscara** de la estructura **COMBOBOXEXITEM** para indicar qué miembros se están usando. El control omite los miembros que no se han marcado como válidos.

> [!Note]  
> Si usa el estilo [**\_ simple CBS**](combo-box-styles.md) , no se muestran los iconos.

 

## <a name="about-comboboxex-control-notification-messages"></a>Acerca de los mensajes de notificación del control ComboBoxEx

Un control ComboBoxEx envía mensajes de notificación para informar sobre los cambios en sí mismo o para solicitar información de elementos de devolución de llamada. El elemento primario del control recibe todos los mensajes de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) del cuadro combinado incluido en el control ComboBoxEx. El control ComboBoxEx envía sus propias notificaciones mediante mensajes de [**\_ notificación de WM**](wm-notify.md) . Como resultado, el propietario del control debe estar preparado para procesar ambas formas de mensajes de notificación.

A continuación se muestran los códigos de notificación específicos de ComboBoxEx que se envían a través de mensajes de [**\_ notificación de WM**](wm-notify.md) .



| notificación                              | **Descripción**                                                                                                            |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)     | Indica que el usuario ha activado la lista desplegable o hace clic en él en el cuadro de edición del control.                               |
| [CBEN \_ ENDEDIT](cben-endedit.md)         | Indica que el usuario ha seleccionado un elemento de la lista desplegable o ha finalizado una operación de edición en el cuadro de edición. |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)   | Informa de que se ha eliminado un elemento.                                                                                          |
| [CBEN \_ GETDISPINFO](cben-getdispinfo.md) | Solicita información sobre los atributos de un elemento.                                                                           |
| [CBEN \_ INSERTITEM](cben-insertitem.md)   | Indica que se ha insertado un elemento en el control.                                                                          |



 

## <a name="comboboxex-control-message-forwarding"></a>Reenvío de mensajes del control ComboBoxEx

A continuación se muestran los mensajes de cuadro combinado estándar que un control ComboBoxEx reenvía a su cuadro combinado secundario. Algunos de estos mensajes pueden ser procesados por el control ComboBoxEx antes o después de que el mensaje se haya reenviado.

-   [**CB \_ DELETESTRING**](cb-deletestring.md)
-   [**CB \_ FindExactString con**](cb-findstringexact.md)
-   [**\_GETCOUNT.**](cb-getcount.md)
-   [**CB \_ GETCURSEL**](cb-getcursel.md)
-   [**CB \_ GETDROPPEDCONTROLRECT**](cb-getdroppedcontrolrect.md)
-   [**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
-   [**CB \_ GETITEMDATA**](cb-getitemdata.md)
-   [**CB \_ GETITEMHEIGHT**](cb-getitemheight.md)
-   [**CB \_ GETLBTEXT**](cb-getlbtext.md)
-   [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md)
-   [**CB \_ GETEXTENDEDUI**](cb-getextendedui.md)
-   [**CB \_ LIMITTEXT**](cb-limittext.md)
-   [**CB \_ RESETCONTENT**](cb-resetcontent.md)
-   [**CB \_ SETCURSEL**](cb-setcursel.md)
-   [**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md)
-   [**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)
-   [**CB \_ SETITEMDATA**](cb-setitemdata.md)
-   [**CB \_ SETITEMHEIGHT**](cb-setitemheight.md)
-   [**CB \_ SHOWDROPDOWN**](cb-showdropdown.md)

A continuación se muestran los mensajes de Windows que un control ComboBoxEx reenvía a su ventana primaria:

-   [**WM \_ (Esto**](/windows/desktop/menurc/wm-command) incluye todas las \_ notificaciones de CBN).
-   [**\_notificaciones de WM**](wm-notify.md)

 

 