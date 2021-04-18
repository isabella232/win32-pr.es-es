---
description: Genera eventos a intervalos, similar a un \_ mensaje del temporizador de WM en la programación de Windows.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: __IntervalTimerInstruction (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __IntervalTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 20dd1c9fb2d009de4d8d957b4d5980cc6d6ff45e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707111"
---
# <a name="__intervaltimerinstruction-class"></a><span data-ttu-id="a3255-103">\_\_Clase IntervalTimerInstruction</span><span class="sxs-lookup"><span data-stu-id="a3255-103">\_\_IntervalTimerInstruction class</span></span>

<span data-ttu-id="a3255-104">La clase del sistema **\_ \_ IntervalTimerInstruction** genera eventos a intervalos, similar a un \_ mensaje del temporizador de WM en la programación de Windows.</span><span class="sxs-lookup"><span data-stu-id="a3255-104">The **\_\_IntervalTimerInstruction** system class generates events at intervals, similar to a WM\_TIMER message in Windows programming.</span></span> <span data-ttu-id="a3255-105">Un consumidor de eventos se registra en eventos de temporizador de intervalo de recepción mediante la creación de una consulta de evento que hace referencia a esta clase.</span><span class="sxs-lookup"><span data-stu-id="a3255-105">An event consumer registers to receive interval timer events by creating an event query that references this class.</span></span> <span data-ttu-id="a3255-106">Debido al comportamiento del sistema operativo, no hay ninguna garantía de que los eventos se entreguen exactamente el intervalo solicitado.</span><span class="sxs-lookup"><span data-stu-id="a3255-106">Due to operating system behavior, there are no guarantees that events will be delivered at precisely the requested interval.</span></span>

<span data-ttu-id="a3255-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a3255-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a3255-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a3255-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3255-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3255-109">Syntax</span></span>

``` syntax
class __IntervalTimerInstruction : __TimerInstruction
{
  uint32  IntervalBetweenEvents;
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="a3255-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="a3255-110">Members</span></span>

<span data-ttu-id="a3255-111">La clase **\_ \_ IntervalTimerInstruction** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a3255-111">The **\_\_IntervalTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="a3255-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a3255-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a3255-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a3255-113">Properties</span></span>

<span data-ttu-id="a3255-114">La clase **\_ \_ IntervalTimerInstruction** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a3255-114">The **\_\_IntervalTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a3255-115">**IntervalBetweenEvents**</span><span class="sxs-lookup"><span data-stu-id="a3255-115">**IntervalBetweenEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3255-116">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a3255-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a3255-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3255-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3255-118">Calificadores: [**unidades**](standard-qualifiers.md) (milisegundos)</span><span class="sxs-lookup"><span data-stu-id="a3255-118">Qualifiers: [**Units**](standard-qualifiers.md) (milliseconds)</span></span>
</dt> </dl>

<span data-ttu-id="a3255-119">Número de milisegundos entre las desencadenaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="a3255-119">Number of milliseconds between event firings.</span></span>

</dd> <dt>

<span data-ttu-id="a3255-120">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="a3255-120">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3255-121">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a3255-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a3255-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3255-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3255-123">Si es **true**, este evento se omitirá si ya se ha pasado el intervalo.</span><span class="sxs-lookup"><span data-stu-id="a3255-123">If **TRUE**, this event is to be skipped if the interval is already passed.</span></span> <span data-ttu-id="a3255-124">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="a3255-124">The default is **FALSE**.</span></span> <span data-ttu-id="a3255-125">Esta propiedad se hereda de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="a3255-125">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="a3255-126">false</span><span class="sxs-lookup"><span data-stu-id="a3255-126">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="a3255-127">Cuando WMI o el consumidor vuelva a estar disponible, se generará y recibirá un evento de notificación.</span><span class="sxs-lookup"><span data-stu-id="a3255-127">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="a3255-128">TRUE</span><span class="sxs-lookup"><span data-stu-id="a3255-128">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="a3255-129">El evento de temporizador no se produce si WMI no está disponible para generarlo en el intervalo de tiempo adecuado o el consumidor que solicita recibir el evento no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a3255-129">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a3255-130">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="a3255-130">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3255-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a3255-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3255-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3255-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3255-133">Calificadores: [ **clave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a3255-133">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a3255-134">Identificador único de este objeto **\_ \_ IntervalTimerInstruction** .</span><span class="sxs-lookup"><span data-stu-id="a3255-134">Unique identifier for this **\_\_IntervalTimerInstruction** object.</span></span> <span data-ttu-id="a3255-135">Esta propiedad se hereda de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="a3255-135">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3255-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3255-136">Remarks</span></span>

<span data-ttu-id="a3255-137">La clase **\_ \_ IntervalTimerInstruction** se deriva de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="a3255-137">The **\_\_IntervalTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="a3255-138">La consulta de eventos especificada para registrarse para un evento de temporizador de intervalo se basa normalmente en la propiedad **TimerId** .</span><span class="sxs-lookup"><span data-stu-id="a3255-138">The event query entered to register for an interval timer event is usually based on the **TimerId** property.</span></span> <span data-ttu-id="a3255-139">Los eventos de notificación generados a partir de un evento de temporizador de intervalo contienen la propiedad **NumFirings** , que contiene los datos que reflejan el número de eventos desencadenados durante el tiempo que no se pudieron recibir los eventos.</span><span class="sxs-lookup"><span data-stu-id="a3255-139">Notification events generated from an interval timer event contain the property **NumFirings** which contains data reflecting how many events fired during the time the events were unable to be received.</span></span> <span data-ttu-id="a3255-140">Si **SkipIfPassed** se establece en **true**, se descarta esa información.</span><span class="sxs-lookup"><span data-stu-id="a3255-140">If **SkipIfPassed** is set to **TRUE**, that information is discarded.</span></span>

<span data-ttu-id="a3255-141">El valor de la propiedad **IntervalBetweenEvents** debe ser razonablemente grande.</span><span class="sxs-lookup"><span data-stu-id="a3255-141">The value for the **IntervalBetweenEvents** property should be reasonably large.</span></span> <span data-ttu-id="a3255-142">Si es demasiado pequeño, WMI puede omitirlo y no generar el evento debido a las limitaciones en algunos sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="a3255-142">If it is too small, WMI may ignore it and not generate the event due to limitations in some operating systems.</span></span>

<span data-ttu-id="a3255-143">WMI genera el evento de temporizador de intervalo mediante la creación de una instancia de la clase [**\_ \_ TimerEvent**](--timerevent.md) .</span><span class="sxs-lookup"><span data-stu-id="a3255-143">WMI generates the interval timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

<span data-ttu-id="a3255-144">Para recibir estos eventos de temporizador en un consumidor de eventos temporal, ejecute [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) con la siguiente cadena de consulta de eventos:</span><span class="sxs-lookup"><span data-stu-id="a3255-144">To receive these timer events in a temporary event consumer, execute [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) with the following event query string:</span></span>


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



<span data-ttu-id="a3255-145">Para recibir estos eventos de temporizador en un consumidor de eventos permanente, debe cargar la consulta anterior en un filtro de eventos, definir un consumidor lógico y crear un enlace de filtro a consumidor para el filtro y el consumidor.</span><span class="sxs-lookup"><span data-stu-id="a3255-145">To receive these timer events in a permanent event consumer, you must load the previous query into an event filter, define a logical consumer, and create a filter-to-consumer binding for the filter and consumer.</span></span> <span data-ttu-id="a3255-146">Para obtener más información, consulte [recibir eventos en todo momento](receiving-events-at-all-times.md).</span><span class="sxs-lookup"><span data-stu-id="a3255-146">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a3255-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a3255-147">Examples</span></span>

<span data-ttu-id="a3255-148">La siguiente declaración de MOF muestra cómo generar un evento de temporizador de intervalo con la propiedad clave establecida en "DoEvents" cada 10 segundos:</span><span class="sxs-lookup"><span data-stu-id="a3255-148">The following MOF declaration shows how to generate an interval timer event with the key property set to "MyEvent" every 10 seconds:</span></span>


```mof
instance of __IntervalTimerInstruction
{
  TimerId = "MyEvent";     // inherited from __TimerInstruction
  SkipIfPassed = FALSE;    // also inherited
  IntervalBetweenEvents = 10000;
};
```



## <a name="requirements"></a><span data-ttu-id="a3255-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3255-149">Requirements</span></span>



| <span data-ttu-id="a3255-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3255-150">Requirement</span></span> | <span data-ttu-id="a3255-151">Value</span><span class="sxs-lookup"><span data-stu-id="a3255-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a3255-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3255-152">Minimum supported client</span></span><br/> | <span data-ttu-id="a3255-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3255-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a3255-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3255-154">Minimum supported server</span></span><br/> | <span data-ttu-id="a3255-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3255-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="a3255-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a3255-156">Namespace</span></span><br/>                | <span data-ttu-id="a3255-157">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="a3255-157">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a3255-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3255-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3255-159">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="a3255-159">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="a3255-160">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="a3255-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a3255-161">Recibir eventos de tiempo o repetición</span><span class="sxs-lookup"><span data-stu-id="a3255-161">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 

