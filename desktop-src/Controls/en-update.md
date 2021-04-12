---
title: Código de notificación de EN_UPDATE (Winuser. h)
description: Se envía cuando un control de edición está a punto de volver a dibujarse.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- EN_UPDATE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b045efcfb5d50cb2a85c9ae230e215263aa2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150909"
---
# <a name="en_update-notification-code"></a><span data-ttu-id="e4dd3-104">EN el \_ código de notificación de actualización</span><span class="sxs-lookup"><span data-stu-id="e4dd3-104">EN\_UPDATE notification code</span></span>

<span data-ttu-id="e4dd3-105">Se envía cuando un control de edición está a punto de volver a dibujarse.</span><span class="sxs-lookup"><span data-stu-id="e4dd3-105">Sent when an edit control is about to redraw itself.</span></span> <span data-ttu-id="e4dd3-106">Este código de notificación se envía una vez que el control ha dado formato al texto, pero antes de que muestre el texto.</span><span class="sxs-lookup"><span data-stu-id="e4dd3-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="e4dd3-107">Esto hace posible cambiar el tamaño de la ventana de control de edición, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="e4dd3-107">This makes it possible to resize the edit control window, if necessary.</span></span> <span data-ttu-id="e4dd3-108">La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e4dd3-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_UPDATE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="e4dd3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4dd3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4dd3-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4dd3-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4dd3-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="e4dd3-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="e4dd3-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="e4dd3-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e4dd3-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4dd3-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4dd3-114">Identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="e4dd3-114">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4dd3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4dd3-115">Remarks</span></span>

<span data-ttu-id="e4dd3-116">**Rich Edit 1,0:** Para recibir los \_ códigos de notificación en la actualización, especifique [**ENM \_ Update**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="e4dd3-116">**Rich Edit 1.0:** To receive EN\_UPDATE notification codes, specify [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="e4dd3-117">**Edición enriquecida 2,0 y versiones posteriores:** La marca de [**\_ actualización ENM**](rich-edit-control-event-mask-flags.md) se omite.</span><span class="sxs-lookup"><span data-stu-id="e4dd3-117">**Rich Edit 2.0 and later:** The [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) flag is ignored.</span></span> <span data-ttu-id="e4dd3-118">\_Siempre se recibe el código de notificación en actualización.</span><span class="sxs-lookup"><span data-stu-id="e4dd3-118">The EN\_UPDATE notification code is always received.</span></span> <span data-ttu-id="e4dd3-119">Sin embargo, cuando Microsoft Rich Edit 3,0 emula Microsoft Rich Edit 1,0, para recibir \_ los códigos de notificación de actualización debe especificar **ENM \_ Update** en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="e4dd3-119">However, when Microsoft Rich Edit 3.0 emulates Microsoft Rich Edit 1.0, to receive EN\_UPDATE notification codes you must specify **ENM\_UPDATE** in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="e4dd3-120">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e4dd3-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4dd3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4dd3-121">Requirements</span></span>



| <span data-ttu-id="e4dd3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4dd3-122">Requirement</span></span> | <span data-ttu-id="e4dd3-123">Value</span><span class="sxs-lookup"><span data-stu-id="e4dd3-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4dd3-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4dd3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e4dd3-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e4dd3-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e4dd3-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4dd3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e4dd3-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4dd3-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e4dd3-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4dd3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4dd3-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4dd3-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4dd3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4dd3-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="e4dd3-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e4dd3-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e4dd3-132">EN \_ cambio</span><span class="sxs-lookup"><span data-stu-id="e4dd3-132">EN\_CHANGE</span></span>](en-change.md)
</dt> <dt>

<span data-ttu-id="e4dd3-133">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="e4dd3-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e4dd3-134">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e4dd3-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

