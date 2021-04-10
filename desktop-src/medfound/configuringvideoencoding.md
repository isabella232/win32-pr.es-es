---
description: Configuración de la codificación de vídeo
ms.assetid: 917600f5-5580-4ca5-bce9-70eadec40df7
title: Configuración de la codificación de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd82240ea9f540f283e0fb6340c06be00336226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153662"
---
# <a name="configuring-video-encoding-microsoft-media-foundation"></a>Configuración de la codificación de vídeo (Microsoft Media Foundation)

Para configurar el codificador de vídeo, realice los pasos siguientes:

1.  Establezca las propiedades en el codificador DMO mediante **IPropertyBag:: Write**. En la lista siguiente se resume el conjunto mínimo de propiedades necesarias para codificar una secuencia de vídeo CBR (todos estos valores tienen valores predeterminados que se pueden usar):

    -   La propiedad[MFPKEY \_ VideoWindow](mfpkey-videowindowproperty.md) especifica la ventana del búfer que se va a utilizar para la secuencia. Para obtener más información sobre la configuración de Windows de búfer y cómo afecta al contenido, consulte [métodos de codificación](encodingmethods.md). La ventana del búfer predeterminado es de tres segundos, que es adecuada para muchos escenarios.
    -   La complejidad del vídeo se establece para determinar el equilibrio entre la calidad del contenido codificado y el tiempo necesario para codificar. Si no establece un valor, se usa el valor predeterminado. Sin embargo, puede encontrar los modos recomendados para un códec específico mediante una llamada a [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) para recuperar g \_ wszWMVCComplexityExLive, g \_ wszWMVCComplexityExOffline y g \_ wszWMVCComplexityExMax. Después, puede establecer [MFPKEY \_ COMPLEXITYEX](mfpkey-complexityexproperty.md) en un valor comprendido entre 0 y la complejidad máxima detectada.
    -   [MFPKEY \_ NÍTIDO](mfpkey-crispproperty.md) especifica la importancia relativa del suavizado de vídeo y la calidad de la imagen de los fotogramas codificados. En la mayoría de los casos, el valor predeterminado funciona bien.
    -   Para el contenido de vídeo almacenado en un contenedor que no sea ASF, la propiedad [MFPKEY \_ ASFOVERHEADPERFRAME](mfpkey-asfoverheadperframeproperty.md) debe establecerse en 0. Este no es el valor predeterminado.

    Para obtener información sobre la configuración de secuencias VBR, consulte [usar la codificación VBR](usingvbrencoding.md).

2.  Configure la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) para el tipo de entrada o, si usa el SDK de Media Foundation, utilice la función [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) . Use una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que describa el contenido de entrada sin comprimir. El códec no cambia el tamaño del vídeo ni convierte el espacio de colores.
3.  Establezca el tipo de entrada mediante [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) o [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).
4.  Configure el tipo de salida del codificador. Una vez establecido el tipo de entrada, el codificador enumera los tipos de salida que se completan, excepto el miembro **dwBitrate** de la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , o el atributo de [**velocidad de \_ \_ \_ bits promedio MF MT**](mf-mt-avg-bitrate-attribute.md) de la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Si recupera un tipo de salida antes de establecer un tipo de entrada, la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) entregada no tendrá una **VIDEOINFOHEADER** asociada.
5.  Recupere los datos privados del códec y agréguelo a la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que pasa a la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) o a [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype). Para obtener más información, consulte [uso de datos privados de códecs de vídeo](usingvideocodecprivatedata.md).
6.  Establezca el tipo de salida llamando al método [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) o [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) . Pase la estructura [**de \_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) con la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) completada (incluidos los datos privados anexados) a la que se hace referencia en el miembro **PbFormat** o construya un [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) llamando a [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader).

> [!Note]  
> El objeto de codificador de vídeo admite dos salidas. La segunda salida es para el codificador "post View". Entrega los ejemplos sin comprimir, ya que se entregarán desde el descodificador. Esto le permite supervisar la calidad de la codificación sin tener que esperar hasta que se procese toda la secuencia. Esta salida es opcional. Si desea usarlo, configure su tipo siguiendo el mismo proceso que se usa para establecer el tipo de entrada del codificador.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 
