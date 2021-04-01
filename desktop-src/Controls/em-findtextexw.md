---
title: Mensaje EM_FINDTEXTEXW (RichEdit. h)
description: Busca texto Unicode dentro de un control Rich Edit.
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- EM_FINDTEXTEXW controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTEXW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf0857e47c6e98f4be6867ca66baef3472766a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996930"
---
# <a name="em_findtextexw-message"></a><span data-ttu-id="f2642-104">\_Mensaje FINDTEXTEXW em</span><span class="sxs-lookup"><span data-stu-id="f2642-104">EM\_FINDTEXTEXW message</span></span>

<span data-ttu-id="f2642-105">Busca texto Unicode dentro de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f2642-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2642-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2642-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2642-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2642-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2642-108">Especifica el comportamiento de la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f2642-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="f2642-109">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f2642-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="f2642-110">Value</span><span class="sxs-lookup"><span data-stu-id="f2642-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="f2642-111">Significado</span><span class="sxs-lookup"><span data-stu-id="f2642-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="f2642-112"><dt>**Francés \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f2642-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="f2642-113">Microsoft Rich Edit 2,0 y versiones posteriores: si se establece, la búsqueda se realiza hacia delante desde **FINDTEXTEX. CTA. cpMin**; Si no se establece, la búsqueda se realiza hacia atrás desde **FINDTEXTEX. CTA. cpMin**.</span><span class="sxs-lookup"><span data-stu-id="f2642-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="f2642-114">Microsoft Rich Edit 1,0: \_ se omite la marca fr Down.</span><span class="sxs-lookup"><span data-stu-id="f2642-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="f2642-115">La búsqueda siempre se reenvía.</span><span class="sxs-lookup"><span data-stu-id="f2642-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="f2642-116"><dt>**MATCHALEFHAMZA de FR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f2642-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="f2642-117">Si se establece, la búsqueda distingue entre alefs con diferentes acentos.</span><span class="sxs-lookup"><span data-stu-id="f2642-117">If set, the search differentiates between alefs with different accents.</span></span> <span data-ttu-id="f2642-118">Si no se establece, el carácter Alef coincide con los alefs árabes y hebreos con acentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="f2642-118">If not set, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="f2642-119"><dt>**\_MATCHCASE MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="f2642-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="f2642-120">Si se establece, la operación de búsqueda distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f2642-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="f2642-121">Si no se establece, la operación de búsqueda no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f2642-121">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="f2642-122"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="f2642-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="f2642-123">Si se establece, la operación de búsqueda tiene en cuenta las marcas diacríticas.</span><span class="sxs-lookup"><span data-stu-id="f2642-123">If set, the search operation considers diacritical marks.</span></span> <span data-ttu-id="f2642-124">Si no se establece, se omiten las marcas diacríticas árabe y hebreo.</span><span class="sxs-lookup"><span data-stu-id="f2642-124">If not set, Arabic and Hebrew diacritical marks are ignored.</span></span> <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="f2642-125"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="f2642-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="f2642-126">Si se establece, la operación de búsqueda tiene en cuenta kashidas.</span><span class="sxs-lookup"><span data-stu-id="f2642-126">If set, the search operation considers kashidas.</span></span> <span data-ttu-id="f2642-127">Si no se establece, se omiten los kashidas en árabe y hebreo.</span><span class="sxs-lookup"><span data-stu-id="f2642-127">If not set, Arabic and Hebrew kashidas are ignored.</span></span> <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="f2642-128"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="f2642-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="f2642-129">Si se establece, la operación busca solo palabras completas que coincidan con la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f2642-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="f2642-130">Si no se establece, la operación también busca fragmentos de palabras que coincidan con la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f2642-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="f2642-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2642-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2642-132">Estructura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) que contiene información sobre la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f2642-132">A [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2642-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2642-133">Return value</span></span>

<span data-ttu-id="f2642-134">Si se encuentra la cadena de destino, el valor devuelto es la posición de base cero del primer carácter de la coincidencia.</span><span class="sxs-lookup"><span data-stu-id="f2642-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="f2642-135">Si no se encuentra el destino, el valor devuelto es-1.</span><span class="sxs-lookup"><span data-stu-id="f2642-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2642-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2642-136">Remarks</span></span>

<span data-ttu-id="f2642-137">Use este mensaje para buscar cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="f2642-137">Use this message to find Unicode strings.</span></span> <span data-ttu-id="f2642-138">Para ANSI;, use [**em \_ FINDTEXTEX**](em-findtextex.md).</span><span class="sxs-lookup"><span data-stu-id="f2642-138">For ANSI;, use [**EM\_FINDTEXTEX**](em-findtextex.md).</span></span>

<span data-ttu-id="f2642-139">El miembro **cpMin** de **FINDTEXTEX. CTA** siempre especifica el punto inicial de la búsqueda y **cpMax** especifica el punto final.</span><span class="sxs-lookup"><span data-stu-id="f2642-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="f2642-140">Al buscar hacia atrás, **cpMin** debe ser igual o mayor que **cpMax**.</span><span class="sxs-lookup"><span data-stu-id="f2642-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="f2642-141">Al buscar hacia delante, un valor de-1 en **cpMax** extiende el intervalo de búsqueda al final del texto.</span><span class="sxs-lookup"><span data-stu-id="f2642-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="f2642-142">Si la operación de búsqueda encuentra una coincidencia, el miembro **chrgText** de la estructura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) devuelve el intervalo de posiciones de caracteres que contiene el texto coincidente.</span><span class="sxs-lookup"><span data-stu-id="f2642-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

<span data-ttu-id="f2642-143">**Em \_ FINDTEXTEXW** usa la estructura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , mientras que [**em \_ FINDTEXTW**](em-findtextw.md) usa la estructura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) .</span><span class="sxs-lookup"><span data-stu-id="f2642-143">**EM\_FINDTEXTEXW** uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, while [**EM\_FINDTEXTW**](em-findtextw.md) uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure.</span></span> <span data-ttu-id="f2642-144">La diferencia es que **em \_ FINDTEXTEXW** informa del intervalo de texto que se encontró.</span><span class="sxs-lookup"><span data-stu-id="f2642-144">The difference is that **EM\_FINDTEXTEXW** reports the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2642-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2642-145">Requirements</span></span>



| <span data-ttu-id="f2642-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2642-146">Requirement</span></span> | <span data-ttu-id="f2642-147">Value</span><span class="sxs-lookup"><span data-stu-id="f2642-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2642-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2642-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f2642-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f2642-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2642-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2642-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f2642-151">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2642-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2642-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2642-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2642-153"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2642-153"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2642-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2642-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2642-155">**\_FINDTEXTW em**</span><span class="sxs-lookup"><span data-stu-id="f2642-155">**EM\_FINDTEXTW**</span></span>](em-findtextw.md)
</dt> </dl>

 

 





