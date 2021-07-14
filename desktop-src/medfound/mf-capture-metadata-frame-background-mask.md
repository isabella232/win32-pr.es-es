---
description: Notifica los metadatos y el búfer de máscara para una máscara de segmentación de fondo que distingue entre el fondo y el primer plano de un fotograma de vídeo.
title: MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK atributo (Mfapi.h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 3dc28d92566b14a44f61fe84bd3f68688c464d4a
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691866"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a>Atributo MF \_ CAPTURE METADATA FRAME BACKGROUND \_ \_ \_ \_ MASK

Notifica los metadatos y el búfer de máscara para una máscara de segmentación de fondo que distingue entre el fondo y el primer plano de un fotograma de vídeo.

## <a name="data-type"></a>Tipo de datos

**Blob**

## <a name="remarks"></a>Observaciones

Los datos que lleva este atributo son una estructura [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) que contiene información sobre las dimensiones de la máscara de fondo, así como su cobertura del marco del que se deduce, que es el marco que genera la secuencia. También lleva un búfer contiguo que representa la máscara que va a aprovechar la aplicación consumidora para definir qué píxeles se consideran parte del primer plano o el fondo. La aplicación consumidora controla la correlación de escala y coordenada de imagen de la máscara con respecto al marco. 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Compilación 22000t<br/>                          |
| Servidor mínimo compatible<br/> | Windows Compilación 22000<br/>                      |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 




