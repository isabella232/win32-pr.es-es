---
description: La clase WMIEvent es una clase base de la que se derivan todas las clases de eventos WMI.
ms.assetid: 0393d3fc-7566-4eda-940e-248d622a903a
title: Clase WMIEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIEvent
- WMIEvent.SECURITY_DESCRIPTOR
- WMIEvent.TIME_CREATED
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 99f6804ef1dad4f37bd2727da2e91e801fb0ece2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083216"
---
# <a name="wmievent-class"></a><span data-ttu-id="1d8b2-103">Clase WMIEvent</span><span class="sxs-lookup"><span data-stu-id="1d8b2-103">WMIEvent class</span></span>

<span data-ttu-id="1d8b2-104">La clase **WMIEvent** es una clase base de la que se derivan todas las clases de eventos WMI.</span><span class="sxs-lookup"><span data-stu-id="1d8b2-104">The **WMIEvent** class is a base class from which all WMI event classes are derived.</span></span>

<span data-ttu-id="1d8b2-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1d8b2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1d8b2-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1d8b2-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d8b2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d8b2-107">Syntax</span></span>

``` syntax
[]
class WMIEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="1d8b2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1d8b2-108">Members</span></span>

<span data-ttu-id="1d8b2-109">La clase **WMIEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1d8b2-109">The **WMIEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="1d8b2-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d8b2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d8b2-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d8b2-111">Properties</span></span>

<span data-ttu-id="1d8b2-112">La clase **WMIEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1d8b2-112">The **WMIEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d8b2-113">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="1d8b2-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d8b2-114">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="1d8b2-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1d8b2-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d8b2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d8b2-116">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="1d8b2-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="1d8b2-117">Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="1d8b2-117">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="1d8b2-118">Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="1d8b2-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="1d8b2-119">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="1d8b2-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d8b2-120">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d8b2-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d8b2-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1d8b2-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d8b2-122">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="1d8b2-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="1d8b2-123">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="1d8b2-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="1d8b2-124">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="1d8b2-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="1d8b2-125">Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="1d8b2-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="1d8b2-126">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d8b2-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d8b2-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d8b2-127">Remarks</span></span>

<span data-ttu-id="1d8b2-128">La clase **WMIEvent** se deriva de [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span><span class="sxs-lookup"><span data-stu-id="1d8b2-128">The **WMIEvent** class is derived from [**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d8b2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d8b2-129">Requirements</span></span>



| <span data-ttu-id="1d8b2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d8b2-130">Requirement</span></span> | <span data-ttu-id="1d8b2-131">Value</span><span class="sxs-lookup"><span data-stu-id="1d8b2-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d8b2-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d8b2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1d8b2-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d8b2-133">Windows Vista</span></span><br/>                                                                                                                              |
| <span data-ttu-id="1d8b2-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d8b2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1d8b2-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1d8b2-135">Windows Server 2003</span></span><br/>                                                                                                                        |
| <span data-ttu-id="1d8b2-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1d8b2-136">Namespace</span></span><br/>                | <span data-ttu-id="1d8b2-137">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="1d8b2-137">Root\\WMI</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="1d8b2-138">MOF</span><span class="sxs-lookup"><span data-stu-id="1d8b2-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d8b2-139"><dt>WMI. mof; </dt> <dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d8b2-139"><dt>Wmi.mof; </dt> <dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d8b2-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d8b2-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d8b2-141"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d8b2-141"><dt>WmiProv.dll</dt></span></span> </dl>                                                                |



## <a name="see-also"></a><span data-ttu-id="1d8b2-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d8b2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d8b2-143">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="1d8b2-143">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="1d8b2-144">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="1d8b2-144">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

