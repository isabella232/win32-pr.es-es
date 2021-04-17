---
description: Un paquete de notificación de Winlogon es un archivo DLL que exporta funciones que controlan eventos de Winlogon. Por ejemplo, cuando un usuario inicia sesión en el sistema, Winlogon llama a la función de controlador de eventos Logon de cada paquete de notificaciones para proporcionar información sobre el evento.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Crear un paquete de notificación Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0127674967ee3155d42e143a1b142d8c83137c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652683"
---
# <a name="creating-a-winlogon-notification-package"></a><span data-ttu-id="a2d0a-104">Crear un paquete de notificación Winlogon</span><span class="sxs-lookup"><span data-stu-id="a2d0a-104">Creating a Winlogon Notification Package</span></span>

<span data-ttu-id="a2d0a-105">Un paquete de notificación de [*Winlogon*](/windows/desktop/SecGloss/w-gly) es un archivo DLL que exporta funciones que controlan eventos de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="a2d0a-105">A [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="a2d0a-106">Por ejemplo, cuando un usuario inicia sesión en el sistema, Winlogon llama a la función de controlador de eventos Logon de cada paquete de notificaciones para proporcionar información sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="a2d0a-106">For example, when a user logs onto the system, Winlogon calls each notification package's logon event handler function to provide information about the event.</span></span>

<span data-ttu-id="a2d0a-107">Los nombres de las funciones del controlador de eventos que se implementan en un paquete de notificación se dejan al desarrollador; Winlogon comprueba el registro para obtener los nombres de las funciones de controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="a2d0a-107">The names of the event handler functions implemented in a notification package are left up to the developer; Winlogon checks the registry to obtain the names of the event handler functions.</span></span> <span data-ttu-id="a2d0a-108">Por ejemplo, un paquete de notificación podría implementar la función de controlador de eventos Logon como, `WLEventLogon` mientras que otra podría usar `HandleLogonEvent` .</span><span class="sxs-lookup"><span data-stu-id="a2d0a-108">For example, one notification package might implement the logon event handler function as `WLEventLogon` whereas another might use `HandleLogonEvent`.</span></span>

<span data-ttu-id="a2d0a-109">No es necesario implementar y registrar controladores de eventos para todos los eventos Winlogon, solo para los eventos que son útiles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a2d0a-109">You do not have to implement and register event handlers for every Winlogon event, only for events that are useful to your application.</span></span> <span data-ttu-id="a2d0a-110">Cada función de controlador de eventos debe usar el prototipo de función descrito en [prototipo de función de controlador de eventos](event-handler-function-prototype.md).</span><span class="sxs-lookup"><span data-stu-id="a2d0a-110">Each event handler function must use the function prototype described in [Event Handler Function Prototype](event-handler-function-prototype.md).</span></span> <span data-ttu-id="a2d0a-111">Este prototipo tiene un único parámetro: una estructura de [**\_ \_ información de notificación WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) que contiene detalles sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="a2d0a-111">This prototype has a single parameter: a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains details about the event.</span></span>

<span data-ttu-id="a2d0a-112">Winlogon omite la salida de las funciones de controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="a2d0a-112">Winlogon ignores the output of event handler functions.</span></span> <span data-ttu-id="a2d0a-113">Si el control de un evento requiere interactuar con Winlogon, use las [funciones de compatibilidad de Winlogon](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a2d0a-113">If handling an event requires interacting with Winlogon, use the [Winlogon Support Functions](authentication-functions.md).</span></span>

<span data-ttu-id="a2d0a-114">Para usar el paquete de notificación de Winlogon, el archivo DLL debe copiarse en la carpeta% SystemRoot% \\ system32 y debe realizarse una actualización del registro para el paquete de notificación.</span><span class="sxs-lookup"><span data-stu-id="a2d0a-114">To use your Winlogon notification package, the DLL must be copied to the %SystemRoot%\\system32 folder, and a registry update must be made for the notification package.</span></span> <span data-ttu-id="a2d0a-115">Para obtener información acerca de la actualización del registro, consulte [registrar un paquete de notificación de Winlogon](registering-a-winlogon-notification-package.md).</span><span class="sxs-lookup"><span data-stu-id="a2d0a-115">For information about the registry update, see [Registering a Winlogon Notification Package](registering-a-winlogon-notification-package.md).</span></span>

 

 
