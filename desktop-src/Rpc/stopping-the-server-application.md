---
title: Detención de la aplicación de servidor
description: Una aplicación de servidor puede dejar de escuchar a los clientes llamando a RpcMgmtStopServerListening y RpcServerUnregisterIf, o simplemente saliendo del proceso de host.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- Llamada a procedimiento remoto RPC, tareas, detención de la aplicación de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f95ba05588e0575949614e05370f86de78207d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473504"
---
# <a name="stopping-the-server-application"></a>Detención de la aplicación de servidor

Una aplicación de servidor puede dejar de escuchar a los clientes llamando a [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) y [**RpcServerUnregisterIf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)o simplemente saliendo del proceso de host. Ambos métodos son aceptables. Si el servidor sigue el primer enfoque, debe implementar los pasos siguientes:

La función de [**servidor RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) no vuelve al programa de llamada hasta que se produce una excepción o hasta que se produce una llamada a [**RpcMgmtStopServerListening.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) De forma predeterminada, solo otro subproceso de servidor puede detener el servidor RPC mediante **RpcMgmtStopServerListening.** Los clientes que intenten detener el servidor recibirán el error RPC \_ S \_ ACCESS \_ DENIED. Sin embargo, es posible configurar RPC para permitir que algunos o todos los clientes detengan el servidor. Consulte **RpcMgmtStopServerListening para** obtener más información.

También puede hacer que la aplicación cliente realice una llamada a procedimiento remoto a una rutina de apagado en el servidor. La rutina de cierre llama [**a RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) y [**RpcServerUnregisterIf.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) Esta aplicación de programa de ejemplo de tutorial usa este enfoque agregando una nueva función remota, **Shutdown**, al archivo Hellop.c.

En la **función Shutdown,** el parámetro null único para [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indica que la aplicación local debe dejar de escuchar las llamadas a procedimiento remoto. Los dos parámetros NULL de [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) son caracteres comodín, lo que indica que se debe anular el registro de todas las interfaces. El **parámetro FALSE** indica que la interfaz se debe quitar del Registro inmediatamente, en lugar de esperar a que se completen las llamadas pendientes.


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



 

 




