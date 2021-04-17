---
description: Es una clase base abstracta que actúa como la clase primaria para todos los eventos intrínsecos y extrínsecos.
ms.assetid: 4d2e4715-041c-49e9-b948-a148dfe85483
ms.tgt_platform: multiple
title: __Event (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Event
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 39a032b3f082ed64ba7999d20366b89e8b3890c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707414"
---
# <a name="__event-class"></a><span data-ttu-id="1a63b-103">\_\_Event (clase)</span><span class="sxs-lookup"><span data-stu-id="1a63b-103">\_\_Event class</span></span>

<span data-ttu-id="1a63b-104">La clase de sistema de **\_ \_ eventos** es una clase base abstracta que actúa como la clase primaria para todos los eventos intrínsecos y extrínsecos.</span><span class="sxs-lookup"><span data-stu-id="1a63b-104">The **\_\_Event** system class is an abstract base class that serves as the parent class for all intrinsic and extrinsic events.</span></span> <span data-ttu-id="1a63b-105">Todos los tipos de eventos nuevos deben derivarse en última instancia del **\_ \_ evento**.</span><span class="sxs-lookup"><span data-stu-id="1a63b-105">All new event types must ultimately derive from **\_\_Event**.</span></span> <span data-ttu-id="1a63b-106">Los eventos intrínsecos se derivan directamente de esta clase.</span><span class="sxs-lookup"><span data-stu-id="1a63b-106">Intrinsic events derive directly from this class.</span></span> <span data-ttu-id="1a63b-107">Los eventos extrínsecos definidos por el usuario se derivan de una subclase de esta clase llamada [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="1a63b-107">User-defined extrinsic events derive from a subclass of this class called [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span>

<span data-ttu-id="1a63b-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1a63b-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1a63b-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1a63b-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a63b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a63b-110">Syntax</span></span>

``` syntax
[abstract]
class __Event : __IndicationRelated
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="1a63b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="1a63b-111">Members</span></span>

<span data-ttu-id="1a63b-112">La clase de **\_ \_ eventos** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1a63b-112">The **\_\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="1a63b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a63b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a63b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a63b-114">Properties</span></span>

<span data-ttu-id="1a63b-115">La clase de **\_ \_ eventos** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1a63b-115">The **\_\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a63b-116">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="1a63b-116">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a63b-117">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="1a63b-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1a63b-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a63b-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a63b-119">Descriptor que utiliza el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="1a63b-119">Descriptor that the event provider uses to determine which users can receive the event.</span></span> <span data-ttu-id="1a63b-120">Para obtener más información, vea [constantes de seguridad de WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1a63b-120">For more information, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a63b-121">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="1a63b-121">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a63b-122">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1a63b-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1a63b-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a63b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a63b-124">Valor único que indica la hora a la que se genera el evento.</span><span class="sxs-lookup"><span data-stu-id="1a63b-124">Unique value that indicates the time the event is generated.</span></span> <span data-ttu-id="1a63b-125">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="1a63b-125">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="1a63b-126">La información tiene el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="1a63b-126">The information is in the Coordinated Universal Time (UTC) format.</span></span>

<span data-ttu-id="1a63b-127">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1a63b-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a63b-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a63b-128">Remarks</span></span>

<span data-ttu-id="1a63b-129">La clase de **\_ \_ eventos** se deriva de [**\_ \_ IndicationRelated**](--indicationrelated.md), que no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="1a63b-129">The **\_\_Event** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a63b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a63b-130">Requirements</span></span>



| <span data-ttu-id="1a63b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a63b-131">Requirement</span></span> | <span data-ttu-id="1a63b-132">Value</span><span class="sxs-lookup"><span data-stu-id="1a63b-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1a63b-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a63b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1a63b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a63b-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1a63b-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a63b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1a63b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a63b-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1a63b-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1a63b-137">Namespace</span></span><br/>                | <span data-ttu-id="1a63b-138">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="1a63b-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="1a63b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a63b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a63b-140">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="1a63b-140">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="1a63b-141">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="1a63b-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="1a63b-142">Determinar el tipo de evento que se va a recibir</span><span class="sxs-lookup"><span data-stu-id="1a63b-142">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="1a63b-143">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="1a63b-143">**\_\_ClassOperationEvent**</span></span>](--classoperationevent.md)
</dt> <dt>

[<span data-ttu-id="1a63b-144">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="1a63b-144">**\_\_InstanceOperationEvent**</span></span>](--instanceoperationevent.md)
</dt> <dt>

[<span data-ttu-id="1a63b-145">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="1a63b-145">**\_\_NamespaceOperationEvent**</span></span>](--namespaceoperationevent.md)
</dt> </dl>

 

