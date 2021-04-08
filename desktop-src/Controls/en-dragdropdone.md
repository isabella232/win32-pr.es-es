---
title: Código de notificación de EN_DRAGDROPDONE (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que se ha completado la operación de arrastrar y colocar. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 3c8b95cc-86ef-4aec-b551-11dca50ea5c5
keywords:
- EN_DRAGDROPDONE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_DRAGDROPDONE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10b6718122791bcc862866fbaf17ed43e8bfd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995979"
---
# <a name="en_dragdropdone-notification-code"></a><span data-ttu-id="a1f6b-105">\_Código de notificación en DRAGDROPDONE</span><span class="sxs-lookup"><span data-stu-id="a1f6b-105">EN\_DRAGDROPDONE notification code</span></span>

<span data-ttu-id="a1f6b-106">Notifica a la ventana primaria de un control Rich Edit que se ha completado la operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="a1f6b-106">Notifies a rich edit control's parent window that the drag-and-drop operation has completed.</span></span> <span data-ttu-id="a1f6b-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a1f6b-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_DRAGDROPDONE

    pnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a1f6b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1f6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1f6b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1f6b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1f6b-110">Una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="a1f6b-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1f6b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1f6b-111">Return value</span></span>

<span data-ttu-id="a1f6b-112">Este código de notificación no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="a1f6b-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1f6b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1f6b-113">Remarks</span></span>

<span data-ttu-id="a1f6b-114">Para recibir un \_ código de notificación en DRAGDROPDONE, especifique la marca [**\_ DRAGDROPDONE de ENM**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="a1f6b-114">To receive an EN\_DRAGDROPDONE notification code, specify the [**ENM\_DRAGDROPDONE**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1f6b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1f6b-115">Requirements</span></span>



| <span data-ttu-id="a1f6b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1f6b-116">Requirement</span></span> | <span data-ttu-id="a1f6b-117">Value</span><span class="sxs-lookup"><span data-stu-id="a1f6b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f6b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1f6b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a1f6b-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a1f6b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1f6b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1f6b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a1f6b-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1f6b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1f6b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1f6b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1f6b-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1f6b-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1f6b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1f6b-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1f6b-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a1f6b-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a1f6b-126">**una \_ SETEVENTMASK**</span><span class="sxs-lookup"><span data-stu-id="a1f6b-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> </dl>

 

 





