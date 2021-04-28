---
title: EM_FINDTEXTEX mensaje (Richedit.h)
description: 'EM_FINDTEXTEX mensaje: busca texto dentro de un control de edición enriquecido.'
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- EM_FINDTEXTEX de mensajes controles de Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2158dabf9ea17d1bd4cac48454bdbb4056765752
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109843"
---
# <a name="em_findtextex-message"></a><span data-ttu-id="d7a6c-104">Mensaje \_ EM FINDTEXTEX</span><span class="sxs-lookup"><span data-stu-id="d7a6c-104">EM\_FINDTEXTEX message</span></span>

<span data-ttu-id="d7a6c-105">Busca texto dentro de un control de edición enriquecido.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7a6c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7a6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7a6c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7a6c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7a6c-108">Especifica el comportamiento de la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="d7a6c-109">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="d7a6c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d7a6c-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="d7a6c-111">Significado</span><span class="sxs-lookup"><span data-stu-id="d7a6c-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="d7a6c-112"><dt>**FR \_ DOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a6c-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="d7a6c-113">Microsoft Rich Edit 2.0 y versiones posteriores: si se establece, la búsqueda se reenvía desde **FINDTEXTEX.chrg.cpMin**; Si no se establece, la búsqueda se hace hacia atrás desde **FINDTEXTEX.chrg.cpMin**.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="d7a6c-114">Microsoft Rich Edit 1.0: se omite la marca FR \_ DOWN.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="d7a6c-115">La búsqueda siempre es hacia delante.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="d7a6c-116"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a6c-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="d7a6c-117">Microsoft Rich Edit 3.0 y versiones posteriores: si se establece, la búsqueda diferencia entre los alefs árabe y hebreo con acentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-117">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic and Hebrew alefs with different accents.</span></span> <span data-ttu-id="d7a6c-118">Si no se establece, el carácter alef coincide solo con todos los alef.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-118">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="d7a6c-119"><dt>**FR \_ MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a6c-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="d7a6c-120">Si se establece, la operación de búsqueda distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="d7a6c-121">Si no se establece, la operación de búsqueda no tiene en cuenta las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-121">If not set, the search operation is case-insensitive.</span></span> <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="d7a6c-122"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a6c-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="d7a6c-123">Microsoft Rich Edit 3.0 y versiones posteriores: si se establece, la operación de búsqueda considera marcas diacríticas en árabe y hebreo.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-123">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="d7a6c-124">Si no se establece, se omiten las marcas diacríticas.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-124">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="d7a6c-125"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a6c-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="d7a6c-126">Microsoft Rich Edit 3.0 y versiones posteriores: si se establece, la operación de búsqueda considera kashidas en árabe y hebreo.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-126">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew kashidas.</span></span> <span data-ttu-id="d7a6c-127">Si no se establece, se omiten los kashidas.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-127">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="d7a6c-128"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a6c-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="d7a6c-129">Si se establece, la operación busca solo palabras enteras que coincidan con la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="d7a6c-130">Si no se establece, la operación también busca fragmentos de palabras que coincidan con la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="d7a6c-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7a6c-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7a6c-132">Estructura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) que contiene información sobre la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-132">A [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7a6c-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7a6c-133">Return value</span></span>

<span data-ttu-id="d7a6c-134">Si se encuentra la cadena de destino, el valor devuelto es la posición de base cero del primer carácter de la coincidencia.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="d7a6c-135">Si no se encuentra el destino, el valor devuelto es -1.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7a6c-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7a6c-136">Remarks</span></span>

<span data-ttu-id="d7a6c-137">Use este mensaje para buscar cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-137">Use this message to find ANSI strings.</span></span> <span data-ttu-id="d7a6c-138">Para Unicode, use [**EM \_ FINDTEXTEXW**](em-findtextexw.md).</span><span class="sxs-lookup"><span data-stu-id="d7a6c-138">For Unicode, use [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span>

<span data-ttu-id="d7a6c-139">El **miembro cpMin** de **FINDTEXTEX.chrg** siempre especifica el punto inicial de la búsqueda y **cpMax** especifica el punto final.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="d7a6c-140">Al buscar hacia atrás, **cpMin** debe ser igual o mayor que **cpMax.**</span><span class="sxs-lookup"><span data-stu-id="d7a6c-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="d7a6c-141">Al buscar hacia delante, un valor de -1 en **cpMax** amplía el intervalo de búsqueda hasta el final del texto.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="d7a6c-142">Si la operación de búsqueda encuentra una coincidencia, el miembro **chrgText** de la estructura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) devuelve el intervalo de posiciones de caracteres que contiene el texto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d7a6c-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7a6c-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7a6c-143">Requirements</span></span>



| <span data-ttu-id="d7a6c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7a6c-144">Requirement</span></span> | <span data-ttu-id="d7a6c-145">Valor</span><span class="sxs-lookup"><span data-stu-id="d7a6c-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a6c-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7a6c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a6c-147">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7a6c-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7a6c-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7a6c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a6c-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7a6c-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7a6c-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7a6c-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7a6c-151"><dt>Richedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a6c-151"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7a6c-152">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d7a6c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a6c-153">**EM \_ FINDTEXT**</span><span class="sxs-lookup"><span data-stu-id="d7a6c-153">**EM\_FINDTEXT**</span></span>](em-findtext.md)
</dt> </dl>

 

 





