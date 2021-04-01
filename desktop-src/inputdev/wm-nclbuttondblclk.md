---
title: Mensaje de WM_NCLBUTTONDBLCLK (Winuser. h)
description: Se envía cuando el usuario hace doble clic en el botón primario del mouse mientras el cursor se encuentra dentro del área no cliente de una ventana. Este mensaje se envía a la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.
ms.assetid: fc655631-64d0-4cc5-b85e-25d274182994
keywords:
- Entrada de mouse y teclado de mensaje de WM_NCLBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_NCLBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db66edcb3b1645c6c34c72e35df53afc516dafc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150152"
---
# <a name="wm_nclbuttondblclk-message"></a><span data-ttu-id="2a8be-106">Mensaje de NCLBUTTONDBLCLK de WM \_</span><span class="sxs-lookup"><span data-stu-id="2a8be-106">WM\_NCLBUTTONDBLCLK message</span></span>

<span data-ttu-id="2a8be-107">Se envía cuando el usuario hace doble clic en el botón primario del mouse mientras el cursor se encuentra dentro del área no cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="2a8be-107">Posted when the user double-clicks the left mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="2a8be-108">Este mensaje se envía a la ventana que contiene el cursor.</span><span class="sxs-lookup"><span data-stu-id="2a8be-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="2a8be-109">Si una ventana ha capturado el mouse, este mensaje no se publica.</span><span class="sxs-lookup"><span data-stu-id="2a8be-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="2a8be-110">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2a8be-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCLBUTTONDBLCLK              0x00A3
```



## <a name="parameters"></a><span data-ttu-id="2a8be-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a8be-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a8be-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a8be-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a8be-113">El valor de la prueba de posicionamiento devuelto por la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado de procesar el mensaje de [**\_ NCHITTEST de WM**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="2a8be-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="2a8be-114">Para obtener una lista de los valores de las pruebas de posicionamiento, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="2a8be-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="2a8be-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a8be-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a8be-116">Estructura de [**puntos**](/previous-versions//dd162808(v=vs.85)) que contiene las coordenadas x e y del cursor.</span><span class="sxs-lookup"><span data-stu-id="2a8be-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="2a8be-117">Las coordenadas son relativas a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2a8be-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a8be-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a8be-118">Return value</span></span>

<span data-ttu-id="2a8be-119">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="2a8be-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a8be-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a8be-120">Remarks</span></span>

<span data-ttu-id="2a8be-121">También puede usar las macros [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) y [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer los valores de las coordenadas x e y de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2a8be-121">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="2a8be-122">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="2a8be-122">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="2a8be-123">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="2a8be-123">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="2a8be-124">De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) prueba el punto especificado para averiguar la ubicación del cursor y realiza la acción adecuada.</span><span class="sxs-lookup"><span data-stu-id="2a8be-124">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to find out the location of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="2a8be-125">Si es necesario, **DefWindowProc** envía el mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) a la ventana.</span><span class="sxs-lookup"><span data-stu-id="2a8be-125">If appropriate, **DefWindowProc** sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="2a8be-126">No es necesario que una ventana tenga el estilo **CS \_ DBLCLKS** para recibir mensajes de **WM \_ NCLBUTTONDBLCLK** .</span><span class="sxs-lookup"><span data-stu-id="2a8be-126">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCLBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="2a8be-127">El sistema genera un mensaje de **WM \_ NCLBUTTONDBLCLK** cuando el usuario presiona, suelta y vuelve a presionar el botón primario del mouse en el límite de tiempo de doble clic del sistema.</span><span class="sxs-lookup"><span data-stu-id="2a8be-127">The system generates a **WM\_NCLBUTTONDBLCLK** message when the user presses, releases, and again presses the left mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="2a8be-128">Al hacer doble clic en el botón primario del mouse, se generan cuatro mensajes: [**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM \_ NCLBUTTONUP**](wm-nclbuttonup.md), **WM \_ NCLBUTTONDBLCLK** y **WM \_ NCLBUTTONUP** de nuevo.</span><span class="sxs-lookup"><span data-stu-id="2a8be-128">Double-clicking the left mouse button actually generates four messages: [**WM\_NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM\_NCLBUTTONUP**](wm-nclbuttonup.md), **WM\_NCLBUTTONDBLCLK**, and **WM\_NCLBUTTONUP** again.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a8be-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a8be-129">Requirements</span></span>



| <span data-ttu-id="2a8be-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a8be-130">Requirement</span></span> | <span data-ttu-id="2a8be-131">Value</span><span class="sxs-lookup"><span data-stu-id="2a8be-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a8be-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a8be-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2a8be-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2a8be-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2a8be-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a8be-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2a8be-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2a8be-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2a8be-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a8be-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a8be-137"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a8be-137"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a8be-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a8be-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a8be-139">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2a8be-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2a8be-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2a8be-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="2a8be-141">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="2a8be-141">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="2a8be-142">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="2a8be-142">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="2a8be-143">**NCHITTEST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="2a8be-143">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="2a8be-144">**NCLBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="2a8be-144">**WM\_NCLBUTTONDOWN**</span></span>](wm-nclbuttondown.md)
</dt> <dt>

[<span data-ttu-id="2a8be-145">**NCLBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="2a8be-145">**WM\_NCLBUTTONUP**</span></span>](wm-nclbuttonup.md)
</dt> <dt>

[<span data-ttu-id="2a8be-146">**SYSCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="2a8be-146">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="2a8be-147">**Vista**</span><span class="sxs-lookup"><span data-stu-id="2a8be-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2a8be-148">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="2a8be-148">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="2a8be-149">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="2a8be-149">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2a8be-150">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="2a8be-150">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="2a8be-151">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a8be-151">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

