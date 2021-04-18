---
description: Representa la aparición de un evento que se ha quitado. Un evento quitado es un evento que no se entrega a un consumidor de eventos.
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: __EventDroppedEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventDroppedEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4e9f68328a3c5c455c98e85a65d53156da6eeada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706847"
---
# <a name="__eventdroppedevent-class"></a><span data-ttu-id="40026-104">\_\_Clase EventDroppedEvent</span><span class="sxs-lookup"><span data-stu-id="40026-104">\_\_EventDroppedEvent class</span></span>

<span data-ttu-id="40026-105">La clase del sistema **\_ \_ EventDroppedEvent** representa la aparición de un evento que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="40026-105">The **\_\_EventDroppedEvent** system class represents the occurrence of an event that is dropped.</span></span> <span data-ttu-id="40026-106">Un evento quitado es un evento que no se entrega a un consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="40026-106">A dropped event is an event that is not delivered to an event consumer.</span></span>

<span data-ttu-id="40026-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="40026-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="40026-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="40026-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="40026-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40026-109">Syntax</span></span>

``` syntax
class __EventDroppedEvent : __SystemEvent
{
  __Event             Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="40026-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="40026-110">Members</span></span>

<span data-ttu-id="40026-111">La clase **\_ \_ EventDroppedEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="40026-111">The **\_\_EventDroppedEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="40026-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40026-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40026-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40026-113">Properties</span></span>

<span data-ttu-id="40026-114">La clase **\_ \_ EventDroppedEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="40026-114">The **\_\_EventDroppedEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40026-115">**Evento**</span><span class="sxs-lookup"><span data-stu-id="40026-115">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40026-116">Tipo de datos: **\_ \_ evento**</span><span class="sxs-lookup"><span data-stu-id="40026-116">Data type: **\_\_Event**</span></span>
</dt> <dt>

<span data-ttu-id="40026-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40026-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40026-118">Evento que se quita.</span><span class="sxs-lookup"><span data-stu-id="40026-118">Event that is dropped.</span></span>

</dd> <dt>

<span data-ttu-id="40026-119">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="40026-119">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40026-120">Tipo de datos: **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="40026-120">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="40026-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40026-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40026-122">Referencia a una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) que representa el consumidor permanente que se identifica para recibir un evento.</span><span class="sxs-lookup"><span data-stu-id="40026-122">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the permanent consumer you identify to receive an event.</span></span> <span data-ttu-id="40026-123">Los distintos consumidores permanentes que se suscriben a un evento pueden seguir recibiendo el evento.</span><span class="sxs-lookup"><span data-stu-id="40026-123">Different permanent consumers that subscribe to an event can continue to receive the event.</span></span>

</dd> <dt>

<span data-ttu-id="40026-124">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="40026-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40026-125">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="40026-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="40026-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40026-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40026-127">Descriptor que un proveedor de eventos utiliza para determinar los usuarios que pueden recibir un evento.</span><span class="sxs-lookup"><span data-stu-id="40026-127">Descriptor that an event provider uses to determine the users who can receive an event.</span></span> <span data-ttu-id="40026-128">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="40026-128">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="40026-129">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="40026-129">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40026-130">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="40026-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="40026-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40026-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40026-132">Valor único que indica la hora a la que se genera un evento.</span><span class="sxs-lookup"><span data-stu-id="40026-132">Unique value that indicates the time when an event is generated.</span></span> <span data-ttu-id="40026-133">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="40026-133">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="40026-134">La información tiene el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="40026-134">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="40026-135">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="40026-135">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="40026-136">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="40026-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40026-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40026-137">Remarks</span></span>

<span data-ttu-id="40026-138">La clase **\_ \_ EventDroppedEvent** se deriva de [**\_ \_ SystemEvent**](--systemevent.md).</span><span class="sxs-lookup"><span data-stu-id="40026-138">The **\_\_EventDroppedEvent** class is derived from [**\_\_SystemEvent**](--systemevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40026-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40026-139">Requirements</span></span>



| <span data-ttu-id="40026-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="40026-140">Requirement</span></span> | <span data-ttu-id="40026-141">Value</span><span class="sxs-lookup"><span data-stu-id="40026-141">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="40026-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40026-142">Minimum supported client</span></span><br/> | <span data-ttu-id="40026-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40026-143">Windows Vista</span></span><br/>       |
| <span data-ttu-id="40026-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40026-144">Minimum supported server</span></span><br/> | <span data-ttu-id="40026-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40026-145">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="40026-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="40026-146">Namespace</span></span><br/>                | <span data-ttu-id="40026-147">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="40026-147">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="40026-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="40026-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40026-149">**\_\_SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="40026-149">**\_\_SystemEvent**</span></span>](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[<span data-ttu-id="40026-150">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="40026-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

