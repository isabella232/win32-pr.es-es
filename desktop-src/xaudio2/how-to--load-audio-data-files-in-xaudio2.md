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
# <a name="how-to-load-audio-data-files-in-xaudio2"></a>Cómo: cargar archivos de datos de audio en XAudio2

> [!Note]  
> Este contenido se aplica solo a las aplicaciones de escritorio y necesitará revisión para funcionar en una aplicación de la tienda Windows. Consulte la documentación de [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)y [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex). Vea SoundFileReader. h/. cpp en el ejemplo BasicSound de Windows 8 de la [Galería de ejemplos de Windows SDK](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).

 

En este tema se describen los pasos necesarios para rellenar las estructuras necesarias para reproducir datos de audio en XAudio2. En los pasos siguientes se cargan los fragmentos ' FMT ' y ' Data ' de un archivo de audio, y se usan para rellenar una estructura **WAVEFORMATEXTENSIBLE** y una estructura de [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .

-   [Preparando el análisis del archivo de audio.](#preparing-to-parse-the-audio-file)
-   [Rellenar estructuras de XAudio2 con el contenido de fragmentos RIFF.](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a>Preparar el análisis del archivo de audio

Los archivos de audio admitidos por XAudio2 usan el formato de archivo de intercambio de recursos (RIFF). RIFF se describe en información general sobre el [formato de archivo de intercambio de recursos (Riff)](resource-interchange-file-format--riff-.md) . Los datos de audio de un archivo RIFF se cargan buscando el fragmento RIFF y, a continuación, recorriendo en bucle el fragmento para buscar fragmentos individuales contenidos en el fragmento RIFF. Las siguientes funciones son ejemplos de código para buscar fragmentos y cargar datos contenidos en los fragmentos.

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

    

-   Para leer los datos de un fragmento una vez que se ha encontrado.

    Una vez que se encuentra un fragmento deseado, sus datos se pueden leer ajustando el puntero de archivo al principio de la sección de datos del fragmento. Una función para leer los datos de un fragmento una vez encontrado podría tener el aspecto siguiente.

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

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a>Rellenar estructuras de XAudio2 con el contenido de fragmentos RIFF

Para que XAudio2 reproduzca audio con una voz de origen, necesita una estructura **WAVEFORMATEX** y una estructura [**de \_ búfer de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . La estructura **WaveFormatEx** puede ser una estructura mayor, como **WAVEFORMATEXTENSIBLE** , que contiene una estructura **WAVEFORMATEX** como primer miembro. Vea la página de referencia de **WAVEFORMATEX** para obtener más información.

En este ejemplo, se usa un **WAVEFORMATEXTENSIBLE** para permitir la carga de archivos de audio PCM con más de dos canales.

En los pasos siguientes se muestra el uso de las funciones descritas anteriormente para rellenar una estructura **WAVEFORMATEXTENSIBLE** y una estructura de [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) . En este caso, el archivo de audio que se está cargando contiene datos PCM y solo contendrá un fragmento ' RIFF ', ' FMT ' y ' Data '. Otros formatos pueden contener tipos de fragmentos adicionales, tal como se describe en [formato de archivo de intercambio de recursos (Riff)](resource-interchange-file-format--riff-.md).

1.  Declare las estructuras de [**\_ búfer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **WAVEFORMATEXTENSIBLE** y XAUDIO2.
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

    

4.  Busque el fragmento de "FMT" y copie su contenido en una estructura **WAVEFORMATEXTENSIBLE** .
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  Busque el fragmento ' Data ' y lea su contenido en un búfer.
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  Rellene una estructura de [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) .
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

 

 
