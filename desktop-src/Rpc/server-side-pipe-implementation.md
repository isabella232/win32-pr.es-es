---
title: Implementación de Server-Side Pipe
description: Los programas de servidor para las aplicaciones distribuidas que utilizan canalizaciones no necesitan implementar las funciones de inserción, extracción o asignación.
ms.assetid: de733075-5767-4d46-b294-089c7e3cc695
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6927350e10061850c5fac0ab0db7c18570dd2bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075980"
---
# <a name="server-side-pipe-implementation"></a><span data-ttu-id="1cd78-103">Implementación de Server-Side Pipe</span><span class="sxs-lookup"><span data-stu-id="1cd78-103">Server-Side Pipe Implementation</span></span>

<span data-ttu-id="1cd78-104">Los programas de servidor para las aplicaciones distribuidas que utilizan canalizaciones no necesitan implementar las funciones de inserción, extracción o asignación.</span><span class="sxs-lookup"><span data-stu-id="1cd78-104">Server programs for distributed applications that use pipes need not implement any push, pull, or alloc functions.</span></span> <span data-ttu-id="1cd78-105">Tienen que contener procedimientos que los clientes pueden invocar de forma remota para iniciar las transferencias de datos.</span><span class="sxs-lookup"><span data-stu-id="1cd78-105">They do need to contain procedures that clients can invoke remotely to initiate data transfers.</span></span> <span data-ttu-id="1cd78-106">En los temas siguientes, en esta sección se explica cómo se pueden implementar los procedimientos remotos del servidor.</span><span class="sxs-lookup"><span data-stu-id="1cd78-106">In the following topics, this section explains how the server's remote procedures can be implemented.</span></span>

-   [<span data-ttu-id="1cd78-107">Implementar canalizaciones de entrada en el servidor</span><span class="sxs-lookup"><span data-stu-id="1cd78-107">Implementing Input Pipes on the Server</span></span>](implementing-input-pipes-on-the-server.md)
-   [<span data-ttu-id="1cd78-108">Implementación de canalizaciones de salida en el servidor</span><span class="sxs-lookup"><span data-stu-id="1cd78-108">Implementing Output Pipes on the Server</span></span>](implementing-output-pipes-on-the-server.md)

 

 




