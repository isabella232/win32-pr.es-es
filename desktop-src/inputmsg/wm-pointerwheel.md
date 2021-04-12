---
title: Mensaje WM_POINTERWHEEL
description: Se envía a la ventana con el foco de teclado en primer plano cuando se gira una rueda de desplazamiento.
ms.assetid: 6eec37da-2200-4be1-bf0b-44704caa1320
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERWHEEL
topic_type:
- apiref
api_name:
- WM_POINTERWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ad1177b2e92e47ca40c745e6cd5f1ea2cf259215
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490030"
---
# <a name="wm_pointerwheel-message"></a><span data-ttu-id="67862-104">Mensaje WM_POINTERWHEEL</span><span class="sxs-lookup"><span data-stu-id="67862-104">WM_POINTERWHEEL message</span></span>

<span data-ttu-id="67862-105">Se envía a la ventana con el foco de teclado en primer plano cuando se gira una rueda de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="67862-105">Posted to the window with foreground keyboard focus when a scroll wheel is rotated.</span></span>

<span data-ttu-id="67862-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="67862-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="67862-107">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="67862-107">\[!Important\]</span></span>  
> <span data-ttu-id="67862-108">Las aplicaciones de escritorio deben tener en cuenta los ppp.</span><span class="sxs-lookup"><span data-stu-id="67862-108">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="67862-109">Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP.</span><span class="sxs-lookup"><span data-stu-id="67862-109">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="67862-110">La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla).</span><span class="sxs-lookup"><span data-stu-id="67862-110">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="67862-111">Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67862-111">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERWHEEL            0x024E
```



## <a name="parameters"></a><span data-ttu-id="67862-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67862-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67862-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67862-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67862-114">Contiene el identificador del puntero y el delta de la rueda.</span><span class="sxs-lookup"><span data-stu-id="67862-114">Contains the pointer identifier and wheel delta.</span></span> <span data-ttu-id="67862-115">Use las siguientes macros para recuperar esta información.</span><span class="sxs-lookup"><span data-stu-id="67862-115">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="67862-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de puntero.</span><span class="sxs-lookup"><span data-stu-id="67862-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier.</span></span>

<span data-ttu-id="67862-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): diferencia de la rueda como un valor corto con signo.</span><span class="sxs-lookup"><span data-stu-id="67862-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): wheel delta as a signed short value.</span></span>

</dd> <dt>

<span data-ttu-id="67862-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67862-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67862-119">Contiene la ubicación del punto del puntero.</span><span class="sxs-lookup"><span data-stu-id="67862-119">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="67862-120">Dado que el puntero puede establecer contacto con el dispositivo a través de un área no trivial, esta ubicación de punto puede ser una simplificación de un área de puntero más compleja.</span><span class="sxs-lookup"><span data-stu-id="67862-120">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="67862-121">Siempre que sea posible, una aplicación debe usar la información de área de puntero completa en lugar de la ubicación del punto.</span><span class="sxs-lookup"><span data-stu-id="67862-121">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="67862-122">Utilice las siguientes macros para recuperar las coordenadas físicas de la pantalla del punto.</span><span class="sxs-lookup"><span data-stu-id="67862-122">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="67862-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): la coordenada X (punto horizontal).</span><span class="sxs-lookup"><span data-stu-id="67862-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="67862-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): la coordenada Y (punto vertical).</span><span class="sxs-lookup"><span data-stu-id="67862-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67862-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67862-125">Return value</span></span>

<span data-ttu-id="67862-126">Si la aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="67862-126">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="67862-127">Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="67862-127">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="67862-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67862-128">Remarks</span></span>

<span data-ttu-id="67862-129">Para recuperar las unidades de desplazamiento de la rueda, use el **inputData** de la estructura de [**POINTER_INFO**](/previous-versions/windows/desktop/api) devuelta por una llamada a la función [**GetPointerInfo**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="67862-129">To retrieve the wheel scroll units, use the **inputData** filed of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure returned by calling [**GetPointerInfo**](/previous-versions/windows/desktop/api) function.</span></span> <span data-ttu-id="67862-130">Este campo contiene un valor con signo y se expresa en un múltiplo de **WHEEL_DELTA**.</span><span class="sxs-lookup"><span data-stu-id="67862-130">This field contains a signed value and is expressed in a multiple of **WHEEL_DELTA**.</span></span> <span data-ttu-id="67862-131">Un valor positivo indica un giro hacia delante y un valor negativo indica un giro hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="67862-131">A positive value indicates a rotation forward and a negative value indicates a rotation backward.</span></span>

<span data-ttu-id="67862-132">Tenga en cuenta que las entradas de la rueda se pueden entregar incluso si el cursor del mouse se encuentra fuera de la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67862-132">Note that the wheel inputs may be delivered even if the mouse cursor is located outside of application s window.</span></span> <span data-ttu-id="67862-133">Los mensajes de la rueda se entregan de forma muy similar a las entradas del teclado.</span><span class="sxs-lookup"><span data-stu-id="67862-133">The wheel messages are delivered in a way very similar to the keyboard inputs.</span></span> <span data-ttu-id="67862-134">La ventana de enfoque de la cola de mensajes foregournd recibe los mensajes de la rueda.</span><span class="sxs-lookup"><span data-stu-id="67862-134">The focus window of the foregournd message queue receives the wheel messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="67862-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67862-135">Requirements</span></span>



| <span data-ttu-id="67862-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="67862-136">Requirement</span></span> | <span data-ttu-id="67862-137">Value</span><span class="sxs-lookup"><span data-stu-id="67862-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67862-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67862-138">Minimum supported client</span></span><br/> | <span data-ttu-id="67862-139">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="67862-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="67862-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67862-140">Minimum supported server</span></span><br/> | <span data-ttu-id="67862-141">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="67862-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="67862-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67862-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="67862-143"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67862-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67862-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="67862-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67862-145">Mensajes</span><span class="sxs-lookup"><span data-stu-id="67862-145">Messages</span></span>](messages.md)
</dt> </dl>

 

