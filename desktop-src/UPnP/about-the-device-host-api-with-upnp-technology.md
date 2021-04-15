---
title: Acerca de la API del host del dispositivo
description: La API de host de dispositivo con tecnología UPnP es un marco para implementar la funcionalidad de dispositivos basados en UPnP en la plataforma Windows.
ms.assetid: fa716c59-d3f0-4cd4-b92d-939b258b0102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c751328696d6524208dc95a0b7961829f8ee231c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419038"
---
# <a name="about-the-device-host-api"></a><span data-ttu-id="9c108-103">Acerca de la API del host del dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c108-103">About the Device Host API</span></span>

<span data-ttu-id="9c108-104">La API de host de dispositivo con tecnología UPnP es un marco para implementar la funcionalidad de dispositivos basados en UPnP en la plataforma Windows.</span><span class="sxs-lookup"><span data-stu-id="9c108-104">The Device Host API with UPnP technology is a framework for implementing UPnP-based device functionality on the Windows platform.</span></span> <span data-ttu-id="9c108-105">Los desarrolladores que crean dispositivos mediante la API de host de dispositivo con tecnología UPnP (a la que se hace referencia como [*dispositivos hospedados*](h-gly.md)) solo necesitan implementar la funcionalidad básica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c108-105">Developers who are creating devices by using the Device Host API with UPnP technology (referred to as [*hosted devices*](h-gly.md)) need only implement the device's core functionality.</span></span> <span data-ttu-id="9c108-106">Los desarrolladores pueden basarse en el host del dispositivo para controlar los detalles específicos de UPnP de detección, descripción, control, eventos y presentación.</span><span class="sxs-lookup"><span data-stu-id="9c108-106">Developers can rely on the device host to handle the UPnP-specific details of discovery, description, control, eventing, and presentation.</span></span> <span data-ttu-id="9c108-107">El host del dispositivo valida los datos entrantes de los clientes basados en UPnP y da formato a todos los datos salientes de los dispositivos hospedados según la arquitectura del dispositivo UPnP.</span><span class="sxs-lookup"><span data-stu-id="9c108-107">The device host validates incoming data from UPnP-based clients and formats all outgoing data from hosted devices according to the UPnP device architecture.</span></span>

<span data-ttu-id="9c108-108">En las secciones siguientes se explica, en general, cómo funciona el host de dispositivo UPnP:</span><span class="sxs-lookup"><span data-stu-id="9c108-108">The following sections explain, in general, how the UPnP device host works:</span></span>

-   [<span data-ttu-id="9c108-109">Implementación de un dispositivo hospedado</span><span class="sxs-lookup"><span data-stu-id="9c108-109">Implementing a Hosted Device</span></span>](implementing-a-hosted-device.md)
-   [<span data-ttu-id="9c108-110">Registro de un dispositivo hospedado con el host del dispositivo</span><span class="sxs-lookup"><span data-stu-id="9c108-110">Registering a Hosted Device with the Device Host</span></span>](registering-a-hosted-device-with-the-device-host.md)
-   [<span data-ttu-id="9c108-111">Proveedores de dispositivos</span><span class="sxs-lookup"><span data-stu-id="9c108-111">Device Providers</span></span>](device-providers.md)
-   [<span data-ttu-id="9c108-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="9c108-112">Eventing</span></span>](eventing.md)
-   [<span data-ttu-id="9c108-113">Presentación</span><span class="sxs-lookup"><span data-stu-id="9c108-113">Presentation</span></span>](presentation.md)

 

 




