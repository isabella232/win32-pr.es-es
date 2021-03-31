---
title: Código de notificación de EN_CORRECTTEXT (RichEdit. h)
description: Notifica a una ventana primaria de un control Rich Edit que \_ se ha producido un gesto SyV correcto, lo que permite a la ventana primaria tener la posibilidad de cancelar la corrección del texto. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- EN_CORRECTTEXT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d1339513a94967ab60bdab2b9ee39172b19e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149944"
---
# <a name="en_correcttext-notification-code"></a><span data-ttu-id="097e7-105">\_Código de notificación en CORRECTTEXT</span><span class="sxs-lookup"><span data-stu-id="097e7-105">EN\_CORRECTTEXT notification code</span></span>

<span data-ttu-id="097e7-106">Notifica a una ventana primaria de un control Rich Edit que \_ se ha producido un gesto SyV correcto, lo que permite a la ventana primaria tener la posibilidad de cancelar la corrección del texto.</span><span class="sxs-lookup"><span data-stu-id="097e7-106">Notifies a rich edit control parent window that a SYV\_CORRECT gesture occurred, giving the parent window a chance to cancel correcting the text.</span></span> <span data-ttu-id="097e7-107">Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="097e7-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="097e7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="097e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="097e7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="097e7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="097e7-110">Estructura [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) que especifica la selección que se va a corregir.</span><span class="sxs-lookup"><span data-stu-id="097e7-110">An [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) structure specifying the selection to be corrected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="097e7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="097e7-111">Return value</span></span>

<span data-ttu-id="097e7-112">Devuelve cero para omitir la acción.</span><span class="sxs-lookup"><span data-stu-id="097e7-112">Return zero to ignore the action.</span></span>

<span data-ttu-id="097e7-113">Devuelve un valor distinto de cero para procesar la acción.</span><span class="sxs-lookup"><span data-stu-id="097e7-113">Returns a nonzero value to process the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="097e7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="097e7-114">Remarks</span></span>

<span data-ttu-id="097e7-115">Este código de notificación se envía solo si están disponibles las capacidades del lápiz.</span><span class="sxs-lookup"><span data-stu-id="097e7-115">This notification code is sent only if pen capabilities are available.</span></span>

<span data-ttu-id="097e7-116">Para recibir los \_ códigos de notificación en CORRECTTEXT, especifique [**ENM \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="097e7-116">To receive EN\_CORRECTTEXT notification codes, specify [**ENM\_CORRECTTEXT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="097e7-117">El \_ código de notificación en CORRECTTEXT solo se admite en la versión de edición enriquecida 1,0.</span><span class="sxs-lookup"><span data-stu-id="097e7-117">The EN\_CORRECTTEXT notification code is only supported in rich edit version 1.0.</span></span> <span data-ttu-id="097e7-118">No se admite en versiones posteriores de Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="097e7-118">It is not supported in later versions of rich edit.</span></span> <span data-ttu-id="097e7-119">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="097e7-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="097e7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="097e7-120">Requirements</span></span>



| <span data-ttu-id="097e7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="097e7-121">Requirement</span></span> | <span data-ttu-id="097e7-122">Value</span><span class="sxs-lookup"><span data-stu-id="097e7-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="097e7-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="097e7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="097e7-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="097e7-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="097e7-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="097e7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="097e7-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="097e7-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="097e7-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="097e7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="097e7-128"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="097e7-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="097e7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="097e7-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="097e7-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="097e7-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="097e7-131">**ENCORRECTTEXT**</span><span class="sxs-lookup"><span data-stu-id="097e7-131">**ENCORRECTTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





