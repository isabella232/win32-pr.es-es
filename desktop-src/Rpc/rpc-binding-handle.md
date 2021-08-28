---
title: RPC_BINDING_HANDLE (Rpcdce.h)
description: El tipo de datos RPC BINDING HANDLE declara un identificador de enlace que contiene información que la biblioteca en tiempo de ejecución de \_ RPC usa para acceder a la información de enlace.
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0218f1a7331a070340b7740c83f8464b2286de2698daf67ac1092aa5c057db03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018589"
---
# <a name="rpc_binding_handle"></a>IDENTIFICADOR \_ DE ENLACE \_ RPC

El **tipo de datos RPC BINDING \_ HANDLE** declara un identificador de enlace que contiene información que la biblioteca en tiempo de ejecución de RPC usa para acceder a la información de enlace.


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a>Comentarios

La biblioteca en tiempo de ejecución usa información de enlace para establecer una relación cliente-servidor que permite la ejecución de llamadas a procedimiento remoto. En función del contexto en el que se crea un identificador de enlace, se considera un identificador de enlace de servidor o un identificador de enlace de cliente.

Un identificador de enlace de servidor contiene la información necesaria para que un cliente establezca una relación con un servidor específico. Cualquier número de rutinas en tiempo de ejecución de la API RPC devuelve un identificador de enlace de servidor que se puede usar para realizar una llamada a procedimiento remoto.

No se puede usar un identificador de enlace de cliente para realizar una llamada a procedimiento remoto. La biblioteca en tiempo de ejecución RPC crea y proporciona un identificador de enlace de cliente a un procedimiento denominado servidor (también denominado rutina de administrador de servidor) como el parámetro RPC \_ BINDING \_ HANDLE. El identificador de enlace de cliente contiene información sobre el cliente que realiza la llamada.

Las **funciones RpcBinding \* *_* y \* _ RpcNsBinding** devuelven el código de estado RPC S WRONG KIND OF BINDING cuando una aplicación proporciona el tipo de \_ identificador de enlace \_ \_ \_ \_ incorrecto.

Una aplicación puede compartir un identificador de enlace único entre varios subprocesos de ejecución. La biblioteca rpc en tiempo de ejecución administra llamadas simultáneas a procedimientos remotos que usan un único identificador de enlace. Sin embargo, la aplicación es responsable del control de simultaneidad del identificador de enlace para las operaciones que modifican un identificador de enlace. Estas operaciones incluyen las rutinas siguientes:

-   [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

Por ejemplo, si una aplicación comparte un identificador de enlace entre dos subprocesos de ejecución y restablece el punto de conexión del identificador de enlace en uno de los subprocesos mediante una llamada a [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), los resultados no están definidos. También se puede restablecer el identificador de enlace en el otro subproceso, o bien se puede producir un error en la operación o se puede bloquear el proceso. Un error común es liberar un identificador de enlace mientras hay una llamada en él en curso. esto normalmente bloquea el proceso de llamada.

Si no desea simultaneidad, puede diseñar una aplicación para crear una copia de un identificador de enlace llamando a [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy). En este caso, una operación para el primer identificador de enlace no tiene ningún efecto en el segundo identificador de enlace.

Las rutinas que requieren un identificador de enlace como parámetro muestran un tipo de datos **de RPC \_ BINDING \_ HANDLE**. Los parámetros de identificador de enlace se pasan por valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce.h (incluir Rpc.h)</dt> </dl> |



 

 





