---
title: Consultar variables de estado
description: La interfaz IUPnPService proporciona el método QueryStateVariable, que devuelve el valor de una variable de estado especificada.
ms.assetid: 9e8b98b0-488a-4f9c-9ad7-039dbd470486
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a716bbe93c2306eca43b977a42f33a85187f92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357001"
---
# <a name="querying-state-variables"></a><span data-ttu-id="d7134-103">Consultar variables de estado</span><span class="sxs-lookup"><span data-stu-id="d7134-103">Querying State Variables</span></span>

<span data-ttu-id="d7134-104">La interfaz [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) proporciona el método [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) , que devuelve el valor de una variable de estado especificada.</span><span class="sxs-lookup"><span data-stu-id="d7134-104">The [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface provides the [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) method, that returns the value of a specified state variable.</span></span>

<span data-ttu-id="d7134-105">El foro de UPnP desaconseja el uso de [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable).</span><span class="sxs-lookup"><span data-stu-id="d7134-105">The UPnP Forum discourages the use of [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable).</span></span> <span data-ttu-id="d7134-106">Se recomienda que los escritores de dispositivos escriban las acciones adecuadas para proporcionar esta información.</span><span class="sxs-lookup"><span data-stu-id="d7134-106">Device writers have been encouraged to write appropriate actions to provide this information.</span></span> <span data-ttu-id="d7134-107">Los escritores de dispositivos no tienen ninguna obligación de implementar **QueryStateVariable**.</span><span class="sxs-lookup"><span data-stu-id="d7134-107">Device writers are under no obligation to implement **QueryStateVariable**.</span></span>

<span data-ttu-id="d7134-108">Vea la sección [invocación de acciones](invoking-actions.md).</span><span class="sxs-lookup"><span data-stu-id="d7134-108">See the section [Invoking Actions](invoking-actions.md).</span></span>

 

 




