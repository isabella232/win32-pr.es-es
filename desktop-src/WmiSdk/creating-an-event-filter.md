---
description: Un filtro de eventos es una clase WMI que describe qué eventos entrega WMI a un consumidor físico.
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: Crear un filtro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693e4ef2eee5de14550b8efbf25a9b6720d6a8b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717203"
---
# <a name="creating-an-event-filter"></a><span data-ttu-id="0aac8-103">Crear un filtro de eventos</span><span class="sxs-lookup"><span data-stu-id="0aac8-103">Creating an Event Filter</span></span>

<span data-ttu-id="0aac8-104">Un filtro de eventos es una clase WMI que describe qué eventos entrega WMI a un consumidor físico.</span><span class="sxs-lookup"><span data-stu-id="0aac8-104">An event filter is a WMI class that describes which events WMI delivers to a physical consumer.</span></span> <span data-ttu-id="0aac8-105">Por ejemplo, un filtro de eventos puede indicar a WMI que entregue a un consumidor todos los eventos de administración de energía o todos los eventos de reinicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="0aac8-105">For example, an event filter can instruct WMI to deliver to a consumer all power management events, or all system reboot events.</span></span> <span data-ttu-id="0aac8-106">Un filtro de eventos también describe las condiciones en las que WMI entrega los eventos.</span><span class="sxs-lookup"><span data-stu-id="0aac8-106">An event filter also describes the conditions under which WMI delivers the events.</span></span> <span data-ttu-id="0aac8-107">Un filtro de eventos puede especificar un evento intrínseco o extrínseco; y el filtro puede hacer referencia a los eventos que se originan en el espacio de nombres, es decir, que no sean el espacio de nombres del filtro.</span><span class="sxs-lookup"><span data-stu-id="0aac8-107">An event filter can specify an intrinsic or extrinsic event; and the filter can refer to events that originate in the namespace—that is, other than the namespace of the filter.</span></span> <span data-ttu-id="0aac8-108">El consumidor permanente debe tener el mismo [**CreatorSID**](--eventconsumer.md) en las instancias de consumidor, filtro y enlace.</span><span class="sxs-lookup"><span data-stu-id="0aac8-108">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="0aac8-109">Para obtener más información, consulte [recepción de eventos de forma segura](receiving-events-securely.md).</span><span class="sxs-lookup"><span data-stu-id="0aac8-109">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="0aac8-110">En el procedimiento siguiente se describe cómo crear un filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="0aac8-110">The following procedure describes how to create an event filter.</span></span>

<span data-ttu-id="0aac8-111">**Para crear un filtro de eventos**</span><span class="sxs-lookup"><span data-stu-id="0aac8-111">**To create an event filter**</span></span>

1.  <span data-ttu-id="0aac8-112">Cree una instancia de la clase del sistema [**\_ \_ EventFilter**](--eventfilter.md) de WMI.</span><span class="sxs-lookup"><span data-stu-id="0aac8-112">Create an instance of the WMI [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>
2.  <span data-ttu-id="0aac8-113">Cree un identificador único para el filtro con la propiedad **Name** , de una de estas dos maneras:</span><span class="sxs-lookup"><span data-stu-id="0aac8-113">Create a unique identifier for your filter with the **Name** property, in one of two ways:</span></span>

    -   <span data-ttu-id="0aac8-114">Use un esquema privado.</span><span class="sxs-lookup"><span data-stu-id="0aac8-114">Use a private scheme.</span></span>

        <span data-ttu-id="0aac8-115">El nombre arbitrario de los filtros de eventos funciona siempre y cuando no esté en conflicto con otros esquemas de nomenclatura de filtros.</span><span class="sxs-lookup"><span data-stu-id="0aac8-115">Arbitrarily naming your event filters works as long as you do not conflict with other filter naming schemes.</span></span> <span data-ttu-id="0aac8-116">Debe evitar conflictos de nombres porque al agregar una instancia con un valor de **nombre** duplicado se sobrescribe la instancia anterior.</span><span class="sxs-lookup"><span data-stu-id="0aac8-116">You must avoid naming conflicts because adding an instance with a duplicate **Name** value overwrites the old instance.</span></span>

    -   <span data-ttu-id="0aac8-117">Use un identificador único global (GUID).</span><span class="sxs-lookup"><span data-stu-id="0aac8-117">Use a globally unique identifier (GUID).</span></span>

        <span data-ttu-id="0aac8-118">Si deja **el nombre** vacío, WMI rellena **el nombre** con un GUID.</span><span class="sxs-lookup"><span data-stu-id="0aac8-118">If you leave **Name** empty, WMI fills **Name** with a GUID.</span></span>

3.  <span data-ttu-id="0aac8-119">Describa el tipo de evento que desea filtrar con la propiedad de **consulta** .</span><span class="sxs-lookup"><span data-stu-id="0aac8-119">Describe the type of event you want filtered with the **Query** property.</span></span>

    <span data-ttu-id="0aac8-120">La propiedad **query** contiene la consulta de lenguaje de consulta de WMI (WQL) que describe el tipo de evento que desea filtrar.</span><span class="sxs-lookup"><span data-stu-id="0aac8-120">The **Query** property contains the WMI Query Language (WQL) query that describes the type of event you want filtered.</span></span> <span data-ttu-id="0aac8-121">Puede lograr un filtrado preciso mediante una variedad de operadores y extensiones para WQL.</span><span class="sxs-lookup"><span data-stu-id="0aac8-121">You can achieve precise filtering using a variety of operators and extensions to WQL.</span></span>

    <span data-ttu-id="0aac8-122">Un evento de registro NT se genera cuando se produce un error en una consulta de un consumidor de eventos permanente.</span><span class="sxs-lookup"><span data-stu-id="0aac8-122">An NT Log event is generated when a query from a permanent event consumer fails.</span></span> <span data-ttu-id="0aac8-123">El origen del evento es WinMgmt, el ID. de evento es 10 y el tipo de evento es error.</span><span class="sxs-lookup"><span data-stu-id="0aac8-123">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

    <span data-ttu-id="0aac8-124">WMI es más eficaz en el procesamiento de consultas específicas y restrictivas que las consultas amplias.</span><span class="sxs-lookup"><span data-stu-id="0aac8-124">WMI is more efficient at processing restrictive, specific queries than broad queries.</span></span> <span data-ttu-id="0aac8-125">Mediante la creación de una consulta específica, puede evitar la comunicación entre procesos y el tráfico de red innecesarios.</span><span class="sxs-lookup"><span data-stu-id="0aac8-125">By creating a specific query, you can avoid unnecessary inter-process communication and network traffic.</span></span> <span data-ttu-id="0aac8-126">En los casos de eventos generados por un proveedor, WMI realiza el filtrado en proceso para el proveedor; Esto garantiza que solo los eventos que coinciden con el filtro incurren en el costo de comunicación entre procesos.</span><span class="sxs-lookup"><span data-stu-id="0aac8-126">In cases of events generated by a provider, WMI performs the filtering in process to the provider; this ensures that only events matching the filter incur the interprocess communication cost.</span></span> <span data-ttu-id="0aac8-127">Para obtener más información, consulte [consultar WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="0aac8-127">For more information, see [Querying WMI](querying-wmi.md).</span></span>

4.  <span data-ttu-id="0aac8-128">Establezca la propiedad **QueryLanguage** en el tipo de lenguaje de consulta que use en la propiedad **query** .</span><span class="sxs-lookup"><span data-stu-id="0aac8-128">Set the **QueryLanguage** property to the type of query language you use in the **Query** property.</span></span>

    <span data-ttu-id="0aac8-129">Casi siempre se establece **QueryLanguage** en "WQL".</span><span class="sxs-lookup"><span data-stu-id="0aac8-129">You will almost always set **QueryLanguage** to "WQL".</span></span>

<span data-ttu-id="0aac8-130">En el ejemplo de código siguiente se describe un filtro de eventos que señala a un evento cada vez que WMI crea una instancia de la clase [**\_ \_ TimerEvent**](--timerevent.md) en el \\ espacio de nombres root cimv2.</span><span class="sxs-lookup"><span data-stu-id="0aac8-130">The following code example describes an event filter that signals an event each time WMI creates an instance of the [**\_\_TimerEvent**](--timerevent.md) class in the root\\cimv2 namespace.</span></span>

``` syntax
instance of __EventFilter as $FILTER
{
    Name = "MyFilterName";
    Query = "select * from __TimerEvent where TimerID=\"MyTimer\"";
    QueryLanguage = "WQL";
    EventNamespace = "\root\cimv2";

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="0aac8-131">La propiedad **EventNamespace** especifica el espacio de nombres desde el que se originan los eventos.</span><span class="sxs-lookup"><span data-stu-id="0aac8-131">The **EventNamespace** property specifies the namespace from which the events originate.</span></span> <span data-ttu-id="0aac8-132">No es necesario crear una instancia de los filtros en el espacio de nombres en el que se originan los eventos.</span><span class="sxs-lookup"><span data-stu-id="0aac8-132">You do not have to create an instance of the filters in the namespace where the events originate.</span></span> <span data-ttu-id="0aac8-133">Si no especifica el espacio de nombres, WMI crea el filtro en el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0aac8-133">If you do not specify the namespace, then WMI creates the filter in the default namespace.</span></span> <span data-ttu-id="0aac8-134">Las clases de eventos intrínsecos, como [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , están disponibles en todos los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="0aac8-134">The intrinsic events classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

<span data-ttu-id="0aac8-135">Para registrar el consumidor lógico para las notificaciones de eventos, debe enlazar los filtros de eventos a un consumidor lógico.</span><span class="sxs-lookup"><span data-stu-id="0aac8-135">To register your logical consumer for event notifications, you must bind the event filters to a logical consumer.</span></span> <span data-ttu-id="0aac8-136">Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="0aac8-136">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

 

 



