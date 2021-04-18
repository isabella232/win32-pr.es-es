---
description: Especifica instrucciones sobre cómo se deben generar los eventos de temporizador para los consumidores.
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: __TimerInstruction (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerInstruction
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6bbbf905a141fb7e9e3621c78709fd78999393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361618"
---
# <a name="__timerinstruction-class"></a><span data-ttu-id="b0856-103">\_\_Clase TimerInstruction</span><span class="sxs-lookup"><span data-stu-id="b0856-103">\_\_TimerInstruction class</span></span>

<span data-ttu-id="b0856-104">La clase **\_ \_ TimerInstruction** Abstract System especifica instrucciones sobre cómo se deben generar [los eventos de temporizador para los](receiving-a-timed-or-repeating-event.md) consumidores.</span><span class="sxs-lookup"><span data-stu-id="b0856-104">The **\_\_TimerInstruction** abstract system class specifies instructions on how [timer events](receiving-a-timed-or-repeating-event.md) should be generated for consumers.</span></span>

<span data-ttu-id="b0856-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b0856-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b0856-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b0856-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0856-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0856-107">Syntax</span></span>

``` syntax
[abstract]
class __TimerInstruction : __EventGenerator
{
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="b0856-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b0856-108">Members</span></span>

<span data-ttu-id="b0856-109">La clase **\_ \_ TimerInstruction** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b0856-109">The **\_\_TimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="b0856-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b0856-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0856-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b0856-111">Properties</span></span>

<span data-ttu-id="b0856-112">La clase **\_ \_ TimerInstruction** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b0856-112">The **\_\_TimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0856-113">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="b0856-113">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0856-114">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b0856-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0856-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b0856-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0856-116">Describe si se generará un evento de notificación y se recibirá cuando un consumidor esté disponible.</span><span class="sxs-lookup"><span data-stu-id="b0856-116">Describes whether a notification event will be generated and receive when a consumer becomes available.</span></span>

<dt>

<span data-ttu-id="b0856-117">false</span><span class="sxs-lookup"><span data-stu-id="b0856-117">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="b0856-118">Cuando WMI o el consumidor vuelva a estar disponible, se generará y recibirá un evento de notificación.</span><span class="sxs-lookup"><span data-stu-id="b0856-118">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="b0856-119">TRUE</span><span class="sxs-lookup"><span data-stu-id="b0856-119">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="b0856-120">El evento de temporizador no se produce si WMI no está disponible para generarlo en el intervalo de tiempo adecuado o el consumidor que solicita recibir el evento no está disponible.</span><span class="sxs-lookup"><span data-stu-id="b0856-120">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b0856-121">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="b0856-121">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0856-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b0856-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0856-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b0856-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0856-124">Calificadores: [ **clave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b0856-124">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b0856-125">Cadena única asignada por el usuario que identifica este evento de temporizador determinado.</span><span class="sxs-lookup"><span data-stu-id="b0856-125">Unique user-assigned string that identifies this particular timer event.</span></span> <span data-ttu-id="b0856-126">Para evitar conflictos de nombres con otros identificadores de temporizador, se puede usar la forma de cadena de un GUID de estilo de entorno de equipo distribuido (DCE).</span><span class="sxs-lookup"><span data-stu-id="b0856-126">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment (DCE)-style GUID can be used.</span></span> <span data-ttu-id="b0856-127">Esta propiedad forma parte de la instancia de [**\_ \_ TimerEvent**](--timerevent.md) que representa el evento.</span><span class="sxs-lookup"><span data-stu-id="b0856-127">This property is part of the [**\_\_TimerEvent**](--timerevent.md) instance that represents the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0856-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0856-128">Remarks</span></span>

<span data-ttu-id="b0856-129">La clase **\_ \_ TimerInstruction** se deriva de [**\_ \_ EventGenerator**](--eventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="b0856-129">The **\_\_TimerInstruction** class is derived from [**\_\_EventGenerator**](--eventgenerator.md).</span></span>

<span data-ttu-id="b0856-130">Las subclases **\_ \_ TimerInstruction** son [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md), usadas por los consumidores para registrarse para un evento de temporizador absoluto y [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md), que se usan para registrarse para un evento de temporizador de intervalo.</span><span class="sxs-lookup"><span data-stu-id="b0856-130">The **\_\_TimerInstruction** subclasses are [**\_\_AbsoluteTimerInstruction**](--absolutetimerinstruction.md), used by consumers to register for an absolute timer event, and [**\_\_IntervalTimerInstruction**](--intervaltimerinstruction.md), used to register for an interval timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0856-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0856-131">Requirements</span></span>



| <span data-ttu-id="b0856-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0856-132">Requirement</span></span> | <span data-ttu-id="b0856-133">Value</span><span class="sxs-lookup"><span data-stu-id="b0856-133">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b0856-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0856-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b0856-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0856-135">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b0856-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0856-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b0856-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0856-137">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b0856-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b0856-138">Namespace</span></span><br/>                | <span data-ttu-id="b0856-139">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="b0856-139">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b0856-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0856-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0856-141">**\_\_EventGenerator**</span><span class="sxs-lookup"><span data-stu-id="b0856-141">**\_\_EventGenerator**</span></span>](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[<span data-ttu-id="b0856-142">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="b0856-142">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

