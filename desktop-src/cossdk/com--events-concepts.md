---
description: Conceptos de eventos COM+
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: Conceptos de eventos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807964"
---
# <a name="com-events-concepts"></a><span data-ttu-id="be03d-103">Conceptos de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="be03d-103">COM+ Events Concepts</span></span>

<span data-ttu-id="be03d-104">El servicio de eventos COM+ es un sistema de eventos automatizado y de *acoplamiento flexible* que almacena información de eventos de distintos publicadores en el catálogo de com+.</span><span class="sxs-lookup"><span data-stu-id="be03d-104">The COM+ events service is an automated, *loosely coupled event* system that stores event information from different publishers in the COM+ catalog.</span></span> <span data-ttu-id="be03d-105">Los suscriptores pueden consultar este almacén de eventos y seleccionar los eventos sobre los que desean conocer.</span><span class="sxs-lookup"><span data-stu-id="be03d-105">Subscribers can query this event store and select the events that they want to hear about.</span></span>

> [!Note]  
> <span data-ttu-id="be03d-106">Un *evento* se identifica mediante un método en una interfaz com+, conocido como *método de evento*, y se origina en un publicador y se envía al suscriptor o suscriptores correctos mediante el servicio de eventos com+.</span><span class="sxs-lookup"><span data-stu-id="be03d-106">An *event* is identified by a method in a COM+ interface, known as an *event method*, and is originated by a publisher and dispatched to the correct subscriber or subscribers through the COM+ events service.</span></span> <span data-ttu-id="be03d-107">Los métodos de evento deben tener un nombre único y solo pueden contener parámetros de entrada (sin parámetros de salida o de entrada/salida).</span><span class="sxs-lookup"><span data-stu-id="be03d-107">Event methods must be uniquely named and can contain only input parameters (no output or input/output parameters).</span></span> <span data-ttu-id="be03d-108">El valor devuelto debe ser **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="be03d-108">The return value must be an **HRESULT**.</span></span>

 

<span data-ttu-id="be03d-109">El servicio de eventos COM+ controla la mayor parte de la semántica de eventos para el publicador y el suscriptor.</span><span class="sxs-lookup"><span data-stu-id="be03d-109">The COM+ events service handles most of the event semantics for the publisher and subscriber.</span></span> <span data-ttu-id="be03d-110">Los publicadores ofrecen para publicar tipos de eventos y los suscriptores solicitan tipos de eventos de los publicadores.</span><span class="sxs-lookup"><span data-stu-id="be03d-110">Publishers offer to publish event types, and subscribers request event types from publishers.</span></span> <span data-ttu-id="be03d-111">A diferencia de un sistema de *eventos estrechamente acoplado* , en el que los publicadores deben controlar la sobrecarga de llamar directamente a los suscriptores, el servicio de eventos com+ mantiene los datos de suscripción en el catálogo de com+, independientemente del publicador y del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="be03d-111">Unlike a *tightly coupled event* system, where publishers must handle the overhead of calling subscribers directly, the COM+ events service maintains subscription data in the COM+ catalog, independent of the publisher and subscriber.</span></span> <span data-ttu-id="be03d-112">Esto simplifica el modelo de programación para el publicador y el suscriptor porque el componente de suscriptor de COM+ no necesita contener la lógica para la creación de suscripciones.</span><span class="sxs-lookup"><span data-stu-id="be03d-112">This simplifies the programming model for the publisher and subscriber because the COM+ subscriber component does not need to contain the logic for building subscriptions.</span></span>

<span data-ttu-id="be03d-113">Dado que el ciclo de vida de los datos de suscripciones de eventos COM+ es independiente del publicador o del suscriptor, las suscripciones se pueden crear antes de que las aplicaciones del suscriptor o del publicador estén activas.</span><span class="sxs-lookup"><span data-stu-id="be03d-113">Because the life cycle of the COM+ events subscription data is separate from that of either the publisher or the subscriber, subscriptions can be built prior to either the subscriber or the publisher applications being active.</span></span> <span data-ttu-id="be03d-114">Esto también significa que los publicadores y suscriptores se pueden desarrollar e implementar por separado.</span><span class="sxs-lookup"><span data-stu-id="be03d-114">This also means that publishers and subscribers can be developed and deployed separately.</span></span> <span data-ttu-id="be03d-115">El publicador se puede escribir sin conocimiento del número y la ubicación de los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="be03d-115">The publisher can be written without knowledge of the number and location of the subscribers.</span></span> <span data-ttu-id="be03d-116">Los suscriptores usan el servicio de eventos COM+ para buscar el publicador y administrar sus suscripciones.</span><span class="sxs-lookup"><span data-stu-id="be03d-116">The subscribers use the COM+ Events service to find the publisher and manage their subscriptions.</span></span>

<span data-ttu-id="be03d-117">En los siguientes temas de esta sección se proporciona información detallada sobre los elementos básicos del servicio de eventos COM+ y cómo usarlos.</span><span class="sxs-lookup"><span data-stu-id="be03d-117">The following topics in this section provide detailed information about the core elements of the COM+ events service and how to use them.</span></span>

-   [<span data-ttu-id="be03d-118">Objeto de la clase de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="be03d-118">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
-   [<span data-ttu-id="be03d-119">Suscripciones</span><span class="sxs-lookup"><span data-stu-id="be03d-119">Subscriptions</span></span>](subscriptions.md)
-   [<span data-ttu-id="be03d-120">Publicar y entregar eventos en COM+</span><span class="sxs-lookup"><span data-stu-id="be03d-120">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
-   [<span data-ttu-id="be03d-121">Filtrado de eventos en COM+</span><span class="sxs-lookup"><span data-stu-id="be03d-121">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
-   [<span data-ttu-id="be03d-122">Usar eventos COM+ con componentes en cola de COM+</span><span class="sxs-lookup"><span data-stu-id="be03d-122">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a><span data-ttu-id="be03d-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="be03d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be03d-124">Consideraciones de seguridad de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="be03d-124">COM+ Events Security Considerations</span></span>](com--events-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="be03d-125">Tareas de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="be03d-125">COM+ Events Tasks</span></span>](com--events-tasks.md)
</dt> </dl>

 

 



