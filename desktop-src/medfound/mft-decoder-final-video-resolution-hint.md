---
description: Especifica la resolución de salida final de la imagen descodificada, después del procesamiento de vídeo.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847a2925f2249c741e9a45a1dcc4826a1cbe3d6bb12cda4d8017ee0fb5de0069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973144"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a>Atributo MFT \_ DECODER FINAL VIDEO RESOLUTION \_ \_ \_ \_ HINT

Especifica la resolución de salida final de la imagen descodificada, después del procesamiento de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Comentarios

Algunos descodificadores de vídeo admiten este atributo. Una aplicación puede establecer este atributo para indicar el ancho y alto de la imagen después del procesamiento de vídeo. El descodificador puede usar esta información para optimizar el proceso de descodificación, especialmente si el tamaño final de la imagen es mucho menor que el tamaño de la imagen nativa. Por ejemplo, el descodificador podría omitir un filtro fuera de bucle.

Los 32 bits superiores contienen el ancho y los 32 bits inferiores contienen el alto.

Para establecer este atributo:

1.  Llame [**a IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el descodificador para obtener un [**puntero DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
2.  Llame [**a MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) para agregar el atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




