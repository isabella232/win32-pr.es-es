---
description: Notifica a las aplicaciones que el sistema se está reanudando de la suspensión o hibernación. Este evento se entrega cada vez que el sistema se reanuda y no indica si un usuario está presente.
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: Evento PBT_APMRESUMEAUTOMATIC (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a481dee356c85b3831fcace0c1ff127b0b276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909689"
---
# <a name="pbt_apmresumeautomatic-event"></a><span data-ttu-id="4ebc4-104">\_Evento PBT APMRESUMEAUTOMATIC</span><span class="sxs-lookup"><span data-stu-id="4ebc4-104">PBT\_APMRESUMEAUTOMATIC event</span></span>

<span data-ttu-id="4ebc4-105">Notifica a las aplicaciones que el sistema se está reanudando de la suspensión o hibernación.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-105">Notifies applications that the system is resuming from sleep or hibernation.</span></span> <span data-ttu-id="4ebc4-106">Este evento se entrega cada vez que el sistema se reanuda y no indica si un usuario está presente.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-106">This event is delivered every time the system resumes and does not indicate whether a user is present.</span></span>

<span data-ttu-id="4ebc4-107">Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="4ebc4-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="4ebc4-108">Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-108">The *wParam* and *lParam* parameters are set as described following.</span></span>

> [!Note]  
> <span data-ttu-id="4ebc4-109">En los sistemas Windows 10, versión 1507 o posterior, si el sistema se está reanudando de la suspensión solo para entrar inmediatamente en hibernación, este evento no se entrega.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-109">In Windows 10, version 1507 systems or later, if the system is resuming from sleep only to immediately enter hibernation, this event is not delivered.</span></span> <span data-ttu-id="4ebc4-110">En este caso, no se envía un mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="4ebc4-110">A [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message is not sent in this case.</span></span>

 


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMEAUTOMATIC
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="4ebc4-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ebc4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ebc4-112">*identificador*</span><span class="sxs-lookup"><span data-stu-id="4ebc4-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="4ebc4-113">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-113">A handle to window.</span></span>

<span data-ttu-id="4ebc4-114"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="4ebc4-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="4ebc4-115">Value</span><span class="sxs-lookup"><span data-stu-id="4ebc4-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="4ebc4-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4ebc4-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="4ebc4-117"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="4ebc4-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="4ebc4-118">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="4ebc4-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="4ebc4-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="4ebc4-120">Value</span><span class="sxs-lookup"><span data-stu-id="4ebc4-120">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="4ebc4-121">Significado</span><span class="sxs-lookup"><span data-stu-id="4ebc4-121">Meaning</span></span>                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="4ebc4-122"><dt>**PBT \_ APMRESUMEAUTOMATIC**</dt> <dt>18 (0X12)</dt></span><span class="sxs-lookup"><span data-stu-id="4ebc4-122"><dt>**PBT\_APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="4ebc4-123">Identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4ebc4-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ebc4-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ebc4-125">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ebc4-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ebc4-126">Return value</span></span>

<span data-ttu-id="4ebc4-127">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ebc4-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ebc4-128">Remarks</span></span>

<span data-ttu-id="4ebc4-129">Si el sistema detecta cualquier actividad de usuario después de difundir PBT \_ APMRESUMEAUTOMATIC, difundirá un [evento \_ APMRESUMESUSPEND de PBT](pbt-apmresumesuspend.md) para que las aplicaciones sepan que pueden reanudar la interacción completa con el usuario.</span><span class="sxs-lookup"><span data-stu-id="4ebc4-129">If the system detects any user activity after broadcasting PBT\_APMRESUMEAUTOMATIC, it will broadcast a [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) event to let applications know they can resume full interaction with the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ebc4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ebc4-130">Requirements</span></span>



| <span data-ttu-id="4ebc4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ebc4-131">Requirement</span></span> | <span data-ttu-id="4ebc4-132">Value</span><span class="sxs-lookup"><span data-stu-id="4ebc4-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ebc4-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ebc4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4ebc4-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4ebc4-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4ebc4-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ebc4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4ebc4-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4ebc4-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4ebc4-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ebc4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ebc4-138"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ebc4-138"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ebc4-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ebc4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ebc4-140">Eventos de reactivación del sistema</span><span class="sxs-lookup"><span data-stu-id="4ebc4-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="4ebc4-141">Eventos de administración de energía</span><span class="sxs-lookup"><span data-stu-id="4ebc4-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="4ebc4-142">PBT \_ APMRESUMESUSPEND</span><span class="sxs-lookup"><span data-stu-id="4ebc4-142">PBT\_APMRESUMESUSPEND</span></span>](pbt-apmresumesuspend.md)
</dt> <dt>

[<span data-ttu-id="4ebc4-143">**POWERBROADCAST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4ebc4-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




