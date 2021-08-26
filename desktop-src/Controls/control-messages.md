---
title: Mensajes de control
description: Esta sección contiene información sobre cómo se usan Windows mensajes para comunicarse con los controles.
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed60ebb66341332b6248b8427045abc5b62a2311427d56e46b25fe93b3d899ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921105"
---
# <a name="control-messages"></a>Mensajes de control

Esta sección contiene información sobre cómo se usan Windows mensajes para comunicarse con los controles.

Se tratan los temas siguientes.

-   [Mensajes a controles comunes](#messages-to-common-controls)
-   [Notificaciones de controles](#notifications-from-controls)
-   [Temas relacionados](#related-topics)

## <a name="messages-to-common-controls"></a>Mensajes a controles comunes

Dado que los controles comunes son ventanas, una aplicación puede comunicarse con ellos mediante mensajes comunes de Microsoft Win32, como [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont) o [**WM \_ SETTEXT.**](/windows/desktop/winmsg/wm-settext) Además, la clase window de cada control común admite un conjunto de mensajes específicos del control. Normalmente, una aplicación usa [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o [**SendDlgItemMessage para**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) pasar mensajes al control (a menudo recibiendo información en el valor devuelto).

Algunos controles comunes también tienen un conjunto de macros que una aplicación puede usar en lugar de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage). Las macros suelen ser más fáciles de usar que las funciones. El código de ejemplo siguiente recupera el texto del elemento de vista de árbol seleccionado, primero mediante los mensajes sin procesar y, en segundo lugar, mediante las macros equivalentes. Suponga que *hwnd* es el identificador de la ventana de control.


```
BOOL fSuccess;
WCHAR itemText[99];
TVITEM tvItem = { 0 };
tvItem.mask = TVIF_TEXT;
tvItem.cchTextMax = ARRAYSIZE(itemText);
tvItem.pszText = itemText;

// This...
tvItem.hItem = (HTREEITEM)SendMessage(hwnd, TVM_GETNEXTITEM, TVGN_CARET, NULL);
fSuccess = SendMessage(hwnd, TVM_GETITEM, 0, (LPARAM)&tvItem);

// ... is equivalent to this.
tvItem.hItem = TreeView_GetSelection(hwnd);
fSuccess = TreeView_GetItem(hwnd, &tvItem);
```



Cuando se realiza un cambio en la configuración de color del sistema, Windows un mensaje [**\_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) de WM a todas las ventanas de nivel superior. La ventana de nivel superior debe reenviar el mensaje **\_ SYSCOLORCHANGE** de WM a sus controles comunes; de lo contrario, los controles no recibirán una notificación del cambio de color. El reenvío del mensaje garantiza que los colores usados por los controles comunes son coherentes con los que usan otros objetos de interfaz de usuario. Por ejemplo, un control de barra de herramientas usa el color "Objetos 3D" para dibujar sus botones. Si el usuario cambia el color del objeto 3D pero el mensaje **\_ SYSCOLORCHANGE** de WM no se reenvía a la barra de herramientas, los botones de la barra de herramientas permanecerán en su color original (o incluso cambiarán a una combinación de colores antiguos y nuevos) mientras cambia el color de otros botones del sistema.

## <a name="notifications-from-controls"></a>Notificaciones de controles

Los controles son ventanas secundarias que envían mensajes de notificación a la ventana primaria cuando se producen eventos, normalmente desencadenados por la entrada del usuario, en el control . La aplicación se basa en estos mensajes de notificación para determinar qué acción quiere realizar el usuario. A excepción de las barras de seguimiento, que usan los mensajes [**WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md) para notificar a su elemento primario los cambios, los controles comunes envían notificaciones como mensajes [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) o [**WM \_ NOTIFY,**](wm-notify.md) como se especifica en el tema de referencia de la notificación. Normalmente, las notificaciones anteriores (las que han estado en la API durante mucho tiempo) usan **WM \_ COMMAND**.

El *parámetro lParam* de [**WM \_ NOTIFY**](wm-notify.md) es la dirección de una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) o la dirección de una estructura mayor que incluye **NMHDR** como su primer miembro. La estructura contiene el código de notificación e identifica el control común que envió el mensaje de notificación. El significado de los miembros de estructura restantes, si los hay, varía en función del código de notificación.

Cada tipo de control común tiene un conjunto correspondiente de códigos de notificación. La biblioteca de controles común también proporciona códigos de notificación que se pueden enviar mediante más de un tipo de control común. Consulte la documentación sobre el control de interés para determinar qué códigos de notificación enviará y qué formato toman.

Para obtener código de ejemplo que muestra cómo controlar [**mensajes \_ WM NOTIFY,**](wm-notify.md) vea el tema de referencia de ese mensaje.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control general](common-control-reference.md)
</dt> </dl>

 

 
