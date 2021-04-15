---
title: Usar el recopilador de eventos de Windows
description: En esta sección se enumeran los temas en los que se explican las tareas que se pueden realizar con el SDK del recopilador de eventos de Windows. En cada uno de los temas siguientes se incluyen ejemplos de código y explicaciones para todas las tareas.
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc618ced4cefc7f17fb63b27bb1e097e65b3adac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695298"
---
# <a name="using-windows-event-collector"></a><span data-ttu-id="18b25-104">Usar el recopilador de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="18b25-104">Using Windows Event Collector</span></span>

<span data-ttu-id="18b25-105">En esta sección se enumeran los temas en los que se explican las tareas que se pueden realizar con el SDK del recopilador de eventos de Windows.</span><span class="sxs-lookup"><span data-stu-id="18b25-105">This section lists the topics that explain the tasks that can be accomplished using the Windows Event Collector SDK.</span></span> <span data-ttu-id="18b25-106">En cada uno de los temas siguientes se incluyen ejemplos de código y explicaciones para todas las tareas.</span><span class="sxs-lookup"><span data-stu-id="18b25-106">Code examples and explanations for all the tasks are included in each of the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="18b25-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="18b25-107">In This Section</span></span>

-   [<span data-ttu-id="18b25-108">Creación de una suscripción iniciada por el recopilador</span><span class="sxs-lookup"><span data-stu-id="18b25-108">Creating a Collector Initiated Subscription</span></span>](creating-an-event-collector-subscription.md)

    <span data-ttu-id="18b25-109">Proporciona información y un ejemplo de código de C++ para crear una suscripción iniciada por el recopilador.</span><span class="sxs-lookup"><span data-stu-id="18b25-109">Provides information and a C++ code example for creating a collector-initiated subscription.</span></span> <span data-ttu-id="18b25-110">Una suscripción iniciada por el recopilador permite recibir eventos en un equipo local (el recopilador de eventos) que se reenvían desde un equipo remoto (un origen de eventos).</span><span class="sxs-lookup"><span data-stu-id="18b25-110">A collector-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source).</span></span>

-   [<span data-ttu-id="18b25-111">Configuración de una suscripción iniciada por el origen</span><span class="sxs-lookup"><span data-stu-id="18b25-111">Setting up a Source Initiated Subscription</span></span>](setting-up-a-source-initiated-subscription.md)

    <span data-ttu-id="18b25-112">Proporciona información y un ejemplo de código de C++ para crear una suscripción iniciada por el origen.</span><span class="sxs-lookup"><span data-stu-id="18b25-112">Provides information and a C++ code example for creating a source-initiated subscription.</span></span> <span data-ttu-id="18b25-113">Una suscripción iniciada por el origen le permite recibir eventos en un equipo local (el recopilador de eventos) que se reenvían desde un equipo remoto (un origen de eventos) sin especificar los orígenes de eventos de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="18b25-113">A source-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source) without specifying the event sources in the subscription.</span></span>

-   [<span data-ttu-id="18b25-114">Agregar un origen de eventos a una suscripción iniciada por el recopilador</span><span class="sxs-lookup"><span data-stu-id="18b25-114">Adding an Event Source to a Collector Initiated Subscription</span></span>](adding-an-event-source-to-an-event-collector-subscription.md)

    <span data-ttu-id="18b25-115">Proporciona información y un ejemplo de código de C++ para agregar un origen de eventos (equipo local o equipo remoto) a una suscripción iniciada por el recopilador.</span><span class="sxs-lookup"><span data-stu-id="18b25-115">Provides information and a C++ code example for adding an event source (local computer or remote computer) to a collector-initiated subscription.</span></span> <span data-ttu-id="18b25-116">Una suscripción iniciada por el recopilador no puede iniciar la recopilación de eventos hasta que se agrega un origen de eventos a la suscripción.</span><span class="sxs-lookup"><span data-stu-id="18b25-116">A collector initiated subscription cannot start collecting events until an event source is added to the subscription.</span></span>

-   [<span data-ttu-id="18b25-117">Creación de suscripciones de eventos de hardware</span><span class="sxs-lookup"><span data-stu-id="18b25-117">Creating Hardware Event Subscriptions</span></span>](creating-hardware-event-subscriptions.md)

    <span data-ttu-id="18b25-118">Proporciona información acerca de cómo crear una suscripción de eventos para recibir eventos de hardware de un equipo que tiene instalado un controlador de administración de placa base (BMC).</span><span class="sxs-lookup"><span data-stu-id="18b25-118">Provides information about how to create an event subscription in order to receive hardware events from a computer that has a Baseboard Management Controller (BMC) installed.</span></span>

-   [<span data-ttu-id="18b25-119">Eliminar una suscripción del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="18b25-119">Deleting an Event Collector Subscription</span></span>](deleting-an-event-collector-subscription.md)

    <span data-ttu-id="18b25-120">Proporciona información y un ejemplo de código de C++ para eliminar una suscripción del recopilador de eventos de un equipo local.</span><span class="sxs-lookup"><span data-stu-id="18b25-120">Provides information and a C++ code example for deleting an Event Collector subscription from a local computer.</span></span>

-   [<span data-ttu-id="18b25-121">Mostrar las propiedades de una suscripción del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="18b25-121">Displaying the Properties of an Event Collector Subscription</span></span>](displaying-the-properties-of-an-event-collector-subscription.md)

    <span data-ttu-id="18b25-122">Proporciona información y un ejemplo de código de C++ para mostrar los valores de propiedad de una suscripción del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="18b25-122">Provides information and a C++ code example for displaying the property values of an Event Collector subscription.</span></span> <span data-ttu-id="18b25-123">Los valores de propiedad pueden proporcionar información útil, como las direcciones de los orígenes de eventos, el estado de la suscripción y los orígenes de eventos, e información sobre cómo se entregan los eventos.</span><span class="sxs-lookup"><span data-stu-id="18b25-123">Property values can provide useful information, such as the addresses of event sources, the status of the subscription and event sources, and information about how events are delivered.</span></span>

-   [<span data-ttu-id="18b25-124">Mostrar el estado de una suscripción del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="18b25-124">Displaying the Status of an Event Collector Subscription</span></span>](displaying-the-status-of-an-event-collector-subscription.md)

    <span data-ttu-id="18b25-125">Proporciona información y un ejemplo de código de C++ para mostrar el estado de tiempo de ejecución de los orígenes de eventos que están asociados a una suscripción del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="18b25-125">Provides information and a C++ code example for displaying the run time status of events sources that are associated to an Event Collector subscription.</span></span> <span data-ttu-id="18b25-126">Esto le permite ver los mensajes de error que pueden ayudar a resolver problemas, lo que impide que un origen de eventos reenvíe eventos.</span><span class="sxs-lookup"><span data-stu-id="18b25-126">This enables you to view error messages that can help solve problems, which prevent an event source from forwarding events.</span></span>

-   [<span data-ttu-id="18b25-127">Enumerar las suscripciones del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="18b25-127">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)

    <span data-ttu-id="18b25-128">Proporciona información y un ejemplo de código de C++ para enumerar las suscripciones que existen en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="18b25-128">Provides information and a C++ code example for listing the subscriptions that exist on a local computer.</span></span> <span data-ttu-id="18b25-129">Puede usar los nombres de suscripción que se obtienen con este ejemplo para eliminar una suscripción, agregar un origen de eventos a una suscripción, recuperar las propiedades de una suscripción o ver el estado de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="18b25-129">You can use the subscription names that are obtained with this example to delete a subscription, add an event source to a subscription, retrieve the properties of a subscription, or view the status of a subscription.</span></span>

-   [<span data-ttu-id="18b25-130">Quitar un origen de eventos de una suscripción iniciada por el recopilador</span><span class="sxs-lookup"><span data-stu-id="18b25-130">Removing an Event Source from a Collector Initiated Subscription</span></span>](removing-an-event-source-from-an-event-collector-subscription.md)

    <span data-ttu-id="18b25-131">Proporciona información y un ejemplo de código de C++ para quitar un origen de eventos de una suscripción iniciada por el recopilador.</span><span class="sxs-lookup"><span data-stu-id="18b25-131">Provides information and a C++ code example for removing an event source from a collector-initiated subscription.</span></span> <span data-ttu-id="18b25-132">Puede quitar un origen de eventos de una suscripción iniciada por el recopilador sin deshabilitar la suscripción.</span><span class="sxs-lookup"><span data-stu-id="18b25-132">You can remove an event source from a collector-initiated subscription without disabling the subscription.</span></span>

-   [<span data-ttu-id="18b25-133">Volver a intentar una suscripción del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="18b25-133">Retrying an Event Collector Subscription</span></span>](retrying-an-event-collector-subscription.md)

    <span data-ttu-id="18b25-134">Proporciona información y un ejemplo de código de C++ para volver a intentar una suscripción del recopilador de eventos cuando se han producido errores en uno o varios orígenes de eventos.</span><span class="sxs-lookup"><span data-stu-id="18b25-134">Provides information and a C++ code example for retrying an Event Collector subscription when one or more event sources have failed.</span></span> <span data-ttu-id="18b25-135">Puede reintentar un solo origen de eventos o puede reintentar toda la suscripción.</span><span class="sxs-lookup"><span data-stu-id="18b25-135">You can retry a single event source or you can retry the entire subscription.</span></span>

 

 




