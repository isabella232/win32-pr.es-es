---
description: Notifica a las aplicaciones que el BIOS de APM ha señalado un evento de OEM de APM.
ms.assetid: 3251ac00-41f1-44e9-a579-fa31e7c7d2ff
title: Evento PBT_APMOEMEVENT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a99b99bdaf69b1a53a24ad33cd898fd1c806694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667207"
---
# <a name="pbt_apmoemevent-event"></a><span data-ttu-id="d933d-103">\_Evento PBT APMOEMEVENT</span><span class="sxs-lookup"><span data-stu-id="d933d-103">PBT\_APMOEMEVENT event</span></span>

<span data-ttu-id="d933d-104">\[PBT \_ APMOEMEVENT está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="d933d-104">\[PBT\_APMOEMEVENT is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d933d-105">Se ha quitado la compatibilidad con este evento en Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="d933d-105">Support for this event was removed in Windows Vista.\]</span></span>

<span data-ttu-id="d933d-106">Notifica a las aplicaciones que el BIOS de APM ha señalado un evento de OEM de APM.</span><span class="sxs-lookup"><span data-stu-id="d933d-106">Notifies applications that the APM BIOS has signaled an APM OEM event.</span></span>

<span data-ttu-id="d933d-107">Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="d933d-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="d933d-108">Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="d933d-108">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMOEMEVENT
            LPARAM lParam); // OEM event code
```



## <a name="parameters"></a><span data-ttu-id="d933d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d933d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d933d-110">*identificador*</span><span class="sxs-lookup"><span data-stu-id="d933d-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d933d-111">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="d933d-111">A handle to window.</span></span>

<span data-ttu-id="d933d-112"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="d933d-112"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="d933d-113">Value</span><span class="sxs-lookup"><span data-stu-id="d933d-113">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="d933d-114">Significado</span><span class="sxs-lookup"><span data-stu-id="d933d-114">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="d933d-115"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="d933d-115"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="d933d-116">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d933d-116">Message identifier.</span></span><br/> |



 

<span data-ttu-id="d933d-117"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="d933d-117"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="d933d-118">Value</span><span class="sxs-lookup"><span data-stu-id="d933d-118">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="d933d-119">Significado</span><span class="sxs-lookup"><span data-stu-id="d933d-119">Meaning</span></span>                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMOEMEVENT"></span><span id="pbt_apmoemevent"></span><dl> <span data-ttu-id="d933d-120"><dt>**PBT \_ APMOEMEVENT**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="d933d-120"><dt>**PBT\_APMOEMEVENT**</dt> <dt>11 (0xB)</dt></span></span> </dl> | <span data-ttu-id="d933d-121">Identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="d933d-121">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d933d-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d933d-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d933d-123">Código de evento definido por el OEM que señaló el BIOS de APM del sistema.</span><span class="sxs-lookup"><span data-stu-id="d933d-123">The OEM-defined event code that was signaled by the system's APM BIOS.</span></span> <span data-ttu-id="d933d-124">Los códigos de evento de OEM están en el intervalo 0200h-02FFh.</span><span class="sxs-lookup"><span data-stu-id="d933d-124">OEM event codes are in the range 0200h - 02FFh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d933d-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d933d-125">Return value</span></span>

<span data-ttu-id="d933d-126">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d933d-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d933d-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d933d-127">Remarks</span></span>

<span data-ttu-id="d933d-128">Dado que no todas las implementaciones de BIOS de APM proporcionan notificaciones de eventos de OEM, este evento nunca se puede difundir en algunos equipos.</span><span class="sxs-lookup"><span data-stu-id="d933d-128">Because not all APM BIOS implementations provide OEM event notifications, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d933d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d933d-129">Requirements</span></span>



| <span data-ttu-id="d933d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d933d-130">Requirement</span></span> | <span data-ttu-id="d933d-131">Value</span><span class="sxs-lookup"><span data-stu-id="d933d-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d933d-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d933d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d933d-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d933d-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d933d-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d933d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d933d-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d933d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d933d-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d933d-136">End of client support</span></span><br/>    | <span data-ttu-id="d933d-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d933d-137">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="d933d-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d933d-138">End of server support</span></span><br/>    | <span data-ttu-id="d933d-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d933d-139">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="d933d-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d933d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d933d-141"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d933d-141"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d933d-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="d933d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d933d-143">Eventos de administración de energía</span><span class="sxs-lookup"><span data-stu-id="d933d-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="d933d-144">**POWERBROADCAST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d933d-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




