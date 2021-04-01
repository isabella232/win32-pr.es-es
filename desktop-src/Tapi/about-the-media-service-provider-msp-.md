---
description: Un proveedor de servicios multimedia (MSP) de TAPI 3 permite un control considerable de las aplicaciones sobre los medios de un mecanismo de transporte determinado.
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: Acerca del proveedor de servicios multimedia (MSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef4d19a2f01c047d5fc2afd4a0323d7908fcac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157000"
---
# <a name="about-the-media-service-provider-msp"></a><span data-ttu-id="e6a4d-103">Acerca del proveedor de servicios multimedia (MSP)</span><span class="sxs-lookup"><span data-stu-id="e6a4d-103">About the Media Service Provider (MSP)</span></span>

<span data-ttu-id="e6a4d-104">Un proveedor de servicios multimedia (MSP) de TAPI 3 permite un control considerable de las aplicaciones sobre los medios de un mecanismo de transporte determinado.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-104">A TAPI 3 media service provider (MSP) allows an application considerable control over the media for a particular transport mechanism.</span></span> <span data-ttu-id="e6a4d-105">Un MSP siempre existe emparejado con un proveedor de servicios de telefonía (TSP).</span><span class="sxs-lookup"><span data-stu-id="e6a4d-105">An MSP always exists paired with a Telephony Service Provider (TSP).</span></span> <span data-ttu-id="e6a4d-106">Del mismo modo que un TSP es una capa de abstracción para el control de llamadas, MSP controla los medios sin necesidad de codificación específica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-106">Just as a TSP is an abstraction layer for call control, the MSP controls media without need for device-specific coding.</span></span> <span data-ttu-id="e6a4d-107">Para obtener un ejemplo de comunicación de MSP/TSP, consulte [información general del proveedor de servicios TAPI](./tapi-service-provider-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e6a4d-107">For an example of MSP/TSP communication, see [TAPI Service Provider Overview](./tapi-service-provider-overview.md).</span></span>

<span data-ttu-id="e6a4d-108">Un MSP permite el control de medios mediante el uso de interfaces de terminal, secuencia y subflujo especiales definidas por TAPI.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-108">An MSP enables media control through the use of special terminal, stream, and substream interfaces defined by TAPI.</span></span> <span data-ttu-id="e6a4d-109">En el diagrama de [acerca de los controles de llamada y multimedia](about-call-and-media-controls.md) se muestra cómo estas interfaces aparecen en una aplicación TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-109">The diagram in [About Call and Media Controls](about-call-and-media-controls.md) illustrates how these interfaces appear to a TAPI 3 application.</span></span>

<span data-ttu-id="e6a4d-110">Además, un MSP puede implementar interfaces privadas [específicas del proveedor](provider-specific-interfaces.md), que TAPI agregará a los objetos estándar expuestos a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-110">In addition, an MSP may implement private [provider-specific interfaces](provider-specific-interfaces.md), which TAPI will aggregate onto the standard objects exposed to an application.</span></span> <span data-ttu-id="e6a4d-111">Por ejemplo, Microsoft IPConf MSP, que se instala con Microsoft Windows 2000, implementa la interfaz [**ITParticipant**](itparticipant.md) , que proporciona controles para miembros individuales de una conferencia.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-111">For example, the Microsoft IPConf MSP, which is installed with Microsoft Windows 2000, implements the [**ITParticipant**](itparticipant.md) interface, which provides controls for individual members of a conference.</span></span>

<span data-ttu-id="e6a4d-112">En el siguiente tema se describen brevemente los MSP que se pueden instalar con un sistema operativo de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-112">The following topic briefly describes the MSPs that may be installed with a Microsoft operating system.</span></span> <span data-ttu-id="e6a4d-113">Para más información sobre la configuración y el uso, consulte el kit de recursos de la plataforma de destino.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-113">For details on configuration and usage, see the resource kit for the target platform.</span></span>

<span data-ttu-id="e6a4d-114">Se pueden escribir otros proveedores de servicios multimedia de terceros para determinados protocolos o para dispositivos físicos.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-114">Additional third-party media service providers can be written for particular protocols or for physical devices.</span></span> <span data-ttu-id="e6a4d-115">La [interfaz del proveedor de servicios multimedia (MSPI)](media-service-provider-interface-mspi-.md) describe las interfaces que se deben implementar para permitir que un MSP interactúe con los componentes de telefonía de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e6a4d-115">The [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md) describes the interfaces that must be implemented to allow an MSP to interact with the components of Microsoft Telephony.</span></span>

 

 
