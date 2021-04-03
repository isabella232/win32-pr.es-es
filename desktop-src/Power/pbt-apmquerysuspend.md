---
description: Solicita permiso para suspender el equipo. Una aplicación que concede este permiso tiene que realizar los preparativos para la suspensión antes de volver.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: Evento PBT_APMQUERYSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909690"
---
# <a name="pbt_apmquerysuspend-event"></a><span data-ttu-id="ef511-104">\_Evento PBT APMQUERYSUSPEND</span><span class="sxs-lookup"><span data-stu-id="ef511-104">PBT\_APMQUERYSUSPEND event</span></span>

<span data-ttu-id="ef511-105">\[PBT \_ APMQUERYSUSPEND está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="ef511-105">\[PBT\_APMQUERYSUSPEND is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ef511-106">Se ha quitado la compatibilidad con este evento en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ef511-106">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="ef511-107">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="ef511-107">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="ef511-108">Solicita permiso para suspender el equipo.</span><span class="sxs-lookup"><span data-stu-id="ef511-108">Requests permission to suspend the computer.</span></span> <span data-ttu-id="ef511-109">Una aplicación que concede este permiso tiene que realizar los preparativos para la suspensión antes de volver.</span><span class="sxs-lookup"><span data-stu-id="ef511-109">An application that grants permission should carry out preparations for the suspension before returning.</span></span>

<span data-ttu-id="ef511-110">Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="ef511-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="ef511-111">Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="ef511-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
```



## <a name="parameters"></a><span data-ttu-id="ef511-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef511-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef511-113">*identificador*</span><span class="sxs-lookup"><span data-stu-id="ef511-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ef511-114">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ef511-114">A handle to window.</span></span>

<span data-ttu-id="ef511-115"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="ef511-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="ef511-116">Value</span><span class="sxs-lookup"><span data-stu-id="ef511-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="ef511-117">Significado</span><span class="sxs-lookup"><span data-stu-id="ef511-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="ef511-118"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="ef511-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="ef511-119">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ef511-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="ef511-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="ef511-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="ef511-121">Value</span><span class="sxs-lookup"><span data-stu-id="ef511-121">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="ef511-122">Significado</span><span class="sxs-lookup"><span data-stu-id="ef511-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <span data-ttu-id="ef511-123"><dt>**PBT \_ APMQUERYSUSPEND**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="ef511-123"><dt>**PBT\_APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ef511-124">Identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="ef511-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ef511-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef511-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef511-126">Marcas de acción.</span><span class="sxs-lookup"><span data-stu-id="ef511-126">The action flags.</span></span> <span data-ttu-id="ef511-127">Si el bit 0 es 1, la aplicación puede preguntar al usuario para obtener instrucciones sobre cómo prepararse para la suspensión; de lo contrario, la aplicación debe prepararse sin la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="ef511-127">If bit 0 is 1, the application can prompt the user for directions on how to prepare for the suspension; otherwise, the application must prepare without user interaction.</span></span> <span data-ttu-id="ef511-128">Todos los demás valores de bit están reservados.</span><span class="sxs-lookup"><span data-stu-id="ef511-128">All other bit values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef511-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef511-129">Return value</span></span>

<span data-ttu-id="ef511-130">Devuelva **true** para permitir que la solicitud se suspenda.</span><span class="sxs-lookup"><span data-stu-id="ef511-130">Return **TRUE** to grant the request to suspend.</span></span> <span data-ttu-id="ef511-131">Para denegar la solicitud, devuelva la **consulta de difusión \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="ef511-131">To deny the request, return **BROADCAST\_QUERY\_DENY**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef511-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef511-132">Remarks</span></span>

<span data-ttu-id="ef511-133">Una aplicación debe procesar este evento lo más rápido posible.</span><span class="sxs-lookup"><span data-stu-id="ef511-133">An application should process this event as quickly as possible.</span></span> <span data-ttu-id="ef511-134">La aplicación puede solicitar al usuario instrucciones sobre cómo prepararse para la suspensión solo si se establece el bit 0 en el parámetro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="ef511-134">The application can prompt the user for directions on how to prepare for suspension only if bit 0 in the *Flags* parameter is set.</span></span> <span data-ttu-id="ef511-135">Sin embargo, si se emite este mensaje porque el usuario está cerrando la tapa del portátil, no será posible preguntar al usuario.</span><span class="sxs-lookup"><span data-stu-id="ef511-135">However, if this message is issued because the user is closing the laptop lid, it will not be possible to prompt the user.</span></span> <span data-ttu-id="ef511-136">Las aplicaciones deben respetar que el usuario espera un determinado comportamiento al cerrar la tapa del portátil o presionar el botón de encendido y permitir que la transición se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="ef511-136">Applications should respect that the user expects a certain behavior when they close the laptop lid or press the power button and allow the transition to succeed.</span></span>

<span data-ttu-id="ef511-137">El sistema permite aproximadamente 20 segundos para que una aplicación Quite el mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) que está enviando el \_ evento PBT APMQUERYSUSPEND desde la cola de mensajes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ef511-137">The system allows approximately 20 seconds for an application to remove the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message that is sending the PBT\_APMQUERYSUSPEND event from the application's message queue.</span></span> <span data-ttu-id="ef511-138">Si una aplicación no quita el mensaje de su cola en menos de 20 segundos, el sistema asumirá que la aplicación está en un estado que no responde y que la aplicación acepta la solicitud de suspensión.</span><span class="sxs-lookup"><span data-stu-id="ef511-138">If an application does not remove the message from its queue in less than 20 seconds, the system will assume that the application is in a non-responsive state, and that the application agrees to the sleep request.</span></span> <span data-ttu-id="ef511-139">Las aplicaciones que no procesan sus colas de mensajes pueden interrumpir sus operaciones.</span><span class="sxs-lookup"><span data-stu-id="ef511-139">Applications that do not process their message queues may have their operations interrupted.</span></span> <span data-ttu-id="ef511-140">Después de quitar el mensaje de la cola de mensajes, una aplicación puede tardar tanto tiempo como sea necesario para realizar las operaciones necesarias antes de entrar en el estado de suspensión.</span><span class="sxs-lookup"><span data-stu-id="ef511-140">After it removes the message from the message queue, an application can take as much time as needed to perform any required operations before entering the sleep state.</span></span> <span data-ttu-id="ef511-141">En este momento, se deben realizar las operaciones que podrían tardar más de 20 segundos, ya que el sistema solo permite 20 segundos para que las operaciones se completen durante el procesamiento de [ \_ APMSUSPEND de PBT](pbt-apmsuspend.md) .</span><span class="sxs-lookup"><span data-stu-id="ef511-141">Any operations that could take longer then 20 seconds should be performed at this time, since the system allows only 20 seconds for operations to complete during [PBT\_APMSUSPEND](pbt-apmsuspend.md) processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef511-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef511-142">Requirements</span></span>



| <span data-ttu-id="ef511-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef511-143">Requirement</span></span> | <span data-ttu-id="ef511-144">Value</span><span class="sxs-lookup"><span data-stu-id="ef511-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef511-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef511-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ef511-146">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ef511-146">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ef511-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef511-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ef511-148">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef511-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ef511-149">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ef511-149">End of client support</span></span><br/>    | <span data-ttu-id="ef511-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ef511-150">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="ef511-151">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="ef511-151">End of server support</span></span><br/>    | <span data-ttu-id="ef511-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ef511-152">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="ef511-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef511-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef511-154"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef511-154"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef511-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef511-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef511-156">Eventos de reactivación del sistema</span><span class="sxs-lookup"><span data-stu-id="ef511-156">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="ef511-157">Eventos de administración de energía</span><span class="sxs-lookup"><span data-stu-id="ef511-157">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="ef511-158">PBT \_ APMSUSPEND</span><span class="sxs-lookup"><span data-stu-id="ef511-158">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="ef511-159">**POWERBROADCAST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ef511-159">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




