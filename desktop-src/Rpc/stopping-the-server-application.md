---
title: Detener la aplicación de servidor
description: Una aplicación de servidor puede dejar de escuchar a los clientes mediante una llamada a RpcMgmtStopServerListening y RpcServerUnregisterIf, o simplemente saliendo del proceso de host.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- RPC llamada a procedimiento remoto, tareas, detener la aplicación de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f95ba05588e0575949614e05370f86de78207d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779218"
---
# <a name="stopping-the-server-application"></a><span data-ttu-id="c3e30-104">Detener la aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="c3e30-104">Stopping the Server Application</span></span>

<span data-ttu-id="c3e30-105">Una aplicación de servidor puede dejar de escuchar a los clientes mediante una llamada a [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) y [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif), o simplemente saliendo del proceso de host.</span><span class="sxs-lookup"><span data-stu-id="c3e30-105">A server application can stop listening for clients by calling [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif), or by simply exiting the host process.</span></span> <span data-ttu-id="c3e30-106">Ambos métodos son aceptables.</span><span class="sxs-lookup"><span data-stu-id="c3e30-106">Both methods are acceptable.</span></span> <span data-ttu-id="c3e30-107">Si el servidor sigue el primer enfoque, debe implementar los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c3e30-107">If the server follows the first approach, it should implement the following steps:</span></span>

<span data-ttu-id="c3e30-108">La función de servidor [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) no vuelve al programa que realiza la llamada hasta que se produce una excepción o hasta que se produce una llamada a [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) .</span><span class="sxs-lookup"><span data-stu-id="c3e30-108">The server function [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) does not return to the calling program until an exception occurs or until a call to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) occurs.</span></span> <span data-ttu-id="c3e30-109">De forma predeterminada, solo se permite que otro subproceso de servidor detenga el servidor RPC mediante **RpcMgmtStopServerListening**.</span><span class="sxs-lookup"><span data-stu-id="c3e30-109">By default, only another server thread is allowed to halt the RPC server by using **RpcMgmtStopServerListening**.</span></span> <span data-ttu-id="c3e30-110">Los clientes que intenten detener el servidor recibirán el error RPC \_ S \_ acceso \_ denegado.</span><span class="sxs-lookup"><span data-stu-id="c3e30-110">Clients who try to halt the server will receive the error RPC\_S\_ACCESS\_DENIED.</span></span> <span data-ttu-id="c3e30-111">Sin embargo, es posible configurar RPC para permitir que algunos o todos los clientes detengan el servidor.</span><span class="sxs-lookup"><span data-stu-id="c3e30-111">However, it is possible to configure RPC to allow some or all clients to stop the server.</span></span> <span data-ttu-id="c3e30-112">Consulte **RpcMgmtStopServerListening** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c3e30-112">See **RpcMgmtStopServerListening** for details.</span></span>

<span data-ttu-id="c3e30-113">También puede hacer que la aplicación cliente realice una llamada a procedimiento remoto a una rutina de apagado en el servidor.</span><span class="sxs-lookup"><span data-stu-id="c3e30-113">You can also have the client application make a remote procedure call to a shutdown routine on the server.</span></span> <span data-ttu-id="c3e30-114">La rutina Shutdown llama a [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) y [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif).</span><span class="sxs-lookup"><span data-stu-id="c3e30-114">The shutdown routine calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif).</span></span> <span data-ttu-id="c3e30-115">En esta aplicación de programa de ejemplo del tutorial se usa este enfoque agregando una nueva función remota, **Shutdown**, al archivo Hellop. c.</span><span class="sxs-lookup"><span data-stu-id="c3e30-115">This tutorial example program application uses this approach by adding a new remote function, **Shutdown**, to the file Hellop.c.</span></span>

<span data-ttu-id="c3e30-116">En la función **Shutdown** , el único parámetro null de [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indica que la aplicación local debe dejar de escuchar las llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="c3e30-116">In the **Shutdown** function, the single null parameter to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indicates that the local application should stop listening for remote procedure calls.</span></span> <span data-ttu-id="c3e30-117">Los dos parámetros null para [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) son caracteres comodín, lo que indica que se debe anular el registro de todas las interfaces.</span><span class="sxs-lookup"><span data-stu-id="c3e30-117">The two null parameters to [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) are wildcards, indicating that all interfaces should be unregistered.</span></span> <span data-ttu-id="c3e30-118">El parámetro **false** indica que la interfaz se debe quitar del registro inmediatamente, en lugar de esperar a que se completen las llamadas pendientes.</span><span class="sxs-lookup"><span data-stu-id="c3e30-118">The **FALSE** parameter indicates that the interface should be removed from the registry immediately, rather than waiting for pending calls to complete.</span></span>


```C++
/* add this function to hellop.c */
void Shutdown(void)
{
    RPC_STATUS status;
 
    status = RpcMgmtStopServerListening(NULL);
 
    if (status) 
    {
       exit(status);
    }
 
    status = RpcServerUnregisterIf(NULL, NULL, FALSE);
 
    if (status) 
    {
       exit(status);
    }
} //end Shutdown
```



 

 




