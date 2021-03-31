---
title: Mensajes de control
description: Esta sección contiene información sobre cómo se usan los mensajes de Windows para comunicarse con los controles.
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923a1b47d625a2797a900a6c582d00c5169097f3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904930"
---
# <a name="control-messages"></a>Mensajes de control

Esta sección contiene información sobre cómo se usan los mensajes de Windows para comunicarse con los controles.

Se tratan los temas siguientes.

-   [Mensajes a controles comunes](#messages-to-common-controls)
-   [Notificaciones de controles](#notifications-from-controls)
-   [Temas relacionados](#related-topics)

## <a name="messages-to-common-controls"></a>Mensajes a controles comunes

Dado que los controles comunes son Windows, una aplicación puede comunicarse con ellos mediante mensajes comunes de Microsoft Win32, como [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont) o [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext). Además, la clase de ventana de cada control común admite un conjunto de mensajes específicos del control. Normalmente, una aplicación usa [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) para pasar mensajes al control (a menudo recibe información en el valor devuelto).

Algunos controles comunes también tienen un conjunto de macros que una aplicación puede usar en lugar de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage). Las macros suelen ser más fáciles de usar que las funciones. En el ejemplo de código siguiente se recupera el texto del elemento de vista de árbol seleccionado, primero mediante los mensajes sin formato y el segundo mediante las macros equivalentes. Supongamos que *hWnd* es el identificador de la ventana de control.


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



Cuando se realiza un cambio en la configuración de color del sistema, Windows envía un mensaje de [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) a todas las ventanas de nivel superior. La ventana de nivel superior debe reenviar el mensaje de **\_ SYSCOLORCHANGE de WM** a sus controles comunes; de lo contrario, los controles no recibirán una notificación del cambio de color. Al reenviar el mensaje se garantiza que los colores utilizados por los controles comunes son coherentes con los utilizados por otros objetos de la interfaz de usuario. Por ejemplo, un control de barra de herramientas usa el color "objetos 3D" para dibujar sus botones. Si el usuario cambia el color del objeto 3D, pero el mensaje **de \_ SYSCOLORCHANGE de WM** no se reenvía a la barra de herramientas, los botones de la barra de herramientas permanecen en su color original (o incluso cambian a una combinación de colores antiguos y nuevos) mientras el color de otros botones del sistema cambia.

## <a name="notifications-from-controls"></a>Notificaciones de controles

Los controles son ventanas secundarias que envían mensajes de notificación a la ventana primaria cuando los eventos, normalmente desencadenados por la entrada del usuario, se producen en el control. La aplicación se basa en estos mensajes de notificación para determinar qué acción desea que realice el usuario. A excepción de trackbars, que usa los mensajes de [**WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md) para notificar a su elemento primario de los cambios, los controles comunes envían notificaciones como [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) o de [**\_ notificaciones de WM**](wm-notify.md) , tal como se especifica en el tema de referencia de la notificación. Normalmente, las notificaciones anteriores (las que han estado en la API durante mucho tiempo) usan **el \_ comando de WM**.

El parámetro *lParam* de [**WM \_ Notify**](wm-notify.md) es la dirección de una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) o la dirección de una estructura mayor que incluye **NMHDR** como primer miembro. La estructura contiene el código de notificación e identifica el control común que envió el mensaje de notificación. El significado del resto de miembros de la estructura, si los hay, varía en función del código de notificación.

Cada tipo de control común tiene un conjunto correspondiente de códigos de notificación. La biblioteca de controles comunes también proporciona códigos de notificación que se pueden enviar por más de un tipo de control común. Consulte la documentación del control de interés para determinar qué códigos de notificación enviará y qué formato deben tomar.

Para ver un ejemplo de código que muestra cómo controlar los mensajes de [**\_ notificación de WM**](wm-notify.md) , consulte el tema de referencia de ese mensaje.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control general](common-control-reference.md)
</dt> </dl>

 

 
