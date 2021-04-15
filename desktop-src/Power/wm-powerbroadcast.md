---
description: Notifica a las aplicaciones que se ha producido un evento de administración de energía.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: Mensaje de WM_POWERBROADCAST (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f1b273462d8de27c19d715836d168ab8bf8c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545486"
---
# <a name="wm_powerbroadcast-message"></a><span data-ttu-id="671bc-103">Mensaje de POWERBROADCAST de WM \_</span><span class="sxs-lookup"><span data-stu-id="671bc-103">WM\_POWERBROADCAST message</span></span>

<span data-ttu-id="671bc-104">Notifica a las aplicaciones que se ha producido un evento de administración de energía.</span><span class="sxs-lookup"><span data-stu-id="671bc-104">Notifies applications that a power-management event has occurred.</span></span>

<span data-ttu-id="671bc-105">Una ventana recibe este mensaje a través de su función **WindowProc** .</span><span class="sxs-lookup"><span data-stu-id="671bc-105">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="671bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="671bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="671bc-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="671bc-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="671bc-108">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="671bc-108">A handle to window.</span></span>

<span data-ttu-id="671bc-109"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="671bc-109"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="671bc-110">Value</span><span class="sxs-lookup"><span data-stu-id="671bc-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="671bc-111">Significado</span><span class="sxs-lookup"><span data-stu-id="671bc-111">Meaning</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="671bc-112">\* \* \* \* <dt>WM \_ POWERBROADCAST \*</dt> \* \* \* <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="671bc-112"><dt>\*\*\*\*WM\_POWERBROADCAST\*\*\*\*</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="671bc-113">Identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="671bc-113">Message identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="671bc-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="671bc-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="671bc-115">El evento de administración de energía.</span><span class="sxs-lookup"><span data-stu-id="671bc-115">The power-management event.</span></span> <span data-ttu-id="671bc-116">Este parámetro puede ser uno de los siguientes identificadores de eventos.</span><span class="sxs-lookup"><span data-stu-id="671bc-116">This parameter can be one of the following event identifiers.</span></span>



| <span data-ttu-id="671bc-117">Evento</span><span class="sxs-lookup"><span data-stu-id="671bc-117">Event</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="671bc-118">Significado</span><span class="sxs-lookup"><span data-stu-id="671bc-118">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="671bc-119"><dt>**[PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="671bc-119"><dt>**[PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="671bc-120">El estado de la energía ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="671bc-120">Power status has changed.</span></span><br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="671bc-121"><dt>**[PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0X12)</dt></span><span class="sxs-lookup"><span data-stu-id="671bc-121"><dt>**[PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span></span> </dl>        | <span data-ttu-id="671bc-122">La operación se está reanudando automáticamente desde un estado de baja energía.</span><span class="sxs-lookup"><span data-stu-id="671bc-122">Operation is resuming automatically from a low-power state.</span></span> <span data-ttu-id="671bc-123">Este mensaje se envía cada vez que se reanuda el sistema.</span><span class="sxs-lookup"><span data-stu-id="671bc-123">This message is sent every time the system resumes.</span></span><br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="671bc-124"><dt>**[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0X7)</dt></span><span class="sxs-lookup"><span data-stu-id="671bc-124"><dt>**[PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span></span> </dl>                  | <span data-ttu-id="671bc-125">La operación se está reanudando desde un estado de baja energía.</span><span class="sxs-lookup"><span data-stu-id="671bc-125">Operation is resuming from a low-power state.</span></span> <span data-ttu-id="671bc-126">Este mensaje se envía después de [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) si la entrada del usuario desencadena la reanudación, como presionar una tecla.</span><span class="sxs-lookup"><span data-stu-id="671bc-126">This message is sent after [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) if the resume is triggered by user input, such as pressing a key.</span></span><br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="671bc-127"><dt>**[PBT \_ APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="671bc-127"><dt>**[PBT\_APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                          | <span data-ttu-id="671bc-128">El sistema está suspendiendo la operación.</span><span class="sxs-lookup"><span data-stu-id="671bc-128">System is suspending operation.</span></span><br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="671bc-129"><dt>**[PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="671bc-129"><dt>**[PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span></span> </dl>   | <span data-ttu-id="671bc-130">Se ha recibido un evento de cambio de configuración de energía.</span><span class="sxs-lookup"><span data-stu-id="671bc-130">A power setting change event has been received.</span></span> <br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="671bc-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="671bc-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="671bc-132">Datos específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="671bc-132">The event-specific data.</span></span> <span data-ttu-id="671bc-133">Para la mayoría de los eventos, este parámetro está reservado y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="671bc-133">For most events, this parameter is reserved and not used.</span></span>

<span data-ttu-id="671bc-134">Si el parámetro *wParam* es [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md), el parámetro *lParam* es un puntero a una estructura de [**\_ configuración de POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="671bc-134">If the *wParam* parameter is [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md), the *lParam* parameter is a pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="671bc-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="671bc-135">Return value</span></span>

<span data-ttu-id="671bc-136">Una aplicación debe devolver **true** si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="671bc-136">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="671bc-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="671bc-137">Remarks</span></span>

<span data-ttu-id="671bc-138">El sistema siempre envía un mensaje [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) cuando se reanuda el sistema.</span><span class="sxs-lookup"><span data-stu-id="671bc-138">The system always sends a [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) message whenever the system resumes.</span></span> <span data-ttu-id="671bc-139">Si el sistema se reanuda en respuesta a la entrada del usuario, como presionar una tecla, el sistema también envía un mensaje de **PBT \_ APMRESUMESUSPEND** después de enviar PBT \_ APMRESUMEAUTOMATIC.</span><span class="sxs-lookup"><span data-stu-id="671bc-139">If the system resumes in response to user input such as pressing a key, the system also sends a **PBT\_APMRESUMESUSPEND** message after sending PBT\_APMRESUMEAUTOMATIC.</span></span>

<span data-ttu-id="671bc-140">**WM \_** Los mensajes POWERBROADCAST no distinguen entre diferentes Estados de energía baja.</span><span class="sxs-lookup"><span data-stu-id="671bc-140">**WM\_POWERBROADCAST** messages do not distinguish between different low-power states.</span></span> <span data-ttu-id="671bc-141">Una aplicación solo puede determinar que el sistema está entrando en estado de baja energía o se ha reanudado. no puede determinar el estado de energía específico.</span><span class="sxs-lookup"><span data-stu-id="671bc-141">An application can determine only that the system is entering or has resumed from a low-power state; it cannot determine the specific power state.</span></span> <span data-ttu-id="671bc-142">El sistema registra los detalles acerca de las transiciones de estado de energía en el registro de eventos del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="671bc-142">The system records details about power state transitions in the Windows System event log.</span></span>

<span data-ttu-id="671bc-143">Para evitar que el sistema pase a un estado de baja energía en Windows Vista, una aplicación debe llamar a [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) para informar al sistema de que está en uso.</span><span class="sxs-lookup"><span data-stu-id="671bc-143">To prevent the system from transitioning to a low-power state in Windows Vista, an application must call [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) to inform the system that it is in use.</span></span>

<span data-ttu-id="671bc-144">Los siguientes mensajes no se admiten en ninguno de los sistemas operativos especificados en la sección de requisitos:</span><span class="sxs-lookup"><span data-stu-id="671bc-144">The following messages are not supported on any of the operating systems specified in the Requirements section:</span></span>

- <span data-ttu-id="671bc-145">PBT_APMQUERYSTANDBY</span><span class="sxs-lookup"><span data-stu-id="671bc-145">PBT_APMQUERYSTANDBY</span></span>  
- <span data-ttu-id="671bc-146">PBT_APMQUERYSTANDBYFAILED</span><span class="sxs-lookup"><span data-stu-id="671bc-146">PBT_APMQUERYSTANDBYFAILED</span></span>  
- <span data-ttu-id="671bc-147">PBT_APMSTANDBY</span><span class="sxs-lookup"><span data-stu-id="671bc-147">PBT_APMSTANDBY</span></span>  
- <span data-ttu-id="671bc-148">PBT_APMRESUMESTANDBY</span><span class="sxs-lookup"><span data-stu-id="671bc-148">PBT_APMRESUMESTANDBY</span></span>  

## <a name="requirements"></a><span data-ttu-id="671bc-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="671bc-149">Requirements</span></span>



| <span data-ttu-id="671bc-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="671bc-150">Requirement</span></span> | <span data-ttu-id="671bc-151">Value</span><span class="sxs-lookup"><span data-stu-id="671bc-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="671bc-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="671bc-152">Minimum supported client</span></span><br/> | <span data-ttu-id="671bc-153">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="671bc-153">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="671bc-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="671bc-154">Minimum supported server</span></span><br/> | <span data-ttu-id="671bc-155">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="671bc-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="671bc-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="671bc-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="671bc-157"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="671bc-157"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="671bc-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="671bc-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671bc-159">\_Mensajes POWERBROADCAST de WM</span><span class="sxs-lookup"><span data-stu-id="671bc-159">WM\_POWERBROADCAST Messages</span></span>](wm-powerbroadcast-messages.md)
</dt> <dt>

[<span data-ttu-id="671bc-160">Mensajes de administración de energía</span><span class="sxs-lookup"><span data-stu-id="671bc-160">Power Management Messages</span></span>](power-management-messages.md)
</dt> </dl>

 

 




