---
description: Puede transmitir datos de audio en XAudio2 mediante la creación de un subproceso independiente y realizar lecturas de búfer de los datos de audio en el subproceso de streaming y, a continuación, usar las devoluciones de llamada para controlar ese subproceso.
ms.assetid: 48b80a66-91c1-973f-069b-6f63422d7154
title: 'Cómo: transmitir un sonido de un disco'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c5598e8913514d6b0bf81b55bab5b481dbc43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815275"
---
# <a name="how-to-stream-a-sound-from-disk"></a>Cómo: transmitir un sonido de un disco

> [!Note]  
> Este contenido se aplica solo a las aplicaciones de escritorio y necesitará revisión para funcionar en una aplicación de la tienda Windows. Consulte la documentación de **CreateFile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)y **GetOverlappedResultEx**. Vea el ejemplo de Windows 8 de StreamEffect en la [Galería de ejemplos de Windows SDK](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).

 

Puede transmitir datos de audio en XAudio2 mediante la creación de un subproceso independiente y realizar lecturas de búfer de los datos de audio en el subproceso de streaming y, a continuación, usar las devoluciones de llamada para controlar ese subproceso.

-   [Realizar lecturas de búfer en el subproceso de streaming](#performing-buffer-reads-in-the-streaming-thread)
-   [Crear la clase de devolución de llamada](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a>Realizar lecturas de búfer en el subproceso de streaming

Para realizar lecturas de búfer en el subproceso de streaming, siga estos pasos:

1.  Cree una matriz de búferes de lectura.

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  Inicializar una estructura superpuesta.

    La estructura se usa para comprobar cuándo ha finalizado una lectura de disco asincrónica.

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  Llame a la función de [**Inicio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) en la [**voz de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) que reproducirá el audio de streaming.

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  Bucle mientras la posición de lectura actual no se pasa al final del archivo de audio.

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    En el bucle, haga lo siguiente:

    1.  Leer un fragmento de datos del disco en el búfer de lectura actual.

        ```
        DWORD dwRead;
        if( SUCCEEDED(hr) && 0 == ReadFile( hFile, pData, dwDataSize, &dwRead, pOverlapped ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
            DWORD cbValid = min( STREAMING_BUFFER_SIZE, cbWaveSize - CurrentPosition );
            DWORD dwRead;
            if( 0 == ReadFile( hFile, buffers[CurrentDiskReadBuffer], STREAMING_BUFFER_SIZE, &dwRead, &Overlapped ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );
            Overlapped.Offset += cbValid;

            //update the file position to where it will be once the read finishes
            CurrentPosition += cbValid;
        ```

        

    2.  Utilice la función **GetOverlappedResult** para esperar a que el evento que indica que la lectura ha finalizado.

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  Espere a que el número de búferes en cola en la [**voz de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) sea menor que el número de búferes de lectura.

        El estado de la [**voz de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) se comprueba con la función [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) .

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  Envíe el búfer de lectura actual a la [**voz de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) mediante la función [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) .

        ```
        XAUDIO2_BUFFER buf = {0};
        buf.AudioBytes = cbValid;
        buf.pAudioData = buffers[CurrentDiskReadBuffer];
        if( CurrentPosition >= cbWaveSize )
        {
            buf.Flags = XAUDIO2_END_OF_STREAM;
        }
        pSourceVoice->SubmitSourceBuffer( &buf );
        ```

        

    5.  Establezca el índice del búfer de lectura actual en el siguiente búfer.

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  Una vez finalizado el bucle, espere a que finalice la reproducción de los búferes en cola restantes.

    Cuando los búferes restantes han terminado de reproducirse, el sonido se detiene y el subproceso puede salir o reutilizarse para transmitir otro sonido.

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a>Crear la clase de devolución de llamada

Para crear la clase de devolución de llamada, cree una clase que herede de la interfaz [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .

La clase debe establecer un evento en su método [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) . Esto permite que el subproceso de streaming se ponga en suspensión hasta que el evento señale que XAudio2 ha terminado de leer desde un búfer de audio. Para obtener más información sobre el uso de devoluciones de llamada con XAudio2, consulte [Cómo: usar devoluciones de llamada de voz de origen](how-to--use-source-voice-callbacks.md).


```
struct StreamingVoiceContext : public IXAudio2VoiceCallback
{
    HANDLE hBufferEndEvent;
    StreamingVoiceContext(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
    ~StreamingVoiceContext(){ CloseHandle( hBufferEndEvent ); }
    void OnBufferEnd( void* ){ SetEvent( hBufferEndEvent ); }
    ...
};
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transmisión de datos de audio](streaming-audio-data.md)
</dt> <dt>

[Devoluciones de llamadas de XAudio2](callbacks.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: crear un gráfico de procesamiento de audio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Cómo: usar devoluciones de llamadas de voces de origen](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 
