---
description: Es una clase base para todos los eventos intrínsecos relacionados con una clase.
ms.assetid: 554bbabd-2639-40f5-8786-6df2188db0ec
ms.tgt_platform: multiple
title: __ClassOperationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0c7a78219cec5c014e289dad4bf1cc29f0466a06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707489"
---
# <a name="__classoperationevent-class"></a><span data-ttu-id="078c9-103">\_\_Clase ClassOperationEvent</span><span class="sxs-lookup"><span data-stu-id="078c9-103">\_\_ClassOperationEvent class</span></span>

<span data-ttu-id="078c9-104">La clase del sistema **\_ \_ ClassOperationEvent** es una clase base para todos los eventos intrínsecos relacionados con una clase.</span><span class="sxs-lookup"><span data-stu-id="078c9-104">The **\_\_ClassOperationEvent** system class is a base class for all intrinsic events that relate to a class.</span></span>

<span data-ttu-id="078c9-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="078c9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="078c9-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="078c9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="078c9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="078c9-107">Syntax</span></span>

``` syntax
class __ClassOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="078c9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="078c9-108">Members</span></span>

<span data-ttu-id="078c9-109">La clase **\_ \_ ClassOperationEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="078c9-109">The **\_\_ClassOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="078c9-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="078c9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="078c9-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="078c9-111">Properties</span></span>

<span data-ttu-id="078c9-112">La clase **\_ \_ ClassOperationEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="078c9-112">The **\_\_ClassOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="078c9-113">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="078c9-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078c9-114">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="078c9-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="078c9-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="078c9-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078c9-116">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="078c9-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="078c9-117">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="078c9-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="078c9-118">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="078c9-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078c9-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="078c9-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="078c9-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="078c9-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078c9-121">Clase afectada por el evento.</span><span class="sxs-lookup"><span data-stu-id="078c9-121">Class affected by the event.</span></span> <span data-ttu-id="078c9-122">En el caso de los eventos de creación, esta es la clase recién creada.</span><span class="sxs-lookup"><span data-stu-id="078c9-122">For creation events, this is the newly created class.</span></span> <span data-ttu-id="078c9-123">En el caso de los eventos de modificación, esta es la nueva versión de la clase modificada.</span><span class="sxs-lookup"><span data-stu-id="078c9-123">For modification events, this is the new version of the changed class.</span></span> <span data-ttu-id="078c9-124">En el caso de los eventos de eliminación, se trata de la clase eliminada.</span><span class="sxs-lookup"><span data-stu-id="078c9-124">For deletion events, this is the deleted class.</span></span>

</dd> <dt>

<span data-ttu-id="078c9-125">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="078c9-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078c9-126">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="078c9-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="078c9-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="078c9-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078c9-128">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="078c9-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="078c9-129">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="078c9-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="078c9-130">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="078c9-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="078c9-131">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="078c9-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="078c9-132">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="078c9-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="078c9-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="078c9-133">Remarks</span></span>

<span data-ttu-id="078c9-134">La clase **\_ \_ ClassOperationEvent** se deriva de [**\_ \_ Event**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="078c9-134">The **\_\_ClassOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="078c9-135">No se crean instancias de **\_ \_ ClassOperationEvent** ; solo se crean las instancias de sus subclases.</span><span class="sxs-lookup"><span data-stu-id="078c9-135">Instances of **\_\_ClassOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="078c9-136">Las siguientes clases se derivan de **\_ \_ ClassOperationEvent**:</span><span class="sxs-lookup"><span data-stu-id="078c9-136">The following classes derive from **\_\_ClassOperationEvent**:</span></span>

[<span data-ttu-id="078c9-137">**\_\_ClassCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="078c9-137">**\_\_ClassCreationEvent**</span></span>](--classcreationevent.md)

[<span data-ttu-id="078c9-138">**\_\_ClassModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="078c9-138">**\_\_ClassModificationEvent**</span></span>](--classmodificationevent.md)

[<span data-ttu-id="078c9-139">**\_\_ClassDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="078c9-139">**\_\_ClassDeletionEvent**</span></span>](--classdeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="078c9-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="078c9-140">Requirements</span></span>



| <span data-ttu-id="078c9-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="078c9-141">Requirement</span></span> | <span data-ttu-id="078c9-142">Value</span><span class="sxs-lookup"><span data-stu-id="078c9-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="078c9-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="078c9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="078c9-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="078c9-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="078c9-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="078c9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="078c9-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="078c9-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="078c9-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="078c9-147">Namespace</span></span><br/>                | <span data-ttu-id="078c9-148">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="078c9-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="078c9-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="078c9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="078c9-150">**\_\_Evento**</span><span class="sxs-lookup"><span data-stu-id="078c9-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="078c9-151">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="078c9-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="078c9-152">Determinar el tipo de evento que se va a recibir</span><span class="sxs-lookup"><span data-stu-id="078c9-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

