---
description: El área de notificación es una parte de la barra de tareas que proporciona un origen temporal para las notificaciones y el estado.
ms.assetid: D37E2BF7-1887-4780-81AD-85B2117321E4
title: Notificaciones y el área de notificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af1d0b8af0b41674f79325f0eeb389cbc8f2c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360427"
---
# <a name="notifications-and-the-notification-area"></a><span data-ttu-id="3bd86-103">Notificaciones y el área de notificación</span><span class="sxs-lookup"><span data-stu-id="3bd86-103">Notifications and the Notification Area</span></span>

<span data-ttu-id="3bd86-104">El área de notificación es una parte de la barra de tareas que proporciona un origen temporal para las notificaciones y el estado.</span><span class="sxs-lookup"><span data-stu-id="3bd86-104">The notification area is a portion of the taskbar that provides a temporary source for notifications and status.</span></span> <span data-ttu-id="3bd86-105">También se puede usar para mostrar iconos de características del sistema y de programas que no tienen presencia en el escritorio, como el nivel de batería, el control de volumen y el estado de la red.</span><span class="sxs-lookup"><span data-stu-id="3bd86-105">It can also be used to display icons for system and program features that have no presence on the desktop, such as battery level, volume control, and network status.</span></span> <span data-ttu-id="3bd86-106">El área de notificación se ha conocido históricamente como la bandeja del sistema o el área de estado.</span><span class="sxs-lookup"><span data-stu-id="3bd86-106">The notification area has been known historically as the system tray or status area.</span></span>

<span data-ttu-id="3bd86-107">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="3bd86-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="3bd86-108">Instrucciones del área de notificación y notificación</span><span class="sxs-lookup"><span data-stu-id="3bd86-108">Notification and Notification Area Guidelines</span></span>](#notification-and-notification-area-guidelines)
-   [<span data-ttu-id="3bd86-109">Crear y mostrar una notificación</span><span class="sxs-lookup"><span data-stu-id="3bd86-109">Creating and Displaying a Notification</span></span>](#notifications-and-the-notification-area)
    -   [<span data-ttu-id="3bd86-110">Icono Agregar un aviso</span><span class="sxs-lookup"><span data-stu-id="3bd86-110">Add a Notification Icon</span></span>](#add-a-notification-icon)
    -   [<span data-ttu-id="3bd86-111">Definición de la versión de NOTIFYICONDATA</span><span class="sxs-lookup"><span data-stu-id="3bd86-111">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
    -   [<span data-ttu-id="3bd86-112">Definir la apariencia y el contenido de la notificación</span><span class="sxs-lookup"><span data-stu-id="3bd86-112">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
    -   [<span data-ttu-id="3bd86-113">Comprobar el estado del usuario</span><span class="sxs-lookup"><span data-stu-id="3bd86-113">Check the User Status</span></span>](#check-the-user-status)
    -   [<span data-ttu-id="3bd86-114">Mostrar la notificación</span><span class="sxs-lookup"><span data-stu-id="3bd86-114">Display the Notification</span></span>](#display-the-notification)
    -   [<span data-ttu-id="3bd86-115">Quitar un icono</span><span class="sxs-lookup"><span data-stu-id="3bd86-115">Removing an Icon</span></span>](#removing-an-icon)
-   [<span data-ttu-id="3bd86-116">Ejemplo de SDK</span><span class="sxs-lookup"><span data-stu-id="3bd86-116">SDK Sample</span></span>](#sdk-sample)
-   [<span data-ttu-id="3bd86-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3bd86-117">Related topics</span></span>](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a><span data-ttu-id="3bd86-118">Instrucciones del área de notificación y notificación</span><span class="sxs-lookup"><span data-stu-id="3bd86-118">Notification and Notification Area Guidelines</span></span>

<span data-ttu-id="3bd86-119">Consulte las secciones [notificaciones](../uxguide/mess-notif.md) y del [área de notificación](../uxguide/winenv-notification.md) de las instrucciones de interacción de la experiencia del usuario de Windows para conocer los procedimientos recomendados para el uso de notificaciones y el área de notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-119">See the [Notifications](../uxguide/mess-notif.md) and [Notification Area](../uxguide/winenv-notification.md) sections of the Windows User Experience Interaction Guidelines for best practices in the use of notifications and the notification area.</span></span> <span data-ttu-id="3bd86-120">El objetivo es proporcionar a los usuarios ventajas mediante el uso adecuado de las notificaciones, sin ser molestas ni distraer.</span><span class="sxs-lookup"><span data-stu-id="3bd86-120">The goal is to provide user benefit through appropriate use of notifications, without being annoying or distracting.</span></span>

<span data-ttu-id="3bd86-121">El área de notificación no es para información crítica que se debe actuar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="3bd86-121">The notification area is not for critical information that must be acted on immediately.</span></span> <span data-ttu-id="3bd86-122">Tampoco está pensado para el acceso rápido a programas o comandos.</span><span class="sxs-lookup"><span data-stu-id="3bd86-122">It is also not intended for quick program or command access.</span></span> <span data-ttu-id="3bd86-123">A partir de Windows 7, gran parte de esa funcionalidad se consigue mejor a través del botón de la barra de tareas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-123">As of Windows 7, much of that functionality is best accomplished through an application's taskbar button.</span></span>

<span data-ttu-id="3bd86-124">Windows 7 permite a un usuario suprimir todas las notificaciones de una aplicación si eligen, por lo que el diseño y el uso de las notificaciones determinan el usuario para permitir que la aplicación siga apareciendo.</span><span class="sxs-lookup"><span data-stu-id="3bd86-124">Windows 7 allows a user to suppress all notifications from an application if they choose, so thoughtful notification design and use will incline the user to allow your application to continue to display them.</span></span> <span data-ttu-id="3bd86-125">Las notificaciones son una interrupción; Asegúrese de que merece la pena.</span><span class="sxs-lookup"><span data-stu-id="3bd86-125">Notifications are an interruption; ensure that they are worth it.</span></span>

<span data-ttu-id="3bd86-126">Windows 7 presenta el concepto de "tiempo de inactividad".</span><span class="sxs-lookup"><span data-stu-id="3bd86-126">Windows 7 introduces the concept of "quiet time".</span></span> <span data-ttu-id="3bd86-127">El tiempo de inactividad se define como la primera hora después de que un nuevo usuario inicie sesión en su cuenta por primera vez o por primera vez después de una actualización de sistema operativo o una instalación limpia.</span><span class="sxs-lookup"><span data-stu-id="3bd86-127">Quiet time is defined as the first hour after a new user logs into his or her account either for the first time or for the first time after an operating system upgrade or clean installation.</span></span> <span data-ttu-id="3bd86-128">Este tiempo se reserva para permitir que el usuario explore y se familiarice con el nuevo entorno sin la distracción de las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="3bd86-128">This time is set aside to allow the user to explore and familiarize themselves with the new environment without the distraction of notifications.</span></span> <span data-ttu-id="3bd86-129">Durante este tiempo, la mayoría de las notificaciones no se deben enviar ni mostrar.</span><span class="sxs-lookup"><span data-stu-id="3bd86-129">During this time, most notifications should not be sent or shown.</span></span> <span data-ttu-id="3bd86-130">Las excepciones incluyen comentarios que el usuario esperaría ver en respuesta a una acción del usuario, como cuando se conecta en un dispositivo USB o imprime un documento.</span><span class="sxs-lookup"><span data-stu-id="3bd86-130">Exceptions include feedback that the user would expect to see in response to a user action, such as when he or she plugs in a USB device or prints a document.</span></span> <span data-ttu-id="3bd86-131">Más adelante en este tema se describen las características específicas de la API de en relación con el tiempo de inactividad.</span><span class="sxs-lookup"><span data-stu-id="3bd86-131">API specifics of regarding quiet time are discussed later in this topic.</span></span>

## <a name="creating-and-displaying-a-notification"></a><span data-ttu-id="3bd86-132">Crear y mostrar una notificación</span><span class="sxs-lookup"><span data-stu-id="3bd86-132">Creating and Displaying a Notification</span></span>

<span data-ttu-id="3bd86-133">En las secciones restantes de este tema se describe el procedimiento básico que se debe seguir para mostrar una notificación de la aplicación al usuario.</span><span class="sxs-lookup"><span data-stu-id="3bd86-133">The remaining sections in this topic outline the basic procedure to follow to display a notification from your application to the user.</span></span>

1.  [<span data-ttu-id="3bd86-134">Icono Agregar un aviso</span><span class="sxs-lookup"><span data-stu-id="3bd86-134">Add a Notification Icon</span></span>](#add-a-notification-icon)
2.  [<span data-ttu-id="3bd86-135">Definición de la versión de NOTIFYICONDATA</span><span class="sxs-lookup"><span data-stu-id="3bd86-135">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
3.  [<span data-ttu-id="3bd86-136">Definir la apariencia y el contenido de la notificación</span><span class="sxs-lookup"><span data-stu-id="3bd86-136">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
4.  [<span data-ttu-id="3bd86-137">Comprobar el estado del usuario</span><span class="sxs-lookup"><span data-stu-id="3bd86-137">Check the User Status</span></span>](#check-the-user-status)
5.  [<span data-ttu-id="3bd86-138">Mostrar la notificación</span><span class="sxs-lookup"><span data-stu-id="3bd86-138">Display the Notification</span></span>](#display-the-notification)
6.  [<span data-ttu-id="3bd86-139">Quitar un icono</span><span class="sxs-lookup"><span data-stu-id="3bd86-139">Removing an Icon</span></span>](#removing-an-icon)

### <a name="add-a-notification-icon"></a><span data-ttu-id="3bd86-140">Icono Agregar un aviso</span><span class="sxs-lookup"><span data-stu-id="3bd86-140">Add a Notification Icon</span></span>

<span data-ttu-id="3bd86-141">Para mostrar una notificación, debe tener un icono en el área de notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-141">To display a notification, you must have an icon in the notification area.</span></span> <span data-ttu-id="3bd86-142">En algunos casos, como Microsoft Communicator o el nivel de batería, ese icono ya estará presente.</span><span class="sxs-lookup"><span data-stu-id="3bd86-142">In certain cases, such as Microsoft Communicator or battery level, that icon will already be present.</span></span> <span data-ttu-id="3bd86-143">En muchos otros casos, sin embargo, agregará un icono al área de notificación solo cuando sea necesario para mostrar la notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-143">In many other cases, however, you will add an icon to the notification area only as long as is needed to show the notification.</span></span> <span data-ttu-id="3bd86-144">En cualquier caso, esto se logra mediante la [**función \_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) .</span><span class="sxs-lookup"><span data-stu-id="3bd86-144">In either case, this is accomplished using the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) function.</span></span> <span data-ttu-id="3bd86-145">**Shell \_ de NotifyIcon** permite agregar, modificar o eliminar un icono en el área de notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-145">**Shell\_NotifyIcon** allows you to add, modify, or delete an icon in the notification area.</span></span>

![área de notificación que contiene tres iconos](images/taskbar/notificationareaicons.png)

<span data-ttu-id="3bd86-147">Cuando se agrega un icono al área de notificación en Windows 7, se agrega de forma predeterminada a la sección de desbordamiento del área de notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-147">When an icon is added to the notification area on Windows 7, it is added to the overflow section of the notification area by default.</span></span> <span data-ttu-id="3bd86-148">Esta área contiene iconos del área de notificación que están activos, pero no visibles en el área de notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-148">This area contains notification area icons that are active, but not visible in the notification area.</span></span> <span data-ttu-id="3bd86-149">Solo el usuario puede promocionar un icono del desbordamiento en el área de notificación, aunque en determinadas circunstancias el sistema puede promover temporalmente un icono en el área de notificación como una vista previa corta (menos de un minuto).</span><span class="sxs-lookup"><span data-stu-id="3bd86-149">Only the user can promote an icon from the overflow to the notification area, although in certain circumstances the system can temporarily promote an icon into the notification area as a short preview (under one minute).</span></span>

> [!Note]  
> <span data-ttu-id="3bd86-150">El usuario debe tener el final de la señal en qué iconos desea ver en el área de notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-150">The user should have the final say on which icons they want to see in their notification area.</span></span> <span data-ttu-id="3bd86-151">Antes de instalar un icono no transitorio en el área de notificación, se debe solicitar permiso al usuario.</span><span class="sxs-lookup"><span data-stu-id="3bd86-151">Before installing a non-transient icon in the notification area, the user should be asked for permission.</span></span> <span data-ttu-id="3bd86-152">También se les debe proporcionar la opción (normalmente, a través de su menú contextual) para quitar el icono del área de notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-152">They should also be given the option (normally though its shortcut menu) to remove the icon from the notification area.</span></span>

 

<span data-ttu-id="3bd86-153">La estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) enviada en la llamada a [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contiene información que especifica el icono del área de notificación y la propia notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-153">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification itself.</span></span> <span data-ttu-id="3bd86-154">A continuación se muestran los elementos específicos del propio icono del área de notificación que se pueden establecer a través de **NOTIFYICONDATA**.</span><span class="sxs-lookup"><span data-stu-id="3bd86-154">The following are those items specific to the notification area icon itself that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="3bd86-155">Recurso del que se toma el icono.</span><span class="sxs-lookup"><span data-stu-id="3bd86-155">The resource from which the icon is taken.</span></span>
-   <span data-ttu-id="3bd86-156">Identificador único para el icono.</span><span class="sxs-lookup"><span data-stu-id="3bd86-156">A unique identifier for the icon.</span></span>
-   <span data-ttu-id="3bd86-157">Estilo de la información sobre herramientas del icono.</span><span class="sxs-lookup"><span data-stu-id="3bd86-157">The style of the icon's tooltip.</span></span>
-   <span data-ttu-id="3bd86-158">El estado del icono (oculto, compartido o ambos) en el área de notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-158">The icon's state (hidden, shared, or both) in the notification area.</span></span>
-   <span data-ttu-id="3bd86-159">Identificador de una ventana de la aplicación asociada al icono.</span><span class="sxs-lookup"><span data-stu-id="3bd86-159">The handle of an application window associated with the icon.</span></span>
-   <span data-ttu-id="3bd86-160">Un identificador de mensaje de devolución de llamada que permite al icono comunicar eventos que se producen dentro del rectángulo delimitador del icono y la notificación de globo con la ventana de la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="3bd86-160">A callback message identifier that allows the icon to communicate events that occur within the icon's bounding rectangle and balloon notification with the associated application window.</span></span> <span data-ttu-id="3bd86-161">El rectángulo delimitador del icono se puede recuperar a través del [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).</span><span class="sxs-lookup"><span data-stu-id="3bd86-161">The icon's bounding rectangle can be retrieved through [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).</span></span>

<span data-ttu-id="3bd86-162">Cada icono del área de notificación puede identificarse de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="3bd86-162">Each icon in the notification area can be identified in two ways:</span></span>

-   <span data-ttu-id="3bd86-163">GUID con el que se declara el icono en el registro.</span><span class="sxs-lookup"><span data-stu-id="3bd86-163">The GUID with which the icon is declared in the registry.</span></span> <span data-ttu-id="3bd86-164">Este es el método preferido en Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3bd86-164">This is the preferred method on Windows 7 and later.</span></span>
-   <span data-ttu-id="3bd86-165">Identificador de una ventana asociada al icono del área de notificación, más un identificador de icono definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-165">The handle of a window associated with the notification area icon, plus an application-defined icon identifier.</span></span> <span data-ttu-id="3bd86-166">Este método se utiliza en Windows Vista y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3bd86-166">This method is used on Windows Vista and earlier.</span></span>

<span data-ttu-id="3bd86-167">Los iconos del área de notificación pueden tener información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="3bd86-167">Icons in the notification area can have a tooltip.</span></span> <span data-ttu-id="3bd86-168">La información sobre herramientas puede ser una información sobre herramientas estándar (preferida) o una interfaz de usuario emergente dibujada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-168">The tooltip can be either a standard tooltip (preferred) or an application-drawn, pop-up UI.</span></span> <span data-ttu-id="3bd86-169">Aunque no se requiere una información sobre herramientas, se recomienda.</span><span class="sxs-lookup"><span data-stu-id="3bd86-169">While a tooltip is not required, it is recommended.</span></span>

<span data-ttu-id="3bd86-170">Los iconos del área de notificación deben tener un reconocimiento de PPP alto.</span><span class="sxs-lookup"><span data-stu-id="3bd86-170">Notification area icons should be high-DPI aware.</span></span> <span data-ttu-id="3bd86-171">Una aplicación debe proporcionar un icono de 16x16 píxeles y un icono de 32x32 en su archivo de recursos y, a continuación, usar [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) para asegurarse de que se carga y escala correctamente el icono correcto.</span><span class="sxs-lookup"><span data-stu-id="3bd86-171">An application should provide both a 16x16 pixel icon and a 32x32 icon in its resource file, and then use [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) to ensure that the correct icon is loaded and scaled appropriately.</span></span>

<span data-ttu-id="3bd86-172">La aplicación responsable del icono del área de notificación debe controlar un clic del mouse para ese icono.</span><span class="sxs-lookup"><span data-stu-id="3bd86-172">The application responsible for the notification area icon should handle a mouse click for that icon.</span></span> <span data-ttu-id="3bd86-173">Cuando un usuario hace clic con el botón secundario en el icono, debe mostrar un menú contextual normal.</span><span class="sxs-lookup"><span data-stu-id="3bd86-173">When a user right-clicks the icon, it should bring up a normal shortcut menu.</span></span> <span data-ttu-id="3bd86-174">Sin embargo, el resultado de un solo clic con el botón primario del mouse variará con la función del icono.</span><span class="sxs-lookup"><span data-stu-id="3bd86-174">However, the result of a single click with the left mouse button will vary with the function of the icon.</span></span> <span data-ttu-id="3bd86-175">Debería mostrar lo que el usuario esperaría ver en el formulario más adecuado para ese contenido, una ventana emergente, un cuadro de diálogo o la propia ventana del programa.</span><span class="sxs-lookup"><span data-stu-id="3bd86-175">It should display what the user would expect to see in the form best suited to that content—a popup window, a dialog box or the program window itself.</span></span> <span data-ttu-id="3bd86-176">Por ejemplo, podría mostrar el texto de estado de un icono de estado o un control deslizante para el control de volumen.</span><span class="sxs-lookup"><span data-stu-id="3bd86-176">For instance, it could show status text for a status icon, or a slider for the volume control.</span></span>

<span data-ttu-id="3bd86-177">La posición de un cuadro de diálogo o ventana emergente que resulte de click debe colocarse cerca de la coordenada del clic en el área de notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-177">The placement of a popup window or dialog box that results from the click should be placed near the coordinate of the click in the notification area.</span></span> <span data-ttu-id="3bd86-178">Use [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) para determinar su ubicación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-178">Use the [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) to determine its location.</span></span>

<span data-ttu-id="3bd86-179">Se puede Agregar el icono al área de notificación sin mostrar una notificación definiendo solo los miembros específicos del icono de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (descrito anteriormente) y llamando [**a \_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) , como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="3bd86-179">The icon can be added to the notification area without displaying a notification by defining only the icon-specific members of [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (discussed above) and calling [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) as shown here:</span></span>


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



<span data-ttu-id="3bd86-180">También puede Agregar el icono al área de notificación y mostrar una notificación en una llamada a NotifyIcon de [**Shell \_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="3bd86-180">You can also add the icon to the notification area and display a notification all in one call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="3bd86-181">Para ello, continúe con las instrucciones de este tema.</span><span class="sxs-lookup"><span data-stu-id="3bd86-181">To do so, continue with the instructions in this topic.</span></span>

### <a name="define-the-notifyicondata-version"></a><span data-ttu-id="3bd86-182">Definición de la versión de NOTIFYICONDATA</span><span class="sxs-lookup"><span data-stu-id="3bd86-182">Define the NOTIFYICONDATA Version</span></span>

<span data-ttu-id="3bd86-183">A medida que Windows ha progresado, la estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) se ha expandido para incluir más miembros para definir más funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="3bd86-183">As Windows has progressed, the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure has expanded to include more members to define more functionality.</span></span> <span data-ttu-id="3bd86-184">Las constantes se usan para declarar la versión de **NOTIFYICONDATA** que se va a usar con el icono del área de notificación, a fin de permitir la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="3bd86-184">Constants are used to declare which version of **NOTIFYICONDATA** to use with your notification area icon, to allow for backward compatibility.</span></span> <span data-ttu-id="3bd86-185">A menos que haya una razón de peso para hacer lo contrario, se recomienda encarecidamente que use la versión de NOTIFYICON \_ versión \_ 4, que se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3bd86-185">Unless there is a compelling reason to do otherwise, it is strongly recommended that you use the NOTIFYICON\_VERSION\_4 version, introduced in Windows Vista.</span></span> <span data-ttu-id="3bd86-186">Esta versión proporciona toda la funcionalidad disponible, incluida la capacidad preferida para identificar el icono del área de notificación a través de un GUID registrado, un mecanismo de devolución de llamada superior y una mejor accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="3bd86-186">This version provides the full available functionality, including the preferred ability to identify the notification area icon though a registered GUID, a superior callback mechanism, and better accessibility.</span></span>

<span data-ttu-id="3bd86-187">Establezca la versión a través de las llamadas siguientes:</span><span class="sxs-lookup"><span data-stu-id="3bd86-187">Set the version through the following calls:</span></span>


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



<span data-ttu-id="3bd86-188">Tenga en cuenta que esta llamada a [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) no muestra una notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-188">Note that this call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) does not display a notification.</span></span>

### <a name="define-the-notification-look-and-contents"></a><span data-ttu-id="3bd86-189">Definir la apariencia y el contenido de la notificación</span><span class="sxs-lookup"><span data-stu-id="3bd86-189">Define the Notification Look and Contents</span></span>

<span data-ttu-id="3bd86-190">Una notificación es un tipo especial de control ToolTip de globo.</span><span class="sxs-lookup"><span data-stu-id="3bd86-190">A notification is a special type of balloon tooltip control.</span></span> <span data-ttu-id="3bd86-191">Contiene un título, texto de cuerpo y un icono.</span><span class="sxs-lookup"><span data-stu-id="3bd86-191">It contains a title, body text, and an icon.</span></span> <span data-ttu-id="3bd86-192">Al igual que una ventana, tiene un botón **cerrar** en la esquina superior derecha.</span><span class="sxs-lookup"><span data-stu-id="3bd86-192">Like a window, it has a **Close** button in its upper right corner.</span></span> <span data-ttu-id="3bd86-193">También contiene un botón **Opciones** que abre el elemento iconos del área de notificación en el panel de control, que permite al usuario Mostrar u ocultar el icono o mostrar solo notificaciones sin icono.</span><span class="sxs-lookup"><span data-stu-id="3bd86-193">It also contains a **Options** button that opens the Notification Area Icons item in the Control Panel, which allows the user to show or hide the icon or show only notifications without an icon.</span></span>

![captura de pantalla del globo de notificación que indica que la energía de la batería es baja](images/taskbar/notificationballoon.png)

<span data-ttu-id="3bd86-195">La estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) enviada en la llamada a [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contiene información que especifica tanto el icono del área de notificación como el globo de notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-195">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification balloon itself.</span></span> <span data-ttu-id="3bd86-196">A continuación se muestran los elementos específicos de la notificación que se pueden establecer a través de **NOTIFYICONDATA**.</span><span class="sxs-lookup"><span data-stu-id="3bd86-196">The following are those items specific to the notification that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="3bd86-197">Icono que se va a mostrar en el globo de notificación, que se especifica mediante el tipo de notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-197">An icon to display in the notification balloon, which is specified by the notification type.</span></span> <span data-ttu-id="3bd86-198">Se puede especificar el tamaño del icono, así como los iconos personalizados.</span><span class="sxs-lookup"><span data-stu-id="3bd86-198">The size of the icon can be specified, as well as custom icons.</span></span>
-   <span data-ttu-id="3bd86-199">Título de la notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-199">A notification title.</span></span> <span data-ttu-id="3bd86-200">Este título debe tener una longitud máxima de 48 caracteres en inglés (para dar cabida a la localización).</span><span class="sxs-lookup"><span data-stu-id="3bd86-200">This title should be a maximum of 48 characters long in English (to accommodate localization).</span></span> <span data-ttu-id="3bd86-201">El título es la primera línea de la notificación y se separa mediante el uso de tamaño de fuente, color y peso.</span><span class="sxs-lookup"><span data-stu-id="3bd86-201">The title is the first line of the notification, and set apart through the use of font size, color, and weight.</span></span>
-   <span data-ttu-id="3bd86-202">Texto que se va a usar en el cuerpo de la notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-202">Text for use in the body of the notification.</span></span> <span data-ttu-id="3bd86-203">Este texto debe tener un máximo de 200 caracteres en inglés (para dar cabida a la localización).</span><span class="sxs-lookup"><span data-stu-id="3bd86-203">This text should be a maximum of 200 characters in English (to accommodate localization).</span></span>
-   <span data-ttu-id="3bd86-204">Si la notificación se debe descartar si no se puede mostrar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="3bd86-204">Whether the notification should be discarded if it cannot be displayed immediately.</span></span>
-   <span data-ttu-id="3bd86-205">Un tiempo de espera para la notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-205">A timeout for the notification.</span></span> <span data-ttu-id="3bd86-206">Este valor se omite en Windows Vista y sistemas posteriores en favor de una configuración de tiempo de espera de accesibilidad para todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="3bd86-206">This setting is ignored in Windows Vista and later systems in favor of a system-wide accessibility timeout setting.</span></span>
-   <span data-ttu-id="3bd86-207">Si la notificación debe respetar el tiempo de inactividad, establezca el valor de la marca [**NIIF \_ respetar el \_ \_ tiempo de silencio**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) .</span><span class="sxs-lookup"><span data-stu-id="3bd86-207">Whether the notification should respect quiet time, set through the [**NIIF\_RESPECT\_QUIET\_TIME**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) flag.</span></span>

> [!Note]  
> <span data-ttu-id="3bd86-208">Las interfaces [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) y [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) son contenedores del modelo de objetos componentes (com) para el [**\_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="3bd86-208">The [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) and [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) interfaces are Component Object Model (COM) wrappers for [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="3bd86-209">Sin embargo, en este momento, no proporcionan la funcionalidad completa de NOTIFYICON \_ versión \_ 4 disponible a través del **\_ NotifyIcon del shell** directamente, incluido el uso de un GUID para identificar el icono del área de notificación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-209">However, at this time, they do not provide the full NOTIFYICON\_VERSION\_4 functionality available through **Shell\_NotifyIcon** directly, including the use of a GUID to identify the notification area icon.</span></span>

 

### <a name="check-the-user-status"></a><span data-ttu-id="3bd86-210">Comprobar el estado del usuario</span><span class="sxs-lookup"><span data-stu-id="3bd86-210">Check the User Status</span></span>

<span data-ttu-id="3bd86-211">El sistema utiliza la función [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) se usa para comprobar si el usuario está en tiempo de inactividad, fuera del equipo o en un estado ininterrumpido como, por ejemplo, el modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="3bd86-211">The system uses the [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) function is used to check whether the user is in quiet time, away from the computer, or in an uninterruptable state such as Presentation mode.</span></span> <span data-ttu-id="3bd86-212">El hecho de que el sistema muestre la notificación dependerá de este estado.</span><span class="sxs-lookup"><span data-stu-id="3bd86-212">Whether the system displays your notification depends on this state.</span></span>

> [!Note]  
> <span data-ttu-id="3bd86-213">Si la aplicación usa un método de notificación personalizado que no usa el [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)o [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), siempre debe llamar explícitamente a [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) para determinar si debe mostrar la interfaz de usuario de notificaciones en ese momento.</span><span class="sxs-lookup"><span data-stu-id="3bd86-213">If your application is using a custom notification method that does not use [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification), or [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), it should always explicitly call [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) to determine whether it should display notification UI at that time.</span></span>

 

<span data-ttu-id="3bd86-214">Las notificaciones que se envían cuando el usuario está en cola para su presentación, pero dado que no puede saber cuándo devolverá el usuario o si la notificación seguirá siendo válida en ese momento, considere la posibilidad de volver a enviar la notificación más adelante.</span><span class="sxs-lookup"><span data-stu-id="3bd86-214">Notifications sent when the user is away are queued for display, but because you cannot know when the user will return or whether the notification will still be valid at that time, you might consider resending the notification later.</span></span>

<span data-ttu-id="3bd86-215">Las notificaciones enviadas durante el tiempo de inactividad se descartan.</span><span class="sxs-lookup"><span data-stu-id="3bd86-215">Notifications sent during quiet time are discarded unshown.</span></span> <span data-ttu-id="3bd86-216">Las directrices de diseño le piden que todas las notificaciones se puedan omitir.</span><span class="sxs-lookup"><span data-stu-id="3bd86-216">Design guidelines ask that all notifications be ignorable.</span></span> <span data-ttu-id="3bd86-217">No deben requerir la intervención inmediata del usuario.</span><span class="sxs-lookup"><span data-stu-id="3bd86-217">They should not require immediate user action.</span></span> <span data-ttu-id="3bd86-218">Por lo tanto, ninguna notificación es tan importante que deba invalidar el tiempo de silencio.</span><span class="sxs-lookup"><span data-stu-id="3bd86-218">Therefore, no notification is so important that it should override quiet time.</span></span>

### <a name="display-the-notification"></a><span data-ttu-id="3bd86-219">Mostrar la notificación</span><span class="sxs-lookup"><span data-stu-id="3bd86-219">Display the Notification</span></span>

<span data-ttu-id="3bd86-220">Una vez que haya establecido la versión de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) y haya definido la notificación en una estructura **NOTIFYICONDATA** , llame a [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para mostrar el icono.</span><span class="sxs-lookup"><span data-stu-id="3bd86-220">Once you have set the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) version and defined the notification in a **NOTIFYICONDATA** structure, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to display the icon.</span></span>

-   <span data-ttu-id="3bd86-221">Si no está presente el icono del área de notificación, llame a [**\_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para agregar el icono.</span><span class="sxs-lookup"><span data-stu-id="3bd86-221">If the notification area icon is not present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to add the icon.</span></span> <span data-ttu-id="3bd86-222">Haga esto para los iconos transitorios y no transitorios.</span><span class="sxs-lookup"><span data-stu-id="3bd86-222">Do this for both transient and non-transient icons.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   <span data-ttu-id="3bd86-223">Si el icono del área de notificación ya está presente, llame a [**\_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para modificar el icono.</span><span class="sxs-lookup"><span data-stu-id="3bd86-223">If the notification area icon is already present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to modify the icon.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

<span data-ttu-id="3bd86-224">En el código siguiente se muestra un ejemplo de configuración de datos de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) y su envío a través del [**\_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="3bd86-224">The following code shows an example of setting [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) data and sending it through [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="3bd86-225">Tenga en cuenta que en este ejemplo se identifica el icono de notificación a través de un GUID (preferido en Windows 7).</span><span class="sxs-lookup"><span data-stu-id="3bd86-225">Note that this example identifies the notification icon through a GUID (preferred in Windows 7).</span></span>


```
// Declare NOTIFYICONDATA details. 
    // Error handling is omitted here for brevity. Do not omit it in your code.
    
    NOTIFYICONDATA nid = {};
    nid.cbSize = sizeof(nid);
    nid.hWnd = hWnd;
    nid.uFlags = NIF_ICON | NIF_TIP | NIF_GUID;
    
    // Note: This is an example GUID only and should not be used.
    // Normally, you should use a GUID-generating tool to provide the value to
    // assign to guidItem.
    static const GUID myGUID = 
    {0x23977b55, 0x10e0, 0x4041, {0xb8, 0x62, 0xb1, 0x95, 0x41, 0x96, 0x36, 0x69}};
    nid.guidItem = myGUID;
    
    nid.guidItem = guid;
    
    // This text will be shown as the icon's tooltip.
    StringCchCopy(nid.szTip, ARRAYSIZE(nid.szTip), L"Test application");
    
    // Load the icon for high DPI.
    LoadIconMetric(hInst, MAKEINTRESOURCE(IDI_SMALL), LIM_SMALL, &(nid.hIcon));
    
    // Show the notification.
    Shell_NotifyIcon(NIM_ADD, &nid) ? S_OK : E_FAIL;
```



### <a name="removing-an-icon"></a><span data-ttu-id="3bd86-226">Quitar un icono</span><span class="sxs-lookup"><span data-stu-id="3bd86-226">Removing an Icon</span></span>

<span data-ttu-id="3bd86-227">Para quitar un icono, por ejemplo, cuando solo se ha agregado el icono temporalmente para difundir una notificación, llame [**a \_ NotifyIcon del shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="3bd86-227">To remove an icon—for instance, when you have only added the icon temporarily to broadcast a notification—call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)as shown here.</span></span> <span data-ttu-id="3bd86-228">En esta llamada solo se necesita una estructura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) mínima que identifique el icono.</span><span class="sxs-lookup"><span data-stu-id="3bd86-228">Only a minimal [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure that identifies the icon is needed in this call.</span></span>


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> <span data-ttu-id="3bd86-229">Cuando se desinstala una aplicación, es posible que el icono del área de notificación siga apareciendo al usuario como una opción en la página iconos del área de notificación del panel de control durante siete días como máximo.</span><span class="sxs-lookup"><span data-stu-id="3bd86-229">When an application is uninstalled, its notification area icon can still appear to the user as an option in the Notification Area Icons page in the Control Panel for up to seven days.</span></span> <span data-ttu-id="3bd86-230">Sin embargo, los cambios realizados no tendrán ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="3bd86-230">However, any changes made there will have no effect.</span></span>

 

## <a name="sdk-sample"></a><span data-ttu-id="3bd86-231">Ejemplo de SDK</span><span class="sxs-lookup"><span data-stu-id="3bd86-231">SDK Sample</span></span>

<span data-ttu-id="3bd86-232">Vea el ejemplo de [ejemplo NotificationIcon](samples-notificationicon.md) en el kit de desarrollo de software (SDK) de Windows para obtener un ejemplo completo del uso del [**\_ NotifyIcon de Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="3bd86-232">See the [NotificationIcon Sample](samples-notificationicon.md) sample in the Windows Software Development Kit (SDK) for a full example of the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bd86-233">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3bd86-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bd86-234">**NotifyIcon de Shell \_**</span><span class="sxs-lookup"><span data-stu-id="3bd86-234">**Shell\_NotifyIcon**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
</dt> <dt>

[<span data-ttu-id="3bd86-235">**Shell \_ NotifyIconGetRect**</span><span class="sxs-lookup"><span data-stu-id="3bd86-235">**Shell\_NotifyIconGetRect**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)
</dt> <dt>

[<span data-ttu-id="3bd86-236">**NOTIFYICONDATA**</span><span class="sxs-lookup"><span data-stu-id="3bd86-236">**NOTIFYICONDATA**</span></span>](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)
</dt> <dt>

[<span data-ttu-id="3bd86-237">**SHQueryUserNotificationState**</span><span class="sxs-lookup"><span data-stu-id="3bd86-237">**SHQueryUserNotificationState**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate)
</dt> <dt>

[<span data-ttu-id="3bd86-238">**IUserNotification**</span><span class="sxs-lookup"><span data-stu-id="3bd86-238">**IUserNotification**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)
</dt> <dt>

[<span data-ttu-id="3bd86-239">**IUserNotification2**</span><span class="sxs-lookup"><span data-stu-id="3bd86-239">**IUserNotification2**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)
</dt> <dt>

[<span data-ttu-id="3bd86-240">La barra de tareas</span><span class="sxs-lookup"><span data-stu-id="3bd86-240">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="3bd86-241">Extensiones de la barra de tareas</span><span class="sxs-lookup"><span data-stu-id="3bd86-241">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
