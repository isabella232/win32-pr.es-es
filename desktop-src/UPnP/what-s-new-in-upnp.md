---
title: Novedades de las API de UPnP
description: Las API de™ UPnP tienen nuevas características y documentación actualizada para Windows XP SP2. En la tabla siguiente se identifica la nueva documentación.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27747c6185b5aecea86e240d388ab10410aa29f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779885"
---
# <a name="whats-new-in-the-upnp-apis"></a><span data-ttu-id="05acb-104">Novedades de las API de UPnP</span><span class="sxs-lookup"><span data-stu-id="05acb-104">What's New in the UPnP APIs</span></span>

<span data-ttu-id="05acb-105">Las API de™ UPnP tienen nuevas características y documentación actualizada para Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="05acb-105">The UPnP™ APIs have new features and updated documentation for Windows XP SP2.</span></span> <span data-ttu-id="05acb-106">En la tabla siguiente se identifica la nueva documentación.</span><span class="sxs-lookup"><span data-stu-id="05acb-106">The following table identifies the new documentation.</span></span>



| <span data-ttu-id="05acb-107">Característica</span><span class="sxs-lookup"><span data-stu-id="05acb-107">Feature</span></span>                                                          | <span data-ttu-id="05acb-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="05acb-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05acb-109">**IUPnPRemoteEndpointInfo**</span><span class="sxs-lookup"><span data-stu-id="05acb-109">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | <span data-ttu-id="05acb-110">Esta nueva interfaz permite a un dispositivo hospedado obtener información sobre un solicitante (es decir, un punto de control) y la solicitud.</span><span class="sxs-lookup"><span data-stu-id="05acb-110">This new interface allows a hosted device to obtain information about a requester (that is, a control point) and the request.</span></span> <span data-ttu-id="05acb-111">Incluye tres métodos, cada uno de los cuales proporciona un tipo de información diferente.</span><span class="sxs-lookup"><span data-stu-id="05acb-111">It includes three methods, each of which provides a different type of information.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="05acb-112">Implementar el comportamiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="05acb-112">Implementing Device Behavior</span></span>](implementing-device-behavior.md) | <span data-ttu-id="05acb-113">En este tema se incluye una nueva sección que explica cómo obtener información del punto de conexión mediante la nueva interfaz [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) .</span><span class="sxs-lookup"><span data-stu-id="05acb-113">This topic includes a new section that explains how to obtain endpoint information by using the new [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="05acb-114">Opciones de configuración</span><span class="sxs-lookup"><span data-stu-id="05acb-114">Configuration Settings</span></span>](configuration-settings.md)             | <span data-ttu-id="05acb-115">Este nuevo tema proporciona información sobre la configuración del registro que afecta al comportamiento de las API de UPnP.</span><span class="sxs-lookup"><span data-stu-id="05acb-115">This new topic provides information about the registry settings that affect the behavior of the UPnP APIs.</span></span>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="05acb-116">Códigos de error de dispositivo</span><span class="sxs-lookup"><span data-stu-id="05acb-116">Device Error Codes</span></span>](device-error-codes.md)                     | <span data-ttu-id="05acb-117">Este nuevo tema explica cómo se convierte un código de error de un dispositivo en un valor HRESULT y viceversa.</span><span class="sxs-lookup"><span data-stu-id="05acb-117">This new topic explains how an error code from a device is converted to an HRESULT value and vice versa.</span></span> <span data-ttu-id="05acb-118">Es necesario entender este proceso para evaluar un valor HRESULT que devuelven los métodos [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) y [**IUPnPService:: QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) .</span><span class="sxs-lookup"><span data-stu-id="05acb-118">An understanding of this process is necessary in order to evaluate an HRESULT value that is returned by the [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**IUPnPService::QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods.</span></span> |



 

 

 




