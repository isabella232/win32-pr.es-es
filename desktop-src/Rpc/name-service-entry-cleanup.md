---
title: Limpieza de entrada de servicio de nombre
description: Una entrada de servicio de nombre debe contener información que no cambia con frecuencia.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe7484d1c6d557899e3b661a3a616c97d3890becfad51df0e91f5a69467faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019610"
---
# <a name="name-service-entry-cleanup"></a>Limpieza de entrada de servicio de nombre

Una entrada de servicio de nombre debe contener información que no cambia con frecuencia. Por esta razón, no incluya puntos de conexión dinámicos en los identificadores de enlace exportados porque cambiarán en cada invocación del servidor y abarrotarán la entrada del servicio de nombres. Para quitar estos identificadores de enlace, use [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).

Por ejemplo, una secuencia razonable de operaciones de servidor sería:

Para más de un transporte:

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

Para colocar enlaces en el asignador de puntos de conexión:

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

Para quitar puntos de conexión de los enlaces:

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

 

 




