---
title: Mensaje EM_GETIMEPROPERTY (RichEdit. h)
description: Recupera la propiedad y las capacidades del editor de métodos de entrada (IME) asociado a la configuración regional de entrada actual.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- EM_GETIMEPROPERTY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETIMEPROPERTY
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c081aa99c99f4cd0995c0f9d2f5256e2958dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150767"
---
# <a name="em_getimeproperty-message"></a><span data-ttu-id="06e78-104">\_Mensaje GETIMEPROPERTY em</span><span class="sxs-lookup"><span data-stu-id="06e78-104">EM\_GETIMEPROPERTY message</span></span>

<span data-ttu-id="06e78-105">Recupera la propiedad y las capacidades del editor de métodos de entrada (IME) asociado a la configuración regional de entrada actual.</span><span class="sxs-lookup"><span data-stu-id="06e78-105">Retrieves the property and capabilities of the Input Method Editor (IME) associated with the current input locale.</span></span>

## <a name="parameters"></a><span data-ttu-id="06e78-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06e78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06e78-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06e78-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06e78-108">Especifica el tipo de información de propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="06e78-108">Specifies the type of property information to retrieve.</span></span> <span data-ttu-id="06e78-109">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="06e78-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="06e78-110">Valor</span><span class="sxs-lookup"><span data-stu-id="06e78-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="06e78-111">Significado</span><span class="sxs-lookup"><span data-stu-id="06e78-111">Meaning</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <span data-ttu-id="06e78-112"><dt>**IGP \_ (propiedad)**</dt></span><span class="sxs-lookup"><span data-stu-id="06e78-112"><dt>**IGP\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="06e78-113">Información de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="06e78-113">Property information.</span></span><br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <span data-ttu-id="06e78-114"><dt>**conversión de IGP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06e78-114"><dt>**IGP\_CONVERSION**</dt></span></span> </dl>          | <span data-ttu-id="06e78-115">Capacidades de conversión.</span><span class="sxs-lookup"><span data-stu-id="06e78-115">Conversion capabilities.</span></span> <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <span data-ttu-id="06e78-116"><dt>**\_frase IGP**</dt></span><span class="sxs-lookup"><span data-stu-id="06e78-116"><dt>**IGP\_SENTENCE**</dt></span></span> </dl>                | <span data-ttu-id="06e78-117">Capacidades del modo de oraciones.</span><span class="sxs-lookup"><span data-stu-id="06e78-117">Sentence mode capabilities.</span></span> <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <span data-ttu-id="06e78-118"><dt>**interfaz de usuario de IGP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06e78-118"><dt>**IGP\_UI**</dt></span></span> </dl>                                  | <span data-ttu-id="06e78-119">Capacidades de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="06e78-119">User interface capabilities.</span></span> <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <span data-ttu-id="06e78-120"><dt>**IGP \_ SETCOMPSTR**</dt></span><span class="sxs-lookup"><span data-stu-id="06e78-120"><dt>**IGP\_SETCOMPSTR**</dt></span></span> </dl>          | <span data-ttu-id="06e78-121">Capacidades de la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="06e78-121">Composition string capabilities.</span></span> <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <span data-ttu-id="06e78-122"><dt>**selección de IGP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06e78-122"><dt>**IGP\_SELECT**</dt></span></span> </dl>                      | <span data-ttu-id="06e78-123">Funcionalidades de herencia de selección.</span><span class="sxs-lookup"><span data-stu-id="06e78-123">Selection inheritance capabilities.</span></span> <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <span data-ttu-id="06e78-124"><dt>**IGP \_ GETIMEVERSION**</dt></span><span class="sxs-lookup"><span data-stu-id="06e78-124"><dt>**IGP\_GETIMEVERSION**</dt></span></span> </dl> | <span data-ttu-id="06e78-125">Recupera el número de versión del sistema para el que se creó el IME especificado.</span><span class="sxs-lookup"><span data-stu-id="06e78-125">Retrieves the system version number for which the specified IME was created.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="06e78-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06e78-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06e78-127">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="06e78-127">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06e78-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06e78-128">Return value</span></span>

<span data-ttu-id="06e78-129">Devuelve el valor de la propiedad o de la capacidad, dependiendo del valor del parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="06e78-129">Returns the property or capability value, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="06e78-130">Para obtener más información, vea la sección Notas.</span><span class="sxs-lookup"><span data-stu-id="06e78-130">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="06e78-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06e78-131">Remarks</span></span>

<span data-ttu-id="06e78-132">Si *wParam* es \_ la propiedad IGP, devuelve uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="06e78-132">If *wParam* is IGP\_PROPERTY, it returns one or more of the following values.</span></span>



| <span data-ttu-id="06e78-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="06e78-133">Requirement</span></span> | <span data-ttu-id="06e78-134">Value</span><span class="sxs-lookup"><span data-stu-id="06e78-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06e78-135">\_prop IME \_ en el \_ símbolo de intercalación</span><span class="sxs-lookup"><span data-stu-id="06e78-135">IME\_PROP\_AT\_CARET</span></span>                | <span data-ttu-id="06e78-136">Si se establece, la ventana de conversión se encuentra en la posición del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="06e78-136">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="06e78-137">Si está desactivada, la ventana está cerca de la posición del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="06e78-137">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="06e78-138">\_interfaz de \_ usuario especial de prop de IME \_</span><span class="sxs-lookup"><span data-stu-id="06e78-138">IME\_PROP\_SPECIAL\_UI</span></span>              | <span data-ttu-id="06e78-139">Si se establece, IME tiene una interfaz de usuario no estándar.</span><span class="sxs-lookup"><span data-stu-id="06e78-139">If set, IME has a nonstandard user interface.</span></span> <span data-ttu-id="06e78-140">La aplicación no debe dibujarse en la ventana del IME.</span><span class="sxs-lookup"><span data-stu-id="06e78-140">The application should not draw in the IME window.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="06e78-141">\_CANDLIST prop \_ IME \_ Start \_ from \_ 1</span><span class="sxs-lookup"><span data-stu-id="06e78-141">IME\_PROP\_CANDLIST\_START\_FROM\_1</span></span> | <span data-ttu-id="06e78-142">Si se establece, las cadenas de la lista de candidatos se numeran a partir de 1.</span><span class="sxs-lookup"><span data-stu-id="06e78-142">If set, strings in the candidate list are numbered starting at 1.</span></span> <span data-ttu-id="06e78-143">Si está desactivada, las cadenas comienzan por cero.</span><span class="sxs-lookup"><span data-stu-id="06e78-143">If clear, strings start at zero.</span></span>                                                                                                                                                                |
| <span data-ttu-id="06e78-144">PROP de IME \_ \_ Unicode</span><span class="sxs-lookup"><span data-stu-id="06e78-144">IME\_PROP\_UNICODE</span></span>                  | <span data-ttu-id="06e78-145">Si se establece, el IME se ve como UnicodeIME.</span><span class="sxs-lookup"><span data-stu-id="06e78-145">If set, the IME is viewed as a UnicodeIME.</span></span> <span data-ttu-id="06e78-146">El sistema y el IME se comunicarán a través de la interfaz UnicodeIME.</span><span class="sxs-lookup"><span data-stu-id="06e78-146">The system and the IME will communicate through the UnicodeIME interface.</span></span> <span data-ttu-id="06e78-147">Si está claro, IME usará la interfaz ANSI para comunicarse con el sistema.</span><span class="sxs-lookup"><span data-stu-id="06e78-147">If clear, IME will use the ANSI interface to communicate with the system.</span></span>                                                                    |
| <span data-ttu-id="06e78-148">\_prop. \_ de IME completada \_ en \_ anulación de selección</span><span class="sxs-lookup"><span data-stu-id="06e78-148">IME\_PROP\_COMPLETE\_ON\_UNSELECT</span></span>   | <span data-ttu-id="06e78-149">Si se establece, la ventana de conversión se encuentra en la posición del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="06e78-149">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="06e78-150">Si está desactivada, la ventana está cerca de la posición del símbolo de intercalación.</span><span class="sxs-lookup"><span data-stu-id="06e78-150">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="06e78-151">PROP de IME \_ \_ Accept \_ \_ VKEY Wide</span><span class="sxs-lookup"><span data-stu-id="06e78-151">IME\_PROP\_ACCEPT\_WIDE\_VKEY</span></span>       | <span data-ttu-id="06e78-152">Si se establece, el IME procesa el Unicode insertado que proviene de la función [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) mediante el \_ paquete VK.</span><span class="sxs-lookup"><span data-stu-id="06e78-152">If set, the IME processes the injected Unicode that came from the [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) function by using VK\_PACKET.</span></span> <span data-ttu-id="06e78-153">Si está desactivada, es posible que el IME no procese el Unicode insertado y que el Unicode insertado se envíe directamente a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="06e78-153">If clear, the IME might not process the injected Unicode, and the injected Unicode might be sent to the application directly.</span></span> |



 

<span data-ttu-id="06e78-154">Si *wParam* es \_ la interfaz de usuario de IGP, devuelve uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="06e78-154">If *wParam* is IGP\_UI, it returns one or more of the following values.</span></span>



| <span data-ttu-id="06e78-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="06e78-155">Requirement</span></span> | <span data-ttu-id="06e78-156">Value</span><span class="sxs-lookup"><span data-stu-id="06e78-156">Value</span></span> |
|-----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06e78-157">Cap de UI \_ \_ 2700</span><span class="sxs-lookup"><span data-stu-id="06e78-157">UI\_CAP\_2700</span></span>   | <span data-ttu-id="06e78-158">Admite valores de escape de texto de 0 o 2700.</span><span class="sxs-lookup"><span data-stu-id="06e78-158">Supports text escapement values of 0 or 2700.</span></span> <span data-ttu-id="06e78-159">Para obtener más información, vea **lfEscapement**.</span><span class="sxs-lookup"><span data-stu-id="06e78-159">For more information, see **lfEscapement**.</span></span>             |
| <span data-ttu-id="06e78-160">\_ROT90 de Cap de IU \_</span><span class="sxs-lookup"><span data-stu-id="06e78-160">UI\_CAP\_ROT90</span></span>  | <span data-ttu-id="06e78-161">Admite valores de escape de texto de 0, 900, 1800 o 2700.</span><span class="sxs-lookup"><span data-stu-id="06e78-161">Supports text escapement values of 0, 900, 1800, or 2700.</span></span> <span data-ttu-id="06e78-162">Para obtener más información, vea **lfEscapement**.</span><span class="sxs-lookup"><span data-stu-id="06e78-162">For more information, see **lfEscapement**.</span></span> |
| <span data-ttu-id="06e78-163">\_ROTANY de Cap de IU \_</span><span class="sxs-lookup"><span data-stu-id="06e78-163">UI\_CAP\_ROTANY</span></span> | <span data-ttu-id="06e78-164">Admite cualquier valor de escape de texto.</span><span class="sxs-lookup"><span data-stu-id="06e78-164">Supports any text escapement value.</span></span> <span data-ttu-id="06e78-165">Para obtener más información, vea **lfEscapement**.</span><span class="sxs-lookup"><span data-stu-id="06e78-165">For more information, see **lfEscapement**.</span></span>                       |



 

<span data-ttu-id="06e78-166">Si *wParam* es IGP \_ SETCOMPSTR, devuelve uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="06e78-166">If *wParam* is IGP\_SETCOMPSTR, it returns one or more of the following values.</span></span>



| <span data-ttu-id="06e78-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="06e78-167">Requirement</span></span> | <span data-ttu-id="06e78-168">Value</span><span class="sxs-lookup"><span data-stu-id="06e78-168">Value</span></span> |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06e78-169">Cap de SCS \_ \_ COMPSTR</span><span class="sxs-lookup"><span data-stu-id="06e78-169">SCS\_CAP\_COMPSTR</span></span>            | <span data-ttu-id="06e78-170">Puede crear la cadena de composición mediante una llamada a la función [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) con el \_ valor SETSTR de SCS.</span><span class="sxs-lookup"><span data-stu-id="06e78-170">Can create the composition string by calling the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with the SCS\_SETSTR value.</span></span>                                                      |
| <span data-ttu-id="06e78-171">Cap de SCS \_ \_ MAKEREAD</span><span class="sxs-lookup"><span data-stu-id="06e78-171">SCS\_CAP\_MAKEREAD</span></span>           | <span data-ttu-id="06e78-172">Puede crear la cadena de lectura a partir de la cadena de composición correspondiente al usar la función [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) con SCS \_ SETSTR y sin establecer *lpRead*.</span><span class="sxs-lookup"><span data-stu-id="06e78-172">Can create the reading string from corresponding composition string when using the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with SCS\_SETSTR and without setting *lpRead*.</span></span> |
| <span data-ttu-id="06e78-173">Cap de SCS \_ \_ SETRECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="06e78-173">SCS\_CAP\_SETRECONVERTSTRING</span></span> | <span data-ttu-id="06e78-174">Este IME puede admitir la reconversión.</span><span class="sxs-lookup"><span data-stu-id="06e78-174">This IME can support reconversion.</span></span> <span data-ttu-id="06e78-175">Use [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="06e78-175">Use [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) to do the reconversion.</span></span>                                                                             |



 

<span data-ttu-id="06e78-176">Si *wParam* es \_ la selección de IGP, devuelve uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="06e78-176">If *wParam* is IGP\_SELECT, it returns one or more of the following values.</span></span>



| <span data-ttu-id="06e78-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="06e78-177">Requirement</span></span> | <span data-ttu-id="06e78-178">Value</span><span class="sxs-lookup"><span data-stu-id="06e78-178">Value</span></span> |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="06e78-179">SELECCIONAR \_ Cap \_ CONVMODE</span><span class="sxs-lookup"><span data-stu-id="06e78-179">SELECT\_CAP\_CONVMODE</span></span> | <span data-ttu-id="06e78-180">Hereda el modo de conversión cuando se selecciona un nuevo IME.</span><span class="sxs-lookup"><span data-stu-id="06e78-180">Inherits conversion mode when a new IME is selected.</span></span> |
| <span data-ttu-id="06e78-181">SELECCIONAR \_ frase de extremo \_</span><span class="sxs-lookup"><span data-stu-id="06e78-181">SELECT\_CAP\_SENTENCE</span></span> | <span data-ttu-id="06e78-182">Hereda el modo de oración cuando se selecciona un nuevo IME.</span><span class="sxs-lookup"><span data-stu-id="06e78-182">Inherits sentence mode when a new IME is selected.</span></span>   |



 

<span data-ttu-id="06e78-183">Si *wParam* es IGP \_ GETIMEVERSION, devuelve uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="06e78-183">If *wParam* is IGP\_GETIMEVERSION, it returns one or more of the following values.</span></span>



| <span data-ttu-id="06e78-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="06e78-184">Requirement</span></span> | <span data-ttu-id="06e78-185">Value</span><span class="sxs-lookup"><span data-stu-id="06e78-185">Value</span></span> |
|--------------|---------------------------------------------|
| <span data-ttu-id="06e78-186">\_0310</span><span class="sxs-lookup"><span data-stu-id="06e78-186">IMEVER\_0310</span></span> | <span data-ttu-id="06e78-187">Se creó el IME para Windows 3,1.</span><span class="sxs-lookup"><span data-stu-id="06e78-187">The IME was created for Windows 3.1.</span></span>        |
| <span data-ttu-id="06e78-188">\_0400</span><span class="sxs-lookup"><span data-stu-id="06e78-188">IMEVER\_0400</span></span> | <span data-ttu-id="06e78-189">Se creó el IME para Windows 95 o posterior.</span><span class="sxs-lookup"><span data-stu-id="06e78-189">The IME was created for Windows 95 or later</span></span> |



 

<span data-ttu-id="06e78-190">Este mensaje es similar a [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), con la excepción de que usa la configuración regional de entrada actual.</span><span class="sxs-lookup"><span data-stu-id="06e78-190">This message is similar to [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), except that it uses the current input locale.</span></span> <span data-ttu-id="06e78-191">La aplicación debe llamar a [**em \_ ISIME**](em-isime.md) antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="06e78-191">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="06e78-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06e78-192">Requirements</span></span>



| <span data-ttu-id="06e78-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="06e78-193">Requirement</span></span> | <span data-ttu-id="06e78-194">Value</span><span class="sxs-lookup"><span data-stu-id="06e78-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06e78-195">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06e78-195">Minimum supported client</span></span><br/> | <span data-ttu-id="06e78-196">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="06e78-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06e78-197">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06e78-197">Minimum supported server</span></span><br/> | <span data-ttu-id="06e78-198">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="06e78-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06e78-199">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06e78-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="06e78-200"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="06e78-200"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06e78-201">Vea también</span><span class="sxs-lookup"><span data-stu-id="06e78-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="06e78-202">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="06e78-202">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="06e78-203">**\_ISIME em**</span><span class="sxs-lookup"><span data-stu-id="06e78-203">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

<span data-ttu-id="06e78-204">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="06e78-204">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="06e78-205">**ImmGetProperty**</span><span class="sxs-lookup"><span data-stu-id="06e78-205">**ImmGetProperty**</span></span>](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

