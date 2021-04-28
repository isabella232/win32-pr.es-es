---
title: EM_FINDTEXTW mensaje (Richedit.h)
description: 'EM_FINDTEXTW mensaje: busca texto Unicode dentro de un control de edición enriquecido.'
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- EM_FINDTEXTW mensaje Controles de Windows
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
ms.openlocfilehash: 325ff948c4c8f03e8051248f15928d8e8c56e52f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109803"
---
# <a name="em_findtextw-message"></a><span data-ttu-id="4d16e-104">Mensaje \_ EM FINDTEXTW</span><span class="sxs-lookup"><span data-stu-id="4d16e-104">EM\_FINDTEXTW message</span></span>

<span data-ttu-id="4d16e-105">Busca texto Unicode dentro de un control de edición enriquecido.</span><span class="sxs-lookup"><span data-stu-id="4d16e-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4d16e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d16e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d16e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d16e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d16e-108">Especifica los parámetros de la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4d16e-108">Specifies the parameters of the search operation.</span></span> <span data-ttu-id="4d16e-109">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4d16e-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="4d16e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="4d16e-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="4d16e-111">Significado</span><span class="sxs-lookup"><span data-stu-id="4d16e-111">Meaning</span></span>                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="4d16e-112"><dt>**FR \_ DOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="4d16e-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="4d16e-113">Si se establece, la operación busca desde el final de la selección actual hasta el final del documento.</span><span class="sxs-lookup"><span data-stu-id="4d16e-113">If set, the operation searches from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="4d16e-114">Si no se establece, la operación busca desde el final de la selección actual hasta el principio del documento.</span><span class="sxs-lookup"><span data-stu-id="4d16e-114">If not set, the operation searches from the end of the current selection to the beginning of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="4d16e-115"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="4d16e-115"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="4d16e-116">De forma predeterminada, los alefs árabe y hebreo con acentos diferentes coinciden con el carácter alef.</span><span class="sxs-lookup"><span data-stu-id="4d16e-116">By default, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <span data-ttu-id="4d16e-117">Establezca esta marca si desea que la búsqueda diferencie entre los alefs con acentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="4d16e-117">Set this flag if you want the search to differentiate between alefs with different accents.</span></span><br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="4d16e-118"><dt>**FR \_ MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="4d16e-118"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="4d16e-119">Si se establece, la operación de búsqueda distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4d16e-119">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="4d16e-120">Si no se establece, la operación de búsqueda no tiene en cuenta mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4d16e-120">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="4d16e-121"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="4d16e-121"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="4d16e-122">De forma predeterminada, se omiten las marcas diacríticas en árabe y hebreo.</span><span class="sxs-lookup"><span data-stu-id="4d16e-122">By default, Arabic and Hebrew diacritical marks are ignored.</span></span> <span data-ttu-id="4d16e-123">Establezca esta marca si desea que la operación de búsqueda tenga en cuenta las marcas diacríticas.</span><span class="sxs-lookup"><span data-stu-id="4d16e-123">Set this flag if you want the search operation to consider diacritical marks.</span></span><br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="4d16e-124"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="4d16e-124"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="4d16e-125">De forma predeterminada, se omiten los kashidas en árabe y hebreo.</span><span class="sxs-lookup"><span data-stu-id="4d16e-125">By default, Arabic and Hebrew kashidas are ignored.</span></span> <span data-ttu-id="4d16e-126">Establezca esta marca si desea que la operación de búsqueda considere kashidas.</span><span class="sxs-lookup"><span data-stu-id="4d16e-126">Set this flag if you want the search operation to consider kashidas.</span></span><br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="4d16e-127"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="4d16e-127"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="4d16e-128">Si se establece, la operación busca solo palabras enteras que coincidan con la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4d16e-128">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="4d16e-129">Si no se establece, la operación también busca fragmentos de palabras que coincidan con la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4d16e-129">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                  |



 

</dd> <dt>

<span data-ttu-id="4d16e-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d16e-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d16e-131">Estructura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) que contiene información sobre la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4d16e-131">A [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d16e-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d16e-132">Return value</span></span>

<span data-ttu-id="4d16e-133">Si se encuentra la cadena de destino, el valor devuelto es la posición de base cero del primer carácter de la coincidencia.</span><span class="sxs-lookup"><span data-stu-id="4d16e-133">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="4d16e-134">Si no se encuentra el destino, el valor devuelto es -1.</span><span class="sxs-lookup"><span data-stu-id="4d16e-134">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d16e-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d16e-135">Remarks</span></span>

<span data-ttu-id="4d16e-136">**EM \_ FINDTEXTW usa** la [**estructura FINDTEXTW,**](/windows/win32/api/richedit/ns-richedit-findtexta) mientras [**que EM \_ FINDTEXTEXW**](em-findtextexw.md) usa la [**estructura FINDTEXTEXW.**](/windows/desktop/api/Richedit/ns-richedit-findtextexa)</span><span class="sxs-lookup"><span data-stu-id="4d16e-136">**EM\_FINDTEXTW** uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure, while [**EM\_FINDTEXTEXW**](em-findtextexw.md) uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure.</span></span> <span data-ttu-id="4d16e-137">La diferencia es que **FINDTEXTEXW informa** del intervalo de texto que se encontró.</span><span class="sxs-lookup"><span data-stu-id="4d16e-137">The difference is that **FINDTEXTEXW** reports back the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d16e-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d16e-138">Requirements</span></span>



| <span data-ttu-id="4d16e-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d16e-139">Requirement</span></span> | <span data-ttu-id="4d16e-140">Valor</span><span class="sxs-lookup"><span data-stu-id="4d16e-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d16e-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d16e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4d16e-142">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d16e-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4d16e-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d16e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4d16e-144">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d16e-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d16e-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d16e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d16e-146"><dt>Richedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="4d16e-146"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d16e-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4d16e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d16e-148">**EM \_ FINDTEXTEXW**</span><span class="sxs-lookup"><span data-stu-id="4d16e-148">**EM\_FINDTEXTEXW**</span></span>](em-findtextexw.md)
</dt> </dl>

 

 





