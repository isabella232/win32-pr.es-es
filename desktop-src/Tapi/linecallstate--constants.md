---
description: Las \_ constantes de marcador de bits LINECALLSTATE describen los Estados de llamada en los que puede estar una llamada.
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: Constantes de LINECALLSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d50301dfeca49513a919fba90cc960c7ccb572d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680362"
---
# <a name="linecallstate_-constants"></a><span data-ttu-id="21c2c-103">Constantes de LINECALLSTATE \_</span><span class="sxs-lookup"><span data-stu-id="21c2c-103">LINECALLSTATE\_ Constants</span></span>

<span data-ttu-id="21c2c-104">Las constantes de marcador de bits **LINECALLSTATE \_** describen los Estados de llamada en los que puede estar una llamada.</span><span class="sxs-lookup"><span data-stu-id="21c2c-104">The **LINECALLSTATE\_** bit-flag constants describe the call states a call can be in.</span></span>

<dl> <dt>

<span data-ttu-id="21c2c-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE \_ aceptado**</span><span class="sxs-lookup"><span data-stu-id="21c2c-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-106">La llamada se encontraba en el estado de la oferta y se aceptó.</span><span class="sxs-lookup"><span data-stu-id="21c2c-106">The call was in the offering state and has been accepted.</span></span> <span data-ttu-id="21c2c-107">Esto indica a otras aplicaciones (de supervisión) que la aplicación propietaria actual ha reclamado la responsabilidad de responder a la llamada.</span><span class="sxs-lookup"><span data-stu-id="21c2c-107">This indicates to other (monitoring) applications that the current owner application has claimed responsibility for answering the call.</span></span> <span data-ttu-id="21c2c-108">En ISDN, el estado aceptado se especifica cuando el equipo de la entidad que llama envía un mensaje al conmutador que indica que está dispuesto a presentar la llamada a la persona llamada.</span><span class="sxs-lookup"><span data-stu-id="21c2c-108">In ISDN, the accepted state is entered when the called-party equipment sends a message to the switch indicating that it is willing to present the call to the called person.</span></span> <span data-ttu-id="21c2c-109">Esto tiene el efecto secundario de las alertas (timbres) de los usuarios en ambos extremos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="21c2c-109">This has the side effect of alerting (ringing) the users at both ends of the call.</span></span> <span data-ttu-id="21c2c-110">Una llamada entrante siempre se puede responder inmediatamente sin aceptarse primero por separado.</span><span class="sxs-lookup"><span data-stu-id="21c2c-110">An incoming call can always be immediately answered without first being separately accepted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="21c2c-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-112">La llamada recibe un tono ocupado.</span><span class="sxs-lookup"><span data-stu-id="21c2c-112">The call is receiving a busy tone.</span></span> <span data-ttu-id="21c2c-113">Un tono ocupado indica que la llamada no se puede completar porque un circuito (tronco) o la estación de la entidad remota están en uso.</span><span class="sxs-lookup"><span data-stu-id="21c2c-113">A busy tone indicates that the call cannot be completed either a circuit (trunk) or the remote party's station are in use.</span></span> <span data-ttu-id="21c2c-114">Vea [**\_ constantes LINEBUSYMODE**](linebusymode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="21c2c-114">See [**LINEBUSYMODE\_ Constants**](linebusymode--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE \_ Conference**</span><span class="sxs-lookup"><span data-stu-id="21c2c-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE\_CONFERENCED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-116">La llamada es un miembro de una llamada de conferencia y está lógicamente en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="21c2c-116">The call is a member of a conference call and is logically in the connected state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="21c2c-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-118">Se ha establecido la llamada y se ha realizado la conexión.</span><span class="sxs-lookup"><span data-stu-id="21c2c-118">The call has been established and the connection is made.</span></span> <span data-ttu-id="21c2c-119">La información puede fluir a través de la llamada entre la dirección de origen y la dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="21c2c-119">Information is able to flow over the call between the originating address and the destination address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**\_marcado LINECALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="21c2c-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**LINECALLSTATE\_DIALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-121">El originador está marcando dígitos en la llamada.</span><span class="sxs-lookup"><span data-stu-id="21c2c-121">The originator is dialing digits on the call.</span></span> <span data-ttu-id="21c2c-122">El modificador recopila los dígitos marcados.</span><span class="sxs-lookup"><span data-stu-id="21c2c-122">The dialed digits are collected by the switch.</span></span> <span data-ttu-id="21c2c-123">Tenga en cuenta que ni [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) ni [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) colocarán la línea en el estado de marcado.</span><span class="sxs-lookup"><span data-stu-id="21c2c-123">Note that neither [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) nor [**TSPI\_lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) will place the line into the dialing state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE \_ DItono**</span><span class="sxs-lookup"><span data-stu-id="21c2c-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-125">La llamada está recibiendo un tono de marcado del conmutador, lo que significa que el conmutador está listo para recibir un número marcado.</span><span class="sxs-lookup"><span data-stu-id="21c2c-125">The call is receiving a dial tone from the switch, which means that the switch is ready to receive a dialed number.</span></span> <span data-ttu-id="21c2c-126">Vea [**\_ constantes de LINEDIALTONEMODE**](linedialtonemode--constants.md) para identificadores de tonos de marcado especiales, como un tono de intermitencia del correo de voz normal.</span><span class="sxs-lookup"><span data-stu-id="21c2c-126">See [**LINEDIALTONEMODE\_ Constants**](linedialtonemode--constants.md) for identifiers of special dial tones, such as a stutter tone of normal voice mail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE \_ DESconectado**</span><span class="sxs-lookup"><span data-stu-id="21c2c-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-128">La parte remota se ha desconectado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="21c2c-128">The remote party has disconnected from the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE \_ inactivo**</span><span class="sxs-lookup"><span data-stu-id="21c2c-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-130">La llamada existe pero no se ha conectado.</span><span class="sxs-lookup"><span data-stu-id="21c2c-130">The call exists but has not been connected.</span></span> <span data-ttu-id="21c2c-131">No existe ninguna actividad en la llamada, lo que significa que no hay ninguna llamada actualmente activa.</span><span class="sxs-lookup"><span data-stu-id="21c2c-131">No activity exists on the call, which means that no call is currently active.</span></span> <span data-ttu-id="21c2c-132">Una llamada nunca puede salir del estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="21c2c-132">A call can never transition out of the idle state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**oferta de LINECALLSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="21c2c-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**LINECALLSTATE\_OFFERING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-134">La llamada se ofrece a la estación, señalando la llegada de una nueva llamada.</span><span class="sxs-lookup"><span data-stu-id="21c2c-134">The call is being offered to the station, signaling the arrival of a new call.</span></span> <span data-ttu-id="21c2c-135">El estado de la oferta no es el mismo que ocasionar que un teléfono o equipo suene.</span><span class="sxs-lookup"><span data-stu-id="21c2c-135">The offering state is not the same as causing a phone or computer to ring.</span></span> <span data-ttu-id="21c2c-136">En algunos entornos, una llamada en el estado de la oferta no hace sonar al usuario hasta que el modificador indica a la línea que se ponga en anillo.</span><span class="sxs-lookup"><span data-stu-id="21c2c-136">In some environments, a call in the offering state does not ring the user until the switch instructs the line to ring.</span></span> <span data-ttu-id="21c2c-137">Un uso de ejemplo podría ser el lugar en el que aparece una llamada entrante en varios conjuntos de estaciones, pero solo los anillos de la dirección principal.</span><span class="sxs-lookup"><span data-stu-id="21c2c-137">An example use might be where an incoming call appears on several station sets but only the primary address rings.</span></span> <span data-ttu-id="21c2c-138">La instrucción para el anillo no afecta a ningún estado de llamada.</span><span class="sxs-lookup"><span data-stu-id="21c2c-138">The instruction to ring does not affect any call states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE en \_ suspensión**</span><span class="sxs-lookup"><span data-stu-id="21c2c-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE\_ONHOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-140">La llamada está en espera por el modificador.</span><span class="sxs-lookup"><span data-stu-id="21c2c-140">The call is on hold by the switch.</span></span> <span data-ttu-id="21c2c-141">Esto libera la línea física, lo que permite que otra llamada use la línea.</span><span class="sxs-lookup"><span data-stu-id="21c2c-141">This frees the physical line, which allows another call to use the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE \_ ONHOLDPENDCONF**</span><span class="sxs-lookup"><span data-stu-id="21c2c-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE\_ONHOLDPENDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-143">La llamada está actualmente en espera mientras se agrega a una conferencia.</span><span class="sxs-lookup"><span data-stu-id="21c2c-143">The call is currently on hold while it is being added to a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE \_ ONHOLDPENDTRANSFER**</span><span class="sxs-lookup"><span data-stu-id="21c2c-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE\_ONHOLDPENDTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-145">La llamada está en espera en el momento de la transferencia a otro número.</span><span class="sxs-lookup"><span data-stu-id="21c2c-145">The call is currently on hold awaiting transfer to another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE \_ continuar**</span><span class="sxs-lookup"><span data-stu-id="21c2c-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE\_PROCEEDING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-147">El marcado se ha completado y la llamada se realiza a través del conmutador o la red telefónica.</span><span class="sxs-lookup"><span data-stu-id="21c2c-147">Dialing has completed and the call is proceeding through the switch or telephone network.</span></span> <span data-ttu-id="21c2c-148">Esto se produce después de que el marcado finalice y antes de que la llamada llegue a la entidad marcada, como se indica por timbre, ocupado o respuesta.</span><span class="sxs-lookup"><span data-stu-id="21c2c-148">This occurs after dialing is complete and before the call reaches the dialed party, as indicated by ringback, busy, or answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**\_timbre LINECALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="21c2c-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-150">Se ha alcanzado la estación a la que se va a llamar y el conmutador del destino está generando un tono de timbre de vuelta al originador.</span><span class="sxs-lookup"><span data-stu-id="21c2c-150">The station to be called has been reached, and the destination's switch is generating a ring tone back to the originator.</span></span> <span data-ttu-id="21c2c-151">Un *timbre* significa que la dirección de destino se alerta a la llamada.</span><span class="sxs-lookup"><span data-stu-id="21c2c-151">A *ringback* means that the destination address is being alerted to the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE \_ SPECIALINFO**</span><span class="sxs-lookup"><span data-stu-id="21c2c-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE\_SPECIALINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-153">La llamada recibe una señal de información especial, que precede a un anuncio pregrabado que indica por qué no se puede completar una llamada.</span><span class="sxs-lookup"><span data-stu-id="21c2c-153">The call is receiving a special information signal, which precedes a prerecorded announcement indicating why a call cannot be completed.</span></span> <span data-ttu-id="21c2c-154">Vea [**\_ constantes LINESPECIALINFO**](linespecialinfo--constants.md).</span><span class="sxs-lookup"><span data-stu-id="21c2c-154">See [**LINESPECIALINFO\_ Constants**](linespecialinfo--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="21c2c-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="21c2c-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="21c2c-156">La llamada existe, pero su estado es desconocido actualmente.</span><span class="sxs-lookup"><span data-stu-id="21c2c-156">The call exists, but its state is currently unknown.</span></span> <span data-ttu-id="21c2c-157">Este puede ser el resultado de una detección deficiente del progreso de la llamada por parte del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="21c2c-157">This may be the result of poor call progress detection by the service provider.</span></span> <span data-ttu-id="21c2c-158">También se puede generar un mensaje de estado de llamada con el estado de llamada establecido en Unknown para informar a la DLL de TAPI sobre una nueva llamada a la vez cuando no se conoce el estado de llamada real de la llamada.</span><span class="sxs-lookup"><span data-stu-id="21c2c-158">A call state message with the call state set to unknown may also be generated to inform the TAPI DLL about a new call at a time when the actual call state of the call is not exactly known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21c2c-159">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21c2c-159">Remarks</span></span>

<span data-ttu-id="21c2c-160">Los 8 bits de orden superior pueden definir un subestado específico del dispositivo de cualquiera de los Estados predefinidos, siempre que \_ se establezca también uno de los bits LINECALLSTATE definidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="21c2c-160">The high-order 8 bits can define a device-specific substate of any of the predefined states, provided that one of the LINECALLSTATE\_ bits defined above is also set.</span></span> <span data-ttu-id="21c2c-161">Los 24 bits de orden inferior están reservados para los Estados predefinidos.</span><span class="sxs-lookup"><span data-stu-id="21c2c-161">The low-order 24 bits are reserved for predefined states.</span></span>

<span data-ttu-id="21c2c-162">El mensaje de [**línea \_ CALLSTATE**](line-callstate.md) que se envía a la aplicación usa las **\_ constantes LINECALLSTATE** como parámetros.</span><span class="sxs-lookup"><span data-stu-id="21c2c-162">The **LINECALLSTATE\_constants** are used as parameters by the [**LINE\_CALLSTATE**](line-callstate.md) message sent to the application.</span></span> <span data-ttu-id="21c2c-163">El mensaje lleva el nuevo estado de la llamada al que la llamada ha pasado.</span><span class="sxs-lookup"><span data-stu-id="21c2c-163">The message carries the new call state that the call transitioned to.</span></span> <span data-ttu-id="21c2c-164">Estas constantes también se usan como miembros en la estructura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) devuelta por la función [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) .</span><span class="sxs-lookup"><span data-stu-id="21c2c-164">These constants are also used as members in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure returned by the [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="21c2c-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21c2c-165">Requirements</span></span>



| <span data-ttu-id="21c2c-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="21c2c-166">Requirement</span></span> | <span data-ttu-id="21c2c-167">Value</span><span class="sxs-lookup"><span data-stu-id="21c2c-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="21c2c-168">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="21c2c-168">TAPI version</span></span><br/> | <span data-ttu-id="21c2c-169">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="21c2c-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="21c2c-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21c2c-170">Header</span></span><br/>       | <dl> <span data-ttu-id="21c2c-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="21c2c-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21c2c-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="21c2c-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21c2c-173">**LÍNEA \_ CALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="21c2c-173">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="21c2c-174">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="21c2c-174">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="21c2c-175">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="21c2c-175">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="21c2c-176">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="21c2c-176">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

