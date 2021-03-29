---
description: Permite el procesamiento de vídeo avanzado por el lector de origen, incluida la conversión del espacio de colores, el desentrelazado, el cambio de tamaño de vídeo y la conversión de velocidad de fotogramas.
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6978239c5c1c466c78a310b38b5d10bd41f9e004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541355"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a>\_Lector de código fuente MF \_ \_ Habilitar atributo de \_ \_ procesamiento de vídeo avanzado \_

Permite el procesamiento de vídeo avanzado por el [lector de origen](source-reader.md), incluida la conversión del espacio de colores, el desentrelazado, el cambio de tamaño de vídeo y la conversión de velocidad de fotogramas.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

Si este atributo es **true**, el lector de origen puede insertar un procesador de vídeo en la canalización de procesamiento, lo que permite los siguientes tipos de conversión de formato:

-   Conversión de espacio de colores (YUV a RGB-32)
-   Desentrelazado
-   Cambio de tamaño de vídeo
-   Conversión de velocidad de fotogramas

Si este atributo es **true**, el atributo [MF \_ ReadWrite \_ Disable \_ Converters](mf-readwrite-disable-converters.md) debe ser **false**.

El lector de origen busca los procesadores de vídeo que están registrados en la categoría de **\_ \_ \_ procesador de vídeo categoría de MFT** , incluidos los MFTs registrados para el proceso local. (Consulte [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) para obtener más información sobre el registro local de MFTs). El lector de origen usa el procesador de vídeo de Transcode (XVP) si no se encuentra ningún otro procesador de vídeo adecuado.

La aplicación especifica el tipo de salida deseado llamando a [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype). Cuando el lector de origen configura el procesador de vídeo, intenta coincidir con los siguientes atributos del tipo de salida:

-   Velocidad de fotogramas ([ \_ \_ \_ velocidad de fotogramas MF MT](mf-mt-frame-rate-attribute.md))
-   Tamaño de marco ([MF \_ MT \_ Frame \_ size](mf-mt-frame-size-attribute.md))
-   Modo entrelazado[( \_ \_ \_ modo entrelazado MF MT](mf-mt-interlace-mode-attribute.md))
-   Relación de aspecto de píxeles ([ \_ relación de aspecto de \_ píxeles \_ \_ MF MT](mf-mt-pixel-aspect-ratio-attribute.md))
-   Subtipo ([ \_ \_ subtipo MF MT](mf-mt-subtype-attribute.md))

Este atributo es similar al del [ \_ lector de código fuente MF habilitar el atributo de \_ \_ \_ \_ procesamiento de vídeo](mf-source-reader-enable-video-processing.md) , pero ofrece las siguientes ventajas:

-   Se admite un mayor número de conversiones de formato.
-   Las aplicaciones pueden registrar sus propios convertidores.
-   Algunas conversiones se pueden realizar en el hardware mediante la GPU.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[Atributos del lector de código fuente](source-reader-attributes.md)
</dt> </dl>

 

 




