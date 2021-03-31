---
description: Informa de un evento de creación de instancia, que es un tipo de evento intrínseco que se genera cuando se agrega una nueva instancia al espacio de nombres.
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: __InstanceCreationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29bdefbe1db20cd8b55b74433061b6c0cf152378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278781"
---
# <a name="__instancecreationevent-class"></a><span data-ttu-id="43d71-103">\_\_Clase InstanceCreationEvent</span><span class="sxs-lookup"><span data-stu-id="43d71-103">\_\_InstanceCreationEvent class</span></span>

<span data-ttu-id="43d71-104">La clase del sistema **\_ \_ InstanceCreationEvent** informa de un evento de creación de instancia, que es un tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que se genera cuando se agrega una nueva instancia al espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="43d71-104">The **\_\_InstanceCreationEvent** system class reports an instance creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a new instance is added to the namespace.</span></span>

<span data-ttu-id="43d71-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="43d71-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="43d71-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="43d71-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d71-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43d71-107">Syntax</span></span>

``` syntax
class __InstanceCreationEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="43d71-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="43d71-108">Members</span></span>

<span data-ttu-id="43d71-109">La clase **\_ \_ InstanceCreationEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="43d71-109">The **\_\_InstanceCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="43d71-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="43d71-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43d71-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="43d71-111">Properties</span></span>

<span data-ttu-id="43d71-112">La clase **\_ \_ InstanceCreationEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="43d71-112">The **\_\_InstanceCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43d71-113">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="43d71-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43d71-114">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="43d71-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="43d71-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43d71-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43d71-116">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="43d71-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="43d71-117">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="43d71-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="43d71-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="43d71-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43d71-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="43d71-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="43d71-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43d71-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43d71-121">Copia de la instancia de que se creó.</span><span class="sxs-lookup"><span data-stu-id="43d71-121">Copy of the instance that was created.</span></span> <span data-ttu-id="43d71-122">Esta propiedad se hereda de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="43d71-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="43d71-123">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="43d71-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43d71-124">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="43d71-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="43d71-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="43d71-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43d71-126">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="43d71-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="43d71-127">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="43d71-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="43d71-128">La información tiene el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="43d71-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="43d71-129">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="43d71-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="43d71-130">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="43d71-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43d71-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43d71-131">Remarks</span></span>

<span data-ttu-id="43d71-132">La clase **\_ \_ InstanceCreationEvent** se deriva de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="43d71-132">The **\_\_InstanceCreationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="43d71-133">**Creación de un recurso: \_ \_ InstanceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="43d71-133">**Creation of a resource: \_\_InstanceCreationEvent**</span></span>

<span data-ttu-id="43d71-134">Supongamos que está interesado en recibir una notificación si el Bloc de notas se ejecuta en un equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="43d71-134">Suppose you are interested in receiving a notification if Notepad is run on a certain computer.</span></span> <span data-ttu-id="43d71-135">Cuando se ejecuta el Bloc de notas, se crea un proceso correspondiente.</span><span class="sxs-lookup"><span data-stu-id="43d71-135">When Notepad runs, a corresponding process is created.</span></span> <span data-ttu-id="43d71-136">Los procesos se pueden administrar mediante WMI y se representan mediante la clase de proceso de Win32 \_ .</span><span class="sxs-lookup"><span data-stu-id="43d71-136">Processes can be managed by using WMI and are represented by the Win32\_Process class.</span></span> <span data-ttu-id="43d71-137">Cuando el Bloc de notas comienza a ejecutarse, una instancia correspondiente de la clase de proceso de Win32 \_ pasa a estar disponible a través de WMI.</span><span class="sxs-lookup"><span data-stu-id="43d71-137">When Notepad starts running, a corresponding instance of the Win32\_Process class becomes available through WMI.</span></span> <span data-ttu-id="43d71-138">Si ha registrado su interés en este evento (emitiendo la consulta de notificación de eventos adecuada), la disponibilidad de esta instancia da como resultado la creación de una instancia de la clase **\_ \_ InstanceCreationEvent** .</span><span class="sxs-lookup"><span data-stu-id="43d71-138">If you have registered your interest in this event (by issuing the appropriate event notification query), the availability of this instance results in the creation of an instance of the **\_\_InstanceCreationEvent** class.</span></span>

<span data-ttu-id="43d71-139">Las consultas de notificación que solicitan la notificación de la creación de un recurso y usan eventos intrínsecos usan una sintaxis similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="43d71-139">Notification queries that request notification of the creation of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

<span data-ttu-id="43d71-140">Para obtener una explicación más amplia del uso de **\_ \_ InstanceCreationEvent** como una manera de supervisar sistemas de archivos, consulte [WMI y supervisión del sistema de archivos](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) en CodeProject.</span><span class="sxs-lookup"><span data-stu-id="43d71-140">For a larger discussion of using **\_\_InstanceCreationEvent** as a way to monitor file systems, see [WMI and File System Monitoring](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) on CodeProject.</span></span>

## <a name="examples"></a><span data-ttu-id="43d71-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="43d71-141">Examples</span></span>

<span data-ttu-id="43d71-142">El ejemplo de [creación de registro de eventos de WMI permanente para supervisar archivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) de PowerShell en la galería de TechNet usa **\_ \_ InstanceCreationEvent** como parte de un script complejo para configurar un registro de eventos de WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="43d71-142">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a complex script to set up a permanent WMI event registration.</span></span>

<span data-ttu-id="43d71-143">El ejemplo de PowerShell de [eventos permanentes de WMI de PowerShell](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) en la galería de TechNet usa **\_ \_ InstanceCreationEvent** como parte de un script de demostración para configurar un registro de eventos permanente.</span><span class="sxs-lookup"><span data-stu-id="43d71-143">The [PowerShell WMI Permanent Events](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a demonstration script for setting up a permanent event registration.</span></span>

<span data-ttu-id="43d71-144">En el ejemplo de VBScript del [evento de creación de procesos de supervisión](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) en TechNet se usa **\_ \_ InstanceCreationEvent** para supervisar el primer evento de creación de instancia de WMI para el [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="43d71-144">The [Monitor process creation event](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) VBScript sample on TechNet uses **\_\_InstanceCreationEvent** to monitors the first WMI instance creation event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="43d71-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43d71-145">Requirements</span></span>



| <span data-ttu-id="43d71-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="43d71-146">Requirement</span></span> | <span data-ttu-id="43d71-147">Value</span><span class="sxs-lookup"><span data-stu-id="43d71-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="43d71-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43d71-148">Minimum supported client</span></span><br/> | <span data-ttu-id="43d71-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43d71-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="43d71-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43d71-150">Minimum supported server</span></span><br/> | <span data-ttu-id="43d71-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43d71-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="43d71-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="43d71-152">Namespace</span></span><br/>                | <span data-ttu-id="43d71-153">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="43d71-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="43d71-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="43d71-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d71-155">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="43d71-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="43d71-156">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="43d71-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

