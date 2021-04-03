---
description: Al crear una voz de origen, puede pasarle una estructura que defina devoluciones de llamada para determinados eventos de audio. Puede utilizar estas devoluciones de llamada para realizar acciones o señalar otro código.
ms.assetid: 0bace0c5-9171-efd8-9a38-2c2b3452f73f
title: 'Cómo: usar devoluciones de llamadas de voces de origen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c10005ed838a22ea0dfce59312d6f293c213c39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810466"
---
# <a name="how-to-use-source-voice-callbacks"></a><span data-ttu-id="8c9ac-104">Cómo: usar devoluciones de llamadas de voces de origen</span><span class="sxs-lookup"><span data-stu-id="8c9ac-104">How to: Use Source Voice Callbacks</span></span>

<span data-ttu-id="8c9ac-105">Al crear una voz de origen, puede pasarle una estructura que defina devoluciones de llamada para determinados eventos de audio.</span><span class="sxs-lookup"><span data-stu-id="8c9ac-105">When you create a source voice, you can pass a structure to it that defines callbacks for certain audio events.</span></span> <span data-ttu-id="8c9ac-106">Puede utilizar estas devoluciones de llamada para realizar acciones o señalar otro código.</span><span class="sxs-lookup"><span data-stu-id="8c9ac-106">You can use these callbacks to perform actions or to signal other code.</span></span>

1.  <span data-ttu-id="8c9ac-107">Cree una clase que herede de la interfaz [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .</span><span class="sxs-lookup"><span data-stu-id="8c9ac-107">Create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span> <span data-ttu-id="8c9ac-108">Todas las funciones miembro de **IXAudio2VoiceCallback** son puramente virtuales y deben definirse.</span><span class="sxs-lookup"><span data-stu-id="8c9ac-108">All member functions of **IXAudio2VoiceCallback** are purely virtual, and must be defined.</span></span> <span data-ttu-id="8c9ac-109">La única función de interés en este ejemplo es [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend).</span><span class="sxs-lookup"><span data-stu-id="8c9ac-109">The only function of interest in this example is [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend).</span></span> <span data-ttu-id="8c9ac-110">Por lo tanto, el resto de las funciones son códigos auxiliares.</span><span class="sxs-lookup"><span data-stu-id="8c9ac-110">Therefore, the rest of the functions are stubs.</span></span> <span data-ttu-id="8c9ac-111">La función **OnStreamEnd** desencadena un evento que indica que el sonido ha terminado de reproducirse.</span><span class="sxs-lookup"><span data-stu-id="8c9ac-111">The **OnStreamEnd** function triggers an event that indicates the sound is done playing.</span></span>

    ```
    class VoiceCallback : public IXAudio2VoiceCallback
    {
    public:
        HANDLE hBufferEndEvent;
        VoiceCallback(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
        ~VoiceCallback(){ CloseHandle( hBufferEndEvent ); }

        //Called when the voice has just finished playing a contiguous audio stream.
        void OnStreamEnd() { SetEvent( hBufferEndEvent ); }

        //Unused methods are stubs
        void OnVoiceProcessingPassEnd() { }
        void OnVoiceProcessingPassStart(UINT32 SamplesRequired) {    }
        void OnBufferEnd(void * pBufferContext)    { }
        void OnBufferStart(void * pBufferContext) {    }
        void OnLoopEnd(void * pBufferContext) {    }
        void OnVoiceError(void * pBufferContext, HRESULT Error) { }
    };
    ```

    

2.  <span data-ttu-id="8c9ac-112">Cree una [**voz de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) con [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) mediante una instancia de la clase de devolución de llamada creada anteriormente como parámetro pCallback.</span><span class="sxs-lookup"><span data-stu-id="8c9ac-112">Create a [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) with [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) using an instance of the callback class created previously as the pCallback parameter.</span></span>

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  <span data-ttu-id="8c9ac-113">Después de iniciar la voz, use el método [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) para esperar a que se desencadene el evento.</span><span class="sxs-lookup"><span data-stu-id="8c9ac-113">After starting the voice, use the [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) method to wait for the event to be triggered.</span></span>

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="8c9ac-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c9ac-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c9ac-115">Devoluciones de llamada</span><span class="sxs-lookup"><span data-stu-id="8c9ac-115">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="8c9ac-116">Devoluciones de llamadas de XAudio2</span><span class="sxs-lookup"><span data-stu-id="8c9ac-116">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="8c9ac-117">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="8c9ac-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="8c9ac-118">Cómo: crear un gráfico de procesamiento de audio básico</span><span class="sxs-lookup"><span data-stu-id="8c9ac-118">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="8c9ac-119">Cómo: transmitir un sonido de un disco</span><span class="sxs-lookup"><span data-stu-id="8c9ac-119">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
