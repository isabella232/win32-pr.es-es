---
description: El receptor de archivos ASF es una implementación de IMFMediaSink proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia ASF en un archivo. Para obtener información sobre el modelo de objetos de los receptores de medios ASF y el uso general, consulte receptores multimedia ASF.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Agregar información de secuencias al receptor de archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e08c6997d9c77836f379d4ca7b75720ddea245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715089"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a>Agregar información de secuencias al receptor de archivos ASF

El receptor de archivos ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia ASF en un archivo. Para obtener información sobre el modelo de objetos y el uso general de los receptores de medios ASF, consulte [receptores de medios ASF](asf-media-sinks.md).

Después de crear una instancia del receptor de archivos, debe configurarse antes de compilar la topología. El receptor de archivos debe conocer las secuencias del archivo de salida, la información del modo de codificación y los metadatos. En este tema se describe el proceso de agregar una secuencia en el receptor de archivos.

-   [Agregar secuencias en el receptor de archivos ASF](#adding-streams-in-the-asf-file-sink)
-   [Enumerar receptores de secuencia](#enumerating-stream-sinks)
-   [Temas relacionados](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a>Agregar secuencias en el receptor de archivos ASF

El receptor de archivos debe conocer los flujos de salida y sus propiedades para que pueda generar ejemplos de salida en consecuencia y agregarlos al archivo ASF de salida. Esta configuración se escribe en el objeto de encabezado ASF final.

Para establecer la información de la secuencia, debe tener una referencia al objeto ContentInfo ASF del receptor de archivo. Para obtener información, consulte [crear el receptor de archivos ASF](creating-the-asf-file-sink.md).

En el procedimiento siguiente se resumen los pasos generales para configurar Stream mediante el uso del objeto de perfil ASF.

**Para configurar la información de la secuencia en el receptor de archivos ASF**

1.  Cree un objeto de perfil ASF llamando a [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).
2.  Para cada secuencia del archivo de salida, cree un tipo de medio para la secuencia de destino que se va a agregar al receptor de archivos. El tipo de medio debe ser compatible con los tipos de salida admitidos por los codificadores de Windows Media.

    Para obtener información acerca de cómo agregar secuencias de audio al perfil, consulte crear secuencias de audio para la codificación ASF.

    Para obtener información acerca de cómo agregar secuencias de vídeo al perfil, consulte crear secuencias de vídeo para la codificación ASF.

3.  Cree secuencias basadas en los tipos de medios creados en el paso 2 llamando a [**IMFASFProfile:: CreateStream (**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).
4.  Asigne un número de secuencia para la secuencia recién creada mediante una llamada al puntero de la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) recibido en el paso 3.
5.  Opcionalmente, configure la secuencia con la siguiente información:
    -   Parámetros de depósito con fugas estableciendo los atributos: [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) o [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
    -   Extensión de carga, exclusión mutua mediante una llamada a métodos [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .
6.  Opcionalmente, puede establecer el tamaño de los paquetes de datos para el perfil estableciendo los atributos [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) y [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) . El perfil ASF expone la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , a la que una aplicación puede obtener referencia llamando a **IMFASFProfile:: QueryInterface**.
7.  Establezca la información de codificación de la secuencia en el receptor de archivos. Se describe en [configuración de las propiedades del receptor de archivos](setting-properties-in-the-file-sink.md).
8.  Agregue la secuencia al perfil llamando a [**IMFASFProfile:: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).
9.  Asocie el perfil con el objeto ContentInfo llamando a [**IMFASFContentInfo:: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).

Para modificar una secuencia existente, la aplicación puede obtener una referencia a la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) del flujo y volver a configurarla según los requisitos. Para agregar o quitar secuencias, la aplicación debe llamar a [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream). Para aplicar estos cambios, las modificaciones o la eliminación de secuencias, debe volver a establecer el perfil en el objeto ContentInfo. Esto sobrescribe el perfil existente que ya está asociado al objeto ContentInfo.


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a>Enumerar receptores de secuencia

Para cada secuencia del perfil que sea consciente del objeto ContentInfo, el receptor de archivos ASF crea y agrega un receptor de flujo que contiene todas las propiedades de la secuencia codificada. El receptor de archivos ASF está diseñado para contener secuencias fijas. Esto significa que no puede Agregar o quitar secuencias mediante una llamada a [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) o [**IMFMediaSink:: RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink). Estas llamadas en el receptor de archivo dan error con \_ el \_ código de error fijo MF E STREAMSINKS \_ . La adición o eliminación de secuencias en el perfil no agrega ni quita automáticamente los receptores de la secuencia en el receptor de archivos. Debe descartar la instancia existente del archivo y volver a crearla con la nueva información de la secuencia si han cambiado las secuencias en el perfil.

El procedimiento siguiente resume los pasos generales para enumerar los receptores de secuencias en el receptor de archivos ASF.

**Para enumerar los receptores de la secuencia**

1.  Llame a [**IMFMediaSink:: GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) para obtener el número total de receptores de flujo en el receptor de archivos ASF.
2.  Recorrer los receptores de flujo Ang obtener una referencia a la interfaz [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) del receptor de flujo.

    O bien

    Llame a [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) para obtener el receptor de flujo especificando el número de secuencia. Cada receptor de flujo se identifica con el número de secuencia que estableció al crear la secuencia en el perfil.

Si va a crear una topología parcial para codificar un archivo multimedia, debe agregar el receptor de archivos a la topología como un nodo de topología de salida. Puede hacerlo especificando cada receptor de vapor en el receptor de archivos o estableciendo el objeto de activación del receptor de archivos y los identificadores del receptor de la secuencia. Para obtener más información y ejemplos de código, vea [crear nodos de salida](creating-output-nodes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Receptores de medios ASF](asf-media-sinks.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



