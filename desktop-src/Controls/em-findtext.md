---
title: Mensaje EM_FINDTEXT (RichEdit. h)
description: Busca texto dentro de un control Rich Edit.
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- EM_FINDTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e50034337f05d2df17af777986136881c503d05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996568"
---
# <a name="em_findtext-message"></a><span data-ttu-id="1fbe0-104">\_Mensaje TEXTOBUSCADO em</span><span class="sxs-lookup"><span data-stu-id="1fbe0-104">EM\_FINDTEXT message</span></span>

<span data-ttu-id="1fbe0-105">Busca texto dentro de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1fbe0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fbe0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fbe0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1fbe0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fbe0-108">Especifique los parámetros de la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-108">Specify the parameters of the search operation.</span></span> <span data-ttu-id="1fbe0-109">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="1fbe0-110">Value</span><span class="sxs-lookup"><span data-stu-id="1fbe0-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="1fbe0-111">Significado</span><span class="sxs-lookup"><span data-stu-id="1fbe0-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="1fbe0-112"><dt>**Francés \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1fbe0-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="1fbe0-113">Microsoft Rich Edit 2,0 y versiones posteriores: si se establece, la búsqueda se realiza desde el final de la selección actual hasta el final del documento.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-113">Microsoft Rich Edit 2.0 and later: If set, the search is from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="1fbe0-114">Si no se establece, la búsqueda se realiza desde el final de la selección actual hasta el principio del documento.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-114">If not set, the search is from the end of the current selection to the beginning of the document.</span></span> <br/> <span data-ttu-id="1fbe0-115">Microsoft Rich Edit 1,0: \_ se omite la marca fr Down.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-115">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="1fbe0-116">La búsqueda siempre va desde el final de la selección actual hasta el final del documento.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-116">The search is always from the end of the current selection to the end of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="1fbe0-117"><dt>**MATCHALEFHAMZA de FR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1fbe0-117"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="1fbe0-118">Microsoft Rich Edit 3,0 y versiones posteriores: si se establece, la búsqueda distingue entre alefs árabes con diferentes acentos.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-118">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic alefs with different accents.</span></span> <span data-ttu-id="1fbe0-119">Si no se establece, todos los alefs solo coinciden con el carácter Alef.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-119">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="1fbe0-120"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="1fbe0-120"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="1fbe0-121">Microsoft Rich Edit 3,0 y versiones posteriores: si se establece, la operación de búsqueda tiene en cuenta las marcas diacríticas árabe y hebreo.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-121">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="1fbe0-122">Si no se establece, se omiten las marcas diacríticas.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-122">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="1fbe0-123"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="1fbe0-123"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="1fbe0-124">Microsoft Rich Edit 3,0 y versiones posteriores: si se establece, la operación de búsqueda considera kashidas árabes.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-124">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic kashidas.</span></span> <span data-ttu-id="1fbe0-125">Si no se establece, se omiten los kashidas.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-125">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <span data-ttu-id="1fbe0-126"><dt>**FR \_ MATCHWIDTH**</dt></span><span class="sxs-lookup"><span data-stu-id="1fbe0-126"><dt>**FR\_MATCHWIDTH**</dt></span></span> </dl>             | <span data-ttu-id="1fbe0-127">Windows 8: si se establece, se considera que las versiones de un solo byte y de doble byte del mismo carácter no son iguales.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-127">Windows 8: If set, single-byte and double-byte versions of the same character are considered to be not equal.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="1fbe0-128"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="1fbe0-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="1fbe0-129">Si se establece, la operación busca solo palabras completas que coincidan con la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="1fbe0-130">Si no se establece, la operación también busca fragmentos de palabras que coincidan con la cadena de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="1fbe0-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1fbe0-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fbe0-132">Una estructura [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) que contiene información sobre la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-132">A [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fbe0-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fbe0-133">Return value</span></span>

<span data-ttu-id="1fbe0-134">Si se encuentra la cadena de destino, el valor devuelto es la posición de base cero del primer carácter de la coincidencia.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="1fbe0-135">Si no se encuentra el destino, el valor devuelto es-1.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fbe0-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1fbe0-136">Remarks</span></span>

<span data-ttu-id="1fbe0-137">El miembro **cpMin** de **FINDTEXT. CTA** siempre especifica el punto inicial de la búsqueda y **cpMax** especifica el punto final.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-137">The **cpMin** member of **FINDTEXT.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="1fbe0-138">Al buscar hacia atrás, **cpMin** debe ser igual o mayor que **cpMax**.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-138">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="1fbe0-139">Al buscar hacia delante, un valor de-1 en **cpMax** extiende el intervalo de búsqueda al final del texto.</span><span class="sxs-lookup"><span data-stu-id="1fbe0-139">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fbe0-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fbe0-140">Requirements</span></span>



| <span data-ttu-id="1fbe0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fbe0-141">Requirement</span></span> | <span data-ttu-id="1fbe0-142">Value</span><span class="sxs-lookup"><span data-stu-id="1fbe0-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fbe0-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fbe0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1fbe0-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1fbe0-144">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1fbe0-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fbe0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1fbe0-146">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fbe0-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1fbe0-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fbe0-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fbe0-148"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fbe0-148"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fbe0-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fbe0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fbe0-150">**FINDTEXT**</span><span class="sxs-lookup"><span data-stu-id="1fbe0-150">**FINDTEXT**</span></span>](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





