---
title: Implementación de un dispositivo hospedado
description: El host de dispositivo con tecnología UPnP implementa la detección, descripción, control y eventos de los protocolos UPnP principales.
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172e9935dcbca73dbb285ba73270375fb5bfb6cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779111"
---
# <a name="implementing-a-hosted-device"></a><span data-ttu-id="0d0b5-103">Implementación de un dispositivo hospedado</span><span class="sxs-lookup"><span data-stu-id="0d0b5-103">Implementing a Hosted Device</span></span>

<span data-ttu-id="0d0b5-104">El host de dispositivo con tecnología UPnP implementa los principales protocolos UPnP: detección, descripción, control y eventos.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-104">The device host with UPnP technology implements the core UPnP protocols: discovery, description, control, and eventing.</span></span> <span data-ttu-id="0d0b5-105">El desarrollador que implementa un dispositivo hospedado solo debe proporcionar:</span><span class="sxs-lookup"><span data-stu-id="0d0b5-105">The developer who implements a hosted device only needs to provide:</span></span>

-   <span data-ttu-id="0d0b5-106">Descripción del dispositivo y sus servicios.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-106">A description of the device and its services.</span></span>
-   <span data-ttu-id="0d0b5-107">Implementación de la funcionalidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-107">An implementation of the device's functionality.</span></span>

<span data-ttu-id="0d0b5-108">Por ejemplo, el desarrollador de un dispositivo de reloj debe proporcionar descripciones de dispositivos y servicios basados en UPnP, y una implementación de las funciones de reloj (por ejemplo, mantener el tiempo, establecer el tiempo y responder a las consultas de la hora actual).</span><span class="sxs-lookup"><span data-stu-id="0d0b5-108">For example, the developer of a clock device must provide UPnP-based device and service descriptions for it, and an implementation of the clock functions (such as keeping time, setting time, and responding to queries for the current time).</span></span> <span data-ttu-id="0d0b5-109">El host del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="0d0b5-109">The device host:</span></span>

-   <span data-ttu-id="0d0b5-110">Anuncia el dispositivo según el protocolo de detección de UPnP.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-110">Announces the device according to the UPnP discovery protocol.</span></span>
-   <span data-ttu-id="0d0b5-111">Responde a las consultas de la descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-111">Responds to queries for the device's description.</span></span>
-   <span data-ttu-id="0d0b5-112">Enruta las solicitudes de control a la parte del código del dispositivo que implementa las funciones de reloj.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-112">Routes control requests to the part of the device's code that implements the clock functions.</span></span>
-   <span data-ttu-id="0d0b5-113">Mantiene las suscripciones de eventos a los servicios.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-113">Maintains event subscriptions to services.</span></span>
-   <span data-ttu-id="0d0b5-114">Envía notificaciones de eventos a los suscriptores cuando cambia el estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="0d0b5-114">Sends event notifications to subscribers when the service's state changes.</span></span>

 

 




