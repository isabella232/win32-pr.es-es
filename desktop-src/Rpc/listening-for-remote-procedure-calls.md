---
title: Escuchando llamadas a procedimientos remotos
description: Una vez que un programa de servidor registra su información de enlace y anuncia su presencia en una base de datos de servicio de nombres, puede empezar a escuchar el punto de conexión para las llamadas a procedimientos remotos.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d9463e0591279377502394541190be685cccd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075008"
---
# <a name="listening-for-remote-procedure-calls"></a><span data-ttu-id="e4d1b-103">Escuchando llamadas a procedimientos remotos</span><span class="sxs-lookup"><span data-stu-id="e4d1b-103">Listening for Remote Procedure Calls</span></span>

<span data-ttu-id="e4d1b-104">Una vez que un programa de servidor registra su información de enlace y anuncia su presencia en una base de datos de servicio de nombres, puede empezar a escuchar el punto de conexión para las llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="e4d1b-104">After a server program registers its binding information and advertises its presence in a name service database, it can begin listening to the endpoint for remote procedure calls.</span></span> <span data-ttu-id="e4d1b-105">Los programas de servidor llaman a la función [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para supervisar los extremos de las invocaciones de cliente de procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="e4d1b-105">Server programs call the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to monitor endpoints for client invocations of remote procedures.</span></span>

<span data-ttu-id="e4d1b-106">La especificación de DCE de [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indica que no debe devolver hasta que una función del programa del servidor llame a [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening).</span><span class="sxs-lookup"><span data-stu-id="e4d1b-106">The DCE specification of [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indicates that it should not return until a function in the server program calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening).</span></span> <span data-ttu-id="e4d1b-107">La implementación de Microsoft RPC de **RpcServerListen** usa dos parámetros que no aparecen en la especificación de DCE: *DontWait* y *MinimumCallThreads*.</span><span class="sxs-lookup"><span data-stu-id="e4d1b-107">The Microsoft RPC implementation of **RpcServerListen** uses two parameters that do not appear in the DCE specification: *DontWait* and *MinimumCallThreads*.</span></span> <span data-ttu-id="e4d1b-108">El programa de servidor puede pasar un valor distinto de cero para el parámetro *DontWait* .</span><span class="sxs-lookup"><span data-stu-id="e4d1b-108">Your server program can pass a nonzero value for the *DontWait* parameter.</span></span> <span data-ttu-id="e4d1b-109">Si es así, la función **RpcServerListen** se devolverá inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="e4d1b-109">If it does, the **RpcServerListen** function will return immediately.</span></span> <span data-ttu-id="e4d1b-110">Use la rutina [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) para realizar la operación de espera normalmente asociada a **RpcServerListen**.</span><span class="sxs-lookup"><span data-stu-id="e4d1b-110">Use the [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) routine to perform the wait operation usually associated with **RpcServerListen**.</span></span>

 

 




