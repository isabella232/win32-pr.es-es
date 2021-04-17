---
description: El servicio de notificación de eventos del sistema funciona con el sistema de eventos COM+.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Arquitectura de SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32976a716ab0ba5651ce6605fe524d639820696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668306"
---
# <a name="sens-architecture"></a><span data-ttu-id="41645-103">Arquitectura de SENS</span><span class="sxs-lookup"><span data-stu-id="41645-103">SENS Architecture</span></span>

<span data-ttu-id="41645-104">El servicio de notificación de eventos del sistema funciona con el sistema de eventos COM+.</span><span class="sxs-lookup"><span data-stu-id="41645-104">The System Event Notification Service works with the COM+ Event System.</span></span> <span data-ttu-id="41645-105">SENS es un publicador de eventos para las clases de eventos que supervisa: eventos de red, Inicio de sesión y energía/batería.</span><span class="sxs-lookup"><span data-stu-id="41645-105">SENS is an event publisher for the classes of events that it monitors: network, logon, and power/battery events.</span></span> <span data-ttu-id="41645-106">La aplicación que recibe una notificación se denomina suscriptor de eventos.</span><span class="sxs-lookup"><span data-stu-id="41645-106">The application receiving a notification is called an event subscriber.</span></span>

<span data-ttu-id="41645-107">Cuando una aplicación se suscribe para recibir notificaciones, también puede especificar filtros asociados a los eventos suscritos.</span><span class="sxs-lookup"><span data-stu-id="41645-107">When an application subscribes to receive notifications, it can also specify filters associated with the subscribed events.</span></span> <span data-ttu-id="41645-108">SENS y los eventos COM+ usan los filtros para determinar más cuando se debe notificar a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41645-108">SENS and COM+ Events use the filters to further determine when the application should be notified.</span></span>

<span data-ttu-id="41645-109">Las notificaciones son asincrónicas, por lo que no es necesario que la aplicación que recibe la notificación esté activa cuando se envía la notificación.</span><span class="sxs-lookup"><span data-stu-id="41645-109">Notifications are asynchronous, so the application receiving the notification does not have to be active when the notification is sent.</span></span> <span data-ttu-id="41645-110">Cuando una aplicación se suscribe para recibir notificaciones, puede especificar si se debe activar cuando se produce el evento o cuando se le notifica posteriormente cuando está activo.</span><span class="sxs-lookup"><span data-stu-id="41645-110">When an application subscribes to receive notifications, it can specify whether it should be activated when the event occurs or notified later when it is active.</span></span>

<span data-ttu-id="41645-111">La suscripción solo puede ser transitoria y válida hasta que la aplicación deje de ejecutarse, o bien puede ser persistente y válida hasta que la aplicación se quite del sistema.</span><span class="sxs-lookup"><span data-stu-id="41645-111">The subscription can be transient and valid only until the application stops running, or it can be persistent and valid until the application is removed from the system.</span></span>

<span data-ttu-id="41645-112">Un almacén de datos de eventos COM+ contiene información sobre el publicador de eventos (SENS), los suscriptores de eventos y los filtros.</span><span class="sxs-lookup"><span data-stu-id="41645-112">A COM+ Events data store contains information about the event publisher (SENS), event subscribers, and filters.</span></span> <span data-ttu-id="41645-113">SENS también Predefine una interfaz de salida para cada clase de evento en una biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="41645-113">SENS also predefines an outgoing interface for each event class in a type library.</span></span>



| <span data-ttu-id="41645-114">Clase de evento</span><span class="sxs-lookup"><span data-stu-id="41645-114">Event class</span></span>    | <span data-ttu-id="41645-115">GUID</span><span class="sxs-lookup"><span data-stu-id="41645-115">GUID</span></span>                          | <span data-ttu-id="41645-116">Interfaz</span><span class="sxs-lookup"><span data-stu-id="41645-116">Interface</span></span>    |
|----------------|-------------------------------|--------------|
| <span data-ttu-id="41645-117">Eventos de red</span><span class="sxs-lookup"><span data-stu-id="41645-117">Network events</span></span> | <span data-ttu-id="41645-118">red de SENSGUID \_ EVENTCLASS \_</span><span class="sxs-lookup"><span data-stu-id="41645-118">SENSGUID\_EVENTCLASS\_NETWORK</span></span> | <span data-ttu-id="41645-119">ISensNetwork</span><span class="sxs-lookup"><span data-stu-id="41645-119">ISensNetwork</span></span> |
| <span data-ttu-id="41645-120">Eventos de inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="41645-120">Logon events</span></span>   | <span data-ttu-id="41645-121">Inicio de sesión de SENSGUID \_ EVENTCLASS \_</span><span class="sxs-lookup"><span data-stu-id="41645-121">SENSGUID\_EVENTCLASS\_LOGON</span></span>   | <span data-ttu-id="41645-122">ISensLogon</span><span class="sxs-lookup"><span data-stu-id="41645-122">ISensLogon</span></span>   |
| <span data-ttu-id="41645-123">Eventos de energía</span><span class="sxs-lookup"><span data-stu-id="41645-123">Power events</span></span>   | <span data-ttu-id="41645-124">SENSGUID \_ EVENTCLASS \_ ONNOW</span><span class="sxs-lookup"><span data-stu-id="41645-124">SENSGUID\_EVENTCLASS\_ONNOW</span></span>   | <span data-ttu-id="41645-125">ISensOnNow</span><span class="sxs-lookup"><span data-stu-id="41645-125">ISensOnNow</span></span>   |



 

<span data-ttu-id="41645-126">Para recibir notificaciones de cualquiera de estos eventos, la aplicación debe hacer dos cosas:</span><span class="sxs-lookup"><span data-stu-id="41645-126">To receive notifications for any of these events, your application must do two things:</span></span>

-   <span data-ttu-id="41645-127">Suscríbase a los eventos de SENS que le interesen.</span><span class="sxs-lookup"><span data-stu-id="41645-127">Subscribe to the SENS events that interest you.</span></span> <span data-ttu-id="41645-128">Para suscribirse a un evento, use las interfaces **IEventSubscription** y **IEVENTSYSTEM** en eventos com+.</span><span class="sxs-lookup"><span data-stu-id="41645-128">To subscribe to an event, use the **IEventSubscription** and **IEventSystem** interfaces in COM+ Events.</span></span> <span data-ttu-id="41645-129">Debe proporcionar un identificador para las clases de eventos y el identificador del publicador SENS, SENSGUID \_ Publisher.</span><span class="sxs-lookup"><span data-stu-id="41645-129">You need to supply an identifier for the event classes and the SENS publisher identifier, SENSGUID\_PUBLISHER.</span></span> <span data-ttu-id="41645-130">Las suscripciones se encuentran en un nivel de evento, por lo que la aplicación de suscripción también debe especificar qué eventos de la clase son de interés.</span><span class="sxs-lookup"><span data-stu-id="41645-130">Subscriptions are on a per event level so the subscribing application must also specify which events within the class are of interest.</span></span> <span data-ttu-id="41645-131">Cada evento corresponde a un método de la interfaz correspondiente a su clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="41645-131">Each event corresponds to a method in the interface corresponding to its event class.</span></span>
-   <span data-ttu-id="41645-132">Cree un objeto de receptor con una implementación para cada interfaz que controla.</span><span class="sxs-lookup"><span data-stu-id="41645-132">Create a sink object with an implementation for each interface that you handle.</span></span> <span data-ttu-id="41645-133">Vea [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)y [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) para obtener más información acerca de estas interfaces y los eventos que se admiten en cada una de ellas.</span><span class="sxs-lookup"><span data-stu-id="41645-133">See [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon), and [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) for more information about these interfaces and the events supported in each one.</span></span>

<span data-ttu-id="41645-134">Cuando se produce uno de los eventos supervisados, SENS procesa cada suscripción con cualquier filtro asociado y notifica a los suscriptores a través del sistema de eventos COM+.</span><span class="sxs-lookup"><span data-stu-id="41645-134">When one of the monitored events occurs, SENS processes each subscription with any associated filters and notifies the subscribers through the COM+ Event system.</span></span>

 

 



