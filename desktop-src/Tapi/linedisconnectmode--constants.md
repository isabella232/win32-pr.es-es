---
description: Las \_ constantes de marcador de bits LINEDISCONNECTMODE describen diferentes razones para una solicitud de desconexión remota. Un modo de desconexión está disponible como estado de la llamada a la aplicación después de que el estado de la llamada pase a desconectado.
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: Constantes de LINEDISCONNECTMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70ba70175685e2c264343f9345227ee64c206f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690804"
---
# <a name="linedisconnectmode_-constants"></a><span data-ttu-id="548e3-104">Constantes de LINEDISCONNECTMODE \_</span><span class="sxs-lookup"><span data-stu-id="548e3-104">LINEDISCONNECTMODE\_ Constants</span></span>

<span data-ttu-id="548e3-105">Las constantes de marcador de bits **LINEDISCONNECTMODE \_** describen diferentes razones para una solicitud de desconexión remota.</span><span class="sxs-lookup"><span data-stu-id="548e3-105">The **LINEDISCONNECTMODE\_** bit-flag constants describe different reasons for a remote disconnect request.</span></span> <span data-ttu-id="548e3-106">Un modo de desconexión está disponible como estado de la llamada a la aplicación después de que el estado de la llamada pase a desconectado.</span><span class="sxs-lookup"><span data-stu-id="548e3-106">A disconnect mode is available as call status to the application after the call state transitions to disconnected.</span></span>

<dl> <dt>

<span data-ttu-id="548e3-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE \_ BADADDRESS**</span><span class="sxs-lookup"><span data-stu-id="548e3-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE\_BADADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-108">La dirección de destino no es válida.</span><span class="sxs-lookup"><span data-stu-id="548e3-108">The destination address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="548e3-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-110">No se pudo conectar la llamada porque no se aceptan llamadas de la dirección de origen en la dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="548e3-110">The call could not be connected because calls from the origination address are not being accepted at the destination address.</span></span> <span data-ttu-id="548e3-111">Esto difiere del rechazo de LINEDISCONNECTMODE \_ en que el bloqueo se implementa en la red (un rechazo pasivo) mientras se implementa un rechazo en el equipo de destino (un rechazo activo).</span><span class="sxs-lookup"><span data-stu-id="548e3-111">This differs from LINEDISCONNECTMODE\_REJECT in that blocking is implemented in the network (a passive reject) while a rejection is implemented in the destination equipment (an active reject).</span></span> <span data-ttu-id="548e3-112">El bloqueo puede deberse a una exclusión específica de la dirección de origen o a que el destino acepta llamadas solo de un conjunto seleccionado de dirección de origen (grupo de usuarios cerrado).</span><span class="sxs-lookup"><span data-stu-id="548e3-112">The blocking can be due to a specific exclusion of the origination address, or because the destination accepts calls from only a selected set of origination address (closed user group).</span></span> <span data-ttu-id="548e3-113">(Versiones de TAPI 2,0 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="548e3-113">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="548e3-114">LINEDISCONNECTMODE \_ blocked es adecuado como respuesta bloqueo.</span><span class="sxs-lookup"><span data-stu-id="548e3-114">LINEDISCONNECTMODE\_BLOCKED is appropriate as a blocklisted response.</span></span> <span data-ttu-id="548e3-115">Por ejemplo, un módem ha recibido una respuesta, ha pasado más de seis segundos sin detectar un timbre, no pudo conectarse un número definido de veces, determina que el número de teléfono no es válido para llamar a y emite una respuesta "bloqueo".</span><span class="sxs-lookup"><span data-stu-id="548e3-115">For example, a modem has received an answer, gone more than six seconds without detecting Ringback, failed to connect a defined number of times, determines that the phone number is not valid to call, and issues a 'blocklisted' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="548e3-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-117">La estación del usuario remoto está ocupada.</span><span class="sxs-lookup"><span data-stu-id="548e3-117">The remote user's station is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="548e3-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-119">Se canceló la llamada.</span><span class="sxs-lookup"><span data-stu-id="548e3-119">The call was cancelled.</span></span> <span data-ttu-id="548e3-120">(Versiones de TAPI 2,0 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="548e3-120">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**congestión de LINEDISCONNECTMODE \_**</span><span class="sxs-lookup"><span data-stu-id="548e3-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**LINEDISCONNECTMODE\_CONGESTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-122">La red está congestionada.</span><span class="sxs-lookup"><span data-stu-id="548e3-122">The network is congested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE \_ DONOTDISTURB**</span><span class="sxs-lookup"><span data-stu-id="548e3-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE\_DONOTDISTURB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-124">No se pudo conectar la llamada porque el destino ha invocado la característica no molestar.</span><span class="sxs-lookup"><span data-stu-id="548e3-124">The call could not be connected because the destination has invoked the Do Not Disturb feature.</span></span> <span data-ttu-id="548e3-125">(Versiones de TAPI 2,0 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="548e3-125">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE \_ reenviado**</span><span class="sxs-lookup"><span data-stu-id="548e3-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-127">El modificador reenvió la llamada.</span><span class="sxs-lookup"><span data-stu-id="548e3-127">The call was forwarded by the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE \_ INcompatible**</span><span class="sxs-lookup"><span data-stu-id="548e3-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-129">El equipo de estación del usuario remoto no es compatible con el tipo de llamada solicitada.</span><span class="sxs-lookup"><span data-stu-id="548e3-129">The remote user's station equipment is incompatible with the type of call requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE \_ NOanswer**</span><span class="sxs-lookup"><span data-stu-id="548e3-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE\_NOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-131">La estación del usuario remoto no responde.</span><span class="sxs-lookup"><span data-stu-id="548e3-131">The remote user's station does not answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE \_ NODIALTONE**</span><span class="sxs-lookup"><span data-stu-id="548e3-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE\_NODIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-133">No se detectó un tono de marcado dentro de un tiempo de espera definido por el proveedor de servicios, en un momento del marcado cuando se esperaba uno (por ejemplo, en una "W" en la cadena de marcado).</span><span class="sxs-lookup"><span data-stu-id="548e3-133">A dial tone was not detected within a service-provider defined timeout, at a point during dialing when one was expected (such as at a "W" in the dialable string).</span></span> <span data-ttu-id="548e3-134">Esto también puede producirse sin un período de tiempo de espera definido por el proveedor del servicio o sin un valor especificado en el miembro **dwWaitForDialTone** de la estructura [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) .</span><span class="sxs-lookup"><span data-stu-id="548e3-134">This can also occur without a service-provider-defined timeout period or without a value specified in the **dwWaitForDialTone** member of the [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) structure.</span></span> <span data-ttu-id="548e3-135">(Versiones de TAPI 1,4 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="548e3-135">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE \_ normal**</span><span class="sxs-lookup"><span data-stu-id="548e3-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-137">Esta es una solicitud de desconexión normal de la parte remota.</span><span class="sxs-lookup"><span data-stu-id="548e3-137">This is a normal disconnect request by the remote party.</span></span> <span data-ttu-id="548e3-138">La llamada finalizó con normalidad.</span><span class="sxs-lookup"><span data-stu-id="548e3-138">The call was terminated normally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE \_ NUMBERCHANGED**</span><span class="sxs-lookup"><span data-stu-id="548e3-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE\_NUMBERCHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-140">No se pudo conectar la llamada porque se ha cambiado el número de destino, pero no se ha proporcionado la redirección automática al nuevo número.</span><span class="sxs-lookup"><span data-stu-id="548e3-140">The call could not be connected because the destination number has been changed, but automatic redirection to the new number is not provided.</span></span> <span data-ttu-id="548e3-141">(Versiones de TAPI 2,0 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="548e3-141">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE \_ OUTOFORDER**</span><span class="sxs-lookup"><span data-stu-id="548e3-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE\_OUTOFORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-143">La llamada no se pudo conectar o se desconectó porque el dispositivo de destino no está en el orden (error de hardware).</span><span class="sxs-lookup"><span data-stu-id="548e3-143">The call could not be connected or was disconnected because the destination device is out of order (hardware failure).</span></span> <span data-ttu-id="548e3-144">(Versiones de TAPI 2,0 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="548e3-144">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**recogida de LINEDISCONNECTMODE \_**</span><span class="sxs-lookup"><span data-stu-id="548e3-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**LINEDISCONNECTMODE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-146">La llamada se tomó desde cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="548e3-146">The call was picked up from elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE \_ QOSUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="548e3-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE\_QOSUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-148">La llamada no se pudo conectar o se desconectó porque no se pudo obtener o mantener la calidad de servicio mínima.</span><span class="sxs-lookup"><span data-stu-id="548e3-148">The call could not be connected or was disconnected because the minimum quality of service could not be obtained or sustained.</span></span> <span data-ttu-id="548e3-149">Esto difiere de LINEDISCONNECTMODE \_ incompatible en que la falta de recursos puede ser una condición temporal en el destino.</span><span class="sxs-lookup"><span data-stu-id="548e3-149">This differs from LINEDISCONNECTMODE\_INCOMPATIBLE in that the lack of resources may be a temporary condition at the destination.</span></span> <span data-ttu-id="548e3-150">(Versiones de TAPI 2,0 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="548e3-150">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE \_ rechazo**</span><span class="sxs-lookup"><span data-stu-id="548e3-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE\_REJECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-152">El usuario remoto ha rechazado la llamada.</span><span class="sxs-lookup"><span data-stu-id="548e3-152">The remote user has rejected the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE \_ TEMPFAILURE**</span><span class="sxs-lookup"><span data-stu-id="548e3-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE\_TEMPFAILURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-154">La llamada no se pudo conectar o se desconectó debido a un error temporal en la red. la llamada se puede volver a intentar más tarde y se espera que finalice finalmente.</span><span class="sxs-lookup"><span data-stu-id="548e3-154">The call could not be connected or was disconnected because of a temporary failure in the network; the call can be reattempted later and is expected to eventually complete.</span></span> <span data-ttu-id="548e3-155">(Versiones de TAPI 2,0 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="548e3-155">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="548e3-156">LINEDISCONNECTMODE \_ TEMPFAILURE es adecuado como respuesta diferida.</span><span class="sxs-lookup"><span data-stu-id="548e3-156">LINEDISCONNECTMODE\_TEMPFAILURE is appropriate as a delayed response.</span></span> <span data-ttu-id="548e3-157">Por ejemplo, un módem que obtiene una señal de ocupado o que es equivalente demasiadas veces en un período de tiempo determinado concluye que el número no se debe volver a llamar hasta que haya transcurrido un tiempo definido y emita una respuesta ' retrasada '.</span><span class="sxs-lookup"><span data-stu-id="548e3-157">For example, a modem getting a busy signal or equivalent too many times in a particular time period concludes that the number should not be called again until a defined time has elapsed and issues a 'delayed' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="548e3-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-159">La razón de la desconexión no está disponible y no se volverá a conocer más adelante.</span><span class="sxs-lookup"><span data-stu-id="548e3-159">The reason for the disconnect is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="548e3-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-161">El motivo de la solicitud de desconexión es desconocido, pero puede ser conocido más adelante.</span><span class="sxs-lookup"><span data-stu-id="548e3-161">The reason for the disconnect request is unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="548e3-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE \_ INaccesible**</span><span class="sxs-lookup"><span data-stu-id="548e3-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="548e3-163">No se pudo establecer contacto con el usuario remoto.</span><span class="sxs-lookup"><span data-stu-id="548e3-163">The remote user could not be reached.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="548e3-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="548e3-164">Remarks</span></span>

<span data-ttu-id="548e3-165">Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="548e3-165">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="548e3-166">Los 16 bits de orden inferior están reservados.</span><span class="sxs-lookup"><span data-stu-id="548e3-166">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="548e3-167">Una solicitud de desconexión remota para una llamada determinada provoca el cambio de estado de la llamada al estado desconectado y se envía un mensaje de [**línea \_ CALLSTATE**](line-callstate.md) a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="548e3-167">A remote disconnect request for a given call results in the call state transitioning to the disconnected state and a [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="548e3-168">La información de LINEDISCONNECTMODE \_ proporciona detalles sobre la solicitud de desconexión remota.</span><span class="sxs-lookup"><span data-stu-id="548e3-168">The LINEDISCONNECTMODE\_ information provides details about the remote disconnect request.</span></span> <span data-ttu-id="548e3-169">Está disponible en la estructura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) de la llamada cuando la llamada está en el estado disconnected.</span><span class="sxs-lookup"><span data-stu-id="548e3-169">It is available in the call's [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure when the call is in the disconnected state.</span></span> <span data-ttu-id="548e3-170">Mientras una llamada se encuentra en este estado, la aplicación sigue teniendo permiso para consultar la información y el estado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="548e3-170">While a call is in this state, the application is still allowed to query the call's information and status.</span></span> <span data-ttu-id="548e3-171">Por ejemplo, la información de usuario que se recibe como parte de la desconexión remota está disponible.</span><span class="sxs-lookup"><span data-stu-id="548e3-171">For example, user-user information that is received as part of the remote disconnect is available then.</span></span> <span data-ttu-id="548e3-172">La aplicación puede borrar una llamada desconectada quitando la llamada.</span><span class="sxs-lookup"><span data-stu-id="548e3-172">The application can clear a disconnected call by dropping the call.</span></span>

<span data-ttu-id="548e3-173">Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión de la API negociada en la línea y no usar este \_ valor de LINEDISCONNECTMODE si no se admite en la versión negociada ( \_ \_ se podría usar LINEDISCONNECTMODE normal o Unknown en su lugar).</span><span class="sxs-lookup"><span data-stu-id="548e3-173">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEDISCONNECTMODE\_ value if it is not supported on the negotiated version (LINEDISCONNECTMODE\_NORMAL or \_UNKNOWN could be used instead).</span></span>

## <a name="requirements"></a><span data-ttu-id="548e3-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="548e3-174">Requirements</span></span>



| <span data-ttu-id="548e3-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="548e3-175">Requirement</span></span> | <span data-ttu-id="548e3-176">Value</span><span class="sxs-lookup"><span data-stu-id="548e3-176">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="548e3-177">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="548e3-177">TAPI version</span></span><br/> | <span data-ttu-id="548e3-178">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="548e3-178">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="548e3-179">Encabezado</span><span class="sxs-lookup"><span data-stu-id="548e3-179">Header</span></span><br/>       | <dl> <span data-ttu-id="548e3-180"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="548e3-180"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="548e3-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="548e3-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="548e3-182">**LÍNEA \_ CALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="548e3-182">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="548e3-183">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="548e3-183">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="548e3-184">**LINEDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="548e3-184">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




