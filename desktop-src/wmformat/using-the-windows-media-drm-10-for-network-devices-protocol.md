---
title: Usar el protocolo DRM 10 de Windows Media para dispositivos de red
description: Usar el protocolo DRM 10 de Windows Media para dispositivos de red
ms.assetid: dec88d72-718c-42ab-8d48-eddf906051ef
keywords:
- Windows Media Format SDK, Windows Media DRM 10 para dispositivos de red
- Windows Media Format SDK, DRM 10 para dispositivos de red
- Advanced Systems Format (ASF), Windows Media DRM 10 para dispositivos de red
- ASF (formato de sistemas avanzados), Windows Media DRM 10 para dispositivos de red
- Advanced Systems Format (ASF), DRM 10 para dispositivos de red
- ASF (formato de sistemas avanzados), DRM 10 para dispositivos de red
- Administración de derechos digitales (DRM), Windows Media DRM 10 para dispositivos de red
- DRM (administración de derechos digitales), Windows Media DRM 10 para dispositivos de red
- Administración de derechos digitales (DRM), DRM 10 para dispositivos de red
- DRM (administración de derechos digitales), DRM 10 para dispositivos de red
- Windows Media DRM 10 para dispositivos de red, protocolos
- DRM 10 para dispositivos de red, protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73908c66dbffe7f50f4f28beb520861611d59962
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357026"
---
# <a name="using-the-windows-media-drm-10-for-network-devices-protocol"></a><span data-ttu-id="5b50a-115">Usar el protocolo DRM 10 de Windows Media para dispositivos de red</span><span class="sxs-lookup"><span data-stu-id="5b50a-115">Using the Windows Media DRM 10 for Network Devices Protocol</span></span>

<span data-ttu-id="5b50a-116">El SDK de Windows Media Format proporciona algunas características para admitir el protocolo de dispositivo de red seguro, Windows Media DRM 10 para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="5b50a-116">The Windows Media Format SDK provides some features to support the secure network device protocol, Windows Media DRM 10 for Network Devices.</span></span> <span data-ttu-id="5b50a-117">Este protocolo define los mensajes que se envían entre un dispositivo de reproducción de medios digitales, como un reproductor de vídeo de un conjunto y el equipo que atiende los datos en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b50a-117">This protocol defines the messages sent between a digital media playback device, such as a set-top video player, and the computer that serves data to the device.</span></span> <span data-ttu-id="5b50a-118">Los datos multimedia enviados entre el servidor y el dispositivo están cifrados para protegerse de la interceptación.</span><span class="sxs-lookup"><span data-stu-id="5b50a-118">The media data sent between server and device is encrypted to protect it from interception.</span></span>

<span data-ttu-id="5b50a-119">La comunicación entre la aplicación y los dispositivos que admiten Windows Media DRM 10 para dispositivos de red puede usar cualquier protocolo de red que prefiera.</span><span class="sxs-lookup"><span data-stu-id="5b50a-119">The communication between your application and devices that support Windows Media DRM 10 for Network Devices can use whatever networking protocols you prefer.</span></span> <span data-ttu-id="5b50a-120">El SDK de Windows Media Format no proporciona ningún objeto que lleve a cabo las comunicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="5b50a-120">The Windows Media Format SDK does not provide any objects that perform the network communications for you.</span></span> <span data-ttu-id="5b50a-121">En su lugar, los objetos de este SDK procesan algunos mensajes de Windows Media DRM 10 para dispositivos de red después de que la aplicación los haya recibido.</span><span class="sxs-lookup"><span data-stu-id="5b50a-121">Instead, the objects of this SDK process some Windows Media DRM 10 for Network Devices messages after your application has received them.</span></span>

<span data-ttu-id="5b50a-122">Las características que admiten Windows Media DRM 10 para dispositivos de red son el registro de dispositivos, la detección de proximidad y la conversión de archivos protegidos con DRM.</span><span class="sxs-lookup"><span data-stu-id="5b50a-122">The features that support Windows Media DRM 10 for Network Devices are device registration, proximity detection, and converting DRM-protected files.</span></span> <span data-ttu-id="5b50a-123">Estas características se describen en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="5b50a-123">These features are described in the following sections.</span></span>



| <span data-ttu-id="5b50a-124">Sección</span><span class="sxs-lookup"><span data-stu-id="5b50a-124">Section</span></span>                                                                                                                                                                          | <span data-ttu-id="5b50a-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b50a-125">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b50a-126">Registro de dispositivos</span><span class="sxs-lookup"><span data-stu-id="5b50a-126">Device Registration</span></span>](device-registration.md)                                                                                                                                   | <span data-ttu-id="5b50a-127">Describe cómo procesar los mensajes de solicitud de registro de los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5b50a-127">Describes how to process registration request messages from devices.</span></span>                                                                       |
| [<span data-ttu-id="5b50a-128">Realización de la detección de proximidad</span><span class="sxs-lookup"><span data-stu-id="5b50a-128">Performing Proximity Detection</span></span>](performing-proximity-detection.md)                                                                                                             | <span data-ttu-id="5b50a-129">Describe el proceso de detección de proximidad.</span><span class="sxs-lookup"><span data-stu-id="5b50a-129">Describes the proximity detection process.</span></span>                                                                                                 |
| [<span data-ttu-id="5b50a-130">Convertir un archivo de DRM-Protected en un flujo de Windows Media DRM 10 para dispositivos de red</span><span class="sxs-lookup"><span data-stu-id="5b50a-130">Converting a DRM-Protected File to a Windows Media DRM 10 for Network Devices Stream</span></span>](converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream.md) | <span data-ttu-id="5b50a-131">Describe cómo convertir un archivo protegido con DRM en una secuencia que se puede enviar a un dispositivo que usa Windows Media DRM 10 para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="5b50a-131">Describes how to convert a DRM-protected file to a stream that can be sent to a device that uses Windows Media DRM 10 for Network Devices.</span></span> |



 

> [!Note]  
> <span data-ttu-id="5b50a-132">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="5b50a-132">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5b50a-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b50a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b50a-134">**Habilitar la compatibilidad con DRM**</span><span class="sxs-lookup"><span data-stu-id="5b50a-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




