---
description: Especifica si el modo de panorámica/examen está habilitado.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: MF_MT_PAN_SCAN_ENABLED atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363970"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>Atributo MF \_ MT \_ PAN SCAN \_ \_ ENABLED

Especifica si el modo de panorámica/examen está habilitado.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Observaciones

Si este atributo es **TRUE,** solo se debe mostrar la región de panorámica o examen del vídeo. La región de panorámica y examen se especifica mediante el atributo [**MF MT PAN SCAN \_ \_ \_ \_ APERTURE.**](mf-mt-pan-scan-aperture-attribute.md)

Si este atributo es **FALSE o** no está establecido, se debe mostrar toda la apertura de pantalla del vídeo. El diafragma de presentación se especifica mediante el atributo [**MF MT MINIMUM DISPLAY \_ \_ \_ \_ APERTURE.**](mf-mt-minimum-display-aperture-attribute.md)

Si establece este atributo en **TRUE,** establezca también el valor del atributo [**MF MT PAN SCAN \_ \_ \_ \_ APERTURE.**](mf-mt-pan-scan-aperture-attribute.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Relación de aspecto de la imagen](picture-aspect-ratio.md)
</dt> </dl>

 

 




