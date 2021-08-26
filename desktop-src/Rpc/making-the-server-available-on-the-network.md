---
title: Hacer que el servidor esté disponible en la red
description: Para que una aplicación de servidor pueda aceptar llamadas a procedimiento remoto, debe estar disponible en la red.
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- Procedimiento remoto Llame a RPC , tareas, lo que hace que el servidor esté disponible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55385a1ba10f7f8ca28622af0b145ce25ef1bbbd0ab8df327687ce7fd7db6f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020059"
---
# <a name="making-the-server-available-on-the-network"></a>Hacer que el servidor esté disponible en la red

Para que una aplicación de servidor pueda aceptar llamadas a procedimiento remoto, debe estar disponible en la red. Para ello, el servidor indica al tiempo de ejecución rpc que está dispuesto a aceptar llamadas en una o varias secuencias de protocolo. Elegir las secuencias de protocolo que admite una aplicación de servidor es una decisión importante. diferentes secuencias de protocolo tienen funcionalidades muy diferentes. Los servidores que esperan que se reciban llamadas localmente deben **usar ncalrpc**. Los servidores que aceptan llamadas remotas deben **usar ncacn \_ ip \_ tcp**. Los servidores no deben comprobar que la secuencia de protocolo en la que reciben llamadas es la secuencia de protocolo en la que esperan recibir llamadas. Consulte Be Wary of Other RPC Endpoints Running in the Same Process in Best RPC Programming Practices (Tener cuidado con otros puntos de conexión RPC que se ejecutan en el mismo proceso en los procedimientos de programación de RPC recomendados) para obtener más información.

En el ejemplo siguiente se **usa ncacn \_ ip \_ tcp**.

La mayoría de los programas de servidor usan todas las secuencias de protocolo disponibles en la red. Para ello, invocan la [**función RpcServerUseProtseq,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) como se muestra en el fragmento de código siguiente:


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



El primer parámetro de la [**función RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) es la secuencia de protocolo. El segundo parámetro depende de la secuencia del protocolo. Como se muestra en el fragmento de código, la mayoría de los programas de servidor establecen este parámetro en **RPC \_ C \_ PROTSEQ \_ MAX \_ REQS \_ DEFAULT**. Este valor establece la biblioteca RPC para usar el valor predeterminado. El tercer parámetro es un descriptor de seguridad y no debe usarse en las aplicaciones. Para obtener más información, vea [**Seguridad**](security.md).

También puede usar las [**funciones RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)o [**RpcServerUseProtseqEpEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)

Una vez que una aplicación de servidor selecciona al menos una secuencia de protocolo, los servidores que usan puntos de conexión dinámicos deben crear información de enlace para cada secuencia de protocolo que use. El servidor almacena la información de enlace en un vector de enlace que, a continuación, puede exportar al servicio del asignador de puntos de conexión.

Use la [**función RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) para obtener un vector de enlace para la aplicación de servidor, como se muestra en el ejemplo siguiente:


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



El único parámetro pasado a la [**función RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) es un puntero a un puntero a una [**estructura RPC BINDING \_ \_ VECTOR.**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) La biblioteca rpc en tiempo de ejecución asigna dinámicamente una matriz de vectores de enlace y almacena la dirección de la matriz en la variable de parámetro (en este caso, **rpcBindingVector**). Cada aplicación de servidor es responsable de liberar este vector de enlace mediante la función [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) una vez que haya terminado de usarlo (por ejemplo, después de pasarlo a las funciones adecuadas).

 

 




