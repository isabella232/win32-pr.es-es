---
description: En este tutorial se muestra cómo usar el Lector de origen para descodificar audio de un archivo multimedia y escribir el audio en un archivo WAVE.
ms.assetid: ed40e201-c6ed-444f-bdaa-a5f33d1cc068
title: 'Tutorial: Decoding Audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eb6d9f48419b62fa1c379c636abaf2bb0a63a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361110"
---
# <a name="tutorial-decoding-audio"></a>Tutorial: Decoding Audio

En este tutorial se muestra cómo usar el Lector de [origen](source-reader.md) para descodificar audio de un archivo multimedia y escribir el audio en un archivo WAVE. El tutorial se basa en el ejemplo [audio clip.](audio-clip-sample.md)

-   [Información general](#overview)
-   [Archivos de encabezado y biblioteca](#header-and-library-files)
-   [Implementación de wmain](#implement-wmain)
-   [Escribir el archivo WAVE](#write-the-wave-file)
-   [Configuración del lector de origen](#configure-the-source-reader)
-   [Escribir el encabezado de archivo WAVE](#write-the-wave-file-header)
-   [Calcular el tamaño máximo de los datos](#calculate-the-maximum-data-size)
-   [Descodificación del audio](#decode-the-audio)
-   [Finalizar el encabezado de archivo](#finalize-the-file-header)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

En este tutorial, creará una aplicación de consola que toma dos argumentos de línea de comandos: el nombre de un archivo de entrada que contiene una secuencia de audio y el nombre del archivo de salida. La aplicación lee cinco segundos de datos de audio del archivo de entrada y escribe el audio en el archivo de salida como datos WAVE.

Para obtener los datos de audio descodificados, la aplicación usa el objeto de lector de origen. El lector de origen expone la [**interfaz IMFSourceReader.**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) Para escribir el audio descodificado en el archivo WAVE, las aplicaciones usan Windows de E/S. En la imagen siguiente se muestra este proceso.

![diagrama que muestra el lector de origen que obtenía datos de audio del archivo de origen.](images/audio-clip-tutorial.gif)

En su forma más sencilla, un archivo WAVE tiene la siguiente estructura:



| Tipo de datos                              | Tamaño (bytes) | Value                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| **FOURCC**                             | 4            | 'RIFF'                                                                |
| **DWORD**                              | 4            | Tamaño total del archivo, sin incluir los primeros 8 bytes                      |
| **FOURCC**                             | 4            | 'WAVE'                                                                |
| **FOURCC**                             | 4            | 'fmt'                                                                |
| **DWORD**                              | 4            | Tamaño de los [**datos DE FORMA DEDATOS**](/previous-versions/dd757713(v=vs.85)) que se muestra a continuación. |
| [**FORMA DE ONDAATEX**](/previous-versions/dd757713(v=vs.85)) | Varía       | Encabezado de formato de audio.                                                  |
| **FOURCC**                             | 4            | 'data'                                                                |
| **DWORD**                              | 4            | Tamaño de los datos de audio.                                               |
| **BYTE**\[\]                           | Varía       | Datos de audio.                                                           |



 

> [!Note]  
> Un **FOURCC** es un **DWORD** formado por la concatenación de cuatro caracteres ASCII.

 

Esta estructura básica se puede ampliar agregando metadatos de archivo y otra información, que está fuera del ámbito de este tutorial.

## <a name="header-and-library-files"></a>Archivos de encabezado y biblioteca

Incluya los siguientes archivos de encabezado en el proyecto:


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



Vínculo a las bibliotecas siguientes:

-   mfplat.lib
-   mfreadwrite.lib
-   mfuuid.lib

## <a name="implement-wmain"></a>Implementación de wmain

El código siguiente muestra la función de punto de entrada para la aplicación.


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



Esta función hace lo siguiente:

1.  Llama [**a CoInitializeEx para**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) inicializar la biblioteca COM.
2.  Llama [**a MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar Media Foundation plataforma.
3.  Llama [**a MFCreateSourceReaderFromURL para**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) crear el lector de origen. Esta función toma el nombre del archivo de entrada y recibe un puntero de [**interfaz DEFUTSourceReader.**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
4.  Crea el archivo de salida llamando a la **función CreateFile,** que devuelve un identificador de archivo.
5.  Llama a la función [WriteWavFile definida por la](#write-the-wave-file) aplicación. Esta función descodifica el audio y escribe el archivo WAVE.
6.  Libera el puntero [**DE ALSOURCESourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) y el identificador de archivo.
7.  Llama [**a MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para apagar Media Foundation plataforma.
8.  Llama [**a CoUninitialize para**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) liberar la biblioteca COM.

## <a name="write-the-wave-file"></a>Escribir el archivo WAVE

La mayor parte del trabajo se produce en `WriteWavFile` la función , a la que se llama desde `wmain` .


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



Esta función llama a una serie de otras funciones definidas por la aplicación:

1.  La [función ConfigureAudioStream](#configure-the-source-reader) inicializa el lector de origen. Esta función recibe un puntero a la interfaz [**IMFMediaType,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que se usa para obtener una descripción del formato de audio descodificado, incluida la frecuencia de muestreo, el número de canales y la profundidad de bits (bits por muestra).
2.  La función WriteWaveHeader escribe la primera parte del archivo WAVE, incluidos el encabezado y el inicio del fragmento "data".
3.  La función CalculateMaxAudioDataSize calcula la cantidad máxima de audio que se escribirá en el archivo, en bytes.
4.  La función WriteWaveData escribe los datos de audio de PCM en el archivo.
5.  La función FixUpChunkSizes escribe la información de tamaño de archivo que aparece después de los valores **FOURCC** "RIFF" y "data" en el archivo WAVE. (Estos valores no se conocen hasta `WriteWaveData` que se completa).

Estas funciones se muestran en las secciones restantes de este tutorial.

## <a name="configure-the-source-reader"></a>Configuración del lector de origen

La `ConfigureAudioStream` función configura el lector de origen para descodificar la secuencia de audio en el archivo de origen. También devuelve información sobre el formato del audio descodificado.

En Media Foundation, los formatos multimedia se describen mediante *objetos de tipo multimedia.* Un objeto de tipo multimedia expone la [**interfaz IMFMediaType,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que hereda la [**interfazATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Básicamente, un tipo de medio es una colección de propiedades que describen el formato. Para obtener más información, vea [Tipos de medios](media-types.md).


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



La `ConfigureAudioStream` función hace lo siguiente:

1.  Llama al [**método IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) para seleccionar la secuencia de audio y anular la selección de todas las demás secuencias. Este paso puede mejorar el rendimiento, ya que impide que el lector de origen se alote en fotogramas de vídeo que la aplicación no usa.
2.  Crea un *tipo de* medio parcial que especifica audio PCM. La función crea el tipo parcial de la siguiente manera:
    1.  Llama [**a MFCreateMediaType para**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) crear un objeto de tipo multimedia vacío.
    2.  Establece el [**atributo MF MT MAJOR \_ \_ \_ TYPE**](mf-mt-major-type-attribute.md) en **MFMediaType \_ Audio**.
    3.  Establece el [**atributo MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md) en **MFAudioFormat \_ PCM.**
3.  Llama [**a IMFSourceReader::SetCurrentMediaType para**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) establecer el tipo parcial en el lector de origen. Si el archivo de origen contiene audio codificado, el lector de origen carga automáticamente el descodificador de audio necesario.
4.  Llama [**a IMFSourceReader::GetCurrentMediaType para**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) obtener el tipo de medio PCM real. Este método devuelve un tipo de medio con todos los detalles de formato rellenados, como la frecuencia de muestreo de audio y el número de canales.
5.  Llama [**a IMFSourceReader::SetStreamSelection para**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) habilitar la secuencia de audio.

## <a name="write-the-wave-file-header"></a>Escribir el encabezado de archivo WAVE

La `WriteWaveHeader` función escribe el encabezado de archivo WAVE.

La única API Media Foundation a la que se llama desde esta función [**es MFCreateWaveFormatExFromMFMediaType,**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)que convierte el tipo de medio en una [**estructuraWAVEATEX.**](/previous-versions/dd757713(v=vs.85))


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



La función es una función auxiliar sencilla que encapsula la Windows `WriteToFile` **WriteFile** y devuelve un **valor HRESULT.**


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



## <a name="calculate-the-maximum-data-size"></a>Calcular el tamaño máximo de los datos

Dado que el tamaño del archivo se almacena como un valor de 4 bytes en el encabezado de archivo, un archivo WAVE se limita a un tamaño máximo de 0xFFFFFFFF bytes, aproximadamente 4 GB. Este valor incluye el tamaño del encabezado de archivo. El audio PCM tiene una velocidad de bits constante, por lo que puede calcular el tamaño máximo de los datos a partir del formato de audio, como se muestra a continuación:


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



Para evitar fotogramas de audio parciales, el tamaño se redondea a la alineación del bloque, que se almacena en el atributo [**MF MT AUDIO BLOCK \_ \_ \_ \_ ALIGNMENT.**](mf-mt-audio-block-alignment-attribute.md)

## <a name="decode-the-audio"></a>Descodificación del audio

La `WriteWaveData` función lee el audio descodificado del archivo de origen y escribe en el archivo WAVE.


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



La `WriteWaveData` función hace lo siguiente en un bucle:

1.  Llama [**a IMFSourceReader::ReadSample para**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) leer audio del archivo de origen. El *parámetro dwFlags* recibe un **OR** bit a bit de marcas de la [**enumeración MF SOURCE READER \_ \_ \_ FLAG.**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) El *parámetro pSample* recibe un puntero a la [**interfaz IMFSample,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) que se usa para tener acceso a los datos de audio. En algunos casos, una llamada a **ReadSample** no genera datos, en cuyo caso el puntero **DESAMPLESample** es **NULL.**
2.  Comprueba *dwFlags para* las marcas siguientes:
    -   **MF \_ SOURCE \_ READERF \_ CURRENTMEDIATYPECHANGED**. Esta marca indica un cambio de formato en el archivo de origen. Los archivos WAVE no admiten cambios de formato.
    -   **MF \_ SOURCE \_ READERF \_ ENDOFSTREAM**. Esta marca indica el final de la secuencia.
3.  Llama [**a IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) para obtener un puntero a un objeto de búfer.
4.  Llama [**a IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obtener un puntero a la memoria del búfer.
5.  Escribe los datos de audio en el archivo de salida.
6.  Llama [**a IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear el objeto de búfer.

La función se interrumpe del bucle cuando se produce alguna de las siguientes situaciones:

-   El formato de la secuencia cambia.
-   Se llega al final de la secuencia.
-   La cantidad máxima de datos de audio se escribe en el archivo de salida.
-   Se produce un error.

## <a name="finalize-the-file-header"></a>Finalizar el encabezado de archivo

Los valores de tamaño que se almacenan en el encabezado WAVE no se conocen hasta que se completa la función anterior. rellena `FixUpChunkSizes` estos valores:


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios de audio](audio-media-types.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 
