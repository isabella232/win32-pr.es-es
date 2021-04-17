---
description: Las \_ constantes de marcador de bits LINEFORWARDMODE describen las condiciones en las que se pueden reenviar las llamadas a una dirección.
ms.assetid: 8cc053bd-1056-42be-b48a-d2312c456893
title: Constantes de LINEFORWARDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33702be12afaef5d1194ca5c0d288bd967a93e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691048"
---
# <a name="lineforwardmode_-constants"></a><span data-ttu-id="ac4de-103">Constantes de LINEFORWARDMODE \_</span><span class="sxs-lookup"><span data-stu-id="ac4de-103">LINEFORWARDMODE\_ Constants</span></span>

<span data-ttu-id="ac4de-104">Las constantes de marcador de bits **LINEFORWARDMODE \_** describen las condiciones en las que se pueden reenviar las llamadas a una dirección.</span><span class="sxs-lookup"><span data-stu-id="ac4de-104">The **LINEFORWARDMODE\_** bit-flag constants describe the conditions under which calls to an address can be forwarded.</span></span>

<dl> <dt>

<span data-ttu-id="ac4de-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="ac4de-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-106">Reenviar todas las llamadas en ocupado, independientemente de su origen.</span><span class="sxs-lookup"><span data-stu-id="ac4de-106">Forward all calls on busy, irrespective of their origin.</span></span> <span data-ttu-id="ac4de-107">Use este valor al reenviar para llamadas internas y externas en ocupado y no se puede controlar por separado ninguna respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac4de-107">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE \_ BUSYEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="ac4de-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE\_BUSYEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-109">Reenviar todas las llamadas externas en ocupado.</span><span class="sxs-lookup"><span data-stu-id="ac4de-109">Forward all external calls on busy.</span></span> <span data-ttu-id="ac4de-110">Use este valor al reenviar para llamadas internas y externas en ocupado y si no hay ninguna respuesta, se puede controlar por separado.</span><span class="sxs-lookup"><span data-stu-id="ac4de-110">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE \_ BUSYINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="ac4de-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE\_BUSYINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-112">Reenviar todas las llamadas internas en ocupado.</span><span class="sxs-lookup"><span data-stu-id="ac4de-112">Forward all internal calls on busy.</span></span> <span data-ttu-id="ac4de-113">Use este valor al reenviar para llamadas internas y externas en ocupado y si no hay ninguna respuesta, se puede controlar por separado.</span><span class="sxs-lookup"><span data-stu-id="ac4de-113">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE \_ BUSYNA**</span><span class="sxs-lookup"><span data-stu-id="ac4de-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE\_BUSYNA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-115">Reenviar todas las llamadas en ocupado/sin respuesta, independientemente de su origen.</span><span class="sxs-lookup"><span data-stu-id="ac4de-115">Forward all calls on busy/no answer, irrespective of their origin.</span></span> <span data-ttu-id="ac4de-116">Use este valor al reenviar para llamadas internas y externas en ocupado y no se puede controlar por separado ninguna respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac4de-116">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE \_ BUSYNAEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="ac4de-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE\_BUSYNAEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-118">Reenviar todas las llamadas externas en ocupado/sin respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac4de-118">Forward all external calls on busy/no answer.</span></span> <span data-ttu-id="ac4de-119">Use este valor cuando el reenvío de llamadas esté ocupado y no se pueda controlar por separado para las llamadas internas.</span><span class="sxs-lookup"><span data-stu-id="ac4de-119">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE \_ BUSYNAINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="ac4de-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE\_BUSYNAINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-121">Reenviar todas las llamadas internas en ocupado/no responde.</span><span class="sxs-lookup"><span data-stu-id="ac4de-121">Forward all internal calls on busy/no answer.</span></span> <span data-ttu-id="ac4de-122">Use este valor cuando el reenvío de llamadas esté ocupado y no se pueda controlar por separado para las llamadas internas.</span><span class="sxs-lookup"><span data-stu-id="ac4de-122">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE \_ BUSYNASPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="ac4de-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE\_BUSYNASPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-124">Avanzar en ocupado/no responder todas las llamadas que se originaron en una dirección especificada (reenvío selectivo de llamadas).</span><span class="sxs-lookup"><span data-stu-id="ac4de-124">Forward on busy/no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE \_ BUSYSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="ac4de-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE\_BUSYSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-126">Adelanta el uso de todas las llamadas que se originaron en una dirección especificada (reenvío selectivo de llamadas).</span><span class="sxs-lookup"><span data-stu-id="ac4de-126">Forward on busy all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE \_ NOANSW**</span><span class="sxs-lookup"><span data-stu-id="ac4de-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE\_NOANSW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-128">Reenviar todas las llamadas sin respuesta, independientemente de su origen.</span><span class="sxs-lookup"><span data-stu-id="ac4de-128">Forward all calls on no answer, irrespective of their origin.</span></span> <span data-ttu-id="ac4de-129">Use este valor cuando no se pueda controlar por separado las llamadas internas y externas en ninguna respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac4de-129">Use this value when call forwarding for internal and external calls on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE \_ NOANSWEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="ac4de-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE\_NOANSWEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-131">Reenviar todas las llamadas externas sin respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac4de-131">Forward all external calls on no answer.</span></span> <span data-ttu-id="ac4de-132">Use este valor cuando el reenvío de llamadas internas y externas sin respuesta se pueda controlar por separado.</span><span class="sxs-lookup"><span data-stu-id="ac4de-132">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE \_ NOANSWINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="ac4de-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE\_NOANSWINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-134">Reenviar todas las llamadas internas sin respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac4de-134">Forward all internal calls on no answer.</span></span> <span data-ttu-id="ac4de-135">Use este valor cuando el reenvío de llamadas internas y externas sin respuesta se pueda controlar por separado.</span><span class="sxs-lookup"><span data-stu-id="ac4de-135">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE \_ NOANSWSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="ac4de-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE\_NOANSWSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-137">Reenviar en no responder todas las llamadas que se originaron en una dirección especificada (reenvío selectivo de llamadas).</span><span class="sxs-lookup"><span data-stu-id="ac4de-137">Forward on no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="ac4de-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-139">Se reenvían las llamadas, pero las condiciones en las que se producirá el reenvío no se conocen y el proveedor de servicios nunca las conocerá.</span><span class="sxs-lookup"><span data-stu-id="ac4de-139">Calls are forwarded, but the conditions under which forwarding will occur are not known, and will never be known by the service provider.</span></span> <span data-ttu-id="ac4de-140">(Versiones de TAPI 1,4 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="ac4de-140">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE no \_ Cond**</span><span class="sxs-lookup"><span data-stu-id="ac4de-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE\_UNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-142">Reenviar todas las llamadas de manera incondicional, independientemente de su origen.</span><span class="sxs-lookup"><span data-stu-id="ac4de-142">Forward all calls unconditionally, irrespective of their origin.</span></span> <span data-ttu-id="ac4de-143">Use este valor cuando el reenvío incondicional para llamadas internas y externas no se puede controlar por separado.</span><span class="sxs-lookup"><span data-stu-id="ac4de-143">Use this value when unconditional forwarding for internal and external calls cannot be controlled separately.</span></span> <span data-ttu-id="ac4de-144">El reenvío incondicional invalida el reenvío de condiciones de respuesta y/o ausencia de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac4de-144">Unconditional forwarding overrides forwarding on busy and/or no answer conditions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE \_ UNCONDEXTERNAL**</span><span class="sxs-lookup"><span data-stu-id="ac4de-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE\_UNCONDEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-146">Reenviar todas las llamadas externas de forma incondicional.</span><span class="sxs-lookup"><span data-stu-id="ac4de-146">Forward all external calls unconditionally.</span></span> <span data-ttu-id="ac4de-147">Use este valor cuando el reenvío incondicional para llamadas internas y externas se puede controlar por separado.</span><span class="sxs-lookup"><span data-stu-id="ac4de-147">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE \_ UNCONDINTERNAL**</span><span class="sxs-lookup"><span data-stu-id="ac4de-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE\_UNCONDINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-149">Reenviar todas las llamadas internas incondicionalmente.</span><span class="sxs-lookup"><span data-stu-id="ac4de-149">Forward all internal calls unconditionally.</span></span> <span data-ttu-id="ac4de-150">Use este valor cuando el reenvío incondicional para llamadas internas y externas se puede controlar por separado.</span><span class="sxs-lookup"><span data-stu-id="ac4de-150">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE \_ UNCONDSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="ac4de-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE\_UNCONDSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-152">Reenviar incondicionalmente todas las llamadas que se originaron en una dirección especificada (reenvío selectivo de llamadas).</span><span class="sxs-lookup"><span data-stu-id="ac4de-152">Unconditionally forward all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac4de-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="ac4de-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac4de-154">Las llamadas se reenvían, pero en este momento no se conocen las condiciones en las que se producirá el reenvío.</span><span class="sxs-lookup"><span data-stu-id="ac4de-154">Calls are forwarded, but the conditions under which forwarding will occur are not known at this time.</span></span> <span data-ttu-id="ac4de-155">Es posible que las condiciones se conozcan en el futuro.</span><span class="sxs-lookup"><span data-stu-id="ac4de-155">It is possible that the conditions may become known at a future time.</span></span> <span data-ttu-id="ac4de-156">(Versiones de TAPI 1,4 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="ac4de-156">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac4de-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac4de-157">Remarks</span></span>

<span data-ttu-id="ac4de-158">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="ac4de-158">No extensibility.</span></span> <span data-ttu-id="ac4de-159">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="ac4de-159">All 32 bits are reserved.</span></span>

<span data-ttu-id="ac4de-160">Las marcas de bits definidas por LINEFORWARDMODE \_ no son ortogonales.</span><span class="sxs-lookup"><span data-stu-id="ac4de-160">The bit flags defined by LINEFORWARDMODE\_ are not orthogonal.</span></span> <span data-ttu-id="ac4de-161">El reenvío incondicional omite cualquier condición específica, como busy o no responde.</span><span class="sxs-lookup"><span data-stu-id="ac4de-161">Unconditional forwarding ignores any specific condition such as busy or no answer.</span></span> <span data-ttu-id="ac4de-162">Si el reenvío incondicional no está en vigor, el reenvío en ocupado y sin respuesta se puede controlar por separado o no por separado.</span><span class="sxs-lookup"><span data-stu-id="ac4de-162">If unconditional forwarding is not in effect, then forwarding on busy and on no answer can be controlled separately or not separately.</span></span> <span data-ttu-id="ac4de-163">Si se controla por separado, las \_ marcas LINEFORWARDMODE busy y LINEFORWARDMODE \_ NOANSW se pueden usar por separado.</span><span class="sxs-lookup"><span data-stu-id="ac4de-163">If controlled separately, the LINEFORWARDMODE\_BUSY and LINEFORWARDMODE\_NOANSW flags can be used separately.</span></span> <span data-ttu-id="ac4de-164">Si no se controla por separado, \_ se debe usar la marca LINEFORWARDMODE BUSYNA.</span><span class="sxs-lookup"><span data-stu-id="ac4de-164">If not controlled separately, the flag LINEFORWARDMODE\_BUSYNA must be used.</span></span> <span data-ttu-id="ac4de-165">Del mismo modo, si el reenvío de llamadas internas y externas se puede controlar por separado, se \_ \_ pueden usar las marcas externas LINEFORWARDMODE internas y LINEFORWARDMODE por separado; de lo contrario, se usa la combinación.</span><span class="sxs-lookup"><span data-stu-id="ac4de-165">Similarly, if forwarding of internal and external calls can be controlled separately, then LINEFORWARDMODE\_INTERNAL and LINEFORWARDMODE\_EXTERNAL flags can be used separately; otherwise the combination is used.</span></span>

<span data-ttu-id="ac4de-166">Las capacidades de dirección indican qué modos de reenvío están disponibles para cada dirección asignada a una línea.</span><span class="sxs-lookup"><span data-stu-id="ac4de-166">Address capabilities indicate which forwarding modes are available for each address assigned to a line.</span></span> <span data-ttu-id="ac4de-167">Una aplicación puede utilizar [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) para establecer condiciones de reenvío en el conmutador.</span><span class="sxs-lookup"><span data-stu-id="ac4de-167">An application can use [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) to set forwarding conditions at the switch.</span></span>

<span data-ttu-id="ac4de-168">Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión de la API negociada en la línea y no usar estos valores de LINEFORWARDMODE \_ si la versión negociada no los admite.</span><span class="sxs-lookup"><span data-stu-id="ac4de-168">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEFORWARDMODE\_ values if the negotiated version does not support them.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac4de-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac4de-169">Requirements</span></span>



| <span data-ttu-id="ac4de-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac4de-170">Requirement</span></span> | <span data-ttu-id="ac4de-171">Value</span><span class="sxs-lookup"><span data-stu-id="ac4de-171">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ac4de-172">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="ac4de-172">TAPI version</span></span><br/> | <span data-ttu-id="ac4de-173">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ac4de-173">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ac4de-174">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac4de-174">Header</span></span><br/>       | <dl> <span data-ttu-id="ac4de-175"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac4de-175"><dt>Tapi.h</dt></span></span> </dl> |



 

 




