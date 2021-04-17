---
description: Notifica a las aplicaciones que el sistema, normalmente un equipo personal con batería, está a punto de entrar en modo de suspensión.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: Mensaje de WM_POWER (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53fd165ee1cefe8970f85daea04b931a673b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677878"
---
# <a name="wm_power-message"></a><span data-ttu-id="b5a3b-103">Mensaje de energía de WM \_</span><span class="sxs-lookup"><span data-stu-id="b5a3b-103">WM\_POWER message</span></span>

<span data-ttu-id="b5a3b-104">Notifica a las aplicaciones que el sistema, normalmente un equipo personal con batería, está a punto de entrar en modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-104">Notifies applications that the system, typically a battery-powered personal computer, is about to enter a suspended mode.</span></span>

> [!Note]  
> <span data-ttu-id="b5a3b-105">El mensaje de **\_ energía de WM** está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-105">The **WM\_POWER** message is obsolete.</span></span> <span data-ttu-id="b5a3b-106">Solo se proporciona para ofrecer compatibilidad con aplicaciones basadas en Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-106">It is provided only for compatibility with 16-bit Windows-based applications.</span></span> <span data-ttu-id="b5a3b-107">Las aplicaciones deben usar el mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="b5a3b-107">Applications should use the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span>

 

<span data-ttu-id="b5a3b-108">Una ventana recibe este mensaje a través de su función **WindowProc** .</span><span class="sxs-lookup"><span data-stu-id="b5a3b-108">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
); 
```



## <a name="parameters"></a><span data-ttu-id="b5a3b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5a3b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5a3b-110">*identificador*</span><span class="sxs-lookup"><span data-stu-id="b5a3b-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b5a3b-111">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-111">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="b5a3b-112">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="b5a3b-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="b5a3b-113">Identificador del mensaje de **\_ energía de WM** .</span><span class="sxs-lookup"><span data-stu-id="b5a3b-113">The **WM\_POWER** message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b5a3b-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5a3b-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5a3b-115">La notificación de evento de potencia.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-115">The power-event notification.</span></span> <span data-ttu-id="b5a3b-116">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b5a3b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b5a3b-117">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="b5a3b-118">Significado</span><span class="sxs-lookup"><span data-stu-id="b5a3b-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <span data-ttu-id="b5a3b-119"><dt>**PWR \_ CRITICALRESUME**</dt></span><span class="sxs-lookup"><span data-stu-id="b5a3b-119"><dt>**PWR\_CRITICALRESUME**</dt></span></span> </dl> | <span data-ttu-id="b5a3b-120">Indica que el sistema está reanudando la operación después de entrar en modo suspendido sin difundir primero un mensaje de notificación **PWR \_ SUSPENDREQUEST** a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-120">Indicates that the system is resuming operation after entering suspended mode without first broadcasting a **PWR\_SUSPENDREQUEST** notification message to the application.</span></span> <span data-ttu-id="b5a3b-121">Una aplicación debe realizar las acciones de recuperación necesarias.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-121">An application should perform any necessary recovery actions.</span></span><br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <span data-ttu-id="b5a3b-122"><dt>**PWR \_ SUSPENDREQUEST**</dt></span><span class="sxs-lookup"><span data-stu-id="b5a3b-122"><dt>**PWR\_SUSPENDREQUEST**</dt></span></span> </dl> | <span data-ttu-id="b5a3b-123">Indica que el sistema está a punto de entrar en modo suspendido.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-123">Indicates that the system is about to enter suspended mode.</span></span><br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <span data-ttu-id="b5a3b-124"><dt>**PWR \_ SUSPENDRESUME**</dt></span><span class="sxs-lookup"><span data-stu-id="b5a3b-124"><dt>**PWR\_SUSPENDRESUME**</dt></span></span> </dl>    | <span data-ttu-id="b5a3b-125">Indica que el sistema está reanudando la operación después de haber entrado en modo suspendido normalmente, es decir, el sistema difunde un mensaje de notificación **PWR \_ SUSPENDREQUEST** a la aplicación antes de que se suspendiera el sistema.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-125">Indicates that the system is resuming operation after having entered suspended mode normally that is, the system broadcast a **PWR\_SUSPENDREQUEST** notification message to the application before the system was suspended.</span></span> <span data-ttu-id="b5a3b-126">Una aplicación debe realizar las acciones de recuperación necesarias.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-126">An application should perform any necessary recovery actions.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b5a3b-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5a3b-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5a3b-128">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-128">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5a3b-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5a3b-129">Return value</span></span>

<span data-ttu-id="b5a3b-130">El valor que devuelve una aplicación depende del valor del parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="b5a3b-130">The value an application returns depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="b5a3b-131">Si *wParam* es **PWR \_ SUSPENDREQUEST**, el valor devuelto es **PWR \_ FAIL** para evitar que el sistema entre en estado suspendido; de lo contrario, es **PWR \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-131">If *wParam* is **PWR\_SUSPENDREQUEST**, the return value is **PWR\_FAIL** to prevent the system from entering the suspended state; otherwise, it is **PWR\_OK**.</span></span> <span data-ttu-id="b5a3b-132">Si *wParam* es **PWR \_ SUSPENDRESUME** o **PWR \_ CRITICALRESUME**, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-132">If *wParam* is **PWR\_SUSPENDRESUME** or **PWR\_CRITICALRESUME**, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5a3b-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5a3b-133">Remarks</span></span>

<span data-ttu-id="b5a3b-134">Este mensaje solo se difunde a una aplicación que se ejecuta en un sistema que se ajusta a la especificación del sistema básico de entrada y salida (BIOS) de administración avanzada de energía (APM).</span><span class="sxs-lookup"><span data-stu-id="b5a3b-134">This message is broadcast only to an application that is running on a system that conforms to the Advanced Power Management (APM) basic input/output system (BIOS) specification.</span></span> <span data-ttu-id="b5a3b-135">El controlador de administración de energía emite el mensaje a cada ventana devuelta por la función **EnumWindows** .</span><span class="sxs-lookup"><span data-stu-id="b5a3b-135">The message is broadcast by the power-management driver to each window returned by the **EnumWindows** function.</span></span>

<span data-ttu-id="b5a3b-136">El modo suspendido es el estado en el que se produce la mayor cantidad de ahorro de energía, pero se conservan todos los datos y parámetros operativos.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-136">The suspended mode is the state in which the greatest amount of power savings occurs, but all operational data and parameters are preserved.</span></span> <span data-ttu-id="b5a3b-137">Se conserva el contenido de la memoria de acceso aleatorio (RAM), pero es probable que se desactiven muchos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b5a3b-137">Random-access memory (RAM) contents are preserved, but many devices are likely to be turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a3b-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5a3b-138">Requirements</span></span>



| <span data-ttu-id="b5a3b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5a3b-139">Requirement</span></span> | <span data-ttu-id="b5a3b-140">Value</span><span class="sxs-lookup"><span data-stu-id="b5a3b-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a3b-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5a3b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a3b-142">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b5a3b-142">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b5a3b-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5a3b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a3b-144">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5a3b-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b5a3b-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5a3b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5a3b-146"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5a3b-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5a3b-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5a3b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a3b-148">**POWERBROADCAST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="b5a3b-148">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




