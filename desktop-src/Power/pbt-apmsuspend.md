---
description: Notifica a las aplicaciones que el equipo está a punto de entrar en estado suspendido.
ms.assetid: 61b177a0-4cff-4740-bed8-a46c06c43be8
title: Evento PBT_APMSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6982e00565329c85e06765879b9b72b07fe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276831"
---
# <a name="pbt_apmsuspend-event"></a><span data-ttu-id="77d0d-103">\_Evento PBT APMSUSPEND</span><span class="sxs-lookup"><span data-stu-id="77d0d-103">PBT\_APMSUSPEND event</span></span>

<span data-ttu-id="77d0d-104">Notifica a las aplicaciones que el equipo está a punto de entrar en estado suspendido.</span><span class="sxs-lookup"><span data-stu-id="77d0d-104">Notifies applications that the computer is about to enter a suspended state.</span></span> <span data-ttu-id="77d0d-105">Este evento se emite normalmente cuando todas las aplicaciones y controladores instalables devuelven **true** a un evento [PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="77d0d-105">This event is typically broadcast when all applications and installable drivers have returned **TRUE** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="77d0d-106">Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="77d0d-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="77d0d-107">Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="77d0d-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMSUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="77d0d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77d0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77d0d-109">*identificador*</span><span class="sxs-lookup"><span data-stu-id="77d0d-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="77d0d-110">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="77d0d-110">A handle to window.</span></span>

<span data-ttu-id="77d0d-111"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="77d0d-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="77d0d-112">Value</span><span class="sxs-lookup"><span data-stu-id="77d0d-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="77d0d-113">Significado</span><span class="sxs-lookup"><span data-stu-id="77d0d-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="77d0d-114"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="77d0d-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="77d0d-115">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="77d0d-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="77d0d-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="77d0d-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="77d0d-117">Value</span><span class="sxs-lookup"><span data-stu-id="77d0d-117">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="77d0d-118">Significado</span><span class="sxs-lookup"><span data-stu-id="77d0d-118">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="77d0d-119"><dt>**PBT \_ APMSUSPEND**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="77d0d-119"><dt>**PBT\_APMSUSPEND**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="77d0d-120">Identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="77d0d-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="77d0d-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77d0d-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77d0d-122">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="77d0d-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77d0d-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77d0d-123">Return value</span></span>

<span data-ttu-id="77d0d-124">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="77d0d-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77d0d-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77d0d-125">Remarks</span></span>

<span data-ttu-id="77d0d-126">Una aplicación debe procesar este evento completando todas las tareas necesarias para guardar los datos.</span><span class="sxs-lookup"><span data-stu-id="77d0d-126">An application should process this event by completing all tasks necessary to save data.</span></span>

<span data-ttu-id="77d0d-127">El sistema permite aproximadamente dos segundos para que una aplicación administre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="77d0d-127">The system allows approximately two seconds for an application to handle this notification.</span></span> <span data-ttu-id="77d0d-128">Si una aplicación sigue realizando operaciones después de que haya expirado su asignación de tiempo, el sistema puede interrumpir la aplicación.</span><span class="sxs-lookup"><span data-stu-id="77d0d-128">If an application is still performing operations after its time allotment has expired, the system may interrupt the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="77d0d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77d0d-129">Requirements</span></span>



| <span data-ttu-id="77d0d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="77d0d-130">Requirement</span></span> | <span data-ttu-id="77d0d-131">Value</span><span class="sxs-lookup"><span data-stu-id="77d0d-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77d0d-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77d0d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="77d0d-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="77d0d-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="77d0d-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77d0d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="77d0d-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="77d0d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="77d0d-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77d0d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="77d0d-137"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77d0d-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77d0d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="77d0d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d0d-139">Criterios de suspensión del sistema</span><span class="sxs-lookup"><span data-stu-id="77d0d-139">System Sleep Criteria</span></span>](system-sleep-criteria.md)
</dt> <dt>

[<span data-ttu-id="77d0d-140">Eventos de reactivación del sistema</span><span class="sxs-lookup"><span data-stu-id="77d0d-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="77d0d-141">Eventos de administración de energía</span><span class="sxs-lookup"><span data-stu-id="77d0d-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="77d0d-142">PBT \_ APMQUERYSUSPEND</span><span class="sxs-lookup"><span data-stu-id="77d0d-142">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="77d0d-143">**SetSystemPowerState**</span><span class="sxs-lookup"><span data-stu-id="77d0d-143">**SetSystemPowerState**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setsystempowerstate)
</dt> <dt>

[<span data-ttu-id="77d0d-144">**POWERBROADCAST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="77d0d-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




