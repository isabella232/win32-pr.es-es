---
description: Captura de una secuencia
ms.assetid: 1d9072dc-4f9b-4111-a747-5eb33ad3ae5b
title: Captura de una secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371d4b92b97a26e81074edee68216255d576e614
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165117"
---
# <a name="capturing-a-stream"></a>Captura de una secuencia

El cliente llama a los métodos de la [**interfaz IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) para leer los datos capturados de un búfer de punto de conexión. El cliente comparte el búfer del punto de conexión con el motor de audio en modo compartido y con el dispositivo de audio en modo exclusivo. Para solicitar un búfer de punto de conexión de un tamaño determinado, el cliente llama al [**método IAudioClient::Initialize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) Para obtener el tamaño del búfer asignado, que puede ser diferente del tamaño solicitado, el cliente llama al método [**IAudioClient::GetBufferSize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)

Para mover un flujo de datos capturados a través del búfer del punto de conexión, el cliente llama alternativamente al método [**IAudioCaptureClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) y al método [**IAudioCaptureClient::ReleaseBuffer.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) El cliente accede a los datos del búfer del punto de conexión como una serie de paquetes de datos. La **llamada a GetBuffer** recupera el siguiente paquete de datos capturados del búfer. Después de leer los datos del paquete, el cliente llama a **ReleaseBuffer** para liberar el paquete y hacer que esté disponible para más datos capturados.

El tamaño del paquete puede variar de una [**llamada a GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) a la siguiente. Antes de **llamar a GetBuffer**, el cliente tiene la opción de llamar al método [**IAudioCaptureClient::GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) para obtener el tamaño del siguiente paquete de antemano. Además, el cliente puede llamar al método [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) para obtener la cantidad total de datos capturados que están disponibles en el búfer. En cualquier momento, el tamaño del paquete siempre es menor o igual que la cantidad total de datos capturados en el búfer.

Durante cada paso de procesamiento, el cliente tiene la opción de procesar los datos capturados de una de las maneras siguientes:

-   El cliente llama alternativamente a [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) y [**ReleaseBuffer,**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer)leyendo un paquete con cada par de llamadas, hasta que **GetBuffer** devuelve AUDCNT \_ S BUFFEREMPTY, lo que indica que el búfer \_ está vacío.
-   El cliente llama a [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) antes de cada par de llamadas a [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) y [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) hasta que **GetNextPacketSize** notifica un tamaño de paquete de 0, lo que indica que el búfer está vacío.

Las dos técnicas producen resultados equivalentes.

En el ejemplo de código siguiente se muestra cómo grabar una secuencia de audio desde el dispositivo de captura predeterminado:


```C++
//-----------------------------------------------------------
// Record an audio stream from the default audio capture
// device. The RecordAudioStream function allocates a shared
// buffer big enough to hold one second of PCM audio data.
// The function uses this buffer to stream data from the
// capture device. The main loop runs every 1/2 second.
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
const IID IID_IAudioCaptureClient = __uuidof(IAudioCaptureClient);

HRESULT RecordAudioStream(MyAudioSink *pMySink)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = REFTIMES_PER_SEC;
    REFERENCE_TIME hnsActualDuration;
    UINT32 bufferFrameCount;
    UINT32 numFramesAvailable;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioCaptureClient *pCaptureClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    UINT32 packetLength = 0;
    BOOL bDone = FALSE;
    BYTE *pData;
    DWORD flags;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eCapture, eConsole, &pDevice);
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

    // Get the size of the allocated buffer.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioCaptureClient,
                         (void**)&pCaptureClient);
    EXIT_ON_ERROR(hr)

    // Notify the audio sink which format to use.
    hr = pMySink->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Calculate the actual duration of the allocated buffer.
    hnsActualDuration = (double)REFTIMES_PER_SEC *
                     bufferFrameCount / pwfx->nSamplesPerSec;

    hr = pAudioClient->Start();  // Start recording.
    EXIT_ON_ERROR(hr)

    // Each loop fills about half of the shared buffer.
    while (bDone == FALSE)
    {
        // Sleep for half the buffer duration.
        Sleep(hnsActualDuration/REFTIMES_PER_MILLISEC/2);

        hr = pCaptureClient->GetNextPacketSize(&packetLength);
        EXIT_ON_ERROR(hr)

        while (packetLength != 0)
        {
            // Get the available data in the shared buffer.
            hr = pCaptureClient->GetBuffer(
                                   &pData,
                                   &numFramesAvailable,
                                   &flags, NULL, NULL);
            EXIT_ON_ERROR(hr)

            if (flags & AUDCLNT_BUFFERFLAGS_SILENT)
            {
                pData = NULL;  // Tell CopyData to write silence.
            }

            // Copy the available capture data to the audio sink.
            hr = pMySink->CopyData(
                              pData, numFramesAvailable, &bDone);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->ReleaseBuffer(numFramesAvailable);
            EXIT_ON_ERROR(hr)

            hr = pCaptureClient->GetNextPacketSize(&packetLength);
            EXIT_ON_ERROR(hr)
        }
    }

    hr = pAudioClient->Stop();  // Stop recording.
    EXIT_ON_ERROR(hr)

Exit:
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pCaptureClient)

    return hr;
}
```



En el ejemplo anterior, la función RecordAudioStream toma un único parámetro, , que es un puntero a un objeto que pertenece a una clase definida por el `pMySink` cliente, MyAudioSink, con dos funciones, CopyData y SetFormat. El código de ejemplo no incluye la implementación de MyAudioSink porque:

-   Ninguno de los miembros de clase se comunica directamente con ninguno de los métodos de las interfaces de WASAPI.
-   La clase podría implementarse de varias maneras, en función de los requisitos del cliente. (Por ejemplo, podría escribir los datos de captura en un archivo WAV).

Sin embargo, la información sobre el funcionamiento de los dos métodos es útil para comprender el ejemplo.

La función CopyData copia un número especificado de fotogramas de audio de una ubicación de búfer especificada. La función RecordAudioStream usa la función CopyData para leer y guardar los datos de audio del búfer compartido. La función SetFormat especifica el formato de la función CopyData que se usará para los datos.

Siempre que el objeto MyAudioSink requiera datos adicionales, la función CopyData genera el valor **FALSE** a través de su tercer parámetro, que, en el ejemplo de código anterior, es un puntero a la variable `bDone` . Cuando el objeto MyAudioSink tiene todos los datos que necesita, la función CopyData establece en TRUE , lo que hace que el programa salga del bucle en la `bDone` función RecordAudioStream. 

La función RecordAudioStream asigna un búfer compartido que tiene una duración de un segundo. (El búfer asignado puede tener una duración ligeramente más larga). Dentro del bucle main, la llamada a la Windows [**sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) hace que el programa espere medio segundo. Al principio de cada llamada **de suspensión,** el búfer compartido está vacío o casi vacío. En el momento en que se devuelve la llamada a **Sleep,** el búfer compartido se rellena aproximadamente a la mitad con datos de captura.

Después de la llamada al método [**IAudioClient::Initialize,**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) la secuencia permanece abierta hasta que el cliente libera todas sus referencias a la interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) y a todas las referencias a las interfaces de servicio que el cliente obtuvo a través del método [**IAudioClient::GetService.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) La llamada [**release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) final cierra la secuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de flujos](stream-management.md)
</dt> </dl>

 

 
