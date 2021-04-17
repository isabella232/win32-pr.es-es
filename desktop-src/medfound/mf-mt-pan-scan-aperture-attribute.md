---
description: Define la abertura Pan/Scan, que es la 4&\# 215; 3 región del vídeo que se debe mostrar en el modo Pan/Scan.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: MF_MT_PAN_SCAN_APERTURE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696640"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a>MF \_ MT \_ pan \_ scan \_ abertura atributo

Define la abertura Pan/Scan, que es la región de vídeo de 4 × 3 que se debe mostrar en el modo Pan/Scan.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

El valor del atributo es una estructura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

Este atributo se usa para recortar el vídeo de pantalla panorámica a una relación de aspecto de 4:3. La abertura Pan/Scan solo se usa en el modo Pan/Scan, que se habilita estableciendo el atributo [**MF \_ MT \_ pan \_ scan \_ Enabled**](mf-mt-pan-scan-enabled-attribute.md) en **true**.

Si el modo de desplazamiento/exploración no está habilitado, use la abertura de la pantalla, especificada por el atributo [**MF \_ MT \_ Minimum \_ Display \_ abertura**](mf-mt-minimum-display-aperture-attribute.md) .

Si no se establece este atributo, se supone que la abertura de exploración o pan es todo el fotograma de vídeo.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Relación de aspecto de la imagen](picture-aspect-ratio.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**\_ \_ apertura geométrica de MF MT \_**](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[**\_ \_ apertura mínima de \_ pantalla MF MT \_**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**examen de pan de MF \_ MT \_ \_ \_ habilitado**](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




