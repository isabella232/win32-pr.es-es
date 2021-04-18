---
description: Hace que se genere un evento en una fecha específica en un momento determinado.
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: __AbsoluteTimerInstruction (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AbsoluteTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f4f55e635e42ec34e9b3558a0784d319e4d91ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697893"
---
# <a name="__absolutetimerinstruction-class"></a><span data-ttu-id="01453-103">\_\_Clase AbsoluteTimerInstruction</span><span class="sxs-lookup"><span data-stu-id="01453-103">\_\_AbsoluteTimerInstruction class</span></span>

<span data-ttu-id="01453-104">La clase del sistema **\_ \_ AbsoluteTimerInstruction** hace que se genere un evento en una fecha específica en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="01453-104">The **\_\_AbsoluteTimerInstruction** system class causes an event to be generated on a specific date at a specific time.</span></span> <span data-ttu-id="01453-105">Un consumidor de eventos se registra para recibir un evento de temporizador absoluto mediante la creación de una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="01453-105">An event consumer registers to receive an absolute timer event by creating an instance of this class.</span></span> <span data-ttu-id="01453-106">El evento se genera una vez.</span><span class="sxs-lookup"><span data-stu-id="01453-106">The event is generated one time.</span></span>

<span data-ttu-id="01453-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="01453-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="01453-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="01453-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01453-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01453-109">Syntax</span></span>

``` syntax
class __AbsoluteTimerInstruction : __TimerInstruction
{
  datetime EventDateTime;
  boolean  SkipIfPassed = FALSE;
  string   TimerId;
};
```

## <a name="members"></a><span data-ttu-id="01453-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="01453-110">Members</span></span>

<span data-ttu-id="01453-111">La clase **\_ \_ AbsoluteTimerInstruction** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="01453-111">The **\_\_AbsoluteTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="01453-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01453-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01453-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01453-113">Properties</span></span>

<span data-ttu-id="01453-114">La clase **\_ \_ AbsoluteTimerInstruction** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="01453-114">The **\_\_AbsoluteTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01453-115">**EventDateTime**</span><span class="sxs-lookup"><span data-stu-id="01453-115">**EventDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01453-116">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="01453-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="01453-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="01453-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="01453-118">Cadena de longitud fija en [formato DMTF](date-and-time-format.md) que especifica cuándo se activa el temporizador.</span><span class="sxs-lookup"><span data-stu-id="01453-118">Fixed-length string in [DMTF format](date-and-time-format.md) that specifies when the timer fires.</span></span>

</dd> <dt>

<span data-ttu-id="01453-119">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="01453-119">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01453-120">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="01453-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01453-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01453-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01453-122">Si **es true**, el evento de temporizador se produce si WMI no puede generarlo en el intervalo de tiempo correcto o el consumidor que solicita recibir el evento no está disponible.</span><span class="sxs-lookup"><span data-stu-id="01453-122">If **TRUE**, the timer event occurs if WMI cannot generate it at the correct time interval, or the consumer requesting to receive the event is unavailable.</span></span> <span data-ttu-id="01453-123">Si **es true**, el evento no se producirá.</span><span class="sxs-lookup"><span data-stu-id="01453-123">If **TRUE**, the event will not occur.</span></span> <span data-ttu-id="01453-124">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="01453-124">The default is **FALSE**.</span></span> <span data-ttu-id="01453-125">Cuando WMI o el consumidor estén disponibles, se generará y recibirá un evento de notificación.</span><span class="sxs-lookup"><span data-stu-id="01453-125">When WMI or the consumer becomes available, a notification event is generated and received.</span></span> <span data-ttu-id="01453-126">Esta propiedad se hereda de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="01453-126">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="01453-127">false</span><span class="sxs-lookup"><span data-stu-id="01453-127">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="01453-128">Cuando WMI o el consumidor vuelva a estar disponible, se generará y recibirá un evento de notificación.</span><span class="sxs-lookup"><span data-stu-id="01453-128">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="01453-129">TRUE</span><span class="sxs-lookup"><span data-stu-id="01453-129">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="01453-130">El evento de temporizador no se produce si WMI no está disponible para generarlo en el intervalo de tiempo adecuado o el consumidor que solicita recibir el evento no está disponible.</span><span class="sxs-lookup"><span data-stu-id="01453-130">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="01453-131">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="01453-131">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01453-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01453-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01453-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01453-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01453-134">Calificadores: [ **clave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="01453-134">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="01453-135">Cadena única asignada por el usuario que identifica un evento de temporizador específico.</span><span class="sxs-lookup"><span data-stu-id="01453-135">Unique user-assigned string that identifies a specific timer event.</span></span> <span data-ttu-id="01453-136">Para evitar conflictos de nombres con otros identificadores de temporizador, se puede usar la forma de cadena de un GUID de estilo de entorno de equipo distribuido.</span><span class="sxs-lookup"><span data-stu-id="01453-136">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment style GUID can be used.</span></span> <span data-ttu-id="01453-137">Esta propiedad se hereda de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="01453-137">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01453-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01453-138">Remarks</span></span>

<span data-ttu-id="01453-139">La clase **\_ \_ AbsoluteTimerInstruction** se deriva de [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="01453-139">The **\_\_AbsoluteTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="01453-140">WMI genera el evento de temporizador absoluto mediante la creación de una instancia de la clase [**\_ \_ TimerEvent**](--timerevent.md) .</span><span class="sxs-lookup"><span data-stu-id="01453-140">WMI generates the absolute timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="01453-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01453-141">Requirements</span></span>



| <span data-ttu-id="01453-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="01453-142">Requirement</span></span> | <span data-ttu-id="01453-143">Value</span><span class="sxs-lookup"><span data-stu-id="01453-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="01453-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01453-144">Minimum supported client</span></span><br/> | <span data-ttu-id="01453-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01453-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="01453-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01453-146">Minimum supported server</span></span><br/> | <span data-ttu-id="01453-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01453-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="01453-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="01453-148">Namespace</span></span><br/>                | <span data-ttu-id="01453-149">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="01453-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="01453-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="01453-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01453-151">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="01453-151">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="01453-152">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="01453-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="01453-153">Recibir eventos de tiempo o repetición</span><span class="sxs-lookup"><span data-stu-id="01453-153">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[<span data-ttu-id="01453-154">Recepción de eventos en todo momento</span><span class="sxs-lookup"><span data-stu-id="01453-154">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="01453-155">Recepción de eventos mientras dure la aplicación</span><span class="sxs-lookup"><span data-stu-id="01453-155">Receiving Events for the Duration of Your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

