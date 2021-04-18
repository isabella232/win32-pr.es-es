---
description: Informa de Cuándo se quita un evento como resultado del desbordamiento de la cola de entrega.
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: __EventQueueOverflowEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventQueueOverflowEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 058b03b8a3311aad805f47a04d20e9f1fa8c2477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716874"
---
# <a name="__eventqueueoverflowevent-class"></a><span data-ttu-id="b9413-103">\_\_Clase EventQueueOverflowEvent</span><span class="sxs-lookup"><span data-stu-id="b9413-103">\_\_EventQueueOverflowEvent class</span></span>

<span data-ttu-id="b9413-104">La clase del sistema **\_ \_ EventQueueOverflowEvent** informa cuando se quita un evento como resultado del desbordamiento de la cola de entrega.</span><span class="sxs-lookup"><span data-stu-id="b9413-104">The **\_\_EventQueueOverflowEvent** system class reports when an event is dropped as a result of delivery queue overflow.</span></span>

<span data-ttu-id="b9413-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b9413-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b9413-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b9413-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9413-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9413-107">Syntax</span></span>

``` syntax
class __EventQueueOverflowEvent : __EventDroppedEvent
{
  uint32              CurrentQueueSize;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="b9413-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b9413-108">Members</span></span>

<span data-ttu-id="b9413-109">La clase **\_ \_ EventQueueOverflowEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b9413-109">The **\_\_EventQueueOverflowEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="b9413-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9413-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9413-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9413-111">Properties</span></span>

<span data-ttu-id="b9413-112">La clase **\_ \_ EventQueueOverflowEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b9413-112">The **\_\_EventQueueOverflowEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b9413-113">**CurrentQueueSize**</span><span class="sxs-lookup"><span data-stu-id="b9413-113">**CurrentQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9413-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9413-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9413-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9413-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9413-116">Tamaño actual de la cola, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b9413-116">Current queue size, in bytes.</span></span> <span data-ttu-id="b9413-117">Esta propiedad tiene como valor predeterminado 10 MB para todas las colas combinadas.</span><span class="sxs-lookup"><span data-stu-id="b9413-117">This property defaults to 10 MB for all queues combined.</span></span>

</dd> <dt>

<span data-ttu-id="b9413-118">**Evento**</span><span class="sxs-lookup"><span data-stu-id="b9413-118">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9413-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="b9413-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b9413-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9413-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9413-121">Evento de interés.</span><span class="sxs-lookup"><span data-stu-id="b9413-121">Event of interest.</span></span> <span data-ttu-id="b9413-122">Esta propiedad se hereda de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="b9413-122">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9413-123">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="b9413-123">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9413-124">Tipo de datos: **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="b9413-124">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="b9413-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9413-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9413-126">Referencia al consumidor previsto.</span><span class="sxs-lookup"><span data-stu-id="b9413-126">Reference to the intended consumer.</span></span> <span data-ttu-id="b9413-127">Esta propiedad se hereda de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="b9413-127">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9413-128">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="b9413-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9413-129">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="b9413-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b9413-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9413-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9413-131">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="b9413-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="b9413-132">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="b9413-132">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9413-133">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="b9413-133">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9413-134">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9413-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9413-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9413-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9413-136">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="b9413-136">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="b9413-137">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="b9413-137">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="b9413-138">La información tiene el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="b9413-138">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="b9413-139">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="b9413-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="b9413-140">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b9413-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9413-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9413-141">Remarks</span></span>

<span data-ttu-id="b9413-142">Solo los usuarios con privilegios de administrador pueden recibir este evento.</span><span class="sxs-lookup"><span data-stu-id="b9413-142">Only users with administrator privileges are able to receive this event.</span></span> <span data-ttu-id="b9413-143">La clase **\_ \_ EventQueueOverflowEvent** se deriva de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="b9413-143">The **\_\_EventQueueOverflowEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

<span data-ttu-id="b9413-144">Para obtener más información, vea la propiedad [**MaximumQueueSize**](--eventconsumer.md) en la clase [**\_ \_ EventConsumer**](--eventconsumer.md) y la propiedad [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) en la clase **\_ WMISetting de Win32** .</span><span class="sxs-lookup"><span data-stu-id="b9413-144">For more information, see the [**MaximumQueueSize**](--eventconsumer.md) property in the [**\_\_EventConsumer**](--eventconsumer.md) class and the [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property in the **Win32\_WMISetting** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9413-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9413-145">Requirements</span></span>



| <span data-ttu-id="b9413-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9413-146">Requirement</span></span> | <span data-ttu-id="b9413-147">Value</span><span class="sxs-lookup"><span data-stu-id="b9413-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b9413-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9413-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b9413-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9413-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b9413-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9413-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b9413-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9413-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b9413-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b9413-152">Namespace</span></span><br/>                | <span data-ttu-id="b9413-153">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="b9413-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b9413-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9413-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9413-155">**\_\_EventDroppedEvent**</span><span class="sxs-lookup"><span data-stu-id="b9413-155">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="b9413-156">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="b9413-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

