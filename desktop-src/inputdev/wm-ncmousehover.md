---
title: Mensaje de WM_NCMOUSEHOVER (Winuser. h)
description: Se envía a una ventana cuando el cursor se mantiene sobre el área no cliente de la ventana durante el período de tiempo especificado en una llamada anterior a TrackMouseEvent.
ms.assetid: ca1afdc2-7884-445e-b9b7-4d7dd5dcea38
keywords:
- Entrada de mouse y teclado de mensaje de WM_NCMOUSEHOVER
topic_type:
- apiref
api_name:
- WM_NCMOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde2e70b04602de5936e945789007a6c5fea8542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079686"
---
# <a name="wm_ncmousehover-message"></a><span data-ttu-id="64b9d-104">Mensaje de NCMOUSEHOVER de WM \_</span><span class="sxs-lookup"><span data-stu-id="64b9d-104">WM\_NCMOUSEHOVER message</span></span>

<span data-ttu-id="64b9d-105">Se envía a una ventana cuando el cursor se mantiene sobre el área no cliente de la ventana durante el período de tiempo especificado en una llamada anterior a [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="64b9d-105">Posted to a window when the cursor hovers over the nonclient area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="64b9d-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="64b9d-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSEHOVER                 0x02A0
```



## <a name="parameters"></a><span data-ttu-id="64b9d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64b9d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64b9d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64b9d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64b9d-109">El valor de la prueba de posicionamiento devuelto por la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado de procesar el mensaje de [**\_ NCHITTEST de WM**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="64b9d-109">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="64b9d-110">Para obtener una lista de los valores de las pruebas de posicionamiento, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="64b9d-110">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="64b9d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64b9d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64b9d-112">Estructura de [**puntos**](/previous-versions//dd162808(v=vs.85)) que contiene las coordenadas x e y del cursor.</span><span class="sxs-lookup"><span data-stu-id="64b9d-112">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="64b9d-113">Las coordenadas son relativas a la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="64b9d-113">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64b9d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64b9d-114">Return value</span></span>

<span data-ttu-id="64b9d-115">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="64b9d-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="64b9d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64b9d-116">Remarks</span></span>

<span data-ttu-id="64b9d-117">El seguimiento de desplazamiento se detiene cuando se genera este mensaje.</span><span class="sxs-lookup"><span data-stu-id="64b9d-117">Hover tracking stops when this message is generated.</span></span> <span data-ttu-id="64b9d-118">La aplicación debe volver a llamar a [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) si requiere un seguimiento adicional del comportamiento de desplazamiento del mouse.</span><span class="sxs-lookup"><span data-stu-id="64b9d-118">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="64b9d-119">También puede usar las macros [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) y [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer los valores de las coordenadas x e y de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="64b9d-119">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="64b9d-120">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="64b9d-120">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="64b9d-121">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="64b9d-121">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="64b9d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64b9d-122">Requirements</span></span>



| <span data-ttu-id="64b9d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="64b9d-123">Requirement</span></span> | <span data-ttu-id="64b9d-124">Value</span><span class="sxs-lookup"><span data-stu-id="64b9d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64b9d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64b9d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="64b9d-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="64b9d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="64b9d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64b9d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="64b9d-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="64b9d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="64b9d-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64b9d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="64b9d-130"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64b9d-130"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64b9d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="64b9d-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="64b9d-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="64b9d-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="64b9d-133">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="64b9d-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="64b9d-134">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="64b9d-134">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="64b9d-135">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="64b9d-135">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="64b9d-136">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="64b9d-136">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="64b9d-137">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="64b9d-137">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="64b9d-138">**NCHITTEST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="64b9d-138">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="64b9d-139">**MOUSEHOVER de WM \_**</span><span class="sxs-lookup"><span data-stu-id="64b9d-139">**WM\_MOUSEHOVER**</span></span>](wm-mousehover.md)
</dt> <dt>

<span data-ttu-id="64b9d-140">**Vista**</span><span class="sxs-lookup"><span data-stu-id="64b9d-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="64b9d-141">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="64b9d-141">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="64b9d-142">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="64b9d-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="64b9d-143">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="64b9d-143">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="64b9d-144">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64b9d-144">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

