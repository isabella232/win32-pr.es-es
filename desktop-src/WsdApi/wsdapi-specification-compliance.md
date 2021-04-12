---
description: Servicios web en la API de dispositivos (WSDAPI) proporciona compatibilidad con el perfil de dispositivos para servicios web (DPWS) en Windows Vista, que permite la comunicación de servicios web (WS) entre equipos basados en Windows y dispositivos conectados a la red.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Compatibilidad con la especificación WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276960"
---
# <a name="wsdapi-specification-compliance"></a><span data-ttu-id="513f4-103">Compatibilidad con la especificación WSDAPI</span><span class="sxs-lookup"><span data-stu-id="513f4-103">WSDAPI Specification Compliance</span></span>

<span data-ttu-id="513f4-104">Servicios web en la API de dispositivos (WSDAPI) proporciona compatibilidad con el [Perfil de dispositivos para servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) en Windows Vista, que permite la comunicación de servicios web (WS) entre equipos basados en Windows y dispositivos conectados a la red.</span><span class="sxs-lookup"><span data-stu-id="513f4-104">Web Services on Devices API (WSDAPI) provides support for the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) on Windows Vista, which enables Web Services (WS) communication between Windows-based PCs and network connected devices.</span></span> <span data-ttu-id="513f4-105">DPWS ensambla especificaciones básicas de WS, como [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)y [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), y las mejora o las limita para proporcionar un conjunto básico de funcionalidades para dispositivos restringidos por recursos.</span><span class="sxs-lookup"><span data-stu-id="513f4-105">DPWS assembles basic WS specifications, such as [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf), and [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), and enhances or constrains them to provide a baseline set of capabilities for resource-constrained devices.</span></span> <span data-ttu-id="513f4-106">Esta especificación de línea de base contiene la funcionalidad necesaria, como la capacidad de describir las propiedades del dispositivo a través de metadatos, y la funcionalidad opcional, como la capacidad de rechazar mensajes específicos por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="513f4-106">This baseline specification contains required functionality, such as the ability to describe properties of the device through metadata, and optional functionality, such as the ability to reject specific messages for security reasons.</span></span>

<span data-ttu-id="513f4-107">La implementación de WSDAPI en Windows Vista es la primera versión de la compatibilidad explícita con DPWS y es una implementación no administrada de DPWS que es independiente y distinta de otras implementaciones de servicios web (como el [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) o [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).</span><span class="sxs-lookup"><span data-stu-id="513f4-107">The WSDAPI implementation in Windows Vista is the first release of explicit support for the DPWS, and is an unmanaged implementation of DPWS that is separate and distinct from other Web Services implementations (such as the [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) or [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).</span></span>

<span data-ttu-id="513f4-108">Los temas siguientes son de interés para los fabricantes de dispositivos y otros implementadores de dispositivos que crean dispositivos que interoperan con clientes y hosts de WSDAPI basados en Windows sin usar WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="513f4-108">The following topics are of interest to device manufacturers and other device implementers that create devices that interoperate with Windows-based WSDAPI clients and hosts without using WSDAPI.</span></span> <span data-ttu-id="513f4-109">En estos temas se describe la implementación de WSDAPI en relación con las especificaciones subyacentes.</span><span class="sxs-lookup"><span data-stu-id="513f4-109">These topics describe the implementation of WSDAPI relative to the underlying specifications.</span></span> <span data-ttu-id="513f4-110">Cubren la implementación de la funcionalidad necesaria, la funcionalidad opcional y la funcionalidad adicional no definida en la especificación.</span><span class="sxs-lookup"><span data-stu-id="513f4-110">They cover the implementation of required functionality, optional functionality, and additional functionality not defined in the specification.</span></span>

-   [<span data-ttu-id="513f4-111">Compatibilidad con la especificación DPWS</span><span class="sxs-lookup"><span data-stu-id="513f4-111">DPWS Specification Compliance</span></span>](dpws-specification-compliance.md)
-   [<span data-ttu-id="513f4-112">Compatibilidad con la especificación de WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="513f4-112">WS-Discovery Specification Compliance</span></span>](ws-discovery-specification-compliance.md)
-   [<span data-ttu-id="513f4-113">Cumplimiento de especificación de WS-MetadataExchange y WS-Transfer</span><span class="sxs-lookup"><span data-stu-id="513f4-113">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [<span data-ttu-id="513f4-114">Funcionalidad de WS-Discovery adicional</span><span class="sxs-lookup"><span data-stu-id="513f4-114">Additional WS-Discovery Functionality</span></span>](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="513f4-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="513f4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="513f4-116">Desarrollo de dispositivos WSD</span><span class="sxs-lookup"><span data-stu-id="513f4-116">WSD Device Development</span></span>](wsd-device-development.md)
</dt> <dt>

[<span data-ttu-id="513f4-117">Recomendaciones de implementación de dispositivos WSD</span><span class="sxs-lookup"><span data-stu-id="513f4-117">WSD Device Implementation Recommendations</span></span>](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
