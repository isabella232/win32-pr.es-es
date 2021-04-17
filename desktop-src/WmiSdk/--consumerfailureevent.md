---
description: Representa la aparición de algún otro evento que se está quitando debido al error de un consumidor de eventos.
ms.assetid: bb6a1ce9-72a2-4528-8bc8-71ac053b6b1d
ms.tgt_platform: multiple
title: __ConsumerFailureEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ConsumerFailureEvent
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 571785245c05d18678c10a65b192a25022fff8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707415"
---
# <a name="__consumerfailureevent-class"></a><span data-ttu-id="29909-103">\_\_Clase ConsumerFailureEvent</span><span class="sxs-lookup"><span data-stu-id="29909-103">\_\_ConsumerFailureEvent class</span></span>

<span data-ttu-id="29909-104">La clase del sistema **\_ \_ ConsumerFailureEvent** representa la aparición de algún otro evento que se está quitando debido al error de un consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="29909-104">The **\_\_ConsumerFailureEvent** system class represents the occurrence of some other event that is being dropped because of the failure of an event consumer.</span></span>

<span data-ttu-id="29909-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="29909-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="29909-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="29909-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="29909-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29909-107">Syntax</span></span>

``` syntax
class __ConsumerFailureEvent : __EventDroppedEvent
{
  uint32              ErrorCode;
  string              ErrorDescription;
  object              ErrorObject;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="29909-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="29909-108">Members</span></span>

<span data-ttu-id="29909-109">La clase **\_ \_ ConsumerFailureEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="29909-109">The **\_\_ConsumerFailureEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="29909-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="29909-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29909-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="29909-111">Properties</span></span>

<span data-ttu-id="29909-112">La clase **\_ \_ ConsumerFailureEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="29909-112">The **\_\_ConsumerFailureEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29909-113">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="29909-113">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29909-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29909-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="29909-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29909-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29909-116">Código de error devuelto por el consumidor.</span><span class="sxs-lookup"><span data-stu-id="29909-116">Error code returned by the consumer.</span></span>

</dd> <dt>

<span data-ttu-id="29909-117">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="29909-117">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29909-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="29909-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29909-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29909-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29909-120">Descripción del código de error extendido, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="29909-120">Extended error code description, if available.</span></span>

</dd> <dt>

<span data-ttu-id="29909-121">**ErrorObject**</span><span class="sxs-lookup"><span data-stu-id="29909-121">**ErrorObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29909-122">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="29909-122">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="29909-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29909-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29909-124">Objeto con error.</span><span class="sxs-lookup"><span data-stu-id="29909-124">Object in error.</span></span>

</dd> <dt>

<span data-ttu-id="29909-125">**Evento**</span><span class="sxs-lookup"><span data-stu-id="29909-125">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29909-126">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="29909-126">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="29909-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29909-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29909-128">Evento en caso de error.</span><span class="sxs-lookup"><span data-stu-id="29909-128">Event in error.</span></span> <span data-ttu-id="29909-129">Esta propiedad se hereda de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="29909-129">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="29909-130">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="29909-130">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29909-131">Tipo de datos: **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="29909-131">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="29909-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29909-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29909-133">Referencia al consumidor previsto.</span><span class="sxs-lookup"><span data-stu-id="29909-133">Reference to the intended consumer.</span></span> <span data-ttu-id="29909-134">Esta propiedad se hereda de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="29909-134">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="29909-135">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="29909-135">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29909-136">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="29909-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="29909-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29909-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29909-138">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="29909-138">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="29909-139">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="29909-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="29909-140">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="29909-140">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29909-141">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="29909-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="29909-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="29909-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29909-143">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="29909-143">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="29909-144">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="29909-144">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="29909-145">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="29909-145">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="29909-146">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="29909-146">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="29909-147">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="29909-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29909-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29909-148">Remarks</span></span>

<span data-ttu-id="29909-149">La clase **\_ \_ ConsumerFailureEvent** se deriva de [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="29909-149">The **\_\_ConsumerFailureEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29909-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29909-150">Requirements</span></span>



| <span data-ttu-id="29909-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="29909-151">Requirement</span></span> | <span data-ttu-id="29909-152">Value</span><span class="sxs-lookup"><span data-stu-id="29909-152">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="29909-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29909-153">Minimum supported client</span></span><br/> | <span data-ttu-id="29909-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29909-154">Windows Vista</span></span><br/>       |
| <span data-ttu-id="29909-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29909-155">Minimum supported server</span></span><br/> | <span data-ttu-id="29909-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29909-156">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="29909-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="29909-157">Namespace</span></span><br/>                | <span data-ttu-id="29909-158">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="29909-158">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="29909-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="29909-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29909-160">**\_\_EventDroppedEvent**</span><span class="sxs-lookup"><span data-stu-id="29909-160">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="29909-161">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="29909-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

