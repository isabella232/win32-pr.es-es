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
# <a name="how-to-use-source-voice-callbacks"></a>Cómo: usar devoluciones de llamadas de voces de origen

Al crear una voz de origen, puede pasarle una estructura que defina devoluciones de llamada para determinados eventos de audio. Puede utilizar estas devoluciones de llamada para realizar acciones o señalar otro código.

1.  Cree una clase que herede de la interfaz [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) . Todas las funciones miembro de **IXAudio2VoiceCallback** son puramente virtuales y deben definirse. La única función de interés en este ejemplo es [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend). Por lo tanto, el resto de las funciones son códigos auxiliares. La función **OnStreamEnd** desencadena un evento que indica que el sonido ha terminado de reproducirse.

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

    

2.  Cree una [**voz de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) con [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) mediante una instancia de la clase de devolución de llamada creada anteriormente como parámetro pCallback.

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  Después de iniciar la voz, use el método [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) para esperar a que se desencadene el evento.

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Devoluciones de llamada](callbacks.md)
</dt> <dt>

[Devoluciones de llamadas de XAudio2](xaudio2-callbacks.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Cómo: crear un gráfico de procesamiento de audio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Cómo: transmitir un sonido de un disco](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
