---
title: Cambios en la mejor ruta a una red
description: Un cambio en cualquiera de los siguientes valores para la mejor ruta a una red de destino determinada hace que el administrador de tablas de enrutamiento genere un mensaje de notificación enviado a cada cliente registrado y a los reenviadores
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8c43483dbd69f5407f9859d5943e515e8825d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676219"
---
# <a name="changes-to-the-best-route-to-a-network"></a><span data-ttu-id="165af-103">Cambios en la mejor ruta a una red</span><span class="sxs-lookup"><span data-stu-id="165af-103">Changes to the Best Route to a Network</span></span>

<span data-ttu-id="165af-104">**Windows Server 2003:** Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="165af-104">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="165af-105">Las nuevas aplicaciones deben usar la API del administrador de tablas de enrutamiento versión 2.</span><span class="sxs-lookup"><span data-stu-id="165af-105">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="165af-106">Un cambio en cualquiera de los siguientes valores para la mejor ruta a una red de destino determinada hace que el administrador de tablas de enrutamiento genere un mensaje de notificación enviado a cada cliente registrado y a los reenviadores:</span><span class="sxs-lookup"><span data-stu-id="165af-106">A change in any of the following values for the best route to a given destination network causes the routing table manager to generate a notification message sent to each registered client and to the forwarders:</span></span>

-   <span data-ttu-id="165af-107">Identificador de protocolo</span><span class="sxs-lookup"><span data-stu-id="165af-107">Protocol identifier</span></span>
-   <span data-ttu-id="165af-108">Índice de interfaz</span><span class="sxs-lookup"><span data-stu-id="165af-108">Interface index</span></span>
-   <span data-ttu-id="165af-109">Dirección del enrutador de próximo salto</span><span class="sxs-lookup"><span data-stu-id="165af-109">Address of next-hop router</span></span>
-   <span data-ttu-id="165af-110">Datos específicos de la familia de protocolos que incluyen métricas de ruta</span><span class="sxs-lookup"><span data-stu-id="165af-110">Protocol family-specific data that includes route metrics</span></span>

<span data-ttu-id="165af-111">Un cambio en el identificador de protocolo, el índice de interfaz o la dirección del enrutador de próximo salto se produce cuando se agrega una nueva entrada de ruta mejor, o cuando se elimina o se agota la entrada de la mejor ruta actual, y deja otra ruta como la nueva ruta mejor.</span><span class="sxs-lookup"><span data-stu-id="165af-111">A change in protocol identifier, interface index, or next-hop router address occurs when a new, better-route entry is added, or when the current best-route entry is deleted or aged out, and leaves another route as the new best route.</span></span>

 

 




