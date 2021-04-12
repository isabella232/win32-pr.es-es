---
description: Se envía a la cola de mensajes del subproceso de instalación cuando expira un temporizador. El mensaje se expone mediante la función GetMessage o PeekMessage.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: Mensaje de WM_TIMER (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c99db67c9c9b3419e477ccd0a78133df453a7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278318"
---
# <a name="wm_timer-message"></a><span data-ttu-id="67914-104">\_Mensaje del temporizador de WM</span><span class="sxs-lookup"><span data-stu-id="67914-104">WM\_TIMER message</span></span>

<span data-ttu-id="67914-105">Se envía a la cola de mensajes del subproceso de instalación cuando expira un temporizador.</span><span class="sxs-lookup"><span data-stu-id="67914-105">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="67914-106">El mensaje se expone mediante la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="67914-106">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span>


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a><span data-ttu-id="67914-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67914-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67914-108">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="67914-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67914-109">Identificador del temporizador.</span><span class="sxs-lookup"><span data-stu-id="67914-109">The timer identifier.</span></span>

</dd> <dt>

<span data-ttu-id="67914-110">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="67914-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67914-111">Puntero a una función de devolución de llamada definida por la aplicación que se pasó a la función [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) cuando se instaló el temporizador.</span><span class="sxs-lookup"><span data-stu-id="67914-111">A pointer to an application-defined callback function that was passed to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function when the timer was installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67914-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67914-112">Return value</span></span>

<span data-ttu-id="67914-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="67914-113">Type: **LRESULT**</span></span>

<span data-ttu-id="67914-114">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="67914-114">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="67914-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67914-115">Remarks</span></span>

<span data-ttu-id="67914-116">Puede procesar el mensaje proporcionando un caso de **\_ temporizador de WM** en el procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="67914-116">You can process the message by providing a **WM\_TIMER** case in the window procedure.</span></span> <span data-ttu-id="67914-117">De lo contrario, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) llamará a la función de devolución de llamada [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) especificada en la llamada a la función [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) que se usa para instalar el temporizador.</span><span class="sxs-lookup"><span data-stu-id="67914-117">Otherwise, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) will call the [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) callback function specified in the call to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function used to install the timer.</span></span>

<span data-ttu-id="67914-118">El mensaje del **\_ temporizador de WM** es un mensaje de prioridad baja.</span><span class="sxs-lookup"><span data-stu-id="67914-118">The **WM\_TIMER** message is a low-priority message.</span></span> <span data-ttu-id="67914-119">Las funciones [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) y [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) exponen este mensaje solo cuando no hay otros mensajes de prioridad más alta en la cola de mensajes del subproceso.</span><span class="sxs-lookup"><span data-stu-id="67914-119">The [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions post this message only when no other higher-priority messages are in the thread's message queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="67914-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67914-120">Requirements</span></span>



| <span data-ttu-id="67914-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="67914-121">Requirement</span></span> | <span data-ttu-id="67914-122">Value</span><span class="sxs-lookup"><span data-stu-id="67914-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67914-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67914-123">Minimum supported client</span></span><br/> | <span data-ttu-id="67914-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="67914-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="67914-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67914-125">Minimum supported server</span></span><br/> | <span data-ttu-id="67914-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="67914-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="67914-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67914-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="67914-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67914-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67914-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="67914-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="67914-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="67914-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="67914-131">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="67914-131">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="67914-132">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="67914-132">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="67914-133">**SetTimer**</span><span class="sxs-lookup"><span data-stu-id="67914-133">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[<span data-ttu-id="67914-134">**TimerProc**</span><span class="sxs-lookup"><span data-stu-id="67914-134">**TimerProc**</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

<span data-ttu-id="67914-135">**Vista**</span><span class="sxs-lookup"><span data-stu-id="67914-135">**Conceptual**</span></span>
</dt> <dt>

<span data-ttu-id="67914-136">[Timers](timers.md) (Temporizadores)</span><span class="sxs-lookup"><span data-stu-id="67914-136">[Timers](timers.md)</span></span>
</dt> </dl>

 

 
