---
description: Notifica los metadatos y el búfer de máscara para una máscara de segmentación de fondo que distingue entre el fondo y el primer plano de un fotograma de vídeo.
title: MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK atributo (Mfapi.h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 1c9cf48235483f13cfa6f9fc04aace5baaf030cf1eb2597b86e9361176a0b9b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973984"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a>Atributo MF \_ CAPTURE METADATA FRAME BACKGROUND \_ \_ \_ \_ MASK

Notifica los metadatos y el búfer de máscara para una máscara de segmentación de fondo que distingue entre el fondo y el primer plano de un fotograma de vídeo.

## <a name="data-type"></a>Tipo de datos

**Blob**

## <a name="remarks"></a>Comentarios

Los datos que lleva este atributo son una estructura [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) que contiene información sobre las dimensiones de la máscara de fondo, así como su cobertura del marco del que se deduce, que es el marco que genera la secuencia. También lleva un búfer contiguo que representa la máscara que va a aprovechar la aplicación de consumo para definir qué píxeles se consideran parte del primer plano o del fondo. La aplicación consumidora controla la correlación de escala y coordenada de imagen de la máscara con respecto al marco. 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Compilación 22000t<br/>                          |
| Servidor mínimo compatible<br/> | Windows Compilación 22000<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 




