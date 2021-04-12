---
title: Tiempo de espera de búsqueda
description: Un cliente también puede imponer un límite de tiempo que esperará a que un servidor devuelva el conjunto de resultados.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- ADSI de tiempo de espera de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfdc63dd4490a840a16eb61598b2461c3e1a40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356693"
---
# <a name="search-time-out"></a><span data-ttu-id="77186-104">Tiempo de espera de búsqueda</span><span class="sxs-lookup"><span data-stu-id="77186-104">Search Time Out</span></span>

<span data-ttu-id="77186-105">Un cliente también puede imponer un límite de tiempo que esperará a que un servidor devuelva el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="77186-105">A client can also impose a time limit that it will wait for a server to return the result set.</span></span> <span data-ttu-id="77186-106">El valor de la opción "tiempo de espera de la búsqueda" especifica este límite.</span><span class="sxs-lookup"><span data-stu-id="77186-106">The value of the "search time out" option specifies this limit.</span></span> <span data-ttu-id="77186-107">Cuando el servidor no responde a una consulta dentro del período de tiempo especificado, el cliente puede detener la búsqueda e intentarlo de nuevo más tarde.</span><span class="sxs-lookup"><span data-stu-id="77186-107">When the server fails to respond to a query within the specified time period, the client can stop the search and try again later.</span></span>

<span data-ttu-id="77186-108">La propiedad de tiempo de espera resulta útil cuando un cliente solicita una búsqueda asincrónica.</span><span class="sxs-lookup"><span data-stu-id="77186-108">The time-out property is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="77186-109">En una búsqueda asincrónica, el cliente realiza una solicitud y, a continuación, continúa con otras tareas mientras espera a que el servidor devuelva los resultados.</span><span class="sxs-lookup"><span data-stu-id="77186-109">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="77186-110">Es posible que el servidor se quede sin conexión sin notificar al cliente.</span><span class="sxs-lookup"><span data-stu-id="77186-110">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="77186-111">En este caso, el cliente no tiene forma de reconocer que el servidor sigue procesando la consulta o si ha dejado de estar activa.</span><span class="sxs-lookup"><span data-stu-id="77186-111">In this case, the client has no way of recognizing that the server is still processing the query, or if it has ceased to be live.</span></span> <span data-ttu-id="77186-112">La propiedad de tiempo de espera proporciona al cliente algún control de estos casos.</span><span class="sxs-lookup"><span data-stu-id="77186-112">The time-out property provides the client some control in such instances.</span></span>

<span data-ttu-id="77186-113">Para obtener más información acerca del uso de la opción de tiempo de espera de búsqueda con una interfaz de búsqueda específica, vea:</span><span class="sxs-lookup"><span data-stu-id="77186-113">For more information about using the search time-out option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="77186-114">Límite de tiempo de cliente con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="77186-114">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="77186-115">Buscar con Objetos de datos ActiveX</span><span class="sxs-lookup"><span data-stu-id="77186-115">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="77186-116">Buscar con OLE DB</span><span class="sxs-lookup"><span data-stu-id="77186-116">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




