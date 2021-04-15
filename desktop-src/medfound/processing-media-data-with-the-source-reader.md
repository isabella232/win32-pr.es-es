---
description: En este tema se describe cómo usar el lector de origen para procesar datos multimedia.
ms.assetid: 583f5736-f767-47c5-8fdc-b3645aed59f6
title: Usar el lector de origen para procesar los datos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b19bce4d83298693825037aef92a220d78ed7c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361835"
---
# <a name="using-the-source-reader-to-process-media-data"></a>Usar el lector de origen para procesar los datos multimedia

En este tema se describe cómo usar el [lector de origen](source-reader.md) para procesar datos multimedia.

Para usar el lector de origen, siga estos pasos básicos:

1.  Cree una instancia del lector de origen.
2.  Enumerar los posibles formatos de salida.
3.  Establezca el formato de salida real para cada flujo.
4.  Procesa los datos del origen.

En el resto de este tema se describen estos pasos con detalle.

-   [Crear el lector de origen](#creating-the-source-reader)
-   [Enumerar formatos de salida](#enumerating-output-formats)
-   [Establecer formatos de salida](#setting-output-formats)
-   [Procesar datos multimedia](#using-the-source-reader-to-process-media-data)
-   [Purga de la canalización de datos](#draining-the-data-pipeline)
-   [Obtención de la duración del archivo](#getting-the-file-duration)
-   [Invoca](#seeking)
-   [Velocidad de reproducción](#playback-rate)
-   [Aceleración de hardware](#hardware-acceleration)
-   [Temas relacionados](#related-topics)

## <a name="creating-the-source-reader"></a>Crear el lector de origen

Para crear una instancia del lector de origen, llame a una de las siguientes funciones:



| Función                                                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)<br/>                                         | Toma una dirección URL como entrada. Esta función usa la [resolución de origen](source-resolver.md) para crear un origen multimedia a partir de la dirección URL.<br/>                                                                       |
| <span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)<br/>      | Toma un puntero a una secuencia de bytes. Esta función también utiliza la resolución de origen para crear el origen de medios.<br/>                                                                                        |
| <span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)<br/> | Toma un puntero a un origen de medios que ya se ha creado. Esta función es útil para los orígenes multimedia que la resolución de origen no puede crear, tales como los dispositivos de captura o los orígenes de medios personalizados.<br/> |



 

Normalmente, para los archivos multimedia, use [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl). En el caso de los dispositivos, como las cámaras Web, use [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource). (Para obtener más información acerca de la captura de dispositivos en Microsoft Media Foundation, consulte [captura de audio y vídeo](audio-video-capture.md)).

Cada una de estas funciones toma un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) opcional, que se usa para establecer varias opciones en el lector de origen, tal y como se describe en los temas de referencia de estas funciones. Para obtener el comportamiento predeterminado, establezca este parámetro en **null**. Cada función devuelve un puntero [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) como parámetro de salida. Debe llamar a la función **CoInitialize (ex)** y [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) antes de llamar a cualquiera de estas funciones.

En el código siguiente se crea el lector de origen a partir de una dirección URL.


```C++
int __cdecl wmain(int argc, __in_ecount(argc) PCWSTR* argv)
{
    if (argc < 2)
    {
        return 1;
    }

    const WCHAR *pszURL = argv[1];

    // Initialize the COM runtime.
    HRESULT hr = CoInitializeEx(0, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        // Initialize the Media Foundation platform.
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            // Create the source reader.
            IMFSourceReader *pReader;
            hr = MFCreateSourceReaderFromURL(pszURL, NULL, &pReader);
            if (SUCCEEDED(hr))
            {
                ReadMediaFile(pReader);
                pReader->Release();
            }
            // Shut down Media Foundation.
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="enumerating-output-formats"></a>Enumerar formatos de salida

Cada origen multimedia tiene al menos un flujo. Por ejemplo, un archivo de vídeo puede contener una secuencia de vídeo y una secuencia de audio. El formato de cada flujo se describe mediante un tipo de medio, representado por la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Para obtener más información sobre los tipos de medios, consulte [tipos de medios](media-types.md). Debe examinar el tipo de medio para comprender el formato de los datos que obtiene del lector de origen.

Inicialmente, cada flujo tiene un formato predeterminado, que se puede encontrar mediante una llamada al método [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) :

Para cada flujo, el origen multimedia ofrece una lista de los posibles tipos de medios para esa secuencia. El número de tipos depende del origen. Si el origen representa un archivo multimedia, normalmente solo hay un tipo por secuencia. Por otro lado, una cámara web podría transmitir vídeo en varios formatos distintos. En ese caso, la aplicación puede seleccionar el formato que se va a usar en la lista de tipos de medios.

Para obtener uno de los tipos de medios de un flujo, llame al método [**IMFSourceReader:: GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) . Este método toma dos parámetros de índice: el índice de la secuencia y un índice en la lista de tipos de medios para la secuencia. Para enumerar todos los tipos de una secuencia, aumente el índice de la lista manteniendo la constante de índice de la secuencia. Cuando el índice de la lista sale de los límites, **GetNativeMediaType** devuelve **MF \_ E \_ no hay \_ más \_ tipos**.


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



Para enumerar los tipos de medios de cada flujo, aumente el índice de la secuencia. Cuando el índice de la secuencia sale de los límites, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) devuelve **MF \_ E \_ INVALIDSTREAMNUMBER**.


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



## <a name="setting-output-formats"></a>Establecer formatos de salida

Para cambiar el formato de salida, llame al método [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) . Este método toma el índice de la secuencia y un tipo de medio:

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

En el caso del tipo de medio, depende de si desea insertar un descodificador.

-   Para obtener datos directamente del origen sin descodificarlos, use uno de los tipos devueltos por [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).
-   Para descodificar la secuencia, cree un nuevo tipo de medio que describa el formato no comprimido deseado.

En el caso del descodificador, cree el tipo de medio de la manera siguiente:

1.  Llame a [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) para crear un nuevo tipo de medio.
2.  Establezca el atributo de [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) para especificar audio o vídeo.
3.  Establezca el atributo [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) para especificar el subtipo del formato de descodificación. (Consulte GUID de [subtipo de audio](audio-subtype-guids.md) y [GUID de subtipo de vídeo](video-subtype-guids.md)).
4.  Llame a [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).

El lector de origen cargará automáticamente el descodificador. Para obtener los detalles completos del formato descodificado, llame a [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) después de la llamada a [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)

El código siguiente configura el flujo de vídeo para RGB-32 y la secuencia de audio para audio PCM.


```C++
HRESULT ConfigureDecoder(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    IMFMediaType *pNativeType = NULL;
    IMFMediaType *pType = NULL;

    // Find the native format of the stream.
    HRESULT hr = pReader->GetNativeMediaType(dwStreamIndex, 0, &pNativeType);
    if (FAILED(hr))
    {
        return hr;
    }

    GUID majorType, subtype;

    // Find the major type.
    hr = pNativeType->GetGUID(MF_MT_MAJOR_TYPE, &majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Define the output type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Select a subtype.
    if (majorType == MFMediaType_Video)
    {
        subtype= MFVideoFormat_RGB32;
    }
    else if (majorType == MFMediaType_Audio)
    {
        subtype = MFAudioFormat_PCM;
    }
    else
    {
        // Unrecognized type. Skip.
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the uncompressed format.
    hr = pReader->SetCurrentMediaType(dwStreamIndex, NULL, pType);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&pNativeType);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="processing-media-data"></a>Procesar datos multimedia

Para obtener datos multimedia del origen, llame al método [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , como se muestra en el código siguiente.


```C++
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );
```



El primer parámetro es el índice de la secuencia para la que desea obtener los datos. También puede especificar el **lector de origen MF en \_ \_ \_ cualquier \_ flujo** para obtener los siguientes datos disponibles de cualquier secuencia. El segundo parámetro contiene marcas opcionales; vea [**la \_ \_ marca de \_ control \_ del lector de código fuente MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) para obtener una lista de ellos. El tercer parámetro recibe el índice de la secuencia que realmente genera los datos. Necesitará esta información si establece el primer parámetro en el **lector de \_ origen MF en \_ \_ cualquier \_ flujo**. El cuarto parámetro recibe marcas de estado, que indican varios eventos que se pueden producir al leer los datos, como los cambios de formato en la secuencia. Para obtener una lista de las marcas de estado, consulte [**MF \_ source \_ Reader \_ Flag**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).

Si el origen multimedia es capaz de generar datos para la secuencia solicitada, el último parámetro de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) recibe un puntero a la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) de un objeto de ejemplo multimedia. Use el ejemplo multimedia para:

-   Obtiene un puntero a los datos multimedia.
-   Obtiene el tiempo de presentación y la duración de la muestra.
-   Obtiene los atributos que describen el entrelazado, el dominio de campo y otros aspectos del ejemplo.

El contenido de los datos multimedia depende del formato del flujo. En el caso de una secuencia de vídeo sin comprimir, cada ejemplo multimedia contiene un solo fotograma de vídeo. En el caso de una secuencia de audio sin comprimir, cada ejemplo multimedia contiene una secuencia de fotogramas de audio.

El método [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) puede devolver **S \_ OK** y no devolver un ejemplo multimedia en el parámetro *pSample* . Por ejemplo, cuando se alcanza el final del archivo, **ReadSample** establece la marca **MF \_ source \_ READERF \_ ENDOFSTREAM** en *dwFlags* y establece *pSample* en **null**. En este caso, el método **ReadSample** devuelve **S \_ OK** porque no se ha producido ningún error, aunque el parámetro *pSample* está establecido en **null**. Por consiguiente, compruebe siempre el valor de *pSample* antes de desreferenciarlo.

En el código siguiente se muestra cómo llamar a [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) en un bucle y comprobar la información devuelta por el método hasta que se alcanza el final del archivo multimedia.


```C++
HRESULT ProcessSamples(IMFSourceReader *pReader)
{
    HRESULT hr = S_OK;
    IMFSample *pSample = NULL;
    size_t  cSamples = 0;

    bool quit = false;
    while (!quit)
    {
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );

        if (FAILED(hr))
        {
            break;
        }

        wprintf(L"Stream %d (%I64d)\n", streamIndex, llTimeStamp);
        if (flags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            wprintf(L"\tEnd of stream\n");
            quit = true;
        }
        if (flags & MF_SOURCE_READERF_NEWSTREAM)
        {
            wprintf(L"\tNew stream\n");
        }
        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            wprintf(L"\tNative type changed\n");
        }
        if (flags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            wprintf(L"\tCurrent type changed\n");
        }
        if (flags & MF_SOURCE_READERF_STREAMTICK)
        {
            wprintf(L"\tStream tick\n");
        }

        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            // The format changed. Reconfigure the decoder.
            hr = ConfigureDecoder(pReader, streamIndex);
            if (FAILED(hr))
            {
                break;
            }
        }

        if (pSample)
        {
            ++cSamples;
        }

        SafeRelease(&pSample);
    }

    if (FAILED(hr))
    {
        wprintf(L"ProcessSamples FAILED, hr = 0x%x\n", hr);
    }
    else
    {
        wprintf(L"Processed %d samples\n", cSamples);
    }
    SafeRelease(&pSample);
    return hr;
}
```



## <a name="draining-the-data-pipeline"></a>Purga de la canalización de datos

Durante el procesamiento de datos, un descodificador u otra transformación podría almacenar en búfer ejemplos de entrada. En el diagrama siguiente, la aplicación llama a [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) y recibe un ejemplo con un tiempo de presentación igual a *T1*. El descodificador contiene ejemplos de *T2* y *T3*.

![Ilustración que muestra el almacenamiento en búfer en un descodificador.](images/sourcereader02.png)

En la siguiente llamada a [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), el lector de código fuente puede proporcionar *T4* al descodificador y devolver *T2* a la aplicación.

Si desea descodificar todos los ejemplos que están almacenados actualmente en el búfer en el descodificador, sin pasar los nuevos ejemplos al descodificador, establezca la marca **de \_ purga del lector de origen MF \_ \_ CONTROLF \_** en el parámetro *dwControlFlags* de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample). Siga haciendo esto en un bucle hasta que **ReadSample** devuelva un puntero de muestra **nulo** . En función de cómo los ejemplos de búferes del descodificador, pueden producirse inmediatamente o después de varias llamadas a **ReadSample**.

## <a name="getting-the-file-duration"></a>Obtención de la duración del archivo

Para obtener la duración de un archivo multimedia, llame al método [**IMFSourceReader:: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) y solicite el atributo de [**\_ \_ duración MF PD**](mf-pd-duration-attribute.md) , tal como se muestra en el código siguiente.


```C++
HRESULT GetDuration(IMFSourceReader *pReader, LONGLONG *phnsDuration)
{
    PROPVARIANT var;
    HRESULT hr = pReader->GetPresentationAttribute(MF_SOURCE_READER_MEDIASOURCE, 
        MF_PD_DURATION, &var);
    if (SUCCEEDED(hr))
    {
        hr = PropVariantToInt64(var, phnsDuration);
        PropVariantClear(&var);
    }
    return hr;
}
```



La función mostrada aquí obtiene la duración en unidades de 100-nanosegundos. Divida por 10 millones para obtener la duración en segundos.

## <a name="seeking"></a>Invoca

Un origen multimedia que obtiene datos de un archivo local normalmente puede buscar posiciones arbitrarias en el archivo. Normalmente, los dispositivos de captura, como las cámaras Web, no pueden buscar, ya que los datos están activos. Un origen que transmite datos a través de una red podría ser capaz de buscar, dependiendo del Protocolo de transmisión por secuencias de red.

Para averiguar si un origen multimedia puede buscar, llame a [**IMFSourceReader:: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) y solicite el atributo de la instancia de [ \_ MEDIASOURCE del lector de origen \_ \_ \_ MF](mf-source-reader-mediasource-characteristics.md) , tal como se muestra en el código siguiente:


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



Esta función obtiene un conjunto de marcas de funcionalidades del origen. Estas marcas se definen en la enumeración de [**\_ características de MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) . Dos marcas están relacionadas con la búsqueda:



| Marca                                                                                                                                      | Descripción                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE \_ puede \_ Buscar**<br/>                 | El origen puede buscar.<br/>                                                                                                                                                                            |
| <span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE \_ tiene \_ una \_ búsqueda lenta**<br/> | La búsqueda puede tardar mucho tiempo en completarse. Por ejemplo, es posible que el origen tenga que descargar todo el archivo antes de que pueda buscar. (No hay ningún criterio estricto para que un origen devuelva esta marca).<br/> |



 

Las siguientes pruebas de código para **MFMEDIASOURCE \_ pueden \_ Buscar** la marca.


```C++
BOOL SourceCanSeek(IMFSourceReader *pReader)
{
    BOOL bCanSeek = FALSE;
    ULONG flags;
    if (SUCCEEDED(GetSourceFlags(pReader, &flags)))
    {
        bCanSeek = ((flags & MFMEDIASOURCE_CAN_SEEK) == MFMEDIASOURCE_CAN_SEEK);
    }
    return bCanSeek;
}
```



Para buscar, llame al método [**IMFSourceReader:: SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) , tal y como se muestra en el código siguiente.


```C++
HRESULT SetPosition(IMFSourceReader *pReader, const LONGLONG& hnsPosition)
{
    PROPVARIANT var;
    HRESULT hr = InitPropVariantFromInt64(hnsPosition, &var);
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentPosition(GUID_NULL, var);
        PropVariantClear(&var);
    }
    return hr;
}
```



El primer parámetro proporciona el formato de hora que se usa para especificar la posición de búsqueda. Todos los orígenes multimedia en Media Foundation son necesarios para admitir unidades 100-nanosegundos, indicado por el valor **\_ null GUID**. El segundo parámetro es un **PROPVARIANT** que contiene la posición de búsqueda. En las unidades de tiempo de 100-nanosegundos, el tipo de datos es **LONGLONG**.

Tenga en cuenta que no todos los orígenes multimedia proporcionan búsquedas precisas de fotogramas. La precisión de la búsqueda depende de varios factores, como el intervalo de fotogramas clave, si el archivo multimedia contiene un índice y si los datos tienen una velocidad de bits constante o variable. Por lo tanto, después de buscar una posición en un archivo, no hay ninguna garantía de que la marca de tiempo en el siguiente ejemplo coincida exactamente con la posición solicitada. Por lo general, la posición real no será posterior a la posición solicitada, por lo que puede descartar muestras hasta alcanzar el punto deseado en la secuencia.

## <a name="playback-rate"></a>Velocidad de reproducción

Aunque puede establecer la velocidad de reproducción mediante el lector de origen, no suele ser muy útil, por las razones siguientes:

-   El lector de origen no admite la reproducción inversa, incluso si el origen multimedia sí lo hace.
-   La aplicación controla los tiempos de presentación, por lo que la aplicación puede implementar la reproducción rápida o lenta sin establecer la tasa en el origen.
-   Algunos orígenes multimedia admiten el modo *delgado* , donde el origen ofrece menos muestras, normalmente solo los fotogramas clave. Sin embargo, si desea quitar fotogramas no clave, puede comprobar cada ejemplo del atributo [ \_ CleanPoint de MFSampleExtension](mfsampleextension-cleanpoint-attribute.md) .

Para establecer la velocidad de reproducción mediante el lector de origen, llame al método [**IMFSourceReader:: GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) para obtener las interfaces [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) y [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) del origen multimedia.

## <a name="hardware-acceleration"></a>Aceleración de hardware

El lector de origen es compatible con la aceleración de vídeo de Microsoft DirectX (DXVA) 2,0 para la descodificación de vídeo acelerada de hardware. Para usar DXVA con el lector de origen, realice los pasos siguientes.

1.  Cree un dispositivo de Microsoft Direct3D.
2.  Llame a la función [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) para crear el administrador de dispositivos de Direct3D. Esta función obtiene un puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .
3.  Llame al método [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) con un puntero al dispositivo Direct3D.
4.  Cree un almacén de atributos mediante una llamada a la función [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .
5.  Cree el lector de origen. Pase el almacén de atributos en el parámetro *pAttributes* de la función de creación.

Cuando se proporciona un dispositivo Direct3D, el lector de código fuente asigna muestras de vídeo que son compatibles con la API del procesador de vídeo de DXVA. Puede usar el procesamiento de vídeo de DXVA para realizar el desentrelazado de hardware o la combinación de vídeo. Para obtener más información, vea [procesamiento de vídeo de DXVA](dxva-video-processing.md). Además, si el descodificador admite DXVA 2,0, usará el dispositivo Direct3D para realizar la descodificación acelerada por hardware.

> [!IMPORTANT]
> A partir de Windows 8, se puede usar [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) en lugar de [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9). En el caso de las aplicaciones de la tienda Windows, debe usar **IMFDXGIDeviceManager**. Para obtener más información, consulte las [API de vídeo de Direct3D 11](direct3d-11-video-apis.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lector de origen](source-reader.md)
</dt> </dl>

 

 




