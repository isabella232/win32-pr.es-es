---
description: Envíe el mensaje **WM_SETREDRAW** a una ventana para permitir que se vuelvan a dibujar los cambios de esa ventana o para evitar que se vuelvan a dibujar los cambios en esa ventana.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: WM_SETREDRAW mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1232833fc4465e2341541a0036af47fdd3b53393
ms.sourcegitcommit: e5d6fb49928cc8cea4ec77dce03b740d40076348
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/10/2021
ms.locfileid: "113593461"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="025ac-103">WM_SETREDRAW mensaje</span><span class="sxs-lookup"><span data-stu-id="025ac-103">WM_SETREDRAW message</span></span>

<span data-ttu-id="025ac-104">El mensaje **WM \_ SETREDRAW** se envía a una ventana para permitir que se vuelvan a dibujar los cambios de esa ventana o para evitar que se vuelvan a dibujar los cambios en esa ventana.</span><span class="sxs-lookup"><span data-stu-id="025ac-104">You send the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn, or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="025ac-105">Para enviar este mensaje, llame a la [**función SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="025ac-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>

```C++
SendMessage(
  (HWND) hWnd,
  WM_SETREDRAW,
  (WPARAM) wParam,
  (LPARAM) lParam
);
```

## <a name="parameters"></a><span data-ttu-id="025ac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="025ac-106">Parameters</span></span>

`wParam`

<span data-ttu-id="025ac-107">Estado de volver a dibujar.</span><span class="sxs-lookup"><span data-stu-id="025ac-107">The redraw state.</span></span> <span data-ttu-id="025ac-108">Si este parámetro es **TRUE,** el contenido se puede volver a dibujar después de un cambio.</span><span class="sxs-lookup"><span data-stu-id="025ac-108">If this parameter is **TRUE**, then the content can be redrawn after a change.</span></span> <span data-ttu-id="025ac-109">Si este parámetro es **FALSE,** no se puede volver a dibujar el contenido después de un cambio.</span><span class="sxs-lookup"><span data-stu-id="025ac-109">If this parameter is **FALSE**, then the content can't be redrawn after a change.</span></span>

`lParam`

<span data-ttu-id="025ac-110">Este parámetro no se usa.</span><span class="sxs-lookup"><span data-stu-id="025ac-110">This parameter isn't used.</span></span>

## <a name="return-value"></a><span data-ttu-id="025ac-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="025ac-111">Return value</span></span>

<span data-ttu-id="025ac-112">La aplicación debe devolver 0 si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="025ac-112">Your application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="025ac-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="025ac-113">Remarks</span></span>

<span data-ttu-id="025ac-114">Este mensaje puede ser útil si la aplicación debe agregar varios elementos a un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="025ac-114">This message can be useful if your application must add several items to a list box.</span></span> <span data-ttu-id="025ac-115">La aplicación puede llamar a este mensaje con *wParam* establecido en **FALSE,** agregar los elementos y, a continuación, volver a llamar al mensaje con *wParam* establecido en **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="025ac-115">Your application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="025ac-116">Por último, la aplicación puede llamar a [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, \_ RDW ERASE \| RDW \_ FRAME \| RDW \_ INVALIDATE \| RDW \_ ALLCHILDREN) para hacer que se vuelva a dibujar el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="025ac-116">Finally, your application can call [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!NOTE] 
> <span data-ttu-id="025ac-117">Debe usar [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) con las marcas especificadas, en lugar de [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), porque la primera es necesaria para algunos controles que tienen su propio área no cliente o tienen estilos de ventana que hacen que se les de un área no cliente (como **WS_THICKFRAME**, **WS_BORDER** o **WS_EX_CLIENTEDGE**).</span><span class="sxs-lookup"><span data-stu-id="025ac-117">You should use [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) with the specified flags, instead of [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), because the former is necessary for some controls that have nonclient area of their own, or have window styles that cause them to be given a nonclient area (such as **WS_THICKFRAME**, **WS_BORDER**, or **WS_EX_CLIENTEDGE**).</span></span> <span data-ttu-id="025ac-118">Si el control no tiene un área no cliente, **RedrawWindow** con estas marcas solo hará tanta invalidación como **Lo haría InvalidateRect.**</span><span class="sxs-lookup"><span data-stu-id="025ac-118">If the control does not have a nonclient area, then **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

<span data-ttu-id="025ac-119">Al pasar **un WM_SETREDRAW** a la función **DefWindowProc** se quita el estilo **WS_VISIBLE** de la ventana cuando *wParam* está establecido en **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="025ac-119">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function removes the **WS_VISIBLE** style from the window when *wParam* is set to **FALSE**.</span></span> <span data-ttu-id="025ac-120">Aunque el contenido de la ventana permanece visible en la pantalla, la función [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) devuelve **FALSE** cuando se llama a en una ventana en este estado.</span><span class="sxs-lookup"><span data-stu-id="025ac-120">Although the window content remains visible on screen, the [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) function returns **FALSE** when called on a window in this state.</span></span> 

<span data-ttu-id="025ac-121">Al pasar **un WM_SETREDRAW** a la función **DefWindowProc** se agrega el estilo **WS_VISIBLE** a la ventana, si no se establece, cuando *wParam* se establece en **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="025ac-121">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function adds the **WS_VISIBLE** style to the window, if not set, when *wParam* is set to **TRUE**.</span></span> <span data-ttu-id="025ac-122">Si la aplicación envía el **mensaje WM_SETREDRAW** con *wParam* establecido en **TRUE** en una ventana oculta, la ventana se vuelve visible.</span><span class="sxs-lookup"><span data-stu-id="025ac-122">If your application sends the **WM_SETREDRAW** message with *wParam* set to **TRUE** to a hidden window, then the window becomes visible.</span></span> 

<span data-ttu-id="025ac-123">**Windows 10 y versiones posteriores; Windows Server 2016 y versiones posteriores.**</span><span class="sxs-lookup"><span data-stu-id="025ac-123">**Windows 10 and later; Windows Server 2016 and later**.</span></span> <span data-ttu-id="025ac-124">El sistema establece una propiedad denominada *SysSetRedraw* en una ventana cuyo procedimiento de ventana **pasa** WM_SETREDRAW mensajes a **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="025ac-124">The system sets a property named *SysSetRedraw* on a window whose window procedure passes **WM_SETREDRAW** messages to **DefWindowProc**.</span></span> <span data-ttu-id="025ac-125">Puede usar la [**función GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) para obtener el valor de propiedad cuando esté disponible.</span><span class="sxs-lookup"><span data-stu-id="025ac-125">You can use the [**GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) function to get the property value when it's available.</span></span> <span data-ttu-id="025ac-126">**GetProp** devuelve un valor distinto de cero cuando se deshabilita volver a dibujar.</span><span class="sxs-lookup"><span data-stu-id="025ac-126">**GetProp** returns a non-zero value when redraw is disabled.</span></span> <span data-ttu-id="025ac-127">**GetProp** devolverá cero cuando se habilite volver a dibujar o cuando la propiedad de ventana no exista.</span><span class="sxs-lookup"><span data-stu-id="025ac-127">**GetProp** will return zero when redraw is enabled, or when the window property doesn't exist.</span></span> 

## <a name="requirements"></a><span data-ttu-id="025ac-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="025ac-128">Requirements</span></span>

| <span data-ttu-id="025ac-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="025ac-129">Requirement</span></span> | <span data-ttu-id="025ac-130">Value</span><span class="sxs-lookup"><span data-stu-id="025ac-130">Value</span></span> |
|-|-|
| <span data-ttu-id="025ac-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="025ac-131">Minimum supported client</span></span> | <span data-ttu-id="025ac-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="025ac-132">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="025ac-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="025ac-133">Minimum supported server</span></span> | <span data-ttu-id="025ac-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="025ac-134">Windows 2000 Server \[desktop apps only\]</span></span> |
| <span data-ttu-id="025ac-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="025ac-135">Header</span></span> | <dl><span data-ttu-id="025ac-136"><dt>Winuser.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="025ac-136"><dt>Winuser.h (include Windows.h)</dt></span></span></dl> |

## <a name="see-also"></a><span data-ttu-id="025ac-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="025ac-137">See also</span></span>

* [<span data-ttu-id="025ac-138">Información general sobre dibujo y dibujo</span><span class="sxs-lookup"><span data-stu-id="025ac-138">Painting and drawing overview</span></span>](painting-and-drawing.md)
* [<span data-ttu-id="025ac-139">Pintar y dibujar mensajes</span><span class="sxs-lookup"><span data-stu-id="025ac-139">Painting and drawing messages</span></span>](painting-and-drawing-messages.md)
* [<span data-ttu-id="025ac-140">Volver a dibujarWindow</span><span class="sxs-lookup"><span data-stu-id="025ac-140">RedrawWindow</span></span>](/windows/win32/api/Winuser/nf-winuser-redrawwindow)
