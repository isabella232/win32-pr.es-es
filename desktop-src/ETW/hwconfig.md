---
description: La clase HWConfig es la clase primaria para los eventos de configuración de hardware en Windows XP. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: Clase HWConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: cfb194e09701dbc52b00279b624877f09ffac24b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913537"
---
# <a name="hwconfig-class"></a><span data-ttu-id="ab593-104">Clase HWConfig</span><span class="sxs-lookup"><span data-stu-id="ab593-104">HWConfig class</span></span>

<span data-ttu-id="ab593-105">La clase **HWConfig** es la clase primaria para los eventos de configuración de hardware en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab593-105">The **HWConfig** class is the parent class for hardware configuration events on Windows XP.</span></span>

<span data-ttu-id="ab593-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="ab593-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab593-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab593-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="ab593-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ab593-108">Members</span></span>

<span data-ttu-id="ab593-109">La clase **HWConfig** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="ab593-109">The **HWConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab593-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab593-110">Remarks</span></span>

<span data-ttu-id="ab593-111">Estos eventos proporcionan la configuración de hardware del equipo.</span><span class="sxs-lookup"><span data-stu-id="ab593-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="ab593-112">A diferencia de otros eventos del registrador del kernel de NT, la sesión del kernel genera automáticamente eventos de configuración de hardware; No habilite estos eventos al iniciar la sesión del registrador del kernel de NT.</span><span class="sxs-lookup"><span data-stu-id="ab593-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="ab593-113">**Windows 2000:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="ab593-113">**Windows 2000:** Not supported.</span></span>

<span data-ttu-id="ab593-114">Para los eventos de configuración de hardware en Windows Vista y Windows Server 2003, vea la clase [SystemConfig](systemconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="ab593-114">For hardware configuration events on Windows Vista and Windows Server 2003, see the [SystemConfig](systemconfig.md) class.</span></span>

<span data-ttu-id="ab593-115">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de configuración de hardware llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="ab593-115">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="ab593-116">Utilice los siguientes tipos de eventos para identificar el evento de configuración de hardware real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="ab593-116">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="ab593-117">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="ab593-117">Event type</span></span>                                                                      | <span data-ttu-id="ab593-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab593-118">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab593-119">**Evento \_ de TRACE \_ Type \_ config \_ CPU**(el valor de tipo de evento es 10)</span><span class="sxs-lookup"><span data-stu-id="ab593-119">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="ab593-120">Evento de configuración de CPU.</span><span class="sxs-lookup"><span data-stu-id="ab593-120">CPU configuration event.</span></span> <span data-ttu-id="ab593-121">Las clases MOF de [**HWConfig \_ CPU**](hwconfig-cpu.md) definen los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="ab593-121">The [**HWConfig\_CPU**](hwconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="ab593-122">**Evento \_ de Tipo de seguimiento \_ \_ configuración de \_ LOGICALDISK**(el valor de tipo de evento es 12)</span><span class="sxs-lookup"><span data-stu-id="ab593-122">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="ab593-123">Evento de configuración de disco lógico.</span><span class="sxs-lookup"><span data-stu-id="ab593-123">Logical disk configuration event.</span></span> <span data-ttu-id="ab593-124">La clase MOF de las clases MOF de [**HWConfig \_ LogDisk**](hwconfig-logdisk.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="ab593-124">The [**HWConfig\_LogDisk**](hwconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="ab593-125">**Evento \_ de Tipo de seguimiento \_ \_ config de \_ NIC**(el valor de tipo de evento es 13)</span><span class="sxs-lookup"><span data-stu-id="ab593-125">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="ab593-126">Evento de configuración de NIC.</span><span class="sxs-lookup"><span data-stu-id="ab593-126">NIC configuration event.</span></span> <span data-ttu-id="ab593-127">Las clases MOF de la [**\_ NIC HWConfig**](hwconfig-nic.md) definen los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="ab593-127">The [**HWConfig\_NIC**](hwconfig-nic.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="ab593-128">**Evento \_ de Tipo de seguimiento \_ \_ configuración de \_ DiscoFísico**(el valor de tipo de evento es 11)</span><span class="sxs-lookup"><span data-stu-id="ab593-128">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="ab593-129">Evento de configuración de disco físico.</span><span class="sxs-lookup"><span data-stu-id="ab593-129">Physical disk configuration event.</span></span> <span data-ttu-id="ab593-130">Las clases MOF de [**HWConfig \_ PhyDisk**](hwconfig-phydisk.md) definen los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="ab593-130">The [**HWConfig\_PhyDisk**](hwconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="ab593-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab593-131">Requirements</span></span>



| <span data-ttu-id="ab593-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab593-132">Requirement</span></span> | <span data-ttu-id="ab593-133">Value</span><span class="sxs-lookup"><span data-stu-id="ab593-133">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="ab593-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab593-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ab593-135">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ab593-135">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ab593-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab593-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ab593-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ab593-137">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="ab593-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab593-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab593-139">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="ab593-139">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="ab593-140">**\_CPU HWConfig**</span><span class="sxs-lookup"><span data-stu-id="ab593-140">**HWConfig\_CPU**</span></span>](hwconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="ab593-141">**HWConfig \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="ab593-141">**HWConfig\_LogDisk**</span></span>](hwconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="ab593-142">**NIC de HWConfig \_**</span><span class="sxs-lookup"><span data-stu-id="ab593-142">**HWConfig\_NIC**</span></span>](hwconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="ab593-143">**HWConfig \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="ab593-143">**HWConfig\_PhyDisk**</span></span>](hwconfig-phydisk.md)
</dt> </dl>

 

 
