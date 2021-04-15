---
description: Una clase base para todos los eventos intrínsecos relacionados con un espacio de nombres.
ms.assetid: 168637b1-217e-4b6d-bd07-25127b9e9f6c
ms.tgt_platform: multiple
title: __NamespaceOperationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: d263af0eab5fc3899b45659bc8409a5e68776fe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649223"
---
# <a name="__namespaceoperationevent-class"></a><span data-ttu-id="171e4-103">\_\_Clase NamespaceOperationEvent</span><span class="sxs-lookup"><span data-stu-id="171e4-103">\_\_NamespaceOperationEvent class</span></span>

<span data-ttu-id="171e4-104">La clase del sistema **\_ \_ NamespaceOperationEvent** es una clase base para todos los eventos intrínsecos relacionados con un espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="171e4-104">The **\_\_NamespaceOperationEvent** system class is a base class for all intrinsic events that relate to a namespace.</span></span>

<span data-ttu-id="171e4-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="171e4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="171e4-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="171e4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="171e4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="171e4-107">Syntax</span></span>

``` syntax
class __NamespaceOperationEvent : __Event
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="171e4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="171e4-108">Members</span></span>

<span data-ttu-id="171e4-109">La clase **\_ \_ NamespaceOperationEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="171e4-109">The **\_\_NamespaceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="171e4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="171e4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="171e4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="171e4-111">Properties</span></span>

<span data-ttu-id="171e4-112">La clase **\_ \_ NamespaceOperationEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="171e4-112">The **\_\_NamespaceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="171e4-113">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="171e4-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="171e4-114">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="171e4-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="171e4-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="171e4-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="171e4-116">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="171e4-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="171e4-117">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="171e4-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="171e4-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="171e4-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="171e4-119">Tipo de datos: **\_ \_ espacio de nombres**</span><span class="sxs-lookup"><span data-stu-id="171e4-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="171e4-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="171e4-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="171e4-121">Espacio de nombres afectado por el evento.</span><span class="sxs-lookup"><span data-stu-id="171e4-121">Namespace affected by the event.</span></span> <span data-ttu-id="171e4-122">En el caso de los eventos de creación, es el espacio de nombres recién creado.</span><span class="sxs-lookup"><span data-stu-id="171e4-122">For creation events, this is the newly created namespace.</span></span> <span data-ttu-id="171e4-123">En el caso de los eventos de modificación, este es el espacio de nombres cambiado.</span><span class="sxs-lookup"><span data-stu-id="171e4-123">For modification events, this is the changed namespace.</span></span> <span data-ttu-id="171e4-124">En el caso de los eventos de eliminación, es el espacio de nombres eliminado.</span><span class="sxs-lookup"><span data-stu-id="171e4-124">For deletion events, this is the deleted namespace.</span></span>

</dd> <dt>

<span data-ttu-id="171e4-125">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="171e4-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="171e4-126">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="171e4-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="171e4-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="171e4-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="171e4-128">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="171e4-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="171e4-129">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="171e4-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="171e4-130">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="171e4-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="171e4-131">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="171e4-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="171e4-132">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="171e4-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="171e4-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="171e4-133">Remarks</span></span>

<span data-ttu-id="171e4-134">La clase **\_ \_ NamespaceOperationEvent** se deriva de [**\_ \_ Event**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="171e4-134">The **\_\_NamespaceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="171e4-135">No se crean instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="171e4-135">Instances of this class are not created.</span></span> <span data-ttu-id="171e4-136">WMI crea instancias de una de las siguientes clases derivadas de esta clase:</span><span class="sxs-lookup"><span data-stu-id="171e4-136">WMI creates instances of one of the following classes derived from this class:</span></span>

[<span data-ttu-id="171e4-137">**\_\_NamespaceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="171e4-137">**\_\_NamespaceCreationEvent**</span></span>](--namespacecreationevent.md)

[<span data-ttu-id="171e4-138">**\_\_NamespaceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="171e4-138">**\_\_NamespaceModificationEvent**</span></span>](--namespacemodificationevent.md)

[<span data-ttu-id="171e4-139">**\_\_NamespaceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="171e4-139">**\_\_NamespaceDeletionEvent**</span></span>](--namespacedeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="171e4-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="171e4-140">Requirements</span></span>



| <span data-ttu-id="171e4-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="171e4-141">Requirement</span></span> | <span data-ttu-id="171e4-142">Value</span><span class="sxs-lookup"><span data-stu-id="171e4-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="171e4-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="171e4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="171e4-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="171e4-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="171e4-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="171e4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="171e4-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="171e4-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="171e4-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="171e4-147">Namespace</span></span><br/>                | <span data-ttu-id="171e4-148">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="171e4-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="171e4-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="171e4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="171e4-150">**\_\_Evento**</span><span class="sxs-lookup"><span data-stu-id="171e4-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="171e4-151">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="171e4-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="171e4-152">Determinar el tipo de evento que se va a recibir</span><span class="sxs-lookup"><span data-stu-id="171e4-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

