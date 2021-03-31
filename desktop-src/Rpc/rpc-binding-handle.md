---
title: RPC_BINDING_HANDLE (Rpcdce. h)
description: El \_ tipo de datos de identificador de enlace RPC declara un identificador de enlace que contiene información que la biblioteca en tiempo de ejecución de RPC utiliza para obtener acceso a la información de enlace.
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e37d14bc5186f05815c10f538b0c90bdddd353
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803992"
---
# <a name="rpc_binding_handle"></a>\_identificador de enlace RPC \_

El tipo de datos de **\_ identificador de enlace RPC** declara un identificador de enlace que contiene información que la biblioteca en tiempo de ejecución de RPC utiliza para obtener acceso a la información de enlace.


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a>Observaciones

La biblioteca en tiempo de ejecución utiliza la información de enlace para establecer una relación cliente-servidor que permite la ejecución de llamadas a procedimientos remotos. En función del contexto en el que se crea un identificador de enlace, se considera un identificador de enlace de servidor o un identificador de enlace del cliente.

Un identificador de enlace de servidor contiene la información necesaria para que un cliente establezca una relación con un servidor específico. Cualquier número de rutinas en tiempo de ejecución de la API de RPC devuelve un identificador de enlace de servidor que se puede utilizar para realizar una llamada a procedimiento remoto.

No se puede usar un identificador de enlace de cliente para realizar una llamada a procedimiento remoto. La biblioteca en tiempo de ejecución de RPC crea y proporciona un identificador de enlace de cliente a un procedimiento llamado-Server (también denominado rutina del administrador de servidores) como \_ parámetro de identificador de enlace RPC \_ . El identificador de enlace de cliente contiene información sobre el cliente que realiza la llamada.

Las funciones ** \* RpcBinding* _ _*y \* RpcNsBinding*_ devuelven el código \_ de estado RPC S \_ \_ tipo incorrecto \_ de \_ enlace cuando una aplicación proporciona el tipo de identificador de enlace incorrecto.

Una aplicación puede compartir un único identificador de enlace entre varios subprocesos de ejecución. La biblioteca en tiempo de ejecución de RPC administra llamadas a procedimientos remotos simultáneas que usan un único identificador de enlace. Sin embargo, la aplicación es responsable de enlazar el control de simultaneidad para las operaciones que modifican un identificador de enlace. Estas operaciones incluyen las siguientes rutinas:

-   [_ *RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

Por ejemplo, si una aplicación comparte un identificador de enlace entre dos subprocesos de ejecución y restablece el punto de conexión de controlador de enlace en uno de los subprocesos llamando a [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), los resultados son indefinidos. También se puede restablecer el controlador de enlace en el otro subproceso o se puede producir un error en la operación o se puede bloquear el proceso. Un error común es liberar un identificador de enlace mientras se está realizando una llamada en él. Normalmente, Esto bloquea el proceso de llamada.

Si no desea la simultaneidad, puede diseñar una aplicación para crear una copia de un identificador de enlace mediante una llamada a [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy). En este caso, una operación al primer identificador de enlace no tiene ningún efecto en el segundo controlador de enlace.

Las rutinas que requieren un identificador de enlace como parámetro muestran un tipo de datos de **\_ \_ identificador de enlace de RPC**. Los parámetros de identificador de enlace se pasan por valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce. h (incluir RPC. h)</dt> </dl> |



 

 





