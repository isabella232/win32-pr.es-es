---
title: Acerca de los controles ComboBoxEx
description: Los controles ComboBoxEx son controles de cuadro combinado que proporcionan compatibilidad nativa con imágenes de elementos.
ms.assetid: a4b1aa79-40c4-4eff-801c-4f308d86fb35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993fa8db73246c62f8ceee805e767c13ffdcc15a12d0222e09f308324cc97bab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831841"
---
# <a name="about-comboboxex-controls"></a>Acerca de los controles ComboBoxEx

Los controles ComboBoxEx son controles de cuadro combinado que proporcionan compatibilidad nativa con imágenes de elementos. Para que las imágenes de elementos se puedan acceder fácilmente, el control proporciona compatibilidad con la lista de imágenes. Con este control, puede proporcionar la funcionalidad de un cuadro combinado sin tener que dibujar manualmente gráficos de elementos.

En este tema se incluyen las siguientes secciones.

-   [Crear controles ComboBoxEx](#creating-comboboxex-controls)
-   [Estilos de control ComboBoxEx](#comboboxex-control-styles)
-   [Elementos de control ComboBoxEx](#comboboxex-control-items)
-   [Elementos de devolución de llamada](#callback-items)
-   [Listas de imágenes de control ComboBoxEx](#comboboxex-control-image-lists)
-   [Acerca de los mensajes de notificación del control ComboBoxEx](#about-comboboxex-control-notification-messages)
-   [Reenvío de mensajes del control ComboBoxEx](#comboboxex-control-message-forwarding)

## <a name="creating-comboboxex-controls"></a>Crear controles ComboBoxEx

De hecho, un control ComboBoxEx crea un cuadro combinado secundario y realiza tareas de dibujo del propietario automáticamente en función de una lista de imágenes asignada. Por lo tanto, [**el estilo \_ CBS OWNERDRAWFIXED**](combo-box-styles.md) está implícito y no es necesario usarlo al crear el control. Dado que las listas de imágenes se usan para proporcionar gráficos de elementos, no se puede usar el estilo [**\_ CBS OWNERDRAWVARIABLE.**](combo-box-styles.md)

Un control ComboBoxEx se debe inicializar mediante una llamada a la función [**InitCommonControlsEx,**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) especificando LAS CLASES DE USEREX DE LA REGLA EN LA ESTRUCTURA \_ \_ [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) que lo acompaña.

Puede crear un control ComboBoxEx mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y [**especificando WC \_ COMBOBOXEX como**](common-control-window-classes.md) clase de ventana. La clase se registra cuando se llama a [**la función InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) como se explicó anteriormente.

Los controles ComboBoxEx se crean sin una lista de imágenes predeterminada. Para usar imágenes de elementos, debe crear una lista de imágenes para el control ComboBoxEx y asignarla al control mediante el mensaje [**\_ SETIMAGELIST de CBEM.**](cbem-setimagelist.md) Si no asigna una lista de imágenes al control ComboBoxEx, el control solo muestra texto de elemento.

## <a name="comboboxex-control-styles"></a>Estilos de control ComboBoxEx

Los controles ComboBoxEx solo admiten los siguientes estilos comboBox:

-   CBS \_ SIMPLE
-   LISTA DESPLEGABLE DE CBS \_
-   LISTA DESPLEGABLE DE CBS \_
-   WS \_ CHILD

También hay varios estilos extendidos [de control ComboBoxEx](comboboxex-control-extended-styles.md) que solo se usan en ComboBoxEx.

> [!Note]  
> Es posible que el estilo SIMPLE de [**\_ CBS**](combo-box-styles.md) no funcione correctamente en algunos casos.

 

Dado que el control ComboBoxEx realiza tareas de dibujo del propietario automáticamente en función de una lista de imágenes asignada, el estilo [**\_ OWNERDRAWFIXED**](combo-box-styles.md) de CBS está implícito; no es necesario usarlo al crear el control. Dado que las listas de imágenes se usan para proporcionar gráficos de elementos, no se puede usar el estilo [**\_ CBS OWNERDRAWVARIABLE.**](combo-box-styles.md) El control ComboBoxEx también admite estilos extendidos de [control ComboBoxEx](comboboxex-control-extended-styles.md) que proporcionan características adicionales.

## <a name="comboboxex-control-items"></a>Elementos de control ComboBoxEx

Los controles ComboBoxEx mantienen información de elementos mediante [**una estructura COMBOBOXEXITEM.**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) Esta estructura incluye miembros para índices de elementos, índices de imagen (normal, estado de selección y superposición), valores de sangría, cadenas de texto y valores específicos del elemento.

El control ComboBoxEx proporciona acceso fácil y manipulación de elementos a través de mensajería. Para agregar o eliminar un elemento, envíe el [**mensaje CBEM \_ INSERTITEM**](cbem-insertitem.md) o [**CBEM \_ DELETEITEM.**](cbem-deleteitem.md) Puede modificar elementos actualmente en el control mediante el [**mensaje \_ SETITEM de CBEM.**](cbem-setitem.md)

## <a name="callback-items"></a>Elementos de devolución de llamada

Los controles ComboBoxEx admiten atributos de elemento de devolución de llamada. Puede especificar un elemento como elemento de devolución de llamada al agregarlo al control mediante [**CBEM \_ INSERTITEM**](cbem-insertitem.md). Al asignar valores a la estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) de un elemento, debe especificar los valores de marca de devolución de llamada adecuados. Los siguientes son los **miembros de la estructura COMBOBOXEXITEM** y sus valores de marca de devolución de llamada correspondientes.



| Miembro             | Valor de devolución de llamada      |
|--------------------|---------------------|
| **pszText**        | LPSTR \_ TEXTCALLBACK |
| **iImage**         | I \_ IMAGECALLBACK    |
| **iSelectedImage** | I \_ IMAGECALLBACK    |
| **iOverlay**       | I \_ IMAGECALLBACK    |
| **iIndent**        | I \_ INDENTCALLBACK   |



 

El control solicitará información sobre los elementos de devolución de llamada mediante el envío de [códigos de notificación \_ GETDISPINFO de CBEN.](cben-getdispinfo.md) Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) Cuando la aplicación procesa este mensaje, debe proporcionar la información solicitada para el control. Si establece el miembro **mask** de la estructura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que lo acompaña en CBEIF \_ DI SETITEM, el control almacenará los datos del elemento y no los volverá a \_ solicitar.

## <a name="comboboxex-control-image-lists"></a>Listas de imágenes de control ComboBoxEx

Si desea que un control ComboBoxEx muestre iconos con elementos, debe proporcionar una lista de imágenes. Los controles ComboBoxEx admiten hasta tres imágenes para un elemento: una para su estado seleccionado, otra para su estado no seleccionado y otra para una imagen superpuesta. Asigne una lista de imágenes existente a un control ComboBoxEx mediante el [**mensaje \_ SETIMAGELIST de CBEM.**](cbem-setimagelist.md)

La [**estructura COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) contiene miembros que representan los índices de imagen para cada lista de imágenes (seleccionada, no seleccionada y superpuesta). Para cada elemento, establezca estos miembros para mostrar las imágenes deseadas. No es necesario especificar índices de imagen para cada tipo de imagen. Puede combinar y hacer coincidir los tipos de imagen como quiera, pero siempre establezca el miembro **mask** de la **estructura COMBOBOXEXITEM** para indicar qué miembros se usan. El control omite los miembros que no se han marcado como válidos.

> [!Note]  
> Si usa el estilo [**\_ SIMPLE de CBS,**](combo-box-styles.md) no se muestran los iconos.

 

## <a name="about-comboboxex-control-notification-messages"></a>Acerca de los mensajes de notificación del control ComboBoxEx

Un control ComboBoxEx envía mensajes de notificación para notificar cambios dentro de sí mismo o para solicitar información del elemento de devolución de llamada. El elemento primario del control recibe todos los [**mensajes \_ WM COMMAND**](/windows/desktop/menurc/wm-command) del cuadro combinado incluido en el control ComboBoxEx. El control ComboBoxEx envía sus propias notificaciones mediante [**mensajes \_ WM NOTIFY.**](wm-notify.md) Como resultado, el propietario del control debe estar preparado para procesar ambas formas de mensajes de notificación.

A continuación se encuentran los códigos de notificación específicos de ComboBoxEx que se envían a través [**de mensajes \_ WM NOTIFY.**](wm-notify.md)



| Notificación                              | **Descripción**                                                                                                            |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)     | Indica que el usuario ha activado la lista desplegable o ha hecho clic en el cuadro de edición del control.                               |
| [CBEN \_ ENDEDIT](cben-endedit.md)         | Indica que el usuario ha seleccionado un elemento de la lista desplegable o ha concluido una operación de edición en el cuadro de edición. |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)   | Informa de que se eliminó un elemento.                                                                                          |
| [GETDISPINFO DE CBEN \_](cben-getdispinfo.md) | Solicita información sobre los atributos de un elemento.                                                                           |
| [CBEN \_ INSERTITEM](cben-insertitem.md)   | Indica que se insertó un elemento en el control .                                                                          |



 

## <a name="comboboxex-control-message-forwarding"></a>Reenvío de mensajes del control ComboBoxEx

Los siguientes son los mensajes de cuadro combinado estándar que un control ComboBoxEx reenvía a su cuadro combinado secundario. El control ComboBoxEx puede procesar algunos de estos mensajes antes o después de que se haya reenviado el mensaje.

-   [**CB \_ DELETESTRING**](cb-deletestring.md)
-   [**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
-   [**CB \_ GETCOUNT**](cb-getcount.md)
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

Estos son los mensajes de Windows que un control ComboBoxEx reenvía a su ventana primaria:

-   [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) (esto incluye todas las notificaciones \_ CBN).
-   [**WM \_ NOTIFY**](wm-notify.md)

 

 