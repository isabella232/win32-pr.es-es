---
title: Realización de la detección de proximidad
description: Realización de la detección de proximidad
ms.assetid: 73207c4c-2d8d-4ec3-b3d0-78f55ee0a754
keywords:
- SDK de Windows Media Format, realización de detección de proximidad
- SDK de Windows Media Format, detección de proximidad
- Advanced Systems Format (ASF), realizando la detección de proximidad
- ASF (formato de sistemas avanzados), realizando detección de proximidad
- Advanced Systems Format (ASF), detección de proximidad
- ASF (formato de sistemas avanzados), detección de proximidad
- Administración de derechos digitales (DRM), realización de detección de proximidad
- DRM (administración de derechos digitales), realización de la detección de proximidad
- Administración de derechos digitales (DRM), detección de proximidad
- DRM (administración de derechos digitales), detección de proximidad
- detección de proximidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9628a6c33832b56858e5c457f15fd0935c2c436
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420223"
---
# <a name="performing-proximity-detection"></a><span data-ttu-id="6bb22-114">Realización de la detección de proximidad</span><span class="sxs-lookup"><span data-stu-id="6bb22-114">Performing Proximity Detection</span></span>

<span data-ttu-id="6bb22-115">Antes de poder transmitir datos cifrados a un dispositivo registrado en el protocolo DRM 10 de Windows Media para dispositivos de red, debe realizar un proceso denominado detección de proximidad (también denominado validación).</span><span class="sxs-lookup"><span data-stu-id="6bb22-115">Before you can stream encrypted data to a registered device in the Windows Media DRM 10 for Network Devices protocol, you must perform a process called proximity detection (also called validation).</span></span> <span data-ttu-id="6bb22-116">Este proceso implica el envío de mensajes al dispositivo y la recepción de respuestas.</span><span class="sxs-lookup"><span data-stu-id="6bb22-116">This process involves sending messages to the device and receiving responses.</span></span> <span data-ttu-id="6bb22-117">El tiempo que se tarda en recibir una respuesta se usa para determinar si el dispositivo está lo suficientemente cerca del equipo en la red para recibir datos seguros.</span><span class="sxs-lookup"><span data-stu-id="6bb22-117">The time it takes to receive a response is used to determine whether the device is "near" enough to the computer on the network to receive secure data.</span></span> <span data-ttu-id="6bb22-118">La confirmación de que el dispositivo está físicamente cerca del equipo cliente en la red ayuda a evitar la suplantación de identidad y otro acceso no autorizado.</span><span class="sxs-lookup"><span data-stu-id="6bb22-118">Confirming that the device is physically close to the client computer on the network helps to prevent spoofing and other unauthorized access.</span></span>

<span data-ttu-id="6bb22-119">Cuando la detección de proximidad se completa correctamente, se dice que el dispositivo es válido.</span><span class="sxs-lookup"><span data-stu-id="6bb22-119">When proximity detection is successfully completed, the device is said to be valid.</span></span> <span data-ttu-id="6bb22-120">Puede comprobar si un dispositivo es válido llamando al método [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) .</span><span class="sxs-lookup"><span data-stu-id="6bb22-120">You can check whether a device is valid by calling the [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) method.</span></span> <span data-ttu-id="6bb22-121">Los dispositivos deben validarse cada 48 horas.</span><span class="sxs-lookup"><span data-stu-id="6bb22-121">Devices must be validated every 48 hours.</span></span> <span data-ttu-id="6bb22-122">Un dispositivo que se validó más de 48 horas antes de que se ejecute el programa debe volver a validarse realizando de nuevo el proceso de detección de proximidad.</span><span class="sxs-lookup"><span data-stu-id="6bb22-122">A device that was validated more than 48 hours before your program runs must be revalidated by performing the proximity detection process again.</span></span>

<span data-ttu-id="6bb22-123">Para realizar la detección de proximidad, debe establecer comunicaciones con el dispositivo y, a continuación, llamar al método [**IWMProximityDetection:: StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) .</span><span class="sxs-lookup"><span data-stu-id="6bb22-123">To perform proximity detection, you must establish communications with the device and then call the [**IWMProximityDetection::StartDetection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmproximitydetection-startdetection) method.</span></span> <span data-ttu-id="6bb22-124">Los componentes de DRM internos del SDK de Windows Media Format completan el proceso de detección de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="6bb22-124">The detection process is completed asynchronously by the internal DRM components of the Windows Media Format SDK.</span></span> <span data-ttu-id="6bb22-125">La aplicación debe incluir una implementación de la interfaz [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) para procesar los mensajes de detección de proximidad.</span><span class="sxs-lookup"><span data-stu-id="6bb22-125">Your application must include an implementation of the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface to process proximity detection messages.</span></span>

<span data-ttu-id="6bb22-126">Hay dos mensajes que se envían mediante el proceso de detección de proximidad: un mensaje de resultado y un mensaje de finalización.</span><span class="sxs-lookup"><span data-stu-id="6bb22-126">There are two messages that are sent by the proximity detection process: a result message and a completion message.</span></span>

<span data-ttu-id="6bb22-127">El mensaje de resultado, el resultado de proximidad de WMT \_ \_ , se envía cuando se completa el proceso de detección.</span><span class="sxs-lookup"><span data-stu-id="6bb22-127">The result message, WMT\_PROXIMITY\_RESULT, is sent when the detection process is completed.</span></span> <span data-ttu-id="6bb22-128">El parámetro *HR* del método de devolución de llamada de [**Estado**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) indica si el dispositivo se ha encontrado lo suficientemente cerca del equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="6bb22-128">The *hr* parameter of the [**OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method indicates whether the device was found to be near enough to the client computer.</span></span> <span data-ttu-id="6bb22-129">Si el parámetro *HR* del mensaje de resultado indica que la operación se ha realizado correctamente, el parámetro *PValue* contiene un **valor DWORD** que especifica la latencia medida para el dispositivo en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="6bb22-129">If the *hr* parameter of the result message indicates success, the *pValue* parameter contains a **DWORD** specifying the measured latency to the device in milliseconds.</span></span>

<span data-ttu-id="6bb22-130">\_ \_ Cuando finaliza la detección, se envía el mensaje de finalización de la proximidad de WMT.</span><span class="sxs-lookup"><span data-stu-id="6bb22-130">The completion message, WMT\_PROXIMITY\_COMPLETED, is sent when the detection is finalized.</span></span> <span data-ttu-id="6bb22-131">Solo debe liberar la interfaz [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) después de recibir este mensaje.</span><span class="sxs-lookup"><span data-stu-id="6bb22-131">You should release the [**IWMProximityDetection**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) interface only after receiving this message.</span></span>

<span data-ttu-id="6bb22-132">Cuando la detección de proximidad de un dispositivo se realiza correctamente, la base de datos de registro de dispositivos se actualiza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="6bb22-132">When proximity detection for a device succeeds, the device registration database is automatically updated.</span></span> <span data-ttu-id="6bb22-133">Las llamadas subsiguientes a [**IWMRegisteredDevice:: IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) devolverán **true** hasta que hayan transcurrido 48 horas y se deba volver a validar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6bb22-133">Subsequent calls to [**IWMRegisteredDevice::IsValid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid) will return **TRUE** until 48 hours have passed and the device needs to be revalidated.</span></span>

<span data-ttu-id="6bb22-134">**Nota:** DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="6bb22-134">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bb22-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6bb22-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bb22-136">**Usar el protocolo DRM 10 de Windows Media para dispositivos de red**</span><span class="sxs-lookup"><span data-stu-id="6bb22-136">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




