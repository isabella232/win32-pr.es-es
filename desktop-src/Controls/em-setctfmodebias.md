---
title: Mensaje EM_SETCTFMODEBIAS (RichEdit. h)
description: Establece la diferencia del modo de Text Services Framework (TSF) para un control Rich Edit.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- EM_SETCTFMODEBIAS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b872fa5489c898ec4482ecdc094de7df6e3180be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535061"
---
# <a name="em_setctfmodebias-message"></a><span data-ttu-id="74256-104">\_Mensaje SETCTFMODEBIAS em</span><span class="sxs-lookup"><span data-stu-id="74256-104">EM\_SETCTFMODEBIAS message</span></span>

<span data-ttu-id="74256-105">Establece la diferencia del modo de Text Services Framework (TSF) para un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="74256-105">Sets the Text Services Framework (TSF) mode bias for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="74256-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74256-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74256-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74256-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74256-108">Valor de diferencia del modo.</span><span class="sxs-lookup"><span data-stu-id="74256-108">Mode bias value.</span></span> <span data-ttu-id="74256-109">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="74256-109">This can be one of the following values.</span></span>



| <span data-ttu-id="74256-110">Value</span><span class="sxs-lookup"><span data-stu-id="74256-110">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="74256-111">Significado</span><span class="sxs-lookup"><span data-stu-id="74256-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <span data-ttu-id="74256-112"><dt>**\_valor predeterminado de CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="74256-112"><dt>**CTFMODEBIAS\_DEFAULT**</dt></span></span> </dl>                                           | <span data-ttu-id="74256-113">No hay ninguna diferencia de modo.</span><span class="sxs-lookup"><span data-stu-id="74256-113">There is no mode bias.</span></span><br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <span data-ttu-id="74256-114"><dt>**\_nombre de archivo CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="74256-114"><dt>**CTFMODEBIAS\_FILENAME**</dt></span></span> </dl>                                        | <span data-ttu-id="74256-115">La diferencia es con un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="74256-115">The bias is to a filename.</span></span><br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <span data-ttu-id="74256-116"><dt>**nombre de CTFMODEBIAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="74256-116"><dt>**CTFMODEBIAS\_NAME**</dt></span></span> </dl>                                                    | <span data-ttu-id="74256-117">La diferencia es con un nombre.</span><span class="sxs-lookup"><span data-stu-id="74256-117">The bias is to a name.</span></span><br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <span data-ttu-id="74256-118"><dt>**lectura de CTFMODEBIAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="74256-118"><dt>**CTFMODEBIAS\_READING**</dt></span></span> </dl>                                           | <span data-ttu-id="74256-119">La diferencia es con la lectura.</span><span class="sxs-lookup"><span data-stu-id="74256-119">The bias is to the reading.</span></span><br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <span data-ttu-id="74256-120"><dt>**CTFMODEBIAS \_ DateTime**</dt></span><span class="sxs-lookup"><span data-stu-id="74256-120"><dt>**CTFMODEBIAS\_DATETIME**</dt></span></span> </dl>                                        | <span data-ttu-id="74256-121">La diferencia es una fecha o una hora.</span><span class="sxs-lookup"><span data-stu-id="74256-121">The bias is to a date or time.</span></span><br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <span data-ttu-id="74256-122"><dt>**CTFMODEBIAS \_ Conversation**</dt></span><span class="sxs-lookup"><span data-stu-id="74256-122"><dt>**CTFMODEBIAS\_CONVERSATION**</dt></span></span> </dl>                            | <span data-ttu-id="74256-123">La diferencia es a una conversación.</span><span class="sxs-lookup"><span data-stu-id="74256-123">The bias is to a conversation.</span></span><br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <span data-ttu-id="74256-124"><dt>**CTFMODEBIAS \_ Numeric**</dt></span><span class="sxs-lookup"><span data-stu-id="74256-124"><dt>**CTFMODEBIAS\_NUMERIC**</dt></span></span> </dl>                                           | <span data-ttu-id="74256-125">La diferencia es un número.</span><span class="sxs-lookup"><span data-stu-id="74256-125">The bias is to a number.</span></span><br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <span data-ttu-id="74256-126"><dt>**CTFMODEBIAS \_ hiragana**</dt></span><span class="sxs-lookup"><span data-stu-id="74256-126"><dt>**CTFMODEBIAS\_HIRAGANA**</dt></span></span> </dl>                                        | <span data-ttu-id="74256-127">La diferencia es con las cadenas hiragana.</span><span class="sxs-lookup"><span data-stu-id="74256-127">The bias is to hiragana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <span data-ttu-id="74256-128"><dt>**CTFMODEBIAS \_ katakana**</dt></span><span class="sxs-lookup"><span data-stu-id="74256-128"><dt>**CTFMODEBIAS\_KATAKANA**</dt></span></span> </dl>                                        | <span data-ttu-id="74256-129">La diferencia es a las cadenas katakana.</span><span class="sxs-lookup"><span data-stu-id="74256-129">The bias is to katakana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <span data-ttu-id="74256-130"><dt>**CTFMODEBIAS \_ HANGUL**</dt></span><span class="sxs-lookup"><span data-stu-id="74256-130"><dt>**CTFMODEBIAS\_HANGUL**</dt></span></span> </dl>                                              | <span data-ttu-id="74256-131">La diferencia se debe a los caracteres hangul.</span><span class="sxs-lookup"><span data-stu-id="74256-131">The bias is to Hangul characters.</span></span><br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <span data-ttu-id="74256-132"><dt>**CTFMODEBIAS \_ HALFWIDTHKATAKANA**</dt></span><span class="sxs-lookup"><span data-stu-id="74256-132"><dt>**CTFMODEBIAS\_HALFWIDTHKATAKANA**</dt></span></span> </dl>             | <span data-ttu-id="74256-133">La diferencia se debe a las cadenas katakana de ancho medio.</span><span class="sxs-lookup"><span data-stu-id="74256-133">The bias is to half-width katakana strings.</span></span><br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <span data-ttu-id="74256-134"><dt>**CTFMODEBIAS \_ FULLWIDTHALPHANUMERIC**</dt></span><span class="sxs-lookup"><span data-stu-id="74256-134"><dt>**CTFMODEBIAS\_FULLWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="74256-135">La diferencia se debe a los caracteres alfanuméricos de ancho completo.</span><span class="sxs-lookup"><span data-stu-id="74256-135">The bias is to full-width alphanumeric characters.</span></span><br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <span data-ttu-id="74256-136"><dt>**CTFMODEBIAS \_ HALFWIDTHALPHANUMERIC**</dt></span><span class="sxs-lookup"><span data-stu-id="74256-136"><dt>**CTFMODEBIAS\_HALFWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="74256-137">La diferencia se debe a caracteres alfanuméricos de ancho medio.</span><span class="sxs-lookup"><span data-stu-id="74256-137">The bias is to half-width alphanumeric characters.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="74256-138">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74256-138">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74256-139">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="74256-139">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74256-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74256-140">Return value</span></span>

<span data-ttu-id="74256-141">Si se realiza correctamente, el valor devuelto es el nuevo valor de diferencia del modo TSF.</span><span class="sxs-lookup"><span data-stu-id="74256-141">If successful, the return value is the new TSF mode bias value.</span></span> <span data-ttu-id="74256-142">Si no se realiza correctamente, el valor devuelto es el valor de diferencia del modo TSF antiguo.</span><span class="sxs-lookup"><span data-stu-id="74256-142">If unsuccessful, the return value is the old TSF mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74256-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74256-143">Remarks</span></span>

<span data-ttu-id="74256-144">Cuando una aplicación de Microsoft Rich Edit usa TSF, puede seleccionar la diferencia del modo TSF.</span><span class="sxs-lookup"><span data-stu-id="74256-144">When a Microsoft Rich Edit application uses TSF, it can select the TSF mode bias.</span></span> <span data-ttu-id="74256-145">Este mensaje establece los criterios por los que aparece una opción alternativa en la parte superior de la lista para la selección.</span><span class="sxs-lookup"><span data-stu-id="74256-145">This message sets the criteria by which an alternative choice appears at the top of the list for selection.</span></span>

<span data-ttu-id="74256-146">Para establecer la diferencia de modo para el editor de métodos de entrada (IME), use [**em \_ SETIMEMODEBIAS**](em-setimemodebias.md).</span><span class="sxs-lookup"><span data-stu-id="74256-146">To set the mode bias for the Input Method Editor (IME), use [**EM\_SETIMEMODEBIAS**](em-setimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74256-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74256-147">Requirements</span></span>



| <span data-ttu-id="74256-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="74256-148">Requirement</span></span> | <span data-ttu-id="74256-149">Value</span><span class="sxs-lookup"><span data-stu-id="74256-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74256-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74256-150">Minimum supported client</span></span><br/> | <span data-ttu-id="74256-151">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="74256-151">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74256-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74256-152">Minimum supported server</span></span><br/> | <span data-ttu-id="74256-153">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="74256-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74256-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74256-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="74256-155"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="74256-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74256-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="74256-156">See also</span></span>

<dl> <dt>

<span data-ttu-id="74256-157">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="74256-157">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="74256-158">**\_GETCTFMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="74256-158">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="74256-159">**\_SETIMEMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="74256-159">**EM\_SETIMEMODEBIAS**</span></span>](em-setimemodebias.md)
</dt> </dl>

 

 





