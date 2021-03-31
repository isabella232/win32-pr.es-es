---
title: Mensaje EM_AUTOURLDETECT (RichEdit. h)
description: Habilita o deshabilita la detección automática de hipervínculos mediante un control Rich Edit.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- EM_AUTOURLDETECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_AUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc8f76b89e5e8aa529084b5c8c0898200e28ed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996654"
---
# <a name="em_autourldetect-message"></a><span data-ttu-id="8e7c4-104">\_Mensaje AUTOURLDETECT em</span><span class="sxs-lookup"><span data-stu-id="8e7c4-104">EM\_AUTOURLDETECT message</span></span>

<span data-ttu-id="8e7c4-105">Habilita o deshabilita la detección automática de hipervínculos mediante un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-105">Enables or disables automatic detection of hyperlinks by a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e7c4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e7c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e7c4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e7c4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e7c4-108">Especifique 0 para deshabilitar la detección automática de vínculos o uno de los valores siguientes para habilitar distintos tipos de detección.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-108">Specify 0 to disable automatic link detection, or one of the following values to enable various kinds of detection.</span></span>



| <span data-ttu-id="8e7c4-109">Value</span><span class="sxs-lookup"><span data-stu-id="8e7c4-109">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="8e7c4-110">Significado</span><span class="sxs-lookup"><span data-stu-id="8e7c4-110">Meaning</span></span>                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <span data-ttu-id="8e7c4-111"><dt>**AURL \_ DISABLEMIXEDLGC**</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c4-111"><dt>**AURL\_DISABLEMIXEDLGC**</dt></span></span> </dl>          | <span data-ttu-id="8e7c4-112">**Windows 8**: deshabilite el reconocimiento de nombres de dominio que contengan etiquetas con caracteres que pertenezcan a más de uno de los siguientes scripts: Latín, griego y cirílico.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-112">**Windows 8**: Disable recognition of domain names that contain labels with characters belonging to more than one of the following scripts: Latin, Greek, and Cyrillic.</span></span> <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <span data-ttu-id="8e7c4-113"><dt>**AURL \_ ENABLEDRIVELETTERS**</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c4-113"><dt>**AURL\_ENABLEDRIVELETTERS**</dt></span></span> </dl> | <span data-ttu-id="8e7c4-114">**Windows 8**: reconoce los nombres de archivo que tienen una especificación de unidad inicial, como c: \\ temp.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-114">**Windows 8**: Recognize file names that have a leading drive specification, such as c:\\temp.</span></span><br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <span data-ttu-id="8e7c4-115"><dt>**AURL \_ ENABLEEA**</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c4-115"><dt>**AURL\_ENABLEEA**</dt></span></span> </dl>                               | <span data-ttu-id="8e7c4-116">Este valor está en desuso; Use **AURL \_ ENABLEEAURLS** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-116">This value is deprecated; use **AURL\_ENABLEEAURLS** instead.</span></span><br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <span data-ttu-id="8e7c4-117"><dt>**AURL \_ ENABLEEAURLS**</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c4-117"><dt>**AURL\_ENABLEEAURLS**</dt></span></span> </dl>                   | <span data-ttu-id="8e7c4-118">Reconoce las direcciones URL que contienen caracteres de Asia oriental.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-118">Recognize URLs that contain East Asian characters.</span></span> <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <span data-ttu-id="8e7c4-119"><dt>**AURL \_ ENABLEEMAILADDR**</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c4-119"><dt>**AURL\_ENABLEEMAILADDR**</dt></span></span> </dl>          | <span data-ttu-id="8e7c4-120">**Windows 8**: reconocer direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-120">**Windows 8**: Recognize email addresses.</span></span><br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <span data-ttu-id="8e7c4-121"><dt>**AURL \_ ENABLETELNO**</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c4-121"><dt>**AURL\_ENABLETELNO**</dt></span></span> </dl>                      | <span data-ttu-id="8e7c4-122">**Windows 8**: reconocer números de teléfono.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-122">**Windows 8**: Recognize telephone numbers.</span></span><br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <span data-ttu-id="8e7c4-123"><dt>**AURL \_ ENABLEURL**</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c4-123"><dt>**AURL\_ENABLEURL**</dt></span></span> </dl>                            | <span data-ttu-id="8e7c4-124">**Windows 8**: reconozca las direcciones URL que incluyen la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-124">**Windows 8**: Recognize URLs that include the path.</span></span><br/>                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="8e7c4-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e7c4-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e7c4-126">Este parámetro determina los esquemas de dirección URL reconocidos si **AURL \_ ENABLEURL** está activo.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-126">This parameter determines the URL schemes recognized if **AURL\_ENABLEURL** is active.</span></span> <span data-ttu-id="8e7c4-127">Si *lParam* es null, se utiliza la lista de nombres de esquema predeterminados (vea la sección comentarios).</span><span class="sxs-lookup"><span data-stu-id="8e7c4-127">If *lParam* is NULL, the default scheme name list is used (see Remarks).</span></span> <span data-ttu-id="8e7c4-128">Como alternativa, *lParam* puede apuntar a una cadena terminada en null que consta de hasta 50 nombres de esquema terminados con dos puntos que sustituyen a la lista de nombres de esquemas predeterminados.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-128">Alternatively, *lParam* can point to a null-terminated string consisting of up to 50 colon-terminated scheme names that supersede the default scheme name list.</span></span> <span data-ttu-id="8e7c4-129">Por ejemplo, la cadena puede ser "News: http: ftp: Telnet:".</span><span class="sxs-lookup"><span data-stu-id="8e7c4-129">For example, the string could be "news:http:ftp:telnet:".</span></span> <span data-ttu-id="8e7c4-130">La sintaxis de nombre de esquema se define en el sitio web de los [identificadores uniformes de recursos (URI): Sintaxis genérica]( https://www.ietf.org/rfc/rfc2396.txt) en el sitio web del equipo de ingeniería de Internet (IETF).</span><span class="sxs-lookup"><span data-stu-id="8e7c4-130">The scheme name syntax is defined in the [Uniform Resource Identifiers (URI): Generic Syntax]( https://www.ietf.org/rfc/rfc2396.txt) document on The Internet Engineering Task Force (IETF) website.</span></span> <span data-ttu-id="8e7c4-131">En concreto, un nombre de esquema puede contener hasta 13 caracteres (incluidos los dos puntos), debe empezar por un carácter alfabético ASCII y puede ir seguido de una combinación de alphabetics ASCII, dígitos y los tres caracteres de puntuación: ".", "+" y "-".</span><span class="sxs-lookup"><span data-stu-id="8e7c4-131">Specifically, a scheme name can contain up to 13 characters (including the colon), must start with an ASCII alphabetic, and can be followed by a mixture of ASCII alphabetics, digits, and the three punctuation characters: ".", "+", and "-".</span></span> <span data-ttu-id="8e7c4-132">El tipo de cadena puede ser **Char \** _ o _*WCHAR \*\*_; el control Rich Edit detecta automáticamente el tipo.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-132">The string type can be either **char\** _ or _*WCHAR\*\*_; the rich edit control automatically detects the type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e7c4-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e7c4-133">Return value</span></span>

<span data-ttu-id="8e7c4-134">Si el mensaje se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-134">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="8e7c4-135">Si se produce un error en el mensaje, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-135">If the message fails, the return value is a nonzero value.</span></span> <span data-ttu-id="8e7c4-136">Por ejemplo, puede producirse un error en el mensaje debido a que no hay memoria suficiente, una opción de detección no válida o una cadena de nombre de esquema no válida.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-136">For example, the message might fail due to insufficient memory, an invalid detection option, or an invalid scheme-name string.</span></span>

<span data-ttu-id="8e7c4-137">Si _lParam \* contiene más de 50 nombres de esquema, se produce un error en el mensaje con un valor devuelto de **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-137">If _lParam\* contains more than 50 scheme names, the message fails with a return value of **E\_INVALIDARG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e7c4-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e7c4-138">Remarks</span></span>

<span data-ttu-id="8e7c4-139">Si la detección automática de direcciones URL está habilitada (es decir, *wParam* incluye **AURL \_ ENABLEURL**), el control Rich Edit examina cualquier texto modificado para determinar si el texto coincide con el formato de una dirección URL (o más general en Windows 8 o posterior, un identificador de recursos de IRI International).</span><span class="sxs-lookup"><span data-stu-id="8e7c4-139">If automatic URL detection is enabled (that is, *wParam* includes **AURL\_ENABLEURL**), the rich edit control scans any modified text to determine whether the text matches the format of a URL (or more generally in Windows 8 or later an IRI International Resource Identifier).</span></span> <span data-ttu-id="8e7c4-140">Si *lParam* es null, el control detecta las direcciones URL que comienzan con los siguientes nombres de esquema:</span><span class="sxs-lookup"><span data-stu-id="8e7c4-140">If *lParam* is NULL, the control detects URLs that begin with the following scheme names:</span></span>

-   <span data-ttu-id="8e7c4-141">callto</span><span class="sxs-lookup"><span data-stu-id="8e7c4-141">callto</span></span>
-   <span data-ttu-id="8e7c4-142">archivo</span><span class="sxs-lookup"><span data-stu-id="8e7c4-142">file</span></span>
-   <span data-ttu-id="8e7c4-143">ftp</span><span class="sxs-lookup"><span data-stu-id="8e7c4-143">ftp</span></span>
-   <span data-ttu-id="8e7c4-144">gopher</span><span class="sxs-lookup"><span data-stu-id="8e7c4-144">gopher</span></span>
-   <span data-ttu-id="8e7c4-145">http</span><span class="sxs-lookup"><span data-stu-id="8e7c4-145">http</span></span>
-   <span data-ttu-id="8e7c4-146">https</span><span class="sxs-lookup"><span data-stu-id="8e7c4-146">https</span></span>
-   <span data-ttu-id="8e7c4-147">mailto</span><span class="sxs-lookup"><span data-stu-id="8e7c4-147">mailto</span></span>
-   <span data-ttu-id="8e7c4-148">news</span><span class="sxs-lookup"><span data-stu-id="8e7c4-148">news</span></span>
-   <span data-ttu-id="8e7c4-149">HDInsight</span><span class="sxs-lookup"><span data-stu-id="8e7c4-149">notes</span></span>
-   <span data-ttu-id="8e7c4-150">NNTP</span><span class="sxs-lookup"><span data-stu-id="8e7c4-150">nntp</span></span>
-   <span data-ttu-id="8e7c4-151">onenote</span><span class="sxs-lookup"><span data-stu-id="8e7c4-151">onenote</span></span>
-   <span data-ttu-id="8e7c4-152">Outlook</span><span class="sxs-lookup"><span data-stu-id="8e7c4-152">outlook</span></span>
-   <span data-ttu-id="8e7c4-153">prospero</span><span class="sxs-lookup"><span data-stu-id="8e7c4-153">prospero</span></span>
-   <span data-ttu-id="8e7c4-154">tel</span><span class="sxs-lookup"><span data-stu-id="8e7c4-154">tel</span></span>
-   <span data-ttu-id="8e7c4-155">telnet</span><span class="sxs-lookup"><span data-stu-id="8e7c4-155">telnet</span></span>
-   <span data-ttu-id="8e7c4-156">wais</span><span class="sxs-lookup"><span data-stu-id="8e7c4-156">wais</span></span>
-   <span data-ttu-id="8e7c4-157">webcal</span><span class="sxs-lookup"><span data-stu-id="8e7c4-157">webcal</span></span>

<span data-ttu-id="8e7c4-158">Cuando se habilita la detección automática de vínculos, el control Rich Edit quita el efecto de **\_ vínculo CFE** del texto modificado que no tiene un formato reconocido por el control.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-158">When automatic link detection is enabled, the rich edit control removes the **CFE\_LINK** effect from modified text that does not have a format recognized by the control.</span></span> <span data-ttu-id="8e7c4-159">Si la aplicación usa el efecto de **\_ vínculo CFE** para marcar otros tipos de texto, no habilite la detección automática de vínculos.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-159">If your application uses the **CFE\_LINK** effect to mark other types of text, do not enable automatic link detection.</span></span> <span data-ttu-id="8e7c4-160">El control Rich Edit no comprueba si existe un vínculo detectado; esa responsabilidad pertenece al cliente.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-160">The rich edit control does not check whether a detected link exists; that responsibility belongs to the client.</span></span>

<span data-ttu-id="8e7c4-161">Un control Rich Edit envía la notificación de [ \_ vínculo en](en-link.md) cuando recibe varios mensajes mientras el puntero del mouse se encuentra sobre el texto que tiene el efecto de **\_ vínculo CFE** .</span><span class="sxs-lookup"><span data-stu-id="8e7c4-161">A rich edit control sends the [EN\_LINK](en-link.md) notification when it receives various messages while the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="8e7c4-162">Para obtener más información, vea [hipervínculos de RichEdit automático](/archive/blogs/murrays/automatic-richedit-hyperlinks) y [hipervínculos de nombre descriptivo de RichEdit](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).</span><span class="sxs-lookup"><span data-stu-id="8e7c4-162">For more information, see [Automatic RichEdit Hyperlinks](/archive/blogs/murrays/automatic-richedit-hyperlinks) and [RichEdit Friendly Name Hyperlinks](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e7c4-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e7c4-163">Requirements</span></span>



| <span data-ttu-id="8e7c4-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e7c4-164">Requirement</span></span> | <span data-ttu-id="8e7c4-165">Value</span><span class="sxs-lookup"><span data-stu-id="8e7c4-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e7c4-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e7c4-166">Minimum supported client</span></span><br/> | <span data-ttu-id="8e7c4-167">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8e7c4-167">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e7c4-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e7c4-168">Minimum supported server</span></span><br/> | <span data-ttu-id="8e7c4-169">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e7c4-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e7c4-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e7c4-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e7c4-171"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c4-171"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e7c4-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e7c4-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e7c4-173">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="8e7c4-173">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[<span data-ttu-id="8e7c4-174">EN \_ vínculo</span><span class="sxs-lookup"><span data-stu-id="8e7c4-174">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 

