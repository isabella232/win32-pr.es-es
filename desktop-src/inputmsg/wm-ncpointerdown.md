---
title: Mensaje WM_NCPOINTERDOWN
description: Se envía cuando un puntero hace contacto sobre el área no cliente de una ventana.
ms.assetid: 3bdc37da-217c-4be1-bf0b-99704bda1322
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_NCPOINTERDOWN
topic_type:
- apiref
api_name:
- WM_NCPOINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6f4c3ef8ed75c5bd29250cd2f9ce4d666b6d961d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996761"
---
# <a name="wm_ncpointerdown-message"></a><span data-ttu-id="259b4-104">Mensaje WM_NCPOINTERDOWN</span><span class="sxs-lookup"><span data-stu-id="259b4-104">WM_NCPOINTERDOWN message</span></span>

<span data-ttu-id="259b4-105">Se envía cuando un puntero hace contacto sobre el área no cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="259b4-105">Posted when a pointer makes contact over the non-client area of a window.</span></span> <span data-ttu-id="259b4-106">El mensaje se dirige a la ventana sobre la que el puntero establece contacto.</span><span class="sxs-lookup"><span data-stu-id="259b4-106">The message targets the window over which the pointer makes contact.</span></span> <span data-ttu-id="259b4-107">El puntero se captura implícitamente en la ventana para que la ventana siga recibiendo entradas para el puntero hasta que interrumpa el contacto.</span><span class="sxs-lookup"><span data-stu-id="259b4-107">The pointer is implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="259b4-108">Si una ventana ha capturado este puntero, este mensaje no se publica.</span><span class="sxs-lookup"><span data-stu-id="259b4-108">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="259b4-109">En su lugar, se expone un [**WM_POINTERDOWN**](wm-pointerdown.md) en la ventana que ha capturado este puntero.</span><span class="sxs-lookup"><span data-stu-id="259b4-109">Instead, a [**WM_POINTERDOWN**](wm-pointerdown.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="259b4-110">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="259b4-110">\[!Important\]</span></span>  
> <span data-ttu-id="259b4-111">Las aplicaciones de escritorio deben tener en cuenta los ppp.</span><span class="sxs-lookup"><span data-stu-id="259b4-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="259b4-112">Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP.</span><span class="sxs-lookup"><span data-stu-id="259b4-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="259b4-113">La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla).</span><span class="sxs-lookup"><span data-stu-id="259b4-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="259b4-114">Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="259b4-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERDOWN                 0x0242
```



## <a name="parameters"></a><span data-ttu-id="259b4-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="259b4-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="259b4-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="259b4-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="259b4-117">Contiene el identificador de puntero e información adicional.</span><span class="sxs-lookup"><span data-stu-id="259b4-117">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="259b4-118">Use las siguientes macros para recuperar esta información.</span><span class="sxs-lookup"><span data-stu-id="259b4-118">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="259b4-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de puntero.</span><span class="sxs-lookup"><span data-stu-id="259b4-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier.</span></span>

<span data-ttu-id="259b4-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): el valor de la prueba de posicionamiento devolvió el procesamiento del mensaje de [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="259b4-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="259b4-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="259b4-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="259b4-122">Contiene la ubicación del punto del puntero.</span><span class="sxs-lookup"><span data-stu-id="259b4-122">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="259b4-123">Dado que el puntero puede establecer contacto con el dispositivo a través de un área no trivial, esta ubicación de punto puede ser una simplificación de un área de puntero más compleja.</span><span class="sxs-lookup"><span data-stu-id="259b4-123">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="259b4-124">Siempre que sea posible, una aplicación debe usar la información de área de puntero completa en lugar de la ubicación del punto.</span><span class="sxs-lookup"><span data-stu-id="259b4-124">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="259b4-125">Utilice las siguientes macros para recuperar las coordenadas físicas de la pantalla del punto.</span><span class="sxs-lookup"><span data-stu-id="259b4-125">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="259b4-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): la coordenada X (punto horizontal).</span><span class="sxs-lookup"><span data-stu-id="259b4-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="259b4-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): la coordenada Y (punto vertical).</span><span class="sxs-lookup"><span data-stu-id="259b4-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="259b4-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="259b4-128">Return value</span></span>

<span data-ttu-id="259b4-129">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="259b4-129">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="259b4-130">Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="259b4-130">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="259b4-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="259b4-131">Remarks</span></span>

<span data-ttu-id="259b4-132">Si la aplicación no procesa este mensaje, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) puede realizar una o varias acciones del sistema según el resultado de la prueba de posicionamiento incluido en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="259b4-132">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="259b4-133">Normalmente, no es necesario que las aplicaciones controlen este mensaje.</span><span class="sxs-lookup"><span data-stu-id="259b4-133">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="259b4-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="259b4-134">Requirements</span></span>



| <span data-ttu-id="259b4-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="259b4-135">Requirement</span></span> | <span data-ttu-id="259b4-136">Value</span><span class="sxs-lookup"><span data-stu-id="259b4-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="259b4-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="259b4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="259b4-138">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="259b4-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="259b4-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="259b4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="259b4-140">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="259b4-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="259b4-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="259b4-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="259b4-142"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="259b4-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="259b4-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="259b4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="259b4-144">Mensajes</span><span class="sxs-lookup"><span data-stu-id="259b4-144">Messages</span></span>](messages.md)
</dt> </dl>

 

