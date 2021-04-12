---
description: Representa un evento del sistema.
ms.assetid: 84099483-03e4-4c21-b680-f0975b18c1f6
ms.tgt_platform: multiple
title: __SystemEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7cc443c9e130106c2f5e8a05a1a2983927f1963e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278213"
---
# <a name="__systemevent-class"></a><span data-ttu-id="d0972-103">\_\_Clase SystemEvent</span><span class="sxs-lookup"><span data-stu-id="d0972-103">\_\_SystemEvent class</span></span>

<span data-ttu-id="d0972-104">La clase del sistema **\_ \_ SystemEvent** representa un evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="d0972-104">The **\_\_SystemEvent** system class represents a system event.</span></span>

<span data-ttu-id="d0972-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d0972-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d0972-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d0972-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0972-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0972-107">Syntax</span></span>

``` syntax
class __SystemEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="d0972-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d0972-108">Members</span></span>

<span data-ttu-id="d0972-109">La clase **\_ \_ SystemEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d0972-109">The **\_\_SystemEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="d0972-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0972-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d0972-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0972-111">Properties</span></span>

<span data-ttu-id="d0972-112">La clase **\_ \_ SystemEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d0972-112">The **\_\_SystemEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0972-113">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="d0972-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0972-114">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="d0972-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d0972-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0972-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0972-116">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="d0972-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="d0972-117">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="d0972-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="d0972-118">Una lista de Access Controls **nulas** (ACL) en el [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acceso ilimitado a todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="d0972-118">A **NULL** Access Control List (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="d0972-119">Para obtener más información, vea [crear un descriptor de seguridad para un nuevo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="d0972-119">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="d0972-120">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="d0972-120">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0972-121">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d0972-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d0972-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0972-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0972-123">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="d0972-123">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="d0972-124">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="d0972-124">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="d0972-125">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="d0972-125">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="d0972-126">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="d0972-126">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="d0972-127">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d0972-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0972-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0972-128">Remarks</span></span>

<span data-ttu-id="d0972-129">La clase **\_ \_ SystemEvent** se deriva de la clase [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) .</span><span class="sxs-lookup"><span data-stu-id="d0972-129">The **\_\_SystemEvent** class is derived from the [**\_\_ExtrinsicEvent**](--extrinsicevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0972-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0972-130">Requirements</span></span>



| <span data-ttu-id="d0972-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0972-131">Requirement</span></span> | <span data-ttu-id="d0972-132">Value</span><span class="sxs-lookup"><span data-stu-id="d0972-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d0972-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0972-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d0972-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0972-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d0972-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0972-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d0972-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0972-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d0972-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d0972-137">Namespace</span></span><br/>                | <span data-ttu-id="d0972-138">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="d0972-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d0972-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0972-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0972-140">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="d0972-140">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

[<span data-ttu-id="d0972-141">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="d0972-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

