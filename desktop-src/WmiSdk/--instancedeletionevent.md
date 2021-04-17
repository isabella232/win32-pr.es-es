---
description: Notifica un evento de eliminación de instancia, que es un tipo de evento intrínseco que se genera cuando se elimina una instancia del espacio de nombres.
ms.assetid: a370fc95-15e3-49c3-98de-2f40d742f207
ms.tgt_platform: multiple
title: __InstanceDeletionEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 018bac665aa95393fc1a9c7e51ad42038e8b27c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706772"
---
# <a name="__instancedeletionevent-class"></a><span data-ttu-id="6c6dd-103">\_\_Clase InstanceDeletionEvent</span><span class="sxs-lookup"><span data-stu-id="6c6dd-103">\_\_InstanceDeletionEvent class</span></span>

<span data-ttu-id="6c6dd-104">La clase del sistema **\_ \_ InstanceDeletionEvent** informa de un evento de eliminación de instancia, que es un tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que se genera cuando se elimina una instancia del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="6c6dd-104">The **\_\_InstanceDeletionEvent** system class reports an instance deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance is deleted from the namespace.</span></span>

<span data-ttu-id="6c6dd-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6c6dd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6c6dd-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6c6dd-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6dd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c6dd-107">Syntax</span></span>

``` syntax
class __InstanceDeletionEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="6c6dd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c6dd-108">Members</span></span>

<span data-ttu-id="6c6dd-109">La clase **\_ \_ InstanceDeletionEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6c6dd-109">The **\_\_InstanceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="6c6dd-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6c6dd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c6dd-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6c6dd-111">Properties</span></span>

<span data-ttu-id="6c6dd-112">La clase **\_ \_ InstanceDeletionEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6c6dd-112">The **\_\_InstanceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c6dd-113">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="6c6dd-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c6dd-114">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="6c6dd-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6c6dd-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6c6dd-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c6dd-116">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="6c6dd-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="6c6dd-117">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="6c6dd-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c6dd-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="6c6dd-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c6dd-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="6c6dd-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="6c6dd-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6c6dd-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c6dd-121">Copia de la instancia de que se eliminó.</span><span class="sxs-lookup"><span data-stu-id="6c6dd-121">Copy of the instance that was deleted.</span></span> <span data-ttu-id="6c6dd-122">Esta propiedad se hereda de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="6c6dd-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c6dd-123">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="6c6dd-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c6dd-124">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6c6dd-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6c6dd-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6c6dd-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c6dd-126">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="6c6dd-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="6c6dd-127">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="6c6dd-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="6c6dd-128">La información tiene el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="6c6dd-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="6c6dd-129">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="6c6dd-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="6c6dd-130">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6c6dd-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c6dd-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c6dd-131">Remarks</span></span>

<span data-ttu-id="6c6dd-132">La clase **\_ \_ InstanceDeletionEvent** se deriva de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="6c6dd-132">The **\_\_InstanceDeletionEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="6c6dd-133">**Eliminación de un recurso: \_ \_ InstanceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="6c6dd-133">**Deletion of a resource: \_\_InstanceDeletionEvent**</span></span>

<span data-ttu-id="6c6dd-134">Si desea asegurarse de que un programa de analizador antivirus determinado se ejecuta en un equipo, puede escribir un script que supervise los procesos del equipo para determinar si se detienen.</span><span class="sxs-lookup"><span data-stu-id="6c6dd-134">If you want to ensure that a particular antivirus scanner program continues to run on a computer, you can write a script that monitors the processes on the computer to determine whether any of them stop.</span></span>

<span data-ttu-id="6c6dd-135">Las consultas de notificación que solicitan la eliminación de un recurso y usan eventos intrínsecos usan una sintaxis similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="6c6dd-135">Notification queries that request notification of the deletion of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceDeletionEvent WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe' `

## <a name="examples"></a><span data-ttu-id="6c6dd-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6c6dd-136">Examples</span></span>

<span data-ttu-id="6c6dd-137">El ejemplo de código VBScript del [evento de eliminación de proceso de supervisión](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) en la galería de TechNet usa **\_ \_ InstanceDeletionEvent** para supervisar la primera aparición de un evento de eliminación de instancia de WMI para el [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="6c6dd-137">The [Monitor process deletion event](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) VBScript code sample on TechNet Gallery uses **\_\_InstanceDeletionEvent** to monitor the first occurrence of a WMI instance deletion event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c6dd-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c6dd-138">Requirements</span></span>



| <span data-ttu-id="6c6dd-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c6dd-139">Requirement</span></span> | <span data-ttu-id="6c6dd-140">Value</span><span class="sxs-lookup"><span data-stu-id="6c6dd-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6c6dd-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c6dd-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6c6dd-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c6dd-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6c6dd-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c6dd-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6c6dd-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c6dd-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6c6dd-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6c6dd-145">Namespace</span></span><br/>                | <span data-ttu-id="6c6dd-146">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="6c6dd-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6c6dd-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c6dd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c6dd-148">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="6c6dd-148">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="6c6dd-149">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="6c6dd-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

