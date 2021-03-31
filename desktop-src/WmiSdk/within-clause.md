---
description: Utilice la cláusula WITHIN en las consultas de eventos para especificar un intervalo de sondeo o un intervalo de agrupación.
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: Cláusula WITHIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d863e2e71d52fe60aeed7697feeb1231164c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155997"
---
# <a name="within-clause"></a><span data-ttu-id="c2ea5-103">Cláusula WITHIN</span><span class="sxs-lookup"><span data-stu-id="c2ea5-103">WITHIN Clause</span></span>

<span data-ttu-id="c2ea5-104">Los consumidores de eventos usan la cláusula WITHIN en las consultas de eventos para especificar un *intervalo de sondeo* o un *intervalo de agrupación*.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-104">Event consumers use the WITHIN clause in event queries to specify a *polling interval* or a *grouping interval*.</span></span>

<span data-ttu-id="c2ea5-105">Un intervalo de sondeo es el intervalo que Instrumental de administración de Windows (WMI) utiliza para sondear el proveedor de datos responsable de la clase para los [eventos intrínsecos](determining-the-type-of-event-to-receive.md), de los que el evento consultado es un miembro.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-105">A polling interval is the interval that Windows Management Instrumentation (WMI) uses to poll the data provider responsible for the class for [intrinsic events](determining-the-type-of-event-to-receive.md), of which the event queried is a member.</span></span> <span data-ttu-id="c2ea5-106">Este intervalo es la cantidad de tiempo máxima que puede transcurrir antes de entregarse la notificación de un evento.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-106">This interval is the maximum amount of time that can pass before notification of an event must be delivered.</span></span> <span data-ttu-id="c2ea5-107">Un consumidor utiliza un intervalo de sondeo en una cláusula WITHIN cuando el consumidor requiere la notificación de cambios en una clase y un proveedor de eventos no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-107">A consumer uses a polling interval in a WITHIN clause when the consumer requires notification of changes to a class, and an event provider is unavailable.</span></span> <span data-ttu-id="c2ea5-108">El consumidor se registra para un evento intrínseco e incluye el intervalo de sondeo.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-108">The consumer registers for an intrinsic event and includes the polling interval.</span></span>

<span data-ttu-id="c2ea5-109">Para especificar un intervalo de sondeo, coloque la cláusula WITHIN inmediatamente antes de la cláusula WHERE, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="c2ea5-109">To specify a polling interval, place the WITHIN clause immediately before the WHERE clause, as shown following:</span></span>


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



<span data-ttu-id="c2ea5-110">IntrinsicEventClass es la clase de eventos intrínseca de la que el evento es un miembro, Interval es el intervalo de sondeo y Value es el valor de la propiedad en la que el consumidor requiere la notificación.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-110">IntrinsicEventClass is the intrinsic event class of which the event is a member, interval is the polling interval, and value is the value for the property on which the consumer requires notification.</span></span>

<span data-ttu-id="c2ea5-111">El intervalo de sondeo es un número de punto flotante y puede ser fraccionario para aceptar valores inferiores a 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-111">The polling interval is a floating-point number, and can be fractional to accept values smaller than 1 second.</span></span> <span data-ttu-id="c2ea5-112">Sin embargo, el intervalo debe representar un número de segundos en lugar de un valor muy pequeño, como 0,001, porque especificar un valor demasiado pequeño puede hacer que WMI rechace la instrucción como no válido, debido a la naturaleza de un uso intensivo de recursos del sondeo.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-112">However, the interval should represent a number of seconds rather than an extremely small value such as 0.001, because specifying a value that is too small can cause WMI to reject the statement as not valid—due to the resource-intensive nature of polling.</span></span> <span data-ttu-id="c2ea5-113">Dado que la mayoría de los consumidores de eventos no requieren una notificación inmediata, se recomienda usar un intervalo que sea superior a 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-113">Because most event consumers do not require immediate notification, it is recommended that they use an interval that is greater than 5 minutes.</span></span>

<span data-ttu-id="c2ea5-114">En el ejemplo de consulta siguiente se solicita que WMI Compruebe cada 10 segundos los cambios que se producen en las instancias de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="c2ea5-114">The following query example requests that WMI check every 10 seconds for changes that occur to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="c2ea5-115">Si se modifica una instancia de la clase dentro del intervalo de sondeo especificado, se envía un evento de notificación para cada modificación.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-115">If an instance of the class is modified within the specified polling interval, a notification event is sent for each modification.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="c2ea5-116">Dependiendo de la consulta, un proveedor de eventos y WMI pueden compartir la tarea de proporcionar eventos.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-116">Depending on the query, an event provider and WMI can share the task of providing events.</span></span> <span data-ttu-id="c2ea5-117">Por ejemplo, un proveedor de eventos que admite eventos de las clases del sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) y [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) , y no eventos de la clase del sistema [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) .</span><span class="sxs-lookup"><span data-stu-id="c2ea5-117">For example, an event provider that supports events of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) and [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system classes, and not events of the [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) system class.</span></span> <span data-ttu-id="c2ea5-118">La siguiente consulta permite al proveedor de eventos generar los eventos de creación y modificación a medida que se producen y que se entregan cuando se crean.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-118">The following query enables the event provider to generate the creation and modification events as they occur and have them delivered when they are created.</span></span> <span data-ttu-id="c2ea5-119">La consulta también permite a WMI generar eventos **\_ \_ InstanceDeletionEvent** cada 10 (diez) segundos mediante el mecanismo de sondeo.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-119">The query also allows WMI to generate **\_\_InstanceDeletionEvent** events every 10 (ten) seconds using the polling mechanism.</span></span>


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



<span data-ttu-id="c2ea5-120">También puede utilizar la cláusula WITHIN para especificar un intervalo de agrupación.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-120">You can also use the WITHIN clause to specify a grouping interval.</span></span> <span data-ttu-id="c2ea5-121">Un intervalo de agrupación es un entero de 32 bits sin signo que especifica el período de tiempo, después de recibir un evento inicial, durante el cual WMI debe recopilar eventos similares.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-121">A grouping interval is an unsigned 32-bit integer that specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span> <span data-ttu-id="c2ea5-122">Cuando expira este período de tiempo, WMI entrega el evento agregado, compuesto por todos los eventos similares.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-122">When this time period expires, WMI delivers the aggregate event, made up of all the similar events.</span></span> <span data-ttu-id="c2ea5-123">Para obtener más información, vea [Group (cláusula](group-clause.md)).</span><span class="sxs-lookup"><span data-stu-id="c2ea5-123">For more information, see [GROUP Clause](group-clause.md).</span></span>

<span data-ttu-id="c2ea5-124">Los consumidores de eventos que se registran para eventos que se producen con frecuencia utilizan un intervalo de agrupación con la cláusula WITHIN.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-124">Event consumers that register for frequently occurring events use a grouping interval with the WITHIN clause.</span></span> <span data-ttu-id="c2ea5-125">Al agregar un grupo en la cláusula WHERE de una consulta de evento, WMI envía un evento agregado en lugar de muchos eventos.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-125">Adding GROUP WITHIN to the WHERE clause in an event query results in WMI sending one aggregate event rather than many events.</span></span> <span data-ttu-id="c2ea5-126">El evento Aggregate se representa mediante la clase de sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) .</span><span class="sxs-lookup"><span data-stu-id="c2ea5-126">The aggregate event is represented by the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span>

<span data-ttu-id="c2ea5-127">Para especificar un intervalo de agrupación, coloque la cláusula WITHIN inmediatamente después de la cláusula GROUP.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-127">To specify a grouping interval, place the WITHIN clause immediately after the GROUP clause.</span></span>


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



<span data-ttu-id="c2ea5-128">EventClass es la clase de eventos de la que el evento es un miembro, Value es el valor de la propiedad en la que el consumidor requiere notificación e Interval es el intervalo de agrupación.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-128">EventClass is the event class of which the event is a member, value is the value for the property on which the consumer requires notification, and Interval is the grouping interval.</span></span>

<span data-ttu-id="c2ea5-129">Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="c2ea5-129">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="c2ea5-130">Los consumidores de eventos permanentes se pueden crear con consultas de sondeo solo si tiene privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="c2ea5-130">Permanent event consumers can be created with polling queries only if you have administrator privileges.</span></span>

 

 
