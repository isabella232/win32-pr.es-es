---
title: Mensaje EM_STREAMIN (RichEdit. h)
description: Reemplaza el contenido de un control Rich Edit por un flujo de datos proporcionado por una aplicación definida \ 8211; Función de devolución de llamada EditStreamCallback.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- EM_STREAMIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_STREAMIN
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fdcf844cce09cf5c49085a9fcf08a38ad988ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492167"
---
# <a name="em_streamin-message"></a><span data-ttu-id="30523-104">\_Mensaje de secuencia em</span><span class="sxs-lookup"><span data-stu-id="30523-104">EM\_STREAMIN message</span></span>

<span data-ttu-id="30523-105">Reemplaza el contenido de un control Rich Edit por un flujo de datos proporcionado por una función de devolución de llamada [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="30523-105">Replaces the contents of a rich edit control with a stream of data provided by an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span>

## <a name="parameters"></a><span data-ttu-id="30523-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30523-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30523-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30523-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30523-108">Especifica el formato de datos y las opciones de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="30523-108">Specifies the data format and replacement options.</span></span> <span data-ttu-id="30523-109">Este valor debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="30523-109">This value must be one of the following values.</span></span>



| <span data-ttu-id="30523-110">Value</span><span class="sxs-lookup"><span data-stu-id="30523-110">Value</span></span>                                                                                                                                       | <span data-ttu-id="30523-111">Significado</span><span class="sxs-lookup"><span data-stu-id="30523-111">Meaning</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="30523-112"><dt>**RTF de SF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="30523-112"><dt>**SF\_RTF**</dt></span></span> </dl>    | <span data-ttu-id="30523-113">RTF</span><span class="sxs-lookup"><span data-stu-id="30523-113">RTF</span></span><br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="30523-114"><dt>**\_texto SF**</dt></span><span class="sxs-lookup"><span data-stu-id="30523-114"><dt>**SF\_TEXT**</dt></span></span> </dl> | <span data-ttu-id="30523-115">Texto</span><span class="sxs-lookup"><span data-stu-id="30523-115">Text</span></span><br/> |



 

<span data-ttu-id="30523-116">Además, puede especificar las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="30523-116">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="30523-117">Value</span><span class="sxs-lookup"><span data-stu-id="30523-117">Value</span></span>                                                                                                                                                         | <span data-ttu-id="30523-118">Significado</span><span class="sxs-lookup"><span data-stu-id="30523-118">Meaning</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="30523-119"><dt>**SFF \_ PLAINRTF**</dt></span><span class="sxs-lookup"><span data-stu-id="30523-119"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>    | <span data-ttu-id="30523-120">Si se especifica, solo se transmiten en secuencias las palabras clave comunes a todos los lenguajes.</span><span class="sxs-lookup"><span data-stu-id="30523-120">If specified, only keywords common to all languages are streamed in.</span></span> <span data-ttu-id="30523-121">Se omiten las palabras clave RTF específicas del lenguaje en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="30523-121">Language-specific RTF keywords in the stream are ignored.</span></span> <span data-ttu-id="30523-122">Si no se especifica, todas las palabras clave se transmiten en.</span><span class="sxs-lookup"><span data-stu-id="30523-122">If not specified, all keywords are streamed in.</span></span> <span data-ttu-id="30523-123">Puede combinar esta marca con la marca **de \_ RTF de SF** .</span><span class="sxs-lookup"><span data-stu-id="30523-123">You can combine this flag with the **SF\_RTF** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="30523-124"><dt>**selección de SFF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="30523-124"><dt>**SFF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="30523-125">Si se especifica, el flujo de datos reemplaza el contenido de la selección actual.</span><span class="sxs-lookup"><span data-stu-id="30523-125">If specified, the data stream replaces the contents of the current selection.</span></span> <span data-ttu-id="30523-126">Si no se especifica, el flujo de datos reemplaza todo el contenido del control.</span><span class="sxs-lookup"><span data-stu-id="30523-126">If not specified, the data stream replaces the entire contents of the control.</span></span> <span data-ttu-id="30523-127">Puede combinar esta marca con el **\_ texto SF** o las marcas de **\_ RTF de SF** .</span><span class="sxs-lookup"><span data-stu-id="30523-127">You can combine this flag with the **SF\_TEXT** or **SF\_RTF** flags.</span></span><br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="30523-128"><dt>**SF \_ UNIcode**</dt></span><span class="sxs-lookup"><span data-stu-id="30523-128"><dt>**SF\_UNICODE**</dt></span></span> </dl>          | <span data-ttu-id="30523-129">**Microsoft Rich Edit 2,0 y versiones posteriores:** Indica texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="30523-129">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="30523-130">Puede combinar esta marca con la marca **de \_ texto SF** .</span><span class="sxs-lookup"><span data-stu-id="30523-130">You can combine this flag with the **SF\_TEXT** flag.</span></span> <br/>                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="30523-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30523-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30523-132">Puntero a una estructura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="30523-132">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="30523-133">En la entrada, el miembro **pfnCallback** de esta estructura debe apuntar a una función [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="30523-133">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="30523-134">En la salida, el miembro **dwError** puede contener un código de error distinto de cero si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="30523-134">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30523-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30523-135">Return value</span></span>

<span data-ttu-id="30523-136">Este mensaje devuelve el número de caracteres leídos.</span><span class="sxs-lookup"><span data-stu-id="30523-136">This message returns the number of characters read.</span></span>

## <a name="remarks"></a><span data-ttu-id="30523-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30523-137">Remarks</span></span>

<span data-ttu-id="30523-138">Cuando se envía un mensaje de **\_ secuencia em** , el control Rich Edit realiza llamadas repetidas a la función [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) especificada por el miembro **pfnCallback** de la estructura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="30523-138">When you send an **EM\_STREAMIN** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="30523-139">Cada vez que se llama a la función de devolución de llamada, rellena un búfer con los datos que se van a leer en el control.</span><span class="sxs-lookup"><span data-stu-id="30523-139">Each time the callback function is called, it fills a buffer with data to read into the control.</span></span> <span data-ttu-id="30523-140">Esto continúa hasta que la función de devolución de llamada indica que se ha completado la operación de transmisión por secuencias o se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="30523-140">This continues until the callback function indicates that the stream-in operation has been completed or an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="30523-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30523-141">Requirements</span></span>



| <span data-ttu-id="30523-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="30523-142">Requirement</span></span> | <span data-ttu-id="30523-143">Value</span><span class="sxs-lookup"><span data-stu-id="30523-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30523-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30523-144">Minimum supported client</span></span><br/> | <span data-ttu-id="30523-145">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="30523-145">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30523-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30523-146">Minimum supported server</span></span><br/> | <span data-ttu-id="30523-147">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="30523-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30523-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30523-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="30523-149"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="30523-149"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30523-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="30523-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="30523-151">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="30523-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="30523-152">**EDITSTREAM**</span><span class="sxs-lookup"><span data-stu-id="30523-152">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="30523-153">*EditStreamCallback*</span><span class="sxs-lookup"><span data-stu-id="30523-153">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="30523-154">**\_STREAMOUT em**</span><span class="sxs-lookup"><span data-stu-id="30523-154">**EM\_STREAMOUT**</span></span>](em-streamout.md)
</dt> </dl>

 

 





