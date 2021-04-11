---
description: En este tema se describen los pasos necesarios para rellenar las estructuras necesarias para reproducir datos de audio en XAudio2.
ms.assetid: caeb522e-d4f6-91e2-5e85-ea0af0f61300
title: 'Cómo: cargar archivos de datos de audio en XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659b4d8e106b6f0b2eb942505f99562f56fdada7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154612"
---
# <a name="how-to-load-audio-data-files-in-xaudio2"></a><span data-ttu-id="34662-103">Cómo: cargar archivos de datos de audio en XAudio2</span><span class="sxs-lookup"><span data-stu-id="34662-103">How to: Load Audio Data Files in XAudio2</span></span>

> [!Note]  
> <span data-ttu-id="34662-104">Este contenido se aplica solo a las aplicaciones de escritorio y necesitará revisión para funcionar en una aplicación de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="34662-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="34662-105">Consulte la documentación de [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)y [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex).</span><span class="sxs-lookup"><span data-stu-id="34662-105">Please refer to the documentation for [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex).</span></span> <span data-ttu-id="34662-106">Vea SoundFileReader. h/. cpp en el ejemplo BasicSound de Windows 8 de la [Galería de ejemplos de Windows SDK](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).</span><span class="sxs-lookup"><span data-stu-id="34662-106">See SoundFileReader.h/.cpp in the BasicSound Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="34662-107">En este tema se describen los pasos necesarios para rellenar las estructuras necesarias para reproducir datos de audio en XAudio2.</span><span class="sxs-lookup"><span data-stu-id="34662-107">This topic describes the steps to populate the structures required to play audio data in XAudio2.</span></span> <span data-ttu-id="34662-108">En los pasos siguientes se cargan los fragmentos ' FMT ' y ' Data ' de un archivo de audio, y se usan para rellenar una estructura **WAVEFORMATEXTENSIBLE** y una estructura de [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="34662-108">The following steps load the 'fmt ' and 'data' chunks of an audio file, and uses them to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>

-   [<span data-ttu-id="34662-109">Preparando el análisis del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="34662-109">Preparing to parse the audio file.</span></span>](#preparing-to-parse-the-audio-file)
-   [<span data-ttu-id="34662-110">Rellenar estructuras de XAudio2 con el contenido de fragmentos RIFF.</span><span class="sxs-lookup"><span data-stu-id="34662-110">Populating XAudio2 structures with the contents of RIFF chunks.</span></span>](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a><span data-ttu-id="34662-111">Preparar el análisis del archivo de audio</span><span class="sxs-lookup"><span data-stu-id="34662-111">Preparing to parse the audio file</span></span>

<span data-ttu-id="34662-112">Los archivos de audio admitidos por XAudio2 usan el formato de archivo de intercambio de recursos (RIFF).</span><span class="sxs-lookup"><span data-stu-id="34662-112">Audio files supported by XAudio2 use the Resource Interchange File Format (RIFF).</span></span> <span data-ttu-id="34662-113">RIFF se describe en información general sobre el [formato de archivo de intercambio de recursos (Riff)](resource-interchange-file-format--riff-.md) .</span><span class="sxs-lookup"><span data-stu-id="34662-113">RIFF is described in the [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md) overview.</span></span> <span data-ttu-id="34662-114">Los datos de audio de un archivo RIFF se cargan buscando el fragmento RIFF y, a continuación, recorriendo en bucle el fragmento para buscar fragmentos individuales contenidos en el fragmento RIFF.</span><span class="sxs-lookup"><span data-stu-id="34662-114">Audio data in a RIFF file is loaded by finding the RIFF chunk and then looping through the chunk to find individual chunks contained in the RIFF chunk.</span></span> <span data-ttu-id="34662-115">Las siguientes funciones son ejemplos de código para buscar fragmentos y cargar datos contenidos en los fragmentos.</span><span class="sxs-lookup"><span data-stu-id="34662-115">The following functions are examples of code to find chunks and load data contained in the chunks.</span></span>

-   <span data-ttu-id="34662-116">Para buscar un fragmento en un archivo RIFF:</span><span class="sxs-lookup"><span data-stu-id="34662-116">To find a chunk in a RIFF file:</span></span>

    ```
    #ifdef _XBOX //Big-Endian
    #define fourccRIFF 'RIFF'
    #define fourccDATA 'data'
    #define fourccFMT 'fmt '
    #define fourccWAVE 'WAVE'
    #define fourccXWMA 'XWMA'
    #define fourccDPDS 'dpds'
    #endif

    #ifndef _XBOX //Little-Endian
    #define fourccRIFF 'FFIR'
    #define fourccDATA 'atad'
    #define fourccFMT ' tmf'
    #define fourccWAVE 'EVAW'
    #define fourccXWMA 'AMWX'
    #define fourccDPDS 'sdpd'
    #endif
    HRESULT FindChunk(HANDLE hFile, DWORD fourcc, DWORD & dwChunkSize, DWORD & dwChunkDataPosition)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );

        DWORD dwChunkType;
        DWORD dwChunkDataSize;
        DWORD dwRIFFDataSize = 0;
        DWORD dwFileType;
        DWORD bytesRead = 0;
        DWORD dwOffset = 0;

        while (hr == S_OK)
        {
            DWORD dwRead;
            if( 0 == ReadFile( hFile, &dwChunkType, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            if( 0 == ReadFile( hFile, &dwChunkDataSize, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            switch (dwChunkType)
            {
            case fourccRIFF:
                dwRIFFDataSize = dwChunkDataSize;
                dwChunkDataSize = 4;
                if( 0 == ReadFile( hFile, &dwFileType, sizeof(DWORD), &dwRead, NULL ) )
                    hr = HRESULT_FROM_WIN32( GetLastError() );
                break;

            default:
                if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, dwChunkDataSize, NULL, FILE_CURRENT ) )
                return HRESULT_FROM_WIN32( GetLastError() );            
            }

            dwOffset += sizeof(DWORD) * 2;
            
            if (dwChunkType == fourcc)
            {
                dwChunkSize = dwChunkDataSize;
                dwChunkDataPosition = dwOffset;
                return S_OK;
            }

            dwOffset += dwChunkDataSize;
            
            if (bytesRead >= dwRIFFDataSize) return S_FALSE;

        }

        return S_OK;
        
    }
    ```

    

-   <span data-ttu-id="34662-117">Para leer los datos de un fragmento una vez que se ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="34662-117">To read data in a chunk after it has been located.</span></span>

    <span data-ttu-id="34662-118">Una vez que se encuentra un fragmento deseado, sus datos se pueden leer ajustando el puntero de archivo al principio de la sección de datos del fragmento.</span><span class="sxs-lookup"><span data-stu-id="34662-118">Once a desired chunk is found, its data can be read by adjusting the file pointer to the beginning of the data section of the chunk.</span></span> <span data-ttu-id="34662-119">Una función para leer los datos de un fragmento una vez encontrado podría tener el aspecto siguiente.</span><span class="sxs-lookup"><span data-stu-id="34662-119">A function to read the data from a chunk once it is found might look like this.</span></span>

    ```
    HRESULT ReadChunkData(HANDLE hFile, void * buffer, DWORD buffersize, DWORD bufferoffset)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, bufferoffset, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );
        DWORD dwRead;
        if( 0 == ReadFile( hFile, buffer, buffersize, &dwRead, NULL ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
        return hr;
    }
    ```

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a><span data-ttu-id="34662-120">Rellenar estructuras de XAudio2 con el contenido de fragmentos RIFF</span><span class="sxs-lookup"><span data-stu-id="34662-120">Populating XAudio2 structures with the contents of RIFF chunks</span></span>

<span data-ttu-id="34662-121">Para que XAudio2 reproduzca audio con una voz de origen, necesita una estructura **WAVEFORMATEX** y una estructura [**de \_ búfer de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="34662-121">In order for XAudio2 to play audio with a source voice, it needs a **WAVEFORMATEX** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="34662-122">La estructura **WaveFormatEx** puede ser una estructura mayor, como **WAVEFORMATEXTENSIBLE** , que contiene una estructura **WAVEFORMATEX** como primer miembro.</span><span class="sxs-lookup"><span data-stu-id="34662-122">The **WAVEFORMATEX** structure may be a larger structure such as **WAVEFORMATEXTENSIBLE** that contains a **WAVEFORMATEX** structure as its first member.</span></span> <span data-ttu-id="34662-123">Vea la página de referencia de **WAVEFORMATEX** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="34662-123">See the **WAVEFORMATEX** reference page for more information.</span></span>

<span data-ttu-id="34662-124">En este ejemplo, se usa un **WAVEFORMATEXTENSIBLE** para permitir la carga de archivos de audio PCM con más de dos canales.</span><span class="sxs-lookup"><span data-stu-id="34662-124">In this example a **WAVEFORMATEXTENSIBLE** is being used to allow loading of PCM audio files with more than two channels.</span></span>

<span data-ttu-id="34662-125">En los pasos siguientes se muestra el uso de las funciones descritas anteriormente para rellenar una estructura **WAVEFORMATEXTENSIBLE** y una estructura de [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="34662-125">The following steps illustrate using the functions described above to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="34662-126">En este caso, el archivo de audio que se está cargando contiene datos PCM y solo contendrá un fragmento ' RIFF ', ' FMT ' y ' Data '.</span><span class="sxs-lookup"><span data-stu-id="34662-126">In this case, the audio file being loaded contains PCM data, and will only contain a 'RIFF', 'fmt ', and 'data' chunk.</span></span> <span data-ttu-id="34662-127">Otros formatos pueden contener tipos de fragmentos adicionales, tal como se describe en [formato de archivo de intercambio de recursos (Riff)](resource-interchange-file-format--riff-.md).</span><span class="sxs-lookup"><span data-stu-id="34662-127">Other formats may contain additional chunk types as described in [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md).</span></span>

1.  <span data-ttu-id="34662-128">Declare las estructuras de [**\_ búfer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **WAVEFORMATEXTENSIBLE** y XAUDIO2.</span><span class="sxs-lookup"><span data-stu-id="34662-128">Declare **WAVEFORMATEXTENSIBLE** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structures.</span></span>
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  <span data-ttu-id="34662-129">Abra el archivo de audio con CreateFile.</span><span class="sxs-lookup"><span data-stu-id="34662-129">Open the audio file with CreateFile.</span></span>
    ```
    #ifdef _XBOX
    char * strFileName = "game:\\media\\MusicMono.wav";
    #else
    TCHAR * strFileName = _TEXT("media\\MusicMono.wav");
    #endif
    // Open the file
    HANDLE hFile = CreateFile(
        strFileName,
        GENERIC_READ,
        FILE_SHARE_READ,
        NULL,
        OPEN_EXISTING,
        0,
        NULL );

    if( INVALID_HANDLE_VALUE == hFile )
        return HRESULT_FROM_WIN32( GetLastError() );

    if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
        return HRESULT_FROM_WIN32( GetLastError() );
    ```

    

3.  <span data-ttu-id="34662-130">Busque el fragmento "RIFF" en el archivo de audio y compruebe el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="34662-130">Locate the 'RIFF' chunk in the audio file, and check the file type.</span></span>
    ```
    DWORD dwChunkSize;
    DWORD dwChunkPosition;
    //check the file type, should be fourccWAVE or 'XWMA'
    FindChunk(hFile,fourccRIFF,dwChunkSize, dwChunkPosition );
    DWORD filetype;
    ReadChunkData(hFile,&filetype,sizeof(DWORD),dwChunkPosition);
    if (filetype != fourccWAVE)
        return S_FALSE;
    ```

    

4.  <span data-ttu-id="34662-131">Busque el fragmento de "FMT" y copie su contenido en una estructura **WAVEFORMATEXTENSIBLE** .</span><span class="sxs-lookup"><span data-stu-id="34662-131">Locate the 'fmt ' chunk, and copy its contents into a **WAVEFORMATEXTENSIBLE** structure.</span></span>
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  <span data-ttu-id="34662-132">Busque el fragmento ' Data ' y lea su contenido en un búfer.</span><span class="sxs-lookup"><span data-stu-id="34662-132">Locate the 'data' chunk, and read its contents into a buffer.</span></span>
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  <span data-ttu-id="34662-133">Rellene una estructura de [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .</span><span class="sxs-lookup"><span data-stu-id="34662-133">Populate an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a><span data-ttu-id="34662-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34662-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34662-135">Introducción</span><span class="sxs-lookup"><span data-stu-id="34662-135">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="34662-136">Cómo: reproducir un sonido con XAudio2</span><span class="sxs-lookup"><span data-stu-id="34662-136">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="34662-137">Referencia de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="34662-137">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
