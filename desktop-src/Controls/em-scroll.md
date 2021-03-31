---
title: Mensaje de EM_SCROLL (Winuser. h)
description: Desplaza el texto verticalmente en un control de edición multilínea. Este mensaje es equivalente a enviar un mensaje de WM \_ VSCROLL al control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- EM_SCROLL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eb185fb14ef866ab0e7ea8c8064445193347d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151148"
---
# <a name="em_scroll-message"></a><span data-ttu-id="d588f-106">\_Mensaje de desplazamiento em</span><span class="sxs-lookup"><span data-stu-id="d588f-106">EM\_SCROLL message</span></span>

<span data-ttu-id="d588f-107">Desplaza el texto verticalmente en un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="d588f-107">Scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="d588f-108">Este mensaje es equivalente a enviar un mensaje de [**WM \_ VSCROLL**](wm-vscroll.md) al control de edición.</span><span class="sxs-lookup"><span data-stu-id="d588f-108">This message is equivalent to sending a [**WM\_VSCROLL**](wm-vscroll.md) message to the edit control.</span></span> <span data-ttu-id="d588f-109">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d588f-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d588f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d588f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d588f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d588f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d588f-112">Acción que va a tomar la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d588f-112">The action the scroll bar is to take.</span></span> <span data-ttu-id="d588f-113">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d588f-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d588f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d588f-114">Value</span></span>                                                                                                                                                   | <span data-ttu-id="d588f-115">Significado</span><span class="sxs-lookup"><span data-stu-id="d588f-115">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="d588f-116"><dt>**SB \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="d588f-116"><dt>**SB\_LINEDOWN**</dt></span></span> </dl> | <span data-ttu-id="d588f-117">Se desplaza hacia abajo una línea.</span><span class="sxs-lookup"><span data-stu-id="d588f-117">Scrolls down one line.</span></span><br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="d588f-118"><dt>**\_línea SB**</dt></span><span class="sxs-lookup"><span data-stu-id="d588f-118"><dt>**SB\_LINEUP**</dt></span></span> </dl>       | <span data-ttu-id="d588f-119">Se desplaza hacia arriba una línea.</span><span class="sxs-lookup"><span data-stu-id="d588f-119">Scrolls up one line.</span></span><br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="d588f-120"><dt>**reavpág SB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d588f-120"><dt>**SB\_PAGEDOWN**</dt></span></span> </dl> | <span data-ttu-id="d588f-121">Se desplaza hacia abajo una página.</span><span class="sxs-lookup"><span data-stu-id="d588f-121">Scrolls down one page.</span></span><br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="d588f-122"><dt>**\_Re Pág de SB**</dt></span><span class="sxs-lookup"><span data-stu-id="d588f-122"><dt>**SB\_PAGEUP**</dt></span></span> </dl>       | <span data-ttu-id="d588f-123">Desplaza hacia arriba una página.</span><span class="sxs-lookup"><span data-stu-id="d588f-123">Scrolls up one page.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="d588f-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d588f-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d588f-125">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d588f-125">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d588f-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d588f-126">Return value</span></span>

<span data-ttu-id="d588f-127">Si el mensaje se realiza correctamente, el [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) del valor devuelto es **true** y [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es el número de líneas que el comando desplaza.</span><span class="sxs-lookup"><span data-stu-id="d588f-127">If the message is successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the return value is **TRUE**, and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the number of lines that the command scrolls.</span></span> <span data-ttu-id="d588f-128">El número devuelto puede no ser el mismo que el número real de líneas desplazadas si el desplazamiento se desplaza hasta el principio o el final del texto.</span><span class="sxs-lookup"><span data-stu-id="d588f-128">The number returned may not be the same as the actual number of lines scrolled if the scrolling moves to the beginning or the end of the text.</span></span> <span data-ttu-id="d588f-129">Si el parámetro *wParam* especifica un valor no válido, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="d588f-129">If the *wParam* parameter specifies an invalid value, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d588f-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d588f-130">Remarks</span></span>

<span data-ttu-id="d588f-131">Para desplazarse a una línea o posición de carácter concreta, use el mensaje [**\_ LINESCROLL em**](em-linescroll.md) .</span><span class="sxs-lookup"><span data-stu-id="d588f-131">To scroll to a specific line or character position, use the [**EM\_LINESCROLL**](em-linescroll.md) message.</span></span> <span data-ttu-id="d588f-132">Para desplazar el símbolo de intercalación a la vista, use el mensaje [**\_ SCROLLCARET em**](em-scrollcaret.md) .</span><span class="sxs-lookup"><span data-stu-id="d588f-132">To scroll the caret into view, use the [**EM\_SCROLLCARET**](em-scrollcaret.md) message.</span></span>

<span data-ttu-id="d588f-133">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d588f-133">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="d588f-134">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="d588f-134">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d588f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d588f-135">Requirements</span></span>



| <span data-ttu-id="d588f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d588f-136">Requirement</span></span> | <span data-ttu-id="d588f-137">Value</span><span class="sxs-lookup"><span data-stu-id="d588f-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d588f-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d588f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d588f-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d588f-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d588f-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d588f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d588f-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d588f-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d588f-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d588f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d588f-143"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d588f-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d588f-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="d588f-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="d588f-145">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d588f-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d588f-146">**\_LINESCROLL em**</span><span class="sxs-lookup"><span data-stu-id="d588f-146">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="d588f-147">**\_SCROLLCARET em**</span><span class="sxs-lookup"><span data-stu-id="d588f-147">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="d588f-148">**VSCROLL de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d588f-148">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

