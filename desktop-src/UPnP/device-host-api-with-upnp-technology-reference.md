---
title: Referencia de API de host de dispositivo
description: Las siguientes interfaces forman parte de la API del host del dispositivo con la tecnología UPnP. El host de dispositivo con tecnología UPnP admite Microsoft Visual Basic y C++.
ms.assetid: 48e20a09-7e78-4b8d-aa16-78751b6fb586
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f42b43efcc1d51eb5e5581770260238640469
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418950"
---
# <a name="device-host-api-reference"></a><span data-ttu-id="f05d6-104">Referencia de API de host de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f05d6-104">Device Host API Reference</span></span>

<span data-ttu-id="f05d6-105">Las siguientes interfaces forman parte de la API del host del dispositivo con la tecnología UPnP.</span><span class="sxs-lookup"><span data-stu-id="f05d6-105">The following interfaces are part of the Device Host API with UPnP technology.</span></span> <span data-ttu-id="f05d6-106">El host de dispositivo con tecnología UPnP admite Microsoft Visual Basic y C++.</span><span class="sxs-lookup"><span data-stu-id="f05d6-106">The Device Host with UPnP technology supports Microsoft Visual Basic and C++.</span></span>

<span data-ttu-id="f05d6-107">Esta API no proporciona compatibilidad con Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="f05d6-107">This API does not provide support for Microsoft Visual Basic Scripting Edition (VBScript).</span></span>



| <span data-ttu-id="f05d6-108">Interfaz</span><span class="sxs-lookup"><span data-stu-id="f05d6-108">Interface</span></span>                                                  | <span data-ttu-id="f05d6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f05d6-109">Description</span></span>                                                                                         |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f05d6-110">**IUPnPDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="f05d6-110">**IUPnPDeviceControl**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol)           | <span data-ttu-id="f05d6-111">Lo usa el host de dispositivo para administrar dispositivos y servicios relacionados.</span><span class="sxs-lookup"><span data-stu-id="f05d6-111">Used by the device host to manage devices and related services.</span></span>                                     |
| [<span data-ttu-id="f05d6-112">**IUPnPDeviceProvider**</span><span class="sxs-lookup"><span data-stu-id="f05d6-112">**IUPnPDeviceProvider**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider)         | <span data-ttu-id="f05d6-113">Lo usa el host de dispositivo para iniciar y detener proveedores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f05d6-113">Used by the device host to start and stop device providers.</span></span>                                         |
| [<span data-ttu-id="f05d6-114">**IUPnPEventSink**</span><span class="sxs-lookup"><span data-stu-id="f05d6-114">**IUPnPEventSink**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink)                   | <span data-ttu-id="f05d6-115">Lo usan los dispositivos para enviar notificaciones de eventos al host de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f05d6-115">Used by devices to send event notifications to the device host.</span></span>                                     |
| [<span data-ttu-id="f05d6-116">**IUPnPEventSource**</span><span class="sxs-lookup"><span data-stu-id="f05d6-116">**IUPnPEventSource**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource)               | <span data-ttu-id="f05d6-117">Lo usa el host del dispositivo para suscribirse o cancelar la suscripción a eventos proporcionados por el servicio hospedado.</span><span class="sxs-lookup"><span data-stu-id="f05d6-117">Used by the device host to subscribe or unsubscribe to events provided by the hosted service.</span></span>       |
| [<span data-ttu-id="f05d6-118">**IUPnPRegistrar**</span><span class="sxs-lookup"><span data-stu-id="f05d6-118">**IUPnPRegistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar)                   | <span data-ttu-id="f05d6-119">Lo usan los dispositivos para registrarse con el host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f05d6-119">Used by devices to register with the device host.</span></span>                                                   |
| [<span data-ttu-id="f05d6-120">**IUPnPRemoteEndpointInfo**</span><span class="sxs-lookup"><span data-stu-id="f05d6-120">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) | <span data-ttu-id="f05d6-121">Lo usan los dispositivos para obtener información sobre un solicitante (es decir, un punto de control) y la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f05d6-121">Used by devices to obtain information about a requester (that is, a control point) and the request.</span></span> |
| [<span data-ttu-id="f05d6-122">**IUPnPReregistrar**</span><span class="sxs-lookup"><span data-stu-id="f05d6-122">**IUPnPReregistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)               | <span data-ttu-id="f05d6-123">Lo usan los dispositivos para volver a registrar con el host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f05d6-123">Used by devices to re-register with the device host.</span></span>                                                |



 

 

 




