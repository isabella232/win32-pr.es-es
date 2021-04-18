---
description: En las \_ constantes LINEFEATURE se enumeran las operaciones que se pueden invocar en una línea mediante esta API.
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: Constantes de LINEFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac930123a10f401a7a79de8ccf6c61452df05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681216"
---
# <a name="linefeature_-constants"></a><span data-ttu-id="ac632-103">Constantes de LINEFEATURE \_</span><span class="sxs-lookup"><span data-stu-id="ac632-103">LINEFEATURE\_ Constants</span></span>

<span data-ttu-id="ac632-104">En **las \_ constantes LINEFEATURE** se enumeran las operaciones que se pueden invocar en una línea mediante esta API.</span><span class="sxs-lookup"><span data-stu-id="ac632-104">The **LINEFEATURE\_ constants** list the operations that can be invoked on a line using this API.</span></span>

<dl> <dt>

<span data-ttu-id="ac632-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="ac632-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac632-106">Las operaciones específicas del dispositivo se pueden usar en la línea.</span><span class="sxs-lookup"><span data-stu-id="ac632-106">Device-specific operations can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac632-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE \_ DEVSPECIFICFEAT**</span><span class="sxs-lookup"><span data-stu-id="ac632-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE\_DEVSPECIFICFEAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac632-108">Las características específicas del dispositivo se pueden usar en la línea.</span><span class="sxs-lookup"><span data-stu-id="ac632-108">Device-specific features can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac632-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE \_ adelante**</span><span class="sxs-lookup"><span data-stu-id="ac632-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac632-110">Se puede usar el reenvío de todas las direcciones en la línea.</span><span class="sxs-lookup"><span data-stu-id="ac632-110">Forwarding of all addresses can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac632-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE \_ FORWARDDND**</span><span class="sxs-lookup"><span data-stu-id="ac632-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac632-112">La función [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (con una dirección de destino vacía) se puede usar para activar la característica no molestar en todas las direcciones de la línea.</span><span class="sxs-lookup"><span data-stu-id="ac632-112">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on all addresses on the line.</span></span> <span data-ttu-id="ac632-113">\_También se establecerá LINEFEATURE forward.</span><span class="sxs-lookup"><span data-stu-id="ac632-113">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="ac632-114">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="ac632-114">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac632-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE \_ FORWARDFWD**</span><span class="sxs-lookup"><span data-stu-id="ac632-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac632-116">La función [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) se puede usar para reenviar llamadas en todas las direcciones de la línea a otros números.</span><span class="sxs-lookup"><span data-stu-id="ac632-116">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on all address on the line to other numbers.</span></span> <span data-ttu-id="ac632-117">\_También se establecerá LINEFEATURE forward.</span><span class="sxs-lookup"><span data-stu-id="ac632-117">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="ac632-118">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="ac632-118">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac632-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE \_ MAKECALL**</span><span class="sxs-lookup"><span data-stu-id="ac632-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac632-120">Se puede colocar una llamada saliente en esta línea mediante una dirección no especificada.</span><span class="sxs-lookup"><span data-stu-id="ac632-120">An outgoing call can be placed on this line using an unspecified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac632-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE \_ SETDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="ac632-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE\_SETDEVSTATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac632-122">La función [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) se puede invocar en el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="ac632-122">The [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) function can be invoked on the line device.</span></span> <span data-ttu-id="ac632-123">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="ac632-123">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac632-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE \_ SETMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="ac632-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac632-125">Se puede establecer el control multimedia en esta línea.</span><span class="sxs-lookup"><span data-stu-id="ac632-125">Media control can be set on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ac632-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE \_ SETTERMINAL**</span><span class="sxs-lookup"><span data-stu-id="ac632-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ac632-127">Se pueden establecer los modos de terminal para esta línea.</span><span class="sxs-lookup"><span data-stu-id="ac632-127">Terminal modes for this line can be set.</span></span>

> [!Note]  
> <span data-ttu-id="ac632-128">Si ninguno de los nuevos bits modificados "FORWARD" se ha establecido en el miembro **dwLineFeatures** de [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) \_ , pero se establece el bit de avance LINEFEATURE, cualquiera de los modos de avance puede funcionar; el proveedor de servicios simplemente no especificó ninguno de ellos.</span><span class="sxs-lookup"><span data-stu-id="ac632-128">If neither of the new modified "FORWARD" bits is set in the **dwLineFeatures** member in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) but the LINEFEATURE\_FORWARD bit is set, then any of the forward modes can work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac632-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac632-129">Remarks</span></span>

<span data-ttu-id="ac632-130">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="ac632-130">No extensibility.</span></span> <span data-ttu-id="ac632-131">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="ac632-131">All 32 bits are reserved.</span></span>

<span data-ttu-id="ac632-132">Las \_ constantes LINEFEATURE se usan en [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (devuelta por [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)).</span><span class="sxs-lookup"><span data-stu-id="ac632-132">The LINEFEATURE\_ constants are used in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (returned by [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)).</span></span> <span data-ttu-id="ac632-133">[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) notifica, para una línea determinada, qué características de línea se pueden invocar realmente mientras la línea está en el estado actual.</span><span class="sxs-lookup"><span data-stu-id="ac632-133">[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) reports, for a given line, which line features can actually be invoked while the line is in the current state.</span></span> <span data-ttu-id="ac632-134">Una aplicación realizaría esta determinación dinámicamente después de que cambie el estado de línea, normalmente causado por las actividades relacionadas con la dirección o la llamada en la línea.</span><span class="sxs-lookup"><span data-stu-id="ac632-134">An application would make this determination dynamically after line state changes, typically caused by address or call-related activities on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac632-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac632-135">Requirements</span></span>



| <span data-ttu-id="ac632-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac632-136">Requirement</span></span> | <span data-ttu-id="ac632-137">Value</span><span class="sxs-lookup"><span data-stu-id="ac632-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ac632-138">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="ac632-138">TAPI version</span></span><br/> | <span data-ttu-id="ac632-139">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ac632-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ac632-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac632-140">Header</span></span><br/>       | <dl> <span data-ttu-id="ac632-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac632-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac632-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac632-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac632-143">**LINEDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="ac632-143">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="ac632-144">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="ac632-144">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="ac632-145">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="ac632-145">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="ac632-146">**lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="ac632-146">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 




