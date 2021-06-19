---
description: Notifica a las aplicaciones que se ha producido un evento de administración de energía.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: WM_POWERBROADCAST mensaje (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b205a146b731bdf8cf9adc1563621232c24c10b4
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396510"
---
# <a name="wm_powerbroadcast-message"></a><span data-ttu-id="faadc-103">Mensaje \_ DE WM POWERBROADCAST</span><span class="sxs-lookup"><span data-stu-id="faadc-103">WM\_POWERBROADCAST message</span></span>

<span data-ttu-id="faadc-104">Notifica a las aplicaciones que se ha producido un evento de administración de energía.</span><span class="sxs-lookup"><span data-stu-id="faadc-104">Notifies applications that a power-management event has occurred.</span></span>

<span data-ttu-id="faadc-105">Una ventana recibe este mensaje a través de su **función WindowProc.**</span><span class="sxs-lookup"><span data-stu-id="faadc-105">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="faadc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="faadc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faadc-107">*Hwnd*</span><span class="sxs-lookup"><span data-stu-id="faadc-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="faadc-108">Identificador a ventana.</span><span class="sxs-lookup"><span data-stu-id="faadc-108">A handle to window.</span></span>

</dd> <dt>
  
<span data-ttu-id="faadc-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="faadc-109">*uMsg*</span></span>
</dt> <dd> 

| <span data-ttu-id="faadc-110">Valor</span><span class="sxs-lookup"><span data-stu-id="faadc-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="faadc-111">Significado</span><span class="sxs-lookup"><span data-stu-id="faadc-111">Meaning</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="faadc-112"><dt>\*:WM \_ POWERBROADCAST\*\*</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="faadc-112"><dt>\*\*\*\*WM\_POWERBROADCAST\*\*\*\*</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="faadc-113">Identificador del mensaje.</span><span class="sxs-lookup"><span data-stu-id="faadc-113">Message identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="faadc-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="faadc-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="faadc-115">Evento de administración de energía.</span><span class="sxs-lookup"><span data-stu-id="faadc-115">The power-management event.</span></span> <span data-ttu-id="faadc-116">Este parámetro puede ser uno de los siguientes identificadores de evento.</span><span class="sxs-lookup"><span data-stu-id="faadc-116">This parameter can be one of the following event identifiers.</span></span>



| <span data-ttu-id="faadc-117">Evento</span><span class="sxs-lookup"><span data-stu-id="faadc-117">Event</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="faadc-118">Significado</span><span class="sxs-lookup"><span data-stu-id="faadc-118">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="faadc-119"><dt>**[PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="faadc-119"><dt>**[PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="faadc-120">El estado de energía ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="faadc-120">Power status has changed.</span></span><br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="faadc-121"><dt>**[PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="faadc-121"><dt>**[PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span></span> </dl>        | <span data-ttu-id="faadc-122">La operación se reanuda automáticamente desde un estado de bajo consumo.</span><span class="sxs-lookup"><span data-stu-id="faadc-122">Operation is resuming automatically from a low-power state.</span></span> <span data-ttu-id="faadc-123">Este mensaje se envía cada vez que se reanuda el sistema.</span><span class="sxs-lookup"><span data-stu-id="faadc-123">This message is sent every time the system resumes.</span></span><br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="faadc-124"><dt>**[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="faadc-124"><dt>**[PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span></span> </dl>                  | <span data-ttu-id="faadc-125">La operación se reanuda desde un estado de bajo consumo.</span><span class="sxs-lookup"><span data-stu-id="faadc-125">Operation is resuming from a low-power state.</span></span> <span data-ttu-id="faadc-126">Este mensaje se envía después de [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) si la reanudación se desencadena mediante la entrada del usuario, como presionar una tecla.</span><span class="sxs-lookup"><span data-stu-id="faadc-126">This message is sent after [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) if the resume is triggered by user input, such as pressing a key.</span></span><br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="faadc-127"><dt>**[PBT \_ APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="faadc-127"><dt>**[PBT\_APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                          | <span data-ttu-id="faadc-128">El sistema suspende la operación.</span><span class="sxs-lookup"><span data-stu-id="faadc-128">System is suspending operation.</span></span><br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="faadc-129"><dt>**[PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="faadc-129"><dt>**[PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span></span> </dl>   | <span data-ttu-id="faadc-130">Se ha recibido un evento de cambio de configuración de energía.</span><span class="sxs-lookup"><span data-stu-id="faadc-130">A power setting change event has been received.</span></span> <br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="faadc-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="faadc-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="faadc-132">Datos específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="faadc-132">The event-specific data.</span></span> <span data-ttu-id="faadc-133">Para la mayoría de los eventos, este parámetro está reservado y no se usa.</span><span class="sxs-lookup"><span data-stu-id="faadc-133">For most events, this parameter is reserved and not used.</span></span>

<span data-ttu-id="faadc-134">Si el *parámetro wParam* es [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md), el parámetro *lParam* es un puntero a una [**estructura DE CONFIGURACIÓN DE POWERBROADCAST. \_**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)</span><span class="sxs-lookup"><span data-stu-id="faadc-134">If the *wParam* parameter is [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md), the *lParam* parameter is a pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faadc-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="faadc-135">Return value</span></span>

<span data-ttu-id="faadc-136">Una aplicación debe devolver **TRUE** si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="faadc-136">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="faadc-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="faadc-137">Remarks</span></span>

<span data-ttu-id="faadc-138">El sistema siempre envía un mensaje [ \_ PBT APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) cada vez que se reanuda el sistema.</span><span class="sxs-lookup"><span data-stu-id="faadc-138">The system always sends a [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) message whenever the system resumes.</span></span> <span data-ttu-id="faadc-139">Si el sistema se reanuda en respuesta a la entrada del usuario, como presionar una tecla, el sistema también envía un mensaje **\_ PBT APMRESUMESUSPEND** después de enviar PBT \_ APMRESUMEAUTOMATIC.</span><span class="sxs-lookup"><span data-stu-id="faadc-139">If the system resumes in response to user input such as pressing a key, the system also sends a **PBT\_APMRESUMESUSPEND** message after sending PBT\_APMRESUMEAUTOMATIC.</span></span>

<span data-ttu-id="faadc-140">**WM \_ Los mensajes POWERBROADCAST** no distinguen entre distintos estados de bajo consumo.</span><span class="sxs-lookup"><span data-stu-id="faadc-140">**WM\_POWERBROADCAST** messages do not distinguish between different low-power states.</span></span> <span data-ttu-id="faadc-141">Una aplicación solo puede determinar que el sistema entra o se ha reanudado desde un estado de bajo consumo. no puede determinar el estado de energía específico.</span><span class="sxs-lookup"><span data-stu-id="faadc-141">An application can determine only that the system is entering or has resumed from a low-power state; it cannot determine the specific power state.</span></span> <span data-ttu-id="faadc-142">El sistema registra detalles sobre las transiciones de estado de energía en el registro de eventos del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="faadc-142">The system records details about power state transitions in the Windows System event log.</span></span>

<span data-ttu-id="faadc-143">Para evitar que el sistema haga la transición a un estado de bajo consumo en Windows Vista, una aplicación debe llamar a [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) para informar al sistema de que está en uso.</span><span class="sxs-lookup"><span data-stu-id="faadc-143">To prevent the system from transitioning to a low-power state in Windows Vista, an application must call [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) to inform the system that it is in use.</span></span>

<span data-ttu-id="faadc-144">Los mensajes siguientes no se admiten en ninguno de los sistemas operativos especificados en la sección Requisitos:</span><span class="sxs-lookup"><span data-stu-id="faadc-144">The following messages are not supported on any of the operating systems specified in the Requirements section:</span></span>

- <span data-ttu-id="faadc-145">PBT_APMQUERYSTANDBY</span><span class="sxs-lookup"><span data-stu-id="faadc-145">PBT_APMQUERYSTANDBY</span></span>  
- <span data-ttu-id="faadc-146">PBT_APMQUERYSTANDBYFAILED</span><span class="sxs-lookup"><span data-stu-id="faadc-146">PBT_APMQUERYSTANDBYFAILED</span></span>  
- <span data-ttu-id="faadc-147">PBT_APMSTANDBY</span><span class="sxs-lookup"><span data-stu-id="faadc-147">PBT_APMSTANDBY</span></span>  
- <span data-ttu-id="faadc-148">PBT_APMRESUMESTANDBY</span><span class="sxs-lookup"><span data-stu-id="faadc-148">PBT_APMRESUMESTANDBY</span></span>  

## <a name="requirements"></a><span data-ttu-id="faadc-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faadc-149">Requirements</span></span>



| <span data-ttu-id="faadc-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="faadc-150">Requirement</span></span> | <span data-ttu-id="faadc-151">Valor</span><span class="sxs-lookup"><span data-stu-id="faadc-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faadc-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="faadc-152">Minimum supported client</span></span><br/> | <span data-ttu-id="faadc-153">Solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="faadc-153">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="faadc-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="faadc-154">Minimum supported server</span></span><br/> | <span data-ttu-id="faadc-155">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="faadc-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="faadc-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="faadc-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="faadc-157"><dt>WinUser.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="faadc-157"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faadc-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="faadc-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faadc-159">Mensajes \_ DE WM POWERBROADCAST</span><span class="sxs-lookup"><span data-stu-id="faadc-159">WM\_POWERBROADCAST Messages</span></span>](wm-powerbroadcast-messages.md)
</dt> <dt>

[<span data-ttu-id="faadc-160">Mensajes de administración de energía</span><span class="sxs-lookup"><span data-stu-id="faadc-160">Power Management Messages</span></span>](power-management-messages.md)
</dt> </dl>

 

 




