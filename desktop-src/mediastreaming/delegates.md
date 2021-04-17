---
title: Delegados
description: La API de streaming de multimedia proporciona las siguientes funciones de controlador de eventos.
ms.assetid: CDE7B829-D0D1-479D-9B35-4445E711AF58
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23fbf0f44a0822fd0c8914833b0696fcb9aacad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533129"
---
# <a name="delegates"></a><span data-ttu-id="fee45-103">Delegados</span><span class="sxs-lookup"><span data-stu-id="fee45-103">Delegates</span></span>

<span data-ttu-id="fee45-104">La [API de streaming de multimedia](media-streaming-api-portal.md) proporciona las siguientes funciones de controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="fee45-104">The [Media Streaming API](media-streaming-api-portal.md) provides the following event handler functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fee45-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="fee45-105">In this section</span></span>



| <span data-ttu-id="fee45-106">Tema</span><span class="sxs-lookup"><span data-stu-id="fee45-106">Topic</span></span>                                                                                   | <span data-ttu-id="fee45-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fee45-107">Description</span></span>                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fee45-108">[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fee45-108">[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span></span><br/>                   | <span data-ttu-id="fee45-109">Representa la función que controlará el evento [**ConnectionStatusChanged**](connectionstatuschanged.md) , que notifica al cliente los cambios en el estado de conexión de red del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fee45-109">Represents the function that will handle the [**ConnectionStatusChanged**](connectionstatuschanged.md) event which notifies the client of changes in the device s network connection status.</span></span><br/>               |
| <span data-ttu-id="fee45-110">[**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fee45-110">[**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span></span><br/>       | <span data-ttu-id="fee45-111">Representa la función que controlará los eventos [**DeviceArrival**](devicearrival.md) y [**DeviceDeparture**](devicedeparture.md) , que notifican al cliente los cambios en la lista de dispositivos almacenados en caché.</span><span class="sxs-lookup"><span data-stu-id="fee45-111">Represents the function that will handle the [**DeviceArrival**](devicearrival.md) and [**DeviceDeparture**](devicedeparture.md) events which notify the client of changes in the list of cached devices.</span></span><br/> |
| <span data-ttu-id="fee45-112">[**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fee45-112">[**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span></span><br/> | <span data-ttu-id="fee45-113">Representa la función que controlará el evento [**RenderingParametersUpdate**](renderingparametersupdate.md) , que notifica al cliente una actualización a cualquiera de los parámetros de control de representación de DMR.</span><span class="sxs-lookup"><span data-stu-id="fee45-113">Represents the function that will handle the [**RenderingParametersUpdate**](renderingparametersupdate.md) event which notifies the client of an update to any of the DMR s rendering control parameters.</span></span><br/>  |
| <span data-ttu-id="fee45-114">[**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fee45-114">[**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span></span><br/> | <span data-ttu-id="fee45-115">Representa la función que controlará el evento [**TransportParametersUpdate**](transportparametersupdate.md) , que notifica al cliente una actualización a cualquiera de los parámetros de transporte DMR.</span><span class="sxs-lookup"><span data-stu-id="fee45-115">Represents the function that will handle the [**TransportParametersUpdate**](transportparametersupdate.md) event which notifies the client of an update to any of the DMR s transport parameters.</span></span><br/>          |



 

 

