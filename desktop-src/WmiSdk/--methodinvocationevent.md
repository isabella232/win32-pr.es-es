---
description: La \_ \_ clase del sistema MethodInvocationEvent está definida pero no se implementa.
ms.assetid: ea736e44-a6bc-41e5-abc5-9e21a5504f44
ms.tgt_platform: multiple
title: __MethodInvocationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodInvocationEvent
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
ms.openlocfilehash: bc7e8d70d027caf31a90d49abc490c2de2d52fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277942"
---
# <a name="__methodinvocationevent-class"></a><span data-ttu-id="dd738-103">\_\_Clase MethodInvocationEvent</span><span class="sxs-lookup"><span data-stu-id="dd738-103">\_\_MethodInvocationEvent class</span></span>

<span data-ttu-id="dd738-104">La clase del sistema **\_ \_ MethodInvocationEvent** está definida pero no se implementa.</span><span class="sxs-lookup"><span data-stu-id="dd738-104">The **\_\_MethodInvocationEvent** system class is defined but is not implemented.</span></span>

<span data-ttu-id="dd738-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="dd738-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dd738-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="dd738-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd738-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd738-107">Syntax</span></span>

``` syntax
class __MethodInvocationEvent : __InstanceOperationEvent
{
  string       Method;
  __Parameters Parameters;
  boolean      PreCall;
  uint8        SECURITY_DESCRIPTOR[];
  object       TargetInstance;
  uint64       TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="dd738-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="dd738-108">Members</span></span>

<span data-ttu-id="dd738-109">La clase **\_ \_ MethodInvocationEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dd738-109">The **\_\_MethodInvocationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="dd738-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd738-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd738-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd738-111">Properties</span></span>

<span data-ttu-id="dd738-112">La clase **\_ \_ MethodInvocationEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dd738-112">The **\_\_MethodInvocationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd738-113">**Método**</span><span class="sxs-lookup"><span data-stu-id="dd738-113">**Method**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd738-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd738-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd738-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd738-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd738-116">Método invocado para desencadenar el evento.</span><span class="sxs-lookup"><span data-stu-id="dd738-116">Method invoked to trigger the event.</span></span>

</dd> <dt>

<span data-ttu-id="dd738-117">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="dd738-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd738-118">Tipo de datos: **\_ \_ parámetros**</span><span class="sxs-lookup"><span data-stu-id="dd738-118">Data type: **\_\_Parameters**</span></span>
</dt> <dt>

<span data-ttu-id="dd738-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd738-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd738-120">Referencia a una instancia de que representa los parámetros de entrada y salida de la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="dd738-120">Reference to an instance that represents the input and output parameters of the method call.</span></span>

</dd> <dt>

<span data-ttu-id="dd738-121">**Llamada precall**</span><span class="sxs-lookup"><span data-stu-id="dd738-121">**PreCall**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd738-122">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dd738-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd738-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd738-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd738-124">Si es **true**, el evento se genera antes de que se llame al método.</span><span class="sxs-lookup"><span data-stu-id="dd738-124">If **TRUE**, the event is raised before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="dd738-125">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="dd738-125">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd738-126">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="dd738-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="dd738-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd738-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd738-128">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="dd738-128">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="dd738-129">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="dd738-129">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="dd738-130">Para obtener más información, vea [descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptors).</span><span class="sxs-lookup"><span data-stu-id="dd738-130">For more information, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

</dd> <dt>

<span data-ttu-id="dd738-131">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="dd738-131">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd738-132">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="dd738-132">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="dd738-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd738-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd738-134">Instancia en la que se invoca el método.</span><span class="sxs-lookup"><span data-stu-id="dd738-134">Instance the method is invoked on.</span></span> <span data-ttu-id="dd738-135">Esta propiedad se hereda de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="dd738-135">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd738-136">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="dd738-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd738-137">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dd738-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dd738-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd738-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd738-139">Valor único que indica la hora a la que se genera un evento.</span><span class="sxs-lookup"><span data-stu-id="dd738-139">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="dd738-140">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="dd738-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="dd738-141">La información tiene el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="dd738-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="dd738-142">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="dd738-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="dd738-143">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dd738-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd738-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd738-144">Remarks</span></span>

<span data-ttu-id="dd738-145">La clase **\_ \_ MethodInvocationEvent** se deriva de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="dd738-145">The **\_\_MethodInvocationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd738-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd738-146">Requirements</span></span>



| <span data-ttu-id="dd738-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd738-147">Requirement</span></span> | <span data-ttu-id="dd738-148">Value</span><span class="sxs-lookup"><span data-stu-id="dd738-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="dd738-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd738-149">Minimum supported client</span></span><br/> | <span data-ttu-id="dd738-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd738-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="dd738-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd738-151">Minimum supported server</span></span><br/> | <span data-ttu-id="dd738-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd738-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="dd738-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd738-153">Namespace</span></span><br/>                | <span data-ttu-id="dd738-154">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="dd738-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="dd738-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd738-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd738-156">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="dd738-156">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="dd738-157">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="dd738-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

