---
title: Mensaje de WM_NCMBUTTONDBLCLK (Winuser. h)
description: Se envía cuando el usuario hace doble clic en el botón central del mouse mientras el cursor se encuentra dentro del área no cliente de una ventana. Este mensaje se envía a la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.
ms.assetid: 7c0f8d6e-eb37-4873-a3f8-777e8b0b22bc
keywords:
- Entrada de mouse y teclado de mensaje de WM_NCMBUTTONDBLCLK
topic_type:
- apiref
api_name:
- WM_NCMBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612a0a7ca0a5731691ec244df505e3d058216e2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801951"
---
# <a name="wm_ncmbuttondblclk-message"></a><span data-ttu-id="c8774-106">Mensaje de NCMBUTTONDBLCLK de WM \_</span><span class="sxs-lookup"><span data-stu-id="c8774-106">WM\_NCMBUTTONDBLCLK message</span></span>

<span data-ttu-id="c8774-107">Se envía cuando el usuario hace doble clic en el botón central del mouse mientras el cursor se encuentra dentro del área no cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="c8774-107">Posted when the user double-clicks the middle mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="c8774-108">Este mensaje se envía a la ventana que contiene el cursor.</span><span class="sxs-lookup"><span data-stu-id="c8774-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="c8774-109">Si una ventana ha capturado el mouse, este mensaje no se publica.</span><span class="sxs-lookup"><span data-stu-id="c8774-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="c8774-110">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c8774-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMBUTTONDBLCLK              0x00A9
```



## <a name="parameters"></a><span data-ttu-id="c8774-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8774-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8774-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8774-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8774-113">El valor de la prueba de posicionamiento devuelto por la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado de procesar el mensaje de [**\_ NCHITTEST de WM**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="c8774-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="c8774-114">Para obtener una lista de los valores de las pruebas de posicionamiento, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="c8774-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="c8774-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8774-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8774-116">Estructura de [**puntos**](/previous-versions//dd162808(v=vs.85)) que contiene las coordenadas x e y del cursor.</span><span class="sxs-lookup"><span data-stu-id="c8774-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="c8774-117">Las coordenadas son relativas a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="c8774-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8774-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8774-118">Return value</span></span>

<span data-ttu-id="c8774-119">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="c8774-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8774-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8774-120">Remarks</span></span>

<span data-ttu-id="c8774-121">No es necesario que una ventana tenga el estilo **CS \_ DBLCLKS** para recibir mensajes de **WM \_ NCMBUTTONDBLCLK** .</span><span class="sxs-lookup"><span data-stu-id="c8774-121">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCMBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="c8774-122">El sistema genera un mensaje de **WM \_ NCMBUTTONDBLCLK** cuando el usuario presiona, suelta y presiona el botón central del mouse dentro del límite de tiempo de doble clic del sistema.</span><span class="sxs-lookup"><span data-stu-id="c8774-122">The system generates a **WM\_NCMBUTTONDBLCLK** message when the user presses, releases, and again presses the middle mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="c8774-123">Al hacer doble clic en el botón central del mouse, se generan cuatro mensajes: [**WM \_ NCMBUTTONDOWN**](wm-ncmbuttondown.md), [**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md), **WM \_ NCMBUTTONDBLCLK** y **WM \_ NCMBUTTONUP** de nuevo.</span><span class="sxs-lookup"><span data-stu-id="c8774-123">Double-clicking the middle mouse button actually generates four messages: [**WM\_NCMBUTTONDOWN**](wm-ncmbuttondown.md), [**WM\_NCMBUTTONUP**](wm-ncmbuttonup.md), **WM\_NCMBUTTONDBLCLK**, and **WM\_NCMBUTTONUP** again.</span></span>

<span data-ttu-id="c8774-124">También puede usar las macros [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) y [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer los valores de las coordenadas x e y de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="c8774-124">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="c8774-125">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="c8774-125">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="c8774-126">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="c8774-126">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="c8774-127">Si es adecuado hacerlo, el sistema envía el mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) a la ventana.</span><span class="sxs-lookup"><span data-stu-id="c8774-127">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8774-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8774-128">Requirements</span></span>



| <span data-ttu-id="c8774-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8774-129">Requirement</span></span> | <span data-ttu-id="c8774-130">Value</span><span class="sxs-lookup"><span data-stu-id="c8774-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8774-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8774-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c8774-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c8774-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c8774-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8774-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c8774-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c8774-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c8774-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8774-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8774-136"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8774-136"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8774-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8774-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8774-138">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c8774-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c8774-139">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c8774-139">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c8774-140">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="c8774-140">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="c8774-141">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="c8774-141">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="c8774-142">**NCHITTEST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c8774-142">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="c8774-143">**NCMBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c8774-143">**WM\_NCMBUTTONDOWN**</span></span>](wm-ncmbuttondown.md)
</dt> <dt>

[<span data-ttu-id="c8774-144">**NCMBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c8774-144">**WM\_NCMBUTTONUP**</span></span>](wm-ncmbuttonup.md)
</dt> <dt>

[<span data-ttu-id="c8774-145">**SYSCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c8774-145">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="c8774-146">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c8774-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c8774-147">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="c8774-147">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="c8774-148">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="c8774-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c8774-149">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="c8774-149">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="c8774-150">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c8774-150">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

