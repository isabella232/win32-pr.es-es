---
description: Permite el procesamiento avanzado de vídeo mediante el Lector de origen, incluida la conversión de espacio de color, el desenlazado, el cambio de tamaño de vídeo y la conversión de velocidad de fotogramas.
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e873252dc67269124283b8e79760938d0f3302d348f21ea5506172cbe7b42ec3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113725"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a>ATRIBUTO ENABLE ADVANCED VIDEO PROCESSING DEL LECTOR DE ORIGEN \_ \_ \_ \_ \_ \_ DE MF

Permite el procesamiento avanzado de vídeo mediante el Lector de [origen,](source-reader.md)incluida la conversión de espacio de color, el desenlazado, el cambio de tamaño de vídeo y la conversión de velocidad de fotogramas.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

Si este atributo es **TRUE**, el Lector de origen puede insertar un procesador de vídeo en la canalización de procesamiento, lo que permite los siguientes tipos de conversión de formato:

-   Conversión de espacio de color (YUV a RGB-32)
-   Desentrelazado
-   Tamaño de vídeo
-   Conversión de velocidad de fotogramas

Si este atributo es **TRUE**, el atributo [MF \_ READWRITE \_ DISABLE \_ CONVERTERS](mf-readwrite-disable-converters.md) debe ser **FALSE.**

El Lector de origen busca procesadores de vídeo registrados en la categoría **MFT \_ CATEGORY VIDEO \_ \_ PROCESSOR,** incluidos los MFT registrados para el proceso local. (Vea [**MFTRegisterLocal para**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) obtener más información sobre el registro local de MFT). El Lector de origen usa el procesador de vídeo transcodificador (XVP) si no se encuentra ningún otro procesador de vídeo adecuado.

La aplicación especifica el tipo de salida deseado llamando [**a IMFSourceReader::SetCurrentMediaType.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) Cuando el Lector de origen configura el procesador de vídeo, intenta hacer coincidir los siguientes atributos del tipo de salida:

-   Velocidad de fotogramas ([MF \_ MT FRAME \_ \_ RATE](mf-mt-frame-rate-attribute.md))
-   Tamaño del marco ([MF \_ MT FRAME \_ \_ SIZE](mf-mt-frame-size-attribute.md))
-   Modo de interlace ([MF \_ MT \_ INTERLACE \_ MODE](mf-mt-interlace-mode-attribute.md))
-   Relación de aspecto de píxeles[(MF \_ MT PIXEL \_ ASPECT \_ \_ RATIO)](mf-mt-pixel-aspect-ratio-attribute.md)
-   Subtipo ([MF \_ MT \_ SUBTYPE](mf-mt-subtype-attribute.md))

Este atributo es similar al atributo [ENABLE VIDEO PROCESSING de MF \_ SOURCE \_ READER, \_ \_ \_ ](mf-source-reader-enable-video-processing.md) pero ofrece las siguientes ventajas:

-   Se admite una mayor variedad de conversiones de formato.
-   Las aplicaciones pueden registrar sus propios convertidores.
-   Algunas conversiones se pueden realizar en hardware mediante la GPU.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[Atributos del lector de origen](source-reader-attributes.md)
</dt> </dl>

 

 




