---
description: Evento de cambio de configuración de energía enviado con un mensaje de ventana de POWERBROADCAST de WM \_ o en una devolución de llamada de notificación de HandlerEx para servicios.
ms.assetid: 0bcadb85-47c5-48a9-b3f9-f0a1ca60b503
title: Evento PBT_POWERSETTINGCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f38486d2e5cce1cfe541468e548e92353c9837
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909686"
---
# <a name="pbt_powersettingchange-event"></a><span data-ttu-id="da5da-103">\_Evento PBT POWERSETTINGCHANGE</span><span class="sxs-lookup"><span data-stu-id="da5da-103">PBT\_POWERSETTINGCHANGE event</span></span>

<span data-ttu-id="da5da-104">Evento de cambio de configuración de energía enviado con un mensaje de ventana de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) o en una devolución de llamada de notificación de [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) para servicios.</span><span class="sxs-lookup"><span data-stu-id="da5da-104">Power setting change event sent with a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) window message or in a [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) notification callback for services.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_POWERSETTINGCHANGE
            LPARAM lParam); // Pointer to POWERBROADCAST_SETTING
```



## <a name="parameters"></a><span data-ttu-id="da5da-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da5da-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da5da-106">*identificador*</span><span class="sxs-lookup"><span data-stu-id="da5da-106">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="da5da-107">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="da5da-107">A handle to window.</span></span>

<span data-ttu-id="da5da-108"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="da5da-108"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="da5da-109">Value</span><span class="sxs-lookup"><span data-stu-id="da5da-109">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="da5da-110">Significado</span><span class="sxs-lookup"><span data-stu-id="da5da-110">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="da5da-111"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="da5da-111"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="da5da-112">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="da5da-112">Message identifier.</span></span><br/> |



 

<span data-ttu-id="da5da-113"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="da5da-113"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="da5da-114">Value</span><span class="sxs-lookup"><span data-stu-id="da5da-114">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="da5da-115">Significado</span><span class="sxs-lookup"><span data-stu-id="da5da-115">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="da5da-116"><dt>**PBT \_ POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="da5da-116"><dt>**PBT\_POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt></span></span> </dl> | <span data-ttu-id="da5da-117">Identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="da5da-117">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="da5da-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da5da-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da5da-119">Puntero a una estructura de [**\_ configuración de POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="da5da-119">Pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da5da-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da5da-120">Return value</span></span>

<span data-ttu-id="da5da-121">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="da5da-121">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="da5da-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da5da-122">Requirements</span></span>



| <span data-ttu-id="da5da-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="da5da-123">Requirement</span></span> | <span data-ttu-id="da5da-124">Value</span><span class="sxs-lookup"><span data-stu-id="da5da-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da5da-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da5da-125">Minimum supported client</span></span><br/> | <span data-ttu-id="da5da-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="da5da-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="da5da-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da5da-127">Minimum supported server</span></span><br/> | <span data-ttu-id="da5da-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="da5da-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da5da-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da5da-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="da5da-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da5da-130"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da5da-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="da5da-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da5da-132">Eventos de administración de energía</span><span class="sxs-lookup"><span data-stu-id="da5da-132">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="da5da-133">**HandlerEx**</span><span class="sxs-lookup"><span data-stu-id="da5da-133">**HandlerEx**</span></span>](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)
</dt> <dt>

[<span data-ttu-id="da5da-134">**POWERBROADCAST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="da5da-134">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> <dt>

[<span data-ttu-id="da5da-135">**configuración de POWERBROADCAST \_**</span><span class="sxs-lookup"><span data-stu-id="da5da-135">**POWERBROADCAST\_SETTING**</span></span>](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
</dt> </dl>

 

