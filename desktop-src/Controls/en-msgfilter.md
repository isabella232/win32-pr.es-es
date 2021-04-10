---
title: Código de notificación de EN_MSGFILTER (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit de un evento de teclado o del mouse en el control. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- EN_MSGFILTER controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40ddb3e9b1d5314e2e981b00f0e0ef8e22974242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150369"
---
# <a name="en_msgfilter-notification-code"></a><span data-ttu-id="124ba-105">\_Código de notificación en MSGFILTER</span><span class="sxs-lookup"><span data-stu-id="124ba-105">EN\_MSGFILTER notification code</span></span>

<span data-ttu-id="124ba-106">Notifica a la ventana primaria de un control Rich Edit de un evento de teclado o del mouse en el control.</span><span class="sxs-lookup"><span data-stu-id="124ba-106">Notifies a rich edit control's parent window of a keyboard or mouse event in the control.</span></span> <span data-ttu-id="124ba-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="124ba-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="124ba-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="124ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="124ba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="124ba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="124ba-110">Estructura [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) que contiene información sobre el mensaje del mouse o del teclado.</span><span class="sxs-lookup"><span data-stu-id="124ba-110">A [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure containing information about the keyboard or mouse message.</span></span> <span data-ttu-id="124ba-111">Si la ventana primaria modifica esta estructura y devuelve un valor distinto de cero, el mensaje modificado se procesa en lugar del original.</span><span class="sxs-lookup"><span data-stu-id="124ba-111">If the parent window modifies this structure and returns a nonzero value, the modified message is processed instead of the original one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="124ba-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="124ba-112">Return value</span></span>

<span data-ttu-id="124ba-113">Devuelve cero si el control debe procesar el evento de teclado o del mouse.</span><span class="sxs-lookup"><span data-stu-id="124ba-113">Return zero if the control should process the keyboard or mouse event.</span></span>

<span data-ttu-id="124ba-114">Devuelve un valor distinto de cero si el control debe omitir el evento de teclado o del mouse.</span><span class="sxs-lookup"><span data-stu-id="124ba-114">Return nonzero if the control should ignore the keyboard or mouse event.</span></span>

## <a name="remarks"></a><span data-ttu-id="124ba-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="124ba-115">Remarks</span></span>

<span data-ttu-id="124ba-116">Para recibir \_ los códigos de notificación en MSGFILTER para los eventos, especifique una o varias de las siguientes marcas en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="124ba-116">To receive EN\_MSGFILTER notification codes for events, specify one or more of the following flags in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>



| <span data-ttu-id="124ba-117">Marca</span><span class="sxs-lookup"><span data-stu-id="124ba-117">Flag</span></span>                                                                             | <span data-ttu-id="124ba-118">Significado</span><span class="sxs-lookup"><span data-stu-id="124ba-118">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="124ba-119">**ENM \_ KEYEVENTS**</span><span class="sxs-lookup"><span data-stu-id="124ba-119">**ENM\_KEYEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)       | <span data-ttu-id="124ba-120">Para recibir códigos de notificación para los eventos de teclado.</span><span class="sxs-lookup"><span data-stu-id="124ba-120">To receive notification codes for keyboard events.</span></span>     |
| [<span data-ttu-id="124ba-121">**ENM \_ MOUSEEVENTS**</span><span class="sxs-lookup"><span data-stu-id="124ba-121">**ENM\_MOUSEEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)   | <span data-ttu-id="124ba-122">Para recibir códigos de notificación para los eventos del mouse.</span><span class="sxs-lookup"><span data-stu-id="124ba-122">To receive notification codes for mouse events.</span></span>        |
| [<span data-ttu-id="124ba-123">**ENM \_ SCROLLEVENTS**</span><span class="sxs-lookup"><span data-stu-id="124ba-123">**ENM\_SCROLLEVENTS**</span></span>](rich-edit-control-event-mask-flags.md) | <span data-ttu-id="124ba-124">Para recibir los códigos de notificación de un evento de rueda del mouse.</span><span class="sxs-lookup"><span data-stu-id="124ba-124">To receive notification codes for a mouse wheel event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="124ba-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="124ba-125">Requirements</span></span>



| <span data-ttu-id="124ba-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="124ba-126">Requirement</span></span> | <span data-ttu-id="124ba-127">Value</span><span class="sxs-lookup"><span data-stu-id="124ba-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="124ba-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="124ba-128">Minimum supported client</span></span><br/> | <span data-ttu-id="124ba-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="124ba-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="124ba-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="124ba-130">Minimum supported server</span></span><br/> | <span data-ttu-id="124ba-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="124ba-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="124ba-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="124ba-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="124ba-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="124ba-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="124ba-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="124ba-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="124ba-135">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="124ba-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="124ba-136">**MSGFILTER**</span><span class="sxs-lookup"><span data-stu-id="124ba-136">**MSGFILTER**</span></span>](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[<span data-ttu-id="124ba-137">**\_notificaciones de WM**</span><span class="sxs-lookup"><span data-stu-id="124ba-137">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





