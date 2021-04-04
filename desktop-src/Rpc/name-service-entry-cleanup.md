---
title: Limpieza de entradas del servicio de nombres
description: Una entrada de servicio de nombres debe contener información que no cambia con frecuencia.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0ed6a21074a49a472d7505dcfea37cf182026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076055"
---
# <a name="name-service-entry-cleanup"></a>Limpieza de entradas del servicio de nombres

Una entrada de servicio de nombres debe contener información que no cambia con frecuencia. Por esta razón, no incluya puntos de conexión dinámicos en los identificadores de enlace exportados porque cambiarán en cada invocación del servidor y se amontonarán en la entrada del servicio de nombres. Para quitar estos identificadores de enlace, use [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).

Por ejemplo, una secuencia de operaciones de servidor razonable sería:

Para más de un transporte:

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

Para colocar enlaces en el asignador de extremos:

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

Para quitar los puntos de conexión de los enlaces:

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

Para agregar enlaces al servicio de nombres:

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




