---
description: Contiene un GUID de formato de DirectShow para un tipo de medio.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: MF_MT_AM_FORMAT_TYPE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360513"
---
# <a name="mf_mt_am_format_type-attribute"></a>MF \_ MT \_ AM \_ \_ atributo de tipo Format

Contiene un GUID de formato de DirectShow para un tipo de medio.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

Este atributo se puede establecer cuando un tipo de medio de DirectShow se convierte en un tipo de medio Media Foundation. El atributo indica el tipo de formato de DirectShow original. El valor corresponde al miembro FormatType de la estructura [**de \_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

En el caso de un formato de audio, el atributo de [**\_ datos de \_ usuario \_ MF MT**](mf-mt-user-data-attribute.md) podría contener el bloque de formato original, si no se reconoció el tipo de formato DirectShow.

No establezca este atributo en un tipo de medio a menos que esté convirtiendo una estructura de formato de DirectShow.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Conversiones de tipos de medios](media-type-conversions.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> <dt>

[**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**MFCreateMediaTypeFromRepresentation**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
