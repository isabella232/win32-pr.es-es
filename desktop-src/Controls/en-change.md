---
title: Código de notificación de EN_CHANGE (Winuser. h)
description: Se envía cuando el usuario ha realizado una acción que puede haber alterado el texto en un control de edición.
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- EN_CHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ef26d1ec4f8ec1dc93e54d46b88c4fe7cc872b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905136"
---
# <a name="en_change-notification-code"></a><span data-ttu-id="5aa7b-104">EN \_ código de notificación de cambio</span><span class="sxs-lookup"><span data-stu-id="5aa7b-104">EN\_CHANGE notification code</span></span>

<span data-ttu-id="5aa7b-105">Se envía cuando el usuario ha realizado una acción que puede haber alterado el texto en un control de edición.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-105">Sent when the user has taken an action that may have altered text in an edit control.</span></span> <span data-ttu-id="5aa7b-106">A diferencia del código de notificación [en la \_ actualización](en-update.md) , este código de notificación se envía cuando el sistema actualiza la pantalla.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-106">Unlike the [EN\_UPDATE](en-update.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="5aa7b-107">La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="5aa7b-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_CHANGE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="5aa7b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5aa7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aa7b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5aa7b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5aa7b-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="5aa7b-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="5aa7b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5aa7b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5aa7b-113">Identificador del control de edición.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5aa7b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aa7b-114">Remarks</span></span>

<span data-ttu-id="5aa7b-115">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-115">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="5aa7b-116">Para recibir los \_ códigos de notificación de cambio, especifique el [**\_ cambio ENM**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa7b-116">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="5aa7b-117">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="5aa7b-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="5aa7b-118">El \_ código de notificación en cambio no se envía cuando se usa el estilo es [**\_ multilínea**](edit-control-styles.md) y el texto se envía a través de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext).</span><span class="sxs-lookup"><span data-stu-id="5aa7b-118">The EN\_CHANGE notification code is not sent when the [**ES\_MULTILINE**](edit-control-styles.md) style is used and the text is sent through [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa7b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aa7b-119">Requirements</span></span>



| <span data-ttu-id="5aa7b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aa7b-120">Requirement</span></span> | <span data-ttu-id="5aa7b-121">Value</span><span class="sxs-lookup"><span data-stu-id="5aa7b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa7b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aa7b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5aa7b-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5aa7b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5aa7b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aa7b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5aa7b-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5aa7b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5aa7b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5aa7b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5aa7b-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5aa7b-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aa7b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aa7b-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="5aa7b-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5aa7b-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5aa7b-130">EN \_ actualización</span><span class="sxs-lookup"><span data-stu-id="5aa7b-130">EN\_UPDATE</span></span>](en-update.md)
</dt> <dt>

<span data-ttu-id="5aa7b-131">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="5aa7b-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5aa7b-132">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5aa7b-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

