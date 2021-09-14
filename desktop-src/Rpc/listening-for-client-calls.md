---
title: Escucha de llamadas de cliente
description: Una vez que la aplicación de servidor ha registrado sus interfaces, creado la información de enlace necesaria y registrado sus puntos de conexión, está listo para empezar a escuchar las llamadas a procedimientos remotos desde programas cliente.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- Llamada a procedimiento remoto RPC, tareas, escucha de llamadas de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f375a4620e301f59d168bf5f7a4dbeedc0fb89f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244538"
---
# <a name="listening-for-client-calls"></a>Escucha de llamadas de cliente

Una vez que la aplicación de servidor ha registrado sus interfaces, creado la información de enlace necesaria y registrado sus puntos de conexión, está listo para empezar a escuchar las llamadas a procedimientos remotos desde programas cliente.

Para escuchar las llamadas a procedimientos remotos, el programa de servidor debe llamar a [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), como se muestra en el fragmento de código siguiente:


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



Un servidor RPC tiene uno o varios subprocesos que recogen las llamadas de cliente y las entregan a las rutinas de las interfaces registradas. El primer parámetro de la [**función RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) es el número mínimo de subprocesos que se va a crear. El parámetro es solo una sugerencia; el tiempo de ejecución de RPC puede optar por omitirlo.

El segundo parámetro de [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) es el número máximo de llamadas a procedimientos remotos simultáneos que se deben controlar. Si desea que la aplicación use el valor máximo predeterminado, pase RPC \_ C LISTEN MAX CALLS DEFAULT como valor para este \_ \_ \_ \_ parámetro.

La especificación DCE llama a [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para que siga ejecutándose hasta que reciba una señal para detenerse. Una extensión de Microsoft a esta función es permitir que comience a escuchar y vuelva inmediatamente. Si desea que la aplicación use el comportamiento predeterminado de DCE, establezca el tercer parámetro en cero. Consulte [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)y [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) para obtener más información.

 

 




