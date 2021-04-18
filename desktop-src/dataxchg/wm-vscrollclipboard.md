---
title: Mensaje de WM_VSCROLLCLIPBOARD (Winuser. h)
description: Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles cuando el Portapapeles contiene datos con el \_ formato CF OWNERDISPLAY y se produce un evento en la barra de desplazamiento vertical del visor del portapapeles.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- Intercambio de datos de mensajes de WM_VSCROLLCLIPBOARD
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a9e80aa342065ee88c8e1d7aa44c1fd598e411
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491068"
---
# <a name="wm_vscrollclipboard-message"></a><span data-ttu-id="378d2-104">Mensaje de VSCROLLCLIPBOARD de WM \_</span><span class="sxs-lookup"><span data-stu-id="378d2-104">WM\_VSCROLLCLIPBOARD message</span></span>

<span data-ttu-id="378d2-105">Se envía al propietario del portapapeles mediante una ventana del visor del portapapeles cuando el Portapapeles contiene datos con el formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) y se produce un evento en la barra de desplazamiento vertical del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="378d2-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and an event occurs in the clipboard viewer's vertical scroll bar.</span></span> <span data-ttu-id="378d2-106">El propietario debe desplazarse por la imagen del portapapeles y actualizar los valores de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="378d2-106">The owner should scroll the clipboard image and update the scroll bar values.</span></span>


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a><span data-ttu-id="378d2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="378d2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="378d2-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="378d2-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="378d2-109">Identificador de la ventana del visor del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="378d2-109">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="378d2-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="378d2-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="378d2-111">La palabra de orden inferior de *lParam* especifica un evento de barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="378d2-111">The low-order word of *lParam* specifies a scroll bar event.</span></span> <span data-ttu-id="378d2-112">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="378d2-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="378d2-113">Valor</span><span class="sxs-lookup"><span data-stu-id="378d2-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="378d2-114">Significado</span><span class="sxs-lookup"><span data-stu-id="378d2-114">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <span data-ttu-id="378d2-115"><dt>**SB \_**</dt> <dt>7</dt> inferiores</span><span class="sxs-lookup"><span data-stu-id="378d2-115"><dt>**SB\_BOTTOM**</dt> <dt>7</dt></span></span> </dl>                      | <span data-ttu-id="378d2-116">Desplácese hacia abajo a la derecha.</span><span class="sxs-lookup"><span data-stu-id="378d2-116">Scroll to lower right.</span></span><br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="378d2-117"><dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="378d2-117"><dt>**SB\_ENDSCROLL**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="378d2-118">Fin de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="378d2-118">End scroll.</span></span><br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="378d2-119"><dt>**SB \_ LINEDOWN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="378d2-119"><dt>**SB\_LINEDOWN**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="378d2-120">Desplazarse una línea hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="378d2-120">Scroll one line down.</span></span><br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="378d2-121"><dt>**SB \_ LÍNEA**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="378d2-121"><dt>**SB\_LINEUP**</dt> <dt>0</dt></span></span> </dl>                      | <span data-ttu-id="378d2-122">Desplazarse una línea hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="378d2-122">Scroll one line up.</span></span><br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="378d2-123"><dt>**SB \_ AvPág**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="378d2-123"><dt>**SB\_PAGEDOWN**</dt> <dt>3</dt></span></span> </dl>                | <span data-ttu-id="378d2-124">Desplazarse una página hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="378d2-124">Scroll one page down.</span></span><br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="378d2-125"><dt>**SB \_ RePág**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="378d2-125"><dt>**SB\_PAGEUP**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="378d2-126">Desplazarse una página hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="378d2-126">Scroll one page up.</span></span><br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="378d2-127"><dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="378d2-127"><dt>**SB\_THUMBPOSITION**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="378d2-128">Desplácese hasta la posición absoluta.</span><span class="sxs-lookup"><span data-stu-id="378d2-128">Scroll to absolute position.</span></span> <span data-ttu-id="378d2-129">La posición actual se especifica mediante la palabra de orden superior.</span><span class="sxs-lookup"><span data-stu-id="378d2-129">The current position is specified by the high-order word.</span></span><br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <span data-ttu-id="378d2-130"><dt>**SB \_ PRINCIPALES**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="378d2-130"><dt>**SB\_TOP**</dt> <dt>6</dt></span></span> </dl>                               | <span data-ttu-id="378d2-131">Desplácese hacia la parte superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="378d2-131">Scroll to upper left.</span></span><br/>                                                                  |



 

<span data-ttu-id="378d2-132">La palabra de orden superior de *lParam* especifica la posición actual del cuadro de desplazamiento si la palabra de orden inferior de *lParam* es **SB \_ THUMBPOSITION**; de lo contrario, no se utiliza la palabra de orden superior de *lParam* .</span><span class="sxs-lookup"><span data-stu-id="378d2-132">The high-order word of *lParam* specifies the current position of the scroll box if the low-order word of *lParam* is **SB\_THUMBPOSITION**; otherwise, the high-order word of *lParam* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="378d2-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="378d2-133">Return value</span></span>

<span data-ttu-id="378d2-134">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="378d2-134">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="378d2-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="378d2-135">Remarks</span></span>

<span data-ttu-id="378d2-136">El propietario del portapapeles puede utilizar la función [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) para desplazar la imagen en la ventana del visor del portapapeles e invalidar la región adecuada.</span><span class="sxs-lookup"><span data-stu-id="378d2-136">The clipboard owner can use the [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) function to scroll the image in the clipboard viewer window and invalidate the appropriate region.</span></span>

## <a name="requirements"></a><span data-ttu-id="378d2-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="378d2-137">Requirements</span></span>



| <span data-ttu-id="378d2-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="378d2-138">Requirement</span></span> | <span data-ttu-id="378d2-139">Value</span><span class="sxs-lookup"><span data-stu-id="378d2-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="378d2-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="378d2-140">Minimum supported client</span></span><br/> | <span data-ttu-id="378d2-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="378d2-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="378d2-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="378d2-142">Minimum supported server</span></span><br/> | <span data-ttu-id="378d2-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="378d2-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="378d2-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="378d2-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="378d2-145"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="378d2-145"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="378d2-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="378d2-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="378d2-147">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="378d2-147">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="378d2-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="378d2-148">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="378d2-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="378d2-149">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="378d2-150">**Vista**</span><span class="sxs-lookup"><span data-stu-id="378d2-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="378d2-151">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="378d2-151">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="378d2-152">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="378d2-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="378d2-153">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="378d2-153">[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

