---
title: Mensaje EM_SETCHARFORMAT (RichEdit. h)
description: Establece el formato de caracteres en un control Rich Edit.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- EM_SETCHARFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba8f37960659f29dd33d5b8f27f0b5a2e3d35eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150921"
---
# <a name="em_setcharformat-message"></a><span data-ttu-id="26f4a-104">\_Mensaje SETCHARFORMAT em</span><span class="sxs-lookup"><span data-stu-id="26f4a-104">EM\_SETCHARFORMAT message</span></span>

<span data-ttu-id="26f4a-105">Establece el formato de caracteres en un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="26f4a-105">Sets character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="26f4a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26f4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f4a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26f4a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26f4a-108">Formato de caracteres que se aplica al control.</span><span class="sxs-lookup"><span data-stu-id="26f4a-108">Character formatting that applies to the control.</span></span> <span data-ttu-id="26f4a-109">Si este parámetro es cero, se establece el formato de carácter predeterminado.</span><span class="sxs-lookup"><span data-stu-id="26f4a-109">If this parameter is zero, the default character format is set.</span></span> <span data-ttu-id="26f4a-110">De lo contrario, puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="26f4a-110">Otherwise, it can be one of the following values.</span></span>



| <span data-ttu-id="26f4a-111">Value</span><span class="sxs-lookup"><span data-stu-id="26f4a-111">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="26f4a-112">Significado</span><span class="sxs-lookup"><span data-stu-id="26f4a-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <span data-ttu-id="26f4a-113"><dt>**SCF \_ todo**</dt></span><span class="sxs-lookup"><span data-stu-id="26f4a-113"><dt>**SCF\_ALL**</dt></span></span> </dl>                                     | <span data-ttu-id="26f4a-114">Aplica el formato a todo el texto del control.</span><span class="sxs-lookup"><span data-stu-id="26f4a-114">Applies the formatting to all text in the control.</span></span> <span data-ttu-id="26f4a-115">No es válido con la **\_ selección SCF** o la **\_ palabra SCF**.</span><span class="sxs-lookup"><span data-stu-id="26f4a-115">Not valid with **SCF\_SELECTION** or **SCF\_WORD**.</span></span><br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <span data-ttu-id="26f4a-116"><dt>**SCF \_ ASSOCIATEFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="26f4a-116"><dt>**SCF\_ASSOCIATEFONT**</dt></span></span> </dl>       | <span data-ttu-id="26f4a-117">**RichEdit 4,1:** Asocia una fuente a un script determinado, con lo que se cambia la fuente predeterminada para ese script.</span><span class="sxs-lookup"><span data-stu-id="26f4a-117">**RichEdit 4.1:** Associates a font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="26f4a-118">Para especificar la fuente, use los siguientes miembros de [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** y **LCID**.</span><span class="sxs-lookup"><span data-stu-id="26f4a-118">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <span data-ttu-id="26f4a-119"><dt>**SCF \_ ASSOCIATEFONT2**</dt></span><span class="sxs-lookup"><span data-stu-id="26f4a-119"><dt>**SCF\_ASSOCIATEFONT2**</dt></span></span> </dl>    | <span data-ttu-id="26f4a-120">**RichEdit 4,1:** Asocia una fuente suplente (plano 2) a un script determinado, con lo que se cambia la fuente predeterminada para ese script.</span><span class="sxs-lookup"><span data-stu-id="26f4a-120">**RichEdit 4.1:** Associates a surrogate (plane-2) font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="26f4a-121">Para especificar la fuente, use los siguientes miembros de [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** y **LCID**.</span><span class="sxs-lookup"><span data-stu-id="26f4a-121">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <span data-ttu-id="26f4a-122"><dt>**SCF \_ CHARREPFROMLCID**</dt></span><span class="sxs-lookup"><span data-stu-id="26f4a-122"><dt>**SCF\_CHARREPFROMLCID**</dt></span></span> </dl> | <span data-ttu-id="26f4a-123">Obtiene el repertorio de caracteres del LCID.</span><span class="sxs-lookup"><span data-stu-id="26f4a-123">Gets the character repertoire from the LCID.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="26f4a-124"><dt>**\_valor predeterminado de SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="26f4a-124"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>                         | <span data-ttu-id="26f4a-125">**RichEdit 4,1:** Establece la fuente predeterminada para el control.</span><span class="sxs-lookup"><span data-stu-id="26f4a-125">**RichEdit 4.1:** Sets the default font for the control.</span></span> <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <span data-ttu-id="26f4a-126"><dt>**DONTSETDEFAULT de SPF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26f4a-126"><dt>**SPF\_DONTSETDEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="26f4a-127">Impide establecer el formato de párrafo predeterminado cuando el control Rich Edit está vacío.</span><span class="sxs-lookup"><span data-stu-id="26f4a-127">Prevents setting the default paragraph format when the rich edit control is empty.</span></span><br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <span data-ttu-id="26f4a-128"><dt>**SCF \_ NOKBUPDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="26f4a-128"><dt>**SCF\_NOKBUPDATE**</dt></span></span> </dl>                | <span data-ttu-id="26f4a-129">**RichEdit 4,1:** Impide que el cambio de teclado coincida con la fuente.</span><span class="sxs-lookup"><span data-stu-id="26f4a-129">**RichEdit 4.1:** Prevents keyboard switching to match the font.</span></span> <span data-ttu-id="26f4a-130">Por ejemplo, si se establece una fuente árabe, normalmente la característica de teclado automático para los idiomas bidireccionales cambia el teclado a un teclado árabe.</span><span class="sxs-lookup"><span data-stu-id="26f4a-130">For example, if an Arabic font is set, normally the automatic keyboard feature for Bidi languages changes the keyboard to an Arabic keyboard.</span></span><br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="26f4a-131"><dt>**selección de SCF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26f4a-131"><dt>**SCF\_SELECTION**</dt></span></span> </dl>                   | <span data-ttu-id="26f4a-132">Aplica el formato a la selección actual.</span><span class="sxs-lookup"><span data-stu-id="26f4a-132">Applies the formatting to the current selection.</span></span> <span data-ttu-id="26f4a-133">Si la selección está vacía, el formato de caracteres se aplica al punto de inserción y el nuevo formato de carácter solo está en vigor hasta que el punto de inserción cambie.</span><span class="sxs-lookup"><span data-stu-id="26f4a-133">If the selection is empty, the character formatting is applied to the insertion point, and the new character format is in effect only until the insertion point changes.</span></span><br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <span data-ttu-id="26f4a-134"><dt>**SETDEFAULT de SPF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26f4a-134"><dt>**SPF\_SETDEFAULT**</dt></span></span> </dl>                | <span data-ttu-id="26f4a-135">Establece los atributos de formato de párrafo predeterminados.</span><span class="sxs-lookup"><span data-stu-id="26f4a-135">Sets the default paragraph formatting attributes.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <span data-ttu-id="26f4a-136"><dt>**SCF \_ SMARTFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="26f4a-136"><dt>**SCF\_SMARTFONT**</dt></span></span> </dl>                   | <span data-ttu-id="26f4a-137">Aplique la fuente solo si puede controlar el script.</span><span class="sxs-lookup"><span data-stu-id="26f4a-137">Apply the font only if it can handle script.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <span data-ttu-id="26f4a-138"><dt>**SCF \_ USEUIRULES**</dt></span><span class="sxs-lookup"><span data-stu-id="26f4a-138"><dt>**SCF\_USEUIRULES**</dt></span></span> </dl>                | <span data-ttu-id="26f4a-139">**RichEdit 4,1:** Se usa con la **\_ selección de SCF**.</span><span class="sxs-lookup"><span data-stu-id="26f4a-139">**RichEdit 4.1:** Used with **SCF\_SELECTION**.</span></span> <span data-ttu-id="26f4a-140">Indica que el formato proviene de una barra de herramientas u otra herramienta de interfaz de usuario, por lo que se deben usar reglas de formato de la interfaz de usuario en lugar del formato literal.</span><span class="sxs-lookup"><span data-stu-id="26f4a-140">Indicates that format came from a toolbar or other UI tool, so UI formatting rules should be used instead of literal formatting.</span></span><br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <span data-ttu-id="26f4a-141"><dt>**\_palabra SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="26f4a-141"><dt>**SCF\_WORD**</dt></span></span> </dl>                                  | <span data-ttu-id="26f4a-142">Aplica el formato a la palabra o palabras seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="26f4a-142">Applies the formatting to the selected word or words.</span></span> <span data-ttu-id="26f4a-143">Si la selección está vacía pero el punto de inserción está dentro de una palabra, el formato se aplica a la palabra.</span><span class="sxs-lookup"><span data-stu-id="26f4a-143">If the selection is empty but the insertion point is inside a word, the formatting is applied to the word.</span></span> <span data-ttu-id="26f4a-144">El valor de la **\_ palabra SCF** debe usarse junto con el valor de **\_ selección del SCF** .</span><span class="sxs-lookup"><span data-stu-id="26f4a-144">The **SCF\_WORD** value must be used in conjunction with the **SCF\_SELECTION** value.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="26f4a-145">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26f4a-145">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26f4a-146">Puntero a una estructura [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) que especifica el formato de caracteres que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="26f4a-146">Pointer to a [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure specifying the character formatting to use.</span></span> <span data-ttu-id="26f4a-147">Solo se cambian los atributos de formato especificados por el miembro **dwMask** .</span><span class="sxs-lookup"><span data-stu-id="26f4a-147">Only the formatting attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="26f4a-148">Microsoft Rich Edit 2,0 y versiones posteriores: este parámetro puede ser un puntero a una estructura [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , que es una extensión de la estructura [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="26f4a-148">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="26f4a-149">Antes de enviar el mensaje **\_ SETCHARFORMAT em** , establezca el miembro **cbSize** de la estructura en `sizeof(CHARFORMAT)` o `sizeof(CHARFORMAT2)` indique qué versión de la estructura se está usando.</span><span class="sxs-lookup"><span data-stu-id="26f4a-149">Before sending the **EM\_SETCHARFORMAT** message, set the structure's **cbSize** member to `sizeof(CHARFORMAT)` or `sizeof(CHARFORMAT2)` indicate which version of the structure is being used.</span></span>

<span data-ttu-id="26f4a-150">Los miembros **szFaceName** y **bCharSet** pueden estar sobrereglados si no son válidos para los caracteres, por ejemplo: Arial en caracteres kanji.</span><span class="sxs-lookup"><span data-stu-id="26f4a-150">The **szFaceName** and **bCharSet** members may be overruled when invalid for characters, for example: Arial on kanji characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f4a-151">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26f4a-151">Return value</span></span>

<span data-ttu-id="26f4a-152">Si la operación se realiza correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="26f4a-152">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="26f4a-153">Si se produce un error en la operación, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="26f4a-153">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="26f4a-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26f4a-154">Remarks</span></span>

<span data-ttu-id="26f4a-155">Si este mensaje se envía más de una vez con los mismos parámetros, se alterna el efecto en el texto.</span><span class="sxs-lookup"><span data-stu-id="26f4a-155">If this message is sent more than once with the same parameters, the effect on the text is toggled.</span></span> <span data-ttu-id="26f4a-156">Es decir, al enviar el mensaje una vez que se produce el efecto, el envío del mensaje se cancela dos veces, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="26f4a-156">That is, sending the message once produces the effect, sending the message twice cancels the effect, and so forth.</span></span>

## <a name="requirements"></a><span data-ttu-id="26f4a-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26f4a-157">Requirements</span></span>



| <span data-ttu-id="26f4a-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="26f4a-158">Requirement</span></span> | <span data-ttu-id="26f4a-159">Value</span><span class="sxs-lookup"><span data-stu-id="26f4a-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26f4a-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26f4a-160">Minimum supported client</span></span><br/> | <span data-ttu-id="26f4a-161">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="26f4a-161">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26f4a-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26f4a-162">Minimum supported server</span></span><br/> | <span data-ttu-id="26f4a-163">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="26f4a-163">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26f4a-164">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26f4a-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="26f4a-165"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="26f4a-165"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f4a-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="26f4a-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="26f4a-167">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="26f4a-167">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="26f4a-168">**CHARFORMAT**</span><span class="sxs-lookup"><span data-stu-id="26f4a-168">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="26f4a-169">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="26f4a-169">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





