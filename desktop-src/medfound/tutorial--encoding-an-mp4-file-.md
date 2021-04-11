---
description: En este tutorial se muestra cómo usar la API de Transcode para codificar un archivo MP4, mediante H. 264 para el flujo de vídeo y AAC para la secuencia de audio.
ms.assetid: 60873aa6-46ec-4a73-94b9-0d8ac602f850
title: 'Tutorial: codificación de un archivo MP4'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae895ef321b35f080bf946384ee32d83c2c539fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276215"
---
# <a name="tutorial-encoding-an-mp4-file"></a>Tutorial: codificación de un archivo MP4

En este tutorial se muestra cómo usar la [API de Transcode](transcode-api.md) para codificar un archivo MP4, mediante H. 264 para el flujo de vídeo y AAC para la secuencia de audio.

-   [Encabezados y archivos de biblioteca](#headers-and-library-files)
-   [Definir los perfiles de codificación](#define-the-encoding-profiles)
-   [Escribir la función wmain](#write-the-wmain-function)
-   [Codificar el archivo](#encode-the-file)
    -   [Crear el origen de medios](#create-the-media-source)
    -   [Obtener la duración de origen](#get-the-source-duration)
    -   [Crear el perfil de transcodificación](#create-the-transcode-profile)
    -   [Ejecutar la sesión de codificación](#run-the-encoding-session)
-   [Aplicación auxiliar de sesión multimedia](#media-session-helper)
-   [Temas relacionados](#related-topics)

## <a name="headers-and-library-files"></a>Encabezados y archivos de biblioteca

Incluya los siguientes archivos de encabezado.


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



Vincule los siguientes archivos de biblioteca.


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a>Definir los perfiles de codificación

Un enfoque para la codificación es definir una lista de perfiles de codificación de destino que se conocen de antemano. En este tutorial, se toma un enfoque relativamente sencillo y se almacena una lista de formatos de codificación para el vídeo H. 264 y el audio AAC.

Para H. 264, los atributos de formato más importantes son el perfil H. 264, la velocidad de fotogramas, el tamaño del fotograma y la velocidad de bits codificada. La siguiente matriz contiene una lista de formatos de codificación H. 264.


```C++
struct H264ProfileInfo
{
    UINT32  profile;
    MFRatio fps;
    MFRatio frame_size;
    UINT32  bitrate;
};

H264ProfileInfo h264_profiles[] = 
{
    { eAVEncH264VProfile_Base, { 15, 1 },       { 176, 144 },   128000 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 30, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 29970, 1000 }, { 320, 240 },   528560 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 720, 576 },  4000000 },
    { eAVEncH264VProfile_Main, { 25, 1 },       { 720, 576 }, 10000000 },
    { eAVEncH264VProfile_Main, { 30, 1 },       { 352, 288 }, 10000000 },
};
```



Los perfiles H. 264 se especifican mediante la enumeración [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) . También puede especificar el nivel H. 264, pero el [**codificador de vídeo h. 264**](h-264-video-encoder.md) Microsoft Media Foundation puede derivar el nivel adecuado para un flujo de vídeo determinado, por lo que se recomienda no reemplazar el nivel seleccionado del codificador. En el caso del contenido entrelazado, también se debe especificar el modo entrelazado (vea [entrelazado de vídeo](video-interlacing.md)).

En el caso de audio AAC, los atributos de formato más importantes son la velocidad de muestra de audio, el número de canales, el número de bits por muestra y la velocidad de bits codificada. Opcionalmente, puede establecer la indicación del nivel de Perfil de audio AAC. Para obtener más información, consulte [**codificador AAC**](aac-encoder.md). La siguiente matriz contiene una lista de formatos de codificación AAC.


```C++
struct AACProfileInfo
{
    UINT32  samplesPerSec;
    UINT32  numChannels;
    UINT32  bitsPerSample;
    UINT32  bytesPerSec;
    UINT32  aacProfile;
};

AACProfileInfo aac_profiles[] = 
{
    { 96000, 2, 16, 24000, 0x29}, 
    { 48000, 2, 16, 24000, 0x29}, 
    { 44100, 2, 16, 16000, 0x29}, 
    { 44100, 2, 16, 12000, 0x29}, 
};
```



> [!Note]  
> Las `H264ProfileInfo` `AACProfileInfo` estructuras y definidas aquí no forman parte de la API de Media Foundation.

 

## <a name="write-the-wmain-function"></a>Escribir la función wmain

En el código siguiente se muestra el punto de entrada de la aplicación de consola.


```C++
int video_profile = 0;
int audio_profile = 0;

int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc < 3 || argc > 5)
    {
        std::cout << "Usage:" << std::endl;
        std::cout << "input output [ audio_profile video_profile ]" << std::endl;
        return 1;
    }

    if (argc > 3)
    {
        audio_profile = _wtoi(argv[3]);
    }
    if (argc > 4)
    {
        video_profile = _wtoi(argv[4]);
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            hr = EncodeFile(argv[1], argv[2]);
            MFShutdown();
        }
        CoUninitialize();
    }

    if (SUCCEEDED(hr))
    {
        std::cout << "Done." << std::endl;
    }
    else
    {
        std::cout << "Error: " << std::hex << hr << std::endl;
    }

    return 0;
}
```



La `wmain` función hace lo siguiente:

1.  Llama a la función [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca com.
2.  Llama a la función [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar Media Foundation.
3.  Llama a la función definida por la aplicación `EncodeFile` . Esta función transcodifica el archivo de entrada en el archivo de salida y se muestra en la sección siguiente.
4.  Llama a la función [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para cerrar Media Foundation.
5.  Llame a la función [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) para anular la inicialización de la biblioteca com.

## <a name="encode-the-file"></a>Codificar el archivo

En el código siguiente se muestra `EncodeFile` la función, que realiza la transcodificación. Esta función se compone principalmente de llamadas a otras funciones definidas por la aplicación, que se muestran más adelante en este tema.


```C++
HRESULT EncodeFile(PCWSTR pszInput, PCWSTR pszOutput)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFMediaSource *pSource = NULL;
    IMFTopology *pTopology = NULL;
    CSession *pSession = NULL;

    MFTIME duration = 0;

    HRESULT hr = CreateMediaSource(pszInput, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetSourceDuration(pSource, &duration);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateTranscodeTopology(pSource, pszOutput, pProfile, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CSession::Create(&pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->StartEncodingSession(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = RunEncodingSession(pSession, duration);

done:            
    if (pSource)
    {
        pSource->Shutdown();
    }

    SafeRelease(&pSession);
    SafeRelease(&pProfile);
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    return hr;
}
```



La `EncodeFile` función realiza los pasos siguientes.

1.  Crea un origen de medios para el archivo de entrada mediante la dirección URL o la ruta de acceso del archivo de entrada. (Consulte [crear el origen de medios](#create-the-media-source)).
2.  Obtiene la duración del archivo de entrada. (Consulte [obtención de la duración de origen](#get-the-source-duration)).
3.  Cree el perfil de transcodificación. (Consulte [creación del perfil de transcodificación](#create-the-transcode-profile)).
4.  Llame a [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) para crear la topología de transcodificación parcial.
5.  Cree un objeto auxiliar que administre la sesión multimedia. (Consulte aplicación auxiliar de sesión multimedia).
6.  Ejecute la sesión de codificación y espere a que se complete. (Consulte [ejecución de la sesión de codificación](#run-the-encoding-session)).
7.  Llame a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para cerrar el origen del medio.
8.  Punteros de interfaz de la versión. Este código usa la función [SafeRelease](saferelease.md) para liberar punteros de interfaz. Otra opción es usar una clase de puntero inteligente COM, como **CComPtr**.

### <a name="create-the-media-source"></a>Crear el origen de medios

El origen multimedia es el objeto que lee y analiza el archivo de entrada. Para crear el origen de medios, pase la dirección URL del archivo de entrada al [solucionador de origen](source-resolver.md). El código siguiente muestra cómo hacerlo.


```C++
HRESULT CreateMediaSource(PCWSTR pszURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source
    hr = pResolver->CreateObjectFromURL(pszURL, MF_RESOLUTION_MEDIASOURCE, 
        NULL, &ObjectType, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pResolver);
    SafeRelease(&pSource);
    return hr;
}
```



Para obtener más información, vea [usar el solucionador de origen](using-the-source-resolver.md).

### <a name="get-the-source-duration"></a>Obtener la duración de origen

Aunque no es necesario, resulta útil consultar el origen de los medios mientras dure el archivo de entrada. Este valor se puede usar para realizar el seguimiento del progreso de la codificación. La duración se almacena en el atributo [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) del descriptor de presentación. Obtiene el descriptor de la presentación mediante una llamada a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



### <a name="create-the-transcode-profile"></a>Crear el perfil de transcodificación

El perfil de transcodificación describe los parámetros de codificación. Para obtener más información sobre la creación de un perfil de transcodificación, consulte [uso de la API de Transcode](fast-transcode-objects.md). Para crear el perfil, realice los pasos siguientes.

1.  Llame a [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) para crear el perfil vacío.
2.  Cree un tipo de medio para la secuencia de audio AAC. Agréguelo al perfil llamando a [**IMFTranscodeProfile:: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).
3.  Cree un tipo de medio para la secuencia de vídeo H. 264. Agréguelo al perfil llamando a [**IMFTranscodeProfile:: SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).
4.  Llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un almacén de atributos para los atributos de nivel de contenedor.
5.  Establezca el atributo [MF \_ Transcode \_ CONTAINERTYPE](mf-transcode-containertype.md) . Este es el único atributo de nivel de contenedor necesario. Para la salida del archivo MP4, establezca este atributo en **MFTranscodeContainerType \_ MPEG4**.
6.  Llame a [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) para establecer los atributos de nivel de contenedor.

En el código siguiente se muestran estos pasos.


```C++
HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFAttributes *pAudio = NULL;
    IMFAttributes *pVideo = NULL;
    IMFAttributes *pContainer = NULL;

    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Audio attributes.
    hr = CreateAACProfile(audio_profile, &pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetAudioAttributes(pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Video attributes.
    hr = CreateH264Profile(video_profile, &pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetVideoAttributes(pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_MPEG4);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr)) 
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAudio);
    SafeRelease(&pVideo);
    SafeRelease(&pContainer);
    return hr;
}
```



Para especificar los atributos de la secuencia de vídeo H. 264, cree un almacén de atributos y establezca los siguientes atributos:



| Atributo                                                       | Descripción                      |
|-----------------------------------------------------------------|---------------------------------|
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)              | Establézcalo en **MFVideoFormat \_ H264**. |
| [**\_Perfil MF MT \_ MPEG2 \_**](mf-mt-mpeg2-profile-attribute.md) | Perfil H. 264.                  |
| [**\_tamaño de \_ marco MF MT \_**](mf-mt-frame-size-attribute.md)       | Tamaño del marco.                     |
| [**\_velocidad de \_ fotogramas MF MT \_**](mf-mt-frame-rate-attribute.md)       | Velocidad de fotogramas.                     |
| [**\_velocidad de \_ bits media MF MT \_**](mf-mt-avg-bitrate-attribute.md)     | Velocidad de bits codificada.               |



 

Para especificar los atributos de la secuencia de audio AAC, cree un almacén de atributos y establezca los siguientes atributos:



| Atributo                                                                                      | Descripción                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                             | Establecer en **MFAudioFormat \_ AAC**            |
| [**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md)        | Velocidad de muestra de audio.                       |
| [**MF \_ MT \_ audio \_ bits \_ por \_ muestra**](mf-mt-audio-bits-per-sample-attribute.md)              | Ejemplo de bits por audio.                   |
| [**\_canales de \_ número de audio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                     | Número de canales de audio.                |
| [**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | Velocidad de bits codificada.                        |
| [**\_alineación del \_ bloque de audio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)               | establézcalo en 1.                                |
| [\_indicación de \_ \_ nivel de \_ Perfil de audio \_ \_ MF MT AAC](mf-mt-aac-audio-profile-level-indication.md) | Indicación del nivel de perfil AAC (opcional). |



 

En el código siguiente se crean los atributos de la secuencia de vídeo.


```C++
HRESULT CreateH264Profile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    IMFAttributes *pAttributes = NULL;

    const H264ProfileInfo& profile = h264_profiles[index];

    HRESULT hr = MFCreateAttributes(&pAttributes, 5);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_H264);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_MPEG2_PROFILE, profile.profile);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(
            pAttributes, MF_MT_FRAME_SIZE, 
            profile.frame_size.Numerator, profile.frame_size.Numerator);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(
            pAttributes, MF_MT_FRAME_RATE, 
            profile.fps.Numerator, profile.fps.Denominator);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AVG_BITRATE, profile.bitrate);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



En el código siguiente se crean los atributos de secuencia de audio.


```C++
HRESULT CreateAACProfile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    const AACProfileInfo& profile = aac_profiles[index];

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 7);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_AAC);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_BITS_PER_SAMPLE, profile.bitsPerSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_SAMPLES_PER_SECOND, profile.samplesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_NUM_CHANNELS, profile.numChannels);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_AVG_BYTES_PER_SECOND, profile.bytesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, 1);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION, profile.aacProfile);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



Tenga en cuenta que la API de Transcode no requiere un tipo de medio real, aunque utiliza atributos de tipo de medio. En concreto, el atributo de [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) no es necesario, ya que los métodos [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) y [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) implican el tipo principal. Sin embargo, también es válido para pasar un tipo de medio real a estos métodos. (La interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) hereda [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)).

### <a name="run-the-encoding-session"></a>Ejecutar la sesión de codificación

En el código siguiente se ejecuta la sesión de codificación. Usa la clase auxiliar de sesión de medios, que se muestra en la sección siguiente.


```C++
HRESULT RunEncodingSession(CSession *pSession, MFTIME duration)
{
    const DWORD WAIT_PERIOD = 500;
    const int   UPDATE_INCR = 5;

    HRESULT hr = S_OK;
    MFTIME pos;
    LONGLONG prev = 0;
    while (1)
    {
        hr = pSession->Wait(WAIT_PERIOD);
        if (hr == E_PENDING)
        {
            hr = pSession->GetEncodingPosition(&pos);

            LONGLONG percent = (100 * pos) / duration ;
            if (percent >= prev + UPDATE_INCR)
            {
                std::cout << percent << "% .. ";  
                prev = percent;
            }
        }
        else
        {
            std::cout << std::endl;
            break;
        }
    }
    return hr;
}
```



## <a name="media-session-helper"></a>Aplicación auxiliar de sesión multimedia

La [sesión multimedia](media-session.md) se describe más detalladamente en la sección [Media Foundation arquitectura](media-foundation-architecture.md) de esta documentación. La sesión multimedia utiliza un modelo de eventos asincrónicos. En una aplicación de GUI, debe responder a los eventos de sesión sin bloquear el subproceso de interfaz de usuario para esperar al siguiente evento. En el tutorial [Cómo reproducir archivos multimedia no protegidos](how-to-play-unprotected-media-files.md) se muestra cómo hacerlo en una aplicación de reproducción. Para la codificación, el principio es el mismo, pero hay menos eventos relevantes:



| Evento                                  | Descripción                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MESessionEnded](mesessionended.md)   | Se genera cuando se completa la codificación.                                                                                                                            |
| [MESessionClosed](mesessionclosed.md) | Se genera cuando se completa el método [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) . Una vez que se genera este evento, es seguro apagar la sesión multimedia. |



 

En el caso de una aplicación de consola, es razonable bloquear y esperar eventos. Dependiendo del archivo de código fuente y de la configuración de la codificación, la codificación podría tardar unos minutos en completarse. Puede obtener actualizaciones de progreso como se indica a continuación:

1.  Llame a [**IMFMediaSession:: GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) para obtener el reloj de la presentación.
2.  Consulte el reloj de la interfaz [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) .
3.  Llame a [**IMFPresentationClock:: getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) para obtener la posición actual.
4.  La posición se proporciona en unidades de tiempo. Para obtener el porcentaje completado, use el valor `(100 * position) / duration` .

Esta es la declaración de la `CSession` clase.


```C++
class CSession  : public IMFAsyncCallback 
{
public:
    static HRESULT Create(CSession **ppSession);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP Invoke(IMFAsyncResult *pResult);

    // Other methods
    HRESULT StartEncodingSession(IMFTopology *pTopology);
    HRESULT GetEncodingPosition(MFTIME *pTime);
    HRESULT Wait(DWORD dwMsec);

private:
    CSession() : m_cRef(1), m_pSession(NULL), m_pClock(NULL), m_hrStatus(S_OK), m_hWaitEvent(NULL)
    {
    }
    virtual ~CSession()
    {
        if (m_pSession)
        {
            m_pSession->Shutdown();
        }

        SafeRelease(&m_pClock);
        SafeRelease(&m_pSession);
        CloseHandle(m_hWaitEvent);
    }

    HRESULT Initialize();

private:
    IMFMediaSession      *m_pSession;
    IMFPresentationClock *m_pClock;
    HRESULT m_hrStatus;
    HANDLE  m_hWaitEvent;
    long    m_cRef;
};
```



En el código siguiente se muestra la implementación completa de la `CSession` clase.


```C++
HRESULT CSession::Create(CSession **ppSession)
{
    *ppSession = NULL;

    CSession *pSession = new (std::nothrow) CSession();
    if (pSession == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pSession->Initialize();
    if (FAILED(hr))
    {
        pSession->Release();
        return hr;
    }
    *ppSession = pSession;
    return S_OK;
}

STDMETHODIMP CSession::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CSession, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CSession::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CSession::Release()
{
    long cRef = InterlockedDecrement(&m_cRef);
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}

HRESULT CSession::Initialize()
{
    IMFClock *pClock = NULL;

    HRESULT hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->GetClock(&pClock);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pClock->QueryInterface(IID_PPV_ARGS(&m_pClock));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->BeginGetEvent(this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_hWaitEvent = CreateEvent(NULL, FALSE, FALSE, NULL);  
    if (m_hWaitEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
done:
    SafeRelease(&pClock);
    return hr;
}

// Implements IMFAsyncCallback::Invoke
STDMETHODIMP CSession::Invoke(IMFAsyncResult *pResult)
{
    IMFMediaEvent* pEvent = NULL;
    MediaEventType meType = MEUnknown;
    HRESULT hrStatus = S_OK;

    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetStatus(&hrStatus);
    if (FAILED(hr))
    {
        goto done;
    }

    if (FAILED(hrStatus))
    {
        hr = hrStatus;
        goto done;
    }

    switch (meType)
    {
    case MESessionEnded:
        hr = m_pSession->Close();
        if (FAILED(hr))
        {
            goto done;
        }
        break;

    case MESessionClosed:
        SetEvent(m_hWaitEvent);
        break;
    }

    if (meType != MESessionClosed)
    {
        hr = m_pSession->BeginGetEvent(this, NULL);
    }

done:
    if (FAILED(hr))
    {
        m_hrStatus = hr;
        m_pSession->Close();
    }

    SafeRelease(&pEvent);
    return hr;
}

HRESULT CSession::StartEncodingSession(IMFTopology *pTopology)
{
    HRESULT hr = m_pSession->SetTopology(0, pTopology);
    if (SUCCEEDED(hr))
    {
        PROPVARIANT varStart;
        PropVariantClear(&varStart);
        hr = m_pSession->Start(&GUID_NULL, &varStart);
    }
    return hr;
}

HRESULT CSession::GetEncodingPosition(MFTIME *pTime)
{
    return m_pClock->GetTime(pTime);
}

HRESULT CSession::Wait(DWORD dwMsec)
{
    HRESULT hr = S_OK;

    DWORD dwTimeoutStatus = WaitForSingleObject(m_hWaitEvent, dwMsec);
    if (dwTimeoutStatus != WAIT_OBJECT_0)
    {
        hr = E_PENDING;
    }
    else
    {
        hr = m_hrStatus;
    }
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Codificador AAC**](aac-encoder.md)
</dt> <dt>

[**Codificador de vídeo H. 264**](h-264-video-encoder.md)
</dt> <dt>

[Sesión de medios](media-session.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> <dt>

[API de transcodificación](transcode-api.md)
</dt> </dl>

 

 
