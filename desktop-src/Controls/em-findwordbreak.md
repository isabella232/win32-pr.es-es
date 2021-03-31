---
title: Mensaje EM_FINDWORDBREAK (RichEdit. h)
description: Busca el siguiente salto de palabra antes o después de la posición del carácter especificado o recupera información sobre el carácter que se encuentra en esa posición.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- EM_FINDWORDBREAK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_FINDWORDBREAK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6533358c0f4f521bc7021e290dfe11d66d4499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491014"
---
# <a name="em_findwordbreak-message"></a><span data-ttu-id="67ed1-104">\_Mensaje FINDWORDBREAK em</span><span class="sxs-lookup"><span data-stu-id="67ed1-104">EM\_FINDWORDBREAK message</span></span>

<span data-ttu-id="67ed1-105">Busca el siguiente salto de palabra antes o después de la posición del carácter especificado o recupera información sobre el carácter que se encuentra en esa posición.</span><span class="sxs-lookup"><span data-stu-id="67ed1-105">Finds the next word break before or after the specified character position or retrieves information about the character at that position.</span></span>

## <a name="parameters"></a><span data-ttu-id="67ed1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67ed1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67ed1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67ed1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67ed1-108">Especifica la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="67ed1-108">Specifies the find operation.</span></span> <span data-ttu-id="67ed1-109">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="67ed1-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="67ed1-110">Valor</span><span class="sxs-lookup"><span data-stu-id="67ed1-110">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="67ed1-111">Significado</span><span class="sxs-lookup"><span data-stu-id="67ed1-111">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <span data-ttu-id="67ed1-112"><dt>**\_clasificación WB**</dt></span><span class="sxs-lookup"><span data-stu-id="67ed1-112"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>                | <span data-ttu-id="67ed1-113">Devuelve la clase de caracteres y las marcas de salto de palabra del carácter que se encuentra en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="67ed1-113">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <span data-ttu-id="67ed1-114"><dt>**WB \_ ISDELIMITER**</dt></span><span class="sxs-lookup"><span data-stu-id="67ed1-114"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl>       | <span data-ttu-id="67ed1-115">Devuelve **true** si el carácter que ocupa la posición especificada es un delimitador o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="67ed1-115">Returns **TRUE** if the character at the specified position is a delimiter, or **FALSE** otherwise.</span></span><br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <span data-ttu-id="67ed1-116"><dt>**WB \_ izquierda**</dt></span><span class="sxs-lookup"><span data-stu-id="67ed1-116"><dt>**WB\_LEFT**</dt></span></span> </dl>                            | <span data-ttu-id="67ed1-117">Busca el carácter más próximo delante de la posición especificada que comienza una palabra.</span><span class="sxs-lookup"><span data-stu-id="67ed1-117">Finds the nearest character before the specified position that begins a word.</span></span><br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <span data-ttu-id="67ed1-118"><dt>**WB \_ LEFTBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="67ed1-118"><dt>**WB\_LEFTBREAK**</dt></span></span> </dl>             | <span data-ttu-id="67ed1-119">Busca la siguiente palabra final antes de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="67ed1-119">Finds the next word end before the specified position.</span></span> <span data-ttu-id="67ed1-120">Este valor es el mismo que WB \_ PREVBREAK.</span><span class="sxs-lookup"><span data-stu-id="67ed1-120">This value is the same as WB\_PREVBREAK.</span></span><br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <span data-ttu-id="67ed1-121"><dt>**WB \_ MOVEWORDLEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="67ed1-121"><dt>**WB\_MOVEWORDLEFT**</dt></span></span> </dl>    | <span data-ttu-id="67ed1-122">Busca el siguiente carácter que comienza una palabra antes de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="67ed1-122">Finds the next character that begins a word before the specified position.</span></span> <span data-ttu-id="67ed1-123">Este valor se utiliza durante el procesamiento de la tecla CTRL + flecha izquierda.</span><span class="sxs-lookup"><span data-stu-id="67ed1-123">This value is used during CTRL+LEFT ARROW key processing.</span></span> <span data-ttu-id="67ed1-124">Este valor es similar a WB \_ MOVEWORDPREV.</span><span class="sxs-lookup"><span data-stu-id="67ed1-124">This value is the similar to WB\_MOVEWORDPREV.</span></span> <span data-ttu-id="67ed1-125">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="67ed1-125">See Remarks for more information.</span></span><br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <span data-ttu-id="67ed1-126"><dt>**WB \_ MOVEWORDRIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="67ed1-126"><dt>**WB\_MOVEWORDRIGHT**</dt></span></span> </dl> | <span data-ttu-id="67ed1-127">Busca el siguiente carácter que comienza una palabra después de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="67ed1-127">Finds the next character that begins a word after the specified position.</span></span> <span data-ttu-id="67ed1-128">Este valor se utiliza durante el procesamiento de la tecla CTRL + flecha derecha.</span><span class="sxs-lookup"><span data-stu-id="67ed1-128">This value is used during CTRL+right key processing.</span></span> <span data-ttu-id="67ed1-129">Este valor es similar a WB \_ MOVEWORDNEXT.</span><span class="sxs-lookup"><span data-stu-id="67ed1-129">This value is similar to WB\_MOVEWORDNEXT.</span></span> <span data-ttu-id="67ed1-130">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="67ed1-130">See Remarks for more information.</span></span><br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <span data-ttu-id="67ed1-131"><dt>**WB, \_ derecho**</dt></span><span class="sxs-lookup"><span data-stu-id="67ed1-131"><dt>**WB\_RIGHT**</dt></span></span> </dl>                         | <span data-ttu-id="67ed1-132">Busca el siguiente carácter que comienza una palabra después de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="67ed1-132">Finds the next character that begins a word after the specified position.</span></span><br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <span data-ttu-id="67ed1-133"><dt>**WB \_ RIGHTBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="67ed1-133"><dt>**WB\_RIGHTBREAK**</dt></span></span> </dl>          | <span data-ttu-id="67ed1-134">Busca el delimitador de final de palabra siguiente después de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="67ed1-134">Finds the next end-of-word delimiter after the specified position.</span></span> <span data-ttu-id="67ed1-135">Este valor es el mismo que WB \_ NEXTBREAK.</span><span class="sxs-lookup"><span data-stu-id="67ed1-135">This value is the same as WB\_NEXTBREAK.</span></span><br/>                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="67ed1-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67ed1-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67ed1-137">Posición inicial de carácter de base cero.</span><span class="sxs-lookup"><span data-stu-id="67ed1-137">Zero-based character starting position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67ed1-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67ed1-138">Return value</span></span>

<span data-ttu-id="67ed1-139">El mensaje devuelve un valor basado en el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="67ed1-139">The message returns a value based on the *wParam* parameter.</span></span>



| <span data-ttu-id="67ed1-140">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="67ed1-140">Return code</span></span>                                                                                    | <span data-ttu-id="67ed1-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="67ed1-141">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="67ed1-142"><dt>**wParam**</dt></span><span class="sxs-lookup"><span data-stu-id="67ed1-142"><dt>**wParam**</dt></span></span> </dl>          | <span data-ttu-id="67ed1-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67ed1-143">Return Value</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="67ed1-144"><dt>**\_clasificación WB**</dt></span><span class="sxs-lookup"><span data-stu-id="67ed1-144"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>    | <span data-ttu-id="67ed1-145">Devuelve la clase de caracteres y las marcas de salto de palabra del carácter que se encuentra en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="67ed1-145">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                |
| <dl> <span data-ttu-id="67ed1-146"><dt>**WB \_ ISDELIMITER**</dt></span><span class="sxs-lookup"><span data-stu-id="67ed1-146"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl> | <span data-ttu-id="67ed1-147">Devuelve **true** si el carácter que ocupa la posición especificada es un delimitador; en caso contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="67ed1-147">Returns **TRUE** if the character at the specified position is a delimiter; otherwise it returns **FALSE**.</span></span><br/> |
| <dl> <span data-ttu-id="67ed1-148"><dt>**Otros**</dt></span><span class="sxs-lookup"><span data-stu-id="67ed1-148"><dt>**Others**</dt></span></span> </dl>          | <span data-ttu-id="67ed1-149">Devuelve el índice de carácter del separador de palabras.</span><span class="sxs-lookup"><span data-stu-id="67ed1-149">Returns the character index of the word break.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="67ed1-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67ed1-150">Remarks</span></span>

<span data-ttu-id="67ed1-151">Si *wParam* es WB \_ left y WB \_ right, el procedimiento de separación de palabras busca saltos de palabra solo después de los delimitadores.</span><span class="sxs-lookup"><span data-stu-id="67ed1-151">If *wParam* is WB\_LEFT and WB\_RIGHT, the word-break procedure finds word breaks only after delimiters.</span></span> <span data-ttu-id="67ed1-152">Esto coincide con la funcionalidad de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="67ed1-152">This matches the functionality of an edit control.</span></span> <span data-ttu-id="67ed1-153">Si *wParam* es WB \_ MOVEWORDLEFT o WB \_ MOVEWORDRIGHT, el procedimiento de separación de palabras también compara las clases de caracteres y las marcas de separación de palabras.</span><span class="sxs-lookup"><span data-stu-id="67ed1-153">If *wParam* is WB\_MOVEWORDLEFT or WB\_MOVEWORDRIGHT, the word-break procedure also compares character classes and word-break flags.</span></span>

<span data-ttu-id="67ed1-154">Para obtener información sobre las clases de caracteres y las marcas de salto de línea, vea [Word y saltos de línea](using-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="67ed1-154">For information about character classes and word-break flags, see [Word and Line Breaks](using-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67ed1-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67ed1-155">Requirements</span></span>



| <span data-ttu-id="67ed1-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="67ed1-156">Requirement</span></span> | <span data-ttu-id="67ed1-157">Value</span><span class="sxs-lookup"><span data-stu-id="67ed1-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67ed1-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67ed1-158">Minimum supported client</span></span><br/> | <span data-ttu-id="67ed1-159">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="67ed1-159">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="67ed1-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67ed1-160">Minimum supported server</span></span><br/> | <span data-ttu-id="67ed1-161">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="67ed1-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67ed1-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67ed1-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="67ed1-163"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="67ed1-163"><dt>Richedit.h</dt></span></span> </dl> |



 

 





