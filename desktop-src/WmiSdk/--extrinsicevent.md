---
description: Actúa como clase primaria para todos los tipos de eventos definidos por el usuario, también conocidos como eventos extrínsecos.
ms.assetid: 8fddbcd1-7393-4a3b-8a10-a8b620efc19f
ms.tgt_platform: multiple
title: __ExtrinsicEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtrinsicEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 76af7a9f32c24b8d44f81c60b0f2fca693c26f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278782"
---
# <a name="__extrinsicevent-class"></a><span data-ttu-id="996b7-103">\_\_Clase ExtrinsicEvent</span><span class="sxs-lookup"><span data-stu-id="996b7-103">\_\_ExtrinsicEvent class</span></span>

<span data-ttu-id="996b7-104">La clase del sistema **\_ \_ ExtrinsicEvent** es una clase base abstracta que actúa como clase primaria para todos los tipos de eventos definidos por el usuario, también conocidos como [eventos extrínsecos](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="996b7-104">The **\_\_ExtrinsicEvent** system class is an abstract base class that serves as a parent class for all user-defined event types, also known as [extrinsic events](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="996b7-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="996b7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="996b7-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="996b7-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="996b7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="996b7-107">Syntax</span></span>

``` syntax
class __ExtrinsicEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="996b7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="996b7-108">Members</span></span>

<span data-ttu-id="996b7-109">La clase **\_ \_ ExtrinsicEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="996b7-109">The **\_\_ExtrinsicEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="996b7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="996b7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="996b7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="996b7-111">Properties</span></span>

<span data-ttu-id="996b7-112">La clase **\_ \_ ExtrinsicEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="996b7-112">The **\_\_ExtrinsicEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="996b7-113">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="996b7-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="996b7-114">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="996b7-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="996b7-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="996b7-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="996b7-116">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="996b7-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="996b7-117">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="996b7-117">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="996b7-118">Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="996b7-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="996b7-119">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="996b7-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="996b7-120">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="996b7-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="996b7-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="996b7-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="996b7-122">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="996b7-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="996b7-123">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="996b7-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="996b7-124">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="996b7-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="996b7-125">Esta propiedad se hereda del [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="996b7-125">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="996b7-126">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="996b7-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="996b7-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="996b7-127">Remarks</span></span>

<span data-ttu-id="996b7-128">La clase **\_ \_ ExtrinsicEvent** se deriva de [**\_ \_ Event**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="996b7-128">The **\_\_ExtrinsicEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="996b7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="996b7-129">Requirements</span></span>



| <span data-ttu-id="996b7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="996b7-130">Requirement</span></span> | <span data-ttu-id="996b7-131">Value</span><span class="sxs-lookup"><span data-stu-id="996b7-131">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="996b7-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="996b7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="996b7-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="996b7-133">Windows Vista</span></span><br/>       |
| <span data-ttu-id="996b7-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="996b7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="996b7-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="996b7-135">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="996b7-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="996b7-136">Namespace</span></span><br/>                | <span data-ttu-id="996b7-137">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="996b7-137">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="996b7-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="996b7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="996b7-139">**\_\_Evento**</span><span class="sxs-lookup"><span data-stu-id="996b7-139">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="996b7-140">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="996b7-140">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

