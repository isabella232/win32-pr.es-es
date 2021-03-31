---
description: Notifica un evento de modificación de instancia, que es un tipo de evento intrínseco generado cuando una instancia cambia en el espacio de nombres.
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: __InstanceModificationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e644db16b6638bbc87006819e186540a9ce1874e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911522"
---
# <a name="__instancemodificationevent-class"></a><span data-ttu-id="5a7f1-103">\_\_Clase InstanceModificationEvent</span><span class="sxs-lookup"><span data-stu-id="5a7f1-103">\_\_InstanceModificationEvent class</span></span>

<span data-ttu-id="5a7f1-104">La clase del sistema **\_ \_ InstanceModificationEvent** informa de un evento de modificación de instancia, que es un tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) generado cuando una instancia cambia en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="5a7f1-104">The **\_\_InstanceModificationEvent** system class reports an instance modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance changes in the namespace.</span></span>

<span data-ttu-id="5a7f1-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5a7f1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5a7f1-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5a7f1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a7f1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a7f1-107">Syntax</span></span>

``` syntax
class __InstanceModificationEvent : __InstanceOperationEvent
{
  object PreviousInstance;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="5a7f1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5a7f1-108">Members</span></span>

<span data-ttu-id="5a7f1-109">La clase **\_ \_ InstanceModificationEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5a7f1-109">The **\_\_InstanceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="5a7f1-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a7f1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a7f1-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a7f1-111">Properties</span></span>

<span data-ttu-id="5a7f1-112">La clase **\_ \_ InstanceModificationEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5a7f1-112">The **\_\_InstanceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a7f1-113">**PreviousInstance**</span><span class="sxs-lookup"><span data-stu-id="5a7f1-113">**PreviousInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a7f1-114">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="5a7f1-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5a7f1-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a7f1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a7f1-116">Copia de la instancia antes de la modificación.</span><span class="sxs-lookup"><span data-stu-id="5a7f1-116">Copy of the instance prior to modification.</span></span>

</dd> <dt>

<span data-ttu-id="5a7f1-117">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="5a7f1-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a7f1-118">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="5a7f1-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5a7f1-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a7f1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a7f1-120">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="5a7f1-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="5a7f1-121">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="5a7f1-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a7f1-122">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="5a7f1-122">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a7f1-123">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="5a7f1-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5a7f1-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a7f1-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a7f1-125">Nueva versión de la instancia modificada.</span><span class="sxs-lookup"><span data-stu-id="5a7f1-125">New version of the changed instance.</span></span> <span data-ttu-id="5a7f1-126">Esta propiedad se hereda de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="5a7f1-126">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a7f1-127">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="5a7f1-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a7f1-128">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a7f1-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a7f1-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a7f1-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a7f1-130">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="5a7f1-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="5a7f1-131">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="5a7f1-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="5a7f1-132">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="5a7f1-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="5a7f1-133">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="5a7f1-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="5a7f1-134">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5a7f1-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a7f1-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a7f1-135">Remarks</span></span>

<span data-ttu-id="5a7f1-136">La clase **\_ \_ InstanceModificationEvent** se deriva de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="5a7f1-136">The **\_\_InstanceModificationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="5a7f1-137">**Modificación de un recurso: \_ \_ InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="5a7f1-137">**Modification of a resource: \_\_InstanceModificationEvent**</span></span>

<span data-ttu-id="5a7f1-138">Supongamos que sospecha que una aplicación de administración que está usando está cambiando erróneamente el tipo de inicio de un servicio en uno de los servidores.</span><span class="sxs-lookup"><span data-stu-id="5a7f1-138">Suppose you suspect that a management application you are using is erroneously changing the startup type of a service on one of your servers.</span></span> <span data-ttu-id="5a7f1-139">Desea escribir un script de WMI para supervisar las modificaciones realizadas en la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="5a7f1-139">You want to write a WMI script to monitor any modifications made to the configuration of the service.</span></span> <span data-ttu-id="5a7f1-140">En cuanto se realiza una modificación en un servicio, su TargetInstance correspondiente refleja la modificación.</span><span class="sxs-lookup"><span data-stu-id="5a7f1-140">As soon as a modification is made to a service, its corresponding TargetInstance reflects the modification.</span></span>

<span data-ttu-id="5a7f1-141">Si registra su interés en este evento, una modificación en la configuración del servicio da como resultado la creación de una instancia de la clase **\_ \_ InstanceModificationEvent** .</span><span class="sxs-lookup"><span data-stu-id="5a7f1-141">If you register your interest in this event, a modification to the configuration of the service results in the creation of an instance of the **\_\_InstanceModificationEvent** class.</span></span>

<span data-ttu-id="5a7f1-142">Las consultas de notificación que solicitan la notificación de la modificación de un recurso y usan eventos intrínsecos usan una sintaxis similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="5a7f1-142">Notification queries that request notification of the modification of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a><span data-ttu-id="5a7f1-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5a7f1-143">Examples</span></span>

<span data-ttu-id="5a7f1-144">El ejemplo de VBScript del [evento de modificación del proceso de supervisión](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) en la galería de TechNet usa **\_ \_ InstanceModificationEvent** para supervisar la primera aparición de un evento de modificación de instancia de WMI para el [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="5a7f1-144">The [Monitor process modification event](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) VBScript sample on TechNet Gallery uses **\_\_InstanceModificationEvent** to monitor the first occurrence of a WMI instance modification event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a7f1-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a7f1-145">Requirements</span></span>



| <span data-ttu-id="5a7f1-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a7f1-146">Requirement</span></span> | <span data-ttu-id="5a7f1-147">Value</span><span class="sxs-lookup"><span data-stu-id="5a7f1-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5a7f1-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a7f1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="5a7f1-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a7f1-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5a7f1-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a7f1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="5a7f1-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a7f1-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5a7f1-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5a7f1-152">Namespace</span></span><br/>                | <span data-ttu-id="5a7f1-153">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="5a7f1-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5a7f1-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a7f1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a7f1-155">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="5a7f1-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="5a7f1-156">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="5a7f1-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

