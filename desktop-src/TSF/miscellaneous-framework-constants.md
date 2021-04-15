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
# <a name="miscellaneous-framework-constants"></a>Constantes de marco de trabajo variadas

Las constantes de marco de trabajo variadas indican la configuración de clientes, procesos o texto.



| Constante o valor                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <dt>**TF \_ CLIENTID \_ null**</dt> <dt>((TfClientId) 0)</dt> </dl>                        | Indica a un servicio de texto que el cliente está desactivado. Vea [TfClientId](tfclientid.md).<br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <dt>**TF \_ \_GUIDATOM no válido**</dt> <dt>((TfGuidAtom) 0)</dt> </dl>               | El valor de [TfGuidAtom](tfguidatom.md) para el proceso actual no es válido.<br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <dt>**TF \_ \_selección predeterminada**</dt> <dt>( \_ selección predeterminada de TS \_ )</dt> </dl> | Usar la selección predeterminada. Usado por [ITfContext:: getSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP:: getSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)y [ITextStoreAnchor:: getSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).<br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <dt>**TF \_ GTP \_ incl \_**</dt> . <dt></dt> </dl>                               | Especifica que el método [ITfEditRecord:: GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) obtendrá la colección de objetos de intervalo que cubren el texto modificado durante la sesión de edición.<br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <dt>**TF \_ \_Objeto HF**</dt> <dt>(1)</dt> </dl>                                              | El desplazamiento de intervalo se detiene si se encuentra un objeto incrustado. Se usa en el miembro **dwFlags** de la estructura [TF \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) .<br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <dt>**TF \_ \_Corrección de IE**</dt> <dt>(1)</dt> </dl>                                  | El texto es una transformación (corrección) de contenido existente, de modo que otros servicios de texto puedan conservar los datos asociados con el texto original. Se usa en el parámetro *dwFlags* de [ITfRange:: InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).<br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <dt>**TF \_ \_Cookie no válida**</dt> <dt>(0xFFFFFFFF)</dt> </dl>                      | No se utiliza.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <dt>**TF \_ \_ \_ Cookie de edición no válida**</dt> <dt>(0)</dt> </dl>               | No se utiliza.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <dt>**TF \_ POPF \_ All**</dt> <dt>(0x1)</dt> </dl>                                               | Todos los contextos se quitan de la pila. Se usa en el parámetro *dwFlags* de [ITfDocumentMgr::P OP](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).<br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <dt>**TF \_ \_Corrección de St**</dt> <dt>(1)</dt> </dl>                                  | El texto es una transformación (corrección) de contenido existente, de modo que otros servicios de texto puedan conservar los datos asociados con el texto original. Se usa en el parámetro *dwFlags* de [ITfRange:: setText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).<br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <dt>**TF \_ \_Corrección de tu**</dt> <dt>(0x1)</dt> </dl>                                | El cambio de texto es el resultado de una transformación (corrección) de contenido existente. Esto implica que la semántica del texto no ha cambiado. Se usa en el parámetro *dwFlags* de [ITfPropertyStore:: OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).<br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <dt>**TF \_ \_HIDETIPUI de EE. UU.**</dt> <dt></dt> </dl>                                | No se utiliza.<br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ITextStoreACP:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
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

[ITfRange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[TF \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





