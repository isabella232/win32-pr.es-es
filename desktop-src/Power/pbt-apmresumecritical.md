---
description: Notifica a las aplicaciones que el sistema ha reanudado la operación.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: Evento PBT_APMRESUMECRITICAL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4a76e163f2e61e723f4df6572254e8ef89b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667206"
---
# <a name="pbt_apmresumecritical-event"></a><span data-ttu-id="6bb66-103">\_Evento PBT APMRESUMECRITICAL</span><span class="sxs-lookup"><span data-stu-id="6bb66-103">PBT\_APMRESUMECRITICAL event</span></span>

<span data-ttu-id="6bb66-104">\[PBT \_ APMRESUMECRITICAL está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6bb66-104">\[PBT\_APMRESUMECRITICAL is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6bb66-105">Se ha quitado la compatibilidad con este evento en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6bb66-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="6bb66-106">Use [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="6bb66-106">Use [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) instead.\]</span></span>

<span data-ttu-id="6bb66-107">Notifica a las aplicaciones que el sistema ha reanudado la operación.</span><span class="sxs-lookup"><span data-stu-id="6bb66-107">Notifies applications that the system has resumed operation.</span></span> <span data-ttu-id="6bb66-108">Este evento puede indicar que algunas o todas las aplicaciones no han recibido un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) .</span><span class="sxs-lookup"><span data-stu-id="6bb66-108">This event can indicate that some or all applications did not receive a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event.</span></span> <span data-ttu-id="6bb66-109">Por ejemplo, este evento se puede difundir después de una suspensión crítica causada por una batería con error.</span><span class="sxs-lookup"><span data-stu-id="6bb66-109">For example, this event can be broadcast after a critical suspension caused by a failing battery.</span></span>

<span data-ttu-id="6bb66-110">Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="6bb66-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="6bb66-111">Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="6bb66-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMECRITICAL
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="6bb66-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6bb66-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bb66-113">*identificador*</span><span class="sxs-lookup"><span data-stu-id="6bb66-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6bb66-114">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6bb66-114">A handle to window.</span></span>

<span data-ttu-id="6bb66-115"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="6bb66-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="6bb66-116">Value</span><span class="sxs-lookup"><span data-stu-id="6bb66-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="6bb66-117">Significado</span><span class="sxs-lookup"><span data-stu-id="6bb66-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="6bb66-118"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb66-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="6bb66-119">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="6bb66-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="6bb66-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="6bb66-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="6bb66-121">Value</span><span class="sxs-lookup"><span data-stu-id="6bb66-121">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="6bb66-122">Significado</span><span class="sxs-lookup"><span data-stu-id="6bb66-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <span data-ttu-id="6bb66-123"><dt>**PBT \_ APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb66-123"><dt>**PBT\_APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="6bb66-124">Identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="6bb66-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6bb66-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6bb66-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6bb66-126">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6bb66-126">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bb66-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bb66-127">Return value</span></span>

<span data-ttu-id="6bb66-128">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6bb66-128">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bb66-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6bb66-129">Remarks</span></span>

<span data-ttu-id="6bb66-130">Dado que se produce una suspensión crítica sin notificación previa, es posible que los recursos y los datos disponibles anteriormente no estén presentes cuando la aplicación reciba este evento.</span><span class="sxs-lookup"><span data-stu-id="6bb66-130">Because a critical suspension occurs without prior notification, resources and data previously available may not be present when the application receives this event.</span></span> <span data-ttu-id="6bb66-131">La aplicación debe intentar restaurar su estado lo mejor que pueda.</span><span class="sxs-lookup"><span data-stu-id="6bb66-131">The application should attempt to restore its state to the best of its ability.</span></span> <span data-ttu-id="6bb66-132">Mientras se encuentra en una suspensión crítica, el sistema mantiene el estado de la DRAM y los discos duros locales, pero es posible que no mantenga conexiones netas.</span><span class="sxs-lookup"><span data-stu-id="6bb66-132">While in a critical suspension, the system maintains the state of the DRAM and local hard disks, but may not maintain net connections.</span></span> <span data-ttu-id="6bb66-133">Es posible que una aplicación tenga que tomar medidas en relación con los archivos que estaban abiertos en la red antes de la suspensión crítica.</span><span class="sxs-lookup"><span data-stu-id="6bb66-133">An application may need to take action with respect to files that were open on the network before critical suspension.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb66-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bb66-134">Requirements</span></span>



| <span data-ttu-id="6bb66-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bb66-135">Requirement</span></span> | <span data-ttu-id="6bb66-136">Value</span><span class="sxs-lookup"><span data-stu-id="6bb66-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb66-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bb66-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb66-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6bb66-138">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6bb66-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bb66-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb66-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6bb66-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6bb66-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6bb66-141">End of client support</span></span><br/>    | <span data-ttu-id="6bb66-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6bb66-142">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="6bb66-143">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6bb66-143">End of server support</span></span><br/>    | <span data-ttu-id="6bb66-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6bb66-144">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="6bb66-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bb66-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bb66-146"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb66-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb66-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bb66-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb66-148">Eventos de reactivación del sistema</span><span class="sxs-lookup"><span data-stu-id="6bb66-148">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="6bb66-149">Eventos de administración de energía</span><span class="sxs-lookup"><span data-stu-id="6bb66-149">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="6bb66-150">**POWERBROADCAST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="6bb66-150">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




