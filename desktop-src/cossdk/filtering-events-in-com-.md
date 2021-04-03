---
description: 'Los eventos COM+ ofrecen dos maneras de controlar qué eventos llegan a los suscriptores: filtrado de publicador y filtrado de parámetros.'
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: Filtrado de eventos en COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807796"
---
# <a name="filtering-events-in-com"></a><span data-ttu-id="4c4c5-103">Filtrado de eventos en COM+</span><span class="sxs-lookup"><span data-stu-id="4c4c5-103">Filtering Events in COM+</span></span>

<span data-ttu-id="4c4c5-104">Los eventos COM+ ofrecen dos maneras de controlar qué eventos llegan a los suscriptores: *filtrado de publicador* y *filtrado de parámetros*.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-104">COM+ Events provides two ways to control which events reach which subscribers: *publisher filtering* and *parameter filtering*.</span></span>

## <a name="publisher-filtering"></a><span data-ttu-id="4c4c5-105">Filtrado de publicador</span><span class="sxs-lookup"><span data-stu-id="4c4c5-105">Publisher Filtering</span></span>

<span data-ttu-id="4c4c5-106">El filtrado de publicador controla el orden y la activación de un método de evento mediante un objeto de [clase de evento](the-com--event-class-object.md) .</span><span class="sxs-lookup"><span data-stu-id="4c4c5-106">Publisher filtering controls the order and firing of an event method by an [event class](the-com--event-class-object.md) object.</span></span> <span data-ttu-id="4c4c5-107">El filtrado de publicadores permite al publicador determinar qué suscriptores reciben un evento determinado.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-107">Publisher filtering allows the publisher to determine which subscribers receive a particular event.</span></span>

<span data-ttu-id="4c4c5-108">Un ejemplo de uso eficaz del filtrado de publicador es el de una bolsa de valores.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-108">An example of effective use of publisher filtering is that of a stock exchange.</span></span> <span data-ttu-id="4c4c5-109">La mayoría de los suscriptores quieren saber cuándo se agrega una nueva cotización.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-109">Most subscribers want to know when a new stock is added.</span></span> <span data-ttu-id="4c4c5-110">Sin embargo, es posible que muchos de estos suscriptores no deseen saber cada vez que cambien los precios de las acciones.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-110">However, many of these same subscribers may not want to know whenever each stock price changes.</span></span> <span data-ttu-id="4c4c5-111">El filtrado de publicador proporciona la granularidad necesaria para ofrecer eficazmente eventos a solo los suscriptores que desean esta información.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-111">Publisher filtering provides the granularity required to effectively deliver events to only the subscribers who want this information.</span></span>

<span data-ttu-id="4c4c5-112">Cuando se invoca un método en el objeto de clase de eventos con instancias, se recopilan los filtros de publicador en ese método.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-112">When a method is invoked on the instantiated event class object, it collects any publisher filters on that method.</span></span> <span data-ttu-id="4c4c5-113">El filtro fuerza el objeto de evento a desencadenar el método de evento para un suscriptor concreto.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-113">The filter forces the event object to fire the event method to a specific subscriber.</span></span> <span data-ttu-id="4c4c5-114">El filtro determina qué suscripciones se activarán y en qué orden se activarán.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-114">The filter determines which subscriptions to fire and in which order to fire them.</span></span> <span data-ttu-id="4c4c5-115">Por ejemplo, el filtro podría leer la lista de suscripciones y crear el pedido basándose en algunos criterios de aplicación y, a continuación, llamar a los suscriptores en ese orden.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-115">For example, the filter could read the subscription list and create the order based on some application criteria and then call the subscribers in that order.</span></span>

<span data-ttu-id="4c4c5-116">Para obtener instrucciones detalladas sobre cómo crear un filtro de publicador, consulte [crear un filtro de publicador](creating-a-publisher-filter.md).</span><span class="sxs-lookup"><span data-stu-id="4c4c5-116">For detailed instructions on creating a publisher filter, see [Creating a Publisher Filter](creating-a-publisher-filter.md).</span></span>

## <a name="parameter-filtering"></a><span data-ttu-id="4c4c5-117">Filtro de parámetros</span><span class="sxs-lookup"><span data-stu-id="4c4c5-117">Parameter Filtering</span></span>

<span data-ttu-id="4c4c5-118">A diferencia del filtrado de publicador, el servicio de eventos COM+ proporciona un filtrado de parámetros de suscriptor opcional para cada suscripción y cada invocación de método de evento.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-118">In contrast to publisher filtering, the COM+ Events service provides an optional subscriber parameter filtering for each subscription and each event method invocation.</span></span> <span data-ttu-id="4c4c5-119">El filtrado de parámetros evalúa la propiedad FilterCriteria de la suscripción con los parámetros del método de evento.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-119">Parameter filtering evaluates the subscription FilterCriteria property against the parameters of the event method.</span></span> <span data-ttu-id="4c4c5-120">Este tipo de filtrado se utiliza por cada método y suscripción, y proporciona un nivel de filtrado de suscriptores en el origen del evento.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-120">This type of filtering is used on a per-method, per-subscription basis and provides a level of subscriber filtering at the event source.</span></span> <span data-ttu-id="4c4c5-121">La cadena de criterios de filtro reconoce los operadores relacionales para comprobar la igualdad (=, = =,!,! =, ~, ~ =,  <>), los paréntesis anidados y las palabras clave lógicas **and**, **or** o **Not**.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-121">The filter criteria string recognizes relational operators for checking equality (=, ==, !, !=, ~, ~=, <>), nested parentheses, and logical keywords **AND**, **OR**, or **NOT**.</span></span>

<span data-ttu-id="4c4c5-122">El filtrado de parámetros se produce después de cualquier filtro de publicador y cuando se desencadena el objeto de evento estándar para una suscripción determinada.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-122">Parameter filtering occurs after any publisher filtering and when the standard event object is fired for a given subscription.</span></span> <span data-ttu-id="4c4c5-123">Si se usa el filtrado del publicador, el filtrado de parámetros solo se produce cuando el filtro del publicador invoca [**IFiringControl:: FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription).</span><span class="sxs-lookup"><span data-stu-id="4c4c5-123">If publisher filtering is used, parameter filtering occurs only when the publisher filter invokes [**IFiringControl::FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription).</span></span> <span data-ttu-id="4c4c5-124">Por este motivo, el filtrado de publicadores y el filtrado de parámetros pueden componerse juntos, pero el filtrado del publicador tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="4c4c5-124">Because of this, publisher filtering and parameter filtering can compose together but publisher filtering takes precedence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c4c5-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c4c5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c4c5-126">Publicar y entregar eventos en COM+</span><span class="sxs-lookup"><span data-stu-id="4c4c5-126">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="4c4c5-127">Suscripciones</span><span class="sxs-lookup"><span data-stu-id="4c4c5-127">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="4c4c5-128">Objeto de la clase de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="4c4c5-128">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="4c4c5-129">Usar eventos COM+ con componentes en cola de COM+</span><span class="sxs-lookup"><span data-stu-id="4c4c5-129">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



