---
description: Representar una secuencia
ms.assetid: 00bfcfd1-6592-43e3-90ad-730c92aa4cd3
title: Representar una secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d96e720bab43c75b0a3958bb3b6137d3a3d9ef6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496361"
---
# <a name="rendering-a-stream"></a>Representar una secuencia

El cliente llama a los métodos de la interfaz [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) para escribir los datos de representación en un búfer de extremo. En el caso de una secuencia en modo compartido, el cliente comparte el búfer del extremo con el motor de audio. En el caso de una secuencia en modo exclusivo, el cliente comparte el búfer del extremo con el dispositivo de audio. Para solicitar un búfer de punto de conexión de un tamaño determinado, el cliente llama al método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . Para obtener el tamaño del búfer asignado, que puede ser diferente del tamaño solicitado, el cliente llama al método [**IAudioClient:: GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .

Para trasladar un flujo de datos de representación a través del búfer del extremo, el cliente llama como método [**IAudioRenderClient:: getBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) y el método [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) . El cliente tiene acceso a los datos del búfer del extremo como una serie de paquetes de datos. La llamada **getBuffer** recupera el siguiente paquete para que el cliente pueda rellenarlo con datos de representación. Después de escribir los datos en el paquete, el cliente llama a **ReleaseBuffer** para agregar el paquete completado a la cola de representación.

En el caso de un búfer de representación, el valor de relleno que indica el método [**IAudioClient:: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) representa la cantidad de datos de representación que se ponen en cola para reproducirse en el búfer. Una aplicación de representación puede utilizar el valor de relleno para determinar cuántos datos nuevos puede escribir de forma segura en el búfer sin el riesgo de sobrescribir los datos escritos previamente que el motor de audio todavía no ha leído del búfer. El espacio disponible es simplemente el tamaño del búfer menos el tamaño del relleno. El cliente puede solicitar un tamaño de paquete que represente parte o todo este espacio disponible en su siguiente llamada a [**getBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) .

El tamaño de un paquete se expresa en *fotogramas de audio*. Una trama de audio en un flujo PCM es un conjunto de ejemplos (el conjunto contiene un ejemplo para cada canal de la secuencia) que se reproducen o se graban al mismo tiempo (reloj). Por lo tanto, el tamaño de un fotograma de audio es el tamaño de ejemplo multiplicado por el número de canales de la secuencia. Por ejemplo, el tamaño del marco de una secuencia estéreo (2 canales) con ejemplos de 16 bits es de cuatro bytes.

En el ejemplo de código siguiente se muestra cómo reproducir una secuencia de audio en el dispositivo de representación predeterminado:


```C++
//-----------------------------------------------------------
// Play an audio stream on the default audio rendering
// device. The PlayAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data to the
// rendering device. The inner loop runs every 1/2 second.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayAudioStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    UINT32 numFramesPadding;
    BYTE *pData;
    DWORD flags = 0;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetMixFormat(&pwfx);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_SHARED,
                         0,
                         hnsRequestedDuration,
                         0,
                         pwfx,
                         NULL);
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Get the actual size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // Grab the entire buffer for the initial fill operation.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    // Load the initial data into the shared buffer.
    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                        bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Sleep for half the buffer duration.
        Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

        // See how much buffer space is available.
        hr = pAudioClient->GetCurrentPadding(&numFramesPadding);
        EXIT_ON_ERROR(hr)

        numFramesAvailable = bufferFrameCount - numFramesPadding;

        // Grab all the available space in the shared buffer.
        hr = pRenderClient->GetBuffer(numFramesAvailable, &pData);
        EXIT_ON_ERROR(hr)

        // Get next 1/2-second of data from the audio source.
        hr = pMySource->LoadData(numFramesAvailable, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(numFramesAvailable, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for last data in buffer to play before stopping.
    Sleep((DWORD)(hnsActualDuration/REFTIMES_PER_MILLISEC/2));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



En el ejemplo anterior, la función PlayAudioStream toma un parámetro único, `pMySource` , que es un puntero a un objeto que pertenece a una clase definida por el cliente, MyAudioSource, con dos funciones miembro, LoadData y SetFormat. En el código de ejemplo no se incluye la implementación de MyAudioSource porque:

-   Ninguno de los miembros de clase se comunica directamente con ninguno de los métodos de las interfaces de WASAPI.
-   La clase podría implementarse de varias maneras, dependiendo de los requisitos del cliente. (Por ejemplo, podría leer los datos de representación de un archivo WAV y realizar una conversión inmediata al formato de secuencia).

Sin embargo, cierta información sobre el funcionamiento de las dos funciones resulta útil para entender el ejemplo.

La función LoadData escribe un número especificado de fotogramas de audio (primer parámetro) en una ubicación de búfer especificada (segundo parámetro). (El tamaño de un fotograma de audio es el número de canales de la secuencia multiplicado por el tamaño de la muestra). La función PlayAudioStream usa LoadData para rellenar partes del búfer compartido con datos de audio. La función SetFormat especifica el formato de la función LoadData que se va a usar para los datos. Si la función LoadData puede escribir al menos un fotograma en la ubicación de búfer especificada pero se queda sin datos antes de que haya escrito el número de fotogramas especificado, escribe el silencio en los fotogramas restantes.

Siempre que LoadData tenga éxito al escribir al menos un fotograma de datos reales (no de silencio) en la ubicación de búfer especificada, genera 0 a través de su tercer parámetro, que en el ejemplo de código anterior, es un puntero de salida a la `flags` variable. Cuando LoadData no tiene datos y no puede escribir incluso un solo fotograma en la ubicación de búfer especificada, no escribe nada en el búfer (ni en silencio) y escribe el valor AUDCLNT \_ BUFFERFLAGS \_ Silent en la `flags` variable. La `flags` variable transmite este valor al método [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , que responde rellenando el número de marcos especificado en el búfer con silencio.

En su llamada al método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , la función PlayAudioStream del ejemplo anterior solicita un búfer compartido que tiene una duración de un segundo. (El búfer asignado puede tener una duración ligeramente mayor). En sus llamadas iniciales a los métodos [**IAudioRenderClient:: getBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) y [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , la función rellena todo el búfer antes de llamar al método [**IAudioClient:: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) para empezar a reproducir el búfer.

Dentro del bucle principal, la función rellena de forma iterativa la mitad del búfer en intervalos de medio segundo. Justo antes de cada llamada a la función de [**suspensión**](/windows/win32/api/synchapi/nf-synchapi-sleep) de Windows en el bucle principal, el búfer está lleno o casi lleno. Cuando se devuelve la llamada de **suspensión** , el búfer se llena aproximadamente a la mitad. El bucle finaliza después de la llamada final a la función LoadData establece la `flags` variable en el valor AUDCLNT \_ BUFFERFLAGS \_ Silent. En ese momento, el búfer contiene al menos un marco de datos reales y puede contener hasta el medio segundo de datos reales. El resto del búfer contiene el silencio. La llamada de **suspensión** que sigue al bucle proporciona el tiempo suficiente (un medio segundo) para reproducir todos los datos restantes. El silencio que sigue a los datos impide que se produzcan sonidos no deseados antes de que la llamada al método [**IAudioClient:: Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) detenga la secuencia de audio. Para obtener más información acerca de la **suspensión**, consulte la documentación de Windows SDK.

Después de la llamada al método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , el flujo permanece abierto hasta que el cliente libera todas sus referencias a la interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) y todas las referencias a las interfaces de servicio que el cliente obtuvo a través del método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) . La llamada de [**versión**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) final cierra la secuencia.

La función PlayAudioStream del ejemplo de código anterior llama a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un enumerador para los dispositivos de punto de conexión de audio en el sistema. A menos que el programa de llamada previamente haya llamado a la función **CoCreateInstance** o [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca com, se producirá un error en la llamada a **CoCreateInstance** . Para obtener más información sobre **CoCreateInstance**, **CoCreateInstance** y **CoInitializeEx**, consulte la documentación de Windows SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de flujos](stream-management.md)
</dt> </dl>

 

 
