---
title: Mensaje de WM_NCRBUTTONDBLCLK (Winuser. h)
description: Se envía cuando el usuario hace doble clic con el botón secundario del mouse mientras el cursor se encuentra dentro del área no cliente de una ventana. Este mensaje se envía a la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.
ms.assetid: 20d62b05-07de-49da-b160-29fa1f5067fa
keywords:
- Entrada de mouse y teclado de mensaje de WM_NCRBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_NCRBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee33d9b31f99a00181427c9a715df792d95fe55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534714"
---
# <a name="wm_ncrbuttondblclk-message"></a><span data-ttu-id="a7f1f-106">Mensaje de NCRBUTTONDBLCLK de WM \_</span><span class="sxs-lookup"><span data-stu-id="a7f1f-106">WM\_NCRBUTTONDBLCLK message</span></span>

<span data-ttu-id="a7f1f-107">Se envía cuando el usuario hace doble clic con el botón secundario del mouse mientras el cursor se encuentra dentro del área no cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="a7f1f-107">Posted when the user double-clicks the right mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="a7f1f-108">Este mensaje se envía a la ventana que contiene el cursor.</span><span class="sxs-lookup"><span data-stu-id="a7f1f-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="a7f1f-109">Si una ventana ha capturado el mouse, este mensaje no se publica.</span><span class="sxs-lookup"><span data-stu-id="a7f1f-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="a7f1f-110">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a7f1f-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCRBUTTONDBLCLK              0x00A6
```



## <a name="parameters"></a><span data-ttu-id="a7f1f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7f1f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7f1f-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a7f1f-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7f1f-113">El valor de la prueba de posicionamiento devuelto por la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado de procesar el mensaje de [**\_ NCHITTEST de WM**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="a7f1f-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="a7f1f-114">Para obtener una lista de los valores de las pruebas de posicionamiento, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="a7f1f-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="a7f1f-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7f1f-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7f1f-116">Estructura de [**puntos**](/previous-versions//dd162808(v=vs.85)) que contiene las coordenadas x e y del cursor.</span><span class="sxs-lookup"><span data-stu-id="a7f1f-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="a7f1f-117">Las coordenadas son relativas a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a7f1f-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7f1f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7f1f-118">Return value</span></span>

<span data-ttu-id="a7f1f-119">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="a7f1f-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7f1f-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7f1f-120">Remarks</span></span>

<span data-ttu-id="a7f1f-121">No es necesario que una ventana tenga el estilo **CS \_ DBLCLKS** para recibir mensajes de **WM \_ NCRBUTTONDBLCLK** .</span><span class="sxs-lookup"><span data-stu-id="a7f1f-121">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCRBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="a7f1f-122">El sistema genera un mensaje de **WM \_ NCRBUTTONDBLCLK** cuando el usuario presiona, suelta y presiona el botón secundario del mouse en el límite de tiempo de doble clic del sistema.</span><span class="sxs-lookup"><span data-stu-id="a7f1f-122">The system generates a **WM\_NCRBUTTONDBLCLK** message when the user presses, releases, and again presses the right mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="a7f1f-123">Al hacer doble clic con el botón secundario del mouse, se generan cuatro mensajes: [**WM \_ NCRBUTTONDOWN**](wm-ncrbuttondown.md), [**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md), **WM \_ NCRBUTTONDBLCLK** y **WM \_ NCRBUTTONUP** de nuevo.</span><span class="sxs-lookup"><span data-stu-id="a7f1f-123">Double-clicking the right mouse button actually generates four messages: [**WM\_NCRBUTTONDOWN**](wm-ncrbuttondown.md), [**WM\_NCRBUTTONUP**](wm-ncrbuttonup.md), **WM\_NCRBUTTONDBLCLK**, and **WM\_NCRBUTTONUP** again.</span></span>

<span data-ttu-id="a7f1f-124">También puede usar las macros [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) y [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer los valores de las coordenadas x e y de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="a7f1f-124">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="a7f1f-125">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="a7f1f-125">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="a7f1f-126">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="a7f1f-126">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="a7f1f-127">Si es adecuado hacerlo, el sistema envía el mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) a la ventana.</span><span class="sxs-lookup"><span data-stu-id="a7f1f-127">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f1f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7f1f-128">Requirements</span></span>



| <span data-ttu-id="a7f1f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7f1f-129">Requirement</span></span> | <span data-ttu-id="a7f1f-130">Value</span><span class="sxs-lookup"><span data-stu-id="a7f1f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f1f-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7f1f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a7f1f-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a7f1f-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a7f1f-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7f1f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a7f1f-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a7f1f-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a7f1f-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7f1f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7f1f-136"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7f1f-136"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7f1f-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7f1f-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="a7f1f-138">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a7f1f-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a7f1f-139">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="a7f1f-139">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="a7f1f-140">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="a7f1f-140">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="a7f1f-141">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="a7f1f-141">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="a7f1f-142">**NCHITTEST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a7f1f-142">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="a7f1f-143">**NCRBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a7f1f-143">**WM\_NCRBUTTONDOWN**</span></span>](wm-ncrbuttondown.md)
</dt> <dt>

[<span data-ttu-id="a7f1f-144">**NCRBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a7f1f-144">**WM\_NCRBUTTONUP**</span></span>](wm-ncrbuttonup.md)
</dt> <dt>

[<span data-ttu-id="a7f1f-145">**SYSCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a7f1f-145">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="a7f1f-146">**Vista**</span><span class="sxs-lookup"><span data-stu-id="a7f1f-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a7f1f-147">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="a7f1f-147">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="a7f1f-148">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="a7f1f-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a7f1f-149">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="a7f1f-149">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="a7f1f-150">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a7f1f-150">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

