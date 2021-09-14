---
title: Limpieza de entrada del servicio de nombres
description: Una entrada del servicio de nombres debe contener información que no cambia con frecuencia.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0ed6a21074a49a472d7505dcfea37cf182026
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169082"
---
# <a name="name-service-entry-cleanup"></a>Limpieza de entrada del servicio de nombres

Una entrada del servicio de nombres debe contener información que no cambia con frecuencia. Por este motivo, no incluya puntos de conexión dinámicos en los identificadores de enlace exportados porque cambiarán en cada invocación del servidor y abarrotarán la entrada del servicio de nombres. Para quitar estos identificadores de enlace, use [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).

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

 

 




