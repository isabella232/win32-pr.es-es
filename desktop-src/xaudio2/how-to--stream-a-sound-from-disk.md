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
# <a name="how-to-stream-a-sound-from-disk"></a><span data-ttu-id="39662-103">Cómo: transmitir un sonido de un disco</span><span class="sxs-lookup"><span data-stu-id="39662-103">How to: Stream a Sound from Disk</span></span>

> [!Note]  
> <span data-ttu-id="39662-104">Este contenido se aplica solo a las aplicaciones de escritorio y necesitará revisión para funcionar en una aplicación de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="39662-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="39662-105">Consulte la documentación de **CreateFile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)y **GetOverlappedResultEx**.</span><span class="sxs-lookup"><span data-stu-id="39662-105">Please refer to the documentation for **CreateFile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and **GetOverlappedResultEx**.</span></span> <span data-ttu-id="39662-106">Vea el ejemplo de Windows 8 de StreamEffect en la [Galería de ejemplos de Windows SDK](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).</span><span class="sxs-lookup"><span data-stu-id="39662-106">See the StreamEffect Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="39662-107">Puede transmitir datos de audio en XAudio2 mediante la creación de un subproceso independiente y realizar lecturas de búfer de los datos de audio en el subproceso de streaming y, a continuación, usar las devoluciones de llamada para controlar ese subproceso.</span><span class="sxs-lookup"><span data-stu-id="39662-107">You can stream audio data in XAudio2 by creating a separate thread and perform buffer reads of the audio data in the streaming thread, and then use callbacks to control that thread.</span></span>

-   [<span data-ttu-id="39662-108">Realizar lecturas de búfer en el subproceso de streaming</span><span class="sxs-lookup"><span data-stu-id="39662-108">Performing buffer reads in the streaming thread</span></span>](#performing-buffer-reads-in-the-streaming-thread)
-   [<span data-ttu-id="39662-109">Crear la clase de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="39662-109">Creating the callback class</span></span>](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a><span data-ttu-id="39662-110">Realizar lecturas de búfer en el subproceso de streaming</span><span class="sxs-lookup"><span data-stu-id="39662-110">Performing buffer reads in the streaming thread</span></span>

<span data-ttu-id="39662-111">Para realizar lecturas de búfer en el subproceso de streaming, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="39662-111">To perform buffer reads in the streaming thread follow these steps:</span></span>

1.  <span data-ttu-id="39662-112">Cree una matriz de búferes de lectura.</span><span class="sxs-lookup"><span data-stu-id="39662-112">Create an array of read buffers.</span></span>

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  <span data-ttu-id="39662-113">Inicializar una estructura superpuesta.</span><span class="sxs-lookup"><span data-stu-id="39662-113">Initialize an OVERLAPPED structure.</span></span>

    <span data-ttu-id="39662-114">La estructura se usa para comprobar cuándo ha finalizado una lectura de disco asincrónica.</span><span class="sxs-lookup"><span data-stu-id="39662-114">The structure is used to check when an asynchronous disk read has finished.</span></span>

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  <span data-ttu-id="39662-115">Llame a la función de [**Inicio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) en la [**voz de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) que reproducirá el audio de streaming.</span><span class="sxs-lookup"><span data-stu-id="39662-115">Call the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) that will be playing the streaming audio.</span></span>

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  <span data-ttu-id="39662-116">Bucle mientras la posición de lectura actual no se pasa al final del archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="39662-116">Loop while the current read position is not passed the end of the audio file.</span></span>

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    <span data-ttu-id="39662-117">En el bucle, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="39662-117">In the loop, do the following:</span></span>

    1.  <span data-ttu-id="39662-118">Leer un fragmento de datos del disco en el búfer de lectura actual.</span><span class="sxs-lookup"><span data-stu-id="39662-118">Read a chunk of data from the disk into the current read buffer.</span></span>

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

        

    2.  <span data-ttu-id="39662-119">Utilice la función **GetOverlappedResult** para esperar a que el evento que indica que la lectura ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="39662-119">Use the **GetOverlappedResult** function to wait for the event that signals the read has finished.</span></span>

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  <span data-ttu-id="39662-120">Espere a que el número de búferes en cola en la [**voz de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) sea menor que el número de búferes de lectura.</span><span class="sxs-lookup"><span data-stu-id="39662-120">Wait for the number of buffers queued on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) to be less than the number of read buffers.</span></span>

        <span data-ttu-id="39662-121">El estado de la [**voz de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) se comprueba con la función [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) .</span><span class="sxs-lookup"><span data-stu-id="39662-121">The state of the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) is checked with the [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) function.</span></span>

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  <span data-ttu-id="39662-122">Envíe el búfer de lectura actual a la [**voz de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) mediante la función [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) .</span><span class="sxs-lookup"><span data-stu-id="39662-122">Submit the current read buffer to the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) using the [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) function.</span></span>

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

        

    5.  <span data-ttu-id="39662-123">Establezca el índice del búfer de lectura actual en el siguiente búfer.</span><span class="sxs-lookup"><span data-stu-id="39662-123">Set the current read buffer index to the next buffer.</span></span>

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  <span data-ttu-id="39662-124">Una vez finalizado el bucle, espere a que finalice la reproducción de los búferes en cola restantes.</span><span class="sxs-lookup"><span data-stu-id="39662-124">After the loop has finished, wait for the remaining queued buffers to finish playing.</span></span>

    <span data-ttu-id="39662-125">Cuando los búferes restantes han terminado de reproducirse, el sonido se detiene y el subproceso puede salir o reutilizarse para transmitir otro sonido.</span><span class="sxs-lookup"><span data-stu-id="39662-125">When the remaining buffers have finished playing, the sound stops, and the thread can exit or be reused to stream another sound.</span></span>

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a><span data-ttu-id="39662-126">Crear la clase de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="39662-126">Creating the callback class</span></span>

<span data-ttu-id="39662-127">Para crear la clase de devolución de llamada, cree una clase que herede de la interfaz [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .</span><span class="sxs-lookup"><span data-stu-id="39662-127">To create the callback class, create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span>

<span data-ttu-id="39662-128">La clase debe establecer un evento en su método [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) .</span><span class="sxs-lookup"><span data-stu-id="39662-128">The class should set an event in its [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) method.</span></span> <span data-ttu-id="39662-129">Esto permite que el subproceso de streaming se ponga en suspensión hasta que el evento señale que XAudio2 ha terminado de leer desde un búfer de audio.</span><span class="sxs-lookup"><span data-stu-id="39662-129">This allows the streaming thread to put itself to sleep until the event signals it that XAudio2 has finished reading from an audio buffer.</span></span> <span data-ttu-id="39662-130">Para obtener más información sobre el uso de devoluciones de llamada con XAudio2, consulte [Cómo: usar devoluciones de llamada de voz de origen](how-to--use-source-voice-callbacks.md).</span><span class="sxs-lookup"><span data-stu-id="39662-130">For more information about using callbacks with XAudio2, see [How to: Use Source Voice Callbacks](how-to--use-source-voice-callbacks.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="39662-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="39662-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39662-132">Transmisión de datos de audio</span><span class="sxs-lookup"><span data-stu-id="39662-132">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="39662-133">Devoluciones de llamadas de XAudio2</span><span class="sxs-lookup"><span data-stu-id="39662-133">XAudio2 Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="39662-134">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="39662-134">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="39662-135">Cómo: crear un gráfico de procesamiento de audio básico</span><span class="sxs-lookup"><span data-stu-id="39662-135">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="39662-136">Cómo: usar devoluciones de llamadas de voces de origen</span><span class="sxs-lookup"><span data-stu-id="39662-136">How to: Use Source Voice Callbacks</span></span>](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 
