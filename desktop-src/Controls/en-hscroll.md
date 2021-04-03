---
title: Código de notificación de EN_HSCROLL (Winuser. h)
description: Se envía cuando el usuario hace clic en la barra de desplazamiento horizontal de un control de edición. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de comando de WM \_ . Se notifica a la ventana primaria antes de que se actualice la pantalla.
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- EN_HSCROLL controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f90f6e781409419e39390e64251506b4cc915a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905357"
---
# <a name="en_hscroll-notification-code"></a><span data-ttu-id="a6611-106">\_Código de notificación en HSCROLL</span><span class="sxs-lookup"><span data-stu-id="a6611-106">EN\_HSCROLL notification code</span></span>

<span data-ttu-id="a6611-107">Se envía cuando el usuario hace clic en la barra de desplazamiento horizontal de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="a6611-107">Sent when the user clicks an edit control's horizontal scroll bar.</span></span> <span data-ttu-id="a6611-108">La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="a6611-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="a6611-109">Se notifica a la ventana primaria antes de que se actualice la pantalla.</span><span class="sxs-lookup"><span data-stu-id="a6611-109">The parent window is notified before the screen is updated.</span></span>


```C++
EN_HSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="a6611-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6611-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6611-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6611-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6611-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="a6611-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="a6611-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="a6611-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="a6611-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6611-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6611-115">Identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="a6611-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6611-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6611-116">Remarks</span></span>

<span data-ttu-id="a6611-117">Este código de notificación se envía para los siguientes eventos del mouse en la barra de desplazamiento horizontal: al hacer clic en cualquier botón de flecha o hacer clic entre el botón de flecha y el control de posición.</span><span class="sxs-lookup"><span data-stu-id="a6611-117">This notification code is sent for the following mouse events on the horizontal scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="a6611-118">Sin embargo, el código de notificación no se envía al hacer clic en el propio botón de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="a6611-118">However, the notification code is not sent when clicking the scroll bar thumb itself.</span></span> <span data-ttu-id="a6611-119">El código de notificación también se envía cuando un evento de teclado provoca un cambio en el área de vista del control de edición, por ejemplo, al presionar Inicio, fin, flecha izquierda o flecha derecha.</span><span class="sxs-lookup"><span data-stu-id="a6611-119">The notification code is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, LEFT ARROW, or RIGHT ARROW.</span></span>

<span data-ttu-id="a6611-120">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a6611-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="a6611-121">Para recibir los códigos de notificación **en \_ HSCROLL** , especifique [**ENM \_ Scroll**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="a6611-121">To receive **EN\_HSCROLL** notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="a6611-122">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a6611-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6611-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6611-123">Requirements</span></span>



| <span data-ttu-id="a6611-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6611-124">Requirement</span></span> | <span data-ttu-id="a6611-125">Value</span><span class="sxs-lookup"><span data-stu-id="a6611-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6611-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6611-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a6611-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a6611-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a6611-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6611-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a6611-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6611-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a6611-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6611-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6611-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6611-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6611-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6611-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="a6611-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a6611-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a6611-134">EN \_ VSCROLL</span><span class="sxs-lookup"><span data-stu-id="a6611-134">EN\_VSCROLL</span></span>](en-vscroll.md)
</dt> <dt>

<span data-ttu-id="a6611-135">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="a6611-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a6611-136">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="a6611-136">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

