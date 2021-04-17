---
description: Notifica a las aplicaciones que se ha denegado el permiso para suspender el equipo.
ms.assetid: 0f68628f-9d38-45ca-9487-95bf62075e00
title: Evento PBT_APMQUERYSUSPENDFAILED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1544cd5ed94ae0228c739e2ddb576b0bd77146eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677897"
---
# <a name="pbt_apmquerysuspendfailed-event"></a><span data-ttu-id="4a730-103">\_Evento PBT APMQUERYSUSPENDFAILED</span><span class="sxs-lookup"><span data-stu-id="4a730-103">PBT\_APMQUERYSUSPENDFAILED event</span></span>

<span data-ttu-id="4a730-104">\[PBT \_ APMQUERYSUSPENDFAILED está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="4a730-104">\[PBT\_APMQUERYSUSPENDFAILED is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4a730-105">Se ha quitado la compatibilidad con este evento en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4a730-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="4a730-106">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="4a730-106">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="4a730-107">Notifica a las aplicaciones que se ha denegado el permiso para suspender el equipo.</span><span class="sxs-lookup"><span data-stu-id="4a730-107">Notifies applications that permission to suspend the computer was denied.</span></span> <span data-ttu-id="4a730-108">Este evento se emite si cualquier aplicación o controlador devolvió una **consulta de difusión \_ \_ Deny** a un evento [PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="4a730-108">This event is broadcast if any application or driver returned **BROADCAST\_QUERY\_DENY** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="4a730-109">Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="4a730-109">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="4a730-110">Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="4a730-110">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPENDFAILED
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="4a730-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a730-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a730-112">*identificador*</span><span class="sxs-lookup"><span data-stu-id="4a730-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="4a730-113">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="4a730-113">A handle to window.</span></span>

<span data-ttu-id="4a730-114"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="4a730-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="4a730-115">Value</span><span class="sxs-lookup"><span data-stu-id="4a730-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="4a730-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4a730-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="4a730-117"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="4a730-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="4a730-118">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4a730-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="4a730-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="4a730-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="4a730-120">Value</span><span class="sxs-lookup"><span data-stu-id="4a730-120">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="4a730-121">Significado</span><span class="sxs-lookup"><span data-stu-id="4a730-121">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPENDFAILED"></span><span id="pbt_apmquerysuspendfailed"></span><dl> <span data-ttu-id="4a730-122"><dt>**PBT \_ APMQUERYSUSPENDFAILED**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="4a730-122"><dt>**PBT\_APMQUERYSUSPENDFAILED**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="4a730-123">Identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="4a730-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4a730-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a730-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a730-125">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4a730-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a730-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a730-126">Return value</span></span>

<span data-ttu-id="4a730-127">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4a730-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a730-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a730-128">Remarks</span></span>

<span data-ttu-id="4a730-129">Las aplicaciones normalmente responden a este evento reanudando el funcionamiento normal.</span><span class="sxs-lookup"><span data-stu-id="4a730-129">Applications typically respond to this event by resuming normal operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a730-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a730-130">Requirements</span></span>



| <span data-ttu-id="4a730-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a730-131">Requirement</span></span> | <span data-ttu-id="4a730-132">Value</span><span class="sxs-lookup"><span data-stu-id="4a730-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a730-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a730-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4a730-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4a730-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4a730-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a730-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4a730-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a730-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4a730-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4a730-137">End of client support</span></span><br/>    | <span data-ttu-id="4a730-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a730-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="4a730-139">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="4a730-139">End of server support</span></span><br/>    | <span data-ttu-id="4a730-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4a730-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="4a730-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a730-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a730-142"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a730-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a730-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a730-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a730-144">Administración de energía</span><span class="sxs-lookup"><span data-stu-id="4a730-144">Power Management</span></span>](power-management-portal.md)
</dt> <dt>

[<span data-ttu-id="4a730-145">Eventos de administración de energía</span><span class="sxs-lookup"><span data-stu-id="4a730-145">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="4a730-146">PBT \_ APMQUERYSUSPEND</span><span class="sxs-lookup"><span data-stu-id="4a730-146">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="4a730-147">**POWERBROADCAST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4a730-147">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




