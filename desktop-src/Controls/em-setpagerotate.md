---
title: Mensaje EM_SETPAGEROTATE (RichEdit. h)
description: Establece el diseño de texto para un control Rich Edit.
ms.assetid: 3c2a37fe-ee9f-4b34-87bf-7ac27d010afc
keywords:
- EM_SETPAGEROTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eb595456bca444c92b536b0e428ee56a5903ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996291"
---
# <a name="em_setpagerotate-message"></a><span data-ttu-id="59ab3-104">\_Mensaje SETPAGEROTATE em</span><span class="sxs-lookup"><span data-stu-id="59ab3-104">EM\_SETPAGEROTATE message</span></span>

<span data-ttu-id="59ab3-105">\[**Em \_ SETPAGEROTATE** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="59ab3-105">\[**EM\_SETPAGEROTATE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="59ab3-106">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="59ab3-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="59ab3-107">Establece el diseño de texto para un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="59ab3-107">Sets the text layout for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="59ab3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59ab3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59ab3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59ab3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59ab3-110">Valor de diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="59ab3-110">Text layout value.</span></span> <span data-ttu-id="59ab3-111">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="59ab3-111">This can be one of the following values.</span></span>



| <span data-ttu-id="59ab3-112">Value</span><span class="sxs-lookup"><span data-stu-id="59ab3-112">Value</span></span>                                                                                                                                       | <span data-ttu-id="59ab3-113">Significado</span><span class="sxs-lookup"><span data-stu-id="59ab3-113">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="EPR_0"></span><span id="epr_0"></span><dl> <span data-ttu-id="59ab3-114"><dt>**EPR \_ 0**</dt></span><span class="sxs-lookup"><span data-stu-id="59ab3-114"><dt>**EPR\_0**</dt></span></span> </dl>       | <span data-ttu-id="59ab3-115">El texto fluye de izquierda a derecha y de arriba a abajo.</span><span class="sxs-lookup"><span data-stu-id="59ab3-115">Text flows from left to right and from top to bottom.</span></span><br/>                              |
| <span id="EPR_90"></span><span id="epr_90"></span><dl> <span data-ttu-id="59ab3-116"><dt>**EPR \_ 90**</dt></span><span class="sxs-lookup"><span data-stu-id="59ab3-116"><dt>**EPR\_90**</dt></span></span> </dl>    | <span data-ttu-id="59ab3-117">El texto fluye de abajo a arriba y de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="59ab3-117">Text flows from bottom to top and from left to right.</span></span><br/>                              |
| <span id="EPR_180"></span><span id="epr_180"></span><dl> <span data-ttu-id="59ab3-118"><dt>**EPR \_ 180**</dt></span><span class="sxs-lookup"><span data-stu-id="59ab3-118"><dt>**EPR\_180**</dt></span></span> </dl> | <span data-ttu-id="59ab3-119">El texto fluye de derecha a izquierda y de abajo a arriba.</span><span class="sxs-lookup"><span data-stu-id="59ab3-119">Text flows from right to left and from bottom to top.</span></span><br/>                              |
| <span id="EPR_270"></span><span id="epr_270"></span><dl> <span data-ttu-id="59ab3-120"><dt>**EPR \_ 270**</dt></span><span class="sxs-lookup"><span data-stu-id="59ab3-120"><dt>**EPR\_270**</dt></span></span> </dl> | <span data-ttu-id="59ab3-121">El texto fluye de arriba abajo y de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="59ab3-121">Text flows from top to bottom and from right to left.</span></span><br/>                              |
| <span id="EPR_SE"></span><span id="epr_se"></span><dl> <span data-ttu-id="59ab3-122"><dt>**EPR \_ se**</dt></span><span class="sxs-lookup"><span data-stu-id="59ab3-122"><dt>**EPR\_SE**</dt></span></span> </dl>    | <span data-ttu-id="59ab3-123">**Windows 8:** El texto fluye de arriba abajo y de izquierda a derecha (diseño de texto mongol).</span><span class="sxs-lookup"><span data-stu-id="59ab3-123">**Windows 8:** Text flows top to bottom and left to right (Mongolian text layout).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="59ab3-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59ab3-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59ab3-125">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="59ab3-125">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59ab3-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59ab3-126">Return value</span></span>

<span data-ttu-id="59ab3-127">El valor devuelto es el nuevo valor de diseño de texto.</span><span class="sxs-lookup"><span data-stu-id="59ab3-127">Return value is the new text layout value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59ab3-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59ab3-128">Remarks</span></span>

<span data-ttu-id="59ab3-129">Este mensaje establece el diseño del texto para todo el documento.</span><span class="sxs-lookup"><span data-stu-id="59ab3-129">This message sets the text layout for the entire document.</span></span> <span data-ttu-id="59ab3-130">Sin embargo, el contenido incrustado no se gira y se debe girar por separado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="59ab3-130">However, embedded contents are not rotated and must be rotated separately by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ab3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59ab3-131">Requirements</span></span>



| <span data-ttu-id="59ab3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="59ab3-132">Requirement</span></span> | <span data-ttu-id="59ab3-133">Value</span><span class="sxs-lookup"><span data-stu-id="59ab3-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59ab3-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59ab3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="59ab3-135">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="59ab3-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59ab3-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59ab3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="59ab3-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="59ab3-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59ab3-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59ab3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="59ab3-139"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="59ab3-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59ab3-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="59ab3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ab3-141">**\_GETPAGEROTATE em**</span><span class="sxs-lookup"><span data-stu-id="59ab3-141">**EM\_GETPAGEROTATE**</span></span>](em-getpagerotate.md)
</dt> </dl>

 

 





