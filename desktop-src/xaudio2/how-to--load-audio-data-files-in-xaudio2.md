---
description: En este tema se describen los pasos para rellenar las estructuras necesarias para reproducir datos de audio en XAudio2.
ms.assetid: caeb522e-d4f6-91e2-5e85-ea0af0f61300
title: 'Cómo: cargar archivos de datos de audio en XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bacf08e8f16e5cd9c42409776b02846990b9d66d685a0186314445742f23341
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962664"
---
# <a name="how-to-load-audio-data-files-in-xaudio2"></a>Cómo: cargar archivos de datos de audio en XAudio2

> [!Note]  
> Este contenido solo se aplica a las aplicaciones de escritorio y requerirá una revisión para funcionar en una Windows Store. Consulte la documentación de [**CreateFile2,**](/windows/win32/api/fileapi/nf-fileapi-createfile2) [**CreateEventEx,**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) [**WaitForSingleObjectEx,**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)y [**GetOverlappedResultEx.**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex) Consulte SoundFileReader.h/.cpp en el ejemplo basicSound Windows 8 de la galería de ejemplos Windows [SDK de .](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208))

 

En este tema se describen los pasos para rellenar las estructuras necesarias para reproducir datos de audio en XAudio2. En los pasos siguientes se cargan los fragmentos "fmt" y "data" de un archivo de audio, y se usan para rellenar una estructura **DE FORMADEDATOSTEXTENSIBLE** y una estructura [**BUFFER de XAUDIO2. \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)

-   [Preparación para analizar el archivo de audio.](#preparing-to-parse-the-audio-file)
-   [Rellenar estructuras XAudio2 con el contenido de fragmentos de RIFF.](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a>Preparación para analizar el archivo de audio

Los archivos de audio compatibles con XAudio2 usan el formato de archivo de intercambio de recursos (RIFF). RIFF se describe en la introducción al formato de archivo de intercambio de recursos [(RIFF).](resource-interchange-file-format--riff-.md) Los datos de audio de un archivo RIFF se cargan buscando el fragmento de RIFF y, a continuación, recorren el fragmento para buscar fragmentos individuales contenidos en el fragmento de RIFF. Las siguientes funciones son ejemplos de código para buscar fragmentos y cargar datos contenidos en los fragmentos.

-   Para buscar un fragmento en un archivo RIFF:

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

    

-   Para leer los datos de un fragmento una vez que se han ubicado.

    Una vez que se encuentra un fragmento deseado, sus datos se pueden leer ajustando el puntero de archivo al principio de la sección de datos del fragmento. Una función para leer los datos de un fragmento una vez que se encuentran podría tener este aspecto.

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

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a>Rellenar estructuras XAudio2 con el contenido de fragmentos de RIFF

Para que XAudio2 reprodgue audio con una voz de origen, necesita una estructura **DE FORMA DESATEX** y una estructura [**\_ BUFFER de XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) La **estructura DE FORMADEDATEX** puede ser una estructura mayor, como **ESTALAATEXTENSIBLE,** que contiene una estructura DE FORMA DEDATOS **COMO** su primer miembro. Para más información, consulte la página de referencia de **LAATEX.**

En este ejemplo se **usa UNA FORMADEDATEXTENSIBLE para** permitir la carga de archivos de audio PCM con más de dos canales.

En los pasos siguientes se ilustra el uso de las funciones descritas anteriormente para rellenar una estructura **DE FORMA DEDATOATEXTENSIBLE** y una [**estructura \_ BUFFER de XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) En este caso, el archivo de audio que se carga contiene datos de PCM y solo contendrá un fragmento "RIFF", "fmt" y "data". Otros formatos pueden contener tipos de fragmentos adicionales, como se describe en [Formato de archivo de intercambio de recursos (RIFF).](resource-interchange-file-format--riff-.md)

1.  Declare estructuras BUFFER DE LA CLASE DE ÁREA DE **TRABAJOATEXTENSIBLE** [**y XAUDIO2. \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  Abra el archivo de audio con CreateFile.
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

    

3.  Busque el fragmento "RIFF" en el archivo de audio y compruebe el tipo de archivo.
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

    

4.  Busque el fragmento 'fmt' y copie su contenido en una **estructura DE FORMAENTEXTENSIBLE.**
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  Busque el fragmento "data" y lea su contenido en un búfer.
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  Rellene una [**estructura \_ BUFFER de XAUDIO2.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> <dt>

[Cómo: reproducir un sonido con XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[Referencia de programación de XAudio2](programming-reference.md)
</dt> </dl>

 

 
