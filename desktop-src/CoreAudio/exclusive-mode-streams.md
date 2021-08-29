---
description: Exclusive-Mode Secuencias
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Exclusive-Mode Secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50bc9b17dbb508d04bd4665b48dfaa8f1373cc1e167b892f7ac791b3d9a0d0b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104415"
---
# <a name="exclusive-mode-streams"></a>Exclusive-Mode Secuencias

Como se explicó anteriormente, si una aplicación abre una secuencia en modo exclusivo, la aplicación tiene un uso exclusivo del dispositivo de punto de conexión de audio que reproduce o registra la secuencia. Por el contrario, varias aplicaciones pueden compartir un dispositivo de punto de conexión de audio abriendo secuencias en modo compartido en el dispositivo.

El acceso en modo exclusivo a un dispositivo de audio puede bloquear sonidos cruciales del sistema, impedir la interoperabilidad con otras aplicaciones y, de lo contrario, degradar la experiencia del usuario. Para mitigar estos problemas, una aplicación con una secuencia en modo exclusivo normalmente vuelve a tener el control del dispositivo de audio cuando la aplicación no es el proceso de primer plano o no está transmitiendo activamente.

La latencia de flujo es el retraso inherente a la ruta de acceso de datos que conecta el búfer de punto de conexión de una aplicación con un dispositivo de punto de conexión de audio. Para una secuencia de representación, la latencia es el retraso máximo desde el momento en que una aplicación escribe una muestra en un búfer de punto de conexión hasta el momento en que la muestra se escucha a través de los hablantes. Para una secuencia de captura, la latencia es el retraso máximo desde el momento en que un sonido entra en el micrófono hasta el momento en que una aplicación puede leer el ejemplo de ese sonido desde el búfer del punto de conexión.

Las aplicaciones que usan secuencias en modo exclusivo a menudo lo hacen porque requieren latencias bajas en las rutas de acceso de datos entre los dispositivos de punto de conexión de audio y los subprocesos de aplicación que acceden a los búferes de punto de conexión. Normalmente, estos subprocesos se ejecutan con una prioridad relativamente alta y se programan para ejecutarse a intervalos periódicos cercanos o iguales que el intervalo periódico que separa las sucesivas pasadas de procesamiento por el hardware de audio. Durante cada paso, el hardware de audio procesa los nuevos datos en los búferes del punto de conexión.

Para lograr las latencias de transmisión más pequeñas, una aplicación puede requerir hardware de audio especial y un sistema informático que se carga ligeramente. La conducción del hardware de audio más allá de sus límites de tiempo o la carga del sistema con tareas de alta prioridad en competencia pueden provocar un problema en una secuencia de audio de baja latencia. Por ejemplo, en el caso de una secuencia de representación, puede producirse un problema si la aplicación no puede escribir en un búfer de punto de conexión antes de que el hardware de audio lea el búfer o si el hardware no puede leer el búfer antes de la hora en que el búfer está programado para reproducirse. Normalmente, una aplicación diseñada para ejecutarse en una amplia variedad de hardware de audio y en una amplia gama de sistemas debe relajar sus requisitos de tiempo lo suficiente como para evitar problemas en todos los entornos de destino.

Windows Vista tiene varias características para admitir aplicaciones que requieren secuencias de audio de baja latencia. Como se describe en Componentes de [audio](user-mode-audio-components.md)en modo de usuario, las aplicaciones que realizan operaciones críticas en el tiempo pueden llamar a las funciones del servicio Programador de clases multimedia (MMCSS) para aumentar la prioridad de subproceso sin denegar los recursos de CPU a las aplicaciones de prioridad inferior. Además, el método [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) admite una marca EVENTCALLBACK AUDCLNT STREAMFLAGS que permite que el subproceso de mantenimiento del búfer de una aplicación programe su ejecución para que se produzca cuando un nuevo búfer esté disponible en el dispositivo \_ \_ de audio. Con estas características, un subproceso de aplicación puede reducir la incertidumbre sobre cuándo se ejecutará, lo que reduce el riesgo de problemas en una secuencia de audio de baja latencia.

Es probable que los controladores de adaptadores de audio más antiguos usen la interfaz de controlador de dispositivo (DDI) WaveCyclic o WavePci, mientras que los controladores de adaptadores de audio más recientes tienen más probabilidades de admitir el DDI de WaveRT. En el caso de las aplicaciones en modo exclusivo, los controladores WaveRT pueden proporcionar un mejor rendimiento que los controladores WaveCyclic o WavePci, pero los controladores waveRT requieren funcionalidades de hardware adicionales. Estas funcionalidades incluyen la capacidad de compartir búferes de hardware directamente con las aplicaciones. Con el uso compartido directo, no se requiere ninguna intervención del sistema para transferir datos entre una aplicación en modo exclusivo y el hardware de audio. En cambio, los controladores WaveCyclic y WavePci son adecuados para adaptadores de audio más antiguos y con menos capacidad. Estos adaptadores se basan en el software del sistema para transportar bloques de datos (conectados a paquetes de solicitud de E/S del sistema o IRP) entre búferes de aplicación y búferes de hardware. Además, los dispositivos de audio USB se basan en el software del sistema para transportar datos entre búferes de aplicación y búferes de hardware. Para mejorar el rendimiento de las aplicaciones en modo exclusivo que se conectan a dispositivos de audio que dependen del sistema para el transporte de datos, WASAPI aumenta automáticamente la prioridad de los subprocesos del sistema que transfieren datos entre las aplicaciones y el hardware. WASAPI usa MMCSS para aumentar la prioridad del subproceso. En Windows Vista, si un subproceso del sistema administra el transporte de datos para una secuencia de reproducción de audio en modo exclusivo con un formato PCM y un período de dispositivo inferior a 10 milisegundos, WASAPI asigna el nombre de tarea MMCSS "Pro Audio" al subproceso. Si el período de dispositivo de la secuencia es mayor o igual que 10 milisegundos, WASAPI asigna el nombre de tarea MMCSS "Audio" al subproceso. Para más información sobre los DDIs de WaveCyclic, WavePci y WaveRT, consulte la documentación Windows DDK. Para obtener información sobre cómo seleccionar un período de dispositivo adecuado, vea [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).

Como se describe en [Controles](session-volume-controls.md)de volumen de sesión, [WASAPI](wasapi.md) proporciona las interfaces [**ISimpleAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) para controlar los niveles de volumen de las secuencias de audio en modo compartido. Sin embargo, los controles de estas interfaces no tienen ningún efecto en los flujos en modo exclusivo. En su lugar, las aplicaciones que administran secuencias en modo exclusivo suelen usar la interfaz [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) en la [API EndpointVolume](endpointvolume-api.md) para controlar los niveles de volumen de esas secuencias. Para obtener información sobre esta interfaz, vea [Controles de volumen de punto de conexión.](endpoint-volume-controls.md)

Para cada dispositivo de reproducción y captura del sistema, el usuario puede controlar si el dispositivo se puede usar en modo exclusivo. Si el usuario deshabilita el uso en modo exclusivo del dispositivo, el dispositivo se puede usar para reproducir o grabar solo secuencias en modo compartido.

Si el usuario habilita el uso en modo exclusivo del dispositivo, el usuario también puede controlar si una solicitud de una aplicación para usar el dispositivo en modo exclusivo adelantará el uso del dispositivo por parte de las aplicaciones que podrían reproducir o grabar secuencias en modo compartido a través del dispositivo. Si el adelantamiento está habilitado, una solicitud de una aplicación para tomar el control exclusivo del dispositivo se realiza correctamente si el dispositivo no está en uso actualmente o si el dispositivo se está utilizando en modo compartido, pero se produce un error en la solicitud si otra aplicación ya tiene control exclusivo del dispositivo. Si el adelantamiento está deshabilitado, una solicitud de una aplicación para tomar el control exclusivo del dispositivo se realiza correctamente si el dispositivo no está actualmente en uso, pero se produce un error en la solicitud si el dispositivo ya se está utilizando en modo compartido o en modo exclusivo.

En Windows Vista, la configuración predeterminada para un dispositivo de punto de conexión de audio es la siguiente:

-   El dispositivo se puede usar para reproducir o grabar secuencias en modo exclusivo.
-   Una solicitud para usar un dispositivo para reproducir o grabar una secuencia en modo exclusivo adelanta cualquier secuencia en modo compartido que se reproduce o graba actualmente a través del dispositivo.

**Para cambiar la configuración de modo exclusivo de un dispositivo de reproducción o grabación**

1.  Haga clic con el botón derecho en el icono del altavoz en el área de notificación, que se encuentra en el lado derecho de la barra de tareas, y seleccione Dispositivos de reproducción **o** **Dispositivos de grabación.** (Como alternativa, ejecute el panel de control multimedia Windows, Mmsys.cpl, desde una ventana del símbolo del sistema. Para obtener más información, vea Comentarios en [constantes XXX de ESTADO \_ \_ DEL](device-state-xxx-constants.md)DISPOSITIVO).
2.  Cuando aparezca **la ventana** Sonido, seleccione **Reproducción** o **Grabación.** A continuación, seleccione una entrada en la lista de nombres de dispositivo y haga clic en **Propiedades.**
3.  Cuando aparezca **la ventana** Propiedades, haga clic **en Avanzadas.**
4.  Para permitir que las aplicaciones usen el dispositivo en modo exclusivo, active la casilla Permitir que las aplicaciones **tomen el control exclusivo de este dispositivo.** Para deshabilitar el uso en modo exclusivo del dispositivo, desactive la casilla.
5.  Si está habilitado el uso en modo exclusivo del dispositivo, puede especificar si una solicitud de control exclusivo del dispositivo se realizará correctamente si el dispositivo está reproduciendo o grabando secuencias en modo compartido. Para dar prioridad a las aplicaciones en modo exclusivo sobre las aplicaciones en modo compartido, active la casilla Con la etiqueta Dar prioridad **a las aplicaciones en modo exclusivo.** Para denegar la prioridad de las aplicaciones en modo exclusivo sobre las aplicaciones en modo compartido, desactive la casilla.

En el ejemplo de código siguiente se muestra cómo reproducir una secuencia de audio de baja latencia en un dispositivo de representación de audio configurado para su uso en modo exclusivo:


```C++
//-----------------------------------------------------------
// Play an exclusive-mode stream on the default audio
// rendering device. The PlayExclusiveStream function uses
// event-driven buffering and MMCSS to play the stream at
// the minimum latency supported by the device.
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

HRESULT PlayExclusiveStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = 0;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    HANDLE hEvent = NULL;
    HANDLE hTask = NULL;
    UINT32 bufferFrameCount;
    BYTE *pData;
    DWORD flags = 0;
    DWORD taskIndex = 0;
    
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

    // Call a helper function to negotiate with the audio
    // device for an exclusive-mode stream format.
    hr = GetStreamFormat(pAudioClient, &pwfx);
    EXIT_ON_ERROR(hr)

    // Initialize the stream to play at the minimum latency.
    hr = pAudioClient->GetDevicePeriod(NULL, &hnsRequestedDuration);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_EXCLUSIVE,
                         AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
                         hnsRequestedDuration,
                         hnsRequestedDuration,
                         pwfx,
                         NULL);
    if (hr == AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED) {
        // Align the buffer if needed, see IAudioClient::Initialize() documentation
        UINT32 nFrames = 0;
        hr = pAudioClient->GetBufferSize(&nFrames);
        EXIT_ON_ERROR(hr)
        hnsRequestedDuration = (REFERENCE_TIME)((double)REFTIMES_PER_SEC / pwfx->nSamplesPerSec * nFrames + 0.5);
        hr = pAudioClient->Initialize(
            AUDCLNT_SHAREMODE_EXCLUSIVE,
            AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
            hnsRequestedDuration,
            hnsRequestedDuration,
            pwfx,
            NULL);
    }
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Create an event handle and register it for
    // buffer-event notifications.
    hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = E_FAIL;
        goto Exit;
    }

    hr = pAudioClient->SetEventHandle(hEvent);
    EXIT_ON_ERROR(hr);

    // Get the actual size of the two allocated buffers.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // To reduce latency, load the first buffer with data
    // from the audio source before starting the stream.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Ask MMCSS to temporarily boost the thread priority
    // to reduce glitches while the low-latency stream plays.
    hTask = AvSetMmThreadCharacteristics(TEXT("Pro Audio"), &taskIndex);
    if (hTask == NULL)
    {
        hr = E_FAIL;
        EXIT_ON_ERROR(hr)
    }

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills one of the two buffers.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Wait for next buffer event to be signaled.
        DWORD retval = WaitForSingleObject(hEvent, 2000);
        if (retval != WAIT_OBJECT_0)
        {
            // Event handle timed out after a 2-second wait.
            pAudioClient->Stop();
            hr = ERROR_TIMEOUT;
            goto Exit;
        }

        // Grab the next empty buffer from the audio device.
        hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
        EXIT_ON_ERROR(hr)

        // Load the buffer with data from the audio source.
        hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for the last buffer to play before stopping.
    Sleep((DWORD)(hnsRequestedDuration/REFTIMES_PER_MILLISEC));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    if (hEvent != NULL)
    {
        CloseHandle(hEvent);
    }
    if (hTask != NULL)
    {
        AvRevertMmThreadCharacteristics(hTask);
    }
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



En el ejemplo de código anterior, la función PlayExclusiveStream se ejecuta en el subproceso de aplicación que proporciona servicios a los búferes de punto de conexión mientras se reproduce una secuencia de representación. La función toma un único parámetro, pMySource, que es un puntero a un objeto que pertenece a una clase definida por el cliente, MyAudioSource. Esta clase tiene dos funciones miembro, LoadData y SetFormat, a las que se llama en el ejemplo de código. MyAudioSource se describe en [Representación de una secuencia.](rendering-a-stream.md)

La función PlayExclusiveStream llama a una función auxiliar, GetStreamFormat, que negocia con el dispositivo de representación predeterminado para determinar si el dispositivo admite un formato de secuencia en modo exclusivo que es adecuado para su uso por parte de la aplicación. El código de la función GetStreamFormat no aparece en el ejemplo de código; esto se debe a que los detalles de su implementación dependen completamente de los requisitos de la aplicación. Sin embargo, la operación de la función GetStreamFormat se puede describir simplemente: llama al método [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) una o varias veces para determinar si el dispositivo admite un formato adecuado. Los requisitos de la aplicación dictan qué formatos presenta GetStreamFormat al método **IsFormatSupported** y el orden en que los presenta. Para obtener más información sobre **IsFormatSupported, vea** [Formatos de dispositivo.](device-formats.md)

Después de la llamada a GetStreamFormat, la función PlayExclusiveStream llama al método [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) para obtener el período mínimo de dispositivo admitido por el hardware de audio. A continuación, la función llama al [**método IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) para solicitar una duración de búfer igual al período mínimo. Si la llamada se realiza correctamente, el método **Initialize** asigna dos búferes de punto de conexión, cada uno de los cuales es igual de duración al período mínimo. Más adelante, cuando la secuencia de audio comience a ejecutarse, la aplicación y el hardware de audio compartirán los dos búferes de forma "ping-ping-ping", es decir, mientras la aplicación escribe en un búfer, el hardware lee desde el otro búfer.

Antes de iniciar la secuencia, la función PlayExclusiveStream hace lo siguiente:

-   Crea y registra el identificador de eventos a través del cual recibirá notificaciones cuando los búferes estén listos para rellenarse.
-   Rellena el primer búfer con datos del origen de audio para reducir el retraso desde que la secuencia comienza a ejecutarse hasta que se escucha el sonido inicial.
-   Llama a **la función AvSetMmThreadCharacteristics** para solicitar que MMCSS aumente la prioridad del subproceso en el que se ejecuta PlayExclusiveStream. (Cuando la secuencia deja de ejecutarse, la llamada a la función **AvRevertMmThreadCharacteristics** restaura la prioridad del subproceso original).

Para obtener más información sobre **AvSetMmThreadCharacteristics** y **AvRevertMmThreadCharacteristics,** consulte la documentación Windows SDK.

Mientras se ejecuta la secuencia, cada iteración del **bucle while** del ejemplo de código anterior rellena un búfer de punto de conexión. Entre iteraciones, la llamada a la función **WaitForSingleObject** espera a que se señale el identificador de evento. Cuando se señala el identificador, el cuerpo del bucle hace lo siguiente:

1.  Llama al [**método IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) para obtener el siguiente búfer.
2.  Rellena el búfer.
3.  Llama al [**método IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) para liberar el búfer.

Para obtener más información sobre **WaitForSingleObject,** consulte la documentación Windows SDK.

Si el adaptador de audio está controlado por un controlador WaveRT, la señalización del identificador de eventos está asociada a las notificaciones de transferencia de DMA desde el hardware de audio. Para un dispositivo de audio USB o para un dispositivo de audio controlado por un controlador WaveCyclic o WavePci, la señalización del identificador de evento está asociada a las finalizaciones de los IRP que transfieren datos desde el búfer de la aplicación al búfer de hardware.

En el ejemplo de código anterior se inserta el hardware de audio y el sistema informático a sus límites de rendimiento. En primer lugar, para reducir la latencia del flujo, la aplicación programa su subproceso de servicio de búfer para usar el período de dispositivo mínimo que admitirá el hardware de audio. En segundo lugar, para asegurarse de que el subproceso se ejecuta de forma confiable dentro de cada período de dispositivo, la llamada a la función **AvSetMmThreadCharacteristics** establece el parámetro TaskName en "Pro Audio", que es, en Windows Vista, el nombre de tarea predeterminado con la prioridad más alta. Considere si los requisitos de tiempo de la aplicación podrían ser relajadas sin poner en peligro su utilidad. Por ejemplo, la aplicación podría programar su subproceso de mantenimiento del búfer para que use un período mayor que el mínimo. Un período más largo podría permitir de forma segura el uso de una prioridad de subproceso inferior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de flujos](stream-management.md)
</dt> </dl>

 

 



