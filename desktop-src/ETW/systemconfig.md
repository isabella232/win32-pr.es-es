---
description: Esta clase es la clase primaria para los eventos de configuración de hardware. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 720c2366-bd68-4895-bfaf-74aa9b64ba4a
title: Clase SystemConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3332d396005deb2fb811d101a99827544ebc6df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913906"
---
# <a name="systemconfig-class"></a><span data-ttu-id="78384-104">Clase SystemConfig</span><span class="sxs-lookup"><span data-stu-id="78384-104">SystemConfig class</span></span>

<span data-ttu-id="78384-105">Esta clase es la clase primaria para los eventos de configuración de hardware.</span><span class="sxs-lookup"><span data-stu-id="78384-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="78384-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="78384-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="78384-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78384-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="78384-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="78384-108">Members</span></span>

<span data-ttu-id="78384-109">La clase **SystemConfig** no define ningún miembro.</span><span class="sxs-lookup"><span data-stu-id="78384-109">The **SystemConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="78384-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78384-110">Remarks</span></span>

<span data-ttu-id="78384-111">Estos eventos proporcionan la configuración de hardware del equipo.</span><span class="sxs-lookup"><span data-stu-id="78384-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="78384-112">A diferencia de otros eventos del registrador del kernel de NT, la sesión del kernel genera automáticamente eventos de configuración de hardware; No habilite estos eventos al iniciar la sesión del registrador del kernel de NT.</span><span class="sxs-lookup"><span data-stu-id="78384-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="78384-113">Para los eventos de configuración de hardware en Windows XP, vea la clase [HWConfig](hwconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="78384-113">For hardware configuration events on Windows XP, see the [HWConfig](hwconfig.md) class.</span></span>

<span data-ttu-id="78384-114">Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de configuración de hardware llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="78384-114">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="78384-115">Utilice los siguientes tipos de eventos para identificar el evento de configuración de hardware real al consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="78384-115">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="78384-116">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="78384-116">Event type</span></span>                                                                      | <span data-ttu-id="78384-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="78384-117">Description</span></span>                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78384-118">**Evento \_ de TRACE \_ Type \_ config \_ CPU**(el valor de tipo de evento es 10)</span><span class="sxs-lookup"><span data-stu-id="78384-118">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="78384-119">Evento de configuración de CPU.</span><span class="sxs-lookup"><span data-stu-id="78384-119">CPU configuration event.</span></span> <span data-ttu-id="78384-120">Las clases MOF de [**SystemConfig \_ CPU**](systemconfig-cpu.md) definen los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="78384-120">The [**SystemConfig\_CPU**](systemconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="78384-121">**Evento \_ de TRACE \_ Type \_ config \_ IDECHANNEL**(el valor de tipo de evento es 23)</span><span class="sxs-lookup"><span data-stu-id="78384-121">**EVENT\_TRACE\_TYPE\_CONFIG\_IDECHANNEL**(Event type value is 23)</span></span><br/>   | <span data-ttu-id="78384-122">Evento de configuración de canal IDE principal y secundario.</span><span class="sxs-lookup"><span data-stu-id="78384-122">Primary and secondary IDE channel configuration event.</span></span> <span data-ttu-id="78384-123">La clase MOF de las clases MOF de [**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="78384-123">The [**SystemConfig\_IDEChannel**](systemconfig-idechannel.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="78384-124">**Evento \_ de TRACE \_ Type \_ config \_ IRQ**(el valor de tipo de evento es 21)</span><span class="sxs-lookup"><span data-stu-id="78384-124">**EVENT\_TRACE\_TYPE\_CONFIG\_IRQ**(Event type value is 21)</span></span><br/>          | <span data-ttu-id="78384-125">Evento de solicitud de interrupción (IRQ).</span><span class="sxs-lookup"><span data-stu-id="78384-125">Interrupt request (IRQ) event.</span></span> <span data-ttu-id="78384-126">La clase MOF [**SystemConfig \_ IRQ**](systemconfig-irq.md) de las clases mof define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="78384-126">The [**SystemConfig\_IRQ**](systemconfig-irq.md) MOF classes MOF class defines the event data for this event.</span></span>                                       |
| <span data-ttu-id="78384-127">**Evento \_ de Tipo de seguimiento \_ \_ configuración de \_ LOGICALDISK**(el valor de tipo de evento es 12)</span><span class="sxs-lookup"><span data-stu-id="78384-127">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="78384-128">Evento de configuración de disco lógico.</span><span class="sxs-lookup"><span data-stu-id="78384-128">Logical disk configuration event.</span></span> <span data-ttu-id="78384-129">La clase MOF de las clases MOF de [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="78384-129">The [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span>                            |
| <span data-ttu-id="78384-130">**Evento \_ de TRACE \_ Type \_ config \_ NETINFO**(el valor de tipo de evento es 17)</span><span class="sxs-lookup"><span data-stu-id="78384-130">**EVENT\_TRACE\_TYPE\_CONFIG\_NETINFO**(Event type value is 17)</span></span><br/>      | <span data-ttu-id="78384-131">Evento iformation de red.</span><span class="sxs-lookup"><span data-stu-id="78384-131">Network iformation event.</span></span> <span data-ttu-id="78384-132">La clase MOF de [**\_ red SystemConfig**](systemconfig-network.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="78384-132">The [**SystemConfig\_Network**](systemconfig-network.md) MOF class defines the event data for this event.</span></span>                                                |
| <span data-ttu-id="78384-133">**Evento \_ de Tipo de seguimiento \_ \_ config de \_ NIC**(el valor de tipo de evento es 13)</span><span class="sxs-lookup"><span data-stu-id="78384-133">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="78384-134">Evento de configuración de NIC.</span><span class="sxs-lookup"><span data-stu-id="78384-134">NIC configuration event.</span></span> <span data-ttu-id="78384-135">Las clases MOF de la [**\_ NIC SystemConfig**](systemconfig-nic.md) definen los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="78384-135">The [**SystemConfig\_NIC**](systemconfig-nic.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="78384-136">**Evento \_ de Tipo de seguimiento \_ \_ configuración de \_ DiscoFísico**(el valor de tipo de evento es 11)</span><span class="sxs-lookup"><span data-stu-id="78384-136">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="78384-137">Evento de configuración de disco físico.</span><span class="sxs-lookup"><span data-stu-id="78384-137">Physical disk configuration event.</span></span> <span data-ttu-id="78384-138">Las clases MOF de [**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md) definen los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="78384-138">The [**SystemConfig\_PhyDisk**](systemconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>                                     |
| <span data-ttu-id="78384-139">**Evento \_ de Configuración de tipo de seguimiento \_ \_ \_ PNP**(el valor de tipo de evento es 22)</span><span class="sxs-lookup"><span data-stu-id="78384-139">**EVENT\_TRACE\_TYPE\_CONFIG\_PNP**(Event type value is 22)</span></span><br/>          | <span data-ttu-id="78384-140">Evento plug and Play.</span><span class="sxs-lookup"><span data-stu-id="78384-140">Plug and play event.</span></span> <span data-ttu-id="78384-141">La clase MOF de las clases MOF [**SystemConfig \_ PNP**](systemconfig-pnp.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="78384-141">The [**SystemConfig\_PNP**](systemconfig-pnp.md) MOF classes MOF class defines the event data for this event.</span></span>                                                 |
| <span data-ttu-id="78384-142">**Evento \_ de TRACE \_ Type \_ config \_ Power**(el valor del tipo de evento es 16)</span><span class="sxs-lookup"><span data-stu-id="78384-142">**EVENT\_TRACE\_TYPE\_CONFIG\_POWER**(Event type value is 16)</span></span><br/>        | <span data-ttu-id="78384-143">Evento de configuración de energía.</span><span class="sxs-lookup"><span data-stu-id="78384-143">Power configuration event.</span></span> <span data-ttu-id="78384-144">La clase [**SystemConfig \_ Power**](systemconfig-power.md) mof define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="78384-144">The [**SystemConfig\_Power**](systemconfig-power.md) MOF class defines the event data for this event.</span></span>                                                   |
| <span data-ttu-id="78384-145">**Evento \_ de Tipo de seguimiento de \_ \_ \_ servicios de configuración**(el valor de tipo de evento es 15)</span><span class="sxs-lookup"><span data-stu-id="78384-145">**EVENT\_TRACE\_TYPE\_CONFIG\_SERVICES**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="78384-146">Evento de configuración de servicios.</span><span class="sxs-lookup"><span data-stu-id="78384-146">Services configuration event.</span></span> <span data-ttu-id="78384-147">La clase MOF de [**SystemConfig \_ Services**](systemconfig-services.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="78384-147">The [**SystemConfig\_Services**](systemconfig-services.md) MOF class defines the event data for this event.</span></span>                                          |
| <span data-ttu-id="78384-148">**Evento \_ de TRACE \_ Type \_ config \_ video**(valor de tipo de evento es 14)</span><span class="sxs-lookup"><span data-stu-id="78384-148">**EVENT\_TRACE\_TYPE\_CONFIG\_VIDEO**(Event type value is 14)</span></span><br/>        | <span data-ttu-id="78384-149">Evento de configuración del adaptador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="78384-149">Graphics adapter configuration event.</span></span> <span data-ttu-id="78384-150">La clase MOF de [**\_ vídeo SystemConfig**](systemconfig-video.md) define los datos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="78384-150">The [**SystemConfig\_Video**](systemconfig-video.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="78384-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78384-151">Requirements</span></span>



| <span data-ttu-id="78384-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="78384-152">Requirement</span></span> | <span data-ttu-id="78384-153">Value</span><span class="sxs-lookup"><span data-stu-id="78384-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78384-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78384-154">Minimum supported client</span></span><br/> | <span data-ttu-id="78384-155">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="78384-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="78384-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78384-156">Minimum supported server</span></span><br/> | <span data-ttu-id="78384-157">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="78384-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78384-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="78384-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78384-159">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="78384-159">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="78384-160">**\_CPU SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="78384-160">**SystemConfig\_CPU**</span></span>](systemconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="78384-161">**SystemConfig \_ IDEChannel**</span><span class="sxs-lookup"><span data-stu-id="78384-161">**SystemConfig\_IDEChannel**</span></span>](systemconfig-idechannel.md)
</dt> <dt>

[<span data-ttu-id="78384-162">**SystemConfig \_ IRQ**</span><span class="sxs-lookup"><span data-stu-id="78384-162">**SystemConfig\_IRQ**</span></span>](systemconfig-irq.md)
</dt> <dt>

[<span data-ttu-id="78384-163">**SystemConfig \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="78384-163">**SystemConfig\_LogDisk**</span></span>](systemconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="78384-164">**\_Red SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="78384-164">**SystemConfig\_Network**</span></span>](systemconfig-network.md)
</dt> <dt>

[<span data-ttu-id="78384-165">**NIC de SystemConfig \_**</span><span class="sxs-lookup"><span data-stu-id="78384-165">**SystemConfig\_NIC**</span></span>](systemconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="78384-166">**SystemConfig \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="78384-166">**SystemConfig\_PhyDisk**</span></span>](systemconfig-phydisk.md)
</dt> <dt>

[<span data-ttu-id="78384-167">**SystemConfig \_ PNP**</span><span class="sxs-lookup"><span data-stu-id="78384-167">**SystemConfig\_PNP**</span></span>](systemconfig-pnp.md)
</dt> <dt>

[<span data-ttu-id="78384-168">**Alimentación de SystemConfig \_**</span><span class="sxs-lookup"><span data-stu-id="78384-168">**SystemConfig\_Power**</span></span>](systemconfig-power.md)
</dt> <dt>

[<span data-ttu-id="78384-169">**Servicios de SystemConfig \_**</span><span class="sxs-lookup"><span data-stu-id="78384-169">**SystemConfig\_Services**</span></span>](systemconfig-services.md)
</dt> <dt>

[<span data-ttu-id="78384-170">**Vídeo de SystemConfig \_**</span><span class="sxs-lookup"><span data-stu-id="78384-170">**SystemConfig\_Video**</span></span>](systemconfig-video.md)
</dt> <dt>

[<span data-ttu-id="78384-171">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="78384-171">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 
