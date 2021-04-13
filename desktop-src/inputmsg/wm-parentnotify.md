---
title: Mensaje WM_PARENTNOTIFY
description: Se envía a una ventana cuando se produce una acción significativa en una ventana descendiente.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_PARENTNOTIFY
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 2e19edf25933a035514f9c42b0da6014eccfdb0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534707"
---
# <a name="wm_parentnotify-message"></a><span data-ttu-id="9ba17-104">Mensaje WM_PARENTNOTIFY</span><span class="sxs-lookup"><span data-stu-id="9ba17-104">WM_PARENTNOTIFY message</span></span>

<span data-ttu-id="9ba17-105">Se envía a una ventana cuando se produce una acción significativa en una ventana descendiente.</span><span class="sxs-lookup"><span data-stu-id="9ba17-105">Sent to a window when a significant action occurs on a descendant window.</span></span> <span data-ttu-id="9ba17-106">Este mensaje se ha ampliado para incluir el evento [**WM_POINTERDOWN**](wm-pointerdown.md) .</span><span class="sxs-lookup"><span data-stu-id="9ba17-106">This message is now extended to include the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span> <span data-ttu-id="9ba17-107">Cuando se crea la ventana secundaria, el sistema envía [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) justo antes de que la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) que crea la ventana devuelva.</span><span class="sxs-lookup"><span data-stu-id="9ba17-107">When the child window is being created, the system sends [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) just before the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function that creates the window returns.</span></span> <span data-ttu-id="9ba17-108">Cuando se destruye la ventana secundaria, el sistema envía el mensaje antes de que se produzca cualquier procesamiento para destruir la ventana.</span><span class="sxs-lookup"><span data-stu-id="9ba17-108">When the child window is being destroyed, the system sends the message before any processing to destroy the window takes place.</span></span>

<span data-ttu-id="9ba17-109">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9ba17-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="9ba17-110">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="9ba17-110">\[!Important\]</span></span>  
> <span data-ttu-id="9ba17-111">Las aplicaciones de escritorio deben tener en cuenta los ppp.</span><span class="sxs-lookup"><span data-stu-id="9ba17-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="9ba17-112">Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP.</span><span class="sxs-lookup"><span data-stu-id="9ba17-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="9ba17-113">La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla).</span><span class="sxs-lookup"><span data-stu-id="9ba17-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="9ba17-114">Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9ba17-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a><span data-ttu-id="9ba17-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ba17-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ba17-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ba17-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ba17-117">La palabra de orden inferior de *wParam* especifica el evento para el que se notifica al elemento primario.</span><span class="sxs-lookup"><span data-stu-id="9ba17-117">The low-order word of *wParam* specifies the event for which the parent is being notified.</span></span> <span data-ttu-id="9ba17-118">El valor de la palabra de orden superior depende del valor de la palabra de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="9ba17-118">The value of the high-order word depends on the value of the low-order word.</span></span> <span data-ttu-id="9ba17-119">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9ba17-119">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="9ba17-120">LOWORD (*wParam*)</span><span class="sxs-lookup"><span data-stu-id="9ba17-120">LOWORD(*wParam*)</span></span>                                                                                                                                                                                                             | <span data-ttu-id="9ba17-121">Significado</span><span class="sxs-lookup"><span data-stu-id="9ba17-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <span data-ttu-id="9ba17-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="9ba17-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span></span> </dl>                | <span data-ttu-id="9ba17-123">Se está creando la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="9ba17-123">The child window is being created.</span></span><br/> <span data-ttu-id="9ba17-124">HIWORD (*wParam*) es el identificador de la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="9ba17-124">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="9ba17-125">*lParam* es un identificador de la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="9ba17-125">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <span data-ttu-id="9ba17-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="9ba17-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span></span> </dl>             | <span data-ttu-id="9ba17-127">Se está destruyendo la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="9ba17-127">The child window is being destroyed.</span></span><br/> <span data-ttu-id="9ba17-128">HIWORD (*wParam*) es el identificador de la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="9ba17-128">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="9ba17-129">*lParam* es un identificador de la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="9ba17-129">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <span data-ttu-id="9ba17-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span><span class="sxs-lookup"><span data-stu-id="9ba17-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span></span> </dl> | <span data-ttu-id="9ba17-131">El usuario ha colocado el cursor sobre la ventana secundaria y ha hecho clic en el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="9ba17-131">The user has placed the cursor over the child window and has clicked the left mouse button.</span></span><br/> <span data-ttu-id="9ba17-132">HIWORD (*wParam*) no está definido.</span><span class="sxs-lookup"><span data-stu-id="9ba17-132">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="9ba17-133">*lParam* es la coordenada x del cursor es la palabra de orden inferior y la coordenada y del cursor es la palabra de orden superior.</span><span class="sxs-lookup"><span data-stu-id="9ba17-133">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <span data-ttu-id="9ba17-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span><span class="sxs-lookup"><span data-stu-id="9ba17-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span></span> </dl> | <span data-ttu-id="9ba17-135">El usuario ha colocado el cursor sobre la ventana secundaria y ha hecho clic en el botón central del mouse.</span><span class="sxs-lookup"><span data-stu-id="9ba17-135">The user has placed the cursor over the child window and has clicked the middle mouse button.</span></span><br/> <span data-ttu-id="9ba17-136">HIWORD (*wParam*) no está definido.</span><span class="sxs-lookup"><span data-stu-id="9ba17-136">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="9ba17-137">*lParam* es la coordenada x del cursor es la palabra de orden inferior y la coordenada y del cursor es la palabra de orden superior.</span><span class="sxs-lookup"><span data-stu-id="9ba17-137">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <span data-ttu-id="9ba17-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span><span class="sxs-lookup"><span data-stu-id="9ba17-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span></span> </dl> | <span data-ttu-id="9ba17-139">El usuario ha colocado el cursor sobre la ventana secundaria y ha hecho clic con el botón secundario del mouse.</span><span class="sxs-lookup"><span data-stu-id="9ba17-139">The user has placed the cursor over the child window and has clicked the right mouse button.</span></span><br/> <span data-ttu-id="9ba17-140">HIWORD (*wParam*) no está definido.</span><span class="sxs-lookup"><span data-stu-id="9ba17-140">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="9ba17-141">*lParam* es la coordenada x del cursor es la palabra de orden inferior y la coordenada y del cursor es la palabra de orden superior.</span><span class="sxs-lookup"><span data-stu-id="9ba17-141">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <span data-ttu-id="9ba17-142"><dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt></span><span class="sxs-lookup"><span data-stu-id="9ba17-142"><dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt></span></span> </dl> | <span data-ttu-id="9ba17-143">El usuario ha colocado el cursor sobre la ventana secundaria y ha hecho clic en el primer o el segundo botón X.</span><span class="sxs-lookup"><span data-stu-id="9ba17-143">The user has placed the cursor over the child window and has clicked the first or second X button.</span></span><br/> <span data-ttu-id="9ba17-144">HIWORD (*wParam*) indica el botón que se presionó.</span><span class="sxs-lookup"><span data-stu-id="9ba17-144">HIWORD(*wParam*) indicates which button was pressed.</span></span> <span data-ttu-id="9ba17-145">Este parámetro puede ser uno de los siguientes valores: XBUTTON1 o XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="9ba17-145">This parameter can be one of the following values: XBUTTON1 or XBUTTON2.</span></span><br/> <span data-ttu-id="9ba17-146">*lParam* es la coordenada x del cursor es la palabra de orden inferior y la coordenada y del cursor es la palabra de orden superior.</span><span class="sxs-lookup"><span data-stu-id="9ba17-146">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <span data-ttu-id="9ba17-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span><span class="sxs-lookup"><span data-stu-id="9ba17-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span></span> </dl> | <span data-ttu-id="9ba17-148">Un puntero ha hecho contacto con la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="9ba17-148">A pointer has made contact with the child window.</span></span><br/> <span data-ttu-id="9ba17-149">HIWORD (*wParam*) contiene el identificador del puntero que generó el evento [**WM_POINTERDOWN**](wm-pointerdown.md) .</span><span class="sxs-lookup"><span data-stu-id="9ba17-149">HIWORD(*wParam*) contains the identifier of the pointer that generated the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span><br/>                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="9ba17-150">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ba17-150">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ba17-151">Contiene la ubicación del punto del puntero.</span><span class="sxs-lookup"><span data-stu-id="9ba17-151">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="9ba17-152">Dado que el puntero puede establecer contacto con el dispositivo a través de un área no trivial, esta ubicación de punto puede ser una simplificación de un área de puntero más compleja.</span><span class="sxs-lookup"><span data-stu-id="9ba17-152">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="9ba17-153">Siempre que sea posible, una aplicación debe usar la información de área de puntero completa en lugar de la ubicación del punto.</span><span class="sxs-lookup"><span data-stu-id="9ba17-153">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="9ba17-154">Utilice las siguientes macros para recuperar las coordenadas físicas de la pantalla del punto.</span><span class="sxs-lookup"><span data-stu-id="9ba17-154">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="9ba17-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): la coordenada X (punto horizontal).</span><span class="sxs-lookup"><span data-stu-id="9ba17-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="9ba17-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): la coordenada Y (punto vertical).</span><span class="sxs-lookup"><span data-stu-id="9ba17-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ba17-157">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ba17-157">Return value</span></span>

<span data-ttu-id="9ba17-158">Si la aplicación procesa este mensaje, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="9ba17-158">If the application processes this message, it returns zero.</span></span>

<span data-ttu-id="9ba17-159">Si la aplicación no procesa este mensaje, llama a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="9ba17-159">If the application does not process this message, it calls [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ba17-160">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ba17-160">Remarks</span></span>

<span data-ttu-id="9ba17-161">Este mensaje también se envía a todas las ventanas antecesoras de la ventana secundaria, incluida la ventana de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="9ba17-161">This message is also sent to all ancestor windows of the child window, including the top-level window.</span></span>

<span data-ttu-id="9ba17-162">Todas las ventanas secundarias, excepto las que tienen el estilo de ventana extendido **WS_EX_NOPARENTNOTIFY** , envían este mensaje a sus ventanas principales.</span><span class="sxs-lookup"><span data-stu-id="9ba17-162">All child windows, except those that have the **WS_EX_NOPARENTNOTIFY** extended window style, send this message to their parent windows.</span></span> <span data-ttu-id="9ba17-163">De forma predeterminada, las ventanas secundarias de un cuadro de diálogo tienen el estilo de **WS_EX_NOPARENTNOTIFY** , a menos que se llame a la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) para crear la ventana secundaria sin este estilo.</span><span class="sxs-lookup"><span data-stu-id="9ba17-163">By default, child windows in a dialog box have the **WS_EX_NOPARENTNOTIFY** style, unless the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function is called to create the child window without this style.</span></span>

<span data-ttu-id="9ba17-164">Esta notificación proporciona a las ventanas antecesoras de la ventana secundaria una oportunidad para examinar la información del puntero y, si es necesario, capturar el puntero mediante las funciones de captura de puntero.</span><span class="sxs-lookup"><span data-stu-id="9ba17-164">This notification provides the child window's ancestor windows an opportunity to examine the pointer information and, if required, capture the pointer using the pointer capture functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba17-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ba17-165">Requirements</span></span>



| <span data-ttu-id="9ba17-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ba17-166">Requirement</span></span> | <span data-ttu-id="9ba17-167">Value</span><span class="sxs-lookup"><span data-stu-id="9ba17-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba17-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ba17-168">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba17-169">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ba17-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="9ba17-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ba17-170">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba17-171">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ba17-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9ba17-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ba17-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ba17-173"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ba17-173"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ba17-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ba17-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba17-175">Mensajes</span><span class="sxs-lookup"><span data-stu-id="9ba17-175">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="9ba17-176">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="9ba17-176">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="9ba17-177">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="9ba17-177">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

<span data-ttu-id="9ba17-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ba17-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9ba17-179">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ba17-179">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9ba17-180">**WM_CREATE**</span><span class="sxs-lookup"><span data-stu-id="9ba17-180">**WM_CREATE**</span></span>](../winmsg/wm-create.md)
</dt> <dt>

[<span data-ttu-id="9ba17-181">**WM_DESTROY**</span><span class="sxs-lookup"><span data-stu-id="9ba17-181">**WM_DESTROY**</span></span>](../winmsg/wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="9ba17-182">**WM_LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="9ba17-182">**WM_LBUTTONDOWN**</span></span>](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[<span data-ttu-id="9ba17-183">**WM_MBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="9ba17-183">**WM_MBUTTONDOWN**</span></span>](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[<span data-ttu-id="9ba17-184">**WM_RBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="9ba17-184">**WM_RBUTTONDOWN**</span></span>](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[<span data-ttu-id="9ba17-185">**WM_XBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="9ba17-185">**WM_XBUTTONDOWN**</span></span>](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

