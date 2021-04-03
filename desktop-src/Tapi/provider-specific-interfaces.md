---
description: TAPI 3 admite la integración de interfaces específicas del proveedor de servicios en los objetos estándar, lo que permite que las aplicaciones aprovechen la funcionalidad específica del proveedor.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Interfaces de Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f95499f005c8c3b3e854f33835b9c9b183416d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083178"
---
# <a name="provider-specific-interfaces"></a><span data-ttu-id="25291-103">Interfaces de Provider-Specific</span><span class="sxs-lookup"><span data-stu-id="25291-103">Provider-Specific Interfaces</span></span>

<span data-ttu-id="25291-104">TAPI 3 admite la integración de interfaces específicas del proveedor de servicios en los objetos estándar, lo que permite que las aplicaciones aprovechen la funcionalidad específica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="25291-104">TAPI 3 supports integration of service provider-specific interfaces into the standard objects, allowing applications to take advantage of provider-specific functionality.</span></span> <span data-ttu-id="25291-105">Además, TAPI 3 permite que los proveedores de servicios entreguen eventos específicos del proveedor a las aplicaciones como objetos COM en la misma interfaz en la que la aplicación recibe eventos estándar.</span><span class="sxs-lookup"><span data-stu-id="25291-105">Additionally, TAPI 3 allows service providers to deliver vendor-specific events to applications as COM objects over the same interface on which the application receives standard events.</span></span>

<span data-ttu-id="25291-106">TAPI consigue esta integración mediante la agregación de objetos específicos del proveedor con los objetos estándar (TAPI, dirección, terminal, llamada y CallHub) y la distribución o delegación de métodos desconocidos para estos objetos específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="25291-106">TAPI achieves this integration by aggregating provider-specific objects with the standard objects – TAPI, Address, Terminal, Call, and CallHub – and dispatching or delegating unknown methods to these provider-specific objects.</span></span>

<span data-ttu-id="25291-107">Por ejemplo, un proveedor de servicios puede permitir que las aplicaciones obtengan información sobre una llamada más allá de lo que expone la interfaz [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="25291-107">For example, a service provider may allow applications to obtain information about a call beyond what is exposed by the [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) interface.</span></span> <span data-ttu-id="25291-108">El proveedor debe definir una interfaz que permita a las aplicaciones realizar estas consultas adicionales e implementar esa interfaz en un objeto.</span><span class="sxs-lookup"><span data-stu-id="25291-108">The vendor must define an interface that allows applications to make these extra queries and implement that interface on an object.</span></span> <span data-ttu-id="25291-109">Este objeto también implementa una interfaz de consulta de información de proveedor para que una aplicación pueda detectar qué tipos de funciones específicas del proveedor pueden estar disponibles.</span><span class="sxs-lookup"><span data-stu-id="25291-109">This object also implements a vendor information-querying interface so that an application can discover what sorts of provider-specific functions might be available.</span></span>

<span data-ttu-id="25291-110">Cuando la aplicación obtiene una referencia a un objeto de llamada, la aplicación puede usar la nueva interfaz específica del proveedor y sus métodos como si se hubieran implementado mediante el propio objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="25291-110">When the application obtains a reference to a call object, the application can use the new provider-specific interface and its methods as if they were implemented by the call object itself.</span></span>

<span data-ttu-id="25291-111">Consulte [referencia de la interfaz del proveedor de servicios multimedia (MSPI)](media-service-provider-interface-mspi-reference.md) para obtener una lista de todas las interfaces MSP estándar.</span><span class="sxs-lookup"><span data-stu-id="25291-111">See [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md) for a list of all standard MSP interfaces.</span></span>

<span data-ttu-id="25291-112">Consulte [interfaces de IPCONF MSP](ipconf-msp-interfaces.md) para obtener una lista de todas las interfaces específicas de IPConf MSP.</span><span class="sxs-lookup"><span data-stu-id="25291-112">See [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a list of all interfaces specific to the IPConf MSP.</span></span>

 

 



