---
description: Obtenga información sobre cómo agregar información de flujo al receptor de archivos de ASF, que una aplicación puede usar para archivar datos multimedia de ASF en un archivo.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Agregar información de flujo al receptor de archivos de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0273f6080293803db7fa7451460e8f8d7700c5e405b9ed09d8d35e384abc8ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975044"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a>Agregar información de flujo al receptor de archivos de ASF

El receptor de archivos ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia de ASF en un archivo. Para obtener información sobre el modelo de objetos de los receptores de medios de ASF y el uso general, vea [Receptores de medios de ASF.](asf-media-sinks.md)

Después de crear una instancia del receptor de archivos, debe configurarse antes de compilar la topología. El receptor del archivo debe conocer los flujos del archivo de salida, la información del modo de codificación y los metadatos. En este tema se describe el proceso de agregar secuencia en el receptor de archivos.

-   [Agregar Secuencias en el receptor de archivos de ASF](#adding-streams-in-the-asf-file-sink)
-   [Enumeración de receptores de flujo](#enumerating-stream-sinks)
-   [Temas relacionados](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a>Agregar Secuencias en el receptor de archivos de ASF

El receptor del archivo debe conocer los flujos de salida y sus propiedades para que pueda generar ejemplos de salida en consecuencia y agregarlos al archivo ASF de salida. Esta configuración se escribe en el objeto de encabezado asf final.

Para establecer la información de flujo, debe tener una referencia al objeto ContentInfo de ASF del receptor de archivos. Para obtener información, vea [Creating the ASF File Sink](creating-the-asf-file-sink.md).

En el procedimiento siguiente se resumen los pasos generales para configurar la secuencia mediante el objeto de perfil de ASF.

**Para configurar la información de flujo en el receptor de archivos de ASF**

1.  Cree un objeto de perfil de ASF llamando [**a MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).
2.  Para cada secuencia del archivo de salida, cree un tipo de medio para la secuencia de destino que se va a agregar en el receptor del archivo. El tipo de medio debe ser compatible con los tipos de salida admitidos por Windows codificadores multimedia.

    Para obtener información sobre cómo agregar secuencias de audio al perfil, vea Creating Audio Secuencias for ASF Encoding (Creación de secuencias de audio para codificación ASF).

    Para obtener información sobre cómo agregar secuencias de vídeo al perfil, consulte Creating Video Secuencias for ASF Encoding (Creación de secuencias de vídeo para codificación ASF).

3.  Cree secuencias basadas en los tipos de medios creados en el paso 2 mediante una llamada [**a IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).
4.  Asigne un número de secuencia para la secuencia recién creada mediante una llamada al puntero de interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) recibido en el paso 3.
5.  Opcionalmente, configure la secuencia con la siguiente información:
    -   Parámetros de cubo de pérdida estableciendo los atributos: [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) o [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
    -   Extensión de carga útil, exclusión mutua mediante una llamada [**a los métodos DE TIPO IMFASFStreamConfig.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
6.  Opcionalmente, establezca el tamaño del paquete de datos para el perfil estableciendo los atributos [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) y [**MF \_ ASFPROFILE \_ MAXPACKETSIZE.**](mf-asfprofile-maxpacketsize-attribute.md) El perfil de ASF expone la interfaz [**DEFAttributes,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) a la que una aplicación puede obtener referencia mediante una llamada a **IMFASFProfile::QueryInterface**.
7.  Establezca la información de codificación para la secuencia en el receptor de archivos. Se describe en [Establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md).
8.  Agregue la secuencia al perfil mediante una llamada [**a IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).
9.  Asocie el perfil al objeto ContentInfo llamando a [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).

Para modificar una secuencia existente, la aplicación puede obtener una referencia a la interfaz [**DEFSTREAMConfig DE LA SECUENCIA**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) Y volver a configurarla según los requisitos. Para agregar o quitar secuencias, la aplicación debe llamar a [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream). Para aplicar estos cambios, modificaciones de secuencias o eliminación, debe volver a establecer el perfil en el objeto ContentInfo. Esto sobrescribe el perfil existente que ya está asociado al objeto ContentInfo.


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



## <a name="enumerating-stream-sinks"></a>Enumeración de receptores de flujo

Para cada secuencia del perfil de la que el objeto ContentInfo es consciente, el receptor del archivo ASF crea y agrega un receptor de flujo que contiene todas las propiedades de la secuencia codificada. El receptor de archivos asf está diseñado para contener secuencias fijas. Esto significa que no se pueden agregar ni quitar secuencias llamando a [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) o [**IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink). Estas llamadas en el receptor de archivos producirán un error con el código \_ de error CORREGIDO MF E \_ STREAMSINKS. \_ La adición o eliminación de secuencias en el perfil no agrega ni quita automáticamente los receptores de flujo en el receptor de archivos. Debe descartar la instancia existente del archivo y volver a crearla con información de secuencia nueva si las secuencias del perfil han cambiado.

En el procedimiento siguiente se resumen los pasos generales para enumerar los receptores de flujo en el receptor de archivos de ASF.

**Para enumerar los receptores de flujo**

1.  Llame [**a IMFMediaSink::GetStreamSinkCount para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) obtener el número total de receptores de flujo en el receptor de archivos asf.
2.  Recorrer en bucle los receptores de flujo para obtener una referencia a la interfaz [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) del receptor de secuencias.

    O bien

    Llame [**a IMFMediaSink::GetStreamSinkById para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) obtener el receptor del flujo especificando el número de secuencia. Cada receptor de flujo se identifica con el número de secuencia que estableció al crear la secuencia en el perfil.

Si va a crear una topología parcial para codificar un archivo multimedia, debe agregar el receptor de archivos a la topología como nodo de topología de salida. Puede hacerlo especificando cada receptor de flujo en el receptor de archivos o estableciendo el objeto de activación del receptor de archivos y los identificadores de receptor del flujo. Para obtener más información y ejemplo de código, vea [Crear nodos de salida.](creating-output-nodes.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Receptores de medios de ASF](asf-media-sinks.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



