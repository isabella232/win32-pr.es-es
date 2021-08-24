---
title: Constantes de marco de trabajo varias (Msctf.h)
description: Varias constantes de marco indican la configuración de clientes, procesos o texto.
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
ms.openlocfilehash: f9bcd6ad253e71d662cbc713398e65c6a250863e18a9fe2d461a2d93717fb7b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906015"
---
# <a name="miscellaneous-framework-constants"></a>Constantes de marco de trabajo varias

Varias constantes de marco indican la configuración de clientes, procesos o texto.



| Constante o valor                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <dt>**TF \_ CLIENTID \_ NULL**</dt> <dt>((TfClientId)0)</dt> </dl>                        | Indica a un servicio de texto que el cliente está desactivado. Vea [TfClientId](tfclientid.md).<br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <dt>**TF \_ \_GUIDATOM NO VÁLIDO**</dt> <dt>((TfGuidAtom)0)</dt> </dl>               | El [valor de TfGuidAtom](tfguidatom.md) para el proceso actual no es válido.<br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <dt>**TF \_ SELECCIÓN \_ PREDETERMINADA**</dt> <dt>( TS SELECCIÓN PREDETERMINADA \_ \_ )</dt> </dl> | Use la selección predeterminada. Usado por [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP::GetSelection e](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).<br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <dt>**TF \_ GTP \_ INCL \_ TEXT**</dt> <dt>( 0x1 )</dt> </dl>                               | Especifica que el [método ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) obtendrá la colección de objetos de intervalo que cubren el texto cambiado durante la sesión de edición.<br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <dt>**TF \_ OBJECT \_ DE OBJECT (**</dt> <dt>1 )</dt> </dl>                                              | El desplazamiento de intervalo se detiene si se encuentra un objeto incrustado. Se usa **en el miembro dwFlags** [de la estructura \_ HALTCOND de](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) TF.<br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <dt>**TF \_ CORRECCIÓN \_ DE E/S**</dt> <dt>( 1 )</dt> </dl>                                  | El texto es una transformación (corrección) del contenido existente, por lo que otros servicios de texto pueden conservar los datos asociados al texto original. Se usa *en el parámetro dwFlags* [de ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).<br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <dt>**TF \_ COOKIE \_ NO VÁLIDA**</dt> ( 0xffffffff <dt>)</dt> </dl>                      | No se usa.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <dt>**TF \_ EDITAR \_ \_ COOKIE NO VÁLIDA**</dt> ( <dt>0 )</dt> </dl>               | No se usa.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <dt>**TF \_ POPF \_ ALL**</dt> <dt>( 0x1 )</dt> </dl>                                               | Todos los contextos se quitan de la pila. Se usa *en el parámetro dwFlags* [de ITfDocumentMgr::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).<br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <dt>**TF \_ CORRECCIÓN \_ DE ST**</dt> ( <dt>1 )</dt> </dl>                                  | El texto es una transformación (corrección) del contenido existente, por lo que otros servicios de texto pueden conservar los datos asociados al texto original. Se usa *en el parámetro dwFlags* [de ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).<br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <dt>**TF \_ TU \_ CORRECTION**</dt> <dt>( 0x1 )</dt> </dl>                                | El cambio de texto es el resultado de una transformación (corrección) del contenido existente. Esto implica que la semántica del texto no ha cambiado. Se usa *en el parámetro dwFlags* [de ITfPropertyStore::OnTextUpdated.](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)<br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <dt>**TF \_ US \_ HIDETIPUI**</dt> <dt>0x00000001</dt> </dl>                                | No se usa.<br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                      |
| Header<br/>                   | <dl> <dt>Msctf.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITfDocumentMgr::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[TF \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





