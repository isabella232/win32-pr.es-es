---
description: En este tutorial se muestra cómo usar el lector de origen para descodificar el audio de un archivo multimedia y escribir el audio en un archivo de sonido.
ms.assetid: ed40e201-c6ed-444f-bdaa-a5f33d1cc068
title: 'Tutorial: descodificar audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eb6d9f48419b62fa1c379c636abaf2bb0a63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568278"
---
# <a name="tutorial-decoding-audio"></a><span data-ttu-id="96b78-103">Tutorial: descodificar audio</span><span class="sxs-lookup"><span data-stu-id="96b78-103">Tutorial: Decoding Audio</span></span>

<span data-ttu-id="96b78-104">En este tutorial se muestra cómo usar el [lector de origen](source-reader.md) para descodificar el audio de un archivo multimedia y escribir el audio en un archivo de sonido.</span><span class="sxs-lookup"><span data-stu-id="96b78-104">This tutorial shows how to use the [Source Reader](source-reader.md) to decode audio from a media file and write the audio to a WAVE file.</span></span> <span data-ttu-id="96b78-105">El tutorial se basa en el ejemplo de [clip de audio](audio-clip-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="96b78-105">The tutorial is based on the [Audio Clip](audio-clip-sample.md) sample.</span></span>

-   [<span data-ttu-id="96b78-106">Información general</span><span class="sxs-lookup"><span data-stu-id="96b78-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="96b78-107">Archivos de encabezado y de biblioteca</span><span class="sxs-lookup"><span data-stu-id="96b78-107">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="96b78-108">Implementar wmain</span><span class="sxs-lookup"><span data-stu-id="96b78-108">Implement wmain</span></span>](#implement-wmain)
-   [<span data-ttu-id="96b78-109">Escribir el archivo de onda</span><span class="sxs-lookup"><span data-stu-id="96b78-109">Write the WAVE File</span></span>](#write-the-wave-file)
-   [<span data-ttu-id="96b78-110">Configuración del lector de origen</span><span class="sxs-lookup"><span data-stu-id="96b78-110">Configure the Source Reader</span></span>](#configure-the-source-reader)
-   [<span data-ttu-id="96b78-111">Escribir el encabezado del archivo de onda</span><span class="sxs-lookup"><span data-stu-id="96b78-111">Write the WAVE File Header</span></span>](#write-the-wave-file-header)
-   [<span data-ttu-id="96b78-112">Calcular el tamaño máximo de los datos</span><span class="sxs-lookup"><span data-stu-id="96b78-112">Calculate the Maximum Data Size</span></span>](#calculate-the-maximum-data-size)
-   [<span data-ttu-id="96b78-113">Descodificación del audio</span><span class="sxs-lookup"><span data-stu-id="96b78-113">Decode the Audio</span></span>](#decode-the-audio)
-   [<span data-ttu-id="96b78-114">Finalización del encabezado del archivo</span><span class="sxs-lookup"><span data-stu-id="96b78-114">Finalize the File Header</span></span>](#finalize-the-file-header)
-   [<span data-ttu-id="96b78-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="96b78-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="96b78-116">Información general</span><span class="sxs-lookup"><span data-stu-id="96b78-116">Overview</span></span>

<span data-ttu-id="96b78-117">En este tutorial, creará una aplicación de consola que toma dos argumentos de línea de comandos: el nombre de un archivo de entrada que contiene una secuencia de audio y el nombre del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="96b78-117">In this tutorial, you will create a console application that takes two command-line arguments: The name of an input file that contains an audio stream, and the output file name.</span></span> <span data-ttu-id="96b78-118">La aplicación Lee cinco segundos de datos de audio del archivo de entrada y escribe el audio en el archivo de salida como datos de onda.</span><span class="sxs-lookup"><span data-stu-id="96b78-118">The application reads five seconds of audio data from the input file and writes the audio to the output file as WAVE data.</span></span>

<span data-ttu-id="96b78-119">Para obtener los datos de audio descodificados, la aplicación utiliza el objeto lector de origen.</span><span class="sxs-lookup"><span data-stu-id="96b78-119">To get the decoded audio data, the application uses the source reader object.</span></span> <span data-ttu-id="96b78-120">El lector de origen expone la interfaz [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .</span><span class="sxs-lookup"><span data-stu-id="96b78-120">The source reader exposes the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface.</span></span> <span data-ttu-id="96b78-121">Para escribir el audio descodificado en el archivo de onda, las aplicaciones usan las funciones de e/s de Windows.</span><span class="sxs-lookup"><span data-stu-id="96b78-121">To write the decoded audio to the WAVE file, the applications uses Windows I/O functions.</span></span> <span data-ttu-id="96b78-122">En la imagen siguiente se ilustra este proceso.</span><span class="sxs-lookup"><span data-stu-id="96b78-122">The following image illustrates this process.</span></span>

![diagrama que muestra el lector de origen que obtiene datos de audio del archivo de código fuente.](images/audio-clip-tutorial.gif)

<span data-ttu-id="96b78-124">En su forma más simple, un archivo de onda tiene la estructura siguiente:</span><span class="sxs-lookup"><span data-stu-id="96b78-124">In its simplest form, a WAVE file has the following structure:</span></span>



| <span data-ttu-id="96b78-125">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="96b78-125">Data Type</span></span>                              | <span data-ttu-id="96b78-126">Tamaño (bytes)</span><span class="sxs-lookup"><span data-stu-id="96b78-126">Size (Bytes)</span></span> | <span data-ttu-id="96b78-127">Value</span><span class="sxs-lookup"><span data-stu-id="96b78-127">Value</span></span>                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| <span data-ttu-id="96b78-128">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="96b78-128">**FOURCC**</span></span>                             | <span data-ttu-id="96b78-129">4</span><span class="sxs-lookup"><span data-stu-id="96b78-129">4</span></span>            | <span data-ttu-id="96b78-130">RIFF</span><span class="sxs-lookup"><span data-stu-id="96b78-130">'RIFF'</span></span>                                                                |
| <span data-ttu-id="96b78-131">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="96b78-131">**DWORD**</span></span>                              | <span data-ttu-id="96b78-132">4</span><span class="sxs-lookup"><span data-stu-id="96b78-132">4</span></span>            | <span data-ttu-id="96b78-133">Tamaño total del archivo, sin incluir los primeros 8 bytes</span><span class="sxs-lookup"><span data-stu-id="96b78-133">Total file size, not including the first 8 bytes</span></span>                      |
| <span data-ttu-id="96b78-134">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="96b78-134">**FOURCC**</span></span>                             | <span data-ttu-id="96b78-135">4</span><span class="sxs-lookup"><span data-stu-id="96b78-135">4</span></span>            | <span data-ttu-id="96b78-136">ONDAS</span><span class="sxs-lookup"><span data-stu-id="96b78-136">'WAVE'</span></span>                                                                |
| <span data-ttu-id="96b78-137">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="96b78-137">**FOURCC**</span></span>                             | <span data-ttu-id="96b78-138">4</span><span class="sxs-lookup"><span data-stu-id="96b78-138">4</span></span>            | <span data-ttu-id="96b78-139">FMT</span><span class="sxs-lookup"><span data-stu-id="96b78-139">'fmt '</span></span>                                                                |
| <span data-ttu-id="96b78-140">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="96b78-140">**DWORD**</span></span>                              | <span data-ttu-id="96b78-141">4</span><span class="sxs-lookup"><span data-stu-id="96b78-141">4</span></span>            | <span data-ttu-id="96b78-142">Tamaño de los datos de [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="96b78-142">Size of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) data that follows.</span></span> |
| <span data-ttu-id="96b78-143">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="96b78-143">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="96b78-144">Varía</span><span class="sxs-lookup"><span data-stu-id="96b78-144">Varies</span></span>       | <span data-ttu-id="96b78-145">Encabezado de formato de audio.</span><span class="sxs-lookup"><span data-stu-id="96b78-145">Audio format header.</span></span>                                                  |
| <span data-ttu-id="96b78-146">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="96b78-146">**FOURCC**</span></span>                             | <span data-ttu-id="96b78-147">4</span><span class="sxs-lookup"><span data-stu-id="96b78-147">4</span></span>            | <span data-ttu-id="96b78-148">Data</span><span class="sxs-lookup"><span data-stu-id="96b78-148">'data'</span></span>                                                                |
| <span data-ttu-id="96b78-149">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="96b78-149">**DWORD**</span></span>                              | <span data-ttu-id="96b78-150">4</span><span class="sxs-lookup"><span data-stu-id="96b78-150">4</span></span>            | <span data-ttu-id="96b78-151">Tamaño de los datos de audio.</span><span class="sxs-lookup"><span data-stu-id="96b78-151">Size of the audio data.</span></span>                                               |
| <span data-ttu-id="96b78-152">**BYTES**\[\]</span><span class="sxs-lookup"><span data-stu-id="96b78-152">**BYTE**\[\]</span></span>                           | <span data-ttu-id="96b78-153">Varía</span><span class="sxs-lookup"><span data-stu-id="96b78-153">Varies</span></span>       | <span data-ttu-id="96b78-154">Datos de audio.</span><span class="sxs-lookup"><span data-stu-id="96b78-154">Audio data.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="96b78-155">Un **FourCC** es un **valor DWORD** formado mediante la concatenación de cuatro caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="96b78-155">A **FOURCC** is a **DWORD** formed by concatenating four ASCII characters.</span></span>

 

<span data-ttu-id="96b78-156">Esta estructura básica se puede extender agregando metadatos de archivo y otra información, que queda fuera del ámbito de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="96b78-156">This basic structure can be extended by adding file metadata and other information, which is beyond the scope of this tutorial.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="96b78-157">Archivos de encabezado y de biblioteca</span><span class="sxs-lookup"><span data-stu-id="96b78-157">Header and Library Files</span></span>

<span data-ttu-id="96b78-158">Incluya los siguientes archivos de encabezado en el proyecto:</span><span class="sxs-lookup"><span data-stu-id="96b78-158">Include the following header files in your project:</span></span>


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



<span data-ttu-id="96b78-159">Vincule a las siguientes bibliotecas:</span><span class="sxs-lookup"><span data-stu-id="96b78-159">Link to the following libraries:</span></span>

-   <span data-ttu-id="96b78-160">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="96b78-160">mfplat.lib</span></span>
-   <span data-ttu-id="96b78-161">mfreadwrite. lib</span><span class="sxs-lookup"><span data-stu-id="96b78-161">mfreadwrite.lib</span></span>
-   <span data-ttu-id="96b78-162">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="96b78-162">mfuuid.lib</span></span>

## <a name="implement-wmain"></a><span data-ttu-id="96b78-163">Implementar wmain</span><span class="sxs-lookup"><span data-stu-id="96b78-163">Implement wmain</span></span>

<span data-ttu-id="96b78-164">En el código siguiente se muestra la función de punto de entrada para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="96b78-164">The following code shows the entry-point function for the application.</span></span>


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        printf("arguments: input_file output_file.wav\n");
        return 1;
    }

    const WCHAR *wszSourceFile = argv[1];
    const WCHAR *wszTargetFile = argv[2];

    const LONG MAX_AUDIO_DURATION_MSEC = 5000; // 5 seconds

    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    HANDLE hFile = INVALID_HANDLE_VALUE;

    // Initialize the COM library.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    // Initialize the Media Foundation platform.
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
    }

    // Create the source reader to read the input file.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSourceReaderFromURL(wszSourceFile, NULL, &pReader);
        if (FAILED(hr))
        {
            printf("Error opening input file: %S\n", wszSourceFile, hr);
        }
    }

    // Open the output file for writing.
    if (SUCCEEDED(hr))
    {
        hFile = CreateFile(wszTargetFile, GENERIC_WRITE, FILE_SHARE_READ, NULL,
            CREATE_ALWAYS, 0, NULL);

        if (hFile == INVALID_HANDLE_VALUE)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            printf("Cannot create output file: %S\n", wszTargetFile, hr);
        }
    }

    // Write the WAVE file.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveFile(pReader, hFile, MAX_AUDIO_DURATION_MSEC);
    }

    if (FAILED(hr))
    {
        printf("Failed, hr = 0x%X\n", hr);
    }

    // Clean up.
    if (hFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(hFile);
    }

    SafeRelease(&pReader);
    MFShutdown();
    CoUninitialize();

    return SUCCEEDED(hr) ? 0 : 1;
};
```



<span data-ttu-id="96b78-165">Esta función hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="96b78-165">This function does the following:</span></span>

1.  <span data-ttu-id="96b78-166">Llama a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="96b78-166">Calls [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="96b78-167">Llama a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar la plataforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="96b78-167">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
3.  <span data-ttu-id="96b78-168">Llama a [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) para crear el lector de origen.</span><span class="sxs-lookup"><span data-stu-id="96b78-168">Calls [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) to create the source reader.</span></span> <span data-ttu-id="96b78-169">Esta función toma el nombre del archivo de entrada y recibe un puntero de la interfaz [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) .</span><span class="sxs-lookup"><span data-stu-id="96b78-169">This function takes the name of the input file and receives an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface pointer.</span></span>
4.  <span data-ttu-id="96b78-170">Crea el archivo de salida mediante una llamada a la función **CreateFile** , que devuelve un identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="96b78-170">Creates the output file by calling the **CreateFile** function, which returns a file handle.</span></span>
5.  <span data-ttu-id="96b78-171">Llama a la función [WriteWavFile](#write-the-wave-file) definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="96b78-171">Calls the application-defined [WriteWavFile](#write-the-wave-file) function.</span></span> <span data-ttu-id="96b78-172">Esta función descodifica el audio y escribe el archivo de onda.</span><span class="sxs-lookup"><span data-stu-id="96b78-172">This function decodes the audio and writes the WAVE file.</span></span>
6.  <span data-ttu-id="96b78-173">Libera el puntero [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) y el identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="96b78-173">Releases the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer and the file handle.</span></span>
7.  <span data-ttu-id="96b78-174">Llama a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para cerrar la plataforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="96b78-174">Calls [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>
8.  <span data-ttu-id="96b78-175">Llama a [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) para liberar la biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="96b78-175">Calls [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to release the COM library.</span></span>

## <a name="write-the-wave-file"></a><span data-ttu-id="96b78-176">Escribir el archivo de onda</span><span class="sxs-lookup"><span data-stu-id="96b78-176">Write the WAVE File</span></span>

<span data-ttu-id="96b78-177">La mayor parte del trabajo ocurre en la `WriteWavFile` función, a la que se llama desde `wmain` .</span><span class="sxs-lookup"><span data-stu-id="96b78-177">Most of the work happens in the `WriteWavFile` function, which is called from `wmain`.</span></span>


```C++
//-------------------------------------------------------------------
// WriteWaveFile
//
// Writes a WAVE file by getting audio data from the source reader.
//
//-------------------------------------------------------------------

HRESULT WriteWaveFile(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    HANDLE hFile,               // Handle to the output file.
    LONG msecAudioData          // Maximum amount of audio data to write, in msec.
    )
{
    HRESULT hr = S_OK;

    DWORD cbHeader = 0;         // Size of the WAVE file header, in bytes.
    DWORD cbAudioData = 0;      // Total bytes of PCM audio data written to the file.
    DWORD cbMaxAudioData = 0;

    IMFMediaType *pAudioType = NULL;    // Represents the PCM audio format.

    // Configure the source reader to get uncompressed PCM audio from the source file.

    hr = ConfigureAudioStream(pReader, &pAudioType);

    // Write the WAVE file header.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveHeader(hFile, pAudioType, &cbHeader);
    }

    // Calculate the maximum amount of audio to decode, in bytes.
    if (SUCCEEDED(hr))
    {
        cbMaxAudioData = CalculateMaxAudioDataSize(pAudioType, cbHeader, msecAudioData);

        // Decode audio data to the file.
        hr = WriteWaveData(hFile, pReader, cbMaxAudioData, &cbAudioData);
    }

    // Fix up the RIFF headers with the correct sizes.
    if (SUCCEEDED(hr))
    {
        hr = FixUpChunkSizes(hFile, cbHeader, cbAudioData);
    }

    SafeRelease(&pAudioType);
    return hr;
}
```



<span data-ttu-id="96b78-178">Esta función llama a una serie de otras funciones definidas por la aplicación:</span><span class="sxs-lookup"><span data-stu-id="96b78-178">This function calls a series of other application-defined functions:</span></span>

1.  <span data-ttu-id="96b78-179">La función [ConfigureAudioStream](#configure-the-source-reader) inicializa el lector de origen.</span><span class="sxs-lookup"><span data-stu-id="96b78-179">The [ConfigureAudioStream](#configure-the-source-reader) function initializes the source reader.</span></span> <span data-ttu-id="96b78-180">Esta función recibe un puntero a la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , que se usa para obtener una descripción del formato de audio descodificado, incluida la velocidad de muestra, el número de canales y la profundidad de bits (bits por muestra).</span><span class="sxs-lookup"><span data-stu-id="96b78-180">This function receives a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which is used to get a description of the decoded audio format, including sample rate, number of channels, and bit depth (bits per sample).</span></span>
2.  <span data-ttu-id="96b78-181">La función WriteWaveHeader escribe la primera parte del archivo de onda, incluido el encabezado y el inicio del fragmento ' Data '.</span><span class="sxs-lookup"><span data-stu-id="96b78-181">The WriteWaveHeader function writes the first part of the WAVE file, including the header and the start of the 'data' chunk.</span></span>
3.  <span data-ttu-id="96b78-182">La función CalculateMaxAudioDataSize calcula la cantidad máxima de audio que se va a escribir en el archivo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="96b78-182">The CalculateMaxAudioDataSize function calculates the maximum amount of audio to write to the file, in bytes.</span></span>
4.  <span data-ttu-id="96b78-183">La función WriteWaveData escribe los datos de audio PCM en el archivo.</span><span class="sxs-lookup"><span data-stu-id="96b78-183">The WriteWaveData function writes the PCM audio data to the file.</span></span>
5.  <span data-ttu-id="96b78-184">La función FixUpChunkSizes escribe la información de tamaño de archivo que aparece después de los valores de **FourCC** ' riff ' y ' Data ' en el archivo de onda.</span><span class="sxs-lookup"><span data-stu-id="96b78-184">The FixUpChunkSizes function writes the file-size information that appears after the 'RIFF' and 'data' **FOURCC** values in the WAVE file.</span></span> <span data-ttu-id="96b78-185">(Estos valores no se conocen hasta que se `WriteWaveData` completa).</span><span class="sxs-lookup"><span data-stu-id="96b78-185">(These values are not known until `WriteWaveData` completes.)</span></span>

<span data-ttu-id="96b78-186">Estas funciones se muestran en las secciones restantes de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="96b78-186">These functions are shown in the remaining sections of this tutorial.</span></span>

## <a name="configure-the-source-reader"></a><span data-ttu-id="96b78-187">Configuración del lector de origen</span><span class="sxs-lookup"><span data-stu-id="96b78-187">Configure the Source Reader</span></span>

<span data-ttu-id="96b78-188">La `ConfigureAudioStream` función configura el lector de origen para descodificar la secuencia de audio en el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="96b78-188">The `ConfigureAudioStream` function configures the source reader to decode the audio stream in the source file.</span></span> <span data-ttu-id="96b78-189">También devuelve información sobre el formato del audio descodificado.</span><span class="sxs-lookup"><span data-stu-id="96b78-189">It also returns information about the format of the decoded audio.</span></span>

<span data-ttu-id="96b78-190">En Media Foundation, los formatos de medios se describen mediante objetos de *tipo de medio* .</span><span class="sxs-lookup"><span data-stu-id="96b78-190">In Media Foundation, media formats are described using *media type* objects.</span></span> <span data-ttu-id="96b78-191">Un objeto de tipo de medio expone la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , que hereda la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="96b78-191">A media type object exposes the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="96b78-192">Esencialmente, un tipo de medio es una colección de propiedades que describen el formato.</span><span class="sxs-lookup"><span data-stu-id="96b78-192">Essentially, a media type is a collection of properties that describe the format.</span></span> <span data-ttu-id="96b78-193">Para obtener más información, consulte [tipos de medios](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="96b78-193">For more information, see [Media Types](media-types.md).</span></span>


```C++
//-------------------------------------------------------------------
// ConfigureAudioStream
//
// Selects an audio stream from the source file, and configures the
// stream to deliver decoded PCM audio.
//-------------------------------------------------------------------

HRESULT ConfigureAudioStream(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    IMFMediaType **ppPCMAudio   // Receives the audio format.
    )
{
    IMFMediaType *pUncompressedAudioType = NULL;
    IMFMediaType *pPartialType = NULL;

    // Select the first audio stream, and deselect all other streams.
    HRESULT hr = pReader->SetStreamSelection(
        (DWORD)MF_SOURCE_READER_ALL_STREAMS, FALSE);

    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM, TRUE);
    }

    // Create a partial media type that specifies uncompressed PCM audio.
    hr = MFCreateMediaType(&pPartialType);

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    }

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    }

    // Set this type on the source reader. The source reader will
    // load the necessary decoder.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            NULL, pPartialType);
    }

    // Get the complete uncompressed format.
    if (SUCCEEDED(hr))
    {
        hr = pReader->GetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            &pUncompressedAudioType);
    }

    // Ensure the stream is selected.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            TRUE);
    }

    // Return the PCM format to the caller.
    if (SUCCEEDED(hr))
    {
        *ppPCMAudio = pUncompressedAudioType;
        (*ppPCMAudio)->AddRef();
    }

    SafeRelease(&pUncompressedAudioType);
    SafeRelease(&pPartialType);
    return hr;
}
```



<span data-ttu-id="96b78-194">La `ConfigureAudioStream` función hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="96b78-194">The `ConfigureAudioStream` function does the following:</span></span>

1.  <span data-ttu-id="96b78-195">Llama al método [**IMFSourceReader:: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) para seleccionar la secuencia de audio y anular la selección de todas las demás secuencias.</span><span class="sxs-lookup"><span data-stu-id="96b78-195">Calls the [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) method to select the audio stream and deselect all other streams.</span></span> <span data-ttu-id="96b78-196">Este paso puede mejorar el rendimiento, ya que impide que el lector de origen se mantenga en fotogramas de vídeo que la aplicación no usa.</span><span class="sxs-lookup"><span data-stu-id="96b78-196">This step can improve performance, because it prevents the source reader from holding onto video frames that the application does not use.</span></span>
2.  <span data-ttu-id="96b78-197">Crea un tipo de medio *parcial* que especifica el audio PCM.</span><span class="sxs-lookup"><span data-stu-id="96b78-197">Creates a *partial* media type that specifies PCM audio.</span></span> <span data-ttu-id="96b78-198">La función crea el tipo parcial de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="96b78-198">The function creates the partial type as follows:</span></span>
    1.  <span data-ttu-id="96b78-199">Llama a [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) para crear un objeto de tipo de medio vacío.</span><span class="sxs-lookup"><span data-stu-id="96b78-199">Calls [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create an empty media type object.</span></span>
    2.  <span data-ttu-id="96b78-200">Establece el atributo de [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) en **MFMediaType \_ audio**.</span><span class="sxs-lookup"><span data-stu-id="96b78-200">Sets the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>
    3.  <span data-ttu-id="96b78-201">Establece el atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) en **MFAudioFormat \_ PCM**.</span><span class="sxs-lookup"><span data-stu-id="96b78-201">Sets the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to **MFAudioFormat\_PCM**.</span></span>
3.  <span data-ttu-id="96b78-202">Llama a [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) para establecer el tipo parcial en el lector de origen.</span><span class="sxs-lookup"><span data-stu-id="96b78-202">Calls [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) to set the partial type on the source reader.</span></span> <span data-ttu-id="96b78-203">Si el archivo de origen contiene audio codificado, el lector de origen carga automáticamente el descodificador de audio necesario.</span><span class="sxs-lookup"><span data-stu-id="96b78-203">If the source file contains encoded audio, the source reader automatically loads the necessary audio decoder.</span></span>
4.  <span data-ttu-id="96b78-204">Llama a [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) para obtener el tipo de medio PCM real.</span><span class="sxs-lookup"><span data-stu-id="96b78-204">Calls [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) to get the actual PCM media type.</span></span> <span data-ttu-id="96b78-205">Este método devuelve un tipo de medio con todos los detalles de formato rellenados, como la velocidad de muestra de audio y el número de canales.</span><span class="sxs-lookup"><span data-stu-id="96b78-205">This method returns a media type with all of the format details filled in, such as the audio sample rate and the number of channels.</span></span>
5.  <span data-ttu-id="96b78-206">Llama a [**IMFSourceReader:: SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) para habilitar la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="96b78-206">Calls [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) to enable the audio stream.</span></span>

## <a name="write-the-wave-file-header"></a><span data-ttu-id="96b78-207">Escribir el encabezado del archivo de onda</span><span class="sxs-lookup"><span data-stu-id="96b78-207">Write the WAVE File Header</span></span>

<span data-ttu-id="96b78-208">La `WriteWaveHeader` función escribe el encabezado del archivo de onda.</span><span class="sxs-lookup"><span data-stu-id="96b78-208">The `WriteWaveHeader` function writes the WAVE file header.</span></span>

<span data-ttu-id="96b78-209">La única Media Foundation API a la que se llama desde esta función es [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), que convierte el tipo de medio en una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="96b78-209">The only Media Foundation API called from this function is [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), which converts the media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>


```C++
//-------------------------------------------------------------------
// WriteWaveHeader
//
// Write the WAVE file header.
//
// Note: This function writes placeholder values for the file size
// and data size, as these values will need to be filled in later.
//-------------------------------------------------------------------

HRESULT WriteWaveHeader(
    HANDLE hFile,               // Output file.
    IMFMediaType *pMediaType,   // PCM audio format.
    DWORD *pcbWritten           // Receives the size of the header.
    )
{
    HRESULT hr = S_OK;
    UINT32 cbFormat = 0;

    WAVEFORMATEX *pWav = NULL;

    *pcbWritten = 0;

    // Convert the PCM audio format into a WAVEFORMATEX structure.
    hr = MFCreateWaveFormatExFromMFMediaType(pMediaType, &pWav, &cbFormat);

    // Write the 'RIFF' header and the start of the 'fmt ' chunk.
    if (SUCCEEDED(hr))
    {
        DWORD header[] = {
            // RIFF header
            FCC('RIFF'),
            0,
            FCC('WAVE'),
            // Start of 'fmt ' chunk
            FCC('fmt '),
            cbFormat
        };

        DWORD dataHeader[] = { FCC('data'), 0 };

        hr = WriteToFile(hFile, header, sizeof(header));

        // Write the WAVEFORMATEX structure.
        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, pWav, cbFormat);
        }

        // Write the start of the 'data' chunk

        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, dataHeader, sizeof(dataHeader));
        }

        if (SUCCEEDED(hr))
        {
            *pcbWritten = sizeof(header) + cbFormat + sizeof(dataHeader);
        }
    }


    CoTaskMemFree(pWav);
    return hr;
}
```



<span data-ttu-id="96b78-210">La `WriteToFile` función es una función auxiliar simple que contiene la función **WriteFile** de Windows y devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="96b78-210">The `WriteToFile` function is a simple helper function that wraps the Windows **WriteFile** function and returns an **HRESULT** value.</span></span>


```C++
//-------------------------------------------------------------------
//
// Writes a block of data to a file
//
// hFile: Handle to the file.
// p: Pointer to the buffer to write.
// cb: Size of the buffer, in bytes.
//
//-------------------------------------------------------------------

HRESULT WriteToFile(HANDLE hFile, void* p, DWORD cb)
{
    DWORD cbWritten = 0;
    HRESULT hr = S_OK;

    BOOL bResult = WriteFile(hFile, p, cb, &cbWritten, NULL);
    if (!bResult)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



## <a name="calculate-the-maximum-data-size"></a><span data-ttu-id="96b78-211">Calcular el tamaño máximo de los datos</span><span class="sxs-lookup"><span data-stu-id="96b78-211">Calculate the Maximum Data Size</span></span>

<span data-ttu-id="96b78-212">Dado que el tamaño del archivo se almacena como un valor de 4 bytes en el encabezado del archivo, un archivo de onda se limita a un tamaño máximo de 0xFFFFFFFF bytes, aproximadamente 4 GB.</span><span class="sxs-lookup"><span data-stu-id="96b78-212">Because the file size is stored as a 4-byte value in the file header, a WAVE file is limited to a maximum size of 0xFFFFFFFF bytes—approximately 4 GB.</span></span> <span data-ttu-id="96b78-213">Este valor incluye el tamaño del encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="96b78-213">This value includes the size of the file header.</span></span> <span data-ttu-id="96b78-214">El audio PCM tiene una velocidad de bits constante, por lo que puede calcular el tamaño máximo de los datos a partir del formato de audio, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="96b78-214">PCM audio has a constant bit rate, so you can calculate the maximum data size from the audio format, as follows:</span></span>


```C++
//-------------------------------------------------------------------
// CalculateMaxAudioDataSize
//
// Calculates how much audio to write to the WAVE file, given the
// audio format and the maximum duration of the WAVE file.
//-------------------------------------------------------------------

DWORD CalculateMaxAudioDataSize(
    IMFMediaType *pAudioType,    // The PCM audio format.
    DWORD cbHeader,              // The size of the WAVE file header.
    DWORD msecAudioData          // Maximum duration, in milliseconds.
    )
{
    UINT32 cbBlockSize = 0;         // Audio frame size, in bytes.
    UINT32 cbBytesPerSecond = 0;    // Bytes per second.

    // Get the audio block size and number of bytes/second from the audio format.

    cbBlockSize = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_BLOCK_ALIGNMENT, 0);
    cbBytesPerSecond = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_AVG_BYTES_PER_SECOND, 0);

    // Calculate the maximum amount of audio data to write.
    // This value equals (duration in seconds x bytes/second), but cannot
    // exceed the maximum size of the data chunk in the WAVE file.

        // Size of the desired audio clip in bytes:
    DWORD cbAudioClipSize = (DWORD)MulDiv(cbBytesPerSecond, msecAudioData, 1000);

    // Largest possible size of the data chunk:
    DWORD cbMaxSize = MAXDWORD - cbHeader;

    // Maximum size altogether.
    cbAudioClipSize = min(cbAudioClipSize, cbMaxSize);

    // Round to the audio block size, so that we do not write a partial audio frame.
    cbAudioClipSize = (cbAudioClipSize / cbBlockSize) * cbBlockSize;

    return cbAudioClipSize;
}
```



<span data-ttu-id="96b78-215">Para evitar fotogramas de audio parciales, el tamaño se redondea a la alineación de bloque, que se almacena en el atributo de [**\_ alineación de bloque de \_ audio \_ \_ MF MT**](mf-mt-audio-block-alignment-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="96b78-215">To avoid partial audio frames, the size is rounded to the block alignment, which is stored in the [**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md) attribute.</span></span>

## <a name="decode-the-audio"></a><span data-ttu-id="96b78-216">Descodificación del audio</span><span class="sxs-lookup"><span data-stu-id="96b78-216">Decode the Audio</span></span>

<span data-ttu-id="96b78-217">La `WriteWaveData` función lee el audio descodificado del archivo de código fuente y escribe en el archivo de onda.</span><span class="sxs-lookup"><span data-stu-id="96b78-217">The `WriteWaveData` function reads decoded audio from the source file and writes to the WAVE file.</span></span>


```C++
//-------------------------------------------------------------------
// WriteWaveData
//
// Decodes PCM audio data from the source file and writes it to
// the WAVE file.
//-------------------------------------------------------------------

HRESULT WriteWaveData(
    HANDLE hFile,               // Output file.
    IMFSourceReader *pReader,   // Source reader.
    DWORD cbMaxAudioData,       // Maximum amount of audio data (bytes).
    DWORD *pcbDataWritten       // Receives the amount of data written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbAudioData = 0;
    DWORD cbBuffer = 0;
    BYTE *pAudioData = NULL;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Get audio samples from the source reader.
    while (true)
    {
        DWORD dwFlags = 0;

        // Read the next sample.
        hr = pReader->ReadSample(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            0, NULL, &dwFlags, NULL, &pSample );

        if (FAILED(hr)) { break; }

        if (dwFlags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            printf("Type change - not supported by WAVE file format.\n");
            break;
        }
        if (dwFlags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            printf("End of input file.\n");
            break;
        }

        if (pSample == NULL)
        {
            printf("No sample\n");
            continue;
        }

        // Get a pointer to the audio data in the sample.

        hr = pSample->ConvertToContiguousBuffer(&pBuffer);

        if (FAILED(hr)) { break; }


        hr = pBuffer->Lock(&pAudioData, NULL, &cbBuffer);

        if (FAILED(hr)) { break; }


        // Make sure not to exceed the specified maximum size.
        if (cbMaxAudioData - cbAudioData < cbBuffer)
        {
            cbBuffer = cbMaxAudioData - cbAudioData;
        }

        // Write this data to the output file.
        hr = WriteToFile(hFile, pAudioData, cbBuffer);

        if (FAILED(hr)) { break; }

        // Unlock the buffer.
        hr = pBuffer->Unlock();
        pAudioData = NULL;

        if (FAILED(hr)) { break; }

        // Update running total of audio data.
        cbAudioData += cbBuffer;

        if (cbAudioData >= cbMaxAudioData)
        {
            break;
        }

        SafeRelease(&pSample);
        SafeRelease(&pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        printf("Wrote %d bytes of audio data.\n", cbAudioData);

        *pcbDataWritten = cbAudioData;
    }

    if (pAudioData)
    {
        pBuffer->Unlock();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pSample);
    return hr;
}
```



<span data-ttu-id="96b78-218">La `WriteWaveData` función realiza lo siguiente en un bucle:</span><span class="sxs-lookup"><span data-stu-id="96b78-218">The `WriteWaveData` function does the following in a loop:</span></span>

1.  <span data-ttu-id="96b78-219">Llama a [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) para leer el audio del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="96b78-219">Calls [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) to read audio from the source file.</span></span> <span data-ttu-id="96b78-220">El parámetro *dwFlags* recibe **una operación OR bit a bit** de las marcas de la enumeración de [**\_ \_ \_ marca del lector de origen MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) .</span><span class="sxs-lookup"><span data-stu-id="96b78-220">The *dwFlags* parameter receives a bitwise **OR** of flags from the [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) enumeration.</span></span> <span data-ttu-id="96b78-221">El parámetro *pSample* recibe un puntero a la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , que se usa para tener acceso a los datos de audio.</span><span class="sxs-lookup"><span data-stu-id="96b78-221">The *pSample* parameter receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which is used to access the audio data.</span></span> <span data-ttu-id="96b78-222">En algunos casos, una llamada a **ReadSample** no genera datos, en cuyo caso el puntero **IMFSample** es **null**.</span><span class="sxs-lookup"><span data-stu-id="96b78-222">In some cases a call to **ReadSample** does not generate data, in which case the **IMFSample** pointer is **NULL**.</span></span>
2.  <span data-ttu-id="96b78-223">Comprueba *dwFlags* para las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="96b78-223">Checks *dwFlags* for the following flags:</span></span>
    -   <span data-ttu-id="96b78-224">**MF \_ SOURCE \_ READERF \_ CURRENTMEDIATYPECHANGED**.</span><span class="sxs-lookup"><span data-stu-id="96b78-224">**MF\_SOURCE\_READERF\_CURRENTMEDIATYPECHANGED**.</span></span> <span data-ttu-id="96b78-225">Esta marca indica un cambio de formato en el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="96b78-225">This flag indicates a format change in the source file.</span></span> <span data-ttu-id="96b78-226">Los archivos de onda no admiten los cambios de formato.</span><span class="sxs-lookup"><span data-stu-id="96b78-226">WAVE files do not support format changes.</span></span>
    -   <span data-ttu-id="96b78-227">**MF \_ SOURCE \_ READERF \_ ENDOFSTREAM**.</span><span class="sxs-lookup"><span data-stu-id="96b78-227">**MF\_SOURCE\_READERF\_ENDOFSTREAM**.</span></span> <span data-ttu-id="96b78-228">Esta marca indica el final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="96b78-228">This flag indicates the end of the stream.</span></span>
3.  <span data-ttu-id="96b78-229">Llama a [**IMFSample:: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) para obtener un puntero a un objeto de búfer.</span><span class="sxs-lookup"><span data-stu-id="96b78-229">Calls [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) to get a pointer to a buffer object.</span></span>
4.  <span data-ttu-id="96b78-230">Llama a [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obtener un puntero a la memoria del búfer.</span><span class="sxs-lookup"><span data-stu-id="96b78-230">Calls [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the buffer memory.</span></span>
5.  <span data-ttu-id="96b78-231">Escribe los datos de audio en el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="96b78-231">Writes the audio data to the output file.</span></span>
6.  <span data-ttu-id="96b78-232">Llama a [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear el objeto de búfer.</span><span class="sxs-lookup"><span data-stu-id="96b78-232">Calls [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer object.</span></span>

<span data-ttu-id="96b78-233">La función se interrumpe fuera del bucle cuando se produce cualquiera de los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="96b78-233">The function breaks out of the loop when any of the following occur:</span></span>

-   <span data-ttu-id="96b78-234">El formato del flujo cambia.</span><span class="sxs-lookup"><span data-stu-id="96b78-234">The stream format changes.</span></span>
-   <span data-ttu-id="96b78-235">Se llega al final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="96b78-235">The end of the stream is reached.</span></span>
-   <span data-ttu-id="96b78-236">La cantidad máxima de datos de audio se escribe en el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="96b78-236">The maximum amount of audio data is written to the output file.</span></span>
-   <span data-ttu-id="96b78-237">Se produce un error.</span><span class="sxs-lookup"><span data-stu-id="96b78-237">An error occurs.</span></span>

## <a name="finalize-the-file-header"></a><span data-ttu-id="96b78-238">Finalización del encabezado del archivo</span><span class="sxs-lookup"><span data-stu-id="96b78-238">Finalize the File Header</span></span>

<span data-ttu-id="96b78-239">Los valores de tamaño que se almacenan en el encabezado de onda no se conocen hasta que se completa la función anterior.</span><span class="sxs-lookup"><span data-stu-id="96b78-239">The size values that are stored in the WAVE header are not known until the previous function completes.</span></span> <span data-ttu-id="96b78-240">El `FixUpChunkSizes` rellenará estos valores:</span><span class="sxs-lookup"><span data-stu-id="96b78-240">The `FixUpChunkSizes` fills in these values:</span></span>


```C++
//-------------------------------------------------------------------
// FixUpChunkSizes
//
// Writes the file-size information into the WAVE file header.
//
// WAVE files use the RIFF file format. Each RIFF chunk has a data
// size, and the RIFF header has a total file size.
//-------------------------------------------------------------------

HRESULT FixUpChunkSizes(
    HANDLE hFile,           // Output file.
    DWORD cbHeader,         // Size of the 'fmt ' chuck.
    DWORD cbAudioData       // Size of the 'data' chunk.
    )
{
    HRESULT hr = S_OK;

    LARGE_INTEGER ll;
    ll.QuadPart = cbHeader - sizeof(DWORD);

    if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    // Write the data size.

    if (SUCCEEDED(hr))
    {
        hr = WriteToFile(hFile, &cbAudioData, sizeof(cbAudioData));
    }

    if (SUCCEEDED(hr))
    {
        // Write the file size.
        ll.QuadPart = sizeof(FOURCC);

        if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        DWORD cbRiffFileSize = cbHeader + cbAudioData - 8;

        // NOTE: The "size" field in the RIFF header does not include
        // the first 8 bytes of the file. (That is, the size of the
        // data that appears after the size field.)

        hr = WriteToFile(hFile, &cbRiffFileSize, sizeof(cbRiffFileSize));
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="96b78-241">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="96b78-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96b78-242">Tipos de medios de audio</span><span class="sxs-lookup"><span data-stu-id="96b78-242">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="96b78-243">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="96b78-243">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="96b78-244">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="96b78-244">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 
