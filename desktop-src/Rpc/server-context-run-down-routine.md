---
title: Rutina de ejecución de contexto de servidor
description: Si la comunicación se interrumpe mientras el servidor mantiene el contexto en nombre del cliente, puede ser necesaria una rutina de limpieza para limpiar el estado que mantiene el servidor en nombre de un cliente determinado.
ms.assetid: b39654e4-6f03-43a0-8a5d-6f24bd0a529c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ad8afb7f698a258d7c4403143e74d566f813a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473532"
---
# <a name="server-context-run-down-routine"></a>Rutina de ejecución de contexto de servidor

Si la comunicación se interrumpe mientras el servidor mantiene el contexto en nombre del cliente, puede ser necesaria una rutina de limpieza para limpiar el estado que mantiene el servidor en nombre de un cliente determinado. Esta rutina de limpieza se denomina rutina *de ejecución de contexto.* Cuando se interrumpe una conexión, el código auxiliar del servidor y la biblioteca en tiempo de ejecución llamarán a esta rutina en cada identificador de contexto abierto por el cliente.

La rutina de ejecución de contexto es necesaria y se declara y se denomina implícitamente cuando se aplica el atributo de identificador de contexto a una \[ **\_** \] definición de tipo. El servidor no llamará a la rutina de ejecución de contexto si el atributo de identificador de contexto se \[ **\_** \] aplicó directamente a un parámetro.

La sintaxis de rutina de ejecución de contexto es:

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

Tenga en cuenta que el nombre de tipo determina el nombre de la rutina de ejecución de contexto.

El fragmento de código siguiente presenta una rutina de ejecución de contexto de ejemplo. que llama al procedimiento RemoteClose usado en el [](server-development-using-context-handles.md)ejemplo de Desarrollo de interfaces mediante identificadores de contexto [,](interface-development-using-context-handles.md)Desarrollo del servidor mediante identificadores de contexto y Desarrollo de cliente [mediante identificadores de contexto](client-development-using-context-handles.md). Este procedimiento cierra el identificador de archivo, libera la memoria asociada al archivo y asigna **NULL** al identificador de contexto. La **asignación de NULL** es el resultado de llamar a la función RemoteClose y no es necesario en un escenario de ejecución. El tiempo de ejecución rpc limpia su estado independientemente de si el identificador de contexto está establecido en **NULL.**

``` syntax
//file: cxhndp.c (fragment of file containing remote procedures)
//The rundown routine is associated with the context handle type.  
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown(
    PCONTEXT_HANDLE_TYPE phContext)
{
    printf("Client died with an open file, closing it..\n");
    RemoteClose(&phContext);
    assert(phContext == 0);
}
```

 

 




