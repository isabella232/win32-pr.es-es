---
title: Constantes de almacén de texto varios (Textstor.h)
description: Las constantes de almacén de texto varios establecen ciertas propiedades para los almacenes de texto.
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55bfa06f7f0ebda1d572a4e637076de25c7a21ef4d273cdc2527ab6481393404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952103"
---
# <a name="miscellaneous-text-store-constants"></a>Constantes de almacén de texto varios

Las constantes de almacén de texto varios establecen ciertas propiedades para los almacenes de texto.



| Constante o valor                                                                                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <dt>**TS \_ SELECCIÓN \_ PREDETERMINADA**</dt> <dt>( ( ULONG )-1 )</dt> </dl> | Si el *parámetro ulIndex* de [ITfContext::GetSelection se](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) establece en este valor, se obtiene la selección predeterminada.<br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <dt>**TS \_ HIDDEN \_ HIDDEN**</dt> <dt>( 0x1 )</dt> </dl>                              | Si *el parámetro dwFlags* de [ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) está establecido en este valor, se puede encontrar un objeto incrustado dentro del texto oculto.<br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <dt>**TS \_ GTA \_ HIDDEN**</dt> <dt>( 0x1 )</dt> </dl>                              | No se usa.<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <dt>**TS \_ CORRECCIÓN \_ ST**</dt> <dt>( 0x1 )</dt> </dl>                     | Si el parámetro *dwFlags* de [ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)o [ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) se establece en este valor, el texto es una transformación (corrección) del contenido existente y se conserva cualquier información de marcado de texto especial (metadatos), como datos de archivo .wav o un identificador de lenguaje.<br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <dt>**TS \_ CORRECCIÓN \_ DE TC**</dt> <dt>( 0x1 )</dt> </dl>                     | Si el parámetro *dwFlags* de [ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) se establece en este valor, el texto es una transformación (corrección) del contenido existente y se conserva cualquier información de marcado de texto especial (metadatos), como datos de archivo .wav o un identificador de idioma.<br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <dt>**TS \_ VCOOKIE \_ NUL**</dt> <dt>( 0xffffffff )</dt> </dl>                    | TSF lo usa internamente.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                         |
| Header<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[Constantes de marco de trabajo varias](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





