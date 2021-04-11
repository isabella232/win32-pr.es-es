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
# <a name="tutorial-encoding-an-mp4-file"></a><span data-ttu-id="45030-103">Tutorial: codificación de un archivo MP4</span><span class="sxs-lookup"><span data-stu-id="45030-103">Tutorial: Encoding an MP4 File</span></span>

<span data-ttu-id="45030-104">En este tutorial se muestra cómo usar la [API de Transcode](transcode-api.md) para codificar un archivo MP4, mediante H. 264 para el flujo de vídeo y AAC para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="45030-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode an MP4 file, using H.264 for the video stream and AAC for the audio stream.</span></span>

-   [<span data-ttu-id="45030-105">Encabezados y archivos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="45030-105">Headers and Library Files</span></span>](#headers-and-library-files)
-   [<span data-ttu-id="45030-106">Definir los perfiles de codificación</span><span class="sxs-lookup"><span data-stu-id="45030-106">Define the Encoding Profiles</span></span>](#define-the-encoding-profiles)
-   [<span data-ttu-id="45030-107">Escribir la función wmain</span><span class="sxs-lookup"><span data-stu-id="45030-107">Write the wmain Function</span></span>](#write-the-wmain-function)
-   [<span data-ttu-id="45030-108">Codificar el archivo</span><span class="sxs-lookup"><span data-stu-id="45030-108">Encode the File</span></span>](#encode-the-file)
    -   [<span data-ttu-id="45030-109">Crear el origen de medios</span><span class="sxs-lookup"><span data-stu-id="45030-109">Create the Media Source</span></span>](#create-the-media-source)
    -   [<span data-ttu-id="45030-110">Obtener la duración de origen</span><span class="sxs-lookup"><span data-stu-id="45030-110">Get the Source Duration</span></span>](#get-the-source-duration)
    -   [<span data-ttu-id="45030-111">Crear el perfil de transcodificación</span><span class="sxs-lookup"><span data-stu-id="45030-111">Create the Transcode Profile</span></span>](#create-the-transcode-profile)
    -   [<span data-ttu-id="45030-112">Ejecutar la sesión de codificación</span><span class="sxs-lookup"><span data-stu-id="45030-112">Run the Encoding Session</span></span>](#run-the-encoding-session)
-   [<span data-ttu-id="45030-113">Aplicación auxiliar de sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="45030-113">Media Session Helper</span></span>](#media-session-helper)
-   [<span data-ttu-id="45030-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45030-114">Related topics</span></span>](#related-topics)

## <a name="headers-and-library-files"></a><span data-ttu-id="45030-115">Encabezados y archivos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="45030-115">Headers and Library Files</span></span>

<span data-ttu-id="45030-116">Incluya los siguientes archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="45030-116">Include the following header files.</span></span>


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



<span data-ttu-id="45030-117">Vincule los siguientes archivos de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="45030-117">Link the following library files.</span></span>


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a><span data-ttu-id="45030-118">Definir los perfiles de codificación</span><span class="sxs-lookup"><span data-stu-id="45030-118">Define the Encoding Profiles</span></span>

<span data-ttu-id="45030-119">Un enfoque para la codificación es definir una lista de perfiles de codificación de destino que se conocen de antemano.</span><span class="sxs-lookup"><span data-stu-id="45030-119">One approach to encoding is to define a list of target encoding profiles that are known in advance.</span></span> <span data-ttu-id="45030-120">En este tutorial, se toma un enfoque relativamente sencillo y se almacena una lista de formatos de codificación para el vídeo H. 264 y el audio AAC.</span><span class="sxs-lookup"><span data-stu-id="45030-120">For this tutorial, we take a relatively simple approach, and store a list of encoding formats for H.264 video and AAC audio.</span></span>

<span data-ttu-id="45030-121">Para H. 264, los atributos de formato más importantes son el perfil H. 264, la velocidad de fotogramas, el tamaño del fotograma y la velocidad de bits codificada.</span><span class="sxs-lookup"><span data-stu-id="45030-121">For H.264, the most important format attributes are the H.264 profile, the frame rate, the frame size, and the encoded bit rate.</span></span> <span data-ttu-id="45030-122">La siguiente matriz contiene una lista de formatos de codificación H. 264.</span><span class="sxs-lookup"><span data-stu-id="45030-122">The following array contains a list of H.264 encoding formats.</span></span>


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



<span data-ttu-id="45030-123">Los perfiles H. 264 se especifican mediante la enumeración [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="45030-123">H.264 profiles are specified using the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span> <span data-ttu-id="45030-124">También puede especificar el nivel H. 264, pero el [**codificador de vídeo h. 264**](h-264-video-encoder.md) Microsoft Media Foundation puede derivar el nivel adecuado para un flujo de vídeo determinado, por lo que se recomienda no reemplazar el nivel seleccionado del codificador.</span><span class="sxs-lookup"><span data-stu-id="45030-124">You could also specify the H.264 level, but the Microsoft Media Foundation [**H.264 Video Encoder**](h-264-video-encoder.md) can derive the proper level for a given video stream, so it is recommended not to override the encoder's selected level.</span></span> <span data-ttu-id="45030-125">En el caso del contenido entrelazado, también se debe especificar el modo entrelazado (vea [entrelazado de vídeo](video-interlacing.md)).</span><span class="sxs-lookup"><span data-stu-id="45030-125">For interlaced content, you would also specify the interlace mode (see [Video Interlacing](video-interlacing.md)).</span></span>

<span data-ttu-id="45030-126">En el caso de audio AAC, los atributos de formato más importantes son la velocidad de muestra de audio, el número de canales, el número de bits por muestra y la velocidad de bits codificada.</span><span class="sxs-lookup"><span data-stu-id="45030-126">For AAC audio, the most important format attributes are the audio sample rate, the number of channels, the number of bits per sample, and the encoded bit rate.</span></span> <span data-ttu-id="45030-127">Opcionalmente, puede establecer la indicación del nivel de Perfil de audio AAC.</span><span class="sxs-lookup"><span data-stu-id="45030-127">Optionally, you can set the AAC audio profile level indication.</span></span> <span data-ttu-id="45030-128">Para obtener más información, consulte [**codificador AAC**](aac-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="45030-128">For more information, see [**AAC Encoder**](aac-encoder.md).</span></span> <span data-ttu-id="45030-129">La siguiente matriz contiene una lista de formatos de codificación AAC.</span><span class="sxs-lookup"><span data-stu-id="45030-129">The following array contains a list of AAC encoding formats.</span></span>


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
> <span data-ttu-id="45030-130">Las `H264ProfileInfo` `AACProfileInfo` estructuras y definidas aquí no forman parte de la API de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="45030-130">The `H264ProfileInfo` and `AACProfileInfo` structures defined here are not part of the Media Foundation API.</span></span>

 

## <a name="write-the-wmain-function"></a><span data-ttu-id="45030-131">Escribir la función wmain</span><span class="sxs-lookup"><span data-stu-id="45030-131">Write the wmain Function</span></span>

<span data-ttu-id="45030-132">En el código siguiente se muestra el punto de entrada de la aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="45030-132">The following code shows the entry point for the console application.</span></span>


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



<span data-ttu-id="45030-133">La `wmain` función hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="45030-133">The `wmain` function does the following:</span></span>

1.  <span data-ttu-id="45030-134">Llama a la función [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="45030-134">Calls the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library.</span></span>
2.  <span data-ttu-id="45030-135">Llama a la función [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="45030-135">Calls the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize Media Foundation.</span></span>
3.  <span data-ttu-id="45030-136">Llama a la función definida por la aplicación `EncodeFile` .</span><span class="sxs-lookup"><span data-stu-id="45030-136">Calls the application-defined `EncodeFile` function.</span></span> <span data-ttu-id="45030-137">Esta función transcodifica el archivo de entrada en el archivo de salida y se muestra en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="45030-137">This function transcodes the input file to the output file, and is shown in the next section.</span></span>
4.  <span data-ttu-id="45030-138">Llama a la función [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para cerrar Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="45030-138">Calls the [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) function to shut down Media Foundation.</span></span>
5.  <span data-ttu-id="45030-139">Llame a la función [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) para anular la inicialización de la biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="45030-139">Call the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function to uninitialize the COM library.</span></span>

## <a name="encode-the-file"></a><span data-ttu-id="45030-140">Codificar el archivo</span><span class="sxs-lookup"><span data-stu-id="45030-140">Encode the File</span></span>

<span data-ttu-id="45030-141">En el código siguiente se muestra `EncodeFile` la función, que realiza la transcodificación.</span><span class="sxs-lookup"><span data-stu-id="45030-141">The following code shows `EncodeFile` function, which performs the transcoding.</span></span> <span data-ttu-id="45030-142">Esta función se compone principalmente de llamadas a otras funciones definidas por la aplicación, que se muestran más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="45030-142">This function consists mostly of calls to other application-defined functions, which are shown later in this topic.</span></span>


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



<span data-ttu-id="45030-143">La `EncodeFile` función realiza los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="45030-143">The `EncodeFile` function performs the following steps.</span></span>

1.  <span data-ttu-id="45030-144">Crea un origen de medios para el archivo de entrada mediante la dirección URL o la ruta de acceso del archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="45030-144">Creates a media source for the input file, using the URL or file path of the input file.</span></span> <span data-ttu-id="45030-145">(Consulte [crear el origen de medios](#create-the-media-source)).</span><span class="sxs-lookup"><span data-stu-id="45030-145">(See [Create the Media Source](#create-the-media-source).)</span></span>
2.  <span data-ttu-id="45030-146">Obtiene la duración del archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="45030-146">Gets the duration of the input file.</span></span> <span data-ttu-id="45030-147">(Consulte [obtención de la duración de origen](#get-the-source-duration)).</span><span class="sxs-lookup"><span data-stu-id="45030-147">(See [Get the Source Duration](#get-the-source-duration).)</span></span>
3.  <span data-ttu-id="45030-148">Cree el perfil de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="45030-148">Create the transcode profile.</span></span> <span data-ttu-id="45030-149">(Consulte [creación del perfil de transcodificación](#create-the-transcode-profile)).</span><span class="sxs-lookup"><span data-stu-id="45030-149">(See [Create the Transcode Profile](#create-the-transcode-profile).)</span></span>
4.  <span data-ttu-id="45030-150">Llame a [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) para crear la topología de transcodificación parcial.</span><span class="sxs-lookup"><span data-stu-id="45030-150">Call [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) to create the partial transcode topology.</span></span>
5.  <span data-ttu-id="45030-151">Cree un objeto auxiliar que administre la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="45030-151">Create a helper object that manages the Media Session.</span></span> <span data-ttu-id="45030-152">(Consulte aplicación auxiliar de sesión multimedia).</span><span class="sxs-lookup"><span data-stu-id="45030-152">(See Media Session Helper).</span></span>
6.  <span data-ttu-id="45030-153">Ejecute la sesión de codificación y espere a que se complete.</span><span class="sxs-lookup"><span data-stu-id="45030-153">Run the encoding session and wait for it to complete.</span></span> <span data-ttu-id="45030-154">(Consulte [ejecución de la sesión de codificación](#run-the-encoding-session)).</span><span class="sxs-lookup"><span data-stu-id="45030-154">(See [Run the Encoding Session](#run-the-encoding-session).)</span></span>
7.  <span data-ttu-id="45030-155">Llame a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para cerrar el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="45030-155">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
8.  <span data-ttu-id="45030-156">Punteros de interfaz de la versión.</span><span class="sxs-lookup"><span data-stu-id="45030-156">Release interface pointers.</span></span> <span data-ttu-id="45030-157">Este código usa la función [SafeRelease](saferelease.md) para liberar punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="45030-157">This code uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span> <span data-ttu-id="45030-158">Otra opción es usar una clase de puntero inteligente COM, como **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="45030-158">Another option is to use a COM smart pointer class, such as **CComPtr**.</span></span>

### <a name="create-the-media-source"></a><span data-ttu-id="45030-159">Crear el origen de medios</span><span class="sxs-lookup"><span data-stu-id="45030-159">Create the Media Source</span></span>

<span data-ttu-id="45030-160">El origen multimedia es el objeto que lee y analiza el archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="45030-160">The media source is the object that reads and parses the input file.</span></span> <span data-ttu-id="45030-161">Para crear el origen de medios, pase la dirección URL del archivo de entrada al [solucionador de origen](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="45030-161">To create the media source, pass the URL of the input file to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="45030-162">El código siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="45030-162">The following code shows how to do this.</span></span>


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



<span data-ttu-id="45030-163">Para obtener más información, vea [usar el solucionador de origen](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="45030-163">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

### <a name="get-the-source-duration"></a><span data-ttu-id="45030-164">Obtener la duración de origen</span><span class="sxs-lookup"><span data-stu-id="45030-164">Get the Source Duration</span></span>

<span data-ttu-id="45030-165">Aunque no es necesario, resulta útil consultar el origen de los medios mientras dure el archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="45030-165">Although not required, it is useful to query the media source for the duration of the input file.</span></span> <span data-ttu-id="45030-166">Este valor se puede usar para realizar el seguimiento del progreso de la codificación.</span><span class="sxs-lookup"><span data-stu-id="45030-166">This value can be used to track the encoding progress.</span></span> <span data-ttu-id="45030-167">La duración se almacena en el atributo [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) del descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="45030-167">The duration is stored in the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute of the presentation descriptor.</span></span> <span data-ttu-id="45030-168">Obtiene el descriptor de la presentación mediante una llamada a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="45030-168">Get the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>


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



### <a name="create-the-transcode-profile"></a><span data-ttu-id="45030-169">Crear el perfil de transcodificación</span><span class="sxs-lookup"><span data-stu-id="45030-169">Create the Transcode Profile</span></span>

<span data-ttu-id="45030-170">El perfil de transcodificación describe los parámetros de codificación.</span><span class="sxs-lookup"><span data-stu-id="45030-170">The transcode profile describes the encoding parameters.</span></span> <span data-ttu-id="45030-171">Para obtener más información sobre la creación de un perfil de transcodificación, consulte [uso de la API de Transcode](fast-transcode-objects.md).</span><span class="sxs-lookup"><span data-stu-id="45030-171">For more information about creating a transcode profile, see [Using the Transcode API](fast-transcode-objects.md).</span></span> <span data-ttu-id="45030-172">Para crear el perfil, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="45030-172">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="45030-173">Llame a [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) para crear el perfil vacío.</span><span class="sxs-lookup"><span data-stu-id="45030-173">Call [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) to create the empty profile.</span></span>
2.  <span data-ttu-id="45030-174">Cree un tipo de medio para la secuencia de audio AAC.</span><span class="sxs-lookup"><span data-stu-id="45030-174">Create a media type for the AAC audio stream.</span></span> <span data-ttu-id="45030-175">Agréguelo al perfil llamando a [**IMFTranscodeProfile:: SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span><span class="sxs-lookup"><span data-stu-id="45030-175">Add it to the profile by calling [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span>
3.  <span data-ttu-id="45030-176">Cree un tipo de medio para la secuencia de vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="45030-176">Create a media type for the H.264 video stream.</span></span> <span data-ttu-id="45030-177">Agréguelo al perfil llamando a [**IMFTranscodeProfile:: SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span><span class="sxs-lookup"><span data-stu-id="45030-177">Add it to the profile by calling [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span>
4.  <span data-ttu-id="45030-178">Llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un almacén de atributos para los atributos de nivel de contenedor.</span><span class="sxs-lookup"><span data-stu-id="45030-178">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
5.  <span data-ttu-id="45030-179">Establezca el atributo [MF \_ Transcode \_ CONTAINERTYPE](mf-transcode-containertype.md) .</span><span class="sxs-lookup"><span data-stu-id="45030-179">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute.</span></span> <span data-ttu-id="45030-180">Este es el único atributo de nivel de contenedor necesario.</span><span class="sxs-lookup"><span data-stu-id="45030-180">This is the only required container-level attribute.</span></span> <span data-ttu-id="45030-181">Para la salida del archivo MP4, establezca este atributo en **MFTranscodeContainerType \_ MPEG4**.</span><span class="sxs-lookup"><span data-stu-id="45030-181">For MP4 file output, set this attribute to **MFTranscodeContainerType\_MPEG4**.</span></span>
6.  <span data-ttu-id="45030-182">Llame a [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) para establecer los atributos de nivel de contenedor.</span><span class="sxs-lookup"><span data-stu-id="45030-182">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes.</span></span>

<span data-ttu-id="45030-183">En el código siguiente se muestran estos pasos.</span><span class="sxs-lookup"><span data-stu-id="45030-183">The following code shows these steps.</span></span>


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



<span data-ttu-id="45030-184">Para especificar los atributos de la secuencia de vídeo H. 264, cree un almacén de atributos y establezca los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="45030-184">To specify the attributes for the H.264 video stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="45030-185">Atributo</span><span class="sxs-lookup"><span data-stu-id="45030-185">Attribute</span></span>                                                       | <span data-ttu-id="45030-186">Descripción</span><span class="sxs-lookup"><span data-stu-id="45030-186">Desription</span></span>                      |
|-----------------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="45030-187">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="45030-187">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)              | <span data-ttu-id="45030-188">Establézcalo en **MFVideoFormat \_ H264**.</span><span class="sxs-lookup"><span data-stu-id="45030-188">Set to **MFVideoFormat\_H264**.</span></span> |
| [<span data-ttu-id="45030-189">**\_Perfil MF MT \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="45030-189">**MF\_MT\_MPEG2\_PROFILE**</span></span>](mf-mt-mpeg2-profile-attribute.md) | <span data-ttu-id="45030-190">Perfil H. 264.</span><span class="sxs-lookup"><span data-stu-id="45030-190">H.264 profile.</span></span>                  |
| [<span data-ttu-id="45030-191">**\_tamaño de \_ marco MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="45030-191">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)       | <span data-ttu-id="45030-192">Tamaño del marco.</span><span class="sxs-lookup"><span data-stu-id="45030-192">Frame size.</span></span>                     |
| [<span data-ttu-id="45030-193">**\_velocidad de \_ fotogramas MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="45030-193">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)       | <span data-ttu-id="45030-194">Velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="45030-194">Frame rate.</span></span>                     |
| [<span data-ttu-id="45030-195">**\_velocidad de \_ bits media MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="45030-195">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)     | <span data-ttu-id="45030-196">Velocidad de bits codificada.</span><span class="sxs-lookup"><span data-stu-id="45030-196">Encoded bit rate.</span></span>               |



 

<span data-ttu-id="45030-197">Para especificar los atributos de la secuencia de audio AAC, cree un almacén de atributos y establezca los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="45030-197">To specify the attributes for the AAC audio stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="45030-198">Atributo</span><span class="sxs-lookup"><span data-stu-id="45030-198">Attribute</span></span>                                                                                      | <span data-ttu-id="45030-199">Descripción</span><span class="sxs-lookup"><span data-stu-id="45030-199">Desription</span></span>                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [<span data-ttu-id="45030-200">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="45030-200">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="45030-201">Establecer en **MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="45030-201">Set to **MFAudioFormat\_AAC**</span></span>            |
| [<span data-ttu-id="45030-202">**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="45030-202">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="45030-203">Velocidad de muestra de audio.</span><span class="sxs-lookup"><span data-stu-id="45030-203">Audio sample rate.</span></span>                       |
| [<span data-ttu-id="45030-204">**MF \_ MT \_ audio \_ bits \_ por \_ muestra**</span><span class="sxs-lookup"><span data-stu-id="45030-204">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="45030-205">Ejemplo de bits por audio.</span><span class="sxs-lookup"><span data-stu-id="45030-205">Bits per audio sample.</span></span>                   |
| [<span data-ttu-id="45030-206">**\_canales de \_ número de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="45030-206">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="45030-207">Número de canales de audio.</span><span class="sxs-lookup"><span data-stu-id="45030-207">Number of audio channels.</span></span>                |
| [<span data-ttu-id="45030-208">**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="45030-208">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="45030-209">Velocidad de bits codificada.</span><span class="sxs-lookup"><span data-stu-id="45030-209">Encoded bit rate.</span></span>                        |
| [<span data-ttu-id="45030-210">**\_alineación del \_ bloque de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="45030-210">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="45030-211">establézcalo en 1.</span><span class="sxs-lookup"><span data-stu-id="45030-211">Set to 1.</span></span>                                |
| [<span data-ttu-id="45030-212">\_indicación de \_ \_ nivel de \_ Perfil de audio \_ \_ MF MT AAC</span><span class="sxs-lookup"><span data-stu-id="45030-212">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="45030-213">Indicación del nivel de perfil AAC (opcional).</span><span class="sxs-lookup"><span data-stu-id="45030-213">AAC profile level indication (optional).</span></span> |



 

<span data-ttu-id="45030-214">En el código siguiente se crean los atributos de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="45030-214">The following code creates the video stream attributes.</span></span>


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



<span data-ttu-id="45030-215">En el código siguiente se crean los atributos de secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="45030-215">The following code creates the audio stream attributes.</span></span>


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



<span data-ttu-id="45030-216">Tenga en cuenta que la API de Transcode no requiere un tipo de medio real, aunque utiliza atributos de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="45030-216">Note that the transcode API does not require a true media type, although it uses media-type attributes.</span></span> <span data-ttu-id="45030-217">En concreto, el atributo de [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) no es necesario, ya que los métodos [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) y [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) implican el tipo principal.</span><span class="sxs-lookup"><span data-stu-id="45030-217">In particular, the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute it not required, because the [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) and [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) methods imply the major type.</span></span> <span data-ttu-id="45030-218">Sin embargo, también es válido para pasar un tipo de medio real a estos métodos.</span><span class="sxs-lookup"><span data-stu-id="45030-218">However, it also valid to pass an actual media type to these methods.</span></span> <span data-ttu-id="45030-219">(La interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) hereda [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)).</span><span class="sxs-lookup"><span data-stu-id="45030-219">(The [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface inherits [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)</span></span>

### <a name="run-the-encoding-session"></a><span data-ttu-id="45030-220">Ejecutar la sesión de codificación</span><span class="sxs-lookup"><span data-stu-id="45030-220">Run the Encoding Session</span></span>

<span data-ttu-id="45030-221">En el código siguiente se ejecuta la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="45030-221">The following code runs the encoding session.</span></span> <span data-ttu-id="45030-222">Usa la clase auxiliar de sesión de medios, que se muestra en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="45030-222">It uses the Media Session helper class, which is shown in the next section.</span></span>


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



## <a name="media-session-helper"></a><span data-ttu-id="45030-223">Aplicación auxiliar de sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="45030-223">Media Session Helper</span></span>

<span data-ttu-id="45030-224">La [sesión multimedia](media-session.md) se describe más detalladamente en la sección [Media Foundation arquitectura](media-foundation-architecture.md) de esta documentación.</span><span class="sxs-lookup"><span data-stu-id="45030-224">The [Media Session](media-session.md) is described more fully in the [Media Foundation Architecture](media-foundation-architecture.md) section of this documentation.</span></span> <span data-ttu-id="45030-225">La sesión multimedia utiliza un modelo de eventos asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="45030-225">The Media Session uses an asynchronous event model.</span></span> <span data-ttu-id="45030-226">En una aplicación de GUI, debe responder a los eventos de sesión sin bloquear el subproceso de interfaz de usuario para esperar al siguiente evento.</span><span class="sxs-lookup"><span data-stu-id="45030-226">In a GUI application, you should respond to session events without blocking the UI thread to wait for the next event.</span></span> <span data-ttu-id="45030-227">En el tutorial [Cómo reproducir archivos multimedia no protegidos](how-to-play-unprotected-media-files.md) se muestra cómo hacerlo en una aplicación de reproducción.</span><span class="sxs-lookup"><span data-stu-id="45030-227">The tutorial [How to Play Unprotected Media Files](how-to-play-unprotected-media-files.md) shows how to do this in a playback application.</span></span> <span data-ttu-id="45030-228">Para la codificación, el principio es el mismo, pero hay menos eventos relevantes:</span><span class="sxs-lookup"><span data-stu-id="45030-228">For encoding, the principle is the same, but fewer events are relevant:</span></span>



| <span data-ttu-id="45030-229">Evento</span><span class="sxs-lookup"><span data-stu-id="45030-229">Event</span></span>                                  | <span data-ttu-id="45030-230">Descripción</span><span class="sxs-lookup"><span data-stu-id="45030-230">Desription</span></span>                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45030-231">MESessionEnded</span><span class="sxs-lookup"><span data-stu-id="45030-231">MESessionEnded</span></span>](mesessionended.md)   | <span data-ttu-id="45030-232">Se genera cuando se completa la codificación.</span><span class="sxs-lookup"><span data-stu-id="45030-232">Raised when the encoding is complete.</span></span>                                                                                                                            |
| [<span data-ttu-id="45030-233">MESessionClosed</span><span class="sxs-lookup"><span data-stu-id="45030-233">MESessionClosed</span></span>](mesessionclosed.md) | <span data-ttu-id="45030-234">Se genera cuando se completa el método [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) .</span><span class="sxs-lookup"><span data-stu-id="45030-234">Raised when the [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) method completes.</span></span> <span data-ttu-id="45030-235">Una vez que se genera este evento, es seguro apagar la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="45030-235">After this event is raised, it is safe to shut down the Media Session.</span></span> |



 

<span data-ttu-id="45030-236">En el caso de una aplicación de consola, es razonable bloquear y esperar eventos.</span><span class="sxs-lookup"><span data-stu-id="45030-236">For a console application, it is reasonable to block and wait for events.</span></span> <span data-ttu-id="45030-237">Dependiendo del archivo de código fuente y de la configuración de la codificación, la codificación podría tardar unos minutos en completarse.</span><span class="sxs-lookup"><span data-stu-id="45030-237">Depending on the source file and the encoding settings, it might take awhile to complete the encoding.</span></span> <span data-ttu-id="45030-238">Puede obtener actualizaciones de progreso como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="45030-238">You can get progress updates as follows:</span></span>

1.  <span data-ttu-id="45030-239">Llame a [**IMFMediaSession:: GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) para obtener el reloj de la presentación.</span><span class="sxs-lookup"><span data-stu-id="45030-239">Call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) to get the presentation clock.</span></span>
2.  <span data-ttu-id="45030-240">Consulte el reloj de la interfaz [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) .</span><span class="sxs-lookup"><span data-stu-id="45030-240">Query the clock for the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span>
3.  <span data-ttu-id="45030-241">Llame a [**IMFPresentationClock:: getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) para obtener la posición actual.</span><span class="sxs-lookup"><span data-stu-id="45030-241">Call [**IMFPresentationClock::GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) to get the current position.</span></span>
4.  <span data-ttu-id="45030-242">La posición se proporciona en unidades de tiempo.</span><span class="sxs-lookup"><span data-stu-id="45030-242">The position is given in units of time.</span></span> <span data-ttu-id="45030-243">Para obtener el porcentaje completado, use el valor `(100 * position) / duration` .</span><span class="sxs-lookup"><span data-stu-id="45030-243">To get the percentage completed, use the value `(100 * position) / duration`.</span></span>

<span data-ttu-id="45030-244">Esta es la declaración de la `CSession` clase.</span><span class="sxs-lookup"><span data-stu-id="45030-244">Here is the declaration of the `CSession` class.</span></span>


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



<span data-ttu-id="45030-245">En el código siguiente se muestra la implementación completa de la `CSession` clase.</span><span class="sxs-lookup"><span data-stu-id="45030-245">The following code shows the complete implementation of the `CSession` class.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="45030-246">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45030-246">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45030-247">**Codificador AAC**</span><span class="sxs-lookup"><span data-stu-id="45030-247">**AAC Encoder**</span></span>](aac-encoder.md)
</dt> <dt>

[<span data-ttu-id="45030-248">**Codificador de vídeo H. 264**</span><span class="sxs-lookup"><span data-stu-id="45030-248">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="45030-249">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="45030-249">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="45030-250">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="45030-250">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="45030-251">API de transcodificación</span><span class="sxs-lookup"><span data-stu-id="45030-251">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 
