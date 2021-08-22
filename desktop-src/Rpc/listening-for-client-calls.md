---
title: Escucha de llamadas de cliente
description: Una vez que la aplicación de servidor ha registrado sus interfaces, creado la información de enlace necesaria y registrado sus puntos de conexión, está lista para empezar a escuchar las llamadas a procedimiento remoto desde programas cliente.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- Llamada a procedimiento remoto RPC, tareas, escucha de llamadas de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f94453a3250cfc1adae72aa0af96297a741beb501839f7f7831e3f88a8c218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928610"
---
# <a name="listening-for-client-calls"></a>Escucha de llamadas de cliente

Una vez que la aplicación de servidor ha registrado sus interfaces, creado la información de enlace necesaria y registrado sus puntos de conexión, está lista para empezar a escuchar las llamadas a procedimiento remoto desde programas cliente.

Para escuchar llamadas a procedimientos remotos, el programa de servidor debe llamar a [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), como se muestra en el fragmento de código siguiente:


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



Un servidor RPC tiene uno o varios subprocesos que recogen las llamadas de cliente y las entregan a las rutinas de las interfaces registradas. El primer parámetro de la [**función RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) es el número mínimo de subprocesos que se va a crear. El parámetro es solo una sugerencia; el tiempo de ejecución de RPC puede optar por omitirlo.

El segundo parámetro de [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) es el número máximo de llamadas simultáneas a procedimiento remoto que se deben controlar. Si desea que la aplicación use el valor máximo predeterminado, pase RPC C LISTEN MAX CALLS DEFAULT como \_ \_ valor para este \_ \_ \_ parámetro.

La especificación DCE llama a [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para que siga ejecutándose hasta que reciba una señal para detenerse. Una extensión de Microsoft para esta función es permitir que comience a escuchar y volver inmediatamente. Si desea que la aplicación use el comportamiento predeterminado de DCE, establezca el tercer parámetro en cero. Consulte [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)y [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) para obtener más información.

 

 




