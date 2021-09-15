---
description: En este tema se describe cómo usar el Lector de origen para procesar datos multimedia.
ms.assetid: 583f5736-f767-47c5-8fdc-b3645aed59f6
title: Usar el lector de origen para procesar datos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad5c8a21a2e547d005e4695a14fe9a6bd09d5d9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474039"
---
# <a name="using-the-source-reader-to-process-media-data"></a>Usar el lector de origen para procesar datos multimedia

En este tema se describe cómo usar el Lector [de origen para](source-reader.md) procesar datos multimedia.

Para usar el Lector de origen, siga estos pasos básicos:

1.  Cree una instancia del Lector de origen.
2.  Enumerar los posibles formatos de salida.
3.  Establezca el formato de salida real de cada secuencia.
4.  Procesar datos desde el origen.

En el resto de este tema se describen estos pasos en detalle.

-   [Creación del lector de origen](#creating-the-source-reader)
-   [Enumeración de formatos de salida](#enumerating-output-formats)
-   [Establecer formatos de salida](#setting-output-formats)
-   [Procesamiento de datos multimedia](#using-the-source-reader-to-process-media-data)
-   [Purgar la canalización de datos](#draining-the-data-pipeline)
-   [Obtención de la duración del archivo](#getting-the-file-duration)
-   [Buscando](#seeking)
-   [Velocidad de reproducción](#playback-rate)
-   [Aceleración de hardware](#hardware-acceleration)
-   [Temas relacionados](#related-topics)

## <a name="creating-the-source-reader"></a>Creación del lector de origen

Para crear una instancia del Lector de origen, llame a una de las siguientes funciones:



| Función                                                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)<br/>                                         | Toma una dirección URL como entrada. Esta función usa el [solucionador de origen](source-resolver.md) para crear un origen multimedia a partir de la dirección URL.<br/>                                                                       |
| <span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)<br/>      | Toma un puntero a una secuencia de bytes. Esta función también usa el solucionador de origen para crear el origen de medios.<br/>                                                                                        |
| <span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)<br/> | Toma un puntero a un origen de medios que ya se ha creado. Esta función es útil para orígenes multimedia que el solucionador de origen no puede crear, como dispositivos de captura o orígenes multimedia personalizados.<br/> |



 

Normalmente, para los archivos multimedia, use [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl). Para dispositivos, como cámaras web, use [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource). (Para obtener más información sobre la captura de dispositivos Microsoft Media Foundation, vea [Captura de audio y vídeo).](audio-video-capture.md)

Cada una de estas funciones toma un puntero [**OPTIONALATTRIBUTEs,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) que se usa para establecer varias opciones en el Lector de origen, como se describe en los temas de referencia de estas funciones. Para obtener el comportamiento predeterminado, establezca este parámetro en **NULL.** Cada función devuelve un [**puntero IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) como parámetro de salida. Debe llamar a **las funciones CoInitialize(Ex)** y [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) antes de llamar a cualquiera de estas funciones.

El código siguiente crea el Lector de origen a partir de una dirección URL.


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



## <a name="enumerating-output-formats"></a>Enumeración de formatos de salida

Cada origen de medios tiene al menos una secuencia. Por ejemplo, un archivo de vídeo puede contener una secuencia de vídeo y una secuencia de audio. El formato de cada secuencia se describe mediante un tipo de medio, representado por la [**interfaz IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) Para obtener más información sobre los tipos de medios, vea [Tipos de medios](media-types.md). Debe examinar el tipo de medio para comprender el formato de los datos que obtiene del Lector de origen.

Inicialmente, cada secuencia tiene un formato predeterminado, que puede encontrar llamando al método [**IMFSourceReader::GetCurrentMediaType:**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype)

Para cada secuencia, el origen multimedia ofrece una lista de posibles tipos de medios para esa secuencia. El número de tipos depende del origen. Si el origen representa un archivo multimedia, normalmente solo hay un tipo por secuencia. Por otro lado, una cámara web podría ser capaz de transmitir vídeo en varios formatos diferentes. En ese caso, la aplicación puede seleccionar el formato que se va a usar en la lista de tipos de medios.

Para obtener uno de los tipos de medios de una secuencia, llame al [**método IMFSourceReader::GetNativeMediaType.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) Este método toma dos parámetros de índice: el índice de la secuencia y un índice en la lista de tipos de medios para la secuencia. Para enumerar todos los tipos de una secuencia, incremente el índice de lista manteniendo la constante del índice de secuencia. Cuando el índice de lista sale de los límites, **GetNativeMediaType** devuelve **MF E NO MORE \_ \_ \_ \_ TYPES**.


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



Para enumerar los tipos de medios de cada secuencia, incremente el índice de la secuencia. Cuando el índice de flujo sale de los límites, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) devuelve **MF E \_ \_ INVALIDSTREAMNUMBER**.


```C++
HRESULT EnumerateMediaTypes(IMFSourceReader *pReader)
{
    HRESULT hr = S_OK;
    DWORD dwStreamIndex = 0;

    while (SUCCEEDED(hr))
    {
        hr = EnumerateTypesForStream(pReader, dwStreamIndex);
        if (hr == MF_E_INVALIDSTREAMNUMBER)
        {
            hr = S_OK;
            break;
        }
        ++dwStreamIndex;
    }
    return hr;
}
```



## <a name="setting-output-formats"></a>Establecer formatos de salida

Para cambiar el formato de salida, llame al [**método IMFSourceReader::SetCurrentMediaType.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) Este método toma el índice de secuencia y un tipo de medio:

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

Para el tipo de medio, depende de si desea insertar un descodificador.

-   Para obtener datos directamente desde el origen sin necesidad de decodificar, use uno de los tipos devueltos por [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).
-   Para descodificar la secuencia, cree un nuevo tipo de medio que describa el formato sin comprimir deseado.

En el caso del descodificador, cree el tipo de medio de la manera siguiente:

1.  Llame [**a MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) para crear un nuevo tipo de medio.
2.  Establezca el [**atributo MF MT MAJOR \_ \_ \_ TYPE**](mf-mt-major-type-attribute.md) para especificar audio o vídeo.
3.  Establezca el [**atributo MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md) para especificar el subtipo del formato de decoding. (Consulte [GUID de subtipo de audio y](audio-subtype-guids.md) GUID de [subtipo de vídeo).](video-subtype-guids.md)
4.  Llame [**a IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).

El Lector de origen cargará automáticamente el descodificador. Para obtener los detalles completos del formato descodificado, llame a [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) después de llamar a [**SetCurrentMediaType.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)

El código siguiente configura la secuencia de vídeo para RGB-32 y la secuencia de audio para el audio PCM.


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



## <a name="processing-media-data"></a>Procesamiento de datos multimedia

Para obtener datos multimedia del origen, llame al [**método IMFSourceReader::ReadSample,**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) como se muestra en el código siguiente.


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



El primer parámetro es el índice de la secuencia para la que desea obtener datos. También puede especificar **MF SOURCE READER ANY STREAM \_ \_ \_ \_ para** obtener los siguientes datos disponibles de cualquier flujo. El segundo parámetro contiene marcas opcionales; Vea [**MF SOURCE READER CONTROL \_ \_ \_ \_ FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) para obtener una lista de estos. El tercer parámetro recibe el índice de la secuencia que realmente genera los datos. Necesitará esta información si establece el primer parámetro en **MF SOURCE READER ANY \_ \_ \_ \_ STREAM**. El cuarto parámetro recibe marcas de estado, lo que indica varios eventos que pueden producirse al leer los datos, como cambios de formato en la secuencia. Para obtener una lista de marcas de estado, vea [**MF \_ SOURCE READER \_ \_ FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).

Si el origen de medios es capaz de generar datos para la secuencia solicitada, el último parámetro de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) recibe un puntero a la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) de un objeto de ejemplo multimedia. Use el ejemplo multimedia para:

-   Obtenga un puntero a los datos multimedia.
-   Obtiene el tiempo de presentación y la duración de la muestra.
-   Obtiene atributos que describen el entrelazado, la dominación de campo y otros aspectos del ejemplo.

El contenido de los datos multimedia depende del formato de la secuencia. Para una secuencia de vídeo sin comprimir, cada ejemplo multimedia contiene un único fotograma de vídeo. Para una secuencia de audio sin comprimir, cada ejemplo multimedia contiene una secuencia de fotogramas de audio.

El [**método ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) puede devolver **S \_ OK** y, sin embargo, no devolver un ejemplo multimedia en el *parámetro pSample.* Por ejemplo, cuando se llega al final del archivo, **ReadSample** establece la marca **MF SOURCE \_ \_ READERF \_ ENDOFSTREAM** en *dwFlags* y establece *pSample* en **NULL.** En este caso, el **método ReadSample** devuelve **S \_ OK** porque no se ha producido ningún error, aunque el *parámetro pSample* esté establecido en **NULL.** Por lo tanto, compruebe siempre el valor de *pSample* antes de desreferenciarlo.

El código siguiente muestra cómo llamar a [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) en un bucle y comprobar la información devuelta por el método hasta que se alcanza el final del archivo multimedia.


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



## <a name="draining-the-data-pipeline"></a>Purgar la canalización de datos

Durante el procesamiento de datos, un descodificador u otra transformación podría almacenar en búfer ejemplos de entrada. En el diagrama siguiente, la aplicación llama a [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) y recibe un ejemplo con un tiempo de presentación igual a *t1.* El descodificador está manteniendo ejemplos *para t2* y *t3.*

![ilustración que muestra el almacenamiento en búfer en un descodificador.](images/sourcereader02.png)

En la siguiente llamada a [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), el Lector de origen podría dar *t4* al descodificador y devolver *t2* a la aplicación.

Si desea descodificar todas las muestras que están actualmente en búfer en el descodificador, sin pasar ninguna muestra nueva al descodificador, establezca la marca **MF \_ SOURCE READER \_ \_ CONTROLF \_ DRAIN** en el parámetro *dwControlFlags* de [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample). Siga haciendo esto en un bucle hasta que **ReadSample** devuelva un puntero de ejemplo **NULL.** Dependiendo de cómo el descodificador almacena en búfer los ejemplos, esto puede ocurrir inmediatamente o después de varias llamadas a **ReadSample**.

## <a name="getting-the-file-duration"></a>Obtención de la duración del archivo

Para obtener la duración de un archivo multimedia, llame al método [**MFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) y solicite el atributo [**MF PD \_ \_ DURATION,**](mf-pd-duration-attribute.md) como se muestra en el código siguiente.


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



La función que se muestra aquí obtiene la duración en unidades de 100 nanosegundos. Divida por 10 000 000 para obtener la duración en segundos.

## <a name="seeking"></a>Buscando

Un origen multimedia que obtiene datos de un archivo local normalmente puede buscar posiciones arbitrarias en el archivo. Por lo general, los dispositivos de captura, como las cámaras web, no pueden buscar, porque los datos están en directo. Un origen que transmite datos a través de una red podría ser capaz de buscar, dependiendo del protocolo de streaming de red.

Para averiguar si un origen multimedia puede buscar, llame a [**MFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) y solicite el atributo [MF SOURCE READER \_ \_ \_ MEDIASOURCE \_ CHARACTERISTICS,](mf-source-reader-mediasource-characteristics.md) como se muestra en el código siguiente:


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



Esta función obtiene un conjunto de marcas de funcionalidades del origen. Estas marcas se definen en la [**enumeración MFMEDIASOURCE \_ CHARACTERISTICS.**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) Dos marcas se relacionan con la búsqueda:



| Marca                                                                                                                                      | Descripción                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE \_ PUEDE \_ BUSCAR**<br/>                 | El origen puede buscar.<br/>                                                                                                                                                                            |
| <span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE \_ TIENE \_ BÚSQUEDA \_ LENTA**<br/> | La búsqueda puede tardar mucho tiempo en completarse. Por ejemplo, es posible que el origen tenga que descargar todo el archivo antes de poder buscarlo. (No hay ningún criterio estricto para que un origen devuelva esta marca).<br/> |



 

El código siguiente comprueba la **marca MFMEDIASOURCE \_ CAN \_ SEEK.**


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



Para buscar, llame al [**método QRSourceReader::SetCurrentPosition,**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) como se muestra en el código siguiente.


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



El primer parámetro proporciona el formato de hora que se usa para especificar la posición de búsqueda. Todos los orígenes multimedia de Media Foundation deben admitir unidades de 100 nanosegundos, indicados por el **valor NULL de \_ GUID.** El segundo parámetro es **PROPVARIANT que** contiene la posición de búsqueda. Para unidades de tiempo de 100 nanosegundos, el tipo de datos **es LONGLONG.**

Tenga en cuenta que no todos los orígenes multimedia proporcionan búsquedas precisas de fotogramas. La precisión de la búsqueda depende de varios factores, como el intervalo de fotogramas clave, si el archivo multimedia contiene un índice y si los datos tienen una frecuencia de bits constante o variable. Por lo tanto, después de buscar una posición en un archivo, no hay ninguna garantía de que la marca de tiempo del ejemplo siguiente coincida exactamente con la posición solicitada. Por lo general, la posición real no será posterior a la posición solicitada, por lo que puede descartar muestras hasta que llegue al punto deseado en la secuencia.

## <a name="playback-rate"></a>Velocidad de reproducción

Aunque puede establecer la velocidad de reproducción mediante el Lector de origen, no suele ser muy útil, por los siguientes motivos:

-   El Lector de origen no admite la reproducción inversa, incluso si lo hace el origen multimedia.
-   La aplicación controla los tiempos de presentación, por lo que la aplicación puede implementar un juego rápido o lento sin establecer la velocidad en el origen.
-   Algunos orígenes multimedia *admiten el modo de* simplificación, donde el origen ofrece menos muestras, normalmente solo los fotogramas clave. Sin embargo, si desea quitar fotogramas que no son de clave, puede comprobar cada ejemplo para el atributo [MFSampleExtension \_ CleanPoint.](mfsampleextension-cleanpoint-attribute.md)

Para establecer la velocidad de reproducción mediante el Lector de origen, llame al método [**QRSourceReader::GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) para obtener las interfaces [**QRRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) y [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) del origen multimedia.

## <a name="hardware-acceleration"></a>Aceleración de hardware

El lector de origen es compatible con La aceleración de vídeo de Microsoft DirectX (DXVA) 2.0 para lacodización de vídeo acelerada por hardware. Para usar DXVA con el Lector de origen, realice los pasos siguientes.

1.  Cree un dispositivo Microsoft Direct3D.
2.  Llame a [**la función DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) para crear el administrador de dispositivos Direct3D. Esta función obtiene un puntero a la [**interfaz IDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)
3.  Llame al [**método IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) con un puntero al dispositivo Direct3D.
4.  Cree un almacén de atributos mediante una llamada [**a la función MFCreateAttributes.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)
5.  Cree el Lector de origen. Pase el almacén de atributos en el *parámetro pAttributes* de la función de creación.

Cuando se proporciona un dispositivo Direct3D, el Lector de origen asigna ejemplos de vídeo compatibles con la API del procesador de vídeo DXVA. Puede usar el procesamiento de vídeo DXVA para realizar el desinterlazado de hardware o la combinación de vídeo. Para obtener más información, vea [DXVA Video Processing](dxva-video-processing.md). Además, si el descodificador admite DXVA 2.0, usará el dispositivo Direct3D para realizar la descodificación acelerada por hardware.

> [!IMPORTANT]
> A partir de Windows 8, se puede usar [**ELIDXGIDeviceManager en**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) lugar de [**IDirect3DDeviceManager9.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) Para Windows store, debe usar **ELIDXGIDeviceManager.** Para más información, consulte las API de vídeo de [Direct3D 11.](direct3d-11-video-apis.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lector de origen](source-reader.md)
</dt> </dl>

 

 




