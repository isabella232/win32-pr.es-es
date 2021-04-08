---
description: Informa de un evento de modificación del espacio de nombres, que es un tipo de evento intrínseco que se genera cuando se modifica un espacio de nombres.
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: __NamespaceModificationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceModificationEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5af5783d3ebfbfb4b7842cb86b1919f8dbed1365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817614"
---
# <a name="__namespacemodificationevent-class"></a><span data-ttu-id="98763-103">\_\_Clase NamespaceModificationEvent</span><span class="sxs-lookup"><span data-stu-id="98763-103">\_\_NamespaceModificationEvent class</span></span>

<span data-ttu-id="98763-104">La clase del sistema **\_ \_ NamespaceModificationEvent** informa de un evento de modificación del espacio de nombres, que es un tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que se genera cuando se modifica un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="98763-104">The **\_\_NamespaceModificationEvent** system class reports a namespace modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a namespace is modified.</span></span>

<span data-ttu-id="98763-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="98763-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="98763-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="98763-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="98763-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98763-107">Syntax</span></span>

``` syntax
class __NamespaceModificationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace PreviousNamespace;
  uint8       SECURITY_DESCRIPTOR [];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="98763-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="98763-108">Members</span></span>

<span data-ttu-id="98763-109">La clase **\_ \_ NamespaceModificationEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="98763-109">The **\_\_NamespaceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="98763-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="98763-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98763-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="98763-111">Properties</span></span>

<span data-ttu-id="98763-112">La clase **\_ \_ NamespaceModificationEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="98763-112">The **\_\_NamespaceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98763-113">**PreviousNamespace**</span><span class="sxs-lookup"><span data-stu-id="98763-113">**PreviousNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98763-114">Tipo de datos: **\_ \_ espacio de nombres**</span><span class="sxs-lookup"><span data-stu-id="98763-114">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="98763-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98763-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98763-116">Copia de la versión original de una instancia de [**\_ \_ espacio de nombres**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="98763-116">Copy of the original version of a [**\_\_Namespace**](--namespace.md) instance.</span></span> <span data-ttu-id="98763-117">La propiedad **nombre** de esta instancia identifica el espacio de nombres que se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="98763-117">The **Name** property of this instance identifies the namespace that is modified.</span></span>

</dd> <dt>

<span data-ttu-id="98763-118">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="98763-118">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98763-119">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="98763-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="98763-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98763-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98763-121">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="98763-121">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="98763-122">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="98763-122">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="98763-123">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="98763-123">**SECURITY\_DESCRIPTOR**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="98763-124">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="98763-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="98763-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98763-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98763-126">Descriptor que el proveedor de eventos utiliza para determinar los usuarios que pueden recibir un evento.</span><span class="sxs-lookup"><span data-stu-id="98763-126">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="98763-127">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="98763-127">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="98763-128">Una lista de control de acceso (ACL) **nula** en el [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado a todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="98763-128">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="98763-129">Para obtener más información, vea [crear un descriptor de seguridad para un nuevo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="98763-129">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="98763-130">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="98763-130">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98763-131">Tipo de datos: **\_ \_ espacio de nombres**</span><span class="sxs-lookup"><span data-stu-id="98763-131">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="98763-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98763-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98763-133">Copia de la instancia de [**\_ \_ espacio de nombres**](--namespace.md) que se modifica.</span><span class="sxs-lookup"><span data-stu-id="98763-133">Copy of the [**\_\_Namespace**](--namespace.md) instance that is modified.</span></span> <span data-ttu-id="98763-134">La propiedad **Name** de la instancia de **\_ \_ espacio de nombres** indica el espacio de nombres que se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="98763-134">The **Name** property of the **\_\_Namespace** instance indicates the namespace that is modified.</span></span> <span data-ttu-id="98763-135">Esta propiedad se hereda de la clase [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="98763-135">This property is inherited from class [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="98763-136">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="98763-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98763-137">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="98763-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="98763-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98763-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98763-139">Valor único que indica la hora a la que se genera un evento.</span><span class="sxs-lookup"><span data-stu-id="98763-139">Unique value that indicates the time that an event is generated.</span></span> <span data-ttu-id="98763-140">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="98763-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="98763-141">La información tiene el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="98763-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="98763-142">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="98763-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="98763-143">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="98763-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98763-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98763-144">Remarks</span></span>

<span data-ttu-id="98763-145">La clase **\_ \_ NamespaceModificationEvent** se deriva de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="98763-145">The **\_\_NamespaceModificationEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

<span data-ttu-id="98763-146">Las únicas diferencias entre el espacio de nombres de destino y el espacio de nombres anterior son los calificadores y las propiedades excepto [**Name**](--namespace.md).</span><span class="sxs-lookup"><span data-stu-id="98763-146">The only differences between the target namespace and the previous namespace is the qualifiers and properties except [**Name**](--namespace.md).</span></span>

<span data-ttu-id="98763-147">Tenga en cuenta que la propiedad [**Name**](--namespace.md) de una instancia de **\_ \_ espacio de nombres** no puede cambiar porque no se puede cambiar el nombre de los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="98763-147">Note that the [**Name**](--namespace.md) property of a **\_\_Namespace** instance cannot change because namespaces cannot be renamed.</span></span> <span data-ttu-id="98763-148">Para modificar el nombre de un espacio de nombres, se debe eliminar la instancia de **\_ \_ espacio de nombres** y volver a crearla con un nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="98763-148">To modify the name of a namespace, the **\_\_Namespace** instance must be deleted and re-created with a new name.</span></span> <span data-ttu-id="98763-149">Por lo tanto, los eventos de modificación del espacio de nombres se generan cuando se produce un cambio en calificadores y propiedades que no sean **Name**.</span><span class="sxs-lookup"><span data-stu-id="98763-149">Therefore, namespace modification events are generated when a change occurs to qualifiers and properties other than **Name**.</span></span> <span data-ttu-id="98763-150">Un evento de modificación del espacio de nombres no se genera cuando se produce algún tipo de cambio en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="98763-150">A namespace modification event is not generated when any kind of change occurs within the namespace.</span></span> <span data-ttu-id="98763-151">Un evento de modificación del espacio de nombres solo se genera cuando se modifica una instancia de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="98763-151">A namespace modification event is generated only when a namespace instance is modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="98763-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98763-152">Requirements</span></span>



| <span data-ttu-id="98763-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="98763-153">Requirement</span></span> | <span data-ttu-id="98763-154">Value</span><span class="sxs-lookup"><span data-stu-id="98763-154">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="98763-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98763-155">Minimum supported client</span></span><br/> | <span data-ttu-id="98763-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98763-156">Windows Vista</span></span><br/>       |
| <span data-ttu-id="98763-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98763-157">Minimum supported server</span></span><br/> | <span data-ttu-id="98763-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98763-158">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="98763-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="98763-159">Namespace</span></span><br/>                | <span data-ttu-id="98763-160">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="98763-160">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="98763-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="98763-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98763-162">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="98763-162">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="98763-163">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="98763-163">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

