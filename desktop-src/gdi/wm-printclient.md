---
description: El mensaje de PRINTCLIENT de WM \_ se envía a una ventana para solicitar que dibuje su área de cliente en el contexto de dispositivo especificado, normalmente en un contexto de dispositivo de impresora.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: Mensaje de WM_PRINTCLIENT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52aca68695964a35ab9a2c4e309cd71c2e9f7eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985799"
---
# <a name="wm_printclient-message"></a><span data-ttu-id="c7ab6-103">Mensaje de PRINTCLIENT de WM \_</span><span class="sxs-lookup"><span data-stu-id="c7ab6-103">WM\_PRINTCLIENT message</span></span>

<span data-ttu-id="c7ab6-104">El mensaje de **\_ PRINTCLIENT de WM** se envía a una ventana para solicitar que dibuje su área de cliente en el contexto de dispositivo especificado, normalmente en un contexto de dispositivo de impresora.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-104">The **WM\_PRINTCLIENT** message is sent to a window to request that it draw its client area in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="c7ab6-105">A diferencia de la [**\_ impresión de WM**](wm-print.md), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)no procesa **\_ PRINTCLIENT** .</span><span class="sxs-lookup"><span data-stu-id="c7ab6-105">Unlike [**WM\_PRINT**](wm-print.md), **WM\_PRINTCLIENT** is not processed by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="c7ab6-106">Una ventana debe procesar el mensaje de **\_ PRINTCLIENT de WM** a través de una función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) definida por la aplicación para que se use correctamente.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-106">A window should process the **WM\_PRINTCLIENT** message through an application-defined [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function for it to be used properly.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="c7ab6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7ab6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7ab6-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7ab6-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7ab6-109">Identificador del contexto de dispositivo en el que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-109">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="c7ab6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7ab6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7ab6-111">Opciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-111">The drawing options.</span></span> <span data-ttu-id="c7ab6-112">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="c7ab6-113">Value</span><span class="sxs-lookup"><span data-stu-id="c7ab6-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="c7ab6-114">Significado</span><span class="sxs-lookup"><span data-stu-id="c7ab6-114">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="c7ab6-115"><dt>**\_CHECKVISIBLE PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="c7ab6-115"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="c7ab6-116">Dibuja la ventana solo si está visible.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-116">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="c7ab6-117"><dt>**\_elementos secundarios PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="c7ab6-117"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="c7ab6-118">Dibuja todas las ventanas secundarias visibles.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-118">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="c7ab6-119"><dt>**\_cliente PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="c7ab6-119"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="c7ab6-120">Dibuja el área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-120">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="c7ab6-121"><dt>**\_ERASEBKGND PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="c7ab6-121"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="c7ab6-122">Borra el fondo antes de dibujar la ventana.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-122">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="c7ab6-123"><dt>**no \_ cliente PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="c7ab6-123"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="c7ab6-124">Dibuja el área no cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-124">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="c7ab6-125"><dt>**propiedad de PRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c7ab6-125"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="c7ab6-126">Dibuja todas las ventanas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-126">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7ab6-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7ab6-127">Remarks</span></span>

<span data-ttu-id="c7ab6-128">Una ventana puede procesar este mensaje de la misma manera que en [**WM \_ Paint**](./wm-paint.md), salvo que no es necesario llamar a [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) y [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) (se proporciona un contexto de dispositivo) y la ventana debe dibujar todo el área cliente en lugar de simplemente la región no válida.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-128">A window can process this message in much the same manner as [**WM\_PAINT**](./wm-paint.md), except that [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) need not be called (a device context is provided), and the window should draw its entire client area rather than just the invalid region.</span></span>

<span data-ttu-id="c7ab6-129">Las ventanas que se pueden usar en cualquier parte del sistema, como los controles, deben procesar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-129">Windows that can be used anywhere in the system, such as controls, should process this message.</span></span> <span data-ttu-id="c7ab6-130">Probablemente merece la pena para otras ventanas procesar este mensaje también porque es relativamente fácil de implementar.</span><span class="sxs-lookup"><span data-stu-id="c7ab6-130">It is probably worthwhile for other windows to process this message as well because it is relatively easy to implement.</span></span>

<span data-ttu-id="c7ab6-131">La función [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) requiere que la ventana que se está animando implemente el mensaje de **\_ PRINTCLIENT de WM** .</span><span class="sxs-lookup"><span data-stu-id="c7ab6-131">The [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) function requires that the window being animated implements the **WM\_PRINTCLIENT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7ab6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7ab6-132">Requirements</span></span>



| <span data-ttu-id="c7ab6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7ab6-133">Requirement</span></span> | <span data-ttu-id="c7ab6-134">Value</span><span class="sxs-lookup"><span data-stu-id="c7ab6-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ab6-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7ab6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c7ab6-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c7ab6-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c7ab6-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7ab6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c7ab6-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c7ab6-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7ab6-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7ab6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7ab6-140"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7ab6-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7ab6-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7ab6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7ab6-142">Información general sobre pintura y dibujo</span><span class="sxs-lookup"><span data-stu-id="c7ab6-142">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="c7ab6-143">Pintar y dibujar mensajes</span><span class="sxs-lookup"><span data-stu-id="c7ab6-143">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="c7ab6-144">**AnimateWindow**</span><span class="sxs-lookup"><span data-stu-id="c7ab6-144">**AnimateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[<span data-ttu-id="c7ab6-145">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="c7ab6-145">**BeginPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="c7ab6-146">**EndPaint**</span><span class="sxs-lookup"><span data-stu-id="c7ab6-146">**EndPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[<span data-ttu-id="c7ab6-147">**pintura de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c7ab6-147">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
