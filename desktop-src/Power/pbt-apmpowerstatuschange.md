---
description: Notifica a las aplicaciones un cambio en el estado de energía del equipo, como un conmutador de la alimentación de la batería a/C.
ms.assetid: dc56fee3-e0df-4f8e-8a41-92460279280a
title: Evento PBT_APMPOWERSTATUSCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ed67f7ba064d44614196da4190ce18a996bd5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276832"
---
# <a name="pbt_apmpowerstatuschange-event"></a><span data-ttu-id="f3259-103">\_Evento PBT APMPOWERSTATUSCHANGE</span><span class="sxs-lookup"><span data-stu-id="f3259-103">PBT\_APMPOWERSTATUSCHANGE event</span></span>

<span data-ttu-id="f3259-104">Notifica a las aplicaciones un cambio en el estado de energía del equipo, como un conmutador de la alimentación de la batería a/C.</span><span class="sxs-lookup"><span data-stu-id="f3259-104">Notifies applications of a change in the power status of the computer, such as a switch from battery power to A/C.</span></span> <span data-ttu-id="f3259-105">El sistema difunde también este evento cuando la energía de la batería restante queda por debajo del umbral especificado por el usuario o cuando la energía de la batería cambia en un porcentaje especificado.</span><span class="sxs-lookup"><span data-stu-id="f3259-105">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

<span data-ttu-id="f3259-106">Una ventana recibe este evento a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="f3259-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="f3259-107">Los parámetros *wParam* e *lParam* se establecen como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="f3259-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMPOWERSTATUSCHANGE
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="f3259-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3259-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3259-109">*identificador*</span><span class="sxs-lookup"><span data-stu-id="f3259-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f3259-110">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f3259-110">A handle to window.</span></span>

<span data-ttu-id="f3259-111"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="f3259-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="f3259-112">Value</span><span class="sxs-lookup"><span data-stu-id="f3259-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="f3259-113">Significado</span><span class="sxs-lookup"><span data-stu-id="f3259-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="f3259-114"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="f3259-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="f3259-115">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f3259-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="f3259-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="f3259-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="f3259-117">Value</span><span class="sxs-lookup"><span data-stu-id="f3259-117">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="f3259-118">Significado</span><span class="sxs-lookup"><span data-stu-id="f3259-118">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="f3259-119"><dt>**PBT \_ APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="f3259-119"><dt>**PBT\_APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="f3259-120">Identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="f3259-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3259-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3259-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3259-122">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f3259-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3259-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3259-123">Return value</span></span>

<span data-ttu-id="f3259-124">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f3259-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3259-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3259-125">Remarks</span></span>

<span data-ttu-id="f3259-126">Una aplicación debe procesar este evento llamando a la función [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) para recuperar el estado de energía actual del equipo.</span><span class="sxs-lookup"><span data-stu-id="f3259-126">An application should process this event by calling the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve the current power status of the computer.</span></span> <span data-ttu-id="f3259-127">En concreto, la aplicación debe comprobar los miembros **ACLineStatus**, **BatteryFlag**, **BatteryLifeTime** y **BatteryLifePercent** de la estructura [**de \_ \_ Estado de energía del sistema**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) en busca de cambios.</span><span class="sxs-lookup"><span data-stu-id="f3259-127">In particular, the application should check the **ACLineStatus**, **BatteryFlag**, **BatteryLifeTime**, and **BatteryLifePercent** members of the [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) structure for any changes.</span></span> <span data-ttu-id="f3259-128">Este evento puede producirse cuando la duración de la batería cae a menos de 5 minutos, o cuando el porcentaje de la duración de la batería cae por debajo del 10 por ciento, o si la duración de la batería cambia en un 3 por ciento.</span><span class="sxs-lookup"><span data-stu-id="f3259-128">This event can occur when battery life drops to less than 5 minutes, or when the percentage of battery life drops below 10 percent, or if the battery life changes by 3 percent.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3259-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3259-129">Requirements</span></span>



| <span data-ttu-id="f3259-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3259-130">Requirement</span></span> | <span data-ttu-id="f3259-131">Value</span><span class="sxs-lookup"><span data-stu-id="f3259-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3259-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3259-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f3259-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f3259-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f3259-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3259-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f3259-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3259-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f3259-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3259-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3259-137"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3259-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3259-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3259-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3259-139">Estado de la alimentación del sistema</span><span class="sxs-lookup"><span data-stu-id="f3259-139">System Power Status</span></span>](system-power-status.md)
</dt> <dt>

[<span data-ttu-id="f3259-140">Eventos de administración de energía</span><span class="sxs-lookup"><span data-stu-id="f3259-140">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="f3259-141">**GetSystemPowerStatus**</span><span class="sxs-lookup"><span data-stu-id="f3259-141">**GetSystemPowerStatus**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus)
</dt> <dt>

[<span data-ttu-id="f3259-142">**Estado de la alimentación del sistema \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f3259-142">**SYSTEM\_POWER\_STATUS**</span></span>](/windows/desktop/api/Winbase/ns-winbase-system_power_status)
</dt> <dt>

[<span data-ttu-id="f3259-143">**POWERBROADCAST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f3259-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




