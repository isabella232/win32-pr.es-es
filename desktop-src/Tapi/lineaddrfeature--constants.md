---
description: En las \_ constantes LINEADDRFEATURE se enumeran las operaciones que se pueden invocar en una dirección.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: Constantes de LINEADDRFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825902c2943806d1d495e14a0f0a5042f2949796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680228"
---
# <a name="lineaddrfeature_-constants"></a><span data-ttu-id="8efc9-103">Constantes de LINEADDRFEATURE \_</span><span class="sxs-lookup"><span data-stu-id="8efc9-103">LINEADDRFEATURE\_ Constants</span></span>

<span data-ttu-id="8efc9-104">En las constantes **LINEADDRFEATURE \_** se enumeran las operaciones que se pueden invocar en una dirección.</span><span class="sxs-lookup"><span data-stu-id="8efc9-104">The **LINEADDRFEATURE\_** constants list the operations that can be invoked on an address.</span></span>

<dl> <dt>

<span data-ttu-id="8efc9-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE \_ adelante**</span><span class="sxs-lookup"><span data-stu-id="8efc9-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-106">La dirección se puede reenviar.</span><span class="sxs-lookup"><span data-stu-id="8efc9-106">The address can be forwarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8efc9-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE \_ MAKECALL**</span><span class="sxs-lookup"><span data-stu-id="8efc9-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-108">Se puede colocar una llamada saliente en la dirección.</span><span class="sxs-lookup"><span data-stu-id="8efc9-108">An outgoing call can be placed on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8efc9-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**recogida de LINEADDRFEATURE \_**</span><span class="sxs-lookup"><span data-stu-id="8efc9-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**LINEADDRFEATURE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-110">Se puede seleccionar una llamada en la dirección.</span><span class="sxs-lookup"><span data-stu-id="8efc9-110">A call can be picked up at the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8efc9-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE \_ PICKUPDIRECT**</span><span class="sxs-lookup"><span data-stu-id="8efc9-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE\_PICKUPDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-112">La función [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) se puede usar para seleccionar una llamada en una dirección específica.</span><span class="sxs-lookup"><span data-stu-id="8efc9-112">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call on a specific address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8efc9-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE \_ PICKUPGROUP**</span><span class="sxs-lookup"><span data-stu-id="8efc9-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE\_PICKUPGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-114">La función [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) se puede usar para seleccionar una llamada en el grupo.</span><span class="sxs-lookup"><span data-stu-id="8efc9-114">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call in the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8efc9-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE \_ PICKUPHELD**</span><span class="sxs-lookup"><span data-stu-id="8efc9-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE\_PICKUPHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-116">La función [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (con una dirección de destino **nula** ) se puede usar para recoger una llamada que se mantiene en la dirección.</span><span class="sxs-lookup"><span data-stu-id="8efc9-116">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call that is held on the address.</span></span> <span data-ttu-id="8efc9-117">Normalmente, solo se usa en una organización exclusiva con puente.</span><span class="sxs-lookup"><span data-stu-id="8efc9-117">This is normally used only in a bridged-exclusive arrangement.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8efc9-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE \_ PICKUPWAITING**</span><span class="sxs-lookup"><span data-stu-id="8efc9-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE\_PICKUPWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-119">La función [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (con una dirección de destino **nula** ) se puede usar para recopilar una llamada de llamada en espera.</span><span class="sxs-lookup"><span data-stu-id="8efc9-119">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call waiting call.</span></span> <span data-ttu-id="8efc9-120">Tenga en cuenta que esto no indica necesariamente que una llamada en espera esté realmente presente, porque a menudo es imposible que un dispositivo de telefonía detecte automáticamente dicha llamada. sin embargo, indica que se invocará la función de enlace-Flash para intentar cambiar a dicha llamada.</span><span class="sxs-lookup"><span data-stu-id="8efc9-120">Note that this does not necessarily indicate that a waiting call is actually present, because it is often impossible for a telephony device to automatically detect such a call; it does, however, indicate that the hook-flash function will be invoked to attempt to switch to such a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8efc9-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE \_ SETMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="8efc9-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-122">Se puede establecer el control multimedia en esta dirección.</span><span class="sxs-lookup"><span data-stu-id="8efc9-122">Media control can be set on this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8efc9-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE \_ SETTERMINAL**</span><span class="sxs-lookup"><span data-stu-id="8efc9-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-124">Se pueden establecer los modos de terminal para esta dirección.</span><span class="sxs-lookup"><span data-stu-id="8efc9-124">The terminal modes for this address can be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8efc9-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE \_ SETUPCONF**</span><span class="sxs-lookup"><span data-stu-id="8efc9-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE\_SETUPCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-126">En esta dirección se puede configurar una llamada de conferencia con una llamada inicial **null** .</span><span class="sxs-lookup"><span data-stu-id="8efc9-126">A conference call with a **NULL** initial call can be set up at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8efc9-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE \_ UNCOMPLETECALL**</span><span class="sxs-lookup"><span data-stu-id="8efc9-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE\_UNCOMPLETECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-128">Las solicitudes de finalización de llamada se pueden cancelar en esta dirección.</span><span class="sxs-lookup"><span data-stu-id="8efc9-128">Call completion requests can be canceled at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8efc9-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**Desactivación \_ de LINEADDRFEATURE**</span><span class="sxs-lookup"><span data-stu-id="8efc9-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-130">Las llamadas se pueden desactivar con esta dirección.</span><span class="sxs-lookup"><span data-stu-id="8efc9-130">Calls can be unparked using this address.</span></span>

> [!Note]  
> <span data-ttu-id="8efc9-131">Si no se establece ninguno de los nuevos bits de "recogida" modificados en el miembro **dwAddressFeatures** de [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) \_ , pero se establece el bit de recogida LINEADDRFEATURE, puede que cualquiera de los modos de recogida funcione; el proveedor de servicios simplemente no especificó ninguno.</span><span class="sxs-lookup"><span data-stu-id="8efc9-131">If none of the new modified "PICKUP" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_PICKUP bit is set, then any of the pickup modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="8efc9-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE \_ FORWARDDND**</span><span class="sxs-lookup"><span data-stu-id="8efc9-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-133">La función [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (con una dirección de destino vacía) se puede usar para activar la característica no molestar en la dirección.</span><span class="sxs-lookup"><span data-stu-id="8efc9-133">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on the address.</span></span> <span data-ttu-id="8efc9-134">\_También se establecerá LINEADDRFEATURE forward.</span><span class="sxs-lookup"><span data-stu-id="8efc9-134">LINEADDRFEATURE\_FORWARD will also be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8efc9-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE \_ FORWARDFWD**</span><span class="sxs-lookup"><span data-stu-id="8efc9-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8efc9-136">La función [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) se puede usar para reenviar las llamadas en la dirección a otros números.</span><span class="sxs-lookup"><span data-stu-id="8efc9-136">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on the address to other numbers.</span></span> <span data-ttu-id="8efc9-137">\_También se establecerá LINEADDRFEATURE forward.</span><span class="sxs-lookup"><span data-stu-id="8efc9-137">LINEADDRFEATURE\_FORWARD will also be set.</span></span>

> [!Note]  
> <span data-ttu-id="8efc9-138">Si ninguno de los nuevos bits modificados "FORWARD" se establece en el miembro **dwAddressFeatures** de [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) , pero \_ se establece el bit de avance LINEADDRFEATURE, puede que cualquiera de los modos de avance funcione; el proveedor de servicios simplemente no especificó ninguno de ellos.</span><span class="sxs-lookup"><span data-stu-id="8efc9-138">If neither of the new modified "FORWARD" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_FORWARD bit is set, then any of the forward modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8efc9-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8efc9-139">Remarks</span></span>

<span data-ttu-id="8efc9-140">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="8efc9-140">No extensibility.</span></span> <span data-ttu-id="8efc9-141">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="8efc9-141">All 32 bits are reserved.</span></span>

<span data-ttu-id="8efc9-142">Esta constante se usa en [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (devuelta por [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) y en [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (devuelta por [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)).</span><span class="sxs-lookup"><span data-stu-id="8efc9-142">This constant is used both in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (returned by [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) and in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (returned by [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)).</span></span> <span data-ttu-id="8efc9-143">**LINEADDRESSCAPS** informa de la disponibilidad de las características de dirección por parte del proveedor de servicios (principalmente, el modificador) para una dirección determinada.</span><span class="sxs-lookup"><span data-stu-id="8efc9-143">**LINEADDRESSCAPS** reports the availability of the address features by the service provider (mainly the switch) for a given address.</span></span> <span data-ttu-id="8efc9-144">Una aplicación realizaría esta determinación cuando se inicializa.</span><span class="sxs-lookup"><span data-stu-id="8efc9-144">An application would make this determination when it initializes.</span></span> <span data-ttu-id="8efc9-145">La estructura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) notifica, para una dirección determinada, en la que se pueden invocar realmente características mientras la dirección está en el estado actual.</span><span class="sxs-lookup"><span data-stu-id="8efc9-145">The [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure reports, for a given address, which address features can actually be invoked while the address is in the current state.</span></span> <span data-ttu-id="8efc9-146">Una aplicación realizaría esta determinación de forma dinámica después de los cambios de estado de dirección, normalmente causado por actividades relacionadas con llamadas en la dirección.</span><span class="sxs-lookup"><span data-stu-id="8efc9-146">An application would make this determination dynamically after address-state changes, typically caused by call-related activities on the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="8efc9-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8efc9-147">Requirements</span></span>



| <span data-ttu-id="8efc9-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="8efc9-148">Requirement</span></span> | <span data-ttu-id="8efc9-149">Value</span><span class="sxs-lookup"><span data-stu-id="8efc9-149">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8efc9-150">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8efc9-150">TAPI version</span></span><br/> | <span data-ttu-id="8efc9-151">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8efc9-151">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8efc9-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8efc9-152">Header</span></span><br/>       | <dl> <span data-ttu-id="8efc9-153"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8efc9-153"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8efc9-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="8efc9-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8efc9-155">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="8efc9-155">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="8efc9-156">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="8efc9-156">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="8efc9-157">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="8efc9-157">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="8efc9-158">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="8efc9-158">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="8efc9-159">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="8efc9-159">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="8efc9-160">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="8efc9-160">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




