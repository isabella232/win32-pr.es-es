---
description: Cuando se envía a una dirección de destino de multidifusión, el protocolo IPv6 de Microsoft requiere normalmente que la aplicación tenga una interfaz de salida especificada.
ms.assetid: dbfeaa1f-a7c5-4a15-90f0-4d1cdaf798e9
title: Direcciones IPv6 de destino de multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aa516713fb47f6af03d8564c464a07a19cf0f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497453"
---
# <a name="ipv6-multicast-destination-addresses"></a><span data-ttu-id="ad84d-103">Direcciones IPv6 de destino de multidifusión</span><span class="sxs-lookup"><span data-stu-id="ad84d-103">IPv6 Multicast Destination Addresses</span></span>

<span data-ttu-id="ad84d-104">Cuando se envía a una dirección de destino de multidifusión, el protocolo IPv6 de Microsoft requiere normalmente que la aplicación tenga una interfaz de salida especificada.</span><span class="sxs-lookup"><span data-stu-id="ad84d-104">When sending to a multicast destination address, the Microsoft IPv6 protocol normally requires that the application have an outgoing interface specified.</span></span> <span data-ttu-id="ad84d-105">Esto se hace con la opción de socket de **\_ multidifusión IPv6 \_ si** se enlaza el socket a una dirección de origen específica.</span><span class="sxs-lookup"><span data-stu-id="ad84d-105">This is done with the **IPV6\_MULTICAST\_IF** socket option or by binding the socket to a specific source address.</span></span>

<span data-ttu-id="ad84d-106">También puede especificar una interfaz predeterminada para una dirección de multidifusión específica, un ámbito de dirección de multidifusión completo o todas las direcciones de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="ad84d-106">You can also specify a default interface for a specific multicast address, an entire multicast address scope, or all multicast addresses.</span></span> <span data-ttu-id="ad84d-107">Esto se hace con una ruta que coloca el prefijo de multidifusión en el vínculo a la interfaz de salida deseada.</span><span class="sxs-lookup"><span data-stu-id="ad84d-107">This is done with a route that places the multicast prefix on-link to the desired outgoing interface.</span></span> <span data-ttu-id="ad84d-108">En los siguientes ejemplos se muestra cómo se puede especificar esto:</span><span class="sxs-lookup"><span data-stu-id="ad84d-108">For following examples show how this can be specified:</span></span>

``` syntax
ipv6 rtu ff02::5/128 3
ipv6 rtu ff0e::/16 3
ipv6 rtu ff00::/8 3
```

 

 



