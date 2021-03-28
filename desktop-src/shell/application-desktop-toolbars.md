---
description: Una barra de herramientas del escritorio de la aplicación (también denominada Appbar) es una ventana similar a la barra de tareas de Windows.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Usar las barras de herramientas del escritorio de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140ef94c1daeb571cd0d766dfbd4dc28b7991efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153922"
---
# <a name="using-application-desktop-toolbars"></a><span data-ttu-id="6ffff-103">Usar las barras de herramientas del escritorio de la aplicación</span><span class="sxs-lookup"><span data-stu-id="6ffff-103">Using Application Desktop Toolbars</span></span>

<span data-ttu-id="6ffff-104">Una *barra de herramientas del escritorio* de la aplicación (también denominada Appbar) es una ventana similar a la barra de tareas de Windows.</span><span class="sxs-lookup"><span data-stu-id="6ffff-104">An *application desktop toolbar* (also called an appbar) is a window that is similar to the Windows taskbar.</span></span> <span data-ttu-id="6ffff-105">Está anclado a un borde de la pantalla y normalmente contiene botones que proporcionan al usuario acceso rápido a otras aplicaciones y ventanas.</span><span class="sxs-lookup"><span data-stu-id="6ffff-105">It is anchored to an edge of the screen, and it typically contains buttons that give the user quick access to other applications and windows.</span></span> <span data-ttu-id="6ffff-106">El sistema impide que otras aplicaciones utilicen el área de escritorio utilizada por un Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-106">The system prevents other applications from using the desktop area used by an appbar.</span></span> <span data-ttu-id="6ffff-107">Puede haber cualquier número de appbars en el escritorio en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="6ffff-107">Any number of appbars can exist on the desktop at any given time.</span></span>

<span data-ttu-id="6ffff-108">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="6ffff-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6ffff-109">Acerca de las barras de herramientas del escritorio de la aplicación</span><span class="sxs-lookup"><span data-stu-id="6ffff-109">About Application Desktop Toolbars</span></span>](#about-application-desktop-toolbars)
    -   [<span data-ttu-id="6ffff-110">Envío de mensajes</span><span class="sxs-lookup"><span data-stu-id="6ffff-110">Sending Messages</span></span>](#sending-messages)
    -   [<span data-ttu-id="6ffff-111">Registro</span><span class="sxs-lookup"><span data-stu-id="6ffff-111">Registration</span></span>](#registration)
    -   [<span data-ttu-id="6ffff-112">Tamaño y posición de Appbar</span><span class="sxs-lookup"><span data-stu-id="6ffff-112">Appbar Size and Position</span></span>](#appbar-size-and-position)
    -   [<span data-ttu-id="6ffff-113">Ocultar automáticamente las barras de herramientas del escritorio de la aplicación</span><span class="sxs-lookup"><span data-stu-id="6ffff-113">Autohide Application Desktop Toolbars</span></span>](#autohide-application-desktop-toolbars)
    -   [<span data-ttu-id="6ffff-114">Mensajes de notificación de Appbar</span><span class="sxs-lookup"><span data-stu-id="6ffff-114">Appbar Notification Messages</span></span>](#appbar-notification-messages)
-   [<span data-ttu-id="6ffff-115">Registro de una barra de herramientas del escritorio de la aplicación</span><span class="sxs-lookup"><span data-stu-id="6ffff-115">Registering an Application Desktop Toolbar</span></span>](#registering-an-application-desktop-toolbar)
-   [<span data-ttu-id="6ffff-116">Establecer el tamaño y la posición de Appbar</span><span class="sxs-lookup"><span data-stu-id="6ffff-116">Setting the Appbar Size and Position</span></span>](#setting-the-appbar-size-and-position)
-   [<span data-ttu-id="6ffff-117">Procesamiento de mensajes de notificación de Appbar</span><span class="sxs-lookup"><span data-stu-id="6ffff-117">Processing Appbar Notification Messages</span></span>](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a><span data-ttu-id="6ffff-118">Acerca de las barras de herramientas del escritorio de la aplicación</span><span class="sxs-lookup"><span data-stu-id="6ffff-118">About Application Desktop Toolbars</span></span>

<span data-ttu-id="6ffff-119">Windows proporciona una API que le permite aprovechar los servicios de Appbar proporcionados por el sistema.</span><span class="sxs-lookup"><span data-stu-id="6ffff-119">Windows provides an API that lets you take advantage of appbar services provided by the system.</span></span> <span data-ttu-id="6ffff-120">Los servicios ayudan a garantizar que los appbars definidos por la aplicación funcionan sin problemas entre sí y con la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="6ffff-120">The services help ensure that application-defined appbars operate smoothly with one another and with the taskbar.</span></span> <span data-ttu-id="6ffff-121">El sistema mantiene información sobre cada Appbar y envía los mensajes appbars para notificarles los eventos que pueden afectar a su tamaño, posición y apariencia.</span><span class="sxs-lookup"><span data-stu-id="6ffff-121">The system maintains information about each appbar and sends the appbars messages to notify them about events that can affect their size, position, and appearance.</span></span>

### <a name="sending-messages"></a><span data-ttu-id="6ffff-122">enviar mensajes</span><span class="sxs-lookup"><span data-stu-id="6ffff-122">Sending Messages</span></span>

<span data-ttu-id="6ffff-123">Una aplicación utiliza un conjunto especial de mensajes, denominados mensajes de Appbar, para agregar o quitar un Appbar, establecer el tamaño y la posición de una Appbar y recuperar información sobre el tamaño, la posición y el estado de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="6ffff-123">An application uses a special set of messages, called appbar messages, to add or remove an appbar, set an appbar's size and position, and retrieve information about the size, position, and state of the taskbar.</span></span> <span data-ttu-id="6ffff-124">Para enviar un mensaje de Appbar, una aplicación debe usar la función [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-124">To send an appbar message, an application must use the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function.</span></span> <span data-ttu-id="6ffff-125">Los parámetros de la función incluyen un identificador de mensaje, como [**ABN \_ New**](abm-new.md), y la dirección de una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-125">The function's parameters include a message identifier, such as [**ABM\_NEW**](abm-new.md), and the address of an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="6ffff-126">Los miembros de la estructura contienen información que el sistema necesita para procesar el mensaje dado.</span><span class="sxs-lookup"><span data-stu-id="6ffff-126">The structure members contain information that the system needs to process the given message.</span></span>

<span data-ttu-id="6ffff-127">Para un mensaje de Appbar determinado, el sistema usa algunos miembros de la estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) y omite los demás.</span><span class="sxs-lookup"><span data-stu-id="6ffff-127">For any given appbar message, the system uses some members of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure and ignores the others.</span></span> <span data-ttu-id="6ffff-128">Sin embargo, el sistema siempre usa los miembros **cbSize** y **hWnd** , por lo que una aplicación debe rellenar estos miembros para cada mensaje de Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-128">However, the system always uses the **cbSize** and **hWnd** members, so an application must fill these members for every appbar message.</span></span> <span data-ttu-id="6ffff-129">El miembro **cbSize** especifica el tamaño de la estructura y el miembro **hWnd** es el identificador de la ventana de Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-129">The **cbSize** member specifies the size of the structure, and the **hWnd** member is the handle to the appbar's window.</span></span>

<span data-ttu-id="6ffff-130">Algunos mensajes de Appbar solicitan información del sistema.</span><span class="sxs-lookup"><span data-stu-id="6ffff-130">Some appbar messages request information from the system.</span></span> <span data-ttu-id="6ffff-131">Al procesar estos mensajes, el sistema copia la información solicitada en la estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-131">When processing these messages, the system copies the requested information into the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

### <a name="registration"></a><span data-ttu-id="6ffff-132">Registro</span><span class="sxs-lookup"><span data-stu-id="6ffff-132">Registration</span></span>

<span data-ttu-id="6ffff-133">El sistema mantiene una lista interna de appbars y mantiene información sobre cada barra de la lista.</span><span class="sxs-lookup"><span data-stu-id="6ffff-133">The system keeps an internal list of appbars and maintains information about each bar in the list.</span></span> <span data-ttu-id="6ffff-134">El sistema utiliza la información para administrar appbars, realizar servicios para ellos y enviarles mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="6ffff-134">The system uses the information to manage appbars, perform services for them, and send them notification messages.</span></span>

<span data-ttu-id="6ffff-135">Una aplicación debe registrar un Appbar (es decir, agregarlo a la lista interna) para poder recibir los servicios de Appbar del sistema.</span><span class="sxs-lookup"><span data-stu-id="6ffff-135">An application must register an appbar (that is, add it to the internal list) before it can receive appbar services from the system.</span></span> <span data-ttu-id="6ffff-136">Para registrar un Appbar, una aplicación envía el [**\_ nuevo mensaje ABN**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-136">To register an appbar, an application sends the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="6ffff-137">La estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) adjunta incluye el identificador de la ventana de Appbar y un identificador de mensaje definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6ffff-137">The accompanying [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure includes the handle to the appbar's window and an application-defined message identifier.</span></span> <span data-ttu-id="6ffff-138">El sistema utiliza el identificador de mensaje para enviar mensajes de notificación al procedimiento de ventana de la ventana de Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-138">The system uses the message identifier to send notification messages to the window procedure of the appbar window.</span></span> <span data-ttu-id="6ffff-139">Para obtener más información, consulte mensajes de notificación de Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-139">For more information, see Appbar Notification Messages.</span></span>

<span data-ttu-id="6ffff-140">Una aplicación anula el registro de una Appbar mediante el envío del mensaje [**ABN \_ Remove**](abm-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-140">An application unregisters an appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="6ffff-141">Al anular el registro de un control Appbar, se quita de la lista interna de appbars del sistema.</span><span class="sxs-lookup"><span data-stu-id="6ffff-141">Unregistering an appbar removes it from the system's internal list of appbars.</span></span> <span data-ttu-id="6ffff-142">El sistema ya no envía mensajes de notificación al Appbar o impide que otras aplicaciones utilicen el área de pantalla utilizada por el Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-142">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span> <span data-ttu-id="6ffff-143">Una aplicación siempre debe enviar **ABN \_ Remove** antes de destruir un Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-143">An application should always send **ABM\_REMOVE** before destroying an appbar.</span></span>

### <a name="appbar-size-and-position"></a><span data-ttu-id="6ffff-144">Tamaño y posición de Appbar</span><span class="sxs-lookup"><span data-stu-id="6ffff-144">Appbar Size and Position</span></span>

<span data-ttu-id="6ffff-145">Una aplicación debe establecer el tamaño y la posición de una Appbar para que no interfiera con ningún otro appbars o la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="6ffff-145">An application should set an appbar's size and position so that it does not interfere with any other appbars or the taskbar.</span></span> <span data-ttu-id="6ffff-146">Cada Appbar debe estar anclado a un borde determinado de la pantalla y varios appbars se pueden anclar a un borde.</span><span class="sxs-lookup"><span data-stu-id="6ffff-146">Every appbar must be anchored to a particular edge of the screen, and multiple appbars can be anchored to an edge.</span></span> <span data-ttu-id="6ffff-147">Sin embargo, si un Appbar está anclado al mismo borde que la barra de tareas, el sistema garantiza que la barra de tareas esté siempre en el borde más externo.</span><span class="sxs-lookup"><span data-stu-id="6ffff-147">However, if an appbar is anchored to the same edge as the taskbar, the system ensures that the taskbar is always on the outermost edge.</span></span>

<span data-ttu-id="6ffff-148">Para establecer el tamaño y la posición de un Appbar, una aplicación propone primero un borde de pantalla y un rectángulo delimitador para el Appbar mediante el envío del mensaje [**\_ QUERYPOS de ABN**](abm-querypos.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-148">To set the size and position of an appbar, an application first proposes a screen edge and bounding rectangle for the appbar by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="6ffff-149">El sistema determina si la barra de tareas u otro Appbar usa cualquier parte del área de la pantalla del rectángulo propuesto, ajusta el rectángulo (si es necesario) y devuelve el rectángulo ajustado a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6ffff-149">The system determines whether any part of the screen area within the proposed rectangle is used by the taskbar or another appbar, adjusts the rectangle (if necessary), and returns the adjusted rectangle to the application.</span></span>

<span data-ttu-id="6ffff-150">A continuación, la aplicación envía el mensaje [**\_ SETPOS de ABN**](abm-setpos.md) para establecer el nuevo rectángulo delimitador para el Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-150">Next, the application sends the [**ABM\_SETPOS**](abm-setpos.md) message to set the new bounding rectangle for the appbar.</span></span> <span data-ttu-id="6ffff-151">De nuevo, el sistema puede ajustar el rectángulo antes de devolverlo a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6ffff-151">Again, the system may adjust the rectangle before returning it to the application.</span></span> <span data-ttu-id="6ffff-152">Por esta razón, la aplicación debe usar el rectángulo ajustado que devuelve **ABN \_ SETPOS** para establecer el tamaño y la posición finales.</span><span class="sxs-lookup"><span data-stu-id="6ffff-152">For this reason, the application should use the adjusted rectangle returned by **ABM\_SETPOS** to set the final size and position.</span></span> <span data-ttu-id="6ffff-153">La aplicación puede usar la función [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para mover el control Appbar a la posición.</span><span class="sxs-lookup"><span data-stu-id="6ffff-153">The application can use the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="6ffff-154">Mediante el uso de un proceso de dos pasos para establecer el tamaño y la posición, el sistema permite que la aplicación proporcione comentarios intermedios al usuario durante la operación de movimiento.</span><span class="sxs-lookup"><span data-stu-id="6ffff-154">By using a two-step process to set the size and position, the system enables the application to provide intermediate feedback to the user during the move operation.</span></span> <span data-ttu-id="6ffff-155">Por ejemplo, si el usuario arrastra un Appbar, es posible que la aplicación muestre un rectángulo sombreado que indica la nueva posición antes de que se mueva realmente el control Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-155">For example, if the user drags an appbar, the application might display a shaded rectangle indicating the new position before the appbar actually moves.</span></span>

<span data-ttu-id="6ffff-156">Una aplicación debe establecer el tamaño y la posición de su Appbar después de registrarlo y siempre que el Appbar reciba el mensaje de notificación [**ABN \_ POSCHANGED**](abn-poschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-156">An application should set the size and position of its appbar after registering it and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="6ffff-157">Un control Appbar recibe este mensaje de notificación cada vez que se produce un cambio en el tamaño, la posición o el estado de visibilidad de la barra de tareas y siempre que se cambia el tamaño, se agrega o se quita otro Appbar en el mismo lado de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6ffff-157">An appbar receives this notification message whenever a change occurs in the taskbar's size, position, or visibility state and whenever another appbar on the same side of the screen is resized, added, or removed.</span></span>

<span data-ttu-id="6ffff-158">Cada vez que un Appbar recibe el mensaje de activación de WM \_ , debe enviar el mensaje de [**\_ activación de ABN**](abm-activate.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-158">Whenever an appbar receives the WM\_ACTIVATE message, it should send the [**ABM\_ACTIVATE**](abm-activate.md) message.</span></span> <span data-ttu-id="6ffff-159">Del mismo modo, cuando un Appbar recibe un mensaje de WINDOWPOSCHANGED de WM \_ , debe llamar a [**ABN \_ WINDOWPOSCHANGED**](abm-windowposchanged.md).</span><span class="sxs-lookup"><span data-stu-id="6ffff-159">Similarly, when an appbar receives a WM\_WINDOWPOSCHANGED message, it must call [**ABM\_WINDOWPOSCHANGED**](abm-windowposchanged.md).</span></span> <span data-ttu-id="6ffff-160">El envío de estos mensajes garantiza que el sistema establezca correctamente el orden z de cualquier appbars de autoocultar en el mismo borde.</span><span class="sxs-lookup"><span data-stu-id="6ffff-160">Sending these messages ensures that the system properly sets the z-order of any autohide appbars on the same edge.</span></span>

### <a name="autohide-application-desktop-toolbars"></a><span data-ttu-id="6ffff-161">Ocultar automáticamente las barras de herramientas del escritorio de la aplicación</span><span class="sxs-lookup"><span data-stu-id="6ffff-161">Autohide Application Desktop Toolbars</span></span>

<span data-ttu-id="6ffff-162">Un Appbar de ocultación automáticamente es aquél que normalmente está oculto, pero se vuelve visible cuando el usuario mueve el cursor del mouse al borde de la pantalla con el que está asociado el Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-162">An autohide appbar is one that is normally hidden but becomes visible when the user moves the mouse cursor to the screen edge with which the appbar is associated.</span></span> <span data-ttu-id="6ffff-163">El Appbar se oculta de nuevo cuando el usuario mueve el cursor del mouse fuera del rectángulo delimitador de la barra.</span><span class="sxs-lookup"><span data-stu-id="6ffff-163">The appbar hides itself again when the user moves the mouse cursor out of the bar's bounding rectangle.</span></span>

<span data-ttu-id="6ffff-164">Aunque el sistema permite una serie de appbars diferentes en un momento dado, solo permite un Appbar de ocultación automáticamente cada vez para cada margen de la pantalla, en función de la primera vez que se atiende.</span><span class="sxs-lookup"><span data-stu-id="6ffff-164">Although the system allows a number of different appbars at any given time, it allows only one autohide appbar at a time for each screen edge on a first-come, first-served basis.</span></span> <span data-ttu-id="6ffff-165">El sistema mantiene automáticamente el orden z de un Appbar de ocultación automática (solo dentro de su grupo de orden z).</span><span class="sxs-lookup"><span data-stu-id="6ffff-165">The system automatically maintains the z-order of an autohide appbar (within its z-order group only).</span></span>

<span data-ttu-id="6ffff-166">Una aplicación utiliza el [**mensaje \_ SETAUTOHIDEBAR de ABN**](abm-setautohidebar.md) para registrar o anular el registro de un Appbar de ocultación.</span><span class="sxs-lookup"><span data-stu-id="6ffff-166">An application uses the [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) message to register or unregister an autohide appbar.</span></span> <span data-ttu-id="6ffff-167">El mensaje especifica el borde del Appbar y una marca que especifica si se va a registrar o anular el registro de la Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-167">The message specifies the edge for the appbar and a flag that specifies whether the appbar is to be registered or unregistered.</span></span> <span data-ttu-id="6ffff-168">Se produce un error en el mensaje si se está registrando un Appbar de ocultación automáticamente pero uno ya está asociado al borde especificado.</span><span class="sxs-lookup"><span data-stu-id="6ffff-168">The message fails if an autohide appbar is being registered but one is already associated with the specified edge.</span></span> <span data-ttu-id="6ffff-169">Una aplicación puede recuperar el identificador del Appbar de ocultación automáticamente asociado a un borde mediante el envío del mensaje [**\_ GETAUTOHIDEBAR de ABN**](abm-getautohidebar.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-169">An application can retrieve the handle to the autohide appbar associated with an edge by sending the [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) message.</span></span>

<span data-ttu-id="6ffff-170">No es necesario que el Appbar oculto se registre como un Appbar normal; es decir, no es necesario que se registre mediante el envío del [**\_ nuevo mensaje ABN**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-170">An autohide appbar does not need to register as a normal appbar; that is, it does not need to be registered by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="6ffff-171">Un Appbar que no está registrado por **ABN \_ nuevo** superpone cualquier appbars anclado en el mismo borde de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6ffff-171">An appbar that is not registered by **ABM\_NEW** overlaps any appbars anchored on the same edge of the screen.</span></span>

### <a name="appbar-notification-messages"></a><span data-ttu-id="6ffff-172">Mensajes de notificación de Appbar</span><span class="sxs-lookup"><span data-stu-id="6ffff-172">Appbar Notification Messages</span></span>

<span data-ttu-id="6ffff-173">El sistema envía mensajes para notificar a un Appbar sobre eventos que pueden afectar a su posición y apariencia.</span><span class="sxs-lookup"><span data-stu-id="6ffff-173">The system sends messages to notify an appbar about events that can affect its position and appearance.</span></span> <span data-ttu-id="6ffff-174">Los mensajes se envían en el contexto de un mensaje definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6ffff-174">The messages are sent in the context of an application-defined message.</span></span> <span data-ttu-id="6ffff-175">La aplicación especifica el identificador del mensaje cuando envía el [**\_ nuevo mensaje ABN**](abm-new.md) para registrar el Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-175">The application specifies the identifier of the message when it sends the [**ABM\_NEW**](abm-new.md) message to register the appbar.</span></span> <span data-ttu-id="6ffff-176">El código de notificación está en el parámetro *wParam* del mensaje definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6ffff-176">The notification code is in the *wParam* parameter of the application-defined message.</span></span>

<span data-ttu-id="6ffff-177">Un Appbar recibe el mensaje de notificación [**ABN \_ POSCHANGED**](abn-poschanged.md) cuando cambia el tamaño, la posición o el estado de visibilidad de la barra de tareas, cuando se agrega otro Appbar al mismo borde de la pantalla, o cuando se cambia el tamaño o se quita otro Appbar en el mismo borde de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6ffff-177">An appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message when the taskbar's size, position, or visibility state changes, when another appbar is added to the same edge of the screen, or when another appbar on the same edge of the screen is resized or removed.</span></span> <span data-ttu-id="6ffff-178">Un Appbar debe responder a este mensaje de notificación mediante el envío de mensajes [**ABN \_ QUERYPOS**](abm-querypos.md) y [**ABN \_ SETPOS**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-178">An appbar should respond to this notification message by sending [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="6ffff-179">Si ha cambiado la posición de una Appbar, debe llamar a la función [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para moverla a la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="6ffff-179">If an appbar's position has changed, it should call the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

<span data-ttu-id="6ffff-180">El sistema envía el mensaje de notificación [**ABN \_ STATECHANGE**](abn-statechange.md) siempre que haya cambiado el estado de ocultación automática o siempre visible de la barra de tareas, es decir, cuando el usuario activa o desactiva la casilla de verificación Mostrar **siempre visible** o **Ocultar automáticamente** en la hoja de propiedades de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="6ffff-180">The system sends the [**ABN\_STATECHANGE**](abn-statechange.md) notification message whenever the taskbar's autohide or always-on-top state has changed—that is, when the user selects or clears the **Always on top** or **Auto hide** check box on the taskbar's property sheet.</span></span> <span data-ttu-id="6ffff-181">Un Appbar puede usar este mensaje de notificación para establecer su estado de conformidad con el de la barra de tareas, si lo desea.</span><span class="sxs-lookup"><span data-stu-id="6ffff-181">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

<span data-ttu-id="6ffff-182">Cuando se inicia una aplicación de pantalla completa o cuando se cierra la última aplicación de pantalla completa, un Appbar recibe el mensaje de notificación [**ABN \_ FULLSCREENAPP**](abn-fullscreenapp.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-182">When a full-screen application is started or when the last full-screen application is closed, an appbar receives the [**ABN\_FULLSCREENAPP**](abn-fullscreenapp.md) notification message.</span></span> <span data-ttu-id="6ffff-183">El parámetro *lParam* indica si la aplicación de pantalla completa se está abriendo o cerrando.</span><span class="sxs-lookup"><span data-stu-id="6ffff-183">The *lParam* parameter indicates whether the full-screen application is opening or closing.</span></span> <span data-ttu-id="6ffff-184">Si se está abriendo, el Appbar debe colocarse en la parte inferior del orden z.</span><span class="sxs-lookup"><span data-stu-id="6ffff-184">If it is opening, the appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="6ffff-185">El Appbar debe restaurar su posición en el orden z cuando se cierre la última aplicación de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="6ffff-185">The appbar should restore its z-order position when the last full-screen application has closed.</span></span>

<span data-ttu-id="6ffff-186">Un Appbar recibe el mensaje de notificación [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) cuando el usuario selecciona el comando Cascade, Tile horizontalmente o mosaicos verticalmente en el menú contextual de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="6ffff-186">An appbar receives the [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) notification message when the user selects the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span> <span data-ttu-id="6ffff-187">El sistema envía el mensaje dos veces, antes de reorganizar las ventanas (*lParam* es **true**) y después de organizar las ventanas (*lParam* es **false**).</span><span class="sxs-lookup"><span data-stu-id="6ffff-187">The system sends the message two times—before rearranging the windows (*lParam* is **TRUE**) and after arranging the windows (*lParam* is **FALSE**).</span></span>

<span data-ttu-id="6ffff-188">Un Appbar puede usar los mensajes de [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) para excluirse de la operación en cascada o de mosaico.</span><span class="sxs-lookup"><span data-stu-id="6ffff-188">An appbar can use [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) messages to exclude itself from the cascade or tile operation.</span></span> <span data-ttu-id="6ffff-189">Para excluirse, el Appbar debe ocultarse cuando *lParam* es **true** y mostrarse cuando *lParam* es **false**.</span><span class="sxs-lookup"><span data-stu-id="6ffff-189">To exclude itself, the appbar should hide itself when *lParam* is **TRUE** and show itself when *lParam* is **FALSE**.</span></span> <span data-ttu-id="6ffff-190">Si una Appbar se oculta en respuesta a este mensaje, no es necesario enviar los mensajes [**ABN \_ QUERYPOS**](abm-querypos.md) y [**ABN \_ SETPOS**](abm-setpos.md) en respuesta a la operación Cascade o Tile.</span><span class="sxs-lookup"><span data-stu-id="6ffff-190">If an appbar hides itself in response to this message, it does not need to send the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages in response to the cascade or tile operation.</span></span>

## <a name="registering-an-application-desktop-toolbar"></a><span data-ttu-id="6ffff-191">Registro de una barra de herramientas del escritorio de la aplicación</span><span class="sxs-lookup"><span data-stu-id="6ffff-191">Registering an Application Desktop Toolbar</span></span>

<span data-ttu-id="6ffff-192">Una aplicación debe registrar un Appbar mediante el envío [**del \_ nuevo mensaje ABN**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-192">An application must register an appbar by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="6ffff-193">El registro de un Appbar lo agrega a la lista interna del sistema y proporciona al sistema un identificador de mensaje que se usa para enviar mensajes de notificación al Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-193">Registering an appbar adds it to the system's internal list and provides the system with a message identifier to use to send notification messages to the appbar.</span></span> <span data-ttu-id="6ffff-194">Antes de salir, una aplicación debe anular el registro de la Appbar mediante el envío del mensaje [**ABN \_ Remove**](abm-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-194">Before exiting, an application must unregister the appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="6ffff-195">Al anular el registro se quita el Appbar de la lista interna del sistema y se impide que la barra reciba mensajes de notificación de Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-195">Unregistering removes the appbar from the system's internal list and prevents the bar from receiving appbar notification messages.</span></span>

<span data-ttu-id="6ffff-196">La función del ejemplo siguiente registra o anula el registro de un Appbar, dependiendo del valor de un parámetro de marca Boolean.</span><span class="sxs-lookup"><span data-stu-id="6ffff-196">The function in the following example either registers or unregisters an appbar, depending on the value of a Boolean flag parameter.</span></span>


```C++
// RegisterAccessBar - registers or unregisters an appbar. 
// Returns TRUE if successful, or FALSE otherwise. 

// hwndAccessBar - handle to the appbar 
// fRegister - register and unregister flag 

// Global variables 
//     g_uSide - screen edge (defaults to ABE_TOP) 
//     g_fAppRegistered - flag indicating whether the bar is registered 

BOOL RegisterAccessBar(HWND hwndAccessBar, BOOL fRegister) 
{ 
    APPBARDATA abd; 
    
    // An application-defined message identifier
    APPBAR_CALLBACK = (WM_USER + 0x01);
    
    // Specify the structure size and handle to the appbar. 
    abd.cbSize = sizeof(APPBARDATA); 
    abd.hWnd = hwndAccessBar; 

    if (fRegister) 
    { 
        // Provide an identifier for notification messages. 
        abd.uCallbackMessage = APPBAR_CALLBACK; 

        // Register the appbar. 
        if (!SHAppBarMessage(ABM_NEW, &abd)) 
            return FALSE; 

        g_uSide = ABE_TOP;       // default edge 
        g_fAppRegistered = TRUE; 

    } 
    else 
    { 
        // Unregister the appbar. 
        SHAppBarMessage(ABM_REMOVE, &abd); 
        g_fAppRegistered = FALSE; 
    } 

    return TRUE; 
}
```



## <a name="setting-the-appbar-size-and-position"></a><span data-ttu-id="6ffff-197">Establecer el tamaño y la posición de Appbar</span><span class="sxs-lookup"><span data-stu-id="6ffff-197">Setting the Appbar Size and Position</span></span>

<span data-ttu-id="6ffff-198">Una aplicación debe establecer el tamaño y la posición de una Appbar después de registrar el Appbar, después de que el usuario del usuario mueva o cambie el tamaño de la Appbar y siempre que el Appbar reciba el mensaje de notificación [**ABN \_ POSCHANGED**](abn-poschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-198">An application should set an appbar's size and position after registering the appbar, after the user user moves or sizes the appbar, and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="6ffff-199">Antes de establecer el tamaño y la posición del Appbar, la aplicación consulta el sistema para obtener un rectángulo delimitador aprobado mediante el envío del mensaje [**\_ QUERYPOS de ABN**](abm-querypos.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-199">Before setting the size and position of the appbar, the application queries the system for an approved bounding rectangle by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="6ffff-200">El sistema devuelve un rectángulo delimitador que no interfiere con la barra de tareas ni con ningún otro Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-200">The system returns a bounding rectangle that does not interfere with the taskbar or any other appbar.</span></span> <span data-ttu-id="6ffff-201">El sistema ajusta el rectángulo únicamente mediante la resta de rectángulos; no realiza ningún esfuerzo para conservar el tamaño inicial del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="6ffff-201">The system adjusts the rectangle purely by rectangle subtraction; it makes no effort to preserve the rectangle's initial size.</span></span> <span data-ttu-id="6ffff-202">Por esta razón, el Appbar debe volver a ajustar el rectángulo, según sea necesario, después de enviar **ABN \_ QUERYPOS**.</span><span class="sxs-lookup"><span data-stu-id="6ffff-202">For this reason, the appbar should readjust the rectangle, as necessary, after sending **ABM\_QUERYPOS**.</span></span>

<span data-ttu-id="6ffff-203">A continuación, la aplicación vuelve a pasar el rectángulo delimitador al sistema mediante el mensaje [**\_ SETPOS de ABN**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="6ffff-203">Next, the application passes the bounding rectangle back to the system by using the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span> <span data-ttu-id="6ffff-204">A continuación, llama a la función [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para mover el control Appbar a la posición.</span><span class="sxs-lookup"><span data-stu-id="6ffff-204">Then it calls the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="6ffff-205">En el ejemplo siguiente se muestra cómo establecer el tamaño y la posición de una Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-205">The following example shows how to set an appbar's size and position.</span></span>


```C++
// AppBarQuerySetPos - sets the size and position of an appbar. 

// uEdge - screen edge to which the appbar is to be anchored 
// lprc - current bounding rectangle of the appbar 
// pabd - address of the APPBARDATA structure with the hWnd and cbSize members filled

void PASCAL AppBarQuerySetPos(UINT uEdge, LPRECT lprc, PAPPBARDATA pabd) 
{ 
    int iHeight = 0; 
    int iWidth = 0; 

    pabd->rc = *lprc; 
    pabd->uEdge = uEdge; 

    // Copy the screen coordinates of the appbar's bounding 
    // rectangle into the APPBARDATA structure. 
    if ((uEdge == ABE_LEFT) || (uEdge == ABE_RIGHT)) 
    { 
        iWidth = pabd->rc.right - pabd->rc.left; 
        pabd->rc.top = 0; 
        pabd->rc.bottom = GetSystemMetrics(SM_CYSCREEN); 
    } 
    else 
    { 
        iHeight = pabd->rc.bottom - pabd->rc.top; 
        pabd->rc.left = 0; 
        pabd->rc.right = GetSystemMetrics(SM_CXSCREEN); 
    } 

    // Query the system for an approved size and position. 
    SHAppBarMessage(ABM_QUERYPOS, pabd); 

    // Adjust the rectangle, depending on the edge to which the appbar is anchored.
    switch (uEdge) 
    { 
        case ABE_LEFT: 
            pabd->rc.right = pabd->rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            pabd->rc.left = pabd->rc.right - iWidth; 
            break; 

        case ABE_TOP: 
            pabd->rc.bottom = pabd->rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            pabd->rc.top = pabd->rc.bottom - iHeight; 
            break; 
    } 

    // Pass the final bounding rectangle to the system. 
    SHAppBarMessage(ABM_SETPOS, pabd); 

    // Move and size the appbar so that it conforms to the 
    // bounding rectangle passed to the system. 
    MoveWindow(pabd->hWnd, 
               pabd->rc.left, 
               pabd->rc.top, 
               pabd->rc.right - pabd->rc.left, 
               pabd->rc.bottom - pabd->rc.top, 
               TRUE); 

}
```



## <a name="processing-appbar-notification-messages"></a><span data-ttu-id="6ffff-206">Procesamiento de mensajes de notificación de Appbar</span><span class="sxs-lookup"><span data-stu-id="6ffff-206">Processing Appbar Notification Messages</span></span>

<span data-ttu-id="6ffff-207">Un control Appbar recibe un mensaje de notificación cuando cambia el estado de la barra de tareas, cuando se inicia una aplicación de pantalla completa (o cuando se cierra la última) o cuando se produce un evento que puede afectar al tamaño y la posición de Appbar.</span><span class="sxs-lookup"><span data-stu-id="6ffff-207">An appbar receives a notification message when the state of the taskbar changes, when a full-screen application starts (or the last one closes), or when an event occurs that can affect the appbar's size and position.</span></span> <span data-ttu-id="6ffff-208">En el ejemplo siguiente se muestra cómo procesar los distintos mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="6ffff-208">The following example shows how to process the various notification messages.</span></span>


```C++
// AppBarCallback - processes notification messages sent by the system. 

// hwndAccessBar - handle to the appbar 
// uNotifyMsg - identifier of the notification message 
// lParam - message parameter 

void AppBarCallback(HWND hwndAccessBar, UINT uNotifyMsg, 
    LPARAM lParam) 
{ 
    APPBARDATA abd; 
    UINT uState; 

    abd.cbSize = sizeof(abd); 
    abd.hWnd = hwndAccessBar; 

    switch (uNotifyMsg) 
    { 
        case ABN_STATECHANGE: 

            // Check to see if the taskbar's always-on-top state has changed
            // and, if it has, change the appbar's state accordingly.
            uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

            SetWindowPos(hwndAccessBar, 
                         (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                         0, 0, 0, 0, 
                         SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 

            break; 

        case ABN_FULLSCREENAPP: 

            // A full-screen application has started, or the last full-screen
            // application has closed. Set the appbar's z-order appropriately.
            if (lParam) 
            { 
                SetWindowPos(hwndAccessBar, 
                             (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                             0, 0, 0, 0, 
                             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 
            else 
            { 
                uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

                if (uState & ABS_ALWAYSONTOP) 
                    SetWindowPos(hwndAccessBar, 
                                 HWND_TOPMOST, 
                                 0, 0, 0, 0, 
                                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 

        case ABN_POSCHANGED: 

            // The taskbar or another appbar has changed its size or position.
            AppBarPosChanged(&abd); 
            break; 
    } 
}
```



<span data-ttu-id="6ffff-209">La función siguiente ajusta el rectángulo de delimitación de una Appbar y, a continuación, llama a la función AppBarQuerySetPos definida por la aplicación (incluida en la sección anterior) para establecer el tamaño y la posición de la barra según corresponda.</span><span class="sxs-lookup"><span data-stu-id="6ffff-209">The following function adjusts an appbar's bounding rectangle and then calls the application-defined AppBarQuerySetPos function (included in the previous section) to set the bar's size and position accordingly.</span></span>


```C++
// AppBarPosChanged - adjusts the appbar's size and position. 

// pabd - address of an APPBARDATA structure that contains information 
//        used to adjust the size and position. 

void PASCAL AppBarPosChanged(PAPPBARDATA pabd) 
{ 
    RECT rc; 
    RECT rcWindow; 
    int iHeight; 
    int iWidth; 

    rc.top = 0; 
    rc.left = 0; 
    rc.right = GetSystemMetrics(SM_CXSCREEN); 
    rc.bottom = GetSystemMetrics(SM_CYSCREEN); 

    GetWindowRect(pabd->hWnd, &rcWindow); 

    iHeight = rcWindow.bottom - rcWindow.top; 
    iWidth = rcWindow.right - rcWindow.left; 

    switch (g_uSide) 
    { 
        case ABE_TOP: 
            rc.bottom = rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            rc.top = rc.bottom - iHeight; 
            break; 

        case ABE_LEFT: 
            rc.right = rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            rc.left = rc.right - iWidth; 
            break; 
    } 

    AppBarQuerySetPos(g_uSide, &rc, pabd); 
}
```



 

 
