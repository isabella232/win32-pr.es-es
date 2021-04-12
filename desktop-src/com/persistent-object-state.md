---
title: Estado del objeto persistente
description: Estado del objeto persistente
ms.assetid: 731fef03-d204-48e7-b33a-801e97a9d2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c08d4dd1175b5a7681f79fa9049772af245a031
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356848"
---
# <a name="persistent-object-state"></a><span data-ttu-id="a2e4b-103">Estado del objeto persistente</span><span class="sxs-lookup"><span data-stu-id="a2e4b-103">Persistent Object State</span></span>

<span data-ttu-id="a2e4b-104">Algunos objetos COM pueden guardar su estado interno cuando un cliente le pide que lo haga.</span><span class="sxs-lookup"><span data-stu-id="a2e4b-104">Some COM objects can save their internal state when asked to do so by a client.</span></span>

<span data-ttu-id="a2e4b-105">COM define los estándares a través de los cuales los clientes pueden solicitar que los objetos se inicialicen, carguen y guarden en un almacén de datos (por ejemplo, archivo plano, almacenamiento estructurado o memoria).</span><span class="sxs-lookup"><span data-stu-id="a2e4b-105">COM defines standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="a2e4b-106">Es responsabilidad del cliente administrar la ubicación donde se almacenan los datos persistentes del objeto, pero no el formato de los datos.</span><span class="sxs-lookup"><span data-stu-id="a2e4b-106">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span> <span data-ttu-id="a2e4b-107">Los objetos COM que se adhieren a estos estándares se denominan *objetos persistentes*.</span><span class="sxs-lookup"><span data-stu-id="a2e4b-107">COM objects that adhere to these standards are called *persistent objects*.</span></span>

<span data-ttu-id="a2e4b-108">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a2e4b-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a2e4b-109">Interfaces de objeto persistentes</span><span class="sxs-lookup"><span data-stu-id="a2e4b-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
-   [<span data-ttu-id="a2e4b-110">Inicializar objetos persistentes</span><span class="sxs-lookup"><span data-stu-id="a2e4b-110">Initializing Persistent Objects</span></span>](initializing-persistent-objects.md)

## <a name="related-topics"></a><span data-ttu-id="a2e4b-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2e4b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2e4b-112">Clientes y servidores COM</span><span class="sxs-lookup"><span data-stu-id="a2e4b-112">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




