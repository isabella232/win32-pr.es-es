---
description: Capturar una secuencia
ms.assetid: 1d9072dc-4f9b-4111-a747-5eb33ad3ae5b
title: Capturar una secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371d4b92b97a26e81074edee68216255d576e614
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907272"
---
# <a name="capturing-a-stream"></a><span data-ttu-id="9b082-103">Capturar una secuencia</span><span class="sxs-lookup"><span data-stu-id="9b082-103">Capturing a Stream</span></span>

<span data-ttu-id="9b082-104">El cliente llama a los métodos de la interfaz [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) para leer los datos capturados de un búfer de extremo.</span><span class="sxs-lookup"><span data-stu-id="9b082-104">The client calls the methods in the [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) interface to read captured data from an endpoint buffer.</span></span> <span data-ttu-id="9b082-105">El cliente comparte el búfer del extremo con el motor de audio en modo compartido y con el dispositivo de audio en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="9b082-105">The client shares the endpoint buffer with the audio engine in shared mode and with the audio device in exclusive mode.</span></span> <span data-ttu-id="9b082-106">Para solicitar un búfer de punto de conexión de un tamaño determinado, el cliente llama al método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="9b082-106">To request an endpoint buffer of a particular size, the client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="9b082-107">Para obtener el tamaño del búfer asignado, que puede ser diferente del tamaño solicitado, el cliente llama al método [**IAudioClient:: GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .</span><span class="sxs-lookup"><span data-stu-id="9b082-107">To get the size of the allocated buffer, which might be different from the requested size, the client calls the [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) method.</span></span>

<span data-ttu-id="9b082-108">Para desplazar una secuencia de datos capturados a través del búfer del punto de conexión, el cliente llama como método [**IAudioCaptureClient:: getBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) y el método [**IAudioCaptureClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="9b082-108">To move a stream of captured data through the endpoint buffer, the client alternately calls the [**IAudioCaptureClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) method and the [**IAudioCaptureClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) method.</span></span> <span data-ttu-id="9b082-109">El cliente tiene acceso a los datos del búfer del extremo como una serie de paquetes de datos.</span><span class="sxs-lookup"><span data-stu-id="9b082-109">The client accesses the data in the endpoint buffer as a series of data packets.</span></span> <span data-ttu-id="9b082-110">La llamada **getBuffer** recupera el siguiente paquete de datos capturados del búfer.</span><span class="sxs-lookup"><span data-stu-id="9b082-110">The **GetBuffer** call retrieves the next packet of captured data from the buffer.</span></span> <span data-ttu-id="9b082-111">Después de leer los datos del paquete, el cliente llama a **ReleaseBuffer** para liberar el paquete y hacer que esté disponible para más datos capturados.</span><span class="sxs-lookup"><span data-stu-id="9b082-111">After reading the data from the packet, the client calls **ReleaseBuffer** to release the packet and make it available for more captured data.</span></span>

<span data-ttu-id="9b082-112">El tamaño de paquete puede variar de una llamada de [**getBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="9b082-112">The packet size can vary from one [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) call to the next.</span></span> <span data-ttu-id="9b082-113">Antes de llamar a **getBuffer**, el cliente tiene la opción de llamar al método [**IAudioCaptureClient:: GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) para obtener el tamaño del siguiente paquete de antemano.</span><span class="sxs-lookup"><span data-stu-id="9b082-113">Before calling **GetBuffer**, the client has the option of calling the [**IAudioCaptureClient::GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) method to get the size of the next packet in advance.</span></span> <span data-ttu-id="9b082-114">Además, el cliente puede llamar al método [**IAudioClient:: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) para obtener la cantidad total de datos capturados que están disponibles en el búfer.</span><span class="sxs-lookup"><span data-stu-id="9b082-114">In addition, the client can call the [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) method to get the total amount of captured data that is available in the buffer.</span></span> <span data-ttu-id="9b082-115">En cualquier momento, el tamaño de paquete siempre es menor o igual que la cantidad total de datos capturados en el búfer.</span><span class="sxs-lookup"><span data-stu-id="9b082-115">At any instant, the packet size is always less than or equal to the total amount of captured data in the buffer.</span></span>

<span data-ttu-id="9b082-116">Durante cada paso de procesamiento, el cliente tiene la opción de procesar los datos capturados de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="9b082-116">During each processing pass, the client has the option of processing the captured data in one of the following ways:</span></span>

-   <span data-ttu-id="9b082-117">El cliente llama también a [**getBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) y [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), leyendo un paquete con cada par de llamadas, hasta que **getBuffer** devuelve AUDCNT \_ S \_ BUFFEREMPTY, lo que indica que el búfer está vacío.</span><span class="sxs-lookup"><span data-stu-id="9b082-117">The client alternately calls [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer), reading one packet with each pair of calls, until **GetBuffer** returns AUDCNT\_S\_BUFFEREMPTY, indicating that the buffer is empty.</span></span>
-   <span data-ttu-id="9b082-118">El cliente llama a [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) antes de cada par de llamadas a [**getBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) y [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) hasta que **GetNextPacketSize** informa de un tamaño de paquete de 0, lo que indica que el búfer está vacío.</span><span class="sxs-lookup"><span data-stu-id="9b082-118">The client calls [**GetNextPacketSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize) before each pair of calls to [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer) and [**ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-releasebuffer) until **GetNextPacketSize** reports a packet size of 0, indicating that the buffer is empty.</span></span>

<span data-ttu-id="9b082-119">Las dos técnicas producen resultados equivalentes.</span><span class="sxs-lookup"><span data-stu-id="9b082-119">The two techniques yield equivalent results.</span></span>

<span data-ttu-id="9b082-120">En el ejemplo de código siguiente se muestra cómo registrar una secuencia de audio desde el dispositivo de captura predeterminado:</span><span class="sxs-lookup"><span data-stu-id="9b082-120">The following code example shows how to record an audio stream from the default capture device:</span></span>


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



<span data-ttu-id="9b082-121">En el ejemplo anterior, la función RecordAudioStream toma un parámetro único, `pMySink` , que es un puntero a un objeto que pertenece a una clase definida por el cliente, MyAudioSink, con dos funciones, CopyData y SetFormat.</span><span class="sxs-lookup"><span data-stu-id="9b082-121">In the preceding example, the RecordAudioStream function takes a single parameter, `pMySink`, which is a pointer to an object that belongs to a client-defined class, MyAudioSink, with two functions, CopyData and SetFormat.</span></span> <span data-ttu-id="9b082-122">En el código de ejemplo no se incluye la implementación de MyAudioSink porque:</span><span class="sxs-lookup"><span data-stu-id="9b082-122">The example code does not include the implementation of MyAudioSink because:</span></span>

-   <span data-ttu-id="9b082-123">Ninguno de los miembros de clase se comunica directamente con ninguno de los métodos de las interfaces de WASAPI.</span><span class="sxs-lookup"><span data-stu-id="9b082-123">None of the class members communicates directly with any of the methods in the interfaces in WASAPI.</span></span>
-   <span data-ttu-id="9b082-124">La clase podría implementarse de varias maneras, dependiendo de los requisitos del cliente.</span><span class="sxs-lookup"><span data-stu-id="9b082-124">The class could be implemented in a variety of ways, depending on the requirements of the client.</span></span> <span data-ttu-id="9b082-125">(Por ejemplo, puede escribir los datos de captura en un archivo WAV).</span><span class="sxs-lookup"><span data-stu-id="9b082-125">(For example, it might write the capture data to a WAV file.)</span></span>

<span data-ttu-id="9b082-126">Sin embargo, la información sobre el funcionamiento de los dos métodos resulta útil para entender el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9b082-126">However, information about the operation of the two methods is useful for understanding the example.</span></span>

<span data-ttu-id="9b082-127">La función CopyData copia un número especificado de fotogramas de audio de una ubicación de búfer especificada.</span><span class="sxs-lookup"><span data-stu-id="9b082-127">The CopyData function copies a specified number of audio frames from a specified buffer location.</span></span> <span data-ttu-id="9b082-128">La función RecordAudioStream usa la función CopyData para leer y guardar los datos de audio desde el búfer compartido.</span><span class="sxs-lookup"><span data-stu-id="9b082-128">The RecordAudioStream function uses the CopyData function to read and save the audio data from the shared buffer.</span></span> <span data-ttu-id="9b082-129">La función SetFormat especifica el formato de la función CopyData que se va a usar para los datos.</span><span class="sxs-lookup"><span data-stu-id="9b082-129">The SetFormat function specifies the format for the CopyData function to use for the data.</span></span>

<span data-ttu-id="9b082-130">Siempre que el objeto MyAudioSink requiera datos adicionales, la función CopyData devuelve el valor **false** a través de su tercer parámetro, que, en el ejemplo de código anterior, es un puntero a la variable `bDone` .</span><span class="sxs-lookup"><span data-stu-id="9b082-130">As long as the MyAudioSink object requires additional data, the CopyData function outputs the value **FALSE** through its third parameter, which, in the preceding code example, is a pointer to the variable `bDone`.</span></span> <span data-ttu-id="9b082-131">Cuando el objeto MyAudioSink tiene todos los datos que necesita, la función CopyData se establece `bDone` en **true**, lo que hace que el programa salga del bucle en la función RecordAudioStream.</span><span class="sxs-lookup"><span data-stu-id="9b082-131">When the MyAudioSink object has all the data that it requires, the CopyData function sets `bDone` to **TRUE**, which causes the program to exit the loop in the RecordAudioStream function.</span></span>

<span data-ttu-id="9b082-132">La función RecordAudioStream asigna un búfer compartido que tiene una duración de un segundo.</span><span class="sxs-lookup"><span data-stu-id="9b082-132">The RecordAudioStream function allocates a shared buffer that has a duration of one second.</span></span> <span data-ttu-id="9b082-133">(El búfer asignado puede tener una duración ligeramente mayor). Dentro del bucle principal, la llamada a la función de [**suspensión**](/windows/desktop/api/synchapi/nf-synchapi-sleep) de Windows hace que el programa espere un medio segundo.</span><span class="sxs-lookup"><span data-stu-id="9b082-133">(The allocated buffer might have a slightly longer duration.) Within the main loop, the call to the Windows [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep) function causes the program to wait for a half second.</span></span> <span data-ttu-id="9b082-134">Al principio de cada llamada de **suspensión** , el búfer compartido está vacío o casi vacío.</span><span class="sxs-lookup"><span data-stu-id="9b082-134">At the start of each **Sleep** call, the shared buffer is empty or nearly empty.</span></span> <span data-ttu-id="9b082-135">En el momento en que se devuelve la llamada de **suspensión** , el búfer compartido es aproximadamente la mitad de los datos de captura.</span><span class="sxs-lookup"><span data-stu-id="9b082-135">By the time the **Sleep** call returns, the shared buffer is about half filled with capture data.</span></span>

<span data-ttu-id="9b082-136">Después de la llamada al método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , el flujo permanece abierto hasta que el cliente libera todas sus referencias a la interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) y todas las referencias a las interfaces de servicio que el cliente obtuvo a través del método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="9b082-136">Following the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the stream remains open until the client releases all of its references to the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and to all references to service interfaces that the client obtained through the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="9b082-137">La llamada de [**versión**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) final cierra la secuencia.</span><span class="sxs-lookup"><span data-stu-id="9b082-137">The final [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call closes the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b082-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b082-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b082-139">Administración de flujos</span><span class="sxs-lookup"><span data-stu-id="9b082-139">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 
