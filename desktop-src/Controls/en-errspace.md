---
title: Código de notificación de EN_ERRSPACE (Winuser. h)
description: Se envía cuando un control de edición no puede asignar suficiente memoria para satisfacer una solicitud concreta. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de comando de WM \_ .
ms.assetid: 23a6eb10-a9d7-4fd5-9176-407c35e6f492
keywords:
- EN_ERRSPACE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05b100811741ee5c5f6bf53eb49ff05b118de3c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905037"
---
# <a name="en_errspace-notification-code"></a><span data-ttu-id="98c34-105">\_Código de notificación en ERRSPACE</span><span class="sxs-lookup"><span data-stu-id="98c34-105">EN\_ERRSPACE notification code</span></span>

<span data-ttu-id="98c34-106">Se envía cuando un control de edición no puede asignar suficiente memoria para satisfacer una solicitud concreta.</span><span class="sxs-lookup"><span data-stu-id="98c34-106">Sent when an edit control cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="98c34-107">La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="98c34-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="98c34-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98c34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98c34-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98c34-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98c34-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="98c34-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="98c34-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="98c34-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="98c34-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98c34-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98c34-113">Identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="98c34-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98c34-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98c34-114">Remarks</span></span>

<span data-ttu-id="98c34-115">La ventana primaria siempre obtendrá un mensaje [**de \_ comando de WM**](/windows/desktop/menurc/wm-command) para este evento; no requiere que se envíe una máscara de notificación con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="98c34-115">The parent window will always get a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event; it does not require a notification mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="98c34-116">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="98c34-116">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="98c34-117">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="98c34-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98c34-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98c34-118">Requirements</span></span>



| <span data-ttu-id="98c34-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="98c34-119">Requirement</span></span> | <span data-ttu-id="98c34-120">Value</span><span class="sxs-lookup"><span data-stu-id="98c34-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98c34-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98c34-121">Minimum supported client</span></span><br/> | <span data-ttu-id="98c34-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="98c34-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="98c34-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98c34-123">Minimum supported server</span></span><br/> | <span data-ttu-id="98c34-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="98c34-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="98c34-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98c34-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="98c34-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98c34-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98c34-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="98c34-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98c34-128">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="98c34-128">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

