---
title: Referencia de la API de Servicios de Escritorio remoto AudioEndpoint
description: Admite interfaces para el registro de puntos de conexión de audio y el transporte de datos.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto, referencia de la API de AudioEndpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1958b21643083a14110ddad77f68024cc464dd36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418952"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a><span data-ttu-id="27bba-104">Referencia de la API de Servicios de Escritorio remoto AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="27bba-104">Remote Desktop Services AudioEndpoint API reference</span></span>

<span data-ttu-id="27bba-105">Un *punto de conexión de audio* representa un dispositivo de audio, una API de audio o cualquier otro origen o receptor de audio, y se usa para enviar datos al motor de audio o consumir datos del mismo.</span><span class="sxs-lookup"><span data-stu-id="27bba-105">An *audio endpoint* represents an audio device, audio API, or any other audio source or sink, and is used to send data to or consume data from the audio engine.</span></span> <span data-ttu-id="27bba-106">Un extremo de audio debe estar conectado al motor de audio a través de una *conexión*, y cada conexión solo puede tener un extremo conectado a él.</span><span class="sxs-lookup"><span data-stu-id="27bba-106">An audio endpoint must be connected to the audio engine through a *connection*, and each connection can have only one endpoint connected to it.</span></span> <span data-ttu-id="27bba-107">Una vez registrado un extremo, el motor de audio conecta el extremo a la conexión.</span><span class="sxs-lookup"><span data-stu-id="27bba-107">After an endpoint is registered, the audio engine attaches the endpoint to the connection.</span></span>

<span data-ttu-id="27bba-108">Cada objeto de extremo debe implementar las interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="27bba-108">Each endpoint object must implement the following interfaces:</span></span>

-   <span data-ttu-id="27bba-109">[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) para permitir que el motor de audio obtenga información sobre el punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="27bba-109">[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) to enable the audio engine to get information about the endpoint.</span></span>
-   <span data-ttu-id="27bba-110">[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) para obtener información sobre el búfer de datos antes de realizar un paso de procesamiento y notificar al punto de conexión la finalización de la fase.</span><span class="sxs-lookup"><span data-stu-id="27bba-110">[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) to get information about the data buffer before performing a processing pass and notifying the endpoint when the pass is complete.</span></span>
-   <span data-ttu-id="27bba-111">La interfaz [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) o [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) , en función de si el objeto de punto de conexión está capturando o representando audio.</span><span class="sxs-lookup"><span data-stu-id="27bba-111">Either the [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) or [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) interface, depending on whether the endpoint object is capturing or rendering audio.</span></span>
-   [<span data-ttu-id="27bba-112">**IAudioDeviceEndpoint**</span><span class="sxs-lookup"><span data-stu-id="27bba-112">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [<span data-ttu-id="27bba-113">**IAudioEndpointControl**</span><span class="sxs-lookup"><span data-stu-id="27bba-113">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

<span data-ttu-id="27bba-114">El motor de audio usa estas interfaces para obtener información sobre los puntos de conexión que están asociados al motor.</span><span class="sxs-lookup"><span data-stu-id="27bba-114">The audio engine uses these interfaces to get information about the endpoints that are attached to the engine.</span></span> <span data-ttu-id="27bba-115">La implementación del punto de conexión debe proporcionar el mecanismo para enviar o consumir datos del motor de acuerdo con lo especificado en estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="27bba-115">The endpoint implementation must provide the mechanism to deliver data to or consume data from the engine as specified by these interfaces.</span></span>

<span data-ttu-id="27bba-116">La API de Servicios de Escritorio remoto AudioEndpoint admite tipos de enumeración, interfaces y estructuras.</span><span class="sxs-lookup"><span data-stu-id="27bba-116">The Remote Desktop Services AudioEndpoint API supports enumeration types, interfaces, and structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="27bba-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="27bba-117">In this section</span></span>

-   [<span data-ttu-id="27bba-118">Servicios de Escritorio remoto tipos de enumeración AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="27bba-118">Remote Desktop Services AudioEndpoint Enumeration Types</span></span>](terminal-services-audioendpoint-enumeration-types.md)
-   [<span data-ttu-id="27bba-119">Servicios de Escritorio remoto funciones AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="27bba-119">Remote Desktop Services AudioEndpoint Functions</span></span>](remote-desktop-services-audioendpoint-functions.md)
-   [<span data-ttu-id="27bba-120">Interfaces de Servicios de Escritorio remoto AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="27bba-120">Remote Desktop Services AudioEndpoint Interfaces</span></span>](terminal-services-audioendpoint-interfaces.md)
-   [<span data-ttu-id="27bba-121">Servicios de Escritorio remoto estructuras AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="27bba-121">Remote Desktop Services AudioEndpoint Structures</span></span>](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a><span data-ttu-id="27bba-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27bba-122">Remarks</span></span>

<span data-ttu-id="27bba-123">La API de Servicios de Escritorio remoto AudioEndpoint es para su uso en escenarios de Escritorio remoto; no es para las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="27bba-123">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




