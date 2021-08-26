---
description: Especifica si está habilitado el modo de panorámica o examen.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: MF_MT_PAN_SCAN_ENABLED atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e78c38cd15f5d735d49b5689905a40d74614b46817a8621ce1dabcdc5a1b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955495"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>Atributo MF \_ MT \_ PAN SCAN \_ \_ ENABLED

Especifica si está habilitado el modo de panorámica o examen.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Comentarios

Si este atributo es **TRUE**, solo se debe mostrar la región de exploración y panorámica del vídeo. La región de panorámica/examen se especifica mediante el atributo [**MF MT PAN SCAN \_ \_ \_ \_ APERTURE.**](mf-mt-pan-scan-aperture-attribute.md)

Si este atributo es **FALSE o** no está establecido, se debe mostrar toda la apertura de pantalla del vídeo. El apertura de la pantalla se especifica mediante el atributo [**MF MT MINIMUM DISPLAY \_ \_ \_ \_ APERTURE.**](mf-mt-minimum-display-aperture-attribute.md)

Si establece este atributo en **TRUE,** establezca también el valor del atributo [**MF MT PAN SCAN \_ \_ \_ \_ APERTURE.**](mf-mt-pan-scan-aperture-attribute.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> <dt>

[Relación de aspecto de la imagen](picture-aspect-ratio.md)
</dt> </dl>

 

 




