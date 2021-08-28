---
description: Configuración de la codificación de vídeo
ms.assetid: 917600f5-5580-4ca5-bce9-70eadec40df7
title: Configuración de la codificación de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c6cb95a0bbe13ac9311bd55d45c67b3bcf4d0fc671fc6e6a6c3731081c2e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974844"
---
# <a name="configuring-video-encoding-microsoft-media-foundation"></a>Configuración de la codificación de vídeo (Microsoft Media Foundation)

Para configurar el codificador de vídeo, realice los pasos siguientes:

1.  Establezca todas las propiedades del codificador DMO mediante **IPropertyBag::Write**. En la lista siguiente se resume el conjunto mínimo de propiedades necesarias para codificar una secuencia de vídeo CBR (todos estos valores tienen valores predeterminados que se pueden usar):

    -   La[propiedad MFPKEY \_ VIDEOWINDOW](mfpkey-videowindowproperty.md) especifica la ventana de búfer que se usará para la secuencia. Para obtener más información sobre la configuración de las ventanas de búfer y cómo afecta al contenido, vea [Métodos de codificación](encodingmethods.md). La ventana de búfer predeterminada es de tres segundos, lo que es adecuado para muchos escenarios.
    -   La complejidad del vídeo se establece para determinar el equilibrio entre la calidad del contenido codificado y el tiempo necesario para codificar. Si no establece un valor, se usa el valor predeterminado. Sin embargo, puede encontrar los modos recomendados para un códec específico llamando a [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) para recuperar g \_ wszWMVCComplexityExLive, g \_ wszWMVCComplexityExOffline y g \_ wszWMVCComplexityExMax. A continuación, puede [establecer MFPKEY \_ COMPLEXITYEX](mfpkey-complexityexproperty.md) en un valor entre 0 y la complejidad máxima notificada.
    -   [MFPKEY \_ SOAP](mfpkey-crispproperty.md) especifica la importancia relativa de la subilidad del vídeo y la calidad de imagen de los fotogramas codificados. En la mayoría de los casos, el valor predeterminado funciona bien.
    -   Para el contenido de vídeo almacenado en un contenedor distinto de ASF, la propiedad [ \_ ASFOVERHEADPERFRAME de MFPKEY](mfpkey-asfoverheadperframeproperty.md) debe establecerse en 0. Este no es el valor predeterminado.

    Para obtener información sobre cómo configurar secuencias de VBR, vea [Using VBR Encoding](usingvbrencoding.md).

2.  Configure la [**DMO \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) para el tipo de entrada o, si usa el SDK de Media Foundation, use la función [**MFInitMediaTypeFromVideoInfoHeader.**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) Use una [**estructura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que describa el contenido de entrada sin comprimir. El códec no cambia el tamaño del vídeo ni convierte el espacio de color.
3.  Establezca el tipo de entrada [**mediante IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) o [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).
4.  Configure el tipo de salida para el codificador. Una vez establecido el tipo de entrada, el codificador enumera los tipos de salida que están completos, excepto el **miembro dwBitrate** de la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o el atributo [**MF MT AVG \_ \_ \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) de la interfaz [**MFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) Si recupera un tipo de salida antes de establecer un tipo de entrada, la estructura [**\_ DMO MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) no tendrá asociado **videoinfoheader.**
5.  Recupere los datos privados del códec y anexe a la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que se pasa a la estructura [**DMO MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) o [**a IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype). Para obtener más información, consulte [Uso de datos privados de códec de vídeo.](usingvideocodecprivatedata.md)
6.  Establezca el tipo de salida mediante una llamada [**al método IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) o [**IMFTransform::SetOutputType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) Pase la estructura [**\_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) de DMO con la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) completada (incluidos los datos privados anexados) a la que se hace referencia en el miembro **pbFormat,** o bien construya [**un VALOR DE TIPO DE MÉTODOSINFORMES**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) mediante una llamada a [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader).

> [!Note]  
> El objeto de codificador de vídeo admite dos salidas. La segunda salida es para el codificador "vista posterior". Entrega las muestras sin comprimir, ya que se entregarán desde el descodificador. Esto le permite supervisar la calidad de la codificación sin tener que esperar hasta que se procese toda la secuencia. Esta salida es opcional. Si desea usarlo, configure su tipo siguiendo el mismo proceso que se usa para establecer el tipo de entrada del codificador.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 
