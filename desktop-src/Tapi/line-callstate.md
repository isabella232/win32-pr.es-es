---
description: El \_ mensaje de línea de CALLSTATE TAPI se envía cuando cambia el estado de la llamada especificada.
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: Mensaje de LINE_CALLSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4159037c448307c99e759d8741ed19a14ab2562f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679491"
---
# <a name="line_callstate-message"></a><span data-ttu-id="11c26-103">Mensaje de línea \_ CALLSTATE</span><span class="sxs-lookup"><span data-stu-id="11c26-103">LINE\_CALLSTATE message</span></span>

<span data-ttu-id="11c26-104">El mensaje de **línea de \_ CALLSTATE** TAPI se envía cuando cambia el estado de la llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="11c26-104">The TAPI **LINE\_CALLSTATE** message is sent when the status of the specified call has changed.</span></span> <span data-ttu-id="11c26-105">Normalmente, se reciben varios mensajes de este tipo durante la duración de una llamada.</span><span class="sxs-lookup"><span data-stu-id="11c26-105">Typically, several such messages are received during the lifetime of a call.</span></span> <span data-ttu-id="11c26-106">Se notifica a las aplicaciones las nuevas llamadas entrantes con este mensaje; la nueva llamada está en el estado de la *oferta* .</span><span class="sxs-lookup"><span data-stu-id="11c26-106">Applications are notified of new incoming calls with this message; the new call is in the *offering* state.</span></span> <span data-ttu-id="11c26-107">La aplicación puede utilizar [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) para recuperar información más detallada sobre el estado actual de la llamada.</span><span class="sxs-lookup"><span data-stu-id="11c26-107">The application can use [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) to retrieve more detailed information about the current status of the call.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="11c26-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11c26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11c26-109">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="11c26-109">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="11c26-110">Identificador de la llamada.</span><span class="sxs-lookup"><span data-stu-id="11c26-110">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="11c26-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="11c26-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="11c26-112">Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.</span><span class="sxs-lookup"><span data-stu-id="11c26-112">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="11c26-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="11c26-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="11c26-114">Nuevo estado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="11c26-114">The new call state.</span></span> <span data-ttu-id="11c26-115">Este parámetro debe ser una y solo una de las siguientes [**\_ constantes LINECALLSTATE**](linecallstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="11c26-115">This parameter must be one and only one of the following [**LINECALLSTATE\_ constants**](linecallstate--constants.md).</span></span>



| <span data-ttu-id="11c26-116">dwParam1</span><span class="sxs-lookup"><span data-stu-id="11c26-116">dwParam1</span></span>                                                                                                                                                                                             | <span data-ttu-id="11c26-117">Significado</span><span class="sxs-lookup"><span data-stu-id="11c26-117">Meaning</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <span data-ttu-id="11c26-118"><dt>**LINECALLSTATE \_ ocupado**</dt></span><span class="sxs-lookup"><span data-stu-id="11c26-118"><dt>**LINECALLSTATE\_BUSY**</dt></span></span> </dl>                         | <span data-ttu-id="11c26-119">*dwParam2* contiene detalles sobre el modo ocupado.</span><span class="sxs-lookup"><span data-stu-id="11c26-119">*dwParam2* contains details about the busy mode.</span></span> <span data-ttu-id="11c26-120">Este parámetro utiliza una de las [**\_ constantes de LINEBUSYMODE**](linebusymode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="11c26-120">This parameter uses one of the [**LINEBUSYMODE\_ constants**](linebusymode--constants.md).</span></span><br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <span data-ttu-id="11c26-121"><dt>**LINECALLSTATE \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="11c26-121"><dt>**LINECALLSTATE\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="11c26-122">*dwParam2* contiene detalles sobre el modo conectado.</span><span class="sxs-lookup"><span data-stu-id="11c26-122">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="11c26-123">Este parámetro utiliza una de las [**\_ constantes de LINECONNECTEDMODE**](lineconnectedmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="11c26-123">This parameter uses one of the [**LINECONNECTEDMODE\_ constants**](lineconnectedmode--constants.md).</span></span><br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <span data-ttu-id="11c26-124"><dt>**LINECALLSTATE \_ DItono**</dt></span><span class="sxs-lookup"><span data-stu-id="11c26-124"><dt>**LINECALLSTATE\_DIALTONE**</dt></span></span> </dl>             | <span data-ttu-id="11c26-125">*dwParam2* contiene detalles sobre el modo de tono de marcado.</span><span class="sxs-lookup"><span data-stu-id="11c26-125">*dwParam2* contains details about the dial tone mode.</span></span> <span data-ttu-id="11c26-126">Este parámetro utiliza una de las [**\_ constantes de LINEDIALTONEMODE**](linedialtonemode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="11c26-126">This parameter uses one of the [**LINEDIALTONEMODE\_ constants**](linedialtonemode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <span data-ttu-id="11c26-127"><dt>**oferta de LINECALLSTATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="11c26-127"><dt>**LINECALLSTATE\_OFFERING**</dt></span></span> </dl>             | <span data-ttu-id="11c26-128">*dwParam2* contiene detalles sobre el modo conectado.</span><span class="sxs-lookup"><span data-stu-id="11c26-128">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="11c26-129">Este parámetro utiliza una de las [**\_ constantes de LINEOFFERINGMODE**](lineofferingmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="11c26-129">This parameter uses one of the [**LINEOFFERINGMODE\_ constants**](lineofferingmode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <span data-ttu-id="11c26-130"><dt>**LINECALLSTATE \_ SPECIALINFO**</dt></span><span class="sxs-lookup"><span data-stu-id="11c26-130"><dt>**LINECALLSTATE\_SPECIALINFO**</dt></span></span> </dl>    | <span data-ttu-id="11c26-131">*dwParam2* contiene los detalles sobre el modo de información especial.</span><span class="sxs-lookup"><span data-stu-id="11c26-131">*dwParam2* contains the details about the special information mode.</span></span> <span data-ttu-id="11c26-132">Este parámetro utiliza una de las [**\_ constantes de LINESPECIALINFO**](linespecialinfo--constants.md).</span><span class="sxs-lookup"><span data-stu-id="11c26-132">This parameter uses one of the [**LINESPECIALINFO\_ constants**](linespecialinfo--constants.md).</span></span><br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <span data-ttu-id="11c26-133"><dt>**LINECALLSTATE \_ DESconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="11c26-133"><dt>**LINECALLSTATE\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="11c26-134">*dwParam2* contiene detalles sobre el modo de desconexión.</span><span class="sxs-lookup"><span data-stu-id="11c26-134">*dwParam2* contains details about the disconnect mode.</span></span> <span data-ttu-id="11c26-135">Este parámetro utiliza una de las [**\_ constantes de LINEDISCONNECTMODE**](linedisconnectmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="11c26-135">This parameter uses one of the [**LINEDISCONNECTMODE\_ constants**](linedisconnectmode--constants.md).</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="11c26-136">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="11c26-136">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="11c26-137">Información dependiente del estado de la llamada.</span><span class="sxs-lookup"><span data-stu-id="11c26-137">Call-state-dependent information.</span></span> <span data-ttu-id="11c26-138">Vea *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="11c26-138">See *dwParam1*.</span></span>

> [!Note]  
> <span data-ttu-id="11c26-139">En los casos en los que una respuesta *diferida* sea adecuada, use LINEDISCONNECTMODE \_ TEMPFAILURE.</span><span class="sxs-lookup"><span data-stu-id="11c26-139">In circumstances where a *delayed* response is appropriate, use LINEDISCONNECTMODE\_TEMPFAILURE.</span></span> <span data-ttu-id="11c26-140">Si una respuesta *bloqueo* es adecuada, use LINEDISCONNECT \_ blocked.</span><span class="sxs-lookup"><span data-stu-id="11c26-140">Where a *blocklisted* response is appropriate, use LINEDISCONNECT\_BLOCKED.</span></span> <span data-ttu-id="11c26-141">Para obtener más información, [**vea \_ constantes LINEDISCONNECTMODE**](linedisconnectmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="11c26-141">For further information, see [**LINEDISCONNECTMODE\_ Constants**](linedisconnectmode--constants.md).</span></span>

 

<span data-ttu-id="11c26-142">Si *dwParam1* es LINECALLSTATE \_ Conference, *DwParam2* contiene el parámetro *hConfCall* de la llamada primaria de la Conferencia de la que el sujeto *hCall* es miembro.</span><span class="sxs-lookup"><span data-stu-id="11c26-142">If *dwParam1* is LINECALLSTATE\_CONFERENCED, *dwParam2* contains the *hConfCall* parameter of the parent call of the conference of which the subject *hCall* is a member.</span></span> <span data-ttu-id="11c26-143">Si la llamada especificada en *dwParam2* no se consideró anteriormente en la aplicación para que fuera una llamada de conferencia primaria (*hConfCall*, la aplicación debe hacerlo como resultado de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="11c26-143">If the call specified in *dwParam2* was not previously considered by the application to be a parent conference call (*hConfCall*, the application must do so as a result of this message.</span></span> <span data-ttu-id="11c26-144">Si la aplicación no tiene un identificador a la llamada primaria de la Conferencia (porque ha llamado previamente a [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) en ese identificador) *dwParam2* se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="11c26-144">If the application does not have a handle to the parent call of the conference (because it has previously called [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) on that handle) *dwParam2* is set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="11c26-145">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="11c26-145">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="11c26-146">Si es cero, este parámetro indica que no ha habido ningún cambio en el privilegio de la aplicación para la llamada.</span><span class="sxs-lookup"><span data-stu-id="11c26-146">If zero, this parameter indicates that there has been no change in the application's privilege for the call.</span></span>

<span data-ttu-id="11c26-147">Si es distinto de cero, especifica el privilegio de la aplicación para la llamada.</span><span class="sxs-lookup"><span data-stu-id="11c26-147">If nonzero, it specifies the application's privilege for the call.</span></span> <span data-ttu-id="11c26-148">Esto sucede en las siguientes situaciones: (1) la primera vez que se asigna a la aplicación un identificador a esta llamada; (2) cuando la aplicación es el destino de una entrega de llamada (incluso si la aplicación ya era propietaria de la llamada).</span><span class="sxs-lookup"><span data-stu-id="11c26-148">This occurs in the following situations: (1) The first time that the application is given a handle to this call; (2) When the application is the target of a call handoff (even if the application already was an owner of the call).</span></span> <span data-ttu-id="11c26-149">Este parámetro utiliza una de las [**\_ constantes LINECALLPRIVILEGE**](linecallprivilege--constants.md)siguientes.</span><span class="sxs-lookup"><span data-stu-id="11c26-149">This parameter uses one of the following [**LINECALLPRIVILEGE\_ constants**](linecallprivilege--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11c26-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11c26-150">Return value</span></span>

<span data-ttu-id="11c26-151">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="11c26-151">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="11c26-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11c26-152">Remarks</span></span>

<span data-ttu-id="11c26-153">Este mensaje se envía a cualquier aplicación que tenga un identificador para la llamada.</span><span class="sxs-lookup"><span data-stu-id="11c26-153">This message is sent to any application that has a handle for the call.</span></span> <span data-ttu-id="11c26-154">El mensaje **line \_ CALLSTATE** también notifica a las aplicaciones que supervisan las llamadas en una línea sobre la existencia y el estado de las llamadas salientes establecidas por otras aplicaciones o manualmente por el usuario (por ejemplo, en un dispositivo telefónico conectado).</span><span class="sxs-lookup"><span data-stu-id="11c26-154">The **LINE\_CALLSTATE** message also notifies applications that monitor calls on a line about the existence and state of outbound calls established by other applications or manually by the user (for example, on an attached phone device).</span></span> <span data-ttu-id="11c26-155">El estado de la llamada de estas llamadas refleja el estado real de la llamada, que no es *ofrecer*.</span><span class="sxs-lookup"><span data-stu-id="11c26-155">The call state of such calls reflects the actual state of the call, which is not *offering*.</span></span> <span data-ttu-id="11c26-156">Al examinar el estado de la llamada, la aplicación puede determinar si la llamada es una llamada entrante que debe responderse o no.</span><span class="sxs-lookup"><span data-stu-id="11c26-156">By examining the call state, the application can determine whether the call is an inbound call that needs to be answered or not.</span></span>

<span data-ttu-id="11c26-157">Un mensaje de **línea \_ CALLSTATE** con un estado de llamada desconocido se puede enviar a una aplicación de supervisión como resultado de un [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**LineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)o [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) correctos solicitados por otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="11c26-157">A **LINE\_CALLSTATE** message with an unknown call state can be sent to a monitoring application as the result of a successful [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference), or [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) that has been requested by another application.</span></span> <span data-ttu-id="11c26-158">Al mismo tiempo que se envía a la aplicación que realiza la solicitud una [**\_ respuesta de línea**](line-reply.md) (Success) para la operación solicitada, se envía a todas las aplicaciones de supervisión de la línea el mensaje **\_ CALLSTATE** (Unknown) de la línea.</span><span class="sxs-lookup"><span data-stu-id="11c26-158">At the same time that the requesting application is sent a [**LINE\_REPLY**](line-reply.md) (success) for the requested operation, any monitoring applications on the line are sent the **LINE\_CALLSTATE** (unknown) message.</span></span> <span data-ttu-id="11c26-159">Un mensaje de **\_ CALLSTATE de línea** que indica que el estado de la llamada "real" de la llamada recién generada se envía (utilizando la información proporcionada por el proveedor de servicios) a las aplicaciones que se solicitan y supervisan poco después.</span><span class="sxs-lookup"><span data-stu-id="11c26-159">A **LINE\_CALLSTATE** message indicating the "real" call state of the newly generated call is sent (using information provided by the service provider) to the requesting and monitoring applications shortly thereafter.</span></span>

<span data-ttu-id="11c26-160">Se envía un mensaje de **\_ CALLSTATE de línea** (desconocido) a las aplicaciones de supervisión solo si [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) hace que las llamadas se resuelvan en una conferencia de tres vías.</span><span class="sxs-lookup"><span data-stu-id="11c26-160">A **LINE\_CALLSTATE** (unknown) message is sent to monitoring applications only if [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) causes calls to be resolved into a three-way conference.</span></span>

<span data-ttu-id="11c26-161">Por compatibilidad con versiones anteriores, las aplicaciones antiguas no esperan ningún valor determinado en *dwParam2* de un mensaje de LINECALLSTATE \_ Conference.</span><span class="sxs-lookup"><span data-stu-id="11c26-161">For backward compatibility, older applications are not expecting any particular value in *dwParam2* of a LINECALLSTATE\_CONFERENCED message.</span></span> <span data-ttu-id="11c26-162">Por tanto, TAPI pasa la llamada primaria *hConfCall* en *dwParam2* independientemente de la versión de la API de la aplicación que recibe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="11c26-162">TAPI therefore passes the parent call *hConfCall* in *dwParam2* regardless of the API version of the application receiving the message.</span></span> <span data-ttu-id="11c26-163">En el caso de una llamada de conferencia iniciada por el proveedor de servicios, la aplicación anterior no es consciente de que la llamada primaria se ha convertido en una llamada de conferencia, a menos que se trate de examinar espontáneamente otra información (por ejemplo, llamar a [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).</span><span class="sxs-lookup"><span data-stu-id="11c26-163">In the case of a conference call initiated by the service provider, the older application is not aware that the parent call has become a conference call unless it happens to spontaneously examine other information (for example, call [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).</span></span>

<span data-ttu-id="11c26-164">Este mensaje no se puede deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="11c26-164">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="11c26-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11c26-165">Requirements</span></span>



| <span data-ttu-id="11c26-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="11c26-166">Requirement</span></span> | <span data-ttu-id="11c26-167">Value</span><span class="sxs-lookup"><span data-stu-id="11c26-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="11c26-168">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="11c26-168">TAPI version</span></span><br/> | <span data-ttu-id="11c26-169">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="11c26-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="11c26-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11c26-170">Header</span></span><br/>       | <dl> <span data-ttu-id="11c26-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="11c26-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11c26-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="11c26-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c26-173">**respuesta de línea \_**</span><span class="sxs-lookup"><span data-stu-id="11c26-173">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="11c26-174">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="11c26-174">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="11c26-175">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="11c26-175">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="11c26-176">**LINEDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="11c26-176">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[<span data-ttu-id="11c26-177">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="11c26-177">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="11c26-178">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="11c26-178">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="11c26-179">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="11c26-179">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[<span data-ttu-id="11c26-180">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="11c26-180">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="11c26-181">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="11c26-181">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="11c26-182">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="11c26-182">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[<span data-ttu-id="11c26-183">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="11c26-183">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="11c26-184">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="11c26-184">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[<span data-ttu-id="11c26-185">**lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="11c26-185">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 




