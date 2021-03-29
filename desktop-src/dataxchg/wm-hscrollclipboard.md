---
title: Mensaje de WM_HSCROLLCLIPBOARD (Winuser. h)
description: Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles.
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- Intercambio de datos de mensajes de WM_HSCROLLCLIPBOARD
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34ee33709601b483258ae0aec4873c47fa69a00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492196"
---
# <a name="wm_hscrollclipboard-message"></a><span data-ttu-id="46aa5-104">Mensaje de HSCROLLCLIPBOARD de WM \_</span><span class="sxs-lookup"><span data-stu-id="46aa5-104">WM\_HSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="46aa5-105">Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="46aa5-105">Sent to the clipboard owner by a clipboard viewer window.</span></span> <span data-ttu-id="46aa5-106">Esto sucede si el Portapapeles contiene datos con el formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) y se produce un evento en la barra de desplazamiento horizontal del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="46aa5-106">This occurs when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's horizontal scroll bar.</span></span> <span data-ttu-id="46aa5-107">El propietario debe desplazarse por la imagen del portapapeles y actualizar los valores de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="46aa5-107">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a><span data-ttu-id="46aa5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46aa5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46aa5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46aa5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46aa5-110">Identificador de la ventana del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="46aa5-110">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="46aa5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46aa5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46aa5-112">La palabra de orden inferior de *lParam* especifica un evento de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="46aa5-112">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="46aa5-113">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="46aa5-113">This parameter can be one of the following values.</span></span> <span data-ttu-id="46aa5-114">La palabra de orden superior de *lParam* especifica la posición actual del cuadro de desplazamiento si la palabra de orden inferior de *lParam* es **SB \_ THUMBPOSITION**; de lo contrario, no se utiliza la palabra de orden superior.</span><span class="sxs-lookup"><span data-stu-id="46aa5-114">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word is not used.</span></span>



| <span data-ttu-id="46aa5-115">Value</span><span class="sxs-lookup"><span data-stu-id="46aa5-115">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="46aa5-116">Significado</span><span class="sxs-lookup"><span data-stu-id="46aa5-116">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="46aa5-117"><dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="46aa5-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="46aa5-118">Fin de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="46aa5-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <span data-ttu-id="46aa5-119"><dt>**SB \_ IZQUIERDO**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="46aa5-119"><dt>**SB\_LEFT**</dt> <dt>6</dt></span></span> </dl>                            | <span data-ttu-id="46aa5-120">Desplácese hacia la parte superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="46aa5-120">Scroll to upper left.</span></span><br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <span data-ttu-id="46aa5-121"><dt>**SB \_ DERECHA**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="46aa5-121"><dt>**SB\_RIGHT**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="46aa5-122">Desplácese hacia abajo a la derecha.</span><span class="sxs-lookup"><span data-stu-id="46aa5-122">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <span data-ttu-id="46aa5-123"><dt>**SB \_ LINELEFT**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="46aa5-123"><dt>**SB\_LINELEFT**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="46aa5-124">Se desplaza una unidad hacia la izquierda.</span><span class="sxs-lookup"><span data-stu-id="46aa5-124">Scrolls left by one unit.</span></span><br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <span data-ttu-id="46aa5-125"><dt>**SB \_ LINERIGHT**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="46aa5-125"><dt>**SB\_LINERIGHT**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="46aa5-126">Se desplaza hacia la derecha una unidad.</span><span class="sxs-lookup"><span data-stu-id="46aa5-126">Scrolls right by one unit.</span></span><br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <span data-ttu-id="46aa5-127"><dt>**SB \_ PAGELEFT**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="46aa5-127"><dt>**SB\_PAGELEFT**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="46aa5-128">Se desplaza hacia la izquierda el ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="46aa5-128">Scrolls left by the width of the window.</span></span><br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <span data-ttu-id="46aa5-129"><dt>**SB \_ ANCLADA**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="46aa5-129"><dt>**SB\_PAGERIGHT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="46aa5-130">Se desplaza a la derecha el ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="46aa5-130">Scrolls right by the width of the window.</span></span><br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="46aa5-131"><dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="46aa5-131"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="46aa5-132">Desplácese hasta la posición absoluta.</span><span class="sxs-lookup"><span data-stu-id="46aa5-132">Scroll to absolute position.</span></span> <span data-ttu-id="46aa5-133">La posición actual se especifica mediante la palabra de orden superior.</span><span class="sxs-lookup"><span data-stu-id="46aa5-133">The current position is specified by the high-order word.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46aa5-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46aa5-134">Return value</span></span>

<span data-ttu-id="46aa5-135">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="46aa5-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="46aa5-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46aa5-136">Remarks</span></span>

<span data-ttu-id="46aa5-137">El propietario del portapapeles puede utilizar la función [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) para desplazar la imagen en la ventana del visor del portapapeles e invalidar la región adecuada.</span><span class="sxs-lookup"><span data-stu-id="46aa5-137">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="46aa5-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46aa5-138">Requirements</span></span>



| <span data-ttu-id="46aa5-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="46aa5-139">Requirement</span></span> | <span data-ttu-id="46aa5-140">Value</span><span class="sxs-lookup"><span data-stu-id="46aa5-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46aa5-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46aa5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="46aa5-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="46aa5-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="46aa5-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46aa5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="46aa5-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="46aa5-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="46aa5-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46aa5-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="46aa5-146"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46aa5-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46aa5-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="46aa5-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="46aa5-148">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="46aa5-148">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="46aa5-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="46aa5-149">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="46aa5-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="46aa5-150">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="46aa5-151">**Vista**</span><span class="sxs-lookup"><span data-stu-id="46aa5-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="46aa5-152">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="46aa5-152">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="46aa5-153">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="46aa5-153">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="46aa5-154">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="46aa5-154">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

