---
title: Administrador de tablas de enrutamiento
description: El administrador de tabla de enrutamiento es el repositorio central de información de enrutamiento de todos los protocolos de enrutamiento que funcionan en el servicio de enrutamiento y acceso remoto (RRAS).
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98094eb34c8575e0c24854813fc7458c98749568
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676115"
---
# <a name="routing-table-manager"></a><span data-ttu-id="b4560-103">Administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="b4560-103">Routing Table Manager</span></span>

<span data-ttu-id="b4560-104">El administrador de tabla de enrutamiento es el repositorio central de información de enrutamiento de todos los protocolos de enrutamiento que funcionan en el servicio de enrutamiento y acceso remoto (RRAS).</span><span class="sxs-lookup"><span data-stu-id="b4560-104">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="b4560-105">Notifica a los clientes cuando se han producido cambios y permite a los clientes intercambiar información privada.</span><span class="sxs-lookup"><span data-stu-id="b4560-105">It notifies clients when changes have occurred, and allows clients to exchange private information.</span></span>

<span data-ttu-id="b4560-106">El administrador de tablas de enrutamiento proporciona información de enrutamiento a todos los clientes interesados, como los protocolos de enrutamiento, los programas de administración y los programas de supervisión.</span><span class="sxs-lookup"><span data-stu-id="b4560-106">The routing table manager provides routing information to all interested clients, such as routing protocols, management programs, and monitoring programs.</span></span> <span data-ttu-id="b4560-107">El administrador de tablas de enrutamiento también determina la mejor ruta para cada red de destino que se conoce en los protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="b4560-107">The routing table manager also determines the best route to each destination network that is known to the routing protocols.</span></span> <span data-ttu-id="b4560-108">El administrador de tablas de enrutamiento determina esta ruta en función de las prioridades del Protocolo de enrutamiento y de las métricas asociadas a las rutas.</span><span class="sxs-lookup"><span data-stu-id="b4560-108">The routing table manager determines this route based on routing protocol priorities and on the metrics associated with the routes.</span></span> <span data-ttu-id="b4560-109">La persona que administra el enrutador puede configurar las prioridades del Protocolo de enrutamiento mediante la consola de administración de RRAS.</span><span class="sxs-lookup"><span data-stu-id="b4560-109">The person administering the router can configure routing protocol priorities using the RRAS management console.</span></span>

<span data-ttu-id="b4560-110">El administrador de tablas de enrutamiento pasa la información de la mejor ruta a los reenviadores (uno por familia de direcciones o uno por cada interfaz) y a todos los clientes interesados.</span><span class="sxs-lookup"><span data-stu-id="b4560-110">The routing table manager passes the best-route information to the forwarders (one per address family, or one per interface) and to all interested clients.</span></span>

<span data-ttu-id="b4560-111">Cada cliente se registra con el administrador de tablas de enrutamiento y, a su vez, recibe un identificador que el cliente utiliza para agregar o eliminar rutas.</span><span class="sxs-lookup"><span data-stu-id="b4560-111">Each client registers with the routing table manager, and in return receives a handle that the client uses to add or delete routes.</span></span> <span data-ttu-id="b4560-112">Los clientes pueden recuperar la información almacenada en la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="b4560-112">Clients can retrieve information stored in the routing table.</span></span> <span data-ttu-id="b4560-113">Además, los clientes pueden registrarse con el administrador de tablas de enrutamiento para recibir una notificación de los cambios en la mejor ruta a un destino.</span><span class="sxs-lookup"><span data-stu-id="b4560-113">Additionally, clients can register with the routing table manager to receive notification of changes to the best route to a destination.</span></span>

 

 




