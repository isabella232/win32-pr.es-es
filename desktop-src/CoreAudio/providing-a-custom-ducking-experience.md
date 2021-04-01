---
description: Una aplicación puede optar por no participar en la experiencia de carga predeterminada que controla el sistema y reemplazarla por una implementación personalizada.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Proporcionar un comportamiento personalizado de patos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4051dc7b79f698f10d007beaafa97e90d79f3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153400"
---
# <a name="providing-a-custom-ducking-behavior"></a><span data-ttu-id="217e4-103">Proporcionar un comportamiento personalizado de patos</span><span class="sxs-lookup"><span data-stu-id="217e4-103">Providing a Custom Ducking Behavior</span></span>

<span data-ttu-id="217e4-104">Una aplicación puede optar por no participar en la experiencia de carga [predeterminada](stream-attenuation.md) que controla el sistema y reemplazarla por una implementación personalizada.</span><span class="sxs-lookup"><span data-stu-id="217e4-104">An application can opt out of the [Default Ducking Experience](stream-attenuation.md) handled by the system and replace it with a custom implementation.</span></span>

<span data-ttu-id="217e4-105">Una aplicación puede proporcionar una experiencia personalizada de patos.</span><span class="sxs-lookup"><span data-stu-id="217e4-105">An application can provide a custom ducking experience.</span></span> <span data-ttu-id="217e4-106">Por ejemplo, Windows Media Player proporciona su propia experiencia de pato al pausar el flujo multimedia actual durante una sesión de comunicación y reanudar la reproducción cuando se cierra la sesión.</span><span class="sxs-lookup"><span data-stu-id="217e4-106">For example, Windows Media Player provides its own ducking experience by pausing the current media stream during a communication session and resuming playback when the session is closed.</span></span> <span data-ttu-id="217e4-107">Con Windows SDK ejemplos se incluye una aplicación multimedia de ejemplo que implementa la pato. para obtener más información, vea [DuckingMediaPlayer](duckingmediaplayer.md).</span><span class="sxs-lookup"><span data-stu-id="217e4-107">A sample media application that implements ducking is included with Windows SDK samples; for more information, see [DuckingMediaPlayer](duckingmediaplayer.md).</span></span> <span data-ttu-id="217e4-108">Para simular la experiencia de apertura y cierre de secuencias de comunicación y la generación de eventos de patos, vea [DuckingCaptureSample](duckingcapturesample.md), que también se incluye con Windows SDK ejemplos.</span><span class="sxs-lookup"><span data-stu-id="217e4-108">To simulate the experience of opening and closing communication streams, and generating ducking events, see [DuckingCaptureSample](duckingcapturesample.md), which is also included with Windows SDK samples.</span></span>

<span data-ttu-id="217e4-109">Una aplicación multimedia que reproduzca sonidos que se atenuarán debe ser consciente de las secuencias de comunicación, cuando se abren y cierran en el sistema.</span><span class="sxs-lookup"><span data-stu-id="217e4-109">A media application that plays sounds to be attenuated must be aware of the communication streams, when they are opened and closed in the system.</span></span> <span data-ttu-id="217e4-110">La implementación personalizada se puede proporcionar mediante MediaFoundation, DirectShow o DirectSound, que usan las API de audio principales.</span><span class="sxs-lookup"><span data-stu-id="217e4-110">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="217e4-111">Un cliente de WASAPI directo también puede invalidar el control predeterminado si sabe cuándo se inicia y finaliza la sesión de comunicación.</span><span class="sxs-lookup"><span data-stu-id="217e4-111">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="217e4-112">**Para proporcionar una experiencia de patos personalizada, un cliente de WASAPI debe realizar las siguientes tareas:**</span><span class="sxs-lookup"><span data-stu-id="217e4-112">**To provide a custom ducking experience, a WASAPI client must perform the following tasks:**</span></span>

1.  <span data-ttu-id="217e4-113">Regístrese para recibir eventos de patos del *Administrador de patos*, un componente del sistema de audio que controla las notificaciones relacionadas con los cambios en el flujo de comunicación.</span><span class="sxs-lookup"><span data-stu-id="217e4-113">Register to receive ducking events from the *ducking manager*—a component of the audio system that handles notifications related to communication stream changes.</span></span> <span data-ttu-id="217e4-114">Para obtener más información, [obtenga eventos](handling-audio-ducking-events-from-communication-devices.md)de perdedor.</span><span class="sxs-lookup"><span data-stu-id="217e4-114">For more information, [Getting Ducking Events](handling-audio-ducking-events-from-communication-devices.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="217e4-115">Si el cliente se registra para recibir notificaciones de patos, el administrador de patos deshabilita el comportamiento predeterminado proporcionado por el sistema.</span><span class="sxs-lookup"><span data-stu-id="217e4-115">If the client is gets registered to receive ducking notifications, the ducking manager disables the default behavior provided by the system.</span></span> <span data-ttu-id="217e4-116">Si el comportamiento predeterminado está deshabilitado explícitamente (consulte [deshabilitación de la experiencia predeterminada de la](disabling-the-ducking-experience.md)misma) y el cliente no proporciona un comportamiento de sustitución, la aplicación no experimenta ningún comportamiento de perdedor.</span><span class="sxs-lookup"><span data-stu-id="217e4-116">If the default behavior is disabled explictly (see [Disabling the Default Ducking Experience](disabling-the-ducking-experience.md)) and the client does not provide a substitute behavior, the application does not experience any ducking behavior.</span></span>

     

2.  <span data-ttu-id="217e4-117">Escuche las notificaciones de eventos de pato enviadas por el administrador de patos y realice el comportamiento deseado.</span><span class="sxs-lookup"><span data-stu-id="217e4-117">Listen for the duck event notifications sent by the ducking manager and perform the desired ducking behavior.</span></span> <span data-ttu-id="217e4-118">Para obtener más información sobre la implementación de un comportamiento de patos, consulte [consideraciones de implementación para las notificaciones de patos](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="217e4-118">For more information about implementing a ducking behavior, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="217e4-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="217e4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="217e4-120">Uso de un dispositivo de comunicación</span><span class="sxs-lookup"><span data-stu-id="217e4-120">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="217e4-121">Experiencia predeterminada de los patos</span><span class="sxs-lookup"><span data-stu-id="217e4-121">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="217e4-122">Deshabilitación de la experiencia de patos predeterminada</span><span class="sxs-lookup"><span data-stu-id="217e4-122">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="217e4-123">Consideraciones de implementación para las notificaciones de patos</span><span class="sxs-lookup"><span data-stu-id="217e4-123">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="217e4-124">Obtención de eventos de pato</span><span class="sxs-lookup"><span data-stu-id="217e4-124">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



