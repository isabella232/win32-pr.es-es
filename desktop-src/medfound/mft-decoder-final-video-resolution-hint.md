---
description: Especifica la resolución de salida final de la imagen descodificada, después del procesamiento de vídeo.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bbc0f01ef2a1d7062c6ab58c528b015383fc68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275842"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a>Atributo de sugerencia de \_ \_ resolución de vídeo final del \_ descodificador de MFT \_ \_

Especifica la resolución de salida final de la imagen descodificada, después del procesamiento de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Observaciones

Algunos descodificadores de vídeo admiten este atributo. Una aplicación puede establecer este atributo para indicar el ancho y el alto de la imagen después del procesamiento de vídeo. El descodificador puede utilizar esta información para optimizar el proceso de descodificación, especialmente si el tamaño de la imagen final es mucho menor que el tamaño de la imagen nativa. Por ejemplo, el descodificador podría omitir un filtro fuera de bucle.

Los 32 bits superiores contienen el ancho y los bits inferiores 32 contienen el alto.

Para establecer este atributo:

1.  Llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el descodificador para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Llame a [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) para agregar el atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de transformación](transform-attributes.md)
</dt> </dl>

 

 




