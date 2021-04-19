---
description: Notifica a las aplicaciones que la energía de la batería es baja.
ms.assetid: ef24b8cf-d801-4452-a03c-3f2bdbdd7e5d
title: Evento PBT_APMBATTERYLOW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64884f9bb01e37883e1be61b2de88862e8b119fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677898"
---
# <a name="pbt_apmbatterylow-event"></a><span data-ttu-id="5c2d9-103">\_Evento PBT APMBATTERYLOW</span><span class="sxs-lookup"><span data-stu-id="5c2d9-103">PBT\_APMBATTERYLOW event</span></span>

<span data-ttu-id="5c2d9-104">\[PBT \_ APMBATTERYLOW está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="5c2d9-104">\[PBT\_APMBATTERYLOW is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5c2d9-105">Se ha quitado la compatibilidad con este evento en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5c2d9-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="5c2d9-106">Use [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="5c2d9-106">Use [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) instead.\]</span></span>

<span data-ttu-id="5c2d9-107">Notifica a las aplicaciones que la energía de la batería es baja.</span><span class="sxs-lookup"><span data-stu-id="5c2d9-107">Notifies applications that the battery power is low.</span></span>

<span data-ttu-id="5c2d9-108">Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="5c2d9-108">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="5c2d9-109">Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="5c2d9-109">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMBATTERYLOW
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="5c2d9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c2d9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c2d9-111">*identificador*</span><span class="sxs-lookup"><span data-stu-id="5c2d9-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5c2d9-112">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="5c2d9-112">A handle to the window.</span></span>

<span data-ttu-id="5c2d9-113"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="5c2d9-113"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="5c2d9-114">Value</span><span class="sxs-lookup"><span data-stu-id="5c2d9-114">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="5c2d9-115">Significado</span><span class="sxs-lookup"><span data-stu-id="5c2d9-115">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="5c2d9-116"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="5c2d9-116"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="5c2d9-117">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="5c2d9-117">Message identifier.</span></span><br/> |



 

<span data-ttu-id="5c2d9-118"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="5c2d9-118"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="5c2d9-119">Value</span><span class="sxs-lookup"><span data-stu-id="5c2d9-119">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="5c2d9-120">Significado</span><span class="sxs-lookup"><span data-stu-id="5c2d9-120">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMBATTERYLOW"></span><span id="pbt_apmbatterylow"></span><dl> <span data-ttu-id="5c2d9-121"><dt>**PBT \_ APMBATTERYLOW**</dt> <dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="5c2d9-121"><dt>**PBT\_APMBATTERYLOW**</dt> <dt>9 (0x9)</dt></span></span> </dl> | <span data-ttu-id="5c2d9-122">Identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="5c2d9-122">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c2d9-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c2d9-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c2d9-124">Reserved, debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5c2d9-124">Reserved, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c2d9-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c2d9-125">Return value</span></span>

<span data-ttu-id="5c2d9-126">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5c2d9-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c2d9-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c2d9-127">Remarks</span></span>

<span data-ttu-id="5c2d9-128">Este evento se emite cuando el BIOS de APM del sistema señala una notificación de baja de la batería de APM.</span><span class="sxs-lookup"><span data-stu-id="5c2d9-128">This event is broadcast when a system's APM BIOS signals an APM battery low notification.</span></span> <span data-ttu-id="5c2d9-129">Dado que algunas implementaciones de BIOS de APM no proporcionan notificaciones cuando las baterías son bajas, este evento nunca se puede difundir en algunos equipos.</span><span class="sxs-lookup"><span data-stu-id="5c2d9-129">Because some APM BIOS implementations do not provide notifications when batteries are low, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c2d9-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c2d9-130">Requirements</span></span>



| <span data-ttu-id="5c2d9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c2d9-131">Requirement</span></span> | <span data-ttu-id="5c2d9-132">Value</span><span class="sxs-lookup"><span data-stu-id="5c2d9-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2d9-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c2d9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5c2d9-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5c2d9-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5c2d9-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c2d9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5c2d9-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c2d9-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5c2d9-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5c2d9-137">End of client support</span></span><br/>    | <span data-ttu-id="5c2d9-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5c2d9-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="5c2d9-139">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5c2d9-139">End of server support</span></span><br/>    | <span data-ttu-id="5c2d9-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5c2d9-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="5c2d9-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c2d9-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c2d9-142"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c2d9-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c2d9-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c2d9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c2d9-144">Eventos de administración de energía</span><span class="sxs-lookup"><span data-stu-id="5c2d9-144">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="5c2d9-145">**POWERBROADCAST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5c2d9-145">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




