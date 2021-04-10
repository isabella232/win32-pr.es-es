---
description: Roles de dispositivo
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: Roles de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7182e3af6bf76af500588546a1b7c0db9eea97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153138"
---
# <a name="device-roles"></a><span data-ttu-id="cd92f-103">Roles de dispositivo</span><span class="sxs-lookup"><span data-stu-id="cd92f-103">Device Roles</span></span>

<span data-ttu-id="cd92f-104">Si un sistema contiene dos o más dispositivos de punto de conexión de representación de audio, es posible que un dispositivo sea el mejor para reproducir un tipo de contenido de audio y que otro dispositivo sea mejor para reproducir otro tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="cd92f-104">If a system contains two or more audio-rendering endpoint devices, then one device might be best for playing one type of audio content, and another device might be best for playing another type of content.</span></span> <span data-ttu-id="cd92f-105">Por ejemplo, si un sistema tiene dos dispositivos de representación, el usuario puede optar por reproducir música en un dispositivo y reproducir sonidos de notificación del sistema en el otro.</span><span class="sxs-lookup"><span data-stu-id="cd92f-105">For example, if a system has two rendering devices, the user might choose to play music on one device and to play system notification sounds on the other.</span></span>

<span data-ttu-id="cd92f-106">Del mismo modo, si un sistema contiene dos o más dispositivos de extremo de captura de audio, es posible que un dispositivo sea el mejor para capturar un tipo de contenido de audio y que otro dispositivo sea el mejor para capturar otro tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="cd92f-106">Similarly, if a system contains two or more audio-capture endpoint devices, then one device might be best for capturing one type of audio content, and another device might be best for capturing another type of content.</span></span> <span data-ttu-id="cd92f-107">Por ejemplo, si un sistema tiene dos dispositivos de captura, el usuario puede optar por grabar música en directo en un dispositivo y usar el otro dispositivo para comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="cd92f-107">For example, if a system has two capture devices, the user might choose to record live music on one device and to use the other device for voice commands.</span></span>

<span data-ttu-id="cd92f-108">Los dispositivos pueden tener tres roles: consola, comunicaciones y multimedia. en la tabla siguiente se describen los roles de dispositivo identificados por las tres constantes (eConsole, eCommunications y eMultimedia) en la enumeración [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .</span><span class="sxs-lookup"><span data-stu-id="cd92f-108">Devices can have three roles: Console, Communications, and Multimedia.The following table describes the device roles identified by the three constants—eConsole, eCommunications, and eMultimedia—in the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration.</span></span>



| <span data-ttu-id="cd92f-109">ERole constante)</span><span class="sxs-lookup"><span data-stu-id="cd92f-109">ERole constant</span></span>  | <span data-ttu-id="cd92f-110">Rol de dispositivo</span><span class="sxs-lookup"><span data-stu-id="cd92f-110">Device role</span></span>                              | <span data-ttu-id="cd92f-111">Ejemplos de representación</span><span class="sxs-lookup"><span data-stu-id="cd92f-111">Rendering examples</span></span>             | <span data-ttu-id="cd92f-112">Ejemplos de captura</span><span class="sxs-lookup"><span data-stu-id="cd92f-112">Capture examples</span></span>                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| <span data-ttu-id="cd92f-113">eConsole</span><span class="sxs-lookup"><span data-stu-id="cd92f-113">eConsole</span></span>        | <span data-ttu-id="cd92f-114">Interacción con el equipo</span><span class="sxs-lookup"><span data-stu-id="cd92f-114">Interaction with the computer</span></span>            | <span data-ttu-id="cd92f-115">Juegos y notificaciones del sistema</span><span class="sxs-lookup"><span data-stu-id="cd92f-115">Games and system notifications</span></span> | <span data-ttu-id="cd92f-116">Comandos de voz</span><span class="sxs-lookup"><span data-stu-id="cd92f-116">Voice commands</span></span>                     |
| <span data-ttu-id="cd92f-117">eCommunications</span><span class="sxs-lookup"><span data-stu-id="cd92f-117">eCommunications</span></span> | <span data-ttu-id="cd92f-118">Comunicaciones de voz con otra persona</span><span class="sxs-lookup"><span data-stu-id="cd92f-118">Voice communications with another person</span></span> | <span data-ttu-id="cd92f-119">Chat y VoIP</span><span class="sxs-lookup"><span data-stu-id="cd92f-119">Chat and VoIP</span></span>                  | <span data-ttu-id="cd92f-120">Chat y VoIP</span><span class="sxs-lookup"><span data-stu-id="cd92f-120">Chat and VoIP</span></span>                      |
| <span data-ttu-id="cd92f-121">eMultimedia</span><span class="sxs-lookup"><span data-stu-id="cd92f-121">eMultimedia</span></span>     | <span data-ttu-id="cd92f-122">Reproducir o grabar contenido de audio</span><span class="sxs-lookup"><span data-stu-id="cd92f-122">Playing or recording audio content</span></span>       | <span data-ttu-id="cd92f-123">Música y películas</span><span class="sxs-lookup"><span data-stu-id="cd92f-123">Music and movies</span></span>               | <span data-ttu-id="cd92f-124">Narración y grabación de música en directo</span><span class="sxs-lookup"><span data-stu-id="cd92f-124">Narration and live music recording</span></span> |



 

<span data-ttu-id="cd92f-125">A un dispositivo de representación o captura determinado se le puede asignar ninguno, uno, algunos o todos los roles de la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="cd92f-125">A particular rendering or capture device might be assigned none, one, some, or all of the roles in the preceding table.</span></span> <span data-ttu-id="cd92f-126">En cualquier momento, cada rol de la tabla se asigna a un solo dispositivo de representación (y solo a uno) y a un solo dispositivo de captura (y solo uno).</span><span class="sxs-lookup"><span data-stu-id="cd92f-126">At any time, each role in the table is assigned to one (and only one) rendering device and to one (and only one) capture device.</span></span> <span data-ttu-id="cd92f-127">Es decir, la asignación de roles a los dispositivos de representación es independiente de la asignación de roles para capturar dispositivos.</span><span class="sxs-lookup"><span data-stu-id="cd92f-127">That is, the assignment of roles to rendering devices is independent of the assignment of roles to capture devices.</span></span>

<span data-ttu-id="cd92f-128">Una aplicación puede optar por reproducir todos los flujos de salida a través de un único dispositivo de punto de conexión de representación y registrar todos sus flujos de entrada desde un único dispositivo de punto de conexión de captura.</span><span class="sxs-lookup"><span data-stu-id="cd92f-128">An application might choose to play all of its output streams through a single rendering endpoint device, and to record all of its input streams from a single capture endpoint device.</span></span> <span data-ttu-id="cd92f-129">Como alternativa, una aplicación puede optar por reproducir algunos de sus flujos de salida a través de un dispositivo de representación y reproducir otros flujos de salida a través de otro dispositivo de representación.</span><span class="sxs-lookup"><span data-stu-id="cd92f-129">Alternatively, an application might choose to play some of its output streams through one rendering device and to play other output streams through another rendering device.</span></span> <span data-ttu-id="cd92f-130">Del mismo modo, podría optar por grabar algunos de sus flujos de entrada a través de un dispositivo de captura y grabar otros flujos de entrada a través de otro dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="cd92f-130">Similarly, it might choose to record some of its input streams through one capture device and to record other input streams through another capture device.</span></span> <span data-ttu-id="cd92f-131">En todos los casos, la aplicación puede asignar cada flujo al dispositivo cuyo rol sea más adecuado para esa secuencia.</span><span class="sxs-lookup"><span data-stu-id="cd92f-131">In all cases, the application can assign each stream to the device whose role is most appropriate for that stream.</span></span>

<span data-ttu-id="cd92f-132">Por ejemplo, una aplicación de VoIP podría asignar el flujo de salida que contiene la notificación de timbre al dispositivo de punto de conexión de representación con el rol eConsole.</span><span class="sxs-lookup"><span data-stu-id="cd92f-132">For example, a VoIP application might assign the output stream that contains the ring-in notification to the rendering endpoint device with the eConsole role.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd92f-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd92f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd92f-134">Dispositivos de punto de conexión de audio</span><span class="sxs-lookup"><span data-stu-id="cd92f-134">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="cd92f-135">Trabajar con roles de dispositivo</span><span class="sxs-lookup"><span data-stu-id="cd92f-135">Working with Device Roles</span></span>](device-roles-in-windows-vista.md)
</dt> <dt>

[<span data-ttu-id="cd92f-136">Interoperabilidad con las API de audio heredadas</span><span class="sxs-lookup"><span data-stu-id="cd92f-136">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



