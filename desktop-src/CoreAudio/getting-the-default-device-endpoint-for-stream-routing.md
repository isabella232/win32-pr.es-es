---
description: En Windows 7, las API de plataforma de alto nivel que usan las API de audio principales como Media Foundation, DirectSound y las API de Wave, implementan la característica de enrutamiento de flujo mediante la administración del cambio de flujo desde un dispositivo existente a un nuevo punto de conexión de audio predeterminado.
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: Obtención del punto de conexión del dispositivo para el enrutamiento de flujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed8c7546c2bd7437ed9705dc93c2a736bbb64e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907269"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a><span data-ttu-id="a7164-103">Obtención del punto de conexión del dispositivo para el enrutamiento de flujo</span><span class="sxs-lookup"><span data-stu-id="a7164-103">Getting the Device Endpoint for Stream Routing</span></span>

<span data-ttu-id="a7164-104">En Windows 7, las API de plataforma de alto nivel que usan las API de audio principales como Media Foundation, DirectSound y las API de Wave, implementan la característica de enrutamiento de flujo mediante la administración del cambio de flujo desde un dispositivo existente a un nuevo punto de conexión de audio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a7164-104">In Windows 7, high-level platform APIs that use Core Audio APIs such as Media Foundation, DirectSound, and Wave APIs, implement the stream routing feature by handling stream switching from an existing device to a new default audio endpoint.</span></span> <span data-ttu-id="a7164-105">Las aplicaciones multimedia que usan estas API (por ejemplo, una aplicación que activa un objeto **IDirectSound** o **IBaseFilter** en un objeto [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) ) usan el comportamiento de enrutamiento de flujo sin modificaciones en el origen.</span><span class="sxs-lookup"><span data-stu-id="a7164-105">Media applications that use these APIs (for example, an application activating an **IDirectSound** or **IBaseFilter** object on an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object) use the stream routing behavior without any modifications to the source.</span></span>

<span data-ttu-id="a7164-106">Las API de alto nivel implementan el enrutamiento de flujos para el punto de conexión de dispositivo que se obtiene a través de [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="a7164-106">The high-level APIs implement stream routing for the device endpoint that is obtained through [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="a7164-107">Si una aplicación se transmite al dispositivo predeterminado, la característica de enrutamiento de flujo funciona como se define.</span><span class="sxs-lookup"><span data-stu-id="a7164-107">If an application streams to the default device, the stream routing feature operates as defined.</span></span> <span data-ttu-id="a7164-108">Los flujos no se cambian al nuevo dispositivo si lo recupera cualquier otro mecanismo, aunque sea el mismo que el dispositivo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a7164-108">Streams are not switched to the new device if it is retrieved by any other mechanism even if it is the same as the default device.</span></span>

<span data-ttu-id="a7164-109">Una aplicación multimedia que usa las API de audio principales directamente (cliente WASAPI) puede proporcionar una implementación de enrutamiento de flujo personalizado para cualquier dispositivo de representación o captura.</span><span class="sxs-lookup"><span data-stu-id="a7164-109">A media application that uses Core Audio APIs directly (WASAPI client) can provide a custom stream routing implementation for any rendering or capture device.</span></span> <span data-ttu-id="a7164-110">Un cliente de WASAPI puede replicar la implementación proporcionada por las API de alto nivel mediante su restricción a las secuencias que se abren en los dispositivos que se establecen como el dispositivo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a7164-110">A WASAPI client can replicate the implemetation provided by the high-level APIs by restricting it to streams that are opened on devices that are set as the default device.</span></span> <span data-ttu-id="a7164-111">Para obtener una referencia al punto de conexión del dispositivo predeterminado, el cliente debe llamar a [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="a7164-111">To get a reference to the default device's endpoint, the client must call [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="a7164-112">En esta llamada, el cliente debe indicar si requiere un puntero al dispositivo predeterminado de representación o el dispositivo predeterminado de captura especificando el parámetro *DataFlow* .</span><span class="sxs-lookup"><span data-stu-id="a7164-112">In this call, the client must indicate whether it requires a pointer to the rendering default device or the capture default device by specifying the *dataFlow* parameter.</span></span> <span data-ttu-id="a7164-113">El cliente también debe especificar el rol adecuado para el punto de conexión en el atributo **ERole** (**eConsole** o **eCommunications**).</span><span class="sxs-lookup"><span data-stu-id="a7164-113">The client must also specify the appropriate role for the endpoint in the **ERole** attribute (**eConsole** or **eCommunications**).</span></span> <span data-ttu-id="a7164-114">No use **eMultimedia**.</span><span class="sxs-lookup"><span data-stu-id="a7164-114">Do not use **eMultimedia**.</span></span>

<span data-ttu-id="a7164-115">Si la aplicación se transmite a cualquier otro dispositivo, la aplicación puede obtener el dispositivo mediante la especificación de una cadena de identificador de punto de conexión (mediante una llamada a [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).</span><span class="sxs-lookup"><span data-stu-id="a7164-115">If the application streams to any other device, the application can get the device by specifying an endpoint ID string (by calling [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)).</span></span>

<span data-ttu-id="a7164-116">Una vez identificado el dispositivo, el cliente de WASAPI puede proporcionar la implementación para el enrutamiento de flujo mediante el control de las notificaciones de sesión de dispositivo y de audio enviadas para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a7164-116">After the device is identified, the WASAPI client can provide the implementation for stream routing by handling the device and audio session notifications sent for the device.</span></span> <span data-ttu-id="a7164-117">Para obtener más información sobre estas notificaciones, consulte [notificaciones relevantes para el enrutamiento de flujos](relevant-device-notifications-for-stream-routing.md).</span><span class="sxs-lookup"><span data-stu-id="a7164-117">For more information about these notifications, see [Relevant Notifications for Stream Routing](relevant-device-notifications-for-stream-routing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7164-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a7164-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7164-119">Acerca de la API de MMDevice</span><span class="sxs-lookup"><span data-stu-id="a7164-119">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="a7164-120">Acerca de WASAPI</span><span class="sxs-lookup"><span data-stu-id="a7164-120">About WASAPI</span></span>](wasapi.md)
</dt> <dt>

[<span data-ttu-id="a7164-121">Enrutamiento de flujos</span><span class="sxs-lookup"><span data-stu-id="a7164-121">Stream Routing</span></span>](stream-routing.md)
</dt> </dl>

 

 



