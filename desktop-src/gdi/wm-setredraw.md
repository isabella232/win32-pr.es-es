---
description: Una aplicación envía el mensaje de SETREDRAW de WM \_ a una ventana para permitir que se vuelvan a dibujar los cambios en esa ventana o para evitar que se vuelvan a dibujar los cambios en esa ventana.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Mensaje de WM_SETREDRAW (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184401e70c8233b03c57db4f8a01bbd6a42e1a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277845"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="f72b2-103">Mensaje de SETREDRAW de WM \_</span><span class="sxs-lookup"><span data-stu-id="f72b2-103">WM\_SETREDRAW message</span></span>

<span data-ttu-id="f72b2-104">Una aplicación envía el mensaje de **\_ SETREDRAW de WM** a una ventana para permitir que se vuelvan a dibujar los cambios en esa ventana o para evitar que se vuelvan a dibujar los cambios en esa ventana.</span><span class="sxs-lookup"><span data-stu-id="f72b2-104">An application sends the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="f72b2-105">Para enviar este mensaje, llame a la función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="f72b2-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND) hWnd,              
  WM_SETREDRAW,             
  (WPARAM) wParam,          
  (LPARAM) lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="f72b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f72b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f72b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f72b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f72b2-108">Estado de redibujo.</span><span class="sxs-lookup"><span data-stu-id="f72b2-108">The redraw state.</span></span> <span data-ttu-id="f72b2-109">Si este parámetro es **true**, el contenido se puede volver a dibujar después de un cambio.</span><span class="sxs-lookup"><span data-stu-id="f72b2-109">If this parameter is **TRUE**, the content can be redrawn after a change.</span></span> <span data-ttu-id="f72b2-110">Si este parámetro es **false**, no se puede volver a dibujar el contenido después de un cambio.</span><span class="sxs-lookup"><span data-stu-id="f72b2-110">If this parameter is **FALSE**, the content cannot be redrawn after a change.</span></span>

</dd> <dt>

<span data-ttu-id="f72b2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f72b2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f72b2-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f72b2-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f72b2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f72b2-113">Return value</span></span>

<span data-ttu-id="f72b2-114">Una aplicación devuelve cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f72b2-114">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="f72b2-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f72b2-115">Remarks</span></span>

<span data-ttu-id="f72b2-116">Este mensaje puede ser útil si una aplicación debe agregar varios elementos a un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="f72b2-116">This message can be useful if an application must add several items to a list box.</span></span> <span data-ttu-id="f72b2-117">La aplicación puede llamar a este mensaje con *wParam* establecido en **false**, agregar los elementos y, a continuación, volver a llamar al mensaje con *wParam* establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="f72b2-117">The application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="f72b2-118">Por último, la aplicación puede llamar a [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **null**, **null**, RDW \_ Erase \| RDW \_ Frame \| RDW \_ Invalidate \| RDW \_ ALLCHILDREN) para hacer que el cuadro de lista se vuelva a dibujar.</span><span class="sxs-lookup"><span data-stu-id="f72b2-118">Finally, the application can call [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!Note]  
> <span data-ttu-id="f72b2-119">[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con las marcas especificadas se usa en lugar de [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) porque el primero es necesario para algunos controles que tienen un área no cliente por su cuenta, o tienen estilos de ventana que provocan que se les proporcione un área no cliente (como **WS \_ THICKFRAME**, **WS \_ Border** o **WS \_ ex \_ CLIENTEDGE**).</span><span class="sxs-lookup"><span data-stu-id="f72b2-119">[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) with the specified flags is used instead of [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) because the former is necessary for some controls that have nonclient area on their own, or have window styles that cause them to be given a nonclient area (such as **WS\_THICKFRAME**, **WS\_BORDER**, or **WS\_EX\_CLIENTEDGE**).</span></span> <span data-ttu-id="f72b2-120">Si el control no tiene un área de cliente, **RedrawWindow** con estas marcas solo realizará la misma invalidación que **InvalidateRect** .</span><span class="sxs-lookup"><span data-stu-id="f72b2-120">If the control does not have a nonclient area, **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

 

<span data-ttu-id="f72b2-121">Si la aplicación envía el mensaje de **\_ SETREDRAW de WM** a una ventana oculta, la ventana se vuelve visible (es decir, el sistema operativo agrega el estilo **\_ visible de WS** a la ventana).</span><span class="sxs-lookup"><span data-stu-id="f72b2-121">If the application sends the **WM\_SETREDRAW** message to a hidden window, the window becomes visible (that is, the operating system adds the **WS\_VISIBLE** style to the window).</span></span>

## <a name="requirements"></a><span data-ttu-id="f72b2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f72b2-122">Requirements</span></span>



| <span data-ttu-id="f72b2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f72b2-123">Requirement</span></span> | <span data-ttu-id="f72b2-124">Value</span><span class="sxs-lookup"><span data-stu-id="f72b2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f72b2-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f72b2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f72b2-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f72b2-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f72b2-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f72b2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f72b2-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f72b2-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f72b2-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f72b2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f72b2-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f72b2-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f72b2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f72b2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72b2-132">Información general sobre pintura y dibujo</span><span class="sxs-lookup"><span data-stu-id="f72b2-132">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="f72b2-133">Pintar y dibujar mensajes</span><span class="sxs-lookup"><span data-stu-id="f72b2-133">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="f72b2-134">**RedrawWindow**</span><span class="sxs-lookup"><span data-stu-id="f72b2-134">**RedrawWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> </dl>

 

 
