---
description: Contiene un GUID DirectShow para un tipo de medio.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: MF_MT_AM_FORMAT_TYPE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff59e148f7532cc07e47acf033de91b5eaeb8969f0c39376850738fd54e758e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973634"
---
# <a name="mf_mt_am_format_type-attribute"></a>Atributo MF \_ MT \_ AM FORMAT \_ \_ TYPE

Contiene un GUID DirectShow para un tipo de medio.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Comentarios

Este atributo se puede establecer cuando un tipo DirectShow medio se convierte en un tipo Media Foundation medio. El atributo indica el tipo de formato DirectShow original. El valor corresponde al miembro formattype de la [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

En el caso de un formato de audio, el atributo [**MF \_ MT USER \_ \_ DATA**](mf-mt-user-data-attribute.md) puede contener el bloque de formato original, si no DirectShow el tipo de formato.

No establezca este atributo en un tipo de medio a menos que esté convirtiendo una estructura DirectShow formato.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Conversiones de tipos de medios](media-type-conversions.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**ATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**MFCreateMediaTypeFromRepresentation**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
