---
title: Mensaje de WM_NCLBUTTONDOWN (Winuser. h)
description: Se envía cuando el usuario presiona el botón primario del mouse mientras el cursor se encuentra dentro del área no cliente de una ventana. Este mensaje se envía a la ventana que contiene el cursor. Si una ventana ha capturado el mouse, este mensaje no se publica.
ms.assetid: fca6d9ec-c549-4c82-9a80-15471481f876
keywords:
- Entrada de mouse y teclado de mensaje de WM_NCLBUTTONDOWN
topic_type:
- apiref
api_name:
- WM_NCLBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c31a6feded21d3a43d7b87c0de6a03724dcf2c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801952"
---
# <a name="wm_nclbuttondown-message"></a><span data-ttu-id="7c398-106">Mensaje de NCLBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="7c398-106">WM\_NCLBUTTONDOWN message</span></span>

<span data-ttu-id="7c398-107">Se envía cuando el usuario presiona el botón primario del mouse mientras el cursor se encuentra dentro del área no cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="7c398-107">Posted when the user presses the left mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="7c398-108">Este mensaje se envía a la ventana que contiene el cursor.</span><span class="sxs-lookup"><span data-stu-id="7c398-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="7c398-109">Si una ventana ha capturado el mouse, este mensaje no se publica.</span><span class="sxs-lookup"><span data-stu-id="7c398-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="7c398-110">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7c398-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCLBUTTONDOWN                0x00A1
```



## <a name="parameters"></a><span data-ttu-id="7c398-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c398-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c398-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c398-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c398-113">El valor de la prueba de posicionamiento devuelto por la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado de procesar el mensaje de [**\_ NCHITTEST de WM**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="7c398-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="7c398-114">Para obtener una lista de los valores de las pruebas de posicionamiento, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="7c398-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="7c398-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c398-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c398-116">Estructura de [**puntos**](/previous-versions//dd162808(v=vs.85)) que contiene las coordenadas x e y del cursor.</span><span class="sxs-lookup"><span data-stu-id="7c398-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="7c398-117">Las coordenadas son relativas a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="7c398-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c398-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c398-118">Return value</span></span>

<span data-ttu-id="7c398-119">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="7c398-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c398-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c398-120">Remarks</span></span>

<span data-ttu-id="7c398-121">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) comprueba el punto especificado para encontrar la ubicación del cursor y realiza la acción adecuada.</span><span class="sxs-lookup"><span data-stu-id="7c398-121">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to find the location of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="7c398-122">Si es necesario, **DefWindowProc** envía el mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) a la ventana.</span><span class="sxs-lookup"><span data-stu-id="7c398-122">If appropriate, **DefWindowProc** sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="7c398-123">También puede usar las macros [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) y [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer los valores de las coordenadas x e y de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="7c398-123">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="7c398-124">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="7c398-124">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="7c398-125">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="7c398-125">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7c398-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c398-126">Requirements</span></span>



| <span data-ttu-id="7c398-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c398-127">Requirement</span></span> | <span data-ttu-id="7c398-128">Value</span><span class="sxs-lookup"><span data-stu-id="7c398-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c398-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c398-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7c398-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7c398-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7c398-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c398-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7c398-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7c398-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7c398-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c398-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c398-134"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c398-134"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c398-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c398-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c398-136">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="7c398-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7c398-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="7c398-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="7c398-138">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="7c398-138">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="7c398-139">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="7c398-139">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="7c398-140">**NCHITTEST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="7c398-140">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="7c398-141">**NCLBUTTONDBLCLK de WM \_**</span><span class="sxs-lookup"><span data-stu-id="7c398-141">**WM\_NCLBUTTONDBLCLK**</span></span>](wm-nclbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="7c398-142">**NCLBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="7c398-142">**WM\_NCLBUTTONUP**</span></span>](wm-nclbuttonup.md)
</dt> <dt>

[<span data-ttu-id="7c398-143">**SYSCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="7c398-143">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="7c398-144">**Vista**</span><span class="sxs-lookup"><span data-stu-id="7c398-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7c398-145">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="7c398-145">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="7c398-146">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="7c398-146">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7c398-147">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="7c398-147">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="7c398-148">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7c398-148">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

