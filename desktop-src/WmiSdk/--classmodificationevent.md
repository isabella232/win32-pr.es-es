---
description: Representa un evento de modificación de clase, que es un tipo de evento intrínseco que se genera cuando se cambia una clase en el espacio de nombres.
ms.assetid: 77e8e025-d584-495d-98f8-71e7fb2c9698
ms.tgt_platform: multiple
title: __ClassModificationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 3634b632fa9ab66f0da3e48bf77fab5875daf12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706475"
---
# <a name="__classmodificationevent-class"></a><span data-ttu-id="8c762-103">\_\_Clase ClassModificationEvent</span><span class="sxs-lookup"><span data-stu-id="8c762-103">\_\_ClassModificationEvent class</span></span>

<span data-ttu-id="8c762-104">La clase del sistema **\_ \_ ClassModificationEvent** representa un evento de modificación de clase, que es un tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que se genera cuando se cambia una clase en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="8c762-104">The **\_\_ClassModificationEvent** system class represents a class modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a class is changed in the namespace.</span></span>

<span data-ttu-id="8c762-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8c762-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8c762-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="8c762-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c762-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c762-107">Syntax</span></span>

``` syntax
class __ClassModificationEvent : __ClassOperationEvent
{
  object PreviousClass;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="8c762-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c762-108">Members</span></span>

<span data-ttu-id="8c762-109">La clase **\_ \_ ClassModificationEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8c762-109">The **\_\_ClassModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="8c762-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c762-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c762-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c762-111">Properties</span></span>

<span data-ttu-id="8c762-112">La clase **\_ \_ ClassModificationEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8c762-112">The **\_\_ClassModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c762-113">**PreviousClass**</span><span class="sxs-lookup"><span data-stu-id="8c762-113">**PreviousClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c762-114">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="8c762-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8c762-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c762-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c762-116">Copia de la versión original de la clase.</span><span class="sxs-lookup"><span data-stu-id="8c762-116">Copy of the original version of the class.</span></span>

</dd> <dt>

<span data-ttu-id="8c762-117">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="8c762-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c762-118">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="8c762-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8c762-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c762-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c762-120">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="8c762-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="8c762-121">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="8c762-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c762-122">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="8c762-122">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c762-123">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="8c762-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8c762-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c762-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c762-125">Copia de la clase recién modificada indicada por el evento de modificación de clase.</span><span class="sxs-lookup"><span data-stu-id="8c762-125">Copy of the newly modified class reported by the class modification event.</span></span> <span data-ttu-id="8c762-126">Esta propiedad se hereda de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="8c762-126">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c762-127">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="8c762-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c762-128">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8c762-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8c762-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c762-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c762-130">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="8c762-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="8c762-131">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="8c762-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="8c762-132">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="8c762-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="8c762-133">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="8c762-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="8c762-134">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8c762-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c762-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c762-135">Remarks</span></span>

<span data-ttu-id="8c762-136">La clase **\_ \_ ClassModificationEvent** se deriva de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="8c762-136">The **\_\_ClassModificationEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="8c762-137">El evento informa de las versiones nuevas y antiguas de la definición de clase.</span><span class="sxs-lookup"><span data-stu-id="8c762-137">The event reports both the new and old versions of the class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c762-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c762-138">Requirements</span></span>



| <span data-ttu-id="8c762-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c762-139">Requirement</span></span> | <span data-ttu-id="8c762-140">Value</span><span class="sxs-lookup"><span data-stu-id="8c762-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8c762-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c762-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8c762-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c762-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8c762-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c762-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8c762-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c762-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8c762-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c762-145">Namespace</span></span><br/>                | <span data-ttu-id="8c762-146">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="8c762-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8c762-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c762-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c762-148">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="8c762-148">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="8c762-149">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="8c762-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

