---
description: Después de crear el consumidor de eventos lógicos y el filtro de eventos, debe vincularlos, lo que registra el consumidor lógico para recibir notificaciones sobre los eventos especificados por el filtro.
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: Enlazar un filtro de eventos con un consumidor lógico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912406"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a><span data-ttu-id="f6303-103">Enlazar un filtro de eventos con un consumidor lógico</span><span class="sxs-lookup"><span data-stu-id="f6303-103">Binding an Event Filter with a Logical Consumer</span></span>

<span data-ttu-id="f6303-104">Después de crear el consumidor de eventos lógicos y el filtro de eventos, debe vincularlos, lo que registra el consumidor lógico para recibir notificaciones sobre los eventos especificados por el filtro.</span><span class="sxs-lookup"><span data-stu-id="f6303-104">After you create the logical event consumer and the event filter you must link them, which registers the logical consumer to receive notification about the events specified by the filter.</span></span>

<span data-ttu-id="f6303-105">En el procedimiento siguiente se describe cómo enlazar un filtro de eventos con un consumidor lógico.</span><span class="sxs-lookup"><span data-stu-id="f6303-105">The following procedure describes how to bind an event filter with a logical consumer.</span></span>

<span data-ttu-id="f6303-106">**Para enlazar un filtro de eventos con un consumidor lógico**</span><span class="sxs-lookup"><span data-stu-id="f6303-106">**To bind an event filter with a logical consumer**</span></span>

1.  <span data-ttu-id="f6303-107">Cree una instancia de la clase del sistema [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="f6303-107">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) system class in the WMI repository.</span></span>

    <span data-ttu-id="f6303-108">La clase [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) es una clase de asociación que vincula la instancia de filtro de eventos y la instancia de consumidor lógico a la vez a través de las propiedades de **filtro** y referencia de **consumidor** .</span><span class="sxs-lookup"><span data-stu-id="f6303-108">The [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class is an association class that links the event filter instance and the logical consumer instance together through the **Filter** and **Consumer** reference properties.</span></span> <span data-ttu-id="f6303-109">Para obtener más información, vea [declarar una clase de asociación](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="f6303-109">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

2.  <span data-ttu-id="f6303-110">Establezca la propiedad **filtro** en la instancia del filtro.</span><span class="sxs-lookup"><span data-stu-id="f6303-110">Set the **Filter** property to the instance of your filter.</span></span>
3.  <span data-ttu-id="f6303-111">Establezca la propiedad **Consumer** en la instancia del consumidor lógico.</span><span class="sxs-lookup"><span data-stu-id="f6303-111">Set the **Consumer** property to the instance of your logical consumer.</span></span>
4.  <span data-ttu-id="f6303-112">Establezca la propiedad **DeliverSynchronously** para determinar el tipo de entrega que desea.</span><span class="sxs-lookup"><span data-stu-id="f6303-112">Set the **DeliverSynchronously** property to determine the type of delivery you want.</span></span>

    <span data-ttu-id="f6303-113">La propiedad **DeliverSynchronously** determina cuándo WMI envía notificaciones de eventos de forma sincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f6303-113">The **DeliverSynchronously** property determines when WMI delivers event notifications synchronously or asynchronously.</span></span> <span data-ttu-id="f6303-114">Al establecer esta propiedad en **true** , se solicita una entrega sincrónica.</span><span class="sxs-lookup"><span data-stu-id="f6303-114">Setting this property to **TRUE** requests a synchronous delivery.</span></span> <span data-ttu-id="f6303-115">Use la entrega sincrónica solo cuando el consumidor permanente pueda procesar eventos en unos 100 microsegundos aproximadamente.</span><span class="sxs-lookup"><span data-stu-id="f6303-115">Use synchronous delivery only when the permanent consumer can process events within approximately 100 microseconds.</span></span>

    > [!Note]  
    > <span data-ttu-id="f6303-116">Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f6303-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="f6303-117">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f6303-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

     

5.  <span data-ttu-id="f6303-118">Al anular el registro del consumidor de eventos lógicos, asegúrese de eliminar la instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="f6303-118">When unregistering your logical event consumer, ensure you delete the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance.</span></span>

    <span data-ttu-id="f6303-119">Cada instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) representa un registro para una notificación de eventos específica.</span><span class="sxs-lookup"><span data-stu-id="f6303-119">Each [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance represents a registration for a specific event notification.</span></span> <span data-ttu-id="f6303-120">Cuando se elimina un enlace, WMI desactiva el registro.</span><span class="sxs-lookup"><span data-stu-id="f6303-120">When you delete a binding, WMI deactivates the registration.</span></span> <span data-ttu-id="f6303-121">Es posible que tenga que eliminar las instancias del consumidor lógico y del filtro de eventos para desactivar el registro, en función de la implementación.</span><span class="sxs-lookup"><span data-stu-id="f6303-121">You might have to delete the logical consumer and event filter instances to deactivate registration, depending on the implementation.</span></span>

<span data-ttu-id="f6303-122">En el ejemplo de código siguiente se muestra una instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) que asocia una instancia de una clase [**ActiveScriptEventConsumer**](activescripteventconsumer.md) con un filtro de eventos específico (la instancia del consumidor de eventos se creó en el tema [crear un consumidor lógico](creating-a-logical-consumer.md) y el filtro de eventos se creó en el tema [crear un filtro de eventos](creating-an-event-filter.md) ).</span><span class="sxs-lookup"><span data-stu-id="f6303-122">The following code example shows you a [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance that associates an instance of an [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class with a specific event filter (the instance of the event consumer was created in the [Creating a Logical Consumer](creating-a-logical-consumer.md) topic, and the event filter was created in the [Creating an Event Filter](creating-an-event-filter.md) topic).</span></span>

``` syntax
instance of __FilterToConsumerBinding
{
    Filter = $FILTER;
    Consumer = $CONSUMER;
    DeliverSynchronously=FALSE;

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="f6303-123">Dos consumidores, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) y [**CommandLineEventConsumer**](commandlineeventconsumer.md), no funcionarán a menos que su creador sea miembro del grupo de administradores local.</span><span class="sxs-lookup"><span data-stu-id="f6303-123">Two consumers, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) and [**CommandLineEventConsumer**](commandlineeventconsumer.md), will not work unless their creator is a member of the local Administrators group.</span></span>

<span data-ttu-id="f6303-124">**:** Cuando un administrador crea una suscripción, su SID no se utiliza para la propiedad **CreatorSID** , pero en su lugar se usa el SID del grupo de administradores locales.</span><span class="sxs-lookup"><span data-stu-id="f6303-124">**:** When an administrator creates a subscription, his SID is not used for the **CreatorSID** property, but the SID of the local Administrators group is used instead.</span></span> <span data-ttu-id="f6303-125">Por lo tanto, los administradores pueden crear las instancias y la suscripción seguirá funcionando.</span><span class="sxs-lookup"><span data-stu-id="f6303-125">Therefore, instances can be created by different administrators and the subscription will still work.</span></span> <span data-ttu-id="f6303-126">Para obtener más información, consulte [recepción de eventos de forma segura](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="f6303-126">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="f6303-127">Cuando un filtro se enlaza a un consumidor lógico, el evento se registra mediante el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) para Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="f6303-127">When a filter is bound to a logical consumer the event is recorded by [Event Tracing](/windows/desktop/ETW/event-tracing-portal) for Windows (ETW).</span></span> <span data-ttu-id="f6303-128">Para obtener más información, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="f6303-128">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6303-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6303-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6303-130">Recepción de eventos en todo momento</span><span class="sxs-lookup"><span data-stu-id="f6303-130">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 
