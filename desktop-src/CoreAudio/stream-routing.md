---
description: El enrutamiento de flujos es la capacidad de una aplicación multimedia para cambiar de flujo entre dispositivos con una interrupción mínima en la reproducción o la sesión de captura.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Enrutamiento de flujos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b21cd15a4467cb9b08747119aab999882ae3b5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496349"
---
# <a name="stream-routing"></a><span data-ttu-id="35a35-103">Enrutamiento de flujos</span><span class="sxs-lookup"><span data-stu-id="35a35-103">Stream Routing</span></span>

<span data-ttu-id="35a35-104">El *enrutamiento de flujos* es la capacidad de una aplicación multimedia para cambiar de flujo entre dispositivos con una interrupción mínima en la reproducción o la sesión de captura.</span><span class="sxs-lookup"><span data-stu-id="35a35-104">*Stream routing* is the ability of a media application to switch streams between devices with minimal interruption to the playback or the capture session.</span></span>

<span data-ttu-id="35a35-105">Un equipo puede tener varios dispositivos de representación y captura.</span><span class="sxs-lookup"><span data-stu-id="35a35-105">A computer can have multiple rendering and capture devices.</span></span> <span data-ttu-id="35a35-106">El sistema muestra estos dispositivos en el panel de control **sonidos** .</span><span class="sxs-lookup"><span data-stu-id="35a35-106">The system lists these devices on the **Sounds** control panel.</span></span> <span data-ttu-id="35a35-107">En esta lista, un usuario puede establecer que un dispositivo sea el dispositivo predeterminado para cada rol: reproducción, grabación o los cuatro roles de comunicaciones (representación de la consola, captura de la consola, representación de la comunicación o captura de comunicación).</span><span class="sxs-lookup"><span data-stu-id="35a35-107">From this list, a user can set a device to be the default device for each role: playback, recording, or the four communications roles (console render, console capture, communication render, or communication capture).</span></span> <span data-ttu-id="35a35-108">La lista de dispositivos se puede modificar de forma dinámica, ya que algunos de estos dispositivos pueden estar disponibles temporalmente, por ejemplo, un casco USB.</span><span class="sxs-lookup"><span data-stu-id="35a35-108">The list of devices may be modified dynamically as some of these devices can be available temporarily, for example a USB headset.</span></span> <span data-ttu-id="35a35-109">Cuando hay varios dispositivos disponibles, el usuario puede cambiar el valor predeterminado a otro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35a35-109">When multiple devices are available, the user can change the default to a different device.</span></span> <span data-ttu-id="35a35-110">El usuario también puede cambiar el formato de un dispositivo (velocidad de muestreo, bits por muestra, etc.) en la pestaña **Opciones avanzadas** de las propiedades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35a35-110">The user can also change the format of a device (sample rate, bits per sample, and so on) on the **Advanced** tab for the device properties.</span></span>

<span data-ttu-id="35a35-111">Considere un escenario en el que un usuario selecciona los **oradores** como el dispositivo predeterminado para representar secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="35a35-111">Consider a scenario in which a user selects **Speakers** as the default device for rendering audio streams.</span></span> <span data-ttu-id="35a35-112">Después, el usuario conecta un auricular USB, selecciona el casco como nuevo dispositivo predeterminado y cambia la velocidad de muestra del dispositivo de 44,1 kHz a 48 kHz.</span><span class="sxs-lookup"><span data-stu-id="35a35-112">The user then connects a USB headset, selects the headset as the new default device, and changes the sample rate of the device from 44.1 kHz to 48 kHz.</span></span> <span data-ttu-id="35a35-113">El usuario desea reproducir la secuencia de audio del casco con la nueva velocidad de muestra con una interrupción mínima en la sesión de streaming.</span><span class="sxs-lookup"><span data-stu-id="35a35-113">The user wants to play the audio stream on the headset at the new sample rate with minimal interruption to the streaming session.</span></span>

<span data-ttu-id="35a35-114">En este escenario, hay dos casos en los que la aplicación multimedia debe controlar:</span><span class="sxs-lookup"><span data-stu-id="35a35-114">In this scenario, there are two cases that the media application must handle:</span></span>

-   <span data-ttu-id="35a35-115">La secuencia se debe transferir al nuevo dispositivo predeterminado con una interrupción mínima para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="35a35-115">The stream must be transferred to the new default device with minimal interruption to playback.</span></span>
-   <span data-ttu-id="35a35-116">El nuevo dispositivo debe reanudar la reproducción en el nuevo formato (es decir, el usuario puede cambiar más de la frecuencia de muestreo).</span><span class="sxs-lookup"><span data-stu-id="35a35-116">The new device must resume playback in the new format (that is, the user can change more than the sample rate).</span></span>

<span data-ttu-id="35a35-117">En Windows Vista, para admitir este escenario, la aplicación multimedia tenía que proporcionar la implementación para el enrutamiento de flujo.</span><span class="sxs-lookup"><span data-stu-id="35a35-117">In Windows Vista, to support this scenario, the media application had to provide the implementation for stream routing.</span></span> <span data-ttu-id="35a35-118">La aplicación era responsable de terminar los flujos existentes y reiniciar las secuencias en el nuevo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35a35-118">The application was responsible for terminating existing streams and restarting the streams on the new device.</span></span> <span data-ttu-id="35a35-119">Si el usuario cambió el dispositivo predeterminado o su formato de combinación cambió, se cerrarán todas las sesiones asociadas y la aplicación tenía que administrar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="35a35-119">If the user changed the default device or its mix format changed, then all of the associated sessions were closed and the application had to handle the recovery.</span></span>

<span data-ttu-id="35a35-120">En Windows 7, una aplicación puede transferir sin problemas un flujo desde un dispositivo predeterminado existente a un nuevo punto de conexión de audio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="35a35-120">In Windows 7, an application can seamlessly transfer a stream from an existing default device to a new default audio endpoint.</span></span> <span data-ttu-id="35a35-121">Los conjuntos de API de audio de alto nivel como Media Foundation, DirectSound y las API de WAVE implementan la característica de enrutamiento de flujo.</span><span class="sxs-lookup"><span data-stu-id="35a35-121">High-level audio API sets such as Media Foundation, DirectSound, and WAVE APIs implement the stream routing feature.</span></span> <span data-ttu-id="35a35-122">Las aplicaciones multimedia que usan estos conjuntos de API para reproducir o capturar una secuencia desde el dispositivo predeterminado usan la implementación predeterminada y no tendrán que modificar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="35a35-122">Media applications that use these API sets to play or capture a stream from the default device use the default implementation and will not have to modify the application.</span></span> <span data-ttu-id="35a35-123">Sin embargo, si la aplicación multimedia usa MMDeviceAPI o WASAPI directamente, la aplicación debe proporcionar la implementación de enrutamiento de flujo.</span><span class="sxs-lookup"><span data-stu-id="35a35-123">However, if your media application uses MMDeviceAPI or WASAPI directly, the application needs to provide the stream routing implementation.</span></span>

> [!Note]  
> <span data-ttu-id="35a35-124">MMDeviceAPI y WASAPI son componentes principales de la API de audio que una aplicación puede usar para representar o capturar un flujo en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35a35-124">MMDeviceAPI and WASAPI are Core Audio API components that an application can use to render or capture a stream on a device.</span></span> <span data-ttu-id="35a35-125">El MMDeviceAPI detecta el nuevo dispositivo de punto de conexión de audio y WASAPI administra el flujo de datos de audio entre una aplicación multimedia y el dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="35a35-125">The MMDeviceAPI discovers the new audio endpoint device, and WASAPI manages the flow of audio data between a media application and the audio endpoint device.</span></span>

 

<span data-ttu-id="35a35-126">Para implementar la característica de enrutamiento de flujo, la aplicación debe escuchar las notificaciones enviadas por MMDeviceAPI y WASAPI cuando:</span><span class="sxs-lookup"><span data-stu-id="35a35-126">To implement the stream routing feature, the application must listen for the notifications sent by MMDeviceAPI and WASAPI when:</span></span>

-   <span data-ttu-id="35a35-127">El usuario cambia el dispositivo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="35a35-127">The default device is changed by the user.</span></span>
-   <span data-ttu-id="35a35-128">Se quita el dispositivo predeterminado existente y se agrega un nuevo dispositivo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="35a35-128">The existing default device is removed and a new default device is added.</span></span>
-   <span data-ttu-id="35a35-129">Se cambia el formato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35a35-129">The device format is changed.</span></span>

<span data-ttu-id="35a35-130">Al controlar estas notificaciones, una aplicación puede realizar las operaciones necesarias de administración de transmisiones mientras se transfiere el flujo al nuevo dispositivo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="35a35-130">By handling these notifications, an application can perform the necessary stream management operations while transferring the stream to the new default device.</span></span> <span data-ttu-id="35a35-131">Además, la aplicación puede representar o capturar las secuencias existentes utilizando el nuevo formato especificado por el usuario mientras una sesión de representación está activa.</span><span class="sxs-lookup"><span data-stu-id="35a35-131">In addition, the application can render or capture existing streams by using the new format specified by the user while a rendering session is active.</span></span>

<span data-ttu-id="35a35-132">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="35a35-132">This section contains the following topics:</span></span>

-   [<span data-ttu-id="35a35-133">Obtención del punto de conexión del dispositivo para el enrutamiento de flujo</span><span class="sxs-lookup"><span data-stu-id="35a35-133">Getting the Device Endpoint for Stream Routing</span></span>](getting-the-default-device-endpoint-for-stream-routing.md)
-   [<span data-ttu-id="35a35-134">Notificaciones relevantes para el enrutamiento de flujos</span><span class="sxs-lookup"><span data-stu-id="35a35-134">Relevant Notifications for Stream Routing</span></span>](relevant-device-notifications-for-stream-routing.md)
-   [<span data-ttu-id="35a35-135">Consideraciones de implementación de enrutamiento de flujo</span><span class="sxs-lookup"><span data-stu-id="35a35-135">Stream Routing Implementation Considerations</span></span>](stream-routing-implementation-considerations.md)

<span data-ttu-id="35a35-136">En los siguientes ejemplos, incluidos en el Windows SDK, se muestra cómo una aplicación puede controlar las notificaciones de enrutamiento de flujo.</span><span class="sxs-lookup"><span data-stu-id="35a35-136">The following samples, included in the Windows SDK, demonstrate how an application can handle stream routing notifications.</span></span>

-   [<span data-ttu-id="35a35-137">RenderSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="35a35-137">RenderSharedTimerDriven</span></span>](rendersharedtimerdriven.md)
-   [<span data-ttu-id="35a35-138">RenderSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="35a35-138">RenderSharedEventDriven</span></span>](rendersharedeventdriven.md)
-   [<span data-ttu-id="35a35-139">RenderExclusiveTimerDriven</span><span class="sxs-lookup"><span data-stu-id="35a35-139">RenderExclusiveTimerDriven</span></span>](renderexclusivetimerdriven.md)
-   [<span data-ttu-id="35a35-140">RenderExclusiveEventDriven</span><span class="sxs-lookup"><span data-stu-id="35a35-140">RenderExclusiveEventDriven</span></span>](renderexclusiveeventdriven.md)
-   [<span data-ttu-id="35a35-141">CaptureSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="35a35-141">CaptureSharedTimerDriven</span></span>](capturesharedtimerdriven.md)
-   [<span data-ttu-id="35a35-142">CaptureSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="35a35-142">CaptureSharedEventDriven</span></span>](capturesharedeventdriven.md)

## <a name="related-topics"></a><span data-ttu-id="35a35-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="35a35-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35a35-144">Administración de flujos</span><span class="sxs-lookup"><span data-stu-id="35a35-144">Stream Management</span></span>](stream-management.md)
</dt> <dt>

[<span data-ttu-id="35a35-145">Acerca de la API de MMDevice</span><span class="sxs-lookup"><span data-stu-id="35a35-145">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="35a35-146">Acerca de WASAPI</span><span class="sxs-lookup"><span data-stu-id="35a35-146">About WASAPI</span></span>](wasapi.md)
</dt> </dl>

 

 



