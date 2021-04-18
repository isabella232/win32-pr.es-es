---
description: Notifica a las aplicaciones que el sistema ha reanudado la operación después de suspenderse.
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: Evento PBT_APMRESUMESUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d26357215853e0989851b6a9e731340a8dc2e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667205"
---
# <a name="pbt_apmresumesuspend-event"></a><span data-ttu-id="a8fb7-103">\_Evento PBT APMRESUMESUSPEND</span><span class="sxs-lookup"><span data-stu-id="a8fb7-103">PBT\_APMRESUMESUSPEND event</span></span>

<span data-ttu-id="a8fb7-104">Notifica a las aplicaciones que el sistema ha reanudado la operación después de suspenderse.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-104">Notifies applications that the system has resumed operation after being suspended.</span></span>

<span data-ttu-id="a8fb7-105">Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fb7-105">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="a8fb7-106">Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-106">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMESUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="a8fb7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8fb7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8fb7-108">*identificador*</span><span class="sxs-lookup"><span data-stu-id="a8fb7-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a8fb7-109">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-109">A handle to window.</span></span>

<span data-ttu-id="a8fb7-110"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="a8fb7-110"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="a8fb7-111">Value</span><span class="sxs-lookup"><span data-stu-id="a8fb7-111">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="a8fb7-112">Significado</span><span class="sxs-lookup"><span data-stu-id="a8fb7-112">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="a8fb7-113"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="a8fb7-113"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="a8fb7-114">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-114">Message identifier.</span></span><br/> |



 

<span data-ttu-id="a8fb7-115"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="a8fb7-115"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="a8fb7-116">Value</span><span class="sxs-lookup"><span data-stu-id="a8fb7-116">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="a8fb7-117">Significado</span><span class="sxs-lookup"><span data-stu-id="a8fb7-117">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="a8fb7-118"><dt>**PBT \_ APMRESUMESUSPEND**</dt> <dt>7 (0X7)</dt></span><span class="sxs-lookup"><span data-stu-id="a8fb7-118"><dt>**PBT\_APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt></span></span> </dl> | <span data-ttu-id="a8fb7-119">Identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-119">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a8fb7-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8fb7-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8fb7-121">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-121">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8fb7-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8fb7-122">Return value</span></span>

<span data-ttu-id="a8fb7-123">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-123">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8fb7-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8fb7-124">Remarks</span></span>

<span data-ttu-id="a8fb7-125">Una aplicación puede recibir este evento solo si recibió el evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) antes de que se suspendiera el equipo.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-125">An application can receive this event only if it received the [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended.</span></span> <span data-ttu-id="a8fb7-126">De lo contrario, la aplicación recibirá un evento [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fb7-126">Otherwise, the application will receive a [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event.</span></span>

<span data-ttu-id="a8fb7-127">Si el sistema se reactiva debido a la actividad del usuario (por ejemplo, al presionar el botón de encendido) o si el sistema detecta la interacción del usuario en la consola física (por ejemplo, la entrada del mouse o del teclado) después de activar desatendido, el sistema emite primero el evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) y, a continuación, difunde el \_ evento APMRESUMESUSPEND de PBT.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-127">If the system wakes due to user activity (such as pressing the power button) or if the system detects user interaction at the physical console (such as mouse or keyboard input) after waking unattended, the system first broadcasts the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event, then it broadcasts the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="a8fb7-128">Además, el sistema activa la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-128">In addition, the system turns on the display.</span></span> <span data-ttu-id="a8fb7-129">La aplicación debe volver a abrir los archivos que cerró cuando el sistema entró en suspensión y prepararse para los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-129">Your application should reopen files that it closed when the system entered sleep and prepare for user input.</span></span>

<span data-ttu-id="a8fb7-130">Si el sistema se reactiva debido a una señal de reactivación externa (reactivación remota), el sistema difundirá solo el evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fb7-130">If the system wakes due to an external wake signal (remote wake), the system broadcasts only the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event.</span></span> <span data-ttu-id="a8fb7-131">\_No se envía el evento PBT APMRESUMESUSPEND.</span><span class="sxs-lookup"><span data-stu-id="a8fb7-131">The PBT\_APMRESUMESUSPEND event is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8fb7-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8fb7-132">Requirements</span></span>



| <span data-ttu-id="a8fb7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8fb7-133">Requirement</span></span> | <span data-ttu-id="a8fb7-134">Value</span><span class="sxs-lookup"><span data-stu-id="a8fb7-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8fb7-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8fb7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a8fb7-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a8fb7-136">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a8fb7-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8fb7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a8fb7-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8fb7-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8fb7-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8fb7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8fb7-140"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8fb7-140"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8fb7-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8fb7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8fb7-142">Eventos de reactivación del sistema</span><span class="sxs-lookup"><span data-stu-id="a8fb7-142">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="a8fb7-143">Eventos de administración de energía</span><span class="sxs-lookup"><span data-stu-id="a8fb7-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="a8fb7-144">PBT \_ APMSUSPEND</span><span class="sxs-lookup"><span data-stu-id="a8fb7-144">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="a8fb7-145">PBT \_ APMRESUMECRITICAL</span><span class="sxs-lookup"><span data-stu-id="a8fb7-145">PBT\_APMRESUMECRITICAL</span></span>](pbt-apmresumecritical.md)
</dt> <dt>

[<span data-ttu-id="a8fb7-146">**POWERBROADCAST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a8fb7-146">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




