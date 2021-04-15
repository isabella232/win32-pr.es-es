---
title: Identificadores de enlace completo y parcialmente
description: Cuando se usan puntos de conexión dinámicos, las bibliotecas en tiempo de ejecución obtienen información del punto de conexión según lo necesiten.
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc1f434ec53ebcfd992b0090ed9066dce2ec627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486823"
---
# <a name="fully-and-partially-bound-handles"></a><span data-ttu-id="fb176-103">Identificadores de enlace completo y parcialmente</span><span class="sxs-lookup"><span data-stu-id="fb176-103">Fully and Partially Bound Handles</span></span>

<span data-ttu-id="fb176-104">Cuando se usan puntos de conexión dinámicos, las bibliotecas en tiempo de ejecución obtienen información del punto de conexión según lo necesiten.</span><span class="sxs-lookup"><span data-stu-id="fb176-104">When you use dynamic endpoints, the run-time libraries obtain endpoint information as they need it.</span></span> <span data-ttu-id="fb176-105">Las bibliotecas en tiempo de ejecución realizan la distinción entre un *identificador de enlace completo* (uno que incluye la información de extremo) y un *identificador de enlace parcial* (uno que no incluye información de extremo).</span><span class="sxs-lookup"><span data-stu-id="fb176-105">The run-time libraries make the distinction between a *fully bound handle* (one that includes endpoint information) and a *partially bound handle* (one that does not include endpoint information).</span></span>

<span data-ttu-id="fb176-106">La biblioteca en tiempo de ejecución del cliente debe convertir el identificador de enlace parcial en un identificador de enlace completo antes de que el cliente pueda enlazar con el servidor.</span><span class="sxs-lookup"><span data-stu-id="fb176-106">The client run-time library must convert the partially bound handle to a fully bound handle before the client can bind to the server.</span></span> <span data-ttu-id="fb176-107">La biblioteca en tiempo de ejecución de cliente intenta convertir el identificador de enlace parcial para la aplicación cliente obteniendo la información del punto de conexión como se muestra:</span><span class="sxs-lookup"><span data-stu-id="fb176-107">The client run-time library tries to convert the partially bound handle for the client application by obtaining the endpoint information as shown:</span></span>

-   <span data-ttu-id="fb176-108">Desde la especificación de interfaz del cliente</span><span class="sxs-lookup"><span data-stu-id="fb176-108">From the client's interface specification</span></span>
-   <span data-ttu-id="fb176-109">Desde un servicio de asignación de puntos de conexión que se ejecuta en el servidor</span><span class="sxs-lookup"><span data-stu-id="fb176-109">From an endpoint-mapping service running on the server</span></span>

<span data-ttu-id="fb176-110">Si el cliente intenta utilizar un identificador de enlace parcial cuando la información del punto de conexión no está disponible en la especificación de interfaz y el asignador de extremos del servidor no tiene información sobre el punto de conexión del servidor, el cliente no tendrá suficiente información para realizar su llamada a procedimiento remoto y se producirá un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="fb176-110">If the client tries to use a partially bound handle when the endpoint information is not available in the interface specification and the server's endpoint-mapper does not have information about the server endpoint, the client will not have enough information to make its remote procedure call and that call will fail.</span></span> <span data-ttu-id="fb176-111">Para evitarlo, debe registrar el extremo en el asignador de extremos cuando la aplicación distribuida utiliza identificadores de enlace parcial.</span><span class="sxs-lookup"><span data-stu-id="fb176-111">To prevent this, you must register the endpoint in the endpoint mapper when your distributed application uses partially bound handles.</span></span> <span data-ttu-id="fb176-112">Para obtener más información acerca del asignador de extremos, consulte [especificar puntos de conexión dinámicos](specifying-endpoints.md).</span><span class="sxs-lookup"><span data-stu-id="fb176-112">For more information about the endpoint mapper, see [Specifying Dynamic Endpoints](specifying-endpoints.md).</span></span>

<span data-ttu-id="fb176-113">Cuando se produce un error en una llamada a procedimiento remoto, la aplicación cliente puede llamar a [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) para quitar la información de punto de conexión desactualizada.</span><span class="sxs-lookup"><span data-stu-id="fb176-113">When a remote procedure call fails, the client application can call [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) to remove out-of-date endpoint information.</span></span> <span data-ttu-id="fb176-114">Cuando el cliente intenta llamar al procedimiento remoto, la biblioteca en tiempo de ejecución de cliente intenta convertir el identificador completamente enlazado en un identificador de enlace parcial.</span><span class="sxs-lookup"><span data-stu-id="fb176-114">When the client tries to call the remote procedure, the client run-time library again tries to convert the fully bound handle to a partially bound handle.</span></span> <span data-ttu-id="fb176-115">Esto resulta útil cuando el servidor se ha detenido y reiniciado con un punto de conexión dinámico diferente.</span><span class="sxs-lookup"><span data-stu-id="fb176-115">This is useful when the server has been stopped and restarted using a different dynamic endpoint.</span></span>

 

 




