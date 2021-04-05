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
# <a name="listening-for-client-calls"></a>Escuchando llamadas de cliente

Una vez que la aplicación de servidor ha registrado sus interfaces, ha creado la información de enlace necesaria y registrado sus extremos, está listo para empezar a escuchar las llamadas a procedimiento remoto desde los programas cliente.

Para escuchar las llamadas a procedimientos remotos, el programa de servidor debe llamar a [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), como se muestra en el siguiente fragmento de código:


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



Un servidor RPC tiene uno o más subprocesos que recopilan llamadas de cliente y las entregan a las rutinas de las interfaces registradas. El primer parámetro de la función [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) es el número mínimo de subprocesos que se van a crear. El parámetro es solo una sugerencia; es posible que el tiempo de ejecución de RPC decida omitirlo.

El segundo parámetro para [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) es el número máximo de llamadas a procedimientos remotos simultáneas que se van a controlar. Si desea que la aplicación use el valor máximo predeterminado, pase el valor \_ \_ \_ predeterminado de las llamadas Max de RPC C Listen \_ \_ como valor para este parámetro.

La especificación de DCE llama a [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para que siga ejecutándose hasta que reciba una señal para detenerse. Una extensión de Microsoft para esta función consiste en permitir que empiece a escuchar y volver inmediatamente. Si desea que la aplicación use el comportamiento predeterminado de DCE, establezca el tercer parámetro en cero. Consulte [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)y [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) para obtener más información.

 

 




