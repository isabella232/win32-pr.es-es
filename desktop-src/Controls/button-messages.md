---
title: 'Mensajes de botón '
description: Un botón puede enviar mensajes a su ventana primaria y una ventana primaria puede enviar mensajes a un botón.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1601f269ec1242a10579d2ace812723d3ead7f84
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103796683"
---
# <a name="button-messages"></a><span data-ttu-id="dc729-103">Mensajes de botón </span><span class="sxs-lookup"><span data-stu-id="dc729-103">Button Messages</span></span>

<span data-ttu-id="dc729-104">Un botón puede enviar mensajes a su ventana primaria y una ventana primaria puede enviar mensajes a un botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-104">A button can send messages to its parent window, and a parent window can send messages to a button.</span></span>

<span data-ttu-id="dc729-105">Los temas siguientes se describen en esta sección.</span><span class="sxs-lookup"><span data-stu-id="dc729-105">The following topics are discussed in this section.</span></span>

-   [<span data-ttu-id="dc729-106">Envío de mensajes a botones</span><span class="sxs-lookup"><span data-stu-id="dc729-106">Sending Messages to Buttons</span></span>](#sending-messages-to-buttons)
-   [<span data-ttu-id="dc729-107">Control de mensajes desde un botón</span><span class="sxs-lookup"><span data-stu-id="dc729-107">Handling Messages from a Button</span></span>](#handling-messages-from-a-button)
-   [<span data-ttu-id="dc729-108">Mensajes de notificación de los botones</span><span class="sxs-lookup"><span data-stu-id="dc729-108">Notification Messages from Buttons</span></span>](#notification-messages-from-buttons)
-   [<span data-ttu-id="dc729-109">Mensajes de color de botón</span><span class="sxs-lookup"><span data-stu-id="dc729-109">Button Color Messages</span></span>](#button-color-messages)
-   [<span data-ttu-id="dc729-110">Procesamiento de mensajes predeterminado del botón</span><span class="sxs-lookup"><span data-stu-id="dc729-110">Button Default Message Processing</span></span>](#button-default-message-processing)
-   [<span data-ttu-id="dc729-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dc729-111">Related topics</span></span>](#related-topics)

## <a name="sending-messages-to-buttons"></a><span data-ttu-id="dc729-112">Envío de mensajes a botones</span><span class="sxs-lookup"><span data-stu-id="dc729-112">Sending Messages to Buttons</span></span>

<span data-ttu-id="dc729-113">Una ventana primaria puede enviar mensajes a un botón de una ventana superpuesta o secundaria mediante la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , o bien puede enviar mensajes a un botón de un cuadro de diálogo mediante las funciones [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)y [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .</span><span class="sxs-lookup"><span data-stu-id="dc729-113">A parent window can send messages to a button in an overlapped or child window by using the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, or it can send messages to a button in a dialog box by using the [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton), and [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) functions.</span></span>

<span data-ttu-id="dc729-114">Una aplicación puede usar el [**mensaje \_ GETCHECK de BM**](bm-getcheck.md) para recuperar el estado de activación de una casilla o un botón de radio.</span><span class="sxs-lookup"><span data-stu-id="dc729-114">An application can use the [**BM\_GETCHECK**](bm-getcheck.md) message to retrieve the check state of a check box or radio button.</span></span> <span data-ttu-id="dc729-115">Una aplicación también puede usar el [**mensaje \_ GETSTATE de BM**](bm-getstate.md) para recuperar los Estados actuales del botón (el estado de activación, el estado de inserción y el estado de foco).</span><span class="sxs-lookup"><span data-stu-id="dc729-115">An application can also use the [**BM\_GETSTATE**](bm-getstate.md) message to retrieve the button's current states (the check state, push state, and focus state).</span></span> <span data-ttu-id="dc729-116">Para obtener información acerca de un estado específico, use una máscara de máscara en el valor de estado devuelto.</span><span class="sxs-lookup"><span data-stu-id="dc729-116">To get information about a specific state, use a bitmask on the returned state value.</span></span>

<span data-ttu-id="dc729-117">El mensaje [**BM \_ SETCHECK**](bm-setcheck.md) establece el estado de activación de una casilla o un botón de opción; el mensaje devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="dc729-117">The [**BM\_SETCHECK**](bm-setcheck.md) message sets the check state of a check box or radio button; the message returns zero.</span></span> <span data-ttu-id="dc729-118">El mensaje de [**BM \_ SETSTATE**](bm-setstate.md) establece el estado de la extracción de un botón; este mensaje también devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="dc729-118">The [**BM\_SETSTATE**](bm-setstate.md) message sets the push state of a button; this message also returns zero.</span></span> <span data-ttu-id="dc729-119">El [**mensaje \_ SETSTYLE de BM**](bm-setstyle.md) cambia el estilo de un botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-119">The [**BM\_SETSTYLE**](bm-setstyle.md) message changes the style of a button.</span></span> <span data-ttu-id="dc729-120">Está diseñado para cambiar los estilos de botón dentro de un tipo (por ejemplo, si se cambia una casilla a una casilla automática).</span><span class="sxs-lookup"><span data-stu-id="dc729-120">It is designed for changing button styles within a type (for example, changing a check box to an automatic check box).</span></span> <span data-ttu-id="dc729-121">No está diseñado para cambiar entre tipos (por ejemplo, al cambiar una casilla a un botón de radio).</span><span class="sxs-lookup"><span data-stu-id="dc729-121">It is not designed for changing between types (for example, changing a check box to a radio button).</span></span> <span data-ttu-id="dc729-122">Una aplicación no debe cambiar un botón de un tipo a otro.</span><span class="sxs-lookup"><span data-stu-id="dc729-122">An application should not change a button from one type to another.</span></span>

<span data-ttu-id="dc729-123">Un botón del estilo de [**\_ icono**](button-styles.md) de [**mapa de \_ bits BS**](button-styles.md) o BS muestra un mapa de bits o un icono en lugar de texto.</span><span class="sxs-lookup"><span data-stu-id="dc729-123">A button of the [**BS\_BITMAP**](button-styles.md) or [**BS\_ICON**](button-styles.md) style displays a bitmap or icon instead of text.</span></span> <span data-ttu-id="dc729-124">El mensaje de el [**\_ SETIMAGE de BM**](bm-setimage.md) asocia un identificador a un mapa de bits o un icono con un botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-124">The [**BM\_SETIMAGE**](bm-setimage.md) message associates a handle to a bitmap or icon with a button.</span></span> <span data-ttu-id="dc729-125">El [**mensaje \_ BM de BM**](bm-getimage.md) recupera un identificador para el mapa de bits o el icono asociado a un botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-125">The [**BM\_GETIMAGE**](bm-getimage.md) message retrieves a handle to the bitmap or icon associated with a button.</span></span>

<span data-ttu-id="dc729-126">Una aplicación también puede usar el mensaje [**DM _ \_ GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) para recuperar el identificador del control de botón de opción predeterminado en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="dc729-126">An application can also use the [**DM\_GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) message to retrieve the identifier of the default push button control in a dialog box.</span></span> <span data-ttu-id="dc729-127">Una aplicación puede usar el mensaje [**DM _ \_ SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) para establecer el botón de opción predeterminado para un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="dc729-127">An application can use the [**DM\_SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) message to set the default push button for a dialog box.</span></span>

<span data-ttu-id="dc729-128">Llamar a la función [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) o [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) es equivalente a enviar un mensaje de [**\_ SETCHECK de BM**](bm-setcheck.md) .</span><span class="sxs-lookup"><span data-stu-id="dc729-128">Calling the [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) or [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) function is equivalent to sending a [**BM\_SETCHECK**](bm-setcheck.md) message.</span></span> <span data-ttu-id="dc729-129">Llamar a la función [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) es equivalente a enviar un mensaje de [**BM \_ GETCHECK**](bm-getcheck.md) .</span><span class="sxs-lookup"><span data-stu-id="dc729-129">Calling the [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) function is equivalent to sending a [**BM\_GETCHECK**](bm-getcheck.md) message.</span></span>

## <a name="handling-messages-from-a-button"></a><span data-ttu-id="dc729-130">Control de mensajes desde un botón</span><span class="sxs-lookup"><span data-stu-id="dc729-130">Handling Messages from a Button</span></span>

<span data-ttu-id="dc729-131">Las notificaciones de un botón se envían como [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) o como mensajes de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="dc729-131">Notifications from a button are sent as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="dc729-132">Puede encontrar información sobre qué mensaje se usa en la página de referencia de cada notificación.</span><span class="sxs-lookup"><span data-stu-id="dc729-132">Information about which message is used can be found on the reference page for each notification.</span></span>

<span data-ttu-id="dc729-133">Para obtener más información sobre cómo controlar los mensajes, vea [control de mensajes](control-messages.md).</span><span class="sxs-lookup"><span data-stu-id="dc729-133">For more information on how to handle messages, see [Control Messages](control-messages.md).</span></span> <span data-ttu-id="dc729-134">Vea también mensajes de botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-134">See also Button Messages.</span></span>

## <a name="notification-messages-from-buttons"></a><span data-ttu-id="dc729-135">Mensajes de notificación de los botones</span><span class="sxs-lookup"><span data-stu-id="dc729-135">Notification Messages from Buttons</span></span>

<span data-ttu-id="dc729-136">Cuando el usuario hace clic en un botón, su estado cambia y el botón envía códigos de notificación, en forma de mensajes de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) , a su ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="dc729-136">When the user clicks a button, its state changes, and the button sends notification codes, in the form of [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages, to its parent window.</span></span> <span data-ttu-id="dc729-137">Por ejemplo, un control de botón de opción envía el código de notificación en el que se [ \_ hace clic en el BN](bn-clicked.md) cada vez que el usuario elige el botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-137">For example, a push button control sends the [BN\_CLICKED](bn-clicked.md) notification code whenever the user chooses the button.</span></span> <span data-ttu-id="dc729-138">En todos los casos (excepto [para BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)), la palabra de orden inferior del parámetro *wParam* contiene el identificador de control, la palabra de orden superior de *wParam* contiene el código de notificación y el parámetro *lParam* contiene el identificador de la ventana de control.</span><span class="sxs-lookup"><span data-stu-id="dc729-138">In all cases (except for [BCN\_HOTITEMCHANGE](bcn-hotitemchange.md)), the low-order word of the *wParam* parameter contains the control identifier, the high-order word of *wParam* contains the notification code, and the *lParam* parameter contains the control window handle.</span></span>

<span data-ttu-id="dc729-139">Tanto el mensaje como la respuesta de la ventana primaria dependen del tipo, el estilo y el estado actual del botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-139">Both the message and the parent window's response depend on the type, style, and current state of the button.</span></span> <span data-ttu-id="dc729-140">A continuación se muestran los códigos de notificación de botón que una aplicación debe supervisar y procesar.</span><span class="sxs-lookup"><span data-stu-id="dc729-140">Following are the button notification codes an application should monitor and process.</span></span>



| <span data-ttu-id="dc729-141">Código de notificación</span><span class="sxs-lookup"><span data-stu-id="dc729-141">Notification code</span></span>                                                        | <span data-ttu-id="dc729-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc729-142">Description</span></span>                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="dc729-143">BCN \_ HOTITEMCHANGE</span><span class="sxs-lookup"><span data-stu-id="dc729-143">BCN\_HOTITEMCHANGE</span></span>](bcn-hotitemchange.md)                              | <span data-ttu-id="dc729-144">El mouse entró o quedó en el área cliente de un botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-144">The mouse entered or left the client area of a button.</span></span> |
| [<span data-ttu-id="dc729-145">BN \_ clic</span><span class="sxs-lookup"><span data-stu-id="dc729-145">BN\_CLICKED</span></span>](bn-clicked.md)                                            | <span data-ttu-id="dc729-146">El usuario hizo clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-146">The user clicked a button.</span></span>                             |
| <span data-ttu-id="dc729-147">[BN \_ DBLCLK](bn-dblclk.md) o [BN \_ ](bn-doubleclicked.md)</span><span class="sxs-lookup"><span data-stu-id="dc729-147">[BN\_DBLCLK](bn-dblclk.md) or [BN\_DOUBLECLICKED](bn-doubleclicked.md)</span></span> | <span data-ttu-id="dc729-148">El usuario hizo doble clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-148">The user double-clicked a button.</span></span>                      |
| [<span data-ttu-id="dc729-149">Deshabilitación de BN \_</span><span class="sxs-lookup"><span data-stu-id="dc729-149">BN\_DISABLE</span></span>](bn-disable.md)                                            | <span data-ttu-id="dc729-150">Un botón está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="dc729-150">A button is disabled.</span></span>                                  |
| <span data-ttu-id="dc729-151">[BN \_ Push](bn-pushed.md) o [BN \_ HILITE](bn-hilite.md)</span><span class="sxs-lookup"><span data-stu-id="dc729-151">[BN\_PUSHED](bn-pushed.md) or [BN\_HILITE](bn-hilite.md)</span></span>               | <span data-ttu-id="dc729-152">El usuario insertó un botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-152">The user pushed a button.</span></span>                              |
| [<span data-ttu-id="dc729-153">BN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="dc729-153">BN\_KILLFOCUS</span></span>](bn-killfocus.md)                                        | <span data-ttu-id="dc729-154">El botón perdió el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="dc729-154">The button lost the keyboard focus.</span></span>                    |
| [<span data-ttu-id="dc729-155">BN \_ Paint</span><span class="sxs-lookup"><span data-stu-id="dc729-155">BN\_PAINT</span></span>](bn-paint.md)                                                | <span data-ttu-id="dc729-156">Se debe pintar el botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-156">The button should be painted.</span></span>                          |
| [<span data-ttu-id="dc729-157">BN ( \_ SETFOCUS)</span><span class="sxs-lookup"><span data-stu-id="dc729-157">BN\_SETFOCUS</span></span>](bn-setfocus.md)                                          | <span data-ttu-id="dc729-158">El botón obtuvo el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="dc729-158">The button gained the keyboard focus.</span></span>                  |
| <span data-ttu-id="dc729-159">[BN \_ Uninserted](bn-unpushed.md) o [BN \_ UNHILITE](bn-unhilite.md)</span><span class="sxs-lookup"><span data-stu-id="dc729-159">[BN\_UNPUSHED](bn-unpushed.md) or [BN\_UNHILITE](bn-unhilite.md)</span></span>       | <span data-ttu-id="dc729-160">El botón ya no se inserta.</span><span class="sxs-lookup"><span data-stu-id="dc729-160">The button is no longer pushed.</span></span>                        |



 

<span data-ttu-id="dc729-161">Un botón envía los códigos de notificación [BN \_ Disable](bn-disable.md), [BN \_ Push](bn-pushed.md), [BN \_ KILLFOCUS](bn-killfocus.md), [BN \_ Paint](bn-paint.md), [BN \_ SETFOCUS](bn-setfocus.md)y [BN \_ unpushd](bn-unpushed.md) solo si tiene el estilo [**BS \_ Notify**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="dc729-161">A button sends the [BN\_DISABLE](bn-disable.md), [BN\_PUSHED](bn-pushed.md), [BN\_KILLFOCUS](bn-killfocus.md), [BN\_PAINT](bn-paint.md), [BN\_SETFOCUS](bn-setfocus.md), and [BN\_UNPUSHED](bn-unpushed.md) notification codes only if it has the [**BS\_NOTIFY**](button-styles.md) style.</span></span> <span data-ttu-id="dc729-162">[BN \_](bn-dblclk.md) Los códigos de notificación de DBLCLK se envían de forma automática para los botones [**BS \_ USERBUTTON**](button-styles.md) [**, \_ y**](button-styles.md) [**BS \_ OWNERDRAW**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="dc729-162">[BN\_DBLCLK](bn-dblclk.md) notification codes are sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="dc729-163">Otros tipos de botón envían BN \_ DBLCLK solo si tienen el estilo de **\_ notificación de BS** .</span><span class="sxs-lookup"><span data-stu-id="dc729-163">Other button types send BN\_DBLCLK only if they have the **BS\_NOTIFY** style.</span></span> <span data-ttu-id="dc729-164">Todos los botones envían el código de notificación en el que se [ \_ hace clic](bn-clicked.md) con el BN, independientemente de sus estilos de botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-164">All buttons send the [BN\_CLICKED](bn-clicked.md) notification code regardless of their button styles.</span></span>

<span data-ttu-id="dc729-165">En el caso de los botones automáticos, el sistema cambia el estado de la extracción y pinta el botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-165">For automatic buttons, the system changes the push state and paints the button.</span></span> <span data-ttu-id="dc729-166">En este caso, la aplicación normalmente solo procesa los códigos de notificación [BN \_ clic](bn-clicked.md) y [BN \_ DBLCLK](bn-dblclk.md) .</span><span class="sxs-lookup"><span data-stu-id="dc729-166">In this case, the application typically processes only the [BN\_CLICKED](bn-clicked.md) and [BN\_DBLCLK](bn-dblclk.md) notification codes.</span></span> <span data-ttu-id="dc729-167">En el caso de los botones que no son automáticos, la aplicación normalmente responde al código de notificación mediante el envío de un mensaje para cambiar el estado del botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-167">For buttons that are not automatic, the application typically responds to the notification code by sending a message to change the state of the button.</span></span> <span data-ttu-id="dc729-168">Para obtener información sobre el envío de mensajes a botones, consulte [envío de mensajes a botones](#sending-messages-to-buttons).</span><span class="sxs-lookup"><span data-stu-id="dc729-168">For information about sending messages to buttons, see [Sending Messages to Buttons](#sending-messages-to-buttons).</span></span>

<span data-ttu-id="dc729-169">Cuando el usuario selecciona un botón dibujado por el propietario, el botón envía a su ventana primaria un mensaje de [**WM \_ DRAWITEM**](wm-drawitem.md) que contiene el identificador del control que se va a dibujar e información sobre sus dimensiones y estado.</span><span class="sxs-lookup"><span data-stu-id="dc729-169">When the user selects an owner-drawn button, the button sends its parent window a [**WM\_DRAWITEM**](wm-drawitem.md) message containing the identifier of the control to be drawn and information about its dimensions and state.</span></span>

## <a name="button-color-messages"></a><span data-ttu-id="dc729-170">Mensajes de color de botón</span><span class="sxs-lookup"><span data-stu-id="dc729-170">Button Color Messages</span></span>

<span data-ttu-id="dc729-171">El sistema proporciona los valores de color predeterminados para los botones.</span><span class="sxs-lookup"><span data-stu-id="dc729-171">The system provides default color values for buttons.</span></span> <span data-ttu-id="dc729-172">Una aplicación puede recuperar los valores predeterminados de estos colores mediante una llamada a la función [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) o establecer los valores mediante una llamada a la función [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) .</span><span class="sxs-lookup"><span data-stu-id="dc729-172">An application can retrieve the default values for these colors by calling the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) function, or set the values by calling the [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) function.</span></span> <span data-ttu-id="dc729-173">En la tabla siguiente se muestran los valores predeterminados de color de botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-173">The following table shows the default button-color values.</span></span>



| <span data-ttu-id="dc729-174">Value</span><span class="sxs-lookup"><span data-stu-id="dc729-174">Value</span></span>               | <span data-ttu-id="dc729-175">Elemento coloreado</span><span class="sxs-lookup"><span data-stu-id="dc729-175">Element colored</span></span>                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc729-176">COLOR \_ BTNFACE</span><span class="sxs-lookup"><span data-stu-id="dc729-176">COLOR\_BTNFACE</span></span>      | <span data-ttu-id="dc729-177">Caras del botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-177">Button faces.</span></span>                                                                                                              |
| <span data-ttu-id="dc729-178">COLOR \_ BTNHIGHLIGHT</span><span class="sxs-lookup"><span data-stu-id="dc729-178">COLOR\_BTNHIGHLIGHT</span></span> | <span data-ttu-id="dc729-179">Área de resaltado (los bordes superior e izquierdo) de un botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-179">Highlight area (the top and left edges) of a button.</span></span>                                                                       |
| <span data-ttu-id="dc729-180">COLOR \_ BTNSHADOW</span><span class="sxs-lookup"><span data-stu-id="dc729-180">COLOR\_BTNSHADOW</span></span>    | <span data-ttu-id="dc729-181">Área de sombra (bordes inferior y derecho) de un botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-181">Shadow area (the bottom and right edges) of a button.</span></span>                                                                      |
| <span data-ttu-id="dc729-182">COLOR \_ BTNTEXT</span><span class="sxs-lookup"><span data-stu-id="dc729-182">COLOR\_BTNTEXT</span></span>      | <span data-ttu-id="dc729-183">Texto normal (no gris) en botones.</span><span class="sxs-lookup"><span data-stu-id="dc729-183">Regular (nongrayed) text in buttons.</span></span>                                                                                       |
| <span data-ttu-id="dc729-184">COLOR \_ GRAYTEXT</span><span class="sxs-lookup"><span data-stu-id="dc729-184">COLOR\_GRAYTEXT</span></span>     | <span data-ttu-id="dc729-185">Texto deshabilitado (gris) en botones.</span><span class="sxs-lookup"><span data-stu-id="dc729-185">Disabled (gray) text in buttons.</span></span> <span data-ttu-id="dc729-186">Este color se establece en 0 si el controlador de pantalla actual no admite un color gris sólido.</span><span class="sxs-lookup"><span data-stu-id="dc729-186">This color is set to 0 if the current display driver does not support a solid gray color.</span></span> |
| <span data-ttu-id="dc729-187">ventana de COLOR \_</span><span class="sxs-lookup"><span data-stu-id="dc729-187">COLOR\_WINDOW</span></span>       | <span data-ttu-id="dc729-188">Fondo de las ventanas.</span><span class="sxs-lookup"><span data-stu-id="dc729-188">Window backgrounds.</span></span>                                                                                                        |
| <span data-ttu-id="dc729-189">COLOR \_ WINDOWFRAME</span><span class="sxs-lookup"><span data-stu-id="dc729-189">COLOR\_WINDOWFRAME</span></span>  | <span data-ttu-id="dc729-190">Marcos de ventana.</span><span class="sxs-lookup"><span data-stu-id="dc729-190">Window frames.</span></span>                                                                                                             |
| <span data-ttu-id="dc729-191">COLOR \_ WINDOWTEXT</span><span class="sxs-lookup"><span data-stu-id="dc729-191">COLOR\_WINDOWTEXT</span></span>   | <span data-ttu-id="dc729-192">Texto en Windows.</span><span class="sxs-lookup"><span data-stu-id="dc729-192">Text in windows.</span></span>                                                                                                           |



 

<span data-ttu-id="dc729-193">Sin embargo, la llamada a [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) afecta a todas las aplicaciones, por lo que no debe llamar a esta función para personalizar los botones de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dc729-193">However, calling [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) affects all applications, so you should not call this function to customize buttons for your application.</span></span>

<span data-ttu-id="dc729-194">El sistema envía un mensaje de [**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md) a la ventana primaria de un botón antes de dibujar un botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-194">The system sends a [**WM\_CTLCOLORBTN**](wm-ctlcolorbtn.md) message to a button's parent window before drawing a button.</span></span> <span data-ttu-id="dc729-195">Este mensaje contiene un identificador para el contexto de dispositivo del botón y un identificador de la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="dc729-195">This message contains a handle to the button's device context and a handle to the child window.</span></span> <span data-ttu-id="dc729-196">La ventana primaria puede usar estos manipuladores para cambiar el texto del botón y los colores de fondo.</span><span class="sxs-lookup"><span data-stu-id="dc729-196">The parent window can use these handles to change the button's text and background colors.</span></span> <span data-ttu-id="dc729-197">Sin embargo, solo los botones dibujados por el propietario responden a la ventana primaria que procesa el mensaje.</span><span class="sxs-lookup"><span data-stu-id="dc729-197">However, only owner-drawn buttons respond to the parent window processing the message.</span></span>

## <a name="button-default-message-processing"></a><span data-ttu-id="dc729-198">Procesamiento de mensajes predeterminado del botón</span><span class="sxs-lookup"><span data-stu-id="dc729-198">Button Default Message Processing</span></span>

<span data-ttu-id="dc729-199">El procedimiento de ventana de la clase de ventana de control de botón predefinido lleva a cabo el procesamiento predeterminado para todos los mensajes que no procesa el procedimiento de control de botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-199">The window procedure for the predefined button control window class carries out default processing for all messages that the button control procedure does not process.</span></span> <span data-ttu-id="dc729-200">Cuando el procedimiento de control de botón devuelve **false** para cualquier mensaje, el procedimiento de ventana predefinido comprueba los mensajes y realiza las acciones predeterminadas que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="dc729-200">When the button control procedure returns **FALSE** for any message, the predefined window procedure checks the messages and performs the default actions listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc729-201">Message</span><span class="sxs-lookup"><span data-stu-id="dc729-201">Message</span></span></th>
<th><span data-ttu-id="dc729-202">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="dc729-202">Default action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc729-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span></span></td>
<td><span data-ttu-id="dc729-204">Envía el botón un <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> y un mensaje de <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> y envía a la ventana primaria un código de notificación de <a href="bn-clicked.md">BN_CLICKED</a> .</span><span class="sxs-lookup"><span data-stu-id="dc729-204">Sends the button a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> and a <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> message, and sends the parent window a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="dc729-206">Devuelve el estado de activación del botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-206">Returns the check state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="dc729-208">Devuelve un identificador para el mapa de bits o el icono asociado al botón o <strong>null</strong> si el botón no tiene ningún mapa de bits o icono.</span><span class="sxs-lookup"><span data-stu-id="dc729-208">Returns a handle to the bitmap or icon associated with the button or <strong>NULL</strong> if the button has no bitmap or icon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="dc729-210">Devuelve el estado de activación actual, el estado de inserción y el estado de foco del botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-210">Returns the current check state, push state, and focus state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="dc729-212">Establece el estado de activación para todos los estilos de botones de radio y casillas.</span><span class="sxs-lookup"><span data-stu-id="dc729-212">Sets the check state for all styles of radio buttons and check boxes.</span></span> <span data-ttu-id="dc729-213">Si el parámetro <em>wParam</em> es mayor que cero para los botones de radio, al botón se le asigna el estilo <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="dc729-213">If the <em>wParam</em> parameter is greater than zero for radio buttons, the button is given the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> style.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="dc729-215">Asocia el identificador de mapa de bits o icono especificado con el botón y devuelve un identificador al mapa de bits o icono anterior.</span><span class="sxs-lookup"><span data-stu-id="dc729-215">Associates the specified bitmap or icon handle with the button and returns a handle to the previous bitmap or icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="dc729-217">Establece el estado de la inserciones del botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-217">Sets the push state of the button.</span></span> <span data-ttu-id="dc729-218">En el caso de los botones dibujados por el propietario, se envía un mensaje <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> a la ventana primaria si ha cambiado el estado del botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-218">For owner-drawn buttons, a <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> message is sent to the parent window if the state of the button has changed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span></span></td>
<td><span data-ttu-id="dc729-220">Establece el estilo del botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-220">Sets the button style.</span></span> <span data-ttu-id="dc729-221">Si la palabra de orden inferior del parámetro <em>lParam</em> es <strong>true</strong>, el botón vuelve a dibujarse.</span><span class="sxs-lookup"><span data-stu-id="dc729-221">If the low-order word of the <em>lParam</em> parameter is <strong>TRUE</strong>, the button is redrawn.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span></span></td>
<td><span data-ttu-id="dc729-223">Activa una casilla o una casilla automática cuando el usuario presiona las teclas más (+) o igual (=).</span><span class="sxs-lookup"><span data-stu-id="dc729-223">Checks a check box or automatic check box when the user presses the plus (+) or equal (=) keys.</span></span> <span data-ttu-id="dc729-224">Desactiva una casilla de verificación o automática cuando el usuario presiona la tecla menos (–).</span><span class="sxs-lookup"><span data-stu-id="dc729-224">Clears a check box or automatic check box when the user presses the minus (–) key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span></span></td>
<td><span data-ttu-id="dc729-226">Pinta el botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-226">Paints the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span></span></td>
<td><span data-ttu-id="dc729-228">Borra el fondo de los botones dibujados por el propietario.</span><span class="sxs-lookup"><span data-stu-id="dc729-228">Erases the background for owner-drawn buttons.</span></span> <span data-ttu-id="dc729-229">Los fondos de otros botones se borran como parte de la <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> y <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="dc729-229">The backgrounds of other buttons are erased as part of the <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> and <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span></span></td>
<td><span data-ttu-id="dc729-231">Devuelve valores que indican el tipo de entrada que procesa el procedimiento de botón predeterminado, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="dc729-231">Returns values that indicate the type of input processed by the default button procedure, as shown in the following table.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc729-232">Estilo de botón</span><span class="sxs-lookup"><span data-stu-id="dc729-232">Button style</span></span></th>
<th><span data-ttu-id="dc729-233">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="dc729-233">Returns</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc729-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="dc729-235">DLGC_WANTCHARS | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="dc729-235">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="dc729-237">DLGC_RADIOBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="dc729-237">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="dc729-239">DLGC_WANTCHARS | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="dc729-239">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="dc729-241">DLGC_DEFPUSHBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="dc729-241">DLGC_DEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span></span></td>
<td><span data-ttu-id="dc729-243">DLGC_STATIC</span><span class="sxs-lookup"><span data-stu-id="dc729-243">DLGC_STATIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="dc729-245">DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="dc729-245">DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="dc729-247">DLGC_RADIOBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="dc729-247">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span></span></td>
<td><span data-ttu-id="dc729-249">Devuelve un identificador de la fuente actual.</span><span class="sxs-lookup"><span data-stu-id="dc729-249">Returns a handle to the current font.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span></span></td>
<td><span data-ttu-id="dc729-251">Empuja el botón si el usuario presiona la barra ESPACIAdora.</span><span class="sxs-lookup"><span data-stu-id="dc729-251">Pushes the button if the user presses the SPACEBAR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span></span></td>
<td><span data-ttu-id="dc729-253">Libera la captura del mouse para todos los casos excepto la tecla TAB.</span><span class="sxs-lookup"><span data-stu-id="dc729-253">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="dc729-255">Quita el rectángulo de foco de un botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-255">Removes the focus rectangle from a button.</span></span> <span data-ttu-id="dc729-256">En el caso de los botones de opción y los botones de preinstalación predeterminados, se invalida el rectángulo de foco.</span><span class="sxs-lookup"><span data-stu-id="dc729-256">For push buttons and default push buttons, the focus rectangle is invalidated.</span></span> <span data-ttu-id="dc729-257">Si el botón tiene la captura del mouse, se libera la captura, no se hace clic en el botón y se quita cualquier estado de la extracción.</span><span class="sxs-lookup"><span data-stu-id="dc729-257">If the button has the mouse capture, the capture is released, the button is not clicked, and any push state is removed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span></span></td>
<td><span data-ttu-id="dc729-259">Envía un código de notificación de <a href="bn-dblclk.md">BN_DBLCLK</a> a la ventana primaria de los botones de radio y los botones dibujados por el propietario.</span><span class="sxs-lookup"><span data-stu-id="dc729-259">Sends a <a href="bn-dblclk.md">BN_DBLCLK</a> notification code to the parent window for radio buttons and owner-drawn buttons.</span></span> <span data-ttu-id="dc729-260">Para otros botones, un doble clic se procesa como un mensaje de <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="dc729-260">For other buttons, a double-click is processed as a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span></span></td>
<td><span data-ttu-id="dc729-262">Resalta el botón si la posición del cursor del mouse está dentro del rectángulo cliente del botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-262">Highlights the button if the position of the mouse cursor is within the button's client rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span></span></td>
<td><span data-ttu-id="dc729-264">Libera la captura del mouse si el botón tenía la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="dc729-264">Releases the mouse capture if the button had the mouse capture.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span></span></td>
<td><span data-ttu-id="dc729-266">Realiza la misma acción que <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, si el botón tiene la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="dc729-266">Performs the same action as <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, if the button has the mouse capture.</span></span> <span data-ttu-id="dc729-267">De lo contrario, no se realiza ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="dc729-267">Otherwise, no action is performed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span></span></td>
<td><span data-ttu-id="dc729-269">Convierte cualquier botón de <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> en un botón de <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="dc729-269">Turns any <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> button into a <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> button.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span></span></td>
<td><span data-ttu-id="dc729-271">Devuelve HTTRANSPARENT si el control de botón es un cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="dc729-271">Returns HTTRANSPARENT, if the button control is a group box.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span></span></td>
<td><span data-ttu-id="dc729-273">Dibuja el botón según su estilo y su estado actual.</span><span class="sxs-lookup"><span data-stu-id="dc729-273">Draws the button according to its style and current state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="dc729-275">Dibuja un rectángulo de foco en el botón que obtiene el foco.</span><span class="sxs-lookup"><span data-stu-id="dc729-275">Draws a focus rectangle on the button getting the focus.</span></span> <span data-ttu-id="dc729-276">En los botones de radio y los botones de radio automáticos, se envía una <a href="bn-clicked.md">BN_CLICKED</a> código de notificación a la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="dc729-276">For radio buttons and automatic radio buttons, the parent window is sent a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span></span></td>
<td><span data-ttu-id="dc729-278">Establece una nueva fuente y, opcionalmente, actualiza la ventana.</span><span class="sxs-lookup"><span data-stu-id="dc729-278">Sets a new font and optionally updates the window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc729-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span></span></td>
<td><span data-ttu-id="dc729-280">Establece el texto del botón.</span><span class="sxs-lookup"><span data-stu-id="dc729-280">Sets the text of the button.</span></span> <span data-ttu-id="dc729-281">En el caso de un cuadro de grupo, el mensaje pinta sobre el texto preexistente antes de volver a pintar el cuadro de grupo con el nuevo texto.</span><span class="sxs-lookup"><span data-stu-id="dc729-281">In the case of a group box, the message paints over the preexisting text before repainting the group box with the new text.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc729-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc729-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span></span></td>
<td><span data-ttu-id="dc729-283">Libera la captura del mouse para todos los casos excepto la tecla TAB.</span><span class="sxs-lookup"><span data-stu-id="dc729-283">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="dc729-284">El procedimiento de ventana predefinido pasa todos los demás mensajes a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para el procesamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="dc729-284">The predefined window procedure passes all other messages to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function for default processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc729-285">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dc729-285">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc729-286">Mensajes de control</span><span class="sxs-lookup"><span data-stu-id="dc729-286">Control Messages</span></span>](control-messages.md)
</dt> </dl>

 

 