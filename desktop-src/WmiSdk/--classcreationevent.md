---
description: Representa un evento de creación de clase, que es un tipo de evento intrínseco que se genera cuando se agrega una nueva clase al espacio de nombres.
ms.assetid: a946a8eb-498c-4104-b80f-e520b0e62e36
ms.tgt_platform: multiple
title: __ClassCreationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 18994ee7067e44a9199de9b62f7ff278a8bece00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706477"
---
# <a name="__classcreationevent-class"></a><span data-ttu-id="c4bd1-103">\_\_Clase ClassCreationEvent</span><span class="sxs-lookup"><span data-stu-id="c4bd1-103">\_\_ClassCreationEvent class</span></span>

<span data-ttu-id="c4bd1-104">La clase del sistema **\_ \_ ClassCreationEvent** representa un evento de creación de clase, que es un tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que se genera cuando se agrega una nueva clase al espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="c4bd1-104">The **\_\_ClassCreationEvent** system class represents a class creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a new class is added to the namespace.</span></span>

<span data-ttu-id="c4bd1-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c4bd1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c4bd1-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c4bd1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4bd1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4bd1-107">Syntax</span></span>

``` syntax
class __ClassCreationEvent : __ClassOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="c4bd1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c4bd1-108">Members</span></span>

<span data-ttu-id="c4bd1-109">La clase **\_ \_ ClassCreationEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c4bd1-109">The **\_\_ClassCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="c4bd1-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c4bd1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4bd1-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c4bd1-111">Properties</span></span>

<span data-ttu-id="c4bd1-112">La clase **\_ \_ ClassCreationEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c4bd1-112">The **\_\_ClassCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4bd1-113">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="c4bd1-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4bd1-114">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="c4bd1-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c4bd1-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4bd1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4bd1-116">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="c4bd1-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="c4bd1-117">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="c4bd1-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4bd1-118">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="c4bd1-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4bd1-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="c4bd1-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c4bd1-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4bd1-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4bd1-121">Copia de la clase recién creada que se muestra en el evento de creación de clases.</span><span class="sxs-lookup"><span data-stu-id="c4bd1-121">Copy of the newly created class reported by the class creation event.</span></span> <span data-ttu-id="c4bd1-122">Esta propiedad se hereda de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="c4bd1-122">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4bd1-123">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="c4bd1-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4bd1-124">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4bd1-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4bd1-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4bd1-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4bd1-126">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="c4bd1-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="c4bd1-127">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="c4bd1-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="c4bd1-128">La información está en el formato de coordenadas de hora universal (UTC).</span><span class="sxs-lookup"><span data-stu-id="c4bd1-128">The information is in the Universal Time Coordinates (UTC) format.</span></span> <span data-ttu-id="c4bd1-129">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="c4bd1-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="c4bd1-130">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c4bd1-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4bd1-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4bd1-131">Remarks</span></span>

<span data-ttu-id="c4bd1-132">La clase **\_ \_ ClassCreationEvent** se deriva de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="c4bd1-132">The **\_\_ClassCreationEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4bd1-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4bd1-133">Requirements</span></span>



| <span data-ttu-id="c4bd1-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4bd1-134">Requirement</span></span> | <span data-ttu-id="c4bd1-135">Value</span><span class="sxs-lookup"><span data-stu-id="c4bd1-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c4bd1-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4bd1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c4bd1-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4bd1-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c4bd1-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4bd1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c4bd1-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4bd1-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c4bd1-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c4bd1-140">Namespace</span></span><br/>                | <span data-ttu-id="c4bd1-141">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="c4bd1-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c4bd1-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4bd1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4bd1-143">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="c4bd1-143">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="c4bd1-144">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="c4bd1-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

