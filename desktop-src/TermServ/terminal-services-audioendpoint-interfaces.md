---
title: Interfaces de Servicios de Escritorio remoto AudioEndpoint
description: Las interfaces siguientes se usan con la API de AudioEndpoint.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de520571c99bf84472760e8a1ca28a52a1d6c32e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685508"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a><span data-ttu-id="ed547-103">Interfaces de Servicios de Escritorio remoto AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed547-103">Remote Desktop Services AudioEndpoint Interfaces</span></span>

<span data-ttu-id="ed547-104">Las interfaces siguientes se usan con la API de AudioEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ed547-104">The following interfaces are used with the AudioEndpoint API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ed547-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ed547-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ed547-106">**IAudioDeviceEndpoint**</span><span class="sxs-lookup"><span data-stu-id="ed547-106">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

<span data-ttu-id="ed547-107">Inicializa un objeto de punto de conexión de dispositivo y obtiene las funciones del dispositivo que representa.</span><span class="sxs-lookup"><span data-stu-id="ed547-107">Initializes a device endpoint object and gets the capabilities of the device that it represents.</span></span>

</dd> <dt>

[<span data-ttu-id="ed547-108">**IAudioEndpoint**</span><span class="sxs-lookup"><span data-stu-id="ed547-108">**IAudioEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

<span data-ttu-id="ed547-109">Proporciona información al motor de audio sobre un punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="ed547-109">Provides information to the audio engine about an audio endpoint.</span></span> <span data-ttu-id="ed547-110">Esta interfaz se implementa mediante un punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="ed547-110">This interface is implemented by an audio endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="ed547-111">**IAudioEndpointControl**</span><span class="sxs-lookup"><span data-stu-id="ed547-111">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

<span data-ttu-id="ed547-112">Controla el estado de flujo de un punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="ed547-112">Controls the stream state of an endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="ed547-113">**IAudioEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="ed547-113">**IAudioEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

<span data-ttu-id="ed547-114">Obtiene la diferencia entre las posiciones de lectura y escritura actuales en el búfer del extremo.</span><span class="sxs-lookup"><span data-stu-id="ed547-114">Gets the difference between the current read and write positions in the endpoint buffer.</span></span>

</dd> <dt>

[<span data-ttu-id="ed547-115">**IAudioInputEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="ed547-115">**IAudioInputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

<span data-ttu-id="ed547-116">Obtiene el búfer de entrada para cada paso de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="ed547-116">Gets the input buffer for each processing pass.</span></span>

</dd> <dt>

[<span data-ttu-id="ed547-117">**IAudioOutputEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="ed547-117">**IAudioOutputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

<span data-ttu-id="ed547-118">Obtiene el búfer de salida para cada paso de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="ed547-118">Gets the output buffer for each processing pass.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed547-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed547-119">Remarks</span></span>

<span data-ttu-id="ed547-120">La API de Servicios de Escritorio remoto AudioEndpoint es para su uso en escenarios de Escritorio remoto; no es para las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="ed547-120">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




