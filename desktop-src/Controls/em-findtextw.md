---
title: Mensaje EM_FINDTEXTW (RichEdit. h)
description: Busca texto Unicode dentro de un control Rich Edit.
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- EM_FINDTEXTW controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bae60269ab3ddb84a17c285c243e00d8117c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803271"
---
# <a name="em_findtextw-message"></a><span data-ttu-id="5d889-104">\_Mensaje FINDTEXTW em</span><span class="sxs-lookup"><span data-stu-id="5d889-104">EM\_FINDTEXTW message</span></span>

<span data-ttu-id="5d889-105">Busca texto Unicode dentro de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="5d889-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d889-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d889-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d889-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d889-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d889-108">Especifica los parámetros de la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5d889-108">Specifies the parameters of the search operation.</span></span> <span data-ttu-id="5d889-109">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5d889-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="5d889-110">Value</span><span class="sxs-lookup"><span data-stu-id="5d889-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="5d889-111">Significado</span><span class="sxs-lookup"><span data-stu-id="5d889-111">Meaning</span></span>                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="5d889-112"><dt>**Francés \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d889-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="5d889-113">Si se establece, la operación busca desde el final de la selección actual hasta el final del documento.</span><span class="sxs-lookup"><span data-stu-id="5d889-113">If set, the operation searches from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="5d889-114">Si no se establece, la operación busca desde el final de la selección actual hasta el principio del documento.</span><span class="sxs-lookup"><span data-stu-id="5d889-114">If not set, the operation searches from the end of the current selection to the beginning of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="5d889-115"><dt>**MATCHALEFHAMZA de FR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d889-115"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="5d889-116">De forma predeterminada, los alefs árabe y hebreo con diferentes acentos coinciden con el carácter Alef.</span><span class="sxs-lookup"><span data-stu-id="5d889-116">By default, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <span data-ttu-id="5d889-117">Establezca esta marca si desea que la búsqueda distinga entre alefs con distintos acentos.</span><span class="sxs-lookup"><span data-stu-id="5d889-117">Set this flag if you want the search to differentiate between alefs with different accents.</span></span><br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="5d889-118"><dt>**\_MATCHCASE MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="5d889-118"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="5d889-119">Si se establece, la operación de búsqueda distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5d889-119">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="5d889-120">Si no se establece, la operación de búsqueda no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5d889-120">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="5d889-121"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="5d889-121"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="5d889-122">De forma predeterminada, se omiten las marcas diacríticas árabe y hebreo.</span><span class="sxs-lookup"><span data-stu-id="5d889-122">By default, Arabic and Hebrew diacritical marks are ignored.</span></span> <span data-ttu-id="5d889-123">Establezca esta marca si desea que la operación de búsqueda considere las marcas diacríticas.</span><span class="sxs-lookup"><span data-stu-id="5d889-123">Set this flag if you want the search operation to consider diacritical marks.</span></span><br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="5d889-124"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="5d889-124"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="5d889-125">De forma predeterminada, se omiten los kashidas árabe y hebreo.</span><span class="sxs-lookup"><span data-stu-id="5d889-125">By default, Arabic and Hebrew kashidas are ignored.</span></span> <span data-ttu-id="5d889-126">Establezca esta marca si desea que la operación de búsqueda considere kashidas.</span><span class="sxs-lookup"><span data-stu-id="5d889-126">Set this flag if you want the search operation to consider kashidas.</span></span><br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="5d889-127"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="5d889-127"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="5d889-128">Si se establece, la operación busca solo palabras completas que coincidan con la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5d889-128">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="5d889-129">Si no se establece, la operación también busca fragmentos de palabras que coincidan con la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5d889-129">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                  |



 

</dd> <dt>

<span data-ttu-id="5d889-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d889-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d889-131">Estructura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) que contiene información sobre la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5d889-131">A [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d889-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d889-132">Return value</span></span>

<span data-ttu-id="5d889-133">Si se encuentra la cadena de destino, el valor devuelto es la posición de base cero del primer carácter de la coincidencia.</span><span class="sxs-lookup"><span data-stu-id="5d889-133">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="5d889-134">Si no se encuentra el destino, el valor devuelto es-1.</span><span class="sxs-lookup"><span data-stu-id="5d889-134">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d889-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d889-135">Remarks</span></span>

<span data-ttu-id="5d889-136">**Em \_ FINDTEXTW** usa la estructura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) , mientras que [**em \_ FINDTEXTEXW**](em-findtextexw.md) usa la estructura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) .</span><span class="sxs-lookup"><span data-stu-id="5d889-136">**EM\_FINDTEXTW** uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure, while [**EM\_FINDTEXTEXW**](em-findtextexw.md) uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure.</span></span> <span data-ttu-id="5d889-137">La diferencia es que **FINDTEXTEXW** devuelve el intervalo de texto que se encontró.</span><span class="sxs-lookup"><span data-stu-id="5d889-137">The difference is that **FINDTEXTEXW** reports back the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d889-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d889-138">Requirements</span></span>



| <span data-ttu-id="5d889-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d889-139">Requirement</span></span> | <span data-ttu-id="5d889-140">Value</span><span class="sxs-lookup"><span data-stu-id="5d889-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d889-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d889-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5d889-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5d889-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d889-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d889-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5d889-144">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5d889-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d889-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d889-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d889-146"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d889-146"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d889-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d889-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d889-148">**\_FINDTEXTEXW em**</span><span class="sxs-lookup"><span data-stu-id="5d889-148">**EM\_FINDTEXTEXW**</span></span>](em-findtextexw.md)
</dt> </dl>

 

 





