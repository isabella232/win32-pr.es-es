---
title: Mensaje EM_STREAMOUT (RichEdit. h)
description: Hace que un control Rich Edit pase su contenido a una función de devolución de llamada EditStreamCallback definida por la aplicación \ 8211;. La función de devolución de llamada puede escribir el flujo de datos en un archivo o en cualquier otra ubicación que elija.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- EM_STREAMOUT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_STREAMOUT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbdef51348593f8dbcfdb1ef579aca7dba6f96e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996433"
---
# <a name="em_streamout-message"></a><span data-ttu-id="a1ac2-105">\_Mensaje STREAMOUT em</span><span class="sxs-lookup"><span data-stu-id="a1ac2-105">EM\_STREAMOUT message</span></span>

<span data-ttu-id="a1ac2-106">Hace que un control Rich Edit pase su contenido a una función de devolución de llamada [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-106">Causes a rich edit control to pass its contents to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span> <span data-ttu-id="a1ac2-107">La función de devolución de llamada puede escribir el flujo de datos en un archivo o en cualquier otra ubicación que elija.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-107">The callback function can then write the stream of data to a file or any other location that it chooses.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1ac2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1ac2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1ac2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1ac2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1ac2-110">Especifica el formato de datos y las opciones de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-110">Specifies the data format and replacement options.</span></span>

<span data-ttu-id="a1ac2-111">Este valor debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-111">This value must be one of the following values.</span></span>



| <span data-ttu-id="a1ac2-112">Value</span><span class="sxs-lookup"><span data-stu-id="a1ac2-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="a1ac2-113">Significado</span><span class="sxs-lookup"><span data-stu-id="a1ac2-113">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="a1ac2-114"><dt>**RTF de SF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a1ac2-114"><dt>**SF\_RTF**</dt></span></span> </dl>                   | <span data-ttu-id="a1ac2-115">RTF.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-115">RTF.</span></span><br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <span data-ttu-id="a1ac2-116"><dt>**\_RTFNOOBJS SF**</dt></span><span class="sxs-lookup"><span data-stu-id="a1ac2-116"><dt>**SF\_RTFNOOBJS**</dt></span></span> </dl> | <span data-ttu-id="a1ac2-117">RTF con espacios en lugar de objetos COM.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-117">RTF with spaces in place of COM objects.</span></span><br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="a1ac2-118"><dt>**\_texto SF**</dt></span><span class="sxs-lookup"><span data-stu-id="a1ac2-118"><dt>**SF\_TEXT**</dt></span></span> </dl>                | <span data-ttu-id="a1ac2-119">Texto con espacios en lugar de objetos COM.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-119">Text with spaces in place of COM objects.</span></span><br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <span data-ttu-id="a1ac2-120"><dt>**SF con \_ texto**</dt></span><span class="sxs-lookup"><span data-stu-id="a1ac2-120"><dt>**SF\_TEXTIZED**</dt></span></span> </dl>    | <span data-ttu-id="a1ac2-121">Texto con una representación de texto de los objetos COM.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-121">Text with a text representation of COM objects.</span></span><br/> |



 

<span data-ttu-id="a1ac2-122">La **opción \_ RTFNOOBJS de SF** es útil si una aplicación almacena objetos com en sí, ya que la representación RTF de objetos com no es muy compacta.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-122">The **SF\_RTFNOOBJS** option is useful if an application stores COM objects itself, as RTF representation of COM objects is not very compact.</span></span> <span data-ttu-id="a1ac2-123">La palabra de control, \\ objattph, seguida de un espacio denota la posición del objeto.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-123">The control word, \\objattph, followed by a space denotes the object position.</span></span>

<span data-ttu-id="a1ac2-124">Además, puede especificar las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-124">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="a1ac2-125">Value</span><span class="sxs-lookup"><span data-stu-id="a1ac2-125">Value</span></span>                                                                                                                                                            | <span data-ttu-id="a1ac2-126">Significado</span><span class="sxs-lookup"><span data-stu-id="a1ac2-126">Meaning</span></span>                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="a1ac2-127"><dt>**SFF \_ PLAINRTF**</dt></span><span class="sxs-lookup"><span data-stu-id="a1ac2-127"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>       | <span data-ttu-id="a1ac2-128">Si se especifica, el control Rich Edit transmite solo las palabras clave comunes a todos los lenguajes, omitiendo las palabras clave específicas del idioma.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-128">If specified, the rich edit control streams out only the keywords common to all languages, ignoring language-specific keywords.</span></span> <span data-ttu-id="a1ac2-129">Si no se especifica, el control Rich Edit transmite todas las palabras clave.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-129">If not specified, the rich edit control streams out all keywords.</span></span> <span data-ttu-id="a1ac2-130">Puede combinar esta marca con la marca **RTFNOOBJS \_ SF** o **SF \_** .</span><span class="sxs-lookup"><span data-stu-id="a1ac2-130">You can combine this flag with the **SF\_RTF** or **SF\_RTFNOOBJS** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="a1ac2-131"><dt>**selección de SFF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a1ac2-131"><dt>**SFF\_SELECTION**</dt></span></span> </dl>    | <span data-ttu-id="a1ac2-132">Si se especifica, el control Rich Edit transmite únicamente el contenido de la selección actual.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-132">If specified, the rich edit control streams out only the contents of the current selection.</span></span> <span data-ttu-id="a1ac2-133">Si no se especifica, el control transmite todo el contenido.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-133">If not specified, the control streams out the entire contents.</span></span> <span data-ttu-id="a1ac2-134">Puede combinar esta marca con cualquiera de los valores de formato de datos.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-134">You can combine this flag with any of data format values.</span></span><br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="a1ac2-135"><dt>**SF \_ UNIcode**</dt></span><span class="sxs-lookup"><span data-stu-id="a1ac2-135"><dt>**SF\_UNICODE**</dt></span></span> </dl>             | <span data-ttu-id="a1ac2-136">**Microsoft Rich Edit 2,0 y versiones posteriores:** Indica texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-136">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="a1ac2-137">Puede combinar esta marca con la marca **de \_ texto SF** .</span><span class="sxs-lookup"><span data-stu-id="a1ac2-137">You can combine this flag with the **SF\_TEXT** flag.</span></span><br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <span data-ttu-id="a1ac2-138"><dt>**el \_ USECODEPAGE de SF**</dt></span><span class="sxs-lookup"><span data-stu-id="a1ac2-138"><dt>**SF\_USECODEPAGE**</dt></span></span> </dl> | <span data-ttu-id="a1ac2-139">**Edición enriquecida 3,0 y versiones posteriores:** Genera RTF UTF-8 así como texto mediante otras páginas de códigos.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-139">**Rich Edit 3.0 and later:** Generates UTF-8 RTF as well as text using other code pages.</span></span> <span data-ttu-id="a1ac2-140">La página de códigos se establece en la palabra alta de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-140">The code page is set in the high word of *wParam*.</span></span> <span data-ttu-id="a1ac2-141">Por ejemplo, en el caso de RTF UTF-8, establezca *wParam* en (CP \_ UTF8 << 16) \| CF \_ USECODEPAGE \| SF \_ RTF.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-141">For example, for UTF-8 RTF, set *wParam* to (CP\_UTF8 << 16) \| SF\_USECODEPAGE \| SF\_RTF.</span></span><br/>                               |



 

</dd> <dt>

<span data-ttu-id="a1ac2-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1ac2-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1ac2-143">Puntero a una estructura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="a1ac2-143">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="a1ac2-144">En la entrada, el miembro **pfnCallback** de esta estructura debe apuntar a una función [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-144">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="a1ac2-145">En la salida, el miembro **dwError** puede contener un código de error distinto de cero si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-145">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1ac2-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1ac2-146">Return value</span></span>

<span data-ttu-id="a1ac2-147">Este mensaje devuelve el número de caracteres escritos en el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-147">This message returns the number of characters written to the data stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1ac2-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1ac2-148">Remarks</span></span>

<span data-ttu-id="a1ac2-149">Cuando se envía un **mensaje \_ STREAMOUT em** , el control Rich Edit realiza llamadas repetidas a la función [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) especificada por el miembro **pfnCallback** de la estructura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="a1ac2-149">When you send an **EM\_STREAMOUT** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="a1ac2-150">Cada vez que llama a la función de devolución de llamada, el control pasa un búfer que contiene una parte del contenido del control.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-150">Each time it calls the callback function, the control passes a buffer containing a portion of the contents of the control.</span></span> <span data-ttu-id="a1ac2-151">Este proceso continúa hasta que el control ha pasado todo su contenido a la función de devolución de llamada o hasta que se produce un error.</span><span class="sxs-lookup"><span data-stu-id="a1ac2-151">This process continues until the control has passed all its contents to the callback function, or until an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1ac2-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1ac2-152">Requirements</span></span>



| <span data-ttu-id="a1ac2-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1ac2-153">Requirement</span></span> | <span data-ttu-id="a1ac2-154">Value</span><span class="sxs-lookup"><span data-stu-id="a1ac2-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1ac2-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1ac2-155">Minimum supported client</span></span><br/> | <span data-ttu-id="a1ac2-156">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a1ac2-156">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1ac2-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1ac2-157">Minimum supported server</span></span><br/> | <span data-ttu-id="a1ac2-158">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1ac2-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1ac2-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1ac2-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1ac2-160"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1ac2-160"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1ac2-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1ac2-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1ac2-162">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a1ac2-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a1ac2-163">**EDITSTREAM**</span><span class="sxs-lookup"><span data-stu-id="a1ac2-163">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="a1ac2-164">*EditStreamCallback*</span><span class="sxs-lookup"><span data-stu-id="a1ac2-164">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="a1ac2-165">**\_secuencia em**</span><span class="sxs-lookup"><span data-stu-id="a1ac2-165">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 





