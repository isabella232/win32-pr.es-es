---
description: En este artículo se presentan algunos ejemplos sencillos que muestran cómo implementar el sonido espacial mediante objetos de audio espacial estático, objetos de audio espacial dinámico y objetos de audio espacial que usan la función de transferencia relativa de la cabeza de Microsoft (HRTF).
ms.assetid: C99C342E-0BD9-486A-92AA-F8DCB72C1B00
title: Representar sonido espacial mediante objetos de audio espacial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd541026aa3e144ec8333c8ac045a17970735f17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807561"
---
# <a name="render-spatial-sound-using-spatial-audio-objects"></a><span data-ttu-id="c352d-103">Representar sonido espacial mediante objetos de audio espacial</span><span class="sxs-lookup"><span data-stu-id="c352d-103">Render Spatial Sound Using Spatial Audio Objects</span></span>

<span data-ttu-id="c352d-104">En este artículo se presentan algunos ejemplos sencillos que muestran cómo implementar el sonido espacial mediante objetos de audio espacial estático, objetos de audio espacial dinámico y objetos de audio espacial que usan la función de transferencia relativa de la cabeza de Microsoft (HRTF).</span><span class="sxs-lookup"><span data-stu-id="c352d-104">This article presents some simple examples that illustrate how to implement spatial sound using static spatial audio objects, dynamic spatial audio objects, and spatial audio objects that use Microsoft's Head Relative Transfer Function (HRTF).</span></span> <span data-ttu-id="c352d-105">Los pasos de implementación para las tres técnicas son muy similares y en este artículo se proporciona un ejemplo de código estructurado similar para cada técnica.</span><span class="sxs-lookup"><span data-stu-id="c352d-105">The implementation steps for all three of these techniques are very similar and this article provides a similarly structured code example for each technique.</span></span> <span data-ttu-id="c352d-106">Para obtener ejemplos completos de un extremo a otro de implementaciones de audio espacial del mundo real, vea el [repositorio de github de ejemplos de sonido espacial de Microsoft](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio).</span><span class="sxs-lookup"><span data-stu-id="c352d-106">For complete end-to-end examples of real-world spatial audio implementations, see [Microsoft Spatial Sound samples github repository](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio).</span></span> <span data-ttu-id="c352d-107">Para obtener información general sobre Windows Sonic, la solución de nivel de plataforma de Microsoft para la compatibilidad con el sonido espacial en Xbox y Windows, consulte el tema sobre el [sonido espacial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="c352d-107">For an overview of Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, see [Spatial Sound](spatial-sound.md).</span></span>

## <a name="render-audio-using-static-spatial-audio-objects"></a><span data-ttu-id="c352d-108">Representar audio mediante objetos de audio espacial estáticos</span><span class="sxs-lookup"><span data-stu-id="c352d-108">Render audio using static spatial audio objects</span></span>

<span data-ttu-id="c352d-109">Un objeto de audio estático se usa para representar el sonido en uno de 18 canales de audio estáticos definidos en la enumeración [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) .</span><span class="sxs-lookup"><span data-stu-id="c352d-109">A static audio object is used to render sound to one of 18 static audio channels defined in the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration.</span></span> <span data-ttu-id="c352d-110">Cada uno de estos canales representa un altavoz real o virtualizado en un punto fijo del espacio que no se mueve con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c352d-110">Each of these channels represents a real or virtualized speaker at a fixed point in space that does not move over time.</span></span> <span data-ttu-id="c352d-111">Los canales estáticos que están disponibles en un dispositivo determinado dependen del formato de sonido espacial que se esté usando.</span><span class="sxs-lookup"><span data-stu-id="c352d-111">The static channels that are available on a particular device depend on the spatial sound format being used.</span></span> <span data-ttu-id="c352d-112">Para obtener una lista de los formatos admitidos y sus recuentos de canales, consulte [sonido espacial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="c352d-112">For a list of the supported formats and their channel counts, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="c352d-113">Al inicializar una secuencia de audio espacial, debe especificar cuál de los canales estáticos disponibles usará la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c352d-113">When you initialize a spatial audio stream, you must specify which of the available static channels the stream will use.</span></span> <span data-ttu-id="c352d-114">Las siguientes definiciones de constantes de ejemplo se pueden usar para especificar configuraciones de altavoces comunes y obtener el número de canales disponibles para cada una de ellas.</span><span class="sxs-lookup"><span data-stu-id="c352d-114">The following example constant definitions can be used to specify common speaker configurations and get the number of channels available for each one.</span></span>


```C++
const AudioObjectType ChannelMask_Mono = AudioObjectType_FrontCenter;
const AudioObjectType ChannelMask_Stereo = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight);
const AudioObjectType ChannelMask_2_1 = (AudioObjectType)(ChannelMask_Stereo | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_Quad = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_BackLeft | AudioObjectType_BackRight);
const AudioObjectType ChannelMask_4_1 = (AudioObjectType)(ChannelMask_Quad | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_5_1 = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_FrontCenter | AudioObjectType_LowFrequency | AudioObjectType_SideLeft | AudioObjectType_SideRight);
const AudioObjectType ChannelMask_7_1 = (AudioObjectType)(ChannelMask_5_1 | AudioObjectType_BackLeft | AudioObjectType_BackRight);

const UINT32 MaxStaticObjectCount_7_1_4 = 12;
const AudioObjectType ChannelMask_7_1_4 = (AudioObjectType)(ChannelMask_7_1 | AudioObjectType_TopFrontLeft | AudioObjectType_TopFrontRight | AudioObjectType_TopBackLeft | AudioObjectType_TopBackRight);

const UINT32 MaxStaticObjectCount_7_1_4_4 = 16;
const AudioObjectType ChannelMask_7_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4 | AudioObjectType_BottomFrontLeft | AudioObjectType_BottomFrontRight |AudioObjectType_BottomBackLeft | AudioObjectType_BottomBackRight);

const UINT32 MaxStaticObjectCount_8_1_4_4 = 17;
const AudioObjectType ChannelMask_8_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4_4 | AudioObjectType_BackCenter);
```



<span data-ttu-id="c352d-115">El primer paso en la representación del audio espacial es obtener el punto de conexión de audio al que se enviarán los datos de audio.</span><span class="sxs-lookup"><span data-stu-id="c352d-115">The first step in rendering spatial audio is to get the audio endpoint to which audio data will be sent.</span></span> <span data-ttu-id="c352d-116">Cree una instancia de [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) y llame a [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obtener el dispositivo de representación de audio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c352d-116">Create an instance of [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) and call [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the default audio render device.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="c352d-117">Al crear una secuencia de audio espacial, debe especificar el formato de audio que la secuencia usará proporcionando una estructura [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="c352d-117">When you create a spatial audio stream, you must specify the audio format the stream will use by providing a [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) structure.</span></span> <span data-ttu-id="c352d-118">Si está reproduciendo audio desde un archivo, el formato del archivo de audio suele determinar el formato.</span><span class="sxs-lookup"><span data-stu-id="c352d-118">If you are playing back audio from a file, the format is typically determined by the audio file format.</span></span> <span data-ttu-id="c352d-119">En este ejemplo se usa un formato mono de 32 bits y 48Hz.</span><span class="sxs-lookup"><span data-stu-id="c352d-119">This example uses a mono, 32-bit, 48Hz format.</span></span>


```C++
WAVEFORMATEX format;
format.wFormatTag = WAVE_FORMAT_IEEE_FLOAT;
format.wBitsPerSample = 32;
format.nChannels = 1;
format.nSamplesPerSec = 48000;
format.nBlockAlign = (format.wBitsPerSample >> 3) * format.nChannels;
format.nAvgBytesPerSec = format.nBlockAlign * format.nSamplesPerSec;
format.cbSize = 0;
```



<span data-ttu-id="c352d-120">El siguiente paso en la representación del audio espacial consiste en inicializar una secuencia de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="c352d-120">The next step in rendering spatial audio is to initialize a spatial audio stream.</span></span> <span data-ttu-id="c352d-121">En primer lugar, obtenga una instancia de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) mediante una llamada a [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="c352d-121">First, get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="c352d-122">Llame a [**ISpatialAudioClient:: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) para asegurarse de que se admite el formato de audio que está usando.</span><span class="sxs-lookup"><span data-stu-id="c352d-122">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="c352d-123">Cree un evento que la canalización de audio usará para notificar a la aplicación que está preparada para obtener más datos de audio.</span><span class="sxs-lookup"><span data-stu-id="c352d-123">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="c352d-124">Rellene una estructura [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) que se usará para inicializar la secuencia de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="c352d-124">Populate a [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure that will be used to initialize the spatial audio stream.</span></span> <span data-ttu-id="c352d-125">En este ejemplo, el campo **StaticObjectTypeMask** se establece en la constante de **\_ estéreo ChannelMask** definida anteriormente en este artículo, lo que significa que el flujo de audio solo puede usar los canales de la parte delantera derecha e izquierda.</span><span class="sxs-lookup"><span data-stu-id="c352d-125">In this example, the **StaticObjectTypeMask** field is set to the **ChannelMask\_Stereo** constant defined previously in this article, meaning that only the front right and left channels can be used by the audio stream.</span></span> <span data-ttu-id="c352d-126">Dado que en este ejemplo solo se usan objetos de audio estáticos y ningún objeto dinámico, el campo **MaxDynamicObjectCount** se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="c352d-126">Because this example uses only static audio objects and no dynamic objects, the **MaxDynamicObjectCount** field is set to 0.</span></span> <span data-ttu-id="c352d-127">El campo **categoría** se establece en un miembro de la enumeración de la [**\_ \_ categoría secuencia de audio**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) , que define el modo en que el sistema mezcla el sonido desde esta secuencia con otros orígenes de audio.</span><span class="sxs-lookup"><span data-stu-id="c352d-127">The **Category** field is set to a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration, which defines how the system mixes the sound from this stream with other audio sources.</span></span>

<span data-ttu-id="c352d-128">Llame a [**ISpatialAudioClient:: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) para activar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c352d-128">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


```C++
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;

// Activate ISpatialAudioClient on the desired audio-device 
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = ChannelMask_Stereo;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = 0;
streamParams.Category = AudioCategory_SoundEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT activationParams;
PropVariantInit(&activationParams);
activationParams.vt = VT_BLOB;
activationParams.blob.cbSize = sizeof(streamParams);
activationParams.blob.pBlobData = reinterpret_cast<BYTE *>(&streamParams);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;
hr = spatialAudioClient->ActivateSpatialAudioStream(&activationParams, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



> [!Note]  
> <span data-ttu-id="c352d-129">Al usar las interfaces de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) en un título del kit de desarrollo de Xbox One (XDK), primero debe llamar a **EnableSpatialAudio** antes de llamar a [**IMMDeviceEnumerator:: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) o [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="c352d-129">When using the [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interfaces on an Xbox One Development Kit (XDK) title, you must first call **EnableSpatialAudio** before calling [**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) or [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="c352d-130">Si no lo hace, se producirá un \_ error de E NOinterface en la llamada a Activate.</span><span class="sxs-lookup"><span data-stu-id="c352d-130">Failure to do so will result in an E\_NOINTERFACE error being returned from the call to Activate.</span></span> <span data-ttu-id="c352d-131">**EnableSpatialAudio** solo está disponible para los títulos de XDK y no es necesario llamarlo para plataforma universal de Windows aplicaciones que se ejecutan en Xbox One, ni para dispositivos que no son de Xbox One.</span><span class="sxs-lookup"><span data-stu-id="c352d-131">**EnableSpatialAudio** is only available for XDK titles, and does not need to be called for Universal Windows Platform apps running on Xbox One, nor for any non-Xbox One devices.</span></span>

 

<span data-ttu-id="c352d-132">Declare un puntero para un [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) que se usará para escribir datos de audio en un canal estático.</span><span class="sxs-lookup"><span data-stu-id="c352d-132">Declare a pointer for an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) that will be used to write audio data to a static channel.</span></span> <span data-ttu-id="c352d-133">Las aplicaciones típicas usarán un objeto para cada canal especificado en el campo **StaticObjectTypeMask** .</span><span class="sxs-lookup"><span data-stu-id="c352d-133">Typical apps will use an object for each channel specified in the **StaticObjectTypeMask** field.</span></span> <span data-ttu-id="c352d-134">Para simplificar, en este ejemplo solo se usa un único objeto de audio estático.</span><span class="sxs-lookup"><span data-stu-id="c352d-134">For simplicity, this example only uses a single static audio object.</span></span>


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



<span data-ttu-id="c352d-135">Antes de escribir el bucle de representación de audio, llame a [**ISpatialAudioObjectRenderStream:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) para indicar a la canalización multimedia que comience a solicitar datos de audio.</span><span class="sxs-lookup"><span data-stu-id="c352d-135">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span> <span data-ttu-id="c352d-136">En este ejemplo se usa un contador para detener la representación de audio después de 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="c352d-136">This example uses a counter to stop the rendering of audio after 5 seconds.</span></span>

<span data-ttu-id="c352d-137">Dentro del bucle de representación, espere al evento de finalización del búfer, proporcionado cuando se inicializó la secuencia de audio espacial, que se va a señalar.</span><span class="sxs-lookup"><span data-stu-id="c352d-137">Inside the render loop, wait for the buffer completion event, provided when the spatial audio stream was initialized, to be signaled.</span></span> <span data-ttu-id="c352d-138">Debe establecer un límite de tiempo de espera razonable, como 100 MS, al esperar el evento porque cualquier cambio en el tipo de representación o punto de conexión hará que ese evento no se señalice nunca.</span><span class="sxs-lookup"><span data-stu-id="c352d-138">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="c352d-139">En este caso, puede llamar a [**ISpatialAudioObjectRenderStream:: RESET**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) para intentar restablecer la secuencia de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="c352d-139">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="c352d-140">A continuación, llame a [**ISpatialAudioObjectRenderStream:: BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) para que el sistema sepa que está a punto de rellenar los búferes de los objetos de audio con datos.</span><span class="sxs-lookup"><span data-stu-id="c352d-140">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="c352d-141">Este método devuelve el número de objetos de audio dinámicos disponibles, no usados en este ejemplo, y el recuento de fotogramas del búfer para los objetos de audio representados por esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="c352d-141">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="c352d-142">Si aún no se ha creado un objeto de audio espacial estático, cree uno o varios llamando a [**ISpatialAudioObjectRenderStream:: ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), pasando un valor de la enumeración [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) que indica el canal estático en el que se representa el audio del objeto.</span><span class="sxs-lookup"><span data-stu-id="c352d-142">If a static spatial audio object has not yet been created, create one or more by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), passing in a value from the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration indicating the static channel to which the object's audio is rendered.</span></span>

<span data-ttu-id="c352d-143">A continuación, llame a [**ISpatialAudioObject:: getBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) para obtener un puntero al búfer de audio del objeto de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="c352d-143">Next, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="c352d-144">Este método también devuelve el tamaño del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c352d-144">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="c352d-145">En este ejemplo se usa un método auxiliar, **WriteToAudioObjectBuffer**, para rellenar el búfer con datos de audio.</span><span class="sxs-lookup"><span data-stu-id="c352d-145">This example uses a helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="c352d-146">Este método se muestra más adelante en este artículo.</span><span class="sxs-lookup"><span data-stu-id="c352d-146">This method is shown later in this article.</span></span> <span data-ttu-id="c352d-147">Después de escribir en el búfer, el ejemplo comprueba si se ha alcanzado la duración de 5 segundos del objeto y, en caso afirmativo, se llama a [**ISpatialAudioObject:: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) para que la canalización de audio sepa que no se escribirá más audio con este objeto y el objeto se establece en **nullptr** para liberar sus recursos.</span><span class="sxs-lookup"><span data-stu-id="c352d-147">After writing to the buffer, the example checks to see if the 5 second lifetime of the object has been reached, and if so, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="c352d-148">Después de escribir los datos en todos los objetos de audio, llame a [**ISpatialAudioObjectRenderStream:: EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) para que el sistema sepa que los datos están listos para su representación.</span><span class="sxs-lookup"><span data-stu-id="c352d-148">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="c352d-149">Solo se puede llamar a **getBuffer** en una llamada a **BeginUpdatingAudioObjects** y **EndUpdatingAudioObjects**.</span><span class="sxs-lookup"><span data-stu-id="c352d-149">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

// This example will render 5 seconds of audio samples
UINT totalFrameCount = format.nSamplesPerSec * 5;

bool isRendering = true;
while (isRendering)
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        hr = spatialAudioStream->Reset();

        if (hr != S_OK)
        {
            // handle the error
            break;
        }
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of dynamic objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    if (audioObjectFrontLeft == nullptr)
    {
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_FrontLeft, &audioObjectFrontLeft);
        if (hr != S_OK) break;
    }

    // Get the buffer to write audio data
    hr = audioObjectFrontLeft->GetBuffer(&buffer, &bufferLength);

    if (totalFrameCount >= frameCount)
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, 200.0f, format.nSamplesPerSec);

        totalFrameCount -= frameCount;
    }
    else
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), totalFrameCount, 750.0f, format.nSamplesPerSec);

        // Set end of stream for the last buffer 
        hr = audioObjectFrontLeft->SetEndOfStream(totalFrameCount);

        audioObjectFrontLeft = nullptr; // Release the object

        isRendering = false;
    }

    // Let the audio engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
};
```



<span data-ttu-id="c352d-150">Cuando haya terminado de representar el audio espacial, detenga la secuencia de audio espacial mediante una llamada a [**ISpatialAudioObjectRenderStream:: Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span><span class="sxs-lookup"><span data-stu-id="c352d-150">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="c352d-151">Si no va a volver a usar el flujo, libere sus recursos llamando a [**ISpatialAudioObjectRenderStream:: RESET**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span><span class="sxs-lookup"><span data-stu-id="c352d-151">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="c352d-152">El método auxiliar **WriteToAudioObjectBuffer** escribe un búfer completo de muestras o el número de muestras restantes especificado por el límite de tiempo definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c352d-152">The **WriteToAudioObjectBuffer** helper method writes either a full buffer of samples or the number of remaining samples specified by our app-defined time limit.</span></span> <span data-ttu-id="c352d-153">Esto también se puede determinar, por ejemplo, por el número de muestras que quedan en un archivo de audio de origen.</span><span class="sxs-lookup"><span data-stu-id="c352d-153">This could also be determined, for example, by the number of samples remaining in a source audio file.</span></span> <span data-ttu-id="c352d-154">Una onda sin simple, la frecuencia de la que se escala mediante el parámetro de entrada *Frequency* , se genera y se escribe en el búfer.</span><span class="sxs-lookup"><span data-stu-id="c352d-154">A simple sin wave, the frequency of which is scaled by the *frequency* input parameter, is generated and written to the buffer.</span></span>


```C++
void WriteToAudioObjectBuffer(FLOAT* buffer, UINT frameCount, FLOAT frequency, UINT samplingRate)
{
    const double PI = 4 * atan2(1.0, 1.0);
    static double _radPhase = 0.0;

    double step = 2 * PI * frequency / samplingRate;

    for (UINT i = 0; i < frameCount; i++)
    {
        double sample = sin(_radPhase);

        buffer[i] = FLOAT(sample);

        _radPhase += step; // next frame phase

        if (_radPhase >= 2 * PI)
        {
            _radPhase -= 2 * PI;
        }
    }
}
```



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a><span data-ttu-id="c352d-155">Representar audio mediante objetos de audio espacial dinámico</span><span class="sxs-lookup"><span data-stu-id="c352d-155">Render audio using dynamic spatial audio objects</span></span>

<span data-ttu-id="c352d-156">Los objetos dinámicos le permiten representar el audio a partir de una posición arbitraria en el espacio, relativa al usuario.</span><span class="sxs-lookup"><span data-stu-id="c352d-156">Dynamic objects allow you to render audio from an arbitrary position in space, relative to the user.</span></span> <span data-ttu-id="c352d-157">La posición y el volumen de un objeto de audio dinámico se pueden cambiar con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c352d-157">The position and volume of a dynamic audio object can be changed over time.</span></span> <span data-ttu-id="c352d-158">Los juegos utilizarán normalmente la posición de un objeto 3D en el mundo de juego para especificar la posición del objeto de audio dinámico asociado.</span><span class="sxs-lookup"><span data-stu-id="c352d-158">Games will typically use the position of a 3D object in the game world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="c352d-159">En el ejemplo siguiente se utilizará una estructura simple, **My3dObject**, para almacenar el conjunto mínimo de datos necesarios para representar un objeto.</span><span class="sxs-lookup"><span data-stu-id="c352d-159">The following example will use a simple structure, **My3dObject**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="c352d-160">Estos datos incluyen un puntero a un [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), la posición, la velocidad, el volumen y la frecuencia de tono para el objeto, y un valor que almacena el número total de fotogramas para los que el objeto debe representar sonido.</span><span class="sxs-lookup"><span data-stu-id="c352d-160">This data includes a pointer to an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), the position, velocity, volume, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


```C++
struct My3dObject
{
    Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float volume;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



<span data-ttu-id="c352d-161">Los pasos de implementación de los objetos de audio dinámico son en gran medida los mismos pasos para los objetos de audio estáticos descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c352d-161">The implementation steps for dynamic audio objects is largely the same as the steps for static audio objects described above.</span></span> <span data-ttu-id="c352d-162">En primer lugar, obtenga un punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="c352d-162">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="c352d-163">A continuación, inicialice la secuencia de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="c352d-163">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="c352d-164">Obtenga una instancia de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) mediante una llamada a [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="c352d-164">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="c352d-165">Llame a [**ISpatialAudioClient:: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) para asegurarse de que se admite el formato de audio que está usando.</span><span class="sxs-lookup"><span data-stu-id="c352d-165">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="c352d-166">Cree un evento que la canalización de audio usará para notificar a la aplicación que está preparada para obtener más datos de audio.</span><span class="sxs-lookup"><span data-stu-id="c352d-166">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="c352d-167">Llame a [**ISpatialAudioClient:: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) para recuperar el número de objetos dinámicos admitidos por el sistema.</span><span class="sxs-lookup"><span data-stu-id="c352d-167">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="c352d-168">Si esta llamada devuelve 0, los objetos de audio espacial dinámico no se admiten ni se habilitan en el dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="c352d-168">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="c352d-169">Para obtener información sobre cómo habilitar el audio espacial y para obtener detalles sobre el número de objetos de audio dinámicos disponibles para diferentes formatos de audio espacial, consulte el [sonido espacial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="c352d-169">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="c352d-170">Al rellenar la estructura [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) , establezca el campo **MaxDynamicObjectCount** en el número máximo de objetos dinámicos que usará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c352d-170">When populating the [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span>

<span data-ttu-id="c352d-171">Llame a [**ISpatialAudioClient:: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) para activar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c352d-171">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

if (maxDynamicObjectCount == 0)
{
    // Dynamic objects are unsupported
    return;
}

// Set the maximum number of dynamic audio objects that will be used
SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;;
hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



<span data-ttu-id="c352d-172">A continuación se ofrece un código específico de la aplicación para admitir este ejemplo, que generará dinámicamente objetos de audio posicionados aleatoriamente y los almacenará en un vector.</span><span class="sxs-lookup"><span data-stu-id="c352d-172">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObject> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-25, 25); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-1, 1); // uniform distribution for random velocity
std::uniform_real_distribution<> vol_dist(0.5, 1.0); // uniform distribution for random volume
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch
int spawnCounter = 0;
```



<span data-ttu-id="c352d-173">Antes de escribir el bucle de representación de audio, llame a [**ISpatialAudioObjectRenderStream:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) para indicar a la canalización multimedia que comience a solicitar datos de audio.</span><span class="sxs-lookup"><span data-stu-id="c352d-173">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="c352d-174">Dentro del bucle de representación, espere a que se produzca el evento de finalización del búfer que se proporcionó cuando se inicializó la secuencia de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="c352d-174">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="c352d-175">Debe establecer un límite de tiempo de espera razonable, como 100 MS, al esperar el evento porque cualquier cambio en el tipo de representación o punto de conexión hará que ese evento no se señalice nunca.</span><span class="sxs-lookup"><span data-stu-id="c352d-175">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="c352d-176">En este caso, puede llamar a [**ISpatialAudioObjectRenderStream:: RESET**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) para intentar restablecer la secuencia de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="c352d-176">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="c352d-177">A continuación, llame a [**ISpatialAudioObjectRenderStream:: BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) para que el sistema sepa que está a punto de rellenar los búferes de los objetos de audio con datos.</span><span class="sxs-lookup"><span data-stu-id="c352d-177">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="c352d-178">Este método devuelve el número de objetos de audio dinámico disponibles y el recuento de fotogramas del búfer para los objetos de audio representados por esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="c352d-178">This method returns the number of available dynamic audio objects and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="c352d-179">Siempre que el contador de generación alcance el valor especificado, se activará un nuevo objeto de audio dinámico llamando a [**ISpatialAudioObjectRenderStream:: ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) especificando [**AudioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span><span class="sxs-lookup"><span data-stu-id="c352d-179">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="c352d-180">Si ya se han asignado todos los objetos de audio dinámicos disponibles, este método devolverá **SPLAUDCLNT \_ E \_ ningún \_ \_ objeto más**.</span><span class="sxs-lookup"><span data-stu-id="c352d-180">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="c352d-181">En este caso, puede elegir liberar uno o más objetos de audio activados previamente en función de su priorización específica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c352d-181">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="c352d-182">Una vez creado el objeto de audio dinámico, se agrega a una nueva estructura **My3dObject** , con los valores de posición, velocidad, volumen y frecuencia aleatorios, que se agregan a la lista de objetos activos.</span><span class="sxs-lookup"><span data-stu-id="c352d-182">After the dynamic audio object has been created, it is added to a new **My3dObject** structure, with randomized position, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="c352d-183">A continuación, recorra en iteración todos los objetos activos, representados en este ejemplo con la estructura **My3dObject** definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c352d-183">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObject** structure.</span></span> <span data-ttu-id="c352d-184">Para cada objeto de audio, llame a [**ISpatialAudioObject:: getBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) para obtener un puntero al búfer de audio del objeto de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="c352d-184">For each audio object, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="c352d-185">Este método también devuelve el tamaño del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c352d-185">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="c352d-186">El método auxiliar, **WriteToAudioObjectBuffer**, para rellenar el búfer con datos de audio.</span><span class="sxs-lookup"><span data-stu-id="c352d-186">The helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="c352d-187">Después de escribir en el búfer, en el ejemplo se actualiza la posición del objeto de audio dinámico llamando a [**ISpatialAudioObject:: SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition).</span><span class="sxs-lookup"><span data-stu-id="c352d-187">After writing to the buffer, the example updates the position of the dynamic audio object by calling [**ISpatialAudioObject::SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition).</span></span> <span data-ttu-id="c352d-188">El volumen del objeto de audio también se puede modificar mediante una llamada a [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume).</span><span class="sxs-lookup"><span data-stu-id="c352d-188">The volume of the audio object can also be modified by calling [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume).</span></span> <span data-ttu-id="c352d-189">Si no actualiza la posición o el volumen del objeto, retendrá la posición y el volumen desde la última vez que se estableció.</span><span class="sxs-lookup"><span data-stu-id="c352d-189">If you don't update the position or volume of the object, it will retain the position and volume from the last time it was set.</span></span> <span data-ttu-id="c352d-190">Si se ha alcanzado la duración definida por la aplicación del objeto, se llama a [**ISpatialAudioObject:: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) para que la canalización de audio sepa que no se escribirá más audio con este objeto y el objeto se establece en **nullptr** para liberar sus recursos.</span><span class="sxs-lookup"><span data-stu-id="c352d-190">If the object's app-defined lifetime has been reached, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="c352d-191">Después de escribir los datos en todos los objetos de audio, llame a [**ISpatialAudioObjectRenderStream:: EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) para que el sistema sepa que los datos están listos para su representación.</span><span class="sxs-lookup"><span data-stu-id="c352d-191">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="c352d-192">Solo se puede llamar a **getBuffer** en una llamada a **BeginUpdatingAudioObjects** y **EndUpdatingAudioObjects**.</span><span class="sxs-lookup"><span data-stu-id="c352d-192">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObject obj = {
                audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(vol_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObject>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;
            it->audioObject->SetVolume(it->volume);

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
} while (objectVector.size() > 0);
```



<span data-ttu-id="c352d-193">Cuando haya terminado de representar el audio espacial, detenga la secuencia de audio espacial mediante una llamada a [**ISpatialAudioObjectRenderStream:: Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span><span class="sxs-lookup"><span data-stu-id="c352d-193">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="c352d-194">Si no va a volver a usar el flujo, libere sus recursos llamando a [**ISpatialAudioObjectRenderStream:: RESET**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span><span class="sxs-lookup"><span data-stu-id="c352d-194">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a><span data-ttu-id="c352d-195">Representar audio mediante objetos de audio espacial dinámico para HRTF</span><span class="sxs-lookup"><span data-stu-id="c352d-195">Render audio using dynamic spatial audio objects for HRTF</span></span>

<span data-ttu-id="c352d-196">Otro conjunto de API, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) y [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), habilitan el audio espacial que usa la función de transferencia relativa a la cabeza (HRTF) de Microsoft para atenuar los sonidos con el fin de simular la posición del emisor en el espacio, en relación con el usuario, que se puede cambiar con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c352d-196">Another set of APIs, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), enable spatial audio that uses Microsoft's Head-relative Transfer Function (HRTF) to attenuate sounds to simulate the emitter's position in space, relative to the user, which can be changed over time.</span></span> <span data-ttu-id="c352d-197">Además de la posición, los objetos de audio de HRTF permiten especificar una orientación en el espacio, un Directivity en el que se emite el sonido, como una forma cónica o cardiode, y un modelo de decadencia cuando el objeto se mueve hacia cerca y más lejos del agente de escucha virtual.</span><span class="sxs-lookup"><span data-stu-id="c352d-197">In addition to position, HRTF audio objects allow you to specify an orientation in space, a directivity in which sound is emitted, such as a cone or cardioid shape, and a decay model as the object moves nearer and further from the virtual listener.</span></span> <span data-ttu-id="c352d-198">Tenga en cuenta que estas interfaces de HRTF solo están disponibles cuando el usuario ha seleccionado Windows Sonic para auriculares como el motor de audio espacial para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c352d-198">Note that these HRTF interfaces are only available when the user has selected Windows Sonic for Headphones as the spatial audio engine for the device.</span></span> <span data-ttu-id="c352d-199">Para obtener información sobre la configuración de un dispositivo para usar Sonic de Windows para auriculares, consulte [sonido espacial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="c352d-199">For information on configuring a device to use Windows Sonic for Headphones, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="c352d-200">Las API [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) y [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) permiten a una aplicación usar explícitamente la ruta de acceso de representación de Windows Sonic para auriculares directamente.</span><span class="sxs-lookup"><span data-stu-id="c352d-200">The [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) APIs allow an application to explicitly use the Windows Sonic for Headphones render path directly.</span></span> <span data-ttu-id="c352d-201">Estas API no admiten formatos de sonido espacial, como Dolby Atmos para Home Theater o Dolby Atmos para auriculares, ni el cambio de formato de salida controlado por el consumidor a través del panel de control de **sonido** ni la reproducción a través de los altavoces.</span><span class="sxs-lookup"><span data-stu-id="c352d-201">These APIs do not support spatial sound formats such as Dolby Atmos for Home Theater or Dolby Atmos for Headphones, nor consumer-controlled output format switching via the **Sound** control panel, nor playback over speakers.</span></span> <span data-ttu-id="c352d-202">Estas interfaces están pensadas para su uso en aplicaciones de Windows Mixed Reality que desean usar Windows Sonic para funciones específicas de auriculares (como valores preestablecidos de entorno y rolloff basados en distancia especificados mediante programación, fuera de las canalizaciones de creación de contenido típicas).</span><span class="sxs-lookup"><span data-stu-id="c352d-202">These interfaces are intended for use in Windows Mixed Reality applications that want to use Windows Sonic for Headphones-specific capabilities (such as environmental presets and distance-based rolloff specified programmatically, outside of typical content authoring pipelines).</span></span> <span data-ttu-id="c352d-203">La mayoría de los juegos y escenarios de realidad virtual preferirán usar [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="c352d-203">Most games and virtual reality scenarios will prefer to use [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) instead.</span></span> <span data-ttu-id="c352d-204">Los pasos de implementación para ambos conjuntos de API son casi idénticos, por lo que es posible implementar tecnologías y cambiar en tiempo de ejecución en función de la característica que esté disponible en el dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="c352d-204">The implementation steps for both API sets are almost identical, so it is possible to implement both technologies and switch at runtime depending on which feature is available on the current device.</span></span>

<span data-ttu-id="c352d-205">Las aplicaciones de realidad mixta usarán normalmente la posición de un objeto 3D en el mundo virtual para especificar la posición del objeto de audio dinámico asociado.</span><span class="sxs-lookup"><span data-stu-id="c352d-205">Mixed-reality apps will typically use the position of a 3D object in the virtual world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="c352d-206">En el ejemplo siguiente se utilizará una estructura simple, **My3dObjectForHrtf**, para almacenar el conjunto mínimo de datos necesarios para representar un objeto.</span><span class="sxs-lookup"><span data-stu-id="c352d-206">The following example will use a simple structure, **My3dObjectForHrtf**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="c352d-207">Estos datos incluyen un puntero a un [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), la posición, la orientación, la velocidad y la frecuencia de tono para el objeto, y un valor que almacena el número total de fotogramas para los que el objeto debe representar sonido.</span><span class="sxs-lookup"><span data-stu-id="c352d-207">This data includes a pointer to an [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), the position, orientation, velocity, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


```C++
struct My3dObjectForHrtf
{
    Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float yRotationRads;
    float deltaYRotation;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



<span data-ttu-id="c352d-208">Los pasos de implementación para objetos de audio HRTF dinámicos son en gran medida los mismos pasos para los objetos de audio dinámico descritos en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="c352d-208">The implementation steps for dynamic HRTF audio objects is largely the same as the steps for dynamic audio objects described in the previous section.</span></span> <span data-ttu-id="c352d-209">En primer lugar, obtenga un punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="c352d-209">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="c352d-210">A continuación, inicialice la secuencia de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="c352d-210">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="c352d-211">Obtenga una instancia de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) mediante una llamada a [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="c352d-211">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="c352d-212">Llame a [**ISpatialAudioClient:: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) para asegurarse de que se admite el formato de audio que está usando.</span><span class="sxs-lookup"><span data-stu-id="c352d-212">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="c352d-213">Cree un evento que la canalización de audio usará para notificar a la aplicación que está preparada para obtener más datos de audio.</span><span class="sxs-lookup"><span data-stu-id="c352d-213">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="c352d-214">Llame a [**ISpatialAudioClient:: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) para recuperar el número de objetos dinámicos admitidos por el sistema.</span><span class="sxs-lookup"><span data-stu-id="c352d-214">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="c352d-215">Si esta llamada devuelve 0, los objetos de audio espacial dinámico no se admiten ni se habilitan en el dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="c352d-215">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="c352d-216">Para obtener información sobre cómo habilitar el audio espacial y para obtener detalles sobre el número de objetos de audio dinámicos disponibles para diferentes formatos de audio espacial, consulte el [sonido espacial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="c352d-216">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="c352d-217">Al rellenar la estructura [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) , establezca el campo **MaxDynamicObjectCount** en el número máximo de objetos dinámicos que usará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c352d-217">When populating the [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span> <span data-ttu-id="c352d-218">Los parámetros de activación de HRTF admiten algunos parámetros adicionales, como [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)y [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), que especifican los valores predeterminados de esta configuración para los nuevos objetos creados a partir de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c352d-218">The activation params for HRTF supports a few additional parameters, such as a [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), a [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), a [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype), and a [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), which specify the default values of these settings for new objects created from the stream.</span></span> <span data-ttu-id="c352d-219">Estos parámetros son opcionales.</span><span class="sxs-lookup"><span data-stu-id="c352d-219">These parameters are optional.</span></span> <span data-ttu-id="c352d-220">Establezca los campos en **nullptr** para no proporcionar valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="c352d-220">Set the fields to **nullptr** to provide no default values.</span></span>

<span data-ttu-id="c352d-221">Llame a [**ISpatialAudioClient:: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) para activar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c352d-221">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStreamForHrtf>  spatialAudioStreamForHrtf;
hr = spatialAudioClient->IsSpatialAudioStreamAvailable(__uuidof(spatialAudioStreamForHrtf), NULL);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

SpatialAudioHrtfActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = NULL;

SpatialAudioHrtfDistanceDecay decayModel;
decayModel.CutoffDistance = 100;
decayModel.MaxGain = 3.98f;
decayModel.MinGain = float(1.58439 * pow(10, -5));
decayModel.Type = SpatialAudioHrtfDistanceDecayType::SpatialAudioHrtfDistanceDecay_NaturalDecay;
decayModel.UnityGainDistance = 1;

streamParams.DistanceDecay = &decayModel;

SpatialAudioHrtfDirectivity directivity;
directivity.Type = SpatialAudioHrtfDirectivityType::SpatialAudioHrtfDirectivity_Cone;
directivity.Scaling = 1.0f;

SpatialAudioHrtfDirectivityCone cone;
cone.directivity = directivity;
cone.InnerAngle = 0.1f;
cone.OuterAngle = 0.2f;

SpatialAudioHrtfDirectivityUnion directivityUnion;
directivityUnion.Cone = cone;
streamParams.Directivity = &directivityUnion;

SpatialAudioHrtfEnvironmentType environment = SpatialAudioHrtfEnvironmentType::SpatialAudioHrtfEnvironment_Large;
streamParams.Environment = &environment;

SpatialAudioHrtfOrientation orientation = { 1,0,0,0,1,0,0,0,1 }; // identity matrix
streamParams.Orientation = &orientation;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStreamForHrtf), (void**)&spatialAudioStreamForHrtf);
```



<span data-ttu-id="c352d-222">A continuación se ofrece un código específico de la aplicación para admitir este ejemplo, que generará dinámicamente objetos de audio posicionados aleatoriamente y los almacenará en un vector.</span><span class="sxs-lookup"><span data-stu-id="c352d-222">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObjectForHrtf> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-10, 10); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-.02, .02); // uniform distribution for random velocity
std::uniform_real_distribution<> yRotation_dist(-3.14, 3.14); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> deltaYRotation_dist(.01, .02); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch

int spawnCounter = 0;
```



<span data-ttu-id="c352d-223">Antes de escribir el bucle de representación de audio, llame a [**ISpatialAudioObjectRenderStreamForHrtf:: Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) para indicar a la canalización multimedia que comience a solicitar datos de audio.</span><span class="sxs-lookup"><span data-stu-id="c352d-223">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStreamForHrtf::Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="c352d-224">Dentro del bucle de representación, espere a que se produzca el evento de finalización del búfer que se proporcionó cuando se inicializó la secuencia de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="c352d-224">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="c352d-225">Debe establecer un límite de tiempo de espera razonable, como 100 MS, al esperar el evento porque cualquier cambio en el tipo de representación o punto de conexión hará que ese evento no se señalice nunca.</span><span class="sxs-lookup"><span data-stu-id="c352d-225">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="c352d-226">En este caso, puede llamar a [**ISpatialAudioRenderStreamForHrtf:: RESET**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) para intentar restablecer la secuencia de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="c352d-226">In this case, you can call [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="c352d-227">A continuación, llame a [**ISpatialAudioRenderStreamForHrtf:: BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) para que el sistema sepa que está a punto de rellenar los búferes de los objetos de audio con datos.</span><span class="sxs-lookup"><span data-stu-id="c352d-227">Next, call [**ISpatialAudioRenderStreamForHrtf::BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="c352d-228">Este método devuelve el número de objetos de audio dinámicos disponibles, no usados en este ejemplo, y el recuento de fotogramas del búfer para los objetos de audio representados por esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="c352d-228">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="c352d-229">Siempre que el contador de generación alcance el valor especificado, se activará un nuevo objeto de audio dinámico llamando a [**ISpatialAudioRenderStreamForHrtf:: ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) especificando [**AudioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span><span class="sxs-lookup"><span data-stu-id="c352d-229">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="c352d-230">Si ya se han asignado todos los objetos de audio dinámicos disponibles, este método devolverá **SPLAUDCLNT \_ E \_ ningún \_ \_ objeto más**.</span><span class="sxs-lookup"><span data-stu-id="c352d-230">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="c352d-231">En este caso, puede elegir liberar uno o más objetos de audio activados previamente en función de su priorización específica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c352d-231">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="c352d-232">Una vez creado el objeto de audio dinámico, se agrega a una nueva estructura **My3dObjectForHrtf** , con los valores de posición, rotación, velocidad, volumen y frecuencia aleatorios, que se agregan a la lista de objetos activos.</span><span class="sxs-lookup"><span data-stu-id="c352d-232">After the dynamic audio object has been created, it is added to a new **My3dObjectForHrtf** structure, with randomized position, rotation, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="c352d-233">A continuación, recorra en iteración todos los objetos activos, representados en este ejemplo con la estructura **My3dObjectForHrtf** definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c352d-233">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObjectForHrtf** structure.</span></span> <span data-ttu-id="c352d-234">Para cada objeto de audio, llame a [**ISpatialAudioObjectForHrtf:: getBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) para obtener un puntero al búfer de audio del objeto de audio espacial.</span><span class="sxs-lookup"><span data-stu-id="c352d-234">For each audio object, call [**ISpatialAudioObjectForHrtf::GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="c352d-235">Este método también devuelve el tamaño del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c352d-235">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="c352d-236">El método auxiliar, **WriteToAudioObjectBuffer**, indicado anteriormente en este artículo, para rellenar el búfer con datos de audio.</span><span class="sxs-lookup"><span data-stu-id="c352d-236">The helper method, **WriteToAudioObjectBuffer**, listed previously in this article, to fill the buffer with audio data.</span></span> <span data-ttu-id="c352d-237">Después de escribir en el búfer, en el ejemplo se actualiza la posición y la orientación del objeto de audio HRTF llamando a [**ISpatialAudioObjectForHrtf:: SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) y [**ISpatialAudioObjectForHrtf:: SetOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation).</span><span class="sxs-lookup"><span data-stu-id="c352d-237">After writing to the buffer, the example updates the position and orientation of the HRTF audio object by calling [**ISpatialAudioObjectForHrtf::SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) and [**ISpatialAudioObjectForHrtf::SetOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation).</span></span> <span data-ttu-id="c352d-238">En este ejemplo, se usa un método auxiliar, **CalculateEmitterConeOrientationMatrix**, para calcular la matriz de orientación en función de la dirección a la que apunta el objeto 3D.</span><span class="sxs-lookup"><span data-stu-id="c352d-238">In this example, a helper method, **CalculateEmitterConeOrientationMatrix**, is used to calculate the orientation matrix given the direction the 3D object is pointing.</span></span> <span data-ttu-id="c352d-239">A continuación se muestra la implementación de este método.</span><span class="sxs-lookup"><span data-stu-id="c352d-239">The implementation of this method is shown below.</span></span> <span data-ttu-id="c352d-240">El volumen del objeto de audio también se puede modificar mediante una llamada a [**ISpatialAudioObjectForHrtf:: SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain).</span><span class="sxs-lookup"><span data-stu-id="c352d-240">The volume of the audio object can also be modified by calling [**ISpatialAudioObjectForHrtf::SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain).</span></span> <span data-ttu-id="c352d-241">Si no actualiza la posición, la orientación o el volumen del objeto, conservará la posición, la orientación y el volumen desde la última vez que se estableció.</span><span class="sxs-lookup"><span data-stu-id="c352d-241">If you don't update the position, orientation, or volume of the object, it will retain the position, orientation, and volume from the last time it was set.</span></span> <span data-ttu-id="c352d-242">Si se ha alcanzado la duración definida por la aplicación del objeto, se llama a [**ISpatialAudioObjectForHrtf:: SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) para que la canalización de audio sepa que no se escribirá más audio con este objeto y el objeto se establece en **nullptr** para liberar sus recursos.</span><span class="sxs-lookup"><span data-stu-id="c352d-242">If the object's app-defined lifetime has been reached, [**ISpatialAudioObjectForHrtf::SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="c352d-243">Después de escribir los datos en todos los objetos de audio, llame a [**ISpatialAudioRenderStreamForHrtf:: EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) para que el sistema sepa que los datos están listos para su representación.</span><span class="sxs-lookup"><span data-stu-id="c352d-243">After writing data to all of your audio objects, call [**ISpatialAudioRenderStreamForHrtf::EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="c352d-244">Solo se puede llamar a **getBuffer** en una llamada a **BeginUpdatingAudioObjects** y **EndUpdatingAudioObjects**.</span><span class="sxs-lookup"><span data-stu-id="c352d-244">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


```C++
// Start streaming / rendering 
hr = spatialAudioStreamForHrtf->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStreamForHrtf->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
        hr = spatialAudioStreamForHrtf->ActivateSpatialAudioObjectForHrtf(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObjectForHrtf obj = { audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(yRotation_dist(gen))),
                static_cast<float>(static_cast<float>(deltaYRotation_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObjectForHrtf>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;


            Windows::Foundation::Numerics::float3 emitterDirection = Windows::Foundation::Numerics::float3(cos(it->yRotationRads), 0, sin(it->yRotationRads));
            Windows::Foundation::Numerics::float3 listenerDirection = Windows::Foundation::Numerics::float3(0, 0, 1);
            DirectX::XMFLOAT4X4 rotationMatrix;

            DirectX::XMMATRIX rotation = CalculateEmitterConeOrientationMatrix(emitterDirection, listenerDirection);
            XMStoreFloat4x4(&rotationMatrix, rotation);

            SpatialAudioHrtfOrientation orientation = {
                rotationMatrix._11, rotationMatrix._12, rotationMatrix._13,
                rotationMatrix._21, rotationMatrix._22, rotationMatrix._23,
                rotationMatrix._31, rotationMatrix._32, rotationMatrix._33
            };

            it->audioObject->SetOrientation(&orientation);
            it->yRotationRads += it->deltaYRotation;

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStreamForHrtf->EndUpdatingAudioObjects();

} while (objectVector.size() > 0);
```



<span data-ttu-id="c352d-245">Cuando haya terminado de representar el audio espacial, detenga la secuencia de audio espacial mediante una llamada a [**ISpatialAudioRenderStreamForHrtf:: Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c352d-245">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioRenderStreamForHrtf::Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)).</span></span> <span data-ttu-id="c352d-246">Si no va a volver a usar el flujo, libere sus recursos llamando a [**ISpatialAudioRenderStreamForHrtf:: RESET**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c352d-246">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="c352d-247">En el ejemplo de código siguiente se muestra la implementación del método auxiliar **CalculateEmitterConeOrientationMatrix** que se usó en el ejemplo anterior para calcular la matriz de orientación en función de la dirección en la que apunta el objeto 3D.</span><span class="sxs-lookup"><span data-stu-id="c352d-247">The following code example shows the implementation of the **CalculateEmitterConeOrientationMatrix** helper method which was used in the example above to calculate the orientation matrix given the direction the 3D object is pointing.</span></span>


```C++
DirectX::XMMATRIX CalculateEmitterConeOrientationMatrix(Windows::Foundation::Numerics::float3 listenerOrientationFront, Windows::Foundation::Numerics::float3 emitterDirection)
{
    DirectX::XMVECTOR vListenerDirection = DirectX::XMLoadFloat3(&listenerOrientationFront);
    DirectX::XMVECTOR vEmitterDirection = DirectX::XMLoadFloat3(&emitterDirection);
    DirectX::XMVECTOR vCross = DirectX::XMVector3Cross(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vDot = DirectX::XMVector3Dot(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vAngle = DirectX::XMVectorACos(vDot);
    float angle = DirectX::XMVectorGetX(vAngle);

    // The angle must be non-zero
    if (fabsf(angle) > FLT_EPSILON)
    {
        // And less than PI
        if (fabsf(angle) < DirectX::XM_PI)
        {
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }

        // If equal to PI, find any other non-collinear vector to generate the perpendicular vector to rotate about
        else
        {
            DirectX::XMFLOAT3 vector = { 1.0f, 1.0f, 1.0f };
            if (listenerOrientationFront.x != 0.0f)
            {
                vector.x = -listenerOrientationFront.x;
            }
            else if (listenerOrientationFront.y != 0.0f)
            {
                vector.y = -listenerOrientationFront.y;
            }
            else // if (_listenerOrientationFront.z != 0.0f)
            {
                vector.z = -listenerOrientationFront.z;
            }
            DirectX::XMVECTOR vVector = DirectX::XMLoadFloat3(&vector);
            vVector = DirectX::XMVector3Normalize(vVector);
            vCross = DirectX::XMVector3Cross(vVector, vEmitterDirection);
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }
    }

    // If the angle is zero, use an identity matrix
    return DirectX::XMMatrixIdentity();
}
```



## <a name="related-topics"></a><span data-ttu-id="c352d-248">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c352d-248">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c352d-249">Sonido espacial</span><span class="sxs-lookup"><span data-stu-id="c352d-249">Spatial Sound</span></span>](spatial-sound.md)
</dt> <dt>

[<span data-ttu-id="c352d-250">**ISpatialAudioClient**</span><span class="sxs-lookup"><span data-stu-id="c352d-250">**ISpatialAudioClient**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[<span data-ttu-id="c352d-251">**ISpatialAudioObject**</span><span class="sxs-lookup"><span data-stu-id="c352d-251">**ISpatialAudioObject**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
