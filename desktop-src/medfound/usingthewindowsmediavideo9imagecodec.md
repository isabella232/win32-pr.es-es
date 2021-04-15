---
description: Uso de la categoría de imagen Windows Media Video 9,1
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: Uso de la categoría de imagen Windows Media Video 9,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b545d37b61a1c89ffdd69615b28f636aa98b32
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689664"
---
# <a name="using-the-windows-media-video-91-image-category"></a>Uso de la categoría de imagen Windows Media Video 9,1

La categoría de imagen Windows Media Video 9,1 es diferente de las otras categorías de salida admitidas por el codificador y el descodificador de Windows Media Video 9. En lugar de procesar vídeo sin comprimir, toma ejemplos de entrada especiales que se componen de datos de transformación estructurados y, en ocasiones, imágenes de mapa de bits RGB en las que se realizan las transformaciones.

El contenido codificado Windows Media Video 9,1 de la imagen es prácticamente idéntico al contenido codificado normal de Windows Media Video 9, pero se identifica por su propio FOURCC ("WMVP").

El tipo de salida del codificador para la imagen de vídeo se establece exactamente de la misma manera que el vídeo estándar de Windows Media, con la excepción de que los valores de subtipo y compresión deben establecerse en los identificadores de imagen de vídeo. Esto incluye la necesidad de obtener datos privados de códec y anexarlos a la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Para obtener más información, consulte Configuración de la [codificación de vídeo](configuringvideoencoding.md).

La configuración del tipo de entrada para la imagen de vídeo también es muy similar a la configuración de entrada de los otros codificadores de vídeo. Puede recuperar un [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) parcialmente completado del codificador llamando a [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype), o bien, si usa el SDK de Media Foundation, llamando a [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) y recuperando el **tipo de \_ medio \_ DMO** mediante [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype). A continuación, establezca el tamaño de fotogramas y la estructura de formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , tal como lo haría para el vídeo estándar. Al igual que con el tipo de salida, debe asegurarse de que el subtipo y los valores de compresión se establecen adecuadamente.

## <a name="creating-input-samples"></a>Crear ejemplos de entrada

Los ejemplos de entrada para el códec de imagen de vídeo están estructurados. La definición de la estructura y las constantes que se usan para la imagen de vídeo no se incluyen con las interfaces de códec de vídeo y Windows Media Audio. Estas definiciones se incluyen en el SDK de Windows Media Format, y su uso se explica por completo en la documentación del SDK de Windows Media Format.

## <a name="decoding"></a>Descodificación

No hay ningún requisito especial para descodificar el vídeo de captura de pantalla. Aparte de un subtipo diferente (MEDIASUBTYPE \_ WMVP) que se usa para la entrada del descodificador, la secuencia de imagen de vídeo comprimida es esencialmente idéntica a una secuencia de Windows Media Video estándar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 
