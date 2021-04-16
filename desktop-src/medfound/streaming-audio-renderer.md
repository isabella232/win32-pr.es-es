---
description: Streaming audio renderer (SAR) es un receptor de medios que representa el audio.
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: Representador de audio de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59c5b55f197d5e9770c6f1be55f680c7f9136f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696674"
---
# <a name="streaming-audio-renderer"></a><span data-ttu-id="00a75-103">Representador de audio de streaming</span><span class="sxs-lookup"><span data-stu-id="00a75-103">Streaming Audio Renderer</span></span>

<span data-ttu-id="00a75-104">Streaming audio renderer (SAR) es un receptor de medios que representa el audio.</span><span class="sxs-lookup"><span data-stu-id="00a75-104">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span> <span data-ttu-id="00a75-105">Cada instancia de SAR representa una secuencia de audio única.</span><span class="sxs-lookup"><span data-stu-id="00a75-105">Each instance of the SAR renders a single audio stream.</span></span> <span data-ttu-id="00a75-106">Para representar varias secuencias, use varias instancias del SAR.</span><span class="sxs-lookup"><span data-stu-id="00a75-106">To render multiple streams, use multiple instances of the SAR.</span></span>

<span data-ttu-id="00a75-107">Para crear el SAR, llame a una de las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="00a75-107">To create the SAR, call either of the following functions:</span></span>

-   <span data-ttu-id="00a75-108">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer).</span><span class="sxs-lookup"><span data-stu-id="00a75-108">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer).</span></span> <span data-ttu-id="00a75-109">Devuelve un puntero al SAR.</span><span class="sxs-lookup"><span data-stu-id="00a75-109">Returns a pointer to the SAR.</span></span>
-   <span data-ttu-id="00a75-110">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate).</span><span class="sxs-lookup"><span data-stu-id="00a75-110">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate).</span></span> <span data-ttu-id="00a75-111">Devuelve un puntero a un objeto de activación, que se puede usar para crear el SAR.</span><span class="sxs-lookup"><span data-stu-id="00a75-111">Returns a pointer to an activation object, which can be used to create the SAR.</span></span>

<span data-ttu-id="00a75-112">La segunda función, que devuelve un objeto de activación, es necesaria si se está reproduciendo contenido protegido, ya que el objeto de activación se debe serializar en el proceso protegido.</span><span class="sxs-lookup"><span data-stu-id="00a75-112">The second function, which returns an activation object, is required if you are playing protected content, because the activation object must be serialized to the protected process.</span></span> <span data-ttu-id="00a75-113">En el caso de contenido sin cifrar, puede usar cualquiera de las dos funciones.</span><span class="sxs-lookup"><span data-stu-id="00a75-113">For clear content, you can use either function.</span></span>

<span data-ttu-id="00a75-114">El SAR puede recibir audio sin comprimir en formato de punto flotante de PCM o IEEE.</span><span class="sxs-lookup"><span data-stu-id="00a75-114">The SAR can receive uncompressed audio in either PCM or IEEE floating-point format.</span></span> <span data-ttu-id="00a75-115">Si la velocidad de reproducción es mayor o menor que 1 ×, el SAR ajusta automáticamente el paso.</span><span class="sxs-lookup"><span data-stu-id="00a75-115">If the playback rate is faster or slower than 1×, the SAR automatically adjusts the pitch.</span></span>

## <a name="configuring-the-audio-renderer"></a><span data-ttu-id="00a75-116">Configuración del representador de audio</span><span class="sxs-lookup"><span data-stu-id="00a75-116">Configuring the Audio Renderer</span></span>

<span data-ttu-id="00a75-117">El SAR admite varios atributos de configuración.</span><span class="sxs-lookup"><span data-stu-id="00a75-117">The SAR supports several configuration attributes.</span></span> <span data-ttu-id="00a75-118">El mecanismo para establecer estos atributos depende de la función a la que llame para crear el SAR.</span><span class="sxs-lookup"><span data-stu-id="00a75-118">The mechanism for setting these attributes depends on which function you call to create the SAR.</span></span> <span data-ttu-id="00a75-119">Si usa la función [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) , haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="00a75-119">If you use the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function, do the following:</span></span>

1.  <span data-ttu-id="00a75-120">Cree un nuevo almacén de atributos mediante una llamada a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="00a75-120">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="00a75-121">Agregue los atributos al almacén de atributos.</span><span class="sxs-lookup"><span data-stu-id="00a75-121">Add the attributes to the attribute store.</span></span>
3.  <span data-ttu-id="00a75-122">Pase el almacén de atributos a la función [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) en el parámetro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="00a75-122">Pass the attribute store to the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function in the *pAudioAttributes* parameter.</span></span>

<span data-ttu-id="00a75-123">Si usa la función [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) , la función devuelve un puntero a la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) en el parámetro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="00a75-123">If you use the [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) function, the function returns a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface in the *ppActivate* parameter.</span></span> <span data-ttu-id="00a75-124">Utilice este puntero para agregar los atributos.</span><span class="sxs-lookup"><span data-stu-id="00a75-124">Use this pointer to add the attributes.</span></span>

<span data-ttu-id="00a75-125">Para obtener una lista de atributos de configuración, vea [atributos de representador de audio](audio-renderer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="00a75-125">For a list of configuration attributes, see [Audio Renderer Attributes](audio-renderer-attributes.md).</span></span>

## <a name="selecting-the-audio-endpoint-device"></a><span data-ttu-id="00a75-126">Selección del dispositivo de extremo de audio</span><span class="sxs-lookup"><span data-stu-id="00a75-126">Selecting the Audio Endpoint Device</span></span>

<span data-ttu-id="00a75-127">Un *dispositivo de punto de conexión de audio* es un dispositivo de hardware que representa o captura audio.</span><span class="sxs-lookup"><span data-stu-id="00a75-127">An *audio endpoint device* is a hardware device that either renders or captures audio.</span></span> <span data-ttu-id="00a75-128">Algunos ejemplos son los altavoces, los auriculares, los micrófonos y los reproductores de CD.</span><span class="sxs-lookup"><span data-stu-id="00a75-128">Examples include speakers, headphones, microphones, and CD players.</span></span> <span data-ttu-id="00a75-129">SAR siempre usa un dispositivo de representación de audio.</span><span class="sxs-lookup"><span data-stu-id="00a75-129">The SAR always uses an audio rendering device.</span></span> <span data-ttu-id="00a75-130">Hay dos maneras de seleccionar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="00a75-130">There are two ways to select the device.</span></span>

<span data-ttu-id="00a75-131">El primer enfoque consiste en enumerar los dispositivos de representación de audio en el sistema mediante la interfaz [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="00a75-131">The first approach is to enumerate the audio rendering devices on the system, using the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="00a75-132">Esta interfaz se documenta en la documentación básica de la API de audio.</span><span class="sxs-lookup"><span data-stu-id="00a75-132">This interface is documented in the core audio API documentation.</span></span>

1.  <span data-ttu-id="00a75-133">Cree el objeto de enumerador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="00a75-133">Create the device enumerator object.</span></span>
2.  <span data-ttu-id="00a75-134">Use el enumerador de dispositivos para enumerar los dispositivos de representación de audio.</span><span class="sxs-lookup"><span data-stu-id="00a75-134">Use the device enumerator to enumerate audio rendering devices.</span></span> <span data-ttu-id="00a75-135">Cada dispositivo se representa mediante un puntero a la interfaz [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) .</span><span class="sxs-lookup"><span data-stu-id="00a75-135">Each device is represented by a pointer to the [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span>
3.  <span data-ttu-id="00a75-136">Seleccione un dispositivo, en función de las propiedades del dispositivo o la selección del usuario.</span><span class="sxs-lookup"><span data-stu-id="00a75-136">Select a device, based on the device properties or the user's selection.</span></span>
4.  <span data-ttu-id="00a75-137">Llame a [**IMMDevice:: getId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obtener el identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="00a75-137">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the device identifier.</span></span>
5.  <span data-ttu-id="00a75-138">Establezca el identificador de dispositivo como el valor del atributo de ID. de [**\_ extremo de \_ atributo de representador \_ \_ \_ de audio MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="00a75-138">Set the device identifier as the value of the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span>

<span data-ttu-id="00a75-139">En lugar de enumerar los dispositivos, puede especificar el dispositivo de audio por su *rol*.</span><span class="sxs-lookup"><span data-stu-id="00a75-139">Rather than enumerate devices, you can specify the audio device by its *role*.</span></span> <span data-ttu-id="00a75-140">Un rol de audio identifica una categoría general de uso.</span><span class="sxs-lookup"><span data-stu-id="00a75-140">An audio role identifies a general category of usage.</span></span> <span data-ttu-id="00a75-141">Por ejemplo, el rol de *consola* se define para juegos y notificaciones del sistema, mientras que el rol *multimedia* se define para música y películas.</span><span class="sxs-lookup"><span data-stu-id="00a75-141">For example, the *console* role is defined for games and system notifications, while the *multimedia* role is defined for music and movies.</span></span> <span data-ttu-id="00a75-142">Cada rol tiene un dispositivo de representación de audio asignado y el usuario puede cambiar estas asignaciones.</span><span class="sxs-lookup"><span data-stu-id="00a75-142">Each role has one audio rendering device assigned to it, and the user can change these assignments.</span></span> <span data-ttu-id="00a75-143">Si especifica un rol de dispositivo, el SAR usa cualquier dispositivo de audio que se haya asignado para ese rol.</span><span class="sxs-lookup"><span data-stu-id="00a75-143">If you specify a device role, the SAR uses whatever audio device has been assigned for that role.</span></span> <span data-ttu-id="00a75-144">Para especificar el rol de dispositivo, establezca el atributo de [**\_ rol de punto de conexión de \_ atributo de representador \_ \_ \_ de audio MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="00a75-144">To specify the device role, set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span>

<span data-ttu-id="00a75-145">Los dos atributos que se enumeran en esta sección son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="00a75-145">The two attributes listed in this section are mutually exclusive.</span></span> <span data-ttu-id="00a75-146">Si no establece ninguno de ellos, el SAR usa el dispositivo de audio que está asignado al rol **eConsole** .</span><span class="sxs-lookup"><span data-stu-id="00a75-146">If you do not set either of them, the SAR uses the audio device that is assigned to the **eConsole** role.</span></span>

<span data-ttu-id="00a75-147">En el código siguiente se enumeran los dispositivos de representación de audio y se asigna el primer dispositivo de la lista al SAR.</span><span class="sxs-lookup"><span data-stu-id="00a75-147">The following code enumerates the audio rendering devices and assigns the first device in the list to the SAR.</span></span> <span data-ttu-id="00a75-148">En este ejemplo se usa la función [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) para crear el SAR.</span><span class="sxs-lookup"><span data-stu-id="00a75-148">This example uses the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function to create the SAR.</span></span>


```C++
#include <mmdeviceapi.h>

HRESULT hr = S_OK;

IMMDeviceEnumerator *pEnum = NULL;      // Audio device enumerator.
IMMDeviceCollection *pDevices = NULL;   // Audio device collection.
IMMDevice *pDevice = NULL;              // An audio device.
IMFAttributes *pAttributes = NULL;      // Attribute store.
IMFMediaSink *pSink = NULL;             // Streaming audio renderer (SAR)

LPWSTR wstrID = NULL;                   // Device ID.

// Create the device enumerator.
hr = CoCreateInstance(
    __uuidof(MMDeviceEnumerator), 
    NULL,
    CLSCTX_ALL, 
    __uuidof(IMMDeviceEnumerator), 
    (void**)&pEnum
    );

// Enumerate the rendering devices.
if (SUCCEEDED(hr))
{
    hr = pEnum->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pDevices);
}

// Get ID of the first device in the list.
if (SUCCEEDED(hr))
{
    hr = pDevices->Item(0, &pDevice);
}

if (SUCCEEDED(hr))
{
    hr = pDevice->GetId(&wstrID);
}

// Create an attribute store and set the device ID attribute.
if (SUCCEEDED(hr))
{
    hr = MFCreateAttributes(&pAttributes, 2);
}

if (SUCCEEDED(hr))
{
    hr = pAttributes->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

// Create the audio renderer.
if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRenderer(pAttributes, &pSink);    
}

SAFE_RELEASE(pEnum);
SAFE_RELEASE(pDevices);
SAFE_RELEASE(pDevice); 
SAFE_RELEASE(pAttributes);
CoTaskMemFree(wstrID);
```



<span data-ttu-id="00a75-149">Para crear el objeto de activación para el SAR, cambie el código que aparece después de la llamada a [**IMMDevice:: getId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="00a75-149">To create the activation object for the SAR, change the code that appears after the call to [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to the following:</span></span>


```C++
IMFActivate *pActivate = NULL;          // Activation object.

if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRendererActivate(&pActivate);    
}

if (SUCCEEDED(hr))
{
    hr = pActivate->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

SAFE_RELEASE(pActivate);
```



## <a name="selecting-the-audio-session"></a><span data-ttu-id="00a75-150">Seleccionar la sesión de audio</span><span class="sxs-lookup"><span data-stu-id="00a75-150">Selecting the Audio Session</span></span>

<span data-ttu-id="00a75-151">Una sesión de audio es un grupo de secuencias de audio relacionadas que una aplicación puede administrar colectivamente.</span><span class="sxs-lookup"><span data-stu-id="00a75-151">An audio session is a group of related audio streams that an application can manage collectively.</span></span> <span data-ttu-id="00a75-152">La aplicación puede controlar el nivel de volumen y silenciar el estado de cada sesión.</span><span class="sxs-lookup"><span data-stu-id="00a75-152">The application can control the volume level and mute state of each session.</span></span> <span data-ttu-id="00a75-153">Las sesiones se identifican mediante un GUID.</span><span class="sxs-lookup"><span data-stu-id="00a75-153">Sessions are identified by GUID.</span></span> <span data-ttu-id="00a75-154">Para especificar la sesión de audio para el SAR, use el atributo de ID. de [ \_ sesión de \_ atributo del representador \_ \_ \_ de audio MF](mf-audio-renderer-attribute-session-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="00a75-154">To specify the audio session for the SAR, use the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID](mf-audio-renderer-attribute-session-id-attribute.md) attribute.</span></span> <span data-ttu-id="00a75-155">Si no se establece este atributo, el SAR se une a la sesión predeterminada para ese proceso, identificado por el **GUID \_ null**.</span><span class="sxs-lookup"><span data-stu-id="00a75-155">If you do not set this attribute, the SAR joins the default session for that process, identified by **GUID\_NULL**.</span></span>

<span data-ttu-id="00a75-156">De forma predeterminada, una sesión de audio es específica del proceso, lo que significa que solo contiene flujos del proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="00a75-156">By default, an audio session is process-specific, meaning it contains only streams from the calling process.</span></span> <span data-ttu-id="00a75-157">Para unirse a una sesión entre procesos, establezca el atributo [MF \_ audio \_ renderer Attribute \_ \_ Flags](mf-audio-renderer-attribute-flags-attribute.md) con el valor **MF \_ audio \_ renderer \_ Attribute \_ Flags \_ CROSSPROCESS**.</span><span class="sxs-lookup"><span data-stu-id="00a75-157">To join a cross-process session, set the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS](mf-audio-renderer-attribute-flags-attribute.md) attribute with the value **MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**.</span></span>

<span data-ttu-id="00a75-158">Después de crear el SAR, use la interfaz [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) para unir la sesión a un grupo de sesiones, todas las cuales están controladas por el mismo control de volumen en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="00a75-158">After you create the SAR, you use the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface to join the session to a group of sessions, all of which are controlled by the same volume control in the control panel.</span></span> <span data-ttu-id="00a75-159">También puede usar esta interfaz para establecer el nombre para mostrar y el icono que aparece en el control de volumen.</span><span class="sxs-lookup"><span data-stu-id="00a75-159">You can also use this interface to set the display name and the icon that appear in the volume control.</span></span>

## <a name="controlling-volume-levels"></a><span data-ttu-id="00a75-160">Controlar los niveles de volumen</span><span class="sxs-lookup"><span data-stu-id="00a75-160">Controlling Volume Levels</span></span>

<span data-ttu-id="00a75-161">Para controlar el nivel de volumen maestro de todas las secuencias de la sesión de audio de SAR, use la interfaz [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) .</span><span class="sxs-lookup"><span data-stu-id="00a75-161">To control the master volume level of all the streams in the SAR's audio session, use the [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) interface.</span></span> <span data-ttu-id="00a75-162">Para controlar el volumen de una secuencia individual, o para controlar el volumen de canales individuales dentro de una secuencia, use la interfaz [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) .</span><span class="sxs-lookup"><span data-stu-id="00a75-162">To control the volume of an individual stream, or to control the volume of individual channels within a stream, use the [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) interface.</span></span> <span data-ttu-id="00a75-163">Ambas interfaces se obtienen mediante una llamada a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice).</span><span class="sxs-lookup"><span data-stu-id="00a75-163">Both interfaces are obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice).</span></span> <span data-ttu-id="00a75-164">Puede llamar a **GetService** directamente en el SAR o llamarlo en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="00a75-164">You can call **GetService** directly on the SAR, or call it on the Media Session.</span></span> <span data-ttu-id="00a75-165">Los niveles de volumen se expresan como valores de atenuación.</span><span class="sxs-lookup"><span data-stu-id="00a75-165">Volume levels are expressed as attenuation values.</span></span> <span data-ttu-id="00a75-166">Para cada canal, el nivel de atenuación es el producto del volumen maestro y el volumen del canal.</span><span class="sxs-lookup"><span data-stu-id="00a75-166">For each channel, the attenuation level is the product of the master volume and the channel volume.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00a75-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00a75-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00a75-168">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="00a75-168">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 
