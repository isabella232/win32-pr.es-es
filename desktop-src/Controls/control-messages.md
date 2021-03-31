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
# <a name="control-messages"></a><span data-ttu-id="24087-103">Mensajes de control</span><span class="sxs-lookup"><span data-stu-id="24087-103">Control Messages</span></span>

<span data-ttu-id="24087-104">Esta sección contiene información sobre cómo se usan los mensajes de Windows para comunicarse con los controles.</span><span class="sxs-lookup"><span data-stu-id="24087-104">This section contains information about how Windows messages are used to communicate with controls.</span></span>

<span data-ttu-id="24087-105">Se tratan los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="24087-105">The following topics are discussed.</span></span>

-   [<span data-ttu-id="24087-106">Mensajes a controles comunes</span><span class="sxs-lookup"><span data-stu-id="24087-106">Messages to Common Controls</span></span>](#messages-to-common-controls)
-   [<span data-ttu-id="24087-107">Notificaciones de controles</span><span class="sxs-lookup"><span data-stu-id="24087-107">Notifications from Controls</span></span>](#notifications-from-controls)
-   [<span data-ttu-id="24087-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24087-108">Related topics</span></span>](#related-topics)

## <a name="messages-to-common-controls"></a><span data-ttu-id="24087-109">Mensajes a controles comunes</span><span class="sxs-lookup"><span data-stu-id="24087-109">Messages to Common Controls</span></span>

<span data-ttu-id="24087-110">Dado que los controles comunes son Windows, una aplicación puede comunicarse con ellos mediante mensajes comunes de Microsoft Win32, como [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont) o [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext).</span><span class="sxs-lookup"><span data-stu-id="24087-110">Because common controls are windows, an application can communicate with them by using common Microsoft Win32 messages such as [**WM\_GETFONT**](/windows/desktop/winmsg/wm-getfont) or [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span> <span data-ttu-id="24087-111">Además, la clase de ventana de cada control común admite un conjunto de mensajes específicos del control.</span><span class="sxs-lookup"><span data-stu-id="24087-111">In addition, the window class of each common control supports a set of control-specific messages.</span></span> <span data-ttu-id="24087-112">Normalmente, una aplicación usa [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) para pasar mensajes al control (a menudo recibe información en el valor devuelto).</span><span class="sxs-lookup"><span data-stu-id="24087-112">Typically, an application uses [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) or [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) to pass messages to the control (often receiving information in the return value).</span></span>

<span data-ttu-id="24087-113">Algunos controles comunes también tienen un conjunto de macros que una aplicación puede usar en lugar de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="24087-113">Some common controls also have a set of macros that an application can use instead of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="24087-114">Las macros suelen ser más fáciles de usar que las funciones.</span><span class="sxs-lookup"><span data-stu-id="24087-114">The macros are typically easier to use than the functions.</span></span> <span data-ttu-id="24087-115">En el ejemplo de código siguiente se recupera el texto del elemento de vista de árbol seleccionado, primero mediante los mensajes sin formato y el segundo mediante las macros equivalentes.</span><span class="sxs-lookup"><span data-stu-id="24087-115">The following example code retrieves the text of the selected tree-view item, first by using the raw messages, and second by using the equivalent macros.</span></span> <span data-ttu-id="24087-116">Supongamos que *hWnd* es el identificador de la ventana de control.</span><span class="sxs-lookup"><span data-stu-id="24087-116">Assume that *hwnd* is the handle of the control window.</span></span>


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



<span data-ttu-id="24087-117">Cuando se realiza un cambio en la configuración de color del sistema, Windows envía un mensaje de [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) a todas las ventanas de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="24087-117">When a change is made to the system color settings, Windows sends a [**WM\_SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) message to all top-level windows.</span></span> <span data-ttu-id="24087-118">La ventana de nivel superior debe reenviar el mensaje de **\_ SYSCOLORCHANGE de WM** a sus controles comunes; de lo contrario, los controles no recibirán una notificación del cambio de color.</span><span class="sxs-lookup"><span data-stu-id="24087-118">Your top-level window must forward the **WM\_SYSCOLORCHANGE** message to its common controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="24087-119">Al reenviar el mensaje se garantiza que los colores utilizados por los controles comunes son coherentes con los utilizados por otros objetos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="24087-119">Forwarding the message ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="24087-120">Por ejemplo, un control de barra de herramientas usa el color "objetos 3D" para dibujar sus botones.</span><span class="sxs-lookup"><span data-stu-id="24087-120">For example, a toolbar control uses the "3-D Objects" color to draw its buttons.</span></span> <span data-ttu-id="24087-121">Si el usuario cambia el color del objeto 3D, pero el mensaje **de \_ SYSCOLORCHANGE de WM** no se reenvía a la barra de herramientas, los botones de la barra de herramientas permanecen en su color original (o incluso cambian a una combinación de colores antiguos y nuevos) mientras el color de otros botones del sistema cambia.</span><span class="sxs-lookup"><span data-stu-id="24087-121">If the user changes the 3-D Object's color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color (or even change to a combination of old and new colors) while the color of other buttons in the system changes.</span></span>

## <a name="notifications-from-controls"></a><span data-ttu-id="24087-122">Notificaciones de controles</span><span class="sxs-lookup"><span data-stu-id="24087-122">Notifications from Controls</span></span>

<span data-ttu-id="24087-123">Los controles son ventanas secundarias que envían mensajes de notificación a la ventana primaria cuando los eventos, normalmente desencadenados por la entrada del usuario, se producen en el control.</span><span class="sxs-lookup"><span data-stu-id="24087-123">Controls are child windows that send notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="24087-124">La aplicación se basa en estos mensajes de notificación para determinar qué acción desea que realice el usuario.</span><span class="sxs-lookup"><span data-stu-id="24087-124">The application relies on these notification messages to determine what action the user wants it to take.</span></span> <span data-ttu-id="24087-125">A excepción de trackbars, que usa los mensajes de [**WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md) para notificar a su elemento primario de los cambios, los controles comunes envían notificaciones como [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) o de [**\_ notificaciones de WM**](wm-notify.md) , tal como se especifica en el tema de referencia de la notificación.</span><span class="sxs-lookup"><span data-stu-id="24087-125">Except for trackbars, which use the [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages to notify their parent of changes, common controls send notifications as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages, as specified in the reference topic for the notification.</span></span> <span data-ttu-id="24087-126">Normalmente, las notificaciones anteriores (las que han estado en la API durante mucho tiempo) usan **el \_ comando de WM**.</span><span class="sxs-lookup"><span data-stu-id="24087-126">Typically, older notifications (those that have been in the API for a long time) use **WM\_COMMAND**.</span></span>

<span data-ttu-id="24087-127">El parámetro *lParam* de [**WM \_ Notify**](wm-notify.md) es la dirección de una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) o la dirección de una estructura mayor que incluye **NMHDR** como primer miembro.</span><span class="sxs-lookup"><span data-stu-id="24087-127">The *lParam* parameter of [**WM\_NOTIFY**](wm-notify.md) is either the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure or the address of a larger structure that includes **NMHDR** as its first member.</span></span> <span data-ttu-id="24087-128">La estructura contiene el código de notificación e identifica el control común que envió el mensaje de notificación.</span><span class="sxs-lookup"><span data-stu-id="24087-128">The structure contains the notification code and identifies the common control that sent the notification message.</span></span> <span data-ttu-id="24087-129">El significado del resto de miembros de la estructura, si los hay, varía en función del código de notificación.</span><span class="sxs-lookup"><span data-stu-id="24087-129">The meaning of the remaining structure members, if any, varies depending on the notification code.</span></span>

<span data-ttu-id="24087-130">Cada tipo de control común tiene un conjunto correspondiente de códigos de notificación.</span><span class="sxs-lookup"><span data-stu-id="24087-130">Each type of common control has a corresponding set of notification codes.</span></span> <span data-ttu-id="24087-131">La biblioteca de controles comunes también proporciona códigos de notificación que se pueden enviar por más de un tipo de control común.</span><span class="sxs-lookup"><span data-stu-id="24087-131">The common control library also provides notification codes that can be sent by more than one type of common control.</span></span> <span data-ttu-id="24087-132">Consulte la documentación del control de interés para determinar qué códigos de notificación enviará y qué formato deben tomar.</span><span class="sxs-lookup"><span data-stu-id="24087-132">See the documentation for the control of interest to determine which notification codes it will send and what format they take.</span></span>

<span data-ttu-id="24087-133">Para ver un ejemplo de código que muestra cómo controlar los mensajes de [**\_ notificación de WM**](wm-notify.md) , consulte el tema de referencia de ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="24087-133">For example code showing how to handle [**WM\_NOTIFY**](wm-notify.md) messages, see the reference topic for that message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24087-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24087-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24087-135">Referencia de control general</span><span class="sxs-lookup"><span data-stu-id="24087-135">General Control Reference</span></span>](common-control-reference.md)
</dt> </dl>

 

 
