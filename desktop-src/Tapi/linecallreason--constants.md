---
description: Las \_ constantes de marcador de bits LINECALLREASON describen el motivo de una llamada.
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: Constantes de LINECALLREASON_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678989"
---
# <a name="linecallreason_-constants"></a><span data-ttu-id="9a0ac-103">Constantes de LINECALLREASON \_</span><span class="sxs-lookup"><span data-stu-id="9a0ac-103">LINECALLREASON\_ Constants</span></span>

<span data-ttu-id="9a0ac-104">Las constantes de marcador de bits **LINECALLREASON \_** describen el motivo de una llamada.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-104">The **LINECALLREASON\_** bit-flag constants describe the reason for a call.</span></span>

<dl> <dt>

<span data-ttu-id="9a0ac-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON \_ CALLCOMPLETION**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON\_CALLCOMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-106">La llamada fue el resultado de una solicitud de finalización de llamada.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-106">The call was the result of a call completion request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON \_ CAMPEDON**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON\_CAMPEDON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-108">La llamada se realizó en la dirección.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-108">The call was camped on the address.</span></span> <span data-ttu-id="9a0ac-109">Normalmente, aparece inicialmente en estado de suspensión y se puede cambiar a mediante [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold).</span><span class="sxs-lookup"><span data-stu-id="9a0ac-109">Usually, it appears initially in the onhold state, and can be switched to using [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold).</span></span> <span data-ttu-id="9a0ac-110">Si una llamada activa se vuelve inactiva, la llamada de acampada puede cambiar al estado de la oferta y el dispositivo comienza a sonar.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-110">If an active call becomes idle, the camped-on call may change to the offering state and the device start ringing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON \_ directo**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-112">Se trata de una llamada directa entrante o saliente.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-112">This is a direct incoming or outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON \_ FWDBUSY**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON\_FWDBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-114">Esta llamada se reenvió desde otra extensión que estaba ocupada en el momento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-114">This call was forwarded from another extension that was busy at the time of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON \_ FWDNOANSWER**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON\_FWDNOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-116">La llamada se reenvió desde otra extensión que no ha respondido a la llamada después de un número de anillos.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-116">The call was forwarded from another extension that didn't answer the call after some number of rings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON \_ FWDUNCOND**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON\_FWDUNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-118">La llamada se reenvió incondicionalmente desde otro número.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-118">The call was forwarded unconditionally from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON \_ intrusión**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-120">La llamada se ha desatacado en la línea, ya sea mediante una acción de finalización de llamada invocada por otra estación o por una acción del operador.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-120">The call intruded onto the line, either by a call completion action invoked by another station or by operator action.</span></span> <span data-ttu-id="9a0ac-121">Dependiendo de la implementación del conmutador, la llamada puede aparecer en el estado conectado o en la Conferencia con una llamada activa existente en la línea.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-121">Depending on switch implementation, the call may appear either in the connected state, or conferenced with an existing active call on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON \_ estacionado**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON\_PARKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-123">La llamada se ha detenido en la dirección.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-123">The call was parked on the address.</span></span> <span data-ttu-id="9a0ac-124">Normalmente, aparece inicialmente en estado de suspensión.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-124">Usually, it appears initially in the onhold state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**recogida de LINECALLREASON \_**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**LINECALLREASON\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-126">La llamada se tomó de otra extensión.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-126">The call was picked up from another extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**redirección de LINECALLREASON \_**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**LINECALLREASON\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-128">La llamada se redirigió a esta estación.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-128">The call was redirected to this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**LINECALLREASON \_ recordatorio**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**LINECALLREASON\_REMINDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-130">La llamada es un recordatorio (o "retirada") de que el usuario tiene una llamada detenida o en espera durante un tiempo prolongado.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-130">The call is a reminder (or "recall") that the user has a call parked or on hold for (potentially) a long time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON \_ ROUTEREQUEST**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON\_ROUTEREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-132">La llamada aparece en la dirección porque el conmutador necesita instrucciones de enrutamiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-132">The call appears on the address because the switch needs routing instructions from the application.</span></span> <span data-ttu-id="9a0ac-133">La aplicación debe examinar el miembro **CalledID** de [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)y usar la función [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) para proporcionar una nueva dirección de marcado para la llamada.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-133">The application should examine the **CalledID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo), and use the [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) function to provide a new dialable address for the call.</span></span> <span data-ttu-id="9a0ac-134">Si se va a bloquear la llamada en su lugar, la aplicación puede llamar a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop).</span><span class="sxs-lookup"><span data-stu-id="9a0ac-134">If the call is to be blocked instead, the application may call [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop).</span></span> <span data-ttu-id="9a0ac-135">Si la aplicación no puede realizar una acción dentro de un período de tiempo de espera definido por el conmutador, se realizará una acción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-135">If the application fails to take action within a switch-defined timeout period, a default action will be taken.</span></span> <span data-ttu-id="9a0ac-136">Un proveedor de servicios puede utilizar esta constante solo si la versión negociada en la línea es 2,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-136">A service provider can use this constant only if the negotiated version on the line is 2.0 or higher.</span></span> <span data-ttu-id="9a0ac-137">En caso contrario, el proveedor de servicios debe sustituir LINECALLREASON no \_ disponible.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-137">Otherwise the service provider should substitute LINECALLREASON\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**transferencia de LINECALLREASON \_**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**LINECALLREASON\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-139">La llamada se ha transferido desde otro número.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-139">The call has been transferred from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-141">La razón de la llamada no está disponible y no se volverá a conocer más adelante.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-141">The reason for the call is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-143">Actualmente, el motivo de la llamada es desconocido, pero puede ser conocido más adelante.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-143">The reason for the call is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0ac-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**Desactivación \_ de LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9a0ac-145">La llamada se recuperó como una llamada estacionada.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-145">The call was retrieved as a parked call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a0ac-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a0ac-146">Remarks</span></span>

<span data-ttu-id="9a0ac-147">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-147">No extensibility.</span></span> <span data-ttu-id="9a0ac-148">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="9a0ac-148">All 32 bits are reserved.</span></span>

<span data-ttu-id="9a0ac-149">Las \_ constantes LINECALLREASON se usan en el miembro **dwReason** de la estructura de datos [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="9a0ac-149">The LINECALLREASON\_ constants are used in the **dwReason** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0ac-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a0ac-150">Requirements</span></span>



| <span data-ttu-id="9a0ac-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a0ac-151">Requirement</span></span> | <span data-ttu-id="9a0ac-152">Value</span><span class="sxs-lookup"><span data-stu-id="9a0ac-152">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9a0ac-153">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="9a0ac-153">TAPI version</span></span><br/> | <span data-ttu-id="9a0ac-154">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="9a0ac-154">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="9a0ac-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a0ac-155">Header</span></span><br/>       | <dl> <span data-ttu-id="9a0ac-156"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a0ac-156"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a0ac-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a0ac-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a0ac-158">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-158">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[<span data-ttu-id="9a0ac-159">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-159">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="9a0ac-160">**lineRedirect**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-160">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[<span data-ttu-id="9a0ac-161">**lineSwapHold**</span><span class="sxs-lookup"><span data-stu-id="9a0ac-161">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




