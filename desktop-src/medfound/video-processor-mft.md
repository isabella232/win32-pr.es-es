---
description: La MFT del procesador de vídeo es una transformación de Microsoft Media Foundation (MFT) que realiza la conversión de ColorSpace, el cambio de tamaño de vídeo, el desentrelazado, la conversión de velocidad de fotogramas, la rotación, el recorte, el espacio de la izquierda y la derecha espacial y la creación de reflejo.
ms.assetid: 1476995A-9692-4B08-8EF7-7DB6321BEC24
title: MFT del procesador de vídeo (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53783b42073414e4dc440546698bf295b404dcc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718975"
---
# <a name="video-processor-mft"></a>MFT del procesador de vídeo

La MFT del procesador de vídeo es una transformación de Microsoft Media Foundation (MFT) que realiza la conversión de ColorSpace, el cambio de tamaño de vídeo, el desentrelazado, la conversión de velocidad de fotogramas, la rotación, el recorte, el espacio de la izquierda y la derecha espacial y la creación de reflejo.

## <a name="clsid"></a>CLSID

CLSID \_ VideoProcessorMFT

## <a name="interfaces"></a>Interfaces

-   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFVideoProcessorControl**](/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol)

## <a name="input-formats"></a>Formatos de entrada

-   **MFVideoFormat \_ ARGB32**
-   **MFVideoFormat \_ AYUV**
-   **MFVideoFormat \_ i420**
-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV11**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ RGB24**
-   **MFVideoFormat \_ RGB32**
-   **MFVideoFormat \_ RGB555**
-   **MFVideoFormat \_ RGB565**
-   **MFVideoFormat \_ RGB8**
-   **MFVideoFormat \_ UYVY**
-   **MFVideoFormat \_ V410**
-   **MFVideoFormat \_ Y216**
-   **MFVideoFormat \_ Y41P**
-   **MFVideoFormat \_ Y41T**
-   **MFVideoFormat \_ Y42T**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**
-   **MFVideoFormat \_ YVYU**

## <a name="output-formats"></a>Formatos de salida

-   **MFVideoFormat \_ ARGB32**
-   **MFVideoFormat \_ AYUV**
-   **MFVideoFormat \_ i420**
-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ RGB24**
-   **MFVideoFormat \_ RGB32**
-   **MFVideoFormat \_ RGB555**
-   **MFVideoFormat \_ RGB565**
-   **MFVideoFormat \_ UYVY**
-   **MFVideoFormat \_ Y216**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

No se admiten todas las combinaciones de formatos de entrada y salida. Para probar si se admite una conversión, establezca el tipo de entrada y, a continuación, llame a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).

Para obtener más información sobre estos formatos, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).

## <a name="remarks"></a>Observaciones

Se puede crear una instancia del procesador de vídeo de una de las siguientes maneras:

-   Llamando a [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). El procesador de vídeo se registra en la categoría **MFT \_ categoría de \_ \_ procesador de vídeo** .
-   Llamando a la función de COM **CoCreateInstance** pasándole el CLSID CLSID **\_ VideoProcessorMFT**.

Los comentarios siguientes se refieren al trabajo con rectángulos de origen y rectángulos de destino en la **MFT del procesador de vídeo**. Los rectángulos de origen y de destino se establecen con [**IMFVideoProcessorControl:: SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) y [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) y algunas veces con [**IMFMediaEngineEx:: UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).

-   El rectángulo de origen se debe alinear y redondear para que coincida con los requisitos del formato de color del fotograma que se encuentra en el procesador de vídeo. Esto es importante porque los formatos como 420 y 422 tienen requisitos sobre las dimensiones y los desplazamientos que se pueden crear y a los que se puede tener acceso. Por ejemplo, un rectángulo de origen de {1, 0, 319, 240} (izquierda, superior, derecha, inferior) se redondeará a {2, 0, 320, 240} cuando el formato de entrada sea 420.
-   Tanto el rectángulo de origen como el de destino siempre se fijarán para caber dentro de sus marcos respectivos, el rectángulo de origen y el rectángulo de destino hasta el marco de destino. Esto significa que los valores negativos no son significativos; siempre se fijarán en 0.
-   El rectángulo de origen se encuentra en el sistema de coordenadas del marco de destino, menos cualquier rectángulo de destino. Esto significa que las transformaciones como la rotación se "deshacen" en el rectángulo de origen. Por lo tanto, no es necesario saber si el vídeo se ha girado o si se ha desempaquetado 3D. Por ejemplo, puede dibujar un rectángulo en la parte superior de la etiqueta de vídeo, tomar las coordenadas relativas (con respecto a la etiqueta de vídeo), normalizarlas (intervalo de 0 a 1) y pasarlas como rectángulo de origen y deben funcionar según lo previsto, incluso si el vídeo se está girando.

El procesador de vídeo admite el procesamiento de vídeo acelerado mediante GPU con Microsoft Direct3D 11. Para obtener más información, consulte [MF \_ SA \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md).

### <a name="stereoscopic-video"></a>Vídeo de Stereoscopic

El procesador de vídeo admite la operación ver desempaquetado en fotogramas de vídeo 3D:

Si el marco de entrada contiene dos vistas empaquetadas en el mismo fotograma, el procesador de vídeo puede dividir las vistas en búferes independientes, o bien extraer la vista base y descartar la segunda vista. Para habilitar ver desempaquetado, establezca el atributo [MF \_ enable \_ 3DVIDEO \_ Output](mf-enable-3dvideo-output.md) en **MF3DVideoOutputType \_ Stereo** o **MF3DVideoOutputType \_ BaseView**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




