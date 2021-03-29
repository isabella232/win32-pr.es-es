---
title: Poner el servidor a disposición en la red
description: Para que una aplicación de servidor pueda aceptar llamadas a procedimientos remotos, debe estar disponible en la red.
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- RPC llamada a procedimiento remoto, tareas, que hacen que el servidor esté disponible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2826e4e63e7e78e7f87f6afc120b80e885cd3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075930"
---
# <a name="making-the-server-available-on-the-network"></a>Poner el servidor a disposición en la red

Para que una aplicación de servidor pueda aceptar llamadas a procedimientos remotos, debe estar disponible en la red. Para ello, el servidor indica al tiempo de ejecución de RPC que está dispuesto a aceptar llamadas en una o varias secuencias de protocolo. La elección de las secuencias de protocolo que admite una aplicación de servidor es una decisión importante; las distintas secuencias de protocolo tienen funcionalidades muy diferentes. Los servidores que esperan que se reciban llamadas localmente deben usar **ncalrpc**. Los servidores que aceptan llamadas remotas deben usar **ncacn \_ IP \_ TCP**. Los servidores no deben comprobar que la secuencia de protocolos en la que reciben llamadas sea la secuencia de protocolos en la que esperan recibir llamadas. Para obtener más información, vea tener cuidado de otros extremos de RPC que se ejecutan en el mismo proceso en las mejores prácticas de programación de RPC.

En el ejemplo siguiente se usa **ncacn \_ IP \_ TCP**.

La mayoría de los programas de servidor utilizan todas las secuencias de protocolo disponibles en la red. Para ello, invocan la función [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) , tal y como se muestra en el siguiente fragmento de código:


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



El primer parámetro de la función [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) es la secuencia de protocolos. El segundo parámetro depende de la secuencia de protocolos. Como se muestra en el fragmento de código, la mayoría de los programas de servidor establecen este parámetro en el **\_ \_ \_ \_ \_ valor predeterminado de PROTSEQ Max req**. Este valor establece la biblioteca RPC para usar el valor predeterminado. El tercer parámetro es un descriptor de seguridad y no debe usarse en las aplicaciones. Para obtener más información, consulte [**seguridad**](security.md).

También puede usar las funciones [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)o [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) .

Después de que una aplicación de servidor Seleccione al menos una secuencia de protocolos, los servidores que usen puntos de conexión dinámicos deben crear información de enlace para cada secuencia de protocolo que use. El servidor almacena la información de enlace en un vector de enlace que, a continuación, puede exportar al servicio del asignador de extremos.

Utilice la función [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) para obtener un vector de enlace para la aplicación de servidor, como se muestra en el ejemplo siguiente:


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



El único parámetro que se pasa a la función [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) es un puntero a un puntero a una estructura de [**\_ \_ Vector de enlace RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) . La biblioteca en tiempo de ejecución de RPC asigna dinámicamente una matriz de vectores de enlace y almacena la dirección de la matriz en la variable de parámetro (en este caso, **rpcBindingVector**). Cada aplicación de servidor es responsable de liberar este vector de enlace mediante la función [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) una vez que ha terminado de utilizarlo (por ejemplo, después de pasarlo a las funciones adecuadas).

 

 




