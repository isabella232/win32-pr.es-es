---
description: Uso de la Windows imagen de Media Video 9.1
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: Uso de la Windows imagen de Media Video 9.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b545d37b61a1c89ffdd69615b28f636aa98b32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363655"
---
# <a name="using-the-windows-media-video-91-image-category"></a>Uso de la Windows imagen de Media Video 9.1

La Windows imagen de Media Video 9.1 es diferente de las otras categorías de salida admitidas por el codificador y descodificador Windows Media Video 9. En lugar de procesar vídeo sin comprimir, toma muestras de entrada especiales que constan de datos de transformación estructurados y, en ocasiones, imágenes de mapa de bits RGB en las que se realizan las transformaciones.

El contenido de Windows media video 9.1 codificado es prácticamente idéntico al contenido codificado normal de Windows Media Video 9, pero se identifica mediante su propio FOURCC ("WMVP").

El tipo de salida del codificador para la imagen de vídeo se establece exactamente de la misma manera que el vídeo multimedia estándar de Windows, salvo que los valores de subtipo y compresión deben establecerse en los identificadores de imagen de vídeo. Esto incluye la necesidad de obtener datos privados de códec y anexar a la [**estructura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) Para obtener más información, vea [Configuring Video Encoding](configuringvideoencoding.md).

La configuración del tipo de entrada para la imagen de vídeo también es muy similar a la configuración de entrada para los demás codificadores de vídeo. Puede recuperar un DMO [**\_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) parcialmente completado del codificador mediante una llamada a [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype), o si usa el SDK de Media Foundation, llamando a [**MFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) y recuperando DMO **MEDIA \_ \_ TYPE** mediante [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype). A continuación, establezca el tamaño del fotograma y la [**estructura de formato VIDEOINFOHEADER,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) tal como lo haría para el vídeo estándar. Al igual que con el tipo de salida, debe asegurarse de que los valores de subtipo y compresión se establecen correctamente.

## <a name="creating-input-samples"></a>Creación de ejemplos de entrada

Los ejemplos de entrada para el códec de imagen de vídeo están estructurados. La definición de la estructura y las constantes usadas para la imagen de vídeo no se incluyen con las interfaces de códec de audio y vídeo multimedia Windows de vídeo. Estas definiciones se incluyen en Windows SDK de formato multimedia y su uso se explica completamente en la documentación del SDK Windows Media Format.

## <a name="decoding"></a>Descodificación

No hay ningún requisito especial para la decodificación de vídeo de captura de pantalla. Aparte de un subtipo diferente (MEDIASUBTYPE WMVP) usado para la entrada del descodificador, la secuencia de imágenes de vídeo comprimida es esencialmente idéntica a una secuencia de vídeo multimedia \_ Windows estándar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 
