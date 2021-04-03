---
title: Código de notificación de EN_VSCROLL (Winuser. h)
description: Se envía cuando el usuario hace clic en la barra de desplazamiento vertical de un control de edición o cuando el usuario desplaza la rueda del mouse sobre el control de edición.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- EN_VSCROLL controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1f99b9ea05d037b5c00562a24bda1e434ce08d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905629"
---
# <a name="en_vscroll-notification-code"></a><span data-ttu-id="64e46-104">\_Código de notificación en VSCROLL</span><span class="sxs-lookup"><span data-stu-id="64e46-104">EN\_VSCROLL notification code</span></span>

<span data-ttu-id="64e46-105">Se envía cuando el usuario hace clic en la barra de desplazamiento vertical de un control de edición o cuando el usuario desplaza la rueda del mouse sobre el control de edición.</span><span class="sxs-lookup"><span data-stu-id="64e46-105">Sent when the user clicks an edit control's vertical scroll bar or when the user scrolls the mouse wheel over the edit control.</span></span> <span data-ttu-id="64e46-106">La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="64e46-106">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="64e46-107">Se notifica a la ventana primaria antes de que se actualice la pantalla.</span><span class="sxs-lookup"><span data-stu-id="64e46-107">The parent window is notified before the screen is updated.</span></span>


```C++
EN_VSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="64e46-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64e46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64e46-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64e46-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64e46-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="64e46-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="64e46-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="64e46-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="64e46-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64e46-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64e46-113">Identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="64e46-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64e46-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64e46-114">Remarks</span></span>

<span data-ttu-id="64e46-115">Este mensaje se envía para los siguientes eventos del mouse en la barra de desplazamiento vertical: al hacer clic en cualquier botón de flecha o hacer clic entre el botón de flecha y el control de posición.</span><span class="sxs-lookup"><span data-stu-id="64e46-115">This message is sent for the following mouse events on the vertical scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="64e46-116">Sin embargo, el mensaje no se envía al hacer clic en el propio Mouse de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="64e46-116">However, the message is not sent when clicking the scroll bar mouse itself.</span></span> <span data-ttu-id="64e46-117">El mensaje también se envía cuando un evento de teclado provoca un cambio en el área de vista del control de edición, por ejemplo, al presionar Inicio, fin, Re Pág, Av Pág, flecha arriba o flecha abajo.</span><span class="sxs-lookup"><span data-stu-id="64e46-117">The message is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, PAGE UP, PAGE DOWN, UP ARROW, or DOWN ARROW.</span></span>

<span data-ttu-id="64e46-118">La rueda del mouse es un mouse con una rueda central que se desplaza.</span><span class="sxs-lookup"><span data-stu-id="64e46-118">The mouse wheel is a mouse that has a center wheel that scrolls.</span></span> <span data-ttu-id="64e46-119">Para obtener más información, vea "la rueda del mouse" en acerca de la [entrada del mouse](/windows/desktop/inputdev/about-mouse-input).</span><span class="sxs-lookup"><span data-stu-id="64e46-119">For more information, see "The Mouse Wheel" in [About Mouse Input](/windows/desktop/inputdev/about-mouse-input).</span></span>

<span data-ttu-id="64e46-120">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="64e46-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="64e46-121">Para recibir los \_ códigos de notificación en VSCROLL, especifique [**ENM \_ Scroll**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="64e46-121">To receive EN\_VSCROLL notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="64e46-122">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="64e46-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64e46-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64e46-123">Requirements</span></span>



| <span data-ttu-id="64e46-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="64e46-124">Requirement</span></span> | <span data-ttu-id="64e46-125">Value</span><span class="sxs-lookup"><span data-stu-id="64e46-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64e46-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64e46-126">Minimum supported client</span></span><br/> | <span data-ttu-id="64e46-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="64e46-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="64e46-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64e46-128">Minimum supported server</span></span><br/> | <span data-ttu-id="64e46-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="64e46-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="64e46-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64e46-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="64e46-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64e46-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64e46-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="64e46-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="64e46-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="64e46-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="64e46-134">EN \_ HSCROLL</span><span class="sxs-lookup"><span data-stu-id="64e46-134">EN\_HSCROLL</span></span>](en-hscroll.md)
</dt> <dt>

<span data-ttu-id="64e46-135">**Vista**</span><span class="sxs-lookup"><span data-stu-id="64e46-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="64e46-136">Usar controles de edición</span><span class="sxs-lookup"><span data-stu-id="64e46-136">Using Edit Controls</span></span>](using-edit-controls.md)
</dt> <dt>

<span data-ttu-id="64e46-137">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="64e46-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="64e46-138">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="64e46-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

