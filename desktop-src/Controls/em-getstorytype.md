---
title: Mensaje EM_GETSTORYTYPE (RichEdit. h)
description: Obtiene el tipo de caso.
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- EM_GETSTORYTYPE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fed85183f292bd1c69e3bbebdadb4b38f9f3bdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905200"
---
# <a name="em_getstorytype-message"></a><span data-ttu-id="76419-104">\_Mensaje GETSTORYTYPE em</span><span class="sxs-lookup"><span data-stu-id="76419-104">EM\_GETSTORYTYPE message</span></span>

<span data-ttu-id="76419-105">Obtiene el tipo de caso.</span><span class="sxs-lookup"><span data-stu-id="76419-105">Gets the story type.</span></span>


```C++
#define EM_GETSTORYTYPE       (WM_USER + 290)
```



## <a name="parameters"></a><span data-ttu-id="76419-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76419-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76419-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76419-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76419-108">Índice del caso.</span><span class="sxs-lookup"><span data-stu-id="76419-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="76419-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76419-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76419-110">Sector debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="76419-110">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76419-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76419-111">Return value</span></span>

<span data-ttu-id="76419-112">Devuelve el tipo de caso, que puede ser un valor personalizado definido por el cliente, o uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="76419-112">Returns the story type, which can be a client-defined custom value, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="76419-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="76419-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="76419-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="76419-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76419-128">Requirements</span></span>



| <span data-ttu-id="76419-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="76419-129">Requirement</span></span> | <span data-ttu-id="76419-130">Value</span><span class="sxs-lookup"><span data-stu-id="76419-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76419-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76419-131">Minimum supported client</span></span><br/> | <span data-ttu-id="76419-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="76419-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="76419-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76419-133">Minimum supported server</span></span><br/> | <span data-ttu-id="76419-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="76419-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76419-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76419-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="76419-136"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="76419-136"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76419-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="76419-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76419-138">**\_SETSTORYTYPE em**</span><span class="sxs-lookup"><span data-stu-id="76419-138">**EM\_SETSTORYTYPE**</span></span>](em-setstorytype.md)
</dt> <dt>

[<span data-ttu-id="76419-139">**ITextStoryRanges:: Item**</span><span class="sxs-lookup"><span data-stu-id="76419-139">**ITextStoryRanges::Item**</span></span>](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





