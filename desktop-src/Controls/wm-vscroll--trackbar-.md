---
title: Código de notificación de WM_VSCROLL (TrackBar) (Winuser. h)
description: El \_ mensaje de VSCROLL de WM se envía al propietario de un control de barra de desplazamiento vertical cuando cambia la posición del control deslizante. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: E491E210-9605-4ABB-A667-471830DA7C2B
keywords:
- Controles de Windows de código de notificación de WM_VSCROLL (TrackBar)
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e13b07fab3335bf99469cd43ed1caa10373a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150531"
---
# <a name="wm_vscroll-trackbar-notification-code"></a><span data-ttu-id="91976-105">\_Código de notificación de VSCROLL (TrackBar) de WM</span><span class="sxs-lookup"><span data-stu-id="91976-105">WM\_VSCROLL (Trackbar) notification code</span></span>

<span data-ttu-id="91976-106">El mensaje de **\_ VSCROLL de WM** se envía al propietario de un control de barra de desplazamiento vertical cuando cambia la posición del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="91976-106">The **WM\_VSCROLL** message is sent to the owner of a vertical trackbar control when the slider changes position.</span></span>

<span data-ttu-id="91976-107">Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="91976-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="91976-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91976-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91976-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91976-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91976-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición actual del control deslizante si el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es TB \_ THUMBPOSITION o TB \_ THUMBTRACK.</span><span class="sxs-lookup"><span data-stu-id="91976-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the slider if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is TB\_THUMBPOSITION or TB\_THUMBTRACK.</span></span> <span data-ttu-id="91976-111">En el resto de códigos de notificación, la palabra de orden superior es cero; Envíe el [**mensaje \_ GETPOS de TBM**](tbm-getpos.md) para determinar la posición del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="91976-111">For all other notification codes, the high-order word is zero; send the [**TBM\_GETPOS**](tbm-getpos.md) message to determine the slider position.</span></span>

<span data-ttu-id="91976-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica un código de notificación que indica la interacción del usuario con el TrackBar.</span><span class="sxs-lookup"><span data-stu-id="91976-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a notification code that indicates the user's interaction with the trackbar.</span></span> <span data-ttu-id="91976-113">Esta palabra puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="91976-113">This word can be one of the following values.</span></span>



| <span data-ttu-id="91976-114">Value</span><span class="sxs-lookup"><span data-stu-id="91976-114">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="91976-115">Significado</span><span class="sxs-lookup"><span data-stu-id="91976-115">Meaning</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <span data-ttu-id="91976-116"><dt>**TB en la \_ parte inferior**</dt></span><span class="sxs-lookup"><span data-stu-id="91976-116"><dt>**TB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="91976-117">El usuario presionó la tecla fin ([**VK \_ End**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="91976-117">The user pressed the END key ([**VK\_END**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <span data-ttu-id="91976-118"><dt>**TB \_ ENDTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="91976-118"><dt>**TB\_ENDTRACK**</dt></span></span> </dl>                | <span data-ttu-id="91976-119">La barra de Estado ha recibido el [**\_ KEYUP de WM**](/windows/desktop/inputdev/wm-keyup), lo que significa que el usuario liberó una clave que envió un código de tecla virtual relevante.</span><span class="sxs-lookup"><span data-stu-id="91976-119">The trackbar received [**WM\_KEYUP**](/windows/desktop/inputdev/wm-keyup), meaning that the user released a key that sent a relevant virtual key code.</span></span> <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <span data-ttu-id="91976-120"><dt>**TB \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="91976-120"><dt>**TB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="91976-121">El usuario presionó la tecla flecha derecha ([**VK \_ derecha**](/windows/desktop/inputdev/virtual-key-codes)) o flecha abajo ([**VK \_ abajo**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="91976-121">The user pressed the RIGHT ARROW ([**VK\_RIGHT**](/windows/desktop/inputdev/virtual-key-codes)) or DOWN ARROW ([**VK\_DOWN**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <span data-ttu-id="91976-122"><dt>**gama de TB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="91976-122"><dt>**TB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="91976-123">El usuario presionó la tecla flecha izquierda ([**VK \_ izquierda**](/windows/desktop/inputdev/virtual-key-codes)) o flecha arriba ([**VK \_ arriba**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="91976-123">The user pressed the LEFT ARROW ([**VK\_LEFT**](/windows/desktop/inputdev/virtual-key-codes)) or UP ARROW ([**VK\_UP**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <span data-ttu-id="91976-124"><dt>**TB \_ Av Pág**</dt></span><span class="sxs-lookup"><span data-stu-id="91976-124"><dt>**TB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="91976-125">El usuario hizo clic en el canal siguiente o a la derecha del control deslizante ([**VK \_ siguiente**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="91976-125">The user clicked the channel below or to the right of the slider ([**VK\_NEXT**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <span data-ttu-id="91976-126"><dt>**TB \_ RePág**</dt></span><span class="sxs-lookup"><span data-stu-id="91976-126"><dt>**TB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="91976-127">El usuario hizo clic en el canal situado encima o a la izquierda del control deslizante ([**VK \_ anterior**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="91976-127">The user clicked the channel above or to the left of the slider ([**VK\_PRIOR**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <span data-ttu-id="91976-128"><dt>**TB \_ THUMBPOSITION**</dt></span><span class="sxs-lookup"><span data-stu-id="91976-128"><dt>**TB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="91976-129">El TrackBar ha recibido [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) después de un código de notificación de TB \_ THUMBTRACK.</span><span class="sxs-lookup"><span data-stu-id="91976-129">The trackbar received [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) following a TB\_THUMBTRACK notification code.</span></span><br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <span data-ttu-id="91976-130"><dt>**TB \_ THUMBTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="91976-130"><dt>**TB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="91976-131">El usuario arrastró el control deslizante.</span><span class="sxs-lookup"><span data-stu-id="91976-131">The user dragged the slider.</span></span><br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <span data-ttu-id="91976-132"><dt>**TB en la \_ parte superior**</dt></span><span class="sxs-lookup"><span data-stu-id="91976-132"><dt>**TB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="91976-133">El usuario presionó la tecla Inicio ([**VK \_ Home**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="91976-133">The user pressed the HOME key ([**VK\_HOME**](/windows/desktop/inputdev/virtual-key-codes)).</span></span> <br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="91976-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91976-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91976-135">Identificador del control TrackBar.</span><span class="sxs-lookup"><span data-stu-id="91976-135">The handle to the trackbar control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91976-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91976-136">Return value</span></span>

<span data-ttu-id="91976-137">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="91976-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="91976-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91976-138">Remarks</span></span>

<span data-ttu-id="91976-139">El código de TB \_ THUMBTRACK se usa normalmente en aplicaciones que proporcionan comentarios cuando el usuario arrastra el cuadro de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="91976-139">The TB\_THUMBTRACK code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="91976-140">Tenga en cuenta que el mensaje de **\_ VSCROLL de WM** solo incluye 16 bits de datos de posición.</span><span class="sxs-lookup"><span data-stu-id="91976-140">Note that the **WM\_VSCROLL** message carries only 16 bits of position data.</span></span> <span data-ttu-id="91976-141">Por lo tanto, las aplicaciones que se basan únicamente en **WM \_ VSCROLL** (y en [**WM \_ HSCROLL**](wm-hscroll--trackbar-.md)) para los datos de posición del control deslizante tienen un valor de posición máximo práctico de 65.535.</span><span class="sxs-lookup"><span data-stu-id="91976-141">Thus, applications that rely solely on **WM\_VSCROLL** (and [**WM\_HSCROLL**](wm-hscroll--trackbar-.md)) for slider position data have a practical maximum position value of 65,535.</span></span>

## <a name="requirements"></a><span data-ttu-id="91976-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91976-142">Requirements</span></span>



| <span data-ttu-id="91976-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="91976-143">Requirement</span></span> | <span data-ttu-id="91976-144">Value</span><span class="sxs-lookup"><span data-stu-id="91976-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91976-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91976-145">Minimum supported client</span></span><br/> | <span data-ttu-id="91976-146">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="91976-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="91976-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91976-147">Minimum supported server</span></span><br/> | <span data-ttu-id="91976-148">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="91976-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="91976-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91976-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="91976-150"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91976-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91976-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="91976-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="91976-152">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="91976-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="91976-153">**HSCROLL de WM \_**</span><span class="sxs-lookup"><span data-stu-id="91976-153">**WM\_HSCROLL**</span></span>](wm-hscroll--trackbar-.md)
</dt> </dl>

 

