---
title: Código de notificación de EN_MAXTEXT (Winuser. h)
description: Se envía cuando la inserción de texto actual ha superado el número de caracteres especificado para el control de edición.
ms.assetid: b03835d6-d06f-415a-97f2-d2b62b17e175
keywords:
- EN_MAXTEXT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_MAXTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 454b48fb232f2225696efacc44d54660d3a83185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535044"
---
# <a name="en_maxtext-notification-code"></a><span data-ttu-id="f5899-104">\_Código de notificación en MAXTEXT</span><span class="sxs-lookup"><span data-stu-id="f5899-104">EN\_MAXTEXT notification code</span></span>

<span data-ttu-id="f5899-105">Se envía cuando la inserción de texto actual ha superado el número de caracteres especificado para el control de edición.</span><span class="sxs-lookup"><span data-stu-id="f5899-105">Sent when the current text insertion has exceeded the specified number of characters for the edit control.</span></span> <span data-ttu-id="f5899-106">La inserción de texto se ha truncado.</span><span class="sxs-lookup"><span data-stu-id="f5899-106">The text insertion has been truncated.</span></span>

<span data-ttu-id="f5899-107">Este código de notificación también se envía cuando un control de edición no tiene el estilo [**es \_ AUTOHSCROLL**](edit-control-styles.md) y el número de caracteres que se va a insertar superará el ancho del control de edición.</span><span class="sxs-lookup"><span data-stu-id="f5899-107">This notification code is also sent when an edit control does not have the [**ES\_AUTOHSCROLL**](edit-control-styles.md) style and the number of characters to be inserted would exceed the width of the edit control.</span></span>

<span data-ttu-id="f5899-108">Este código de notificación también se envía cuando un control de edición no tiene el estilo [**es \_ AUTOVSCROLL**](edit-control-styles.md) y el número total de líneas resultante de una inserción de texto superaría el alto del control de edición.</span><span class="sxs-lookup"><span data-stu-id="f5899-108">This notification code is also sent when an edit control does not have the [**ES\_AUTOVSCROLL**](edit-control-styles.md) style and the total number of lines resulting from a text insertion would exceed the height of the edit control.</span></span>

<span data-ttu-id="f5899-109">La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="f5899-109">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_MAXTEXT

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="f5899-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5899-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5899-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5899-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5899-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="f5899-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="f5899-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="f5899-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="f5899-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5899-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5899-115">Identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="f5899-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5899-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5899-116">Remarks</span></span>

<span data-ttu-id="f5899-117">La ventana primaria siempre recibe un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) para este evento, pero no requiere que se envíe una máscara de notificación con [**em \_**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="f5899-117">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="f5899-118">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f5899-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="f5899-119">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f5899-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5899-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5899-120">Requirements</span></span>



| <span data-ttu-id="f5899-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5899-121">Requirement</span></span> | <span data-ttu-id="f5899-122">Value</span><span class="sxs-lookup"><span data-stu-id="f5899-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5899-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5899-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f5899-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f5899-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f5899-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5899-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f5899-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5899-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f5899-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5899-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5899-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5899-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5899-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5899-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5899-130">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f5899-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

