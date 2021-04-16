---
title: Conexión del cliente y el servidor
description: Para comunicarse, los programas de cliente y servidor deben establecer una sesión de comunicación a través de la red o redes que los conectan.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- RPC llamada a procedimiento remoto, tareas, conexión de cliente y servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a22ea7a9a6dd30f2b9495b6d2ee868aac217f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486858"
---
# <a name="connecting-the-client-and-the-server"></a><span data-ttu-id="7bbc0-104">Conexión del cliente y el servidor</span><span class="sxs-lookup"><span data-stu-id="7bbc0-104">Connecting the Client and the Server</span></span>

<span data-ttu-id="7bbc0-105">Para comunicarse, los programas de cliente y servidor deben establecer una sesión de comunicación a través de la red o redes que los conectan.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-105">To communicate, client and server programs must establish a communication session across the network or networks that connect them.</span></span> <span data-ttu-id="7bbc0-106">Una vez que se establece la conexión, el cliente puede llamar a procedimientos remotos en el programa de servidor como si fueran locales para el programa cliente.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-106">Once they establish the connection, the client can call remote procedures in the server program as if they were local to the client program.</span></span>

<span data-ttu-id="7bbc0-107">En esta sección se proporciona información conceptual sobre cómo establecer una conexión entre clientes y servidores para llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-107">This section provides a conceptual overview of how to establish a connection between clients and servers for remote procedure calls.</span></span> <span data-ttu-id="7bbc0-108">No proporciona una explicación detallada de este tema.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-108">It does not provide an in-depth discussion of this topic.</span></span> <span data-ttu-id="7bbc0-109">Todos los conceptos de esta sección se presentan en detalle en los capítulos posteriores y en la sección de referencia de la función RPC.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-109">All of the concepts in this section are presented in detail in later chapters and in the RPC Function Reference section.</span></span>

<span data-ttu-id="7bbc0-110">La discusión presentada en esta sección se divide en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="7bbc0-110">The discussion presented in this section is divided into the following topics:</span></span>

-   [<span data-ttu-id="7bbc0-111">Terminología de enlace RPC esencial</span><span class="sxs-lookup"><span data-stu-id="7bbc0-111">Essential RPC Binding Terminology</span></span>](essential-rpc-binding-terminology.md)
-   [<span data-ttu-id="7bbc0-112">Cómo se prepara el servidor para una conexión</span><span class="sxs-lookup"><span data-stu-id="7bbc0-112">How the Server Prepares for a Connection</span></span>](how-the-server-prepares-for-a-connection.md)
-   [<span data-ttu-id="7bbc0-113">Cómo el cliente establece una conexión</span><span class="sxs-lookup"><span data-stu-id="7bbc0-113">How the Client Establishes a Connection</span></span>](how-the-client-establishes-a-connection.md)

<span data-ttu-id="7bbc0-114">Tenga en cuenta que en la discusión se asumen los identificadores de enlace explícitos.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-114">Note that the discussion assumes explicit binding handles.</span></span> <span data-ttu-id="7bbc0-115">Sin embargo, si la aplicación usa otros tipos de identificadores de enlace, es posible que tenga que modificar los pasos que se presentan en esta sección.</span><span class="sxs-lookup"><span data-stu-id="7bbc0-115">However, if your application uses other types of binding handles, you may have to modify the steps presented in this section.</span></span> <span data-ttu-id="7bbc0-116">Para obtener más información, vea [enlazar y controlar](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="7bbc0-116">For more information, see [Binding and Handles](binding-and-handles.md).</span></span>

 

 




