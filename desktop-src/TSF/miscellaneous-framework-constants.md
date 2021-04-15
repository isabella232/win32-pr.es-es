---
title: Constantes de marco de trabajo variadas (msctf. h)
description: Las constantes de marco de trabajo variadas indican la configuración de clientes, procesos o texto.
ms.assetid: fa53c1f1-50eb-45eb-b2ea-f236a376d41a
topic_type:
- apiref
api_name:
- TF_CLIENTID_NULL
- TF_INVALID_GUIDATOM
- TF_DEFAULT_SELECTION
- TF_GTP_INCL_TEXT
- TF_HF_OBJECT
- TF_IE_CORRECTION
- TF_INVALID_COOKIE
- TF_INVALID_EDIT_COOKIE
- TF_POPF_ALL
- TF_ST_CORRECTION
- TF_TU_CORRECTION
- TF_US_HIDETIPUI
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9eab083f6763d4244d0720b04c2a22744febc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492316"
---
# <a name="miscellaneous-framework-constants"></a><span data-ttu-id="1670f-103">Constantes de marco de trabajo variadas</span><span class="sxs-lookup"><span data-stu-id="1670f-103">Miscellaneous Framework Constants</span></span>

<span data-ttu-id="1670f-104">Las constantes de marco de trabajo variadas indican la configuración de clientes, procesos o texto.</span><span class="sxs-lookup"><span data-stu-id="1670f-104">Miscellaneous framework constants indicate settings for clients, processes, or text.</span></span>



| <span data-ttu-id="1670f-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="1670f-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="1670f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="1670f-106">Description</span></span>                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <span data-ttu-id="1670f-107"><dt>**TF \_ CLIENTID \_ null**</dt> <dt>((TfClientId) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="1670f-107"><dt>**TF\_CLIENTID\_NULL**</dt> <dt>((TfClientId)0)</dt></span></span> </dl>                        | <span data-ttu-id="1670f-108">Indica a un servicio de texto que el cliente está desactivado.</span><span class="sxs-lookup"><span data-stu-id="1670f-108">Indicates to a text service that the client is deactivated.</span></span> <span data-ttu-id="1670f-109">Vea [TfClientId](tfclientid.md).</span><span class="sxs-lookup"><span data-stu-id="1670f-109">See [TfClientId](tfclientid.md).</span></span><br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <span data-ttu-id="1670f-110"><dt>**TF \_ \_GUIDATOM no válido**</dt> <dt>((TfGuidAtom) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="1670f-110"><dt>**TF\_INVALID\_GUIDATOM**</dt> <dt>((TfGuidAtom)0)</dt></span></span> </dl>               | <span data-ttu-id="1670f-111">El valor de [TfGuidAtom](tfguidatom.md) para el proceso actual no es válido.</span><span class="sxs-lookup"><span data-stu-id="1670f-111">The [TfGuidAtom](tfguidatom.md) value for the current process is invalid.</span></span><br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <span data-ttu-id="1670f-112"><dt>**TF \_ \_selección predeterminada**</dt> <dt>( \_ selección predeterminada de TS \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="1670f-112"><dt>**TF\_DEFAULT\_SELECTION**</dt> <dt>( TS\_DEFAULT\_SELECTION )</dt></span></span> </dl> | <span data-ttu-id="1670f-113">Usar la selección predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1670f-113">Use the default selection.</span></span> <span data-ttu-id="1670f-114">Usado por [ITfContext:: getSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP:: getSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)y [ITextStoreAnchor:: getSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).</span><span class="sxs-lookup"><span data-stu-id="1670f-114">Used by [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection), and [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).</span></span><br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <span data-ttu-id="1670f-115"><dt>**TF \_ GTP \_ incl \_**</dt> . <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1670f-115"><dt>**TF\_GTP\_INCL\_TEXT**</dt> <dt>( 0x1 )</dt></span></span> </dl>                               | <span data-ttu-id="1670f-116">Especifica que el método [ITfEditRecord:: GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) obtendrá la colección de objetos de intervalo que cubren el texto modificado durante la sesión de edición.</span><span class="sxs-lookup"><span data-stu-id="1670f-116">Specifies that the [ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) method will obtain the collection of range objects that cover the text changed during the edit session.</span></span><br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <span data-ttu-id="1670f-117"><dt>**TF \_ \_Objeto HF**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="1670f-117"><dt>**TF\_HF\_OBJECT**</dt> <dt>( 1 )</dt></span></span> </dl>                                              | <span data-ttu-id="1670f-118">El desplazamiento de intervalo se detiene si se encuentra un objeto incrustado.</span><span class="sxs-lookup"><span data-stu-id="1670f-118">The range shift stops if an embedded object is encountered.</span></span> <span data-ttu-id="1670f-119">Se usa en el miembro **dwFlags** de la estructura [TF \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) .</span><span class="sxs-lookup"><span data-stu-id="1670f-119">Used in **dwFlags** member of [TF\_HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) structure.</span></span><br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <span data-ttu-id="1670f-120"><dt>**TF \_ \_Corrección de IE**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="1670f-120"><dt>**TF\_IE\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="1670f-121">El texto es una transformación (corrección) de contenido existente, de modo que otros servicios de texto puedan conservar los datos asociados con el texto original.</span><span class="sxs-lookup"><span data-stu-id="1670f-121">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="1670f-122">Se usa en el parámetro *dwFlags* de [ITfRange:: InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).</span><span class="sxs-lookup"><span data-stu-id="1670f-122">Used in *dwFlags* parameter of [ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).</span></span><br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <span data-ttu-id="1670f-123"><dt>**TF \_ \_Cookie no válida**</dt> <dt>(0xFFFFFFFF)</dt></span><span class="sxs-lookup"><span data-stu-id="1670f-123"><dt>**TF\_INVALID\_COOKIE**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                      | <span data-ttu-id="1670f-124">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1670f-124">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <span data-ttu-id="1670f-125"><dt>**TF \_ \_ \_ Cookie de edición no válida**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="1670f-125"><dt>**TF\_INVALID\_EDIT\_COOKIE**</dt> <dt>( 0 )</dt></span></span> </dl>               | <span data-ttu-id="1670f-126">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1670f-126">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <span data-ttu-id="1670f-127"><dt>**TF \_ POPF \_ All**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="1670f-127"><dt>**TF\_POPF\_ALL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                               | <span data-ttu-id="1670f-128">Todos los contextos se quitan de la pila.</span><span class="sxs-lookup"><span data-stu-id="1670f-128">All contexts are removed from the stack.</span></span> <span data-ttu-id="1670f-129">Se usa en el parámetro *dwFlags* de [ITfDocumentMgr::P OP](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).</span><span class="sxs-lookup"><span data-stu-id="1670f-129">Used in *dwFlags* parameter of [ITfDocumentMgr::Pop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).</span></span><br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <span data-ttu-id="1670f-130"><dt>**TF \_ \_Corrección de St**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="1670f-130"><dt>**TF\_ST\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="1670f-131">El texto es una transformación (corrección) de contenido existente, de modo que otros servicios de texto puedan conservar los datos asociados con el texto original.</span><span class="sxs-lookup"><span data-stu-id="1670f-131">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="1670f-132">Se usa en el parámetro *dwFlags* de [ITfRange:: setText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).</span><span class="sxs-lookup"><span data-stu-id="1670f-132">Used in *dwFlags* parameter of [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).</span></span><br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <span data-ttu-id="1670f-133"><dt>**TF \_ \_Corrección de tu**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="1670f-133"><dt>**TF\_TU\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                | <span data-ttu-id="1670f-134">El cambio de texto es el resultado de una transformación (corrección) de contenido existente.</span><span class="sxs-lookup"><span data-stu-id="1670f-134">The text change is the result of a transform (correction) of existing content.</span></span> <span data-ttu-id="1670f-135">Esto implica que la semántica del texto no ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="1670f-135">This implies that the semantics of the text have not changed.</span></span> <span data-ttu-id="1670f-136">Se usa en el parámetro *dwFlags* de [ITfPropertyStore:: OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).</span><span class="sxs-lookup"><span data-stu-id="1670f-136">Used in *dwFlags* parameter of [ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).</span></span><br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <span data-ttu-id="1670f-137"><dt>**TF \_ \_HIDETIPUI de EE. UU.**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1670f-137"><dt>**TF\_US\_HIDETIPUI**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="1670f-138">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1670f-138">Not used.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="1670f-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1670f-139">Requirements</span></span>



| <span data-ttu-id="1670f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="1670f-140">Requirement</span></span> | <span data-ttu-id="1670f-141">Value</span><span class="sxs-lookup"><span data-stu-id="1670f-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1670f-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1670f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1670f-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1670f-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1670f-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1670f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1670f-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1670f-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1670f-146">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1670f-146">Redistributable</span></span><br/>          | <span data-ttu-id="1670f-147">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1670f-147">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="1670f-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1670f-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="1670f-149"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="1670f-149"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="1670f-150">IDL</span><span class="sxs-lookup"><span data-stu-id="1670f-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1670f-151"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1670f-151"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1670f-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="1670f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1670f-153">ITextStoreACP:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="1670f-153">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="1670f-154">ITextStoreAnchor::GetSelection</span><span class="sxs-lookup"><span data-stu-id="1670f-154">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[<span data-ttu-id="1670f-155">ITfContext::GetSelection</span><span class="sxs-lookup"><span data-stu-id="1670f-155">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="1670f-156">ITfDocumentMgr::P op</span><span class="sxs-lookup"><span data-stu-id="1670f-156">ITfDocumentMgr::Pop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[<span data-ttu-id="1670f-157">ITfEditRecord::GetTextAndPropertyUpdates</span><span class="sxs-lookup"><span data-stu-id="1670f-157">ITfEditRecord::GetTextAndPropertyUpdates</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[<span data-ttu-id="1670f-158">ITfPropertyStore::OnTextUpdated</span><span class="sxs-lookup"><span data-stu-id="1670f-158">ITfPropertyStore::OnTextUpdated</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[<span data-ttu-id="1670f-159">ITfRange::InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="1670f-159">ITfRange::InsertEmbedded</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[<span data-ttu-id="1670f-160">ITfRange:: SetText</span><span class="sxs-lookup"><span data-stu-id="1670f-160">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="1670f-161">TfClientId</span><span class="sxs-lookup"><span data-stu-id="1670f-161">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="1670f-162">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="1670f-162">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="1670f-163">TF \_ HALTCOND</span><span class="sxs-lookup"><span data-stu-id="1670f-163">TF\_HALTCOND</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





