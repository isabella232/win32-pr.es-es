---
description: Uso de la Windows imagen de Media Video 9.1
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: Uso de la Windows imagen de Media Video 9.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c630be78ec3edef1a47322b31f6a2331f15134a0cdffa4107b5a79daa86e9091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972634"
---
# <a name="using-the-windows-media-video-91-image-category"></a>Uso de la Windows imagen de Media Video 9.1

La Windows imagen de Media Video 9.1 es diferente de las otras categorías de salida admitidas por el codificador y descodificador Windows Media Video 9. En lugar de procesar vídeo sin comprimir, toma muestras de entrada especiales que constan de datos de transformación estructurados y, en ocasiones, imágenes de mapa de bits RGB en las que se realizan las transformaciones.

El contenido codificado de Windows Media Video 9.1 Image es prácticamente idéntico al contenido codificado normal de Windows Media Video 9, pero se identifica mediante su propio FOURCC ("WMVP").

El tipo de salida del codificador para la imagen de vídeo se establece exactamente de la misma manera que el vídeo multimedia estándar de Windows, salvo que los valores de subtipo y compresión deben establecerse en los identificadores de imagen de vídeo. Esto incluye la necesidad de obtener datos privados de códec y anexar a la [**estructura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) Para obtener más información, vea [Configuring Video Encoding](configuringvideoencoding.md).

La configuración del tipo de entrada para la imagen de vídeo también es muy similar a la configuración de entrada para los demás codificadores de vídeo. Puede recuperar un tipo DMO [**\_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) parcialmente completado del codificador mediante una llamada a [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)o, si usa el SDK de Media Foundation, llame a [**MFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) y recupere DMO **MEDIA \_ \_ TYPE** mediante [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype). A continuación, establezca el tamaño del fotograma y la [**estructura de formato VIDEOINFOHEADER,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) tal como lo haría para el vídeo estándar. Al igual que con el tipo de salida, debe asegurarse de que los valores de subtipo y compresión se establecen correctamente.

## <a name="creating-input-samples"></a>Creación de ejemplos de entrada

Los ejemplos de entrada para el códec de imagen de vídeo están estructurados. La definición de la estructura y las constantes usadas para la imagen de vídeo no se incluyen con las interfaces de códecs Windows audio multimedia y vídeo. Estas definiciones se incluyen en el SDK Windows Media Format y su uso se explica completamente en la documentación del SDK Windows Media Format.

## <a name="decoding"></a>Descodificación

No hay ningún requisito especial para la decodificación de vídeo de captura de pantalla. Aparte de un subtipo diferente (MEDIASUBTYPE WMVP) que se usa para la entrada del descodificador, la secuencia de imágenes de vídeo comprimida es esencialmente idéntica a una secuencia de vídeo \_ multimedia Windows estándar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 
