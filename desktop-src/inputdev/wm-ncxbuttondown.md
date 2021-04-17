---
title: Mensaje de WM_NCXBUTTONDOWN (Winuser. h)
description: Se envía cuando el usuario presiona el primer o el segundo botón X mientras el cursor se encuentra en el área no cliente de una ventana. Este mensaje se envía a la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.
ms.assetid: 72744c98-1898-4548-bd10-61ad53eeab15
keywords:
- Entrada de mouse y teclado de mensaje de WM_NCXBUTTONDOWN
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd615b1e30e013f23097cdc7a8ca7c22c338684a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714585"
---
# <a name="wm_ncxbuttondown-message"></a><span data-ttu-id="cd7f1-106">Mensaje de NCXBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="cd7f1-106">WM\_NCXBUTTONDOWN message</span></span>

<span data-ttu-id="cd7f1-107">Se envía cuando el usuario presiona el primer o el segundo botón X mientras el cursor se encuentra en el área no cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-107">Posted when the user presses the first or second X button while the cursor is in the nonclient area of a window.</span></span> <span data-ttu-id="cd7f1-108">Este mensaje se envía a la ventana que contiene el cursor.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="cd7f1-109">Si una ventana ha capturado el mouse, este mensaje *no* se publica.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-109">If a window has captured the mouse, this message is *not* posted.</span></span>

<span data-ttu-id="cd7f1-110">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cd7f1-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCXBUTTONDOWN                0x00AB
```



## <a name="parameters"></a><span data-ttu-id="cd7f1-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd7f1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd7f1-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd7f1-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd7f1-113">La palabra de orden inferior especifica el valor de la prueba de posicionamiento devuelto por la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para procesar el mensaje de [**\_ NCHITTEST de WM**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="cd7f1-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function from processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="cd7f1-114">Para obtener una lista de los valores de las pruebas de posicionamiento, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span> <span data-ttu-id="cd7f1-115">La palabra de orden superior indica el botón que se presionó.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-115">The high-order word indicates which button was pressed.</span></span> <span data-ttu-id="cd7f1-116">Puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-116">It can be one of the following values.</span></span>



| <span data-ttu-id="cd7f1-117">Value</span><span class="sxs-lookup"><span data-stu-id="cd7f1-117">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="cd7f1-118">Significado</span><span class="sxs-lookup"><span data-stu-id="cd7f1-118">Meaning</span></span>                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="cd7f1-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="cd7f1-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="cd7f1-120">Se presionó el primer botón X.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-120">The first X button was pressed.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="cd7f1-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="cd7f1-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="cd7f1-122">Se presionó el segundo botón X.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-122">The second X button was pressed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd7f1-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd7f1-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd7f1-124">Puntero a una estructura de [**puntos**](/previous-versions//dd162808(v=vs.85)) que contiene las coordenadas x e y del cursor.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-124">A pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="cd7f1-125">Las coordenadas son relativas a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-125">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd7f1-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd7f1-126">Return value</span></span>

<span data-ttu-id="cd7f1-127">Si una aplicación procesa este mensaje, debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-127">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="cd7f1-128">Para obtener más información sobre cómo procesar el valor devuelto, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-128">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd7f1-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd7f1-129">Remarks</span></span>

<span data-ttu-id="cd7f1-130">Use el código siguiente para obtener la información del parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="cd7f1-130">Use the following code to get the information in the *wParam* parameter.</span></span>


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



<span data-ttu-id="cd7f1-131">También puede usar el código siguiente para obtener las coordenadas x e y de *lParam*:</span><span class="sxs-lookup"><span data-stu-id="cd7f1-131">You can also use the following code to get the x- and y-coordinates from *lParam*:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="cd7f1-132">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-132">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="cd7f1-133">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-133">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="cd7f1-134">De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) prueba el punto especificado para obtener la posición del cursor y realiza la acción adecuada.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-134">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to get the position of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="cd7f1-135">Si es necesario, envía el mensaje de [**\_ SYSCOMMAND de WM**](/windows/desktop/menurc/wm-syscommand) a la ventana.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-135">If appropriate, it sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="cd7f1-136">A diferencia de los mensajes [**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM \_ NCMBUTTONDOWN**](wm-ncmbuttondown.md)y [**WM \_ NCRBUTTONDOWN**](wm-ncrbuttondown.md) , una aplicación debe devolver **true** desde este mensaje si lo procesa.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-136">Unlike the [**WM\_NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM\_NCMBUTTONDOWN**](wm-ncmbuttondown.md), and [**WM\_NCRBUTTONDOWN**](wm-ncrbuttondown.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="cd7f1-137">Esto permitirá que el software que simula este mensaje en sistemas Windows anteriores a Windows 2000 determine si el procedimiento de ventana procesó el mensaje o llamó a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para procesarlo.</span><span class="sxs-lookup"><span data-stu-id="cd7f1-137">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd7f1-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd7f1-138">Requirements</span></span>



| <span data-ttu-id="cd7f1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd7f1-139">Requirement</span></span> | <span data-ttu-id="cd7f1-140">Value</span><span class="sxs-lookup"><span data-stu-id="cd7f1-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd7f1-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd7f1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cd7f1-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cd7f1-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cd7f1-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd7f1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cd7f1-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cd7f1-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cd7f1-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd7f1-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd7f1-146"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd7f1-146"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd7f1-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd7f1-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd7f1-148">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="cd7f1-148">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cd7f1-149">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="cd7f1-149">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="cd7f1-150">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="cd7f1-150">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="cd7f1-151">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="cd7f1-151">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="cd7f1-152">**NCHITTEST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="cd7f1-152">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="cd7f1-153">**NCXBUTTONDBLCLK de WM \_**</span><span class="sxs-lookup"><span data-stu-id="cd7f1-153">**WM\_NCXBUTTONDBLCLK**</span></span>](wm-ncxbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="cd7f1-154">**NCXBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="cd7f1-154">**WM\_NCXBUTTONUP**</span></span>](wm-ncxbuttonup.md)
</dt> <dt>

[<span data-ttu-id="cd7f1-155">**SYSCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="cd7f1-155">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="cd7f1-156">**Vista**</span><span class="sxs-lookup"><span data-stu-id="cd7f1-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cd7f1-157">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="cd7f1-157">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="cd7f1-158">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="cd7f1-158">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="cd7f1-159">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="cd7f1-159">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="cd7f1-160">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cd7f1-160">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

