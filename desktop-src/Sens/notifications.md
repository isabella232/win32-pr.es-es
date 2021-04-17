---
description: El servicio de notificación de eventos del sistema permite a las aplicaciones móviles recibir notificaciones de los eventos del sistema que controla SENS. Cuando se produce el evento solicitado, SENS lo notifica a la aplicación.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Notificaciones (servicio de notificación de eventos del sistema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272f0ea60369015328e34d3a83231ab0b254253a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668307"
---
# <a name="notifications-system-event-notification-service"></a><span data-ttu-id="e38cb-104">Notificaciones (servicio de notificación de eventos del sistema)</span><span class="sxs-lookup"><span data-stu-id="e38cb-104">Notifications (System Event Notification Service)</span></span>

<span data-ttu-id="e38cb-105">El servicio de notificación de eventos del sistema permite a las aplicaciones móviles recibir notificaciones de los eventos del sistema que controla SENS.</span><span class="sxs-lookup"><span data-stu-id="e38cb-105">The System Event Notification Service enables mobile-aware applications to receive notifications from system events that SENS monitors.</span></span> <span data-ttu-id="e38cb-106">Cuando se produce el evento solicitado, SENS lo notifica a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e38cb-106">When the requested event occurs, SENS notifies the application.</span></span>

<span data-ttu-id="e38cb-107">SENS puede notificar a las aplicaciones sobre tres clases de eventos del sistema:</span><span class="sxs-lookup"><span data-stu-id="e38cb-107">SENS can notify applications about three classes of system events:</span></span>

-   <span data-ttu-id="e38cb-108">Eventos de red TCP/IP, como el estado de una conexión de red TCP/IP o la calidad de la conexión.</span><span class="sxs-lookup"><span data-stu-id="e38cb-108">TCP/IP network events, such as the status of a TCP/IP network connection or the quality of the connection.</span></span>
-   <span data-ttu-id="e38cb-109">Eventos de inicio de sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="e38cb-109">User logon events.</span></span>
-   <span data-ttu-id="e38cb-110">Eventos de alimentación de batería y AC.</span><span class="sxs-lookup"><span data-stu-id="e38cb-110">Battery and AC power events.</span></span>

<span data-ttu-id="e38cb-111">Por ejemplo, una aplicación puede suscribirse a cualquiera de los siguientes eventos del sistema:</span><span class="sxs-lookup"><span data-stu-id="e38cb-111">For example, an application can subscribe to any of the following system events:</span></span>

-   <span data-ttu-id="e38cb-112">Establecimiento de conectividad de red</span><span class="sxs-lookup"><span data-stu-id="e38cb-112">Establishment of network connectivity</span></span>
-   <span data-ttu-id="e38cb-113">Notificación cuando se puede alcanzar un destino especificado dentro de los parámetros de calidad de conexión (QOC) especificados</span><span class="sxs-lookup"><span data-stu-id="e38cb-113">Notification when a specified destination can be reached within specified Quality of Connection (QOC) parameters</span></span>
-   <span data-ttu-id="e38cb-114">El equipo ha cambiado a la energía de la batería</span><span class="sxs-lookup"><span data-stu-id="e38cb-114">The computer has switched to battery power</span></span>
-   <span data-ttu-id="e38cb-115">El porcentaje de energía de la batería restante está dentro de un parámetro especificado</span><span class="sxs-lookup"><span data-stu-id="e38cb-115">The percentage of remaining battery power is within a specified parameter</span></span>
-   <span data-ttu-id="e38cb-116">Eventos programados mediante el administrador de sincronización</span><span class="sxs-lookup"><span data-stu-id="e38cb-116">Scheduled events using Synchronization Manager occur</span></span>

<span data-ttu-id="e38cb-117">**Windows Server 2008 R2 y Windows 7:** El suscriptor tiene un máximo de 3 minutos para responder a una notificación en las interfaces [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) y [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) .</span><span class="sxs-lookup"><span data-stu-id="e38cb-117">**Windows Server 2008 R2 and Windows 7:** The subscriber has a maximum of 3 minutes to respond to a notification on the [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) and [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) interfaces.</span></span> <span data-ttu-id="e38cb-118">Después de 3 minutos, SENS cancela la llamada a los suscriptores y desbloquea el subproceso de notificación.</span><span class="sxs-lookup"><span data-stu-id="e38cb-118">After 3 minutes, SENS cancels the call to subscribers and unblocks the notification thread.</span></span> <span data-ttu-id="e38cb-119">Si se requiere una operación larga para responder a la notificación, vuelva de **ISensLogon** o **ISensLogon2** lo más rápido posible y abra otro subproceso para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="e38cb-119">If a lengthy operation is required to respond to the notification, return from **ISensLogon** or **ISensLogon2** as quickly as possible and open another thread for processing.</span></span>

 

 



