---
title: Mensaje EM_FORMATRANGE (RichEdit. h)
description: Da formato a un intervalo de texto en un control Rich Edit para un dispositivo específico.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- EM_FORMATRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_FORMATRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f235fb054643623510ea23e73001aaeb070be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905314"
---
# <a name="em_formatrange-message"></a><span data-ttu-id="89494-104">\_Mensaje FORMATRANGE em</span><span class="sxs-lookup"><span data-stu-id="89494-104">EM\_FORMATRANGE message</span></span>

<span data-ttu-id="89494-105">Da formato a un intervalo de texto en un control Rich Edit para un dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="89494-105">Formats a range of text in a rich edit control for a specific device.</span></span>

## <a name="parameters"></a><span data-ttu-id="89494-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89494-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89494-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89494-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89494-108">Especifica si se va a representar el texto.</span><span class="sxs-lookup"><span data-stu-id="89494-108">Specifies whether to render the text.</span></span> <span data-ttu-id="89494-109">Si este parámetro no es cero, se representa el texto.</span><span class="sxs-lookup"><span data-stu-id="89494-109">If this parameter is not zero, the text is rendered.</span></span> <span data-ttu-id="89494-110">De lo contrario, el texto se mide simplemente.</span><span class="sxs-lookup"><span data-stu-id="89494-110">Otherwise, the text is just measured.</span></span>

</dd> <dt>

<span data-ttu-id="89494-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89494-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89494-112">Una estructura [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) que contiene información sobre el dispositivo de salida o **null** para liberar información almacenada en memoria caché por el control.</span><span class="sxs-lookup"><span data-stu-id="89494-112">A [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure containing information about the output device, or **NULL** to free information cached by the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89494-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89494-113">Return value</span></span>

<span data-ttu-id="89494-114">Este mensaje devuelve el índice del último carácter que cabe en la región, más 1.</span><span class="sxs-lookup"><span data-stu-id="89494-114">This message returns the index of the last character that fits in the region, plus 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="89494-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89494-115">Remarks</span></span>

<span data-ttu-id="89494-116">Este mensaje se usa normalmente para dar formato al contenido de un control Rich Edit para un dispositivo de salida, como una impresora.</span><span class="sxs-lookup"><span data-stu-id="89494-116">This message is typically used to format the content of rich edit control for an output device such as a printer.</span></span>

<span data-ttu-id="89494-117">Después de usar este mensaje para dar formato a un intervalo de texto, es importante que libere información en caché enviando **\_ FORMATRANGE de EM** de nuevo, pero con *lParam* establecido en **null**; de lo contrario, se producirá una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="89494-117">After using this message to format a range of text, it is important that you free cached information by sending **EM\_FORMATRANGE** again, but with *lParam* set to **NULL**; otherwise, a memory leak will occur.</span></span> <span data-ttu-id="89494-118">Además, después de usar este mensaje para un dispositivo, debe liberar la información almacenada en caché antes de utilizarla de nuevo para un dispositivo diferente.</span><span class="sxs-lookup"><span data-stu-id="89494-118">Also, after using this message for one device, you must free cached information before using it again for a different device.</span></span>

## <a name="requirements"></a><span data-ttu-id="89494-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89494-119">Requirements</span></span>



| <span data-ttu-id="89494-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="89494-120">Requirement</span></span> | <span data-ttu-id="89494-121">Value</span><span class="sxs-lookup"><span data-stu-id="89494-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89494-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89494-122">Minimum supported client</span></span><br/> | <span data-ttu-id="89494-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="89494-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89494-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89494-124">Minimum supported server</span></span><br/> | <span data-ttu-id="89494-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="89494-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89494-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89494-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="89494-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="89494-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89494-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="89494-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="89494-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="89494-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="89494-130">**\_DISPLAYBAND em**</span><span class="sxs-lookup"><span data-stu-id="89494-130">**EM\_DISPLAYBAND**</span></span>](em-displayband.md)
</dt> <dt>

<span data-ttu-id="89494-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="89494-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="89494-132">Imprimir controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="89494-132">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

 





