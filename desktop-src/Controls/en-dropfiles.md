---
title: Código de notificación de EN_DROPFILES (RichEdit. h)
description: Notifica a una ventana primaria de un control Rich Edit que el usuario está intentando colocar archivos en el control. Un control Rich Edit envía este código de notificación en forma de mensaje de notificación de WM \_ cuando recibe el mensaje de DROPFILES de WM \_ .
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- EN_DROPFILES controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c0ed1a4a9b95348b1de20e54fcf3b167df19f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489286"
---
# <a name="en_dropfiles-notification-code"></a><span data-ttu-id="8186f-105">\_Código de notificación en DROPFILES</span><span class="sxs-lookup"><span data-stu-id="8186f-105">EN\_DROPFILES notification code</span></span>

<span data-ttu-id="8186f-106">Notifica a una ventana primaria de un control Rich Edit que el usuario está intentando colocar archivos en el control.</span><span class="sxs-lookup"><span data-stu-id="8186f-106">Notifies a rich edit control parent window that the user is attempting to drop files into the control.</span></span> <span data-ttu-id="8186f-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) cuando recibe el mensaje de [**\_ DROPFILES de WM**](/windows/desktop/shell/wm-dropfiles) .</span><span class="sxs-lookup"><span data-stu-id="8186f-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message when it receives the [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) message.</span></span>


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8186f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8186f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8186f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8186f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8186f-110">Estructura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) que recibe la información de los archivos colocados.</span><span class="sxs-lookup"><span data-stu-id="8186f-110">An [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure that receives dropped files information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8186f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8186f-111">Return value</span></span>

<span data-ttu-id="8186f-112">Devuelve un valor distinto de cero para permitir la operación de colocar.</span><span class="sxs-lookup"><span data-stu-id="8186f-112">Return a nonzero value to allow the drop operation.</span></span>

<span data-ttu-id="8186f-113">Devuelve cero para omitir la operación de colocar.</span><span class="sxs-lookup"><span data-stu-id="8186f-113">Return zero to ignore the drop operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="8186f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8186f-114">Remarks</span></span>

<span data-ttu-id="8186f-115">Para que un control de edición enriquecido reciba mensajes de [**WM \_ DROPFILES**](/windows/desktop/shell/wm-dropfiles) , la ventana primaria debe registrar el control como destino de colocación mediante la función [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) .</span><span class="sxs-lookup"><span data-stu-id="8186f-115">For a rich edit control to receive [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) messages, the parent window must register the control as a drop target by using the [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) function.</span></span> <span data-ttu-id="8186f-116">El control no se registra a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="8186f-116">The control does not register itself.</span></span>

<span data-ttu-id="8186f-117">Para recibir los \_ códigos de notificación en DROPFILES, especifique [**ENM \_ DROPFILES**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="8186f-117">To receive EN\_DROPFILES notification codes, specify [**ENM\_DROPFILES**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8186f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8186f-118">Requirements</span></span>



| <span data-ttu-id="8186f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8186f-119">Requirement</span></span> | <span data-ttu-id="8186f-120">Value</span><span class="sxs-lookup"><span data-stu-id="8186f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8186f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8186f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8186f-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8186f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8186f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8186f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8186f-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8186f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8186f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8186f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8186f-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8186f-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8186f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8186f-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="8186f-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8186f-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8186f-129">**ENDROPFILES**</span><span class="sxs-lookup"><span data-stu-id="8186f-129">**ENDROPFILES**</span></span>](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

