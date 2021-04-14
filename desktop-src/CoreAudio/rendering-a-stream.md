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
# <a name="rendering-a-stream"></a><span data-ttu-id="adc58-103">Representar una secuencia</span><span class="sxs-lookup"><span data-stu-id="adc58-103">Rendering a Stream</span></span>

<span data-ttu-id="adc58-104">El cliente llama a los métodos de la interfaz [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) para escribir los datos de representación en un búfer de extremo.</span><span class="sxs-lookup"><span data-stu-id="adc58-104">The client calls the methods in the [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient) interface to write rendering data to an endpoint buffer.</span></span> <span data-ttu-id="adc58-105">En el caso de una secuencia en modo compartido, el cliente comparte el búfer del extremo con el motor de audio.</span><span class="sxs-lookup"><span data-stu-id="adc58-105">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span> <span data-ttu-id="adc58-106">En el caso de una secuencia en modo exclusivo, el cliente comparte el búfer del extremo con el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="adc58-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span> <span data-ttu-id="adc58-107">Para solicitar un búfer de punto de conexión de un tamaño determinado, el cliente llama al método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="adc58-107">To request an endpoint buffer of a particular size, the client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="adc58-108">Para obtener el tamaño del búfer asignado, que puede ser diferente del tamaño solicitado, el cliente llama al método [**IAudioClient:: GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) .</span><span class="sxs-lookup"><span data-stu-id="adc58-108">To get the size of the allocated buffer, which might be different from the requested size, the client calls the [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize) method.</span></span>

<span data-ttu-id="adc58-109">Para trasladar un flujo de datos de representación a través del búfer del extremo, el cliente llama como método [**IAudioRenderClient:: getBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) y el método [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="adc58-109">To move a stream of rendering data through the endpoint buffer, the client alternately calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method and the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method.</span></span> <span data-ttu-id="adc58-110">El cliente tiene acceso a los datos del búfer del extremo como una serie de paquetes de datos.</span><span class="sxs-lookup"><span data-stu-id="adc58-110">The client accesses the data in the endpoint buffer as a series of data packets.</span></span> <span data-ttu-id="adc58-111">La llamada **getBuffer** recupera el siguiente paquete para que el cliente pueda rellenarlo con datos de representación.</span><span class="sxs-lookup"><span data-stu-id="adc58-111">The **GetBuffer** call retrieves the next packet so that the client can fill it with rendering data.</span></span> <span data-ttu-id="adc58-112">Después de escribir los datos en el paquete, el cliente llama a **ReleaseBuffer** para agregar el paquete completado a la cola de representación.</span><span class="sxs-lookup"><span data-stu-id="adc58-112">After writing the data to the packet, the client calls **ReleaseBuffer** to add the completed packet to the rendering queue.</span></span>

<span data-ttu-id="adc58-113">En el caso de un búfer de representación, el valor de relleno que indica el método [**IAudioClient:: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) representa la cantidad de datos de representación que se ponen en cola para reproducirse en el búfer.</span><span class="sxs-lookup"><span data-stu-id="adc58-113">For a rendering buffer, the padding value that is reported by the [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding) method represents the amount of rendering data that is queued up to play in the buffer.</span></span> <span data-ttu-id="adc58-114">Una aplicación de representación puede utilizar el valor de relleno para determinar cuántos datos nuevos puede escribir de forma segura en el búfer sin el riesgo de sobrescribir los datos escritos previamente que el motor de audio todavía no ha leído del búfer.</span><span class="sxs-lookup"><span data-stu-id="adc58-114">A rendering application can use the padding value to determine how much new data it can safely write to the buffer without the risk of overwriting previously written data that the audio engine has not yet read from the buffer.</span></span> <span data-ttu-id="adc58-115">El espacio disponible es simplemente el tamaño del búfer menos el tamaño del relleno.</span><span class="sxs-lookup"><span data-stu-id="adc58-115">The available space is simply the buffer size minus the padding size.</span></span> <span data-ttu-id="adc58-116">El cliente puede solicitar un tamaño de paquete que represente parte o todo este espacio disponible en su siguiente llamada a [**getBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) .</span><span class="sxs-lookup"><span data-stu-id="adc58-116">The client can request a packet size that represents some or all of this available space in its next [**GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) call.</span></span>

<span data-ttu-id="adc58-117">El tamaño de un paquete se expresa en *fotogramas de audio*.</span><span class="sxs-lookup"><span data-stu-id="adc58-117">The size of a packet is expressed in *audio frames*.</span></span> <span data-ttu-id="adc58-118">Una trama de audio en un flujo PCM es un conjunto de ejemplos (el conjunto contiene un ejemplo para cada canal de la secuencia) que se reproducen o se graban al mismo tiempo (reloj).</span><span class="sxs-lookup"><span data-stu-id="adc58-118">An audio frame in a PCM stream is a set of samples (the set contains one sample for each channel in the stream) that play or are recorded at the same time (clock tick).</span></span> <span data-ttu-id="adc58-119">Por lo tanto, el tamaño de un fotograma de audio es el tamaño de ejemplo multiplicado por el número de canales de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="adc58-119">Thus, the size of an audio frame is the sample size multiplied by the number of channels in the stream.</span></span> <span data-ttu-id="adc58-120">Por ejemplo, el tamaño del marco de una secuencia estéreo (2 canales) con ejemplos de 16 bits es de cuatro bytes.</span><span class="sxs-lookup"><span data-stu-id="adc58-120">For example, the frame size for a stereo (2-channel) stream with 16-bit samples is four bytes.</span></span>

<span data-ttu-id="adc58-121">En el ejemplo de código siguiente se muestra cómo reproducir una secuencia de audio en el dispositivo de representación predeterminado:</span><span class="sxs-lookup"><span data-stu-id="adc58-121">The following code example shows how to play an audio stream on the default rendering device:</span></span>


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



<span data-ttu-id="adc58-122">En el ejemplo anterior, la función PlayAudioStream toma un parámetro único, `pMySource` , que es un puntero a un objeto que pertenece a una clase definida por el cliente, MyAudioSource, con dos funciones miembro, LoadData y SetFormat.</span><span class="sxs-lookup"><span data-stu-id="adc58-122">In the preceding example, the PlayAudioStream function takes a single parameter, `pMySource`, which is a pointer to an object that belongs to a client-defined class, MyAudioSource, with two member functions, LoadData and SetFormat.</span></span> <span data-ttu-id="adc58-123">En el código de ejemplo no se incluye la implementación de MyAudioSource porque:</span><span class="sxs-lookup"><span data-stu-id="adc58-123">The example code does not include the implementation of MyAudioSource because:</span></span>

-   <span data-ttu-id="adc58-124">Ninguno de los miembros de clase se comunica directamente con ninguno de los métodos de las interfaces de WASAPI.</span><span class="sxs-lookup"><span data-stu-id="adc58-124">None of the class members communicates directly with any of the methods in the interfaces in WASAPI.</span></span>
-   <span data-ttu-id="adc58-125">La clase podría implementarse de varias maneras, dependiendo de los requisitos del cliente.</span><span class="sxs-lookup"><span data-stu-id="adc58-125">The class could be implemented in a variety of ways, depending on the requirements of the client.</span></span> <span data-ttu-id="adc58-126">(Por ejemplo, podría leer los datos de representación de un archivo WAV y realizar una conversión inmediata al formato de secuencia).</span><span class="sxs-lookup"><span data-stu-id="adc58-126">(For example, it might read the rendering data from a WAV file and perform on-the-fly conversion to the stream format.)</span></span>

<span data-ttu-id="adc58-127">Sin embargo, cierta información sobre el funcionamiento de las dos funciones resulta útil para entender el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="adc58-127">However, some information about the operation of the two functions is useful for understanding the example.</span></span>

<span data-ttu-id="adc58-128">La función LoadData escribe un número especificado de fotogramas de audio (primer parámetro) en una ubicación de búfer especificada (segundo parámetro).</span><span class="sxs-lookup"><span data-stu-id="adc58-128">The LoadData function writes a specified number of audio frames (first parameter) to a specified buffer location (second parameter).</span></span> <span data-ttu-id="adc58-129">(El tamaño de un fotograma de audio es el número de canales de la secuencia multiplicado por el tamaño de la muestra). La función PlayAudioStream usa LoadData para rellenar partes del búfer compartido con datos de audio.</span><span class="sxs-lookup"><span data-stu-id="adc58-129">(The size of an audio frame is the number of channels in the stream multiplied by the sample size.) The PlayAudioStream function uses LoadData to fill portions of the shared buffer with audio data.</span></span> <span data-ttu-id="adc58-130">La función SetFormat especifica el formato de la función LoadData que se va a usar para los datos.</span><span class="sxs-lookup"><span data-stu-id="adc58-130">The SetFormat function specifies the format for the LoadData function to use for the data.</span></span> <span data-ttu-id="adc58-131">Si la función LoadData puede escribir al menos un fotograma en la ubicación de búfer especificada pero se queda sin datos antes de que haya escrito el número de fotogramas especificado, escribe el silencio en los fotogramas restantes.</span><span class="sxs-lookup"><span data-stu-id="adc58-131">If the LoadData function is able to write at least one frame to the specified buffer location but runs out of data before it has written the specified number of frames, then it writes silence to the remaining frames.</span></span>

<span data-ttu-id="adc58-132">Siempre que LoadData tenga éxito al escribir al menos un fotograma de datos reales (no de silencio) en la ubicación de búfer especificada, genera 0 a través de su tercer parámetro, que en el ejemplo de código anterior, es un puntero de salida a la `flags` variable.</span><span class="sxs-lookup"><span data-stu-id="adc58-132">As long as LoadData succeeds in writing at least one frame of real data (not silence) to the specified buffer location, it outputs 0 through its third parameter, which, in the preceding code example, is an output pointer to the `flags` variable.</span></span> <span data-ttu-id="adc58-133">Cuando LoadData no tiene datos y no puede escribir incluso un solo fotograma en la ubicación de búfer especificada, no escribe nada en el búfer (ni en silencio) y escribe el valor AUDCLNT \_ BUFFERFLAGS \_ Silent en la `flags` variable.</span><span class="sxs-lookup"><span data-stu-id="adc58-133">When LoadData is out of data and cannot write even a single frame to the specified buffer location, it writes nothing to the buffer (not even silence), and it writes the value AUDCLNT\_BUFFERFLAGS\_SILENT to the `flags` variable.</span></span> <span data-ttu-id="adc58-134">La `flags` variable transmite este valor al método [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , que responde rellenando el número de marcos especificado en el búfer con silencio.</span><span class="sxs-lookup"><span data-stu-id="adc58-134">The `flags` variable conveys this value to the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method, which responds by filling the specified number of frames in the buffer with silence.</span></span>

<span data-ttu-id="adc58-135">En su llamada al método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , la función PlayAudioStream del ejemplo anterior solicita un búfer compartido que tiene una duración de un segundo.</span><span class="sxs-lookup"><span data-stu-id="adc58-135">In its call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the PlayAudioStream function in the preceding example requests a shared buffer that has a duration of one second.</span></span> <span data-ttu-id="adc58-136">(El búfer asignado puede tener una duración ligeramente mayor). En sus llamadas iniciales a los métodos [**IAudioRenderClient:: getBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) y [**IAudioRenderClient:: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) , la función rellena todo el búfer antes de llamar al método [**IAudioClient:: Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) para empezar a reproducir el búfer.</span><span class="sxs-lookup"><span data-stu-id="adc58-136">(The allocated buffer might have a slightly longer duration.) In its initial calls to the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) and [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) methods, the function fills the entire buffer before calling the [**IAudioClient::Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start) method to begin playing the buffer.</span></span>

<span data-ttu-id="adc58-137">Dentro del bucle principal, la función rellena de forma iterativa la mitad del búfer en intervalos de medio segundo.</span><span class="sxs-lookup"><span data-stu-id="adc58-137">Within the main loop, the function iteratively fills half of the buffer at half-second intervals.</span></span> <span data-ttu-id="adc58-138">Justo antes de cada llamada a la función de [**suspensión**](/windows/win32/api/synchapi/nf-synchapi-sleep) de Windows en el bucle principal, el búfer está lleno o casi lleno.</span><span class="sxs-lookup"><span data-stu-id="adc58-138">Just before each call to the Windows [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) function in the main loop, the buffer is full or nearly full.</span></span> <span data-ttu-id="adc58-139">Cuando se devuelve la llamada de **suspensión** , el búfer se llena aproximadamente a la mitad.</span><span class="sxs-lookup"><span data-stu-id="adc58-139">When the **Sleep** call returns, the buffer is about half full.</span></span> <span data-ttu-id="adc58-140">El bucle finaliza después de la llamada final a la función LoadData establece la `flags` variable en el valor AUDCLNT \_ BUFFERFLAGS \_ Silent.</span><span class="sxs-lookup"><span data-stu-id="adc58-140">The loop ends after the final call to the LoadData function sets the `flags` variable to the value AUDCLNT\_BUFFERFLAGS\_SILENT.</span></span> <span data-ttu-id="adc58-141">En ese momento, el búfer contiene al menos un marco de datos reales y puede contener hasta el medio segundo de datos reales.</span><span class="sxs-lookup"><span data-stu-id="adc58-141">At that point, the buffer contains at least one frame of real data, and it might contain as much as a half second of real data.</span></span> <span data-ttu-id="adc58-142">El resto del búfer contiene el silencio.</span><span class="sxs-lookup"><span data-stu-id="adc58-142">The remainder of the buffer contains silence.</span></span> <span data-ttu-id="adc58-143">La llamada de **suspensión** que sigue al bucle proporciona el tiempo suficiente (un medio segundo) para reproducir todos los datos restantes.</span><span class="sxs-lookup"><span data-stu-id="adc58-143">The **Sleep** call that follows the loop provides sufficient time (a half second) to play all of the remaining data.</span></span> <span data-ttu-id="adc58-144">El silencio que sigue a los datos impide que se produzcan sonidos no deseados antes de que la llamada al método [**IAudioClient:: Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) detenga la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="adc58-144">The silence that follows the data prevents unwanted sounds before the call to the [**IAudioClient::Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop) method stops the audio stream.</span></span> <span data-ttu-id="adc58-145">Para obtener más información acerca de la **suspensión**, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="adc58-145">For more information about **Sleep**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="adc58-146">Después de la llamada al método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) , el flujo permanece abierto hasta que el cliente libera todas sus referencias a la interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) y todas las referencias a las interfaces de servicio que el cliente obtuvo a través del método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="adc58-146">Following the call to the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method, the stream remains open until the client releases all of its references to the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface and to all references to service interfaces that the client obtained through the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="adc58-147">La llamada de [**versión**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) final cierra la secuencia.</span><span class="sxs-lookup"><span data-stu-id="adc58-147">The final [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) call closes the stream.</span></span>

<span data-ttu-id="adc58-148">La función PlayAudioStream del ejemplo de código anterior llama a la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear un enumerador para los dispositivos de punto de conexión de audio en el sistema.</span><span class="sxs-lookup"><span data-stu-id="adc58-148">The PlayAudioStream function in the preceding code example calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="adc58-149">A menos que el programa de llamada previamente haya llamado a la función **CoCreateInstance** o [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca com, se producirá un error en la llamada a **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="adc58-149">Unless the calling program previously called either the **CoCreateInstance** or [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="adc58-150">Para obtener más información sobre **CoCreateInstance**, **CoCreateInstance** y **CoInitializeEx**, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="adc58-150">For more information about **CoCreateInstance**, **CoCreateInstance**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="adc58-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="adc58-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adc58-152">Administración de flujos</span><span class="sxs-lookup"><span data-stu-id="adc58-152">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 
