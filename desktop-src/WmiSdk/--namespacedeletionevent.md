---
description: Informa de un evento de eliminación de espacio de nombres, que es un tipo de evento intrínseco que se genera cuando se quita un subespacio de nombres del espacio de nombres actual.
ms.assetid: f7160a90-562d-40d9-9189-32aaabcd81d0
ms.tgt_platform: multiple
title: __NamespaceDeletionEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6e23f909718167760c02bbdb38e2a075d04bc516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649224"
---
# <a name="__namespacedeletionevent-class"></a><span data-ttu-id="decbd-103">\_\_Clase NamespaceDeletionEvent</span><span class="sxs-lookup"><span data-stu-id="decbd-103">\_\_NamespaceDeletionEvent class</span></span>

<span data-ttu-id="decbd-104">La clase del sistema **\_ \_ NamespaceDeletionEvent** informa de un evento de eliminación de espacio de nombres, que es un tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que se genera cuando se quita un subespacio de nombres del espacio de nombres actual.</span><span class="sxs-lookup"><span data-stu-id="decbd-104">The **\_\_NamespaceDeletionEvent** system class reports a namespace deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a sub-namespace is removed from the current namespace.</span></span>

<span data-ttu-id="decbd-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="decbd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="decbd-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="decbd-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="decbd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="decbd-107">Syntax</span></span>

``` syntax
class __NamespaceDeletionEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="decbd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="decbd-108">Members</span></span>

<span data-ttu-id="decbd-109">La clase **\_ \_ NamespaceDeletionEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="decbd-109">The **\_\_NamespaceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="decbd-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="decbd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="decbd-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="decbd-111">Properties</span></span>

<span data-ttu-id="decbd-112">La clase **\_ \_ NamespaceDeletionEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="decbd-112">The **\_\_NamespaceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="decbd-113">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="decbd-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="decbd-114">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="decbd-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="decbd-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="decbd-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="decbd-116">Descriptor que el proveedor de eventos utiliza para determinar los usuarios que pueden recibir un evento.</span><span class="sxs-lookup"><span data-stu-id="decbd-116">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="decbd-117">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="decbd-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="decbd-118">**TargetNamespace**</span><span class="sxs-lookup"><span data-stu-id="decbd-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="decbd-119">Tipo de datos: **\_ \_ espacio de nombres**</span><span class="sxs-lookup"><span data-stu-id="decbd-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="decbd-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="decbd-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="decbd-121">Copia de la instancia de [**\_ \_ espacio de nombres**](--namespace.md) que se elimina.</span><span class="sxs-lookup"><span data-stu-id="decbd-121">Copy of the [**\_\_Namespace**](--namespace.md) instance that is deleted.</span></span> <span data-ttu-id="decbd-122">La propiedad **Name** de la instancia de **\_ \_ espacio de nombres** identifica el espacio de nombres que se elimina.</span><span class="sxs-lookup"><span data-stu-id="decbd-122">The **Name** property of the **\_\_Namespace** instance identifies the namespace that is deleted.</span></span> <span data-ttu-id="decbd-123">Esta propiedad se hereda de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="decbd-123">This property is inherited from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="decbd-124">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="decbd-124">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="decbd-125">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="decbd-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="decbd-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="decbd-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="decbd-127">Valor único que indica la hora a la que se genera un evento.</span><span class="sxs-lookup"><span data-stu-id="decbd-127">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="decbd-128">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="decbd-128">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="decbd-129">La información tiene el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="decbd-129">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="decbd-130">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="decbd-130">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="decbd-131">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="decbd-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="decbd-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="decbd-132">Remarks</span></span>

<span data-ttu-id="decbd-133">La clase **\_ \_ NamespaceDeletionEvent** se deriva de [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="decbd-133">The **\_\_NamespaceDeletionEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="decbd-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="decbd-134">Requirements</span></span>



| <span data-ttu-id="decbd-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="decbd-135">Requirement</span></span> | <span data-ttu-id="decbd-136">Value</span><span class="sxs-lookup"><span data-stu-id="decbd-136">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="decbd-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="decbd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="decbd-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="decbd-138">Windows Vista</span></span><br/>       |
| <span data-ttu-id="decbd-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="decbd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="decbd-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="decbd-140">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="decbd-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="decbd-141">Namespace</span></span><br/>                | <span data-ttu-id="decbd-142">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="decbd-142">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="decbd-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="decbd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="decbd-144">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="decbd-144">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="decbd-145">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="decbd-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

