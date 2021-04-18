---
title: Mensaje de WM_NCXBUTTONDBLCLK (Winuser. h)
description: Se envía cuando el usuario hace doble clic en el primer o el segundo botón X mientras el cursor se encuentra en el área no cliente de una ventana. Este mensaje se envía a la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.
ms.assetid: 8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef
keywords:
- Entrada de mouse y teclado de mensaje de WM_NCXBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1455f6d6c2fa40f34bbfbe00e0c7a30daa52f375
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714625"
---
# <a name="wm_ncxbuttondblclk-message"></a><span data-ttu-id="ae641-106">Mensaje de NCXBUTTONDBLCLK de WM \_</span><span class="sxs-lookup"><span data-stu-id="ae641-106">WM\_NCXBUTTONDBLCLK message</span></span>

<span data-ttu-id="ae641-107">Se envía cuando el usuario hace doble clic en el primer o el segundo botón X mientras el cursor se encuentra en el área no cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="ae641-107">Posted when the user double-clicks the first or second X button while the cursor is in the nonclient area of a window.</span></span> <span data-ttu-id="ae641-108">Este mensaje se envía a la ventana que contiene el cursor.</span><span class="sxs-lookup"><span data-stu-id="ae641-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="ae641-109">Si una ventana ha capturado el mouse, este mensaje no se publica.</span><span class="sxs-lookup"><span data-stu-id="ae641-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="ae641-110">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ae641-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCXBUTTONDBLCLK              0x00AD
```



## <a name="parameters"></a><span data-ttu-id="ae641-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae641-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae641-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae641-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae641-113">La palabra de orden inferior especifica el valor de la prueba de posicionamiento devuelto por la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para procesar el mensaje de [**\_ NCHITTEST de WM**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="ae641-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function from processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="ae641-114">Para obtener una lista de los valores de las pruebas de posicionamiento, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="ae641-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="ae641-115">La palabra de orden superior indica en qué botón se hizo doble clic.</span><span class="sxs-lookup"><span data-stu-id="ae641-115">The high-order word indicates which button was double-clicked.</span></span> <span data-ttu-id="ae641-116">Puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="ae641-116">It can be one of the following values.</span></span>



| <span data-ttu-id="ae641-117">Value</span><span class="sxs-lookup"><span data-stu-id="ae641-117">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="ae641-118">Significado</span><span class="sxs-lookup"><span data-stu-id="ae641-118">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="ae641-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="ae641-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="ae641-120">Se hizo doble clic en el primer botón X..</span><span class="sxs-lookup"><span data-stu-id="ae641-120">The first X button was double-clicked..</span></span><br/> |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="ae641-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="ae641-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="ae641-122">Se hizo doble clic en el segundo botón X.</span><span class="sxs-lookup"><span data-stu-id="ae641-122">The second X button was double-clicked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ae641-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae641-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae641-124">Puntero a una estructura de [**puntos**](/previous-versions//dd162808(v=vs.85)) que contiene las coordenadas x e y del cursor.</span><span class="sxs-lookup"><span data-stu-id="ae641-124">A pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="ae641-125">Las coordenadas son relativas a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ae641-125">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae641-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae641-126">Return value</span></span>

<span data-ttu-id="ae641-127">Si una aplicación procesa este mensaje, debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="ae641-127">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="ae641-128">Para obtener más información sobre cómo procesar el valor devuelto, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="ae641-128">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae641-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae641-129">Remarks</span></span>

<span data-ttu-id="ae641-130">Use el código siguiente para obtener la información del parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="ae641-130">Use the following code to get the information in the *wParam* parameter.</span></span>


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



<span data-ttu-id="ae641-131">También puede usar el código siguiente para obtener las coordenadas x e y de *lParam*:</span><span class="sxs-lookup"><span data-stu-id="ae641-131">You can also use the following code to get the x- and y-coordinates from *lParam*:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="ae641-132">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="ae641-132">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="ae641-133">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="ae641-133">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="ae641-134">De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) prueba el punto especificado para obtener la posición del cursor y realiza la acción adecuada.</span><span class="sxs-lookup"><span data-stu-id="ae641-134">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to get the position of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="ae641-135">Si es necesario, envía el mensaje de [**\_ SYSCOMMAND de WM**](/windows/desktop/menurc/wm-syscommand) a la ventana.</span><span class="sxs-lookup"><span data-stu-id="ae641-135">If appropriate, it sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="ae641-136">No es necesario que una ventana tenga el estilo **CS \_ DBLCLKS** para recibir mensajes de **WM \_ NCXBUTTONDBLCLK** .</span><span class="sxs-lookup"><span data-stu-id="ae641-136">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCXBUTTONDBLCLK** messages.</span></span> <span data-ttu-id="ae641-137">El sistema genera un mensaje de **WM \_ NCXBUTTONDBLCLK** cuando el usuario presiona, suelta y presiona un botón X dentro del límite de tiempo de doble clic del sistema.</span><span class="sxs-lookup"><span data-stu-id="ae641-137">The system generates a **WM\_NCXBUTTONDBLCLK** message when the user presses, releases, and again presses an X button within the system's double-click time limit.</span></span> <span data-ttu-id="ae641-138">Al hacer doble clic en uno de estos botones, se generan cuatro mensajes: [**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md), [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md), **WM \_ NCXBUTTONDBLCLK** y **WM \_ NCXBUTTONUP** de nuevo.</span><span class="sxs-lookup"><span data-stu-id="ae641-138">Double-clicking one of these buttons actually generates four messages: [**WM\_NCXBUTTONDOWN**](wm-ncxbuttondown.md), [**WM\_NCXBUTTONUP**](wm-ncxbuttonup.md), **WM\_NCXBUTTONDBLCLK**, and **WM\_NCXBUTTONUP** again.</span></span>

<span data-ttu-id="ae641-139">A diferencia de los mensajes [**WM \_ NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md), [**WM \_ NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md)y [**WM \_ NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md) , una aplicación debe devolver **true** desde este mensaje si lo procesa.</span><span class="sxs-lookup"><span data-stu-id="ae641-139">Unlike the [**WM\_NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md), [**WM\_NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md), and [**WM\_NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="ae641-140">Esto permitirá que el software que simula este mensaje en sistemas Windows anteriores a Windows 2000 determine si el procedimiento de ventana procesó el mensaje o llamó a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para procesarlo.</span><span class="sxs-lookup"><span data-stu-id="ae641-140">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae641-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae641-141">Requirements</span></span>



| <span data-ttu-id="ae641-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae641-142">Requirement</span></span> | <span data-ttu-id="ae641-143">Value</span><span class="sxs-lookup"><span data-stu-id="ae641-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae641-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae641-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ae641-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ae641-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ae641-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae641-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ae641-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ae641-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ae641-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae641-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae641-149"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae641-149"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae641-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae641-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae641-151">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ae641-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ae641-152">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="ae641-152">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="ae641-153">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="ae641-153">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="ae641-154">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="ae641-154">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="ae641-155">**NCHITTEST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ae641-155">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="ae641-156">**NCXBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ae641-156">**WM\_NCXBUTTONDOWN**</span></span>](wm-ncxbuttondown.md)
</dt> <dt>

[<span data-ttu-id="ae641-157">**NCXBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ae641-157">**WM\_NCXBUTTONUP**</span></span>](wm-ncxbuttonup.md)
</dt> <dt>

[<span data-ttu-id="ae641-158">**SYSCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ae641-158">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="ae641-159">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ae641-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ae641-160">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="ae641-160">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="ae641-161">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="ae641-161">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ae641-162">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="ae641-162">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="ae641-163">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ae641-163">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

