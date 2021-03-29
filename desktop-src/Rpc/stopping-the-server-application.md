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
# <a name="stopping-the-server-application"></a>Detener la aplicación de servidor

Una aplicación de servidor puede dejar de escuchar a los clientes mediante una llamada a [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) y [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif), o simplemente saliendo del proceso de host. Ambos métodos son aceptables. Si el servidor sigue el primer enfoque, debe implementar los pasos siguientes:

La función de servidor [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) no vuelve al programa que realiza la llamada hasta que se produce una excepción o hasta que se produce una llamada a [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) . De forma predeterminada, solo se permite que otro subproceso de servidor detenga el servidor RPC mediante **RpcMgmtStopServerListening**. Los clientes que intenten detener el servidor recibirán el error RPC \_ S \_ acceso \_ denegado. Sin embargo, es posible configurar RPC para permitir que algunos o todos los clientes detengan el servidor. Consulte **RpcMgmtStopServerListening** para obtener más información.

También puede hacer que la aplicación cliente realice una llamada a procedimiento remoto a una rutina de apagado en el servidor. La rutina Shutdown llama a [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) y [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif). En esta aplicación de programa de ejemplo del tutorial se usa este enfoque agregando una nueva función remota, **Shutdown**, al archivo Hellop. c.

En la función **Shutdown** , el único parámetro null de [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indica que la aplicación local debe dejar de escuchar las llamadas a procedimientos remotos. Los dos parámetros null para [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) son caracteres comodín, lo que indica que se debe anular el registro de todas las interfaces. El parámetro **false** indica que la interfaz se debe quitar del registro inmediatamente, en lugar de esperar a que se completen las llamadas pendientes.


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



 

 




