---
title: Usar punteros opacos
description: Los clientes a menudo deben almacenar información adicional específica del cliente acerca de los destinos.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9893b3a8b8e8a69ab78f33156efbe872b86d83ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903668"
---
# <a name="using-opaque-pointers"></a><span data-ttu-id="c0782-103">Usar punteros opacos</span><span class="sxs-lookup"><span data-stu-id="c0782-103">Using Opaque Pointers</span></span>

<span data-ttu-id="c0782-104">Los clientes a menudo deben almacenar información adicional específica del cliente acerca de los destinos.</span><span class="sxs-lookup"><span data-stu-id="c0782-104">Clients often must store additional, client-specific information about destinations.</span></span> <span data-ttu-id="c0782-105">El administrador de tablas de enrutamiento permite a los clientes almacenar esta información en estructuras de destino de la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="c0782-105">The routing table manager enables clients to store this information in destination structures in the routing table.</span></span> <span data-ttu-id="c0782-106">La información se almacena y se recupera mediante *punteros opacos*.</span><span class="sxs-lookup"><span data-stu-id="c0782-106">The information is stored and retrieved by using *opaque pointers*.</span></span> <span data-ttu-id="c0782-107">La información almacenada es privada y solo es accesible para el cliente que posee el puntero opaco.</span><span class="sxs-lookup"><span data-stu-id="c0782-107">The information stored is private, and accessible only to the client that owns the opaque pointer.</span></span>

<span data-ttu-id="c0782-108">Por ejemplo, el administrador del grupo de multidifusión mantiene una lista de entradas de reenvío de multidifusión que dependen de un destino determinado.</span><span class="sxs-lookup"><span data-stu-id="c0782-108">For example, the multicast group manager keeps a list of multicast forwarding entries that are dependent on a particular destination.</span></span> <span data-ttu-id="c0782-109">El administrador del grupo de multidifusión usa un puntero opaco en ese destino.</span><span class="sxs-lookup"><span data-stu-id="c0782-109">The multicast group manager uses an opaque pointer in that destination.</span></span> <span data-ttu-id="c0782-110">En otro ejemplo, un protocolo de enrutamiento que anuncia un destino determinado puede mantener la información relacionada con su propio anuncio de ruta del destino mediante un puntero opaco, aunque no sea el propietario de la mejor ruta.</span><span class="sxs-lookup"><span data-stu-id="c0782-110">In another example, a routing protocol that advertises a particular destination can keep information related to its own route advertisement of the destination using an opaque pointer, even though it does not own the best route.</span></span>

<span data-ttu-id="c0782-111">El número de punteros opacos es limitado; estos punteros se asignan a los clientes en función de la primera vez que se atiende.</span><span class="sxs-lookup"><span data-stu-id="c0782-111">The number of opaque pointers is limited; these pointers are allocated to clients on a first-come, first-served basis.</span></span> <span data-ttu-id="c0782-112">El administrador del enrutador debe asignar el número correcto de punteros durante la configuración del enrutador. por lo tanto, los protocolos de enrutamiento y otros clientes deben documentar el uso de punteros opacos.</span><span class="sxs-lookup"><span data-stu-id="c0782-112">The router administrator must allocate the correct number of pointers during the router configuration; therefore, routing protocols and other clients must document their use of opaque pointers.</span></span>

 

 




