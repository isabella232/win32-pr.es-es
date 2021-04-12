---
description: Se envía cuando se debe borrar el fondo de la ventana (por ejemplo, cuando se cambia el tamaño de una ventana). El mensaje se envía para preparar una parte invalidada de una ventana para su dibujo.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: Mensaje de WM_ERASEBKGND (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277765"
---
# <a name="wm_erasebkgnd-message"></a><span data-ttu-id="42755-104">Mensaje de ERASEBKGND de WM \_</span><span class="sxs-lookup"><span data-stu-id="42755-104">WM\_ERASEBKGND message</span></span>

<span data-ttu-id="42755-105">Se envía cuando se debe borrar el fondo de la ventana (por ejemplo, cuando se cambia el tamaño de una ventana).</span><span class="sxs-lookup"><span data-stu-id="42755-105">Sent when the window background must be erased (for example, when a window is resized).</span></span> <span data-ttu-id="42755-106">El mensaje se envía para preparar una parte invalidada de una ventana para su dibujo.</span><span class="sxs-lookup"><span data-stu-id="42755-106">The message is sent to prepare an invalidated portion of a window for painting.</span></span>


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a><span data-ttu-id="42755-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42755-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42755-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42755-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42755-109">Identificador del contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42755-109">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="42755-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42755-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42755-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42755-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42755-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42755-112">Return value</span></span>

<span data-ttu-id="42755-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="42755-113">Type: **LRESULT**</span></span>

<span data-ttu-id="42755-114">Una aplicación debe devolver un valor distinto de cero si borra el fondo; de lo contrario, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="42755-114">An application should return nonzero if it erases the background; otherwise, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="42755-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42755-115">Remarks</span></span>

<span data-ttu-id="42755-116">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) borra el fondo mediante el pincel de fondo de clase especificado por el miembro **hbrBackground** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) .</span><span class="sxs-lookup"><span data-stu-id="42755-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function erases the background by using the class background brush specified by the **hbrBackground** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure.</span></span> <span data-ttu-id="42755-117">Si **hbrBackground** es **null**, la aplicación debe procesar el mensaje de **\_ ERASEBKGND de WM** y borrar el fondo.</span><span class="sxs-lookup"><span data-stu-id="42755-117">If **hbrBackground** is **NULL**, the application should process the **WM\_ERASEBKGND** message and erase the background.</span></span>

<span data-ttu-id="42755-118">Una aplicación debe devolver un valor distinto de cero en respuesta a **WM \_ ERASEBKGND** si procesa el mensaje y borra el fondo; esto indica que no es necesario borrar más.</span><span class="sxs-lookup"><span data-stu-id="42755-118">An application should return nonzero in response to **WM\_ERASEBKGND** if it processes the message and erases the background; this indicates that no further erasing is required.</span></span> <span data-ttu-id="42755-119">Si la aplicación devuelve cero, la ventana permanecerá marcada para borrarse.</span><span class="sxs-lookup"><span data-stu-id="42755-119">If the application returns zero, the window will remain marked for erasing.</span></span> <span data-ttu-id="42755-120">(Normalmente, esto indica que el miembro **fErase** de la estructura [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) será **true**).</span><span class="sxs-lookup"><span data-stu-id="42755-120">(Typically, this indicates that the **fErase** member of the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure will be **TRUE**.)</span></span>

## <a name="requirements"></a><span data-ttu-id="42755-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42755-121">Requirements</span></span>



| <span data-ttu-id="42755-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="42755-122">Requirement</span></span> | <span data-ttu-id="42755-123">Value</span><span class="sxs-lookup"><span data-stu-id="42755-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42755-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42755-124">Minimum supported client</span></span><br/> | <span data-ttu-id="42755-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="42755-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="42755-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42755-126">Minimum supported server</span></span><br/> | <span data-ttu-id="42755-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="42755-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42755-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42755-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="42755-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42755-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42755-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="42755-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="42755-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="42755-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="42755-132">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="42755-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="42755-133">**WNDCLASS**</span><span class="sxs-lookup"><span data-stu-id="42755-133">**WNDCLASS**</span></span>](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

<span data-ttu-id="42755-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="42755-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="42755-135">Iconos</span><span class="sxs-lookup"><span data-stu-id="42755-135">Icons</span></span>](../menurc/icons.md)
</dt> <dt>

<span data-ttu-id="42755-136">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="42755-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="42755-137">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="42755-137">**BeginPaint**</span></span>](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="42755-138">**PAINTSTRUCT (**</span><span class="sxs-lookup"><span data-stu-id="42755-138">**PAINTSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
