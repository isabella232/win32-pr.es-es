---
title: Código de notificación de EN_REQUESTRESIZE (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que el contenido del control es menor o mayor que el tamaño de la ventana del control. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- EN_REQUESTRESIZE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150558"
---
# <a name="en_requestresize-notification-code"></a><span data-ttu-id="7c9c4-105">\_Código de notificación en REQUESTRESIZE</span><span class="sxs-lookup"><span data-stu-id="7c9c4-105">EN\_REQUESTRESIZE notification code</span></span>

<span data-ttu-id="7c9c4-106">Notifica a la ventana primaria de un control Rich Edit que el contenido del control es menor o mayor que el tamaño de la ventana del control.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-106">Notifies a rich edit control's parent window that the control's contents are either smaller or larger than the control's window size.</span></span> <span data-ttu-id="7c9c4-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7c9c4-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7c9c4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c9c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c9c4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c9c4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c9c4-110">Una estructura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) que recibe el tamaño solicitado.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-110">A [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure that receives the requested size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c9c4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c9c4-111">Return value</span></span>

<span data-ttu-id="7c9c4-112">Este código de notificación no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c9c4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c9c4-113">Remarks</span></span>

<span data-ttu-id="7c9c4-114">Para admitir el comportamiento sin límite de un control Rich Edit, la ventana primaria debe cambiar el tamaño del control cuando recibe este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="7c9c4-114">To support the bottomless behavior of a rich edit control, the parent window must resize the control when it receives this notification code.</span></span>

<span data-ttu-id="7c9c4-115">Para recibir los \_ códigos de notificación en REQUESTRESIZE, especifique [**ENM \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="7c9c4-115">To receive EN\_REQUESTRESIZE notification codes, specify [**ENM\_REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c9c4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c9c4-116">Requirements</span></span>



| <span data-ttu-id="7c9c4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c9c4-117">Requirement</span></span> | <span data-ttu-id="7c9c4-118">Value</span><span class="sxs-lookup"><span data-stu-id="7c9c4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c9c4-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c9c4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7c9c4-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7c9c4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c9c4-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c9c4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7c9c4-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c9c4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c9c4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c9c4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c9c4-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c9c4-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c9c4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c9c4-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c9c4-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="7c9c4-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7c9c4-127">**REQRESIZE**</span><span class="sxs-lookup"><span data-stu-id="7c9c4-127">**REQRESIZE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[<span data-ttu-id="7c9c4-128">**\_notificaciones de WM**</span><span class="sxs-lookup"><span data-stu-id="7c9c4-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





