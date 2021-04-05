---
title: Escuchando llamadas de cliente
description: Una vez que la aplicación de servidor ha registrado sus interfaces, ha creado la información de enlace necesaria y registrado sus extremos, está listo para empezar a escuchar las llamadas a procedimiento remoto desde los programas cliente.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- RPC llamada a procedimiento remoto, tareas, escucha de llamadas de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f375a4620e301f59d168bf5f7a4dbeedc0fb89f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903773"
---
# <a name="listening-for-client-calls"></a><span data-ttu-id="06cfc-104">Escuchando llamadas de cliente</span><span class="sxs-lookup"><span data-stu-id="06cfc-104">Listening for Client Calls</span></span>

<span data-ttu-id="06cfc-105">Una vez que la aplicación de servidor ha registrado sus interfaces, ha creado la información de enlace necesaria y registrado sus extremos, está listo para empezar a escuchar las llamadas a procedimiento remoto desde los programas cliente.</span><span class="sxs-lookup"><span data-stu-id="06cfc-105">After your server application has registered its interfaces, created the necessary binding information, and registered its endpoints, it is ready to begin listening for remote procedure calls from client programs.</span></span>

<span data-ttu-id="06cfc-106">Para escuchar las llamadas a procedimientos remotos, el programa de servidor debe llamar a [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), como se muestra en el siguiente fragmento de código:</span><span class="sxs-lookup"><span data-stu-id="06cfc-106">To listen for remote procedure calls, your server program must call [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



<span data-ttu-id="06cfc-107">Un servidor RPC tiene uno o más subprocesos que recopilan llamadas de cliente y las entregan a las rutinas de las interfaces registradas.</span><span class="sxs-lookup"><span data-stu-id="06cfc-107">An RPC Server has one or more threads that pick up client calls and deliver them to the routines in the registered interfaces.</span></span> <span data-ttu-id="06cfc-108">El primer parámetro de la función [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) es el número mínimo de subprocesos que se van a crear.</span><span class="sxs-lookup"><span data-stu-id="06cfc-108">The first parameter to the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function is the minimum number of threads to create.</span></span> <span data-ttu-id="06cfc-109">El parámetro es solo una sugerencia; es posible que el tiempo de ejecución de RPC decida omitirlo.</span><span class="sxs-lookup"><span data-stu-id="06cfc-109">The parameter is only a hint; the RPC run time may chose to ignore it.</span></span>

<span data-ttu-id="06cfc-110">El segundo parámetro para [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) es el número máximo de llamadas a procedimientos remotos simultáneas que se van a controlar.</span><span class="sxs-lookup"><span data-stu-id="06cfc-110">The second parameter to [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) is the maximum number of concurrent remote procedure calls to handle.</span></span> <span data-ttu-id="06cfc-111">Si desea que la aplicación use el valor máximo predeterminado, pase el valor \_ \_ \_ predeterminado de las llamadas Max de RPC C Listen \_ \_ como valor para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="06cfc-111">If you want your application to use the default maximum value, pass RPC\_C\_LISTEN\_MAX\_CALLS\_DEFAULT as the value for this parameter.</span></span>

<span data-ttu-id="06cfc-112">La especificación de DCE llama a [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para que siga ejecutándose hasta que reciba una señal para detenerse.</span><span class="sxs-lookup"><span data-stu-id="06cfc-112">The DCE specification calls for [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) to keep running until it receives a signal to stop.</span></span> <span data-ttu-id="06cfc-113">Una extensión de Microsoft para esta función consiste en permitir que empiece a escuchar y volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="06cfc-113">One Microsoft extension to this function is to enable it to begin listening and return immediately.</span></span> <span data-ttu-id="06cfc-114">Si desea que la aplicación use el comportamiento predeterminado de DCE, establezca el tercer parámetro en cero.</span><span class="sxs-lookup"><span data-stu-id="06cfc-114">If you want your application to use the default DCE behavior, set the third parameter to zero.</span></span> <span data-ttu-id="06cfc-115">Consulte [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)y [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="06cfc-115">See [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), and [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) for details.</span></span>

 

 




