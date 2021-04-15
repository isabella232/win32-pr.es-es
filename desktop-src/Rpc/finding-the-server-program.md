---
title: Buscar el programa de servidor
description: Una vez que el tiempo de ejecución de RPC del cliente se conecta a un sistema host de servidor solicitado en el identificador de enlace, la biblioteca en tiempo de ejecución de RPC del cliente encuentra el proceso de servidor.
ms.assetid: 0c863018-746a-4793-abe7-1838d988e0f4
keywords:
- RPC llamada a procedimiento remoto, tareas, buscar el programa de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b822dbca1a927e13f01d7c91aa7c78267db4d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676179"
---
# <a name="finding-the-server-program"></a><span data-ttu-id="8ead3-104">Buscar el programa de servidor</span><span class="sxs-lookup"><span data-stu-id="8ead3-104">Finding the Server Program</span></span>

<span data-ttu-id="8ead3-105">Una vez que el tiempo de ejecución de RPC del cliente se conecta a un sistema host de servidor solicitado en el identificador de enlace, la biblioteca en tiempo de ejecución de RPC del cliente encuentra el proceso de servidor.</span><span class="sxs-lookup"><span data-stu-id="8ead3-105">After the client side RPC run time connects to a server host system requested in the binding handle, the client RPC run-time library finds the server process.</span></span> <span data-ttu-id="8ead3-106">Para ello, consulta la asignación de punto de conexión en el sistema host del servidor.</span><span class="sxs-lookup"><span data-stu-id="8ead3-106">To do this, it queries the endpoint map on the server host system.</span></span> <span data-ttu-id="8ead3-107">La asignación de punto de conexión contiene información sobre el punto de conexión al que escucha el servidor.</span><span class="sxs-lookup"><span data-stu-id="8ead3-107">The endpoint map contains information about which endpoint the server is listening to.</span></span>

 

 




