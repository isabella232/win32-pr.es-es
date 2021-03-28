---
description: El mensaje de NCPAINT de WM \_ se envía a una ventana cuando se debe pintar su marco.
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: Mensaje de WM_NCPAINT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6c2e211f3dc1602821b0197d295f940606c262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908934"
---
# <a name="wm_ncpaint-message"></a><span data-ttu-id="200b4-103">Mensaje de NCPAINT de WM \_</span><span class="sxs-lookup"><span data-stu-id="200b4-103">WM\_NCPAINT message</span></span>

<span data-ttu-id="200b4-104">El mensaje de **\_ NCPAINT de WM** se envía a una ventana cuando se debe pintar su marco.</span><span class="sxs-lookup"><span data-stu-id="200b4-104">The **WM\_NCPAINT** message is sent to a window when its frame must be painted.</span></span>

<span data-ttu-id="200b4-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="200b4-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="200b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="200b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="200b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="200b4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="200b4-108">Identificador de la región de actualización de la ventana.</span><span class="sxs-lookup"><span data-stu-id="200b4-108">A handle to the update region of the window.</span></span> <span data-ttu-id="200b4-109">La región de actualización se recorta en el marco de la ventana.</span><span class="sxs-lookup"><span data-stu-id="200b4-109">The update region is clipped to the window frame.</span></span>

</dd> <dt>

<span data-ttu-id="200b4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="200b4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="200b4-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="200b4-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="200b4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="200b4-112">Return value</span></span>

<span data-ttu-id="200b4-113">Una aplicación devuelve cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="200b4-113">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="200b4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="200b4-114">Remarks</span></span>

<span data-ttu-id="200b4-115">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pinta el marco de la ventana.</span><span class="sxs-lookup"><span data-stu-id="200b4-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function paints the window frame.</span></span>

<span data-ttu-id="200b4-116">Una aplicación puede interceptar el mensaje de **\_ NCPAINT de WM** y pintar su propio marco de ventana personalizado.</span><span class="sxs-lookup"><span data-stu-id="200b4-116">An application can intercept the **WM\_NCPAINT** message and paint its own custom window frame.</span></span> <span data-ttu-id="200b4-117">La región de recorte de una ventana siempre es rectangular, incluso si se modifica la forma del marco.</span><span class="sxs-lookup"><span data-stu-id="200b4-117">The clipping region for a window is always rectangular, even if the shape of the frame is altered.</span></span>

<span data-ttu-id="200b4-118">El valor de *wParam* se puede pasar a [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) como en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="200b4-118">The *wParam* value can be passed to [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) as in the following example.</span></span>


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



## <a name="requirements"></a><span data-ttu-id="200b4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="200b4-119">Requirements</span></span>



| <span data-ttu-id="200b4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="200b4-120">Requirement</span></span> | <span data-ttu-id="200b4-121">Value</span><span class="sxs-lookup"><span data-stu-id="200b4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="200b4-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="200b4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="200b4-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="200b4-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="200b4-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="200b4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="200b4-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="200b4-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="200b4-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="200b4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="200b4-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="200b4-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="200b4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="200b4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="200b4-129">Información general sobre pintura y dibujo</span><span class="sxs-lookup"><span data-stu-id="200b4-129">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="200b4-130">Pintar y dibujar mensajes</span><span class="sxs-lookup"><span data-stu-id="200b4-130">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="200b4-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="200b4-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="200b4-132">**GetWindowDC**</span><span class="sxs-lookup"><span data-stu-id="200b4-132">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="200b4-133">**pintura de WM \_**</span><span class="sxs-lookup"><span data-stu-id="200b4-133">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> <dt>

[<span data-ttu-id="200b4-134">**GetDCEx**</span><span class="sxs-lookup"><span data-stu-id="200b4-134">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 
