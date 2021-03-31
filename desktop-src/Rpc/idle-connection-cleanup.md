---
title: Limpieza de conexión inactiva
description: De forma predeterminada, las conexiones del grupo de subprocesos no se cierran hasta que se cierra toda la asociación.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75587781991c2aae86968d90c9da51331d7a29e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903213"
---
# <a name="idle-connection-cleanup"></a><span data-ttu-id="88405-103">Limpieza de conexión inactiva</span><span class="sxs-lookup"><span data-stu-id="88405-103">Idle Connection Cleanup</span></span>

<span data-ttu-id="88405-104">De forma predeterminada, las conexiones del grupo de subprocesos no se cierran hasta que se cierra toda la asociación.</span><span class="sxs-lookup"><span data-stu-id="88405-104">By default, connections in the thread pool are not closed until the whole association is shut down.</span></span> <span data-ttu-id="88405-105">Esta directiva permite a los clientes con un gran número de subprocesos o identidades de seguridad realizar llamadas RPC al servidor de una manera eficaz.</span><span class="sxs-lookup"><span data-stu-id="88405-105">This policy enables clients with a large number of threads or security identities to make RPC calls to the server in an efficient manner.</span></span> <span data-ttu-id="88405-106">El inconveniente es que se puede confirmar una cantidad imordenada de recursos para mantener esas conexiones.</span><span class="sxs-lookup"><span data-stu-id="88405-106">The drawback is that an inordinate amount of resources may be committed to maintaining those connections.</span></span> <span data-ttu-id="88405-107">Para administrar el proceso, RPC proporciona la función [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) .</span><span class="sxs-lookup"><span data-stu-id="88405-107">To manage the process, RPC provides the [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) function.</span></span> <span data-ttu-id="88405-108">Esta función habilita la limpieza de la conexión inactiva; el cliente examina periódicamente el grupo de conexiones y cierra las conexiones que no se han usado recientemente.</span><span class="sxs-lookup"><span data-stu-id="88405-108">This function enables idle connection cleanup; the client periodically scans the connection pool and closes connections that have not been recently used.</span></span> <span data-ttu-id="88405-109">Si la Asociación ha mantenido identificadores de contexto, la limpieza de la conexión inactiva cierra todas las conexiones inactivas, pero garantiza que al menos una conexión se deja abierta, incluso si la conexión está inactiva (de lo contrario, el servidor obtiene las ejecuciones de identificador de contexto).</span><span class="sxs-lookup"><span data-stu-id="88405-109">If the association has maintained context handles, the idle connection cleanup closes all idle connections, but makes sure at least one connection is left open, even if the connection is idle (otherwise the server gets context handle run downs).</span></span> <span data-ttu-id="88405-110">Si la asociación no ha mantenido los identificadores de contexto, la limpieza de la conexión inactiva cierra todas las conexiones inactivas, aunque no deje ninguna conexión en el grupo.</span><span class="sxs-lookup"><span data-stu-id="88405-110">If the association has not maintained context handles, idle connection cleanup closes all idle connections, even if doing so leaves no connections in the pool.</span></span>

<span data-ttu-id="88405-111">En Windows XP, el tiempo de ejecución de RPC realiza un seguimiento del número de conexiones abiertas en una asociación y activa automáticamente la limpieza de la conexión inactiva si el número de conexiones en cualquier asociación supera un determinado umbral.</span><span class="sxs-lookup"><span data-stu-id="88405-111">On Windows XP, the RPC run time keeps track of the number of open connections in an association, and automatically turns on idle connection cleanup if the number of connections in any association exceeds a certain threshold.</span></span>

 

 




