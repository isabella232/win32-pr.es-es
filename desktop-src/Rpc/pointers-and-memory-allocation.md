---
title: Punteros y asignación de memoria
description: La capacidad de cambiar la memoria a través de punteros a menudo requiere que el servidor y el cliente asignen suficiente memoria para los elementos de la matriz.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdd4c51207de093dfe2d32ec0c275aa7a05a317
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149514"
---
# <a name="pointers-and-memory-allocation"></a>Punteros y asignación de memoria

La capacidad de cambiar la memoria a través de punteros a menudo requiere que el servidor y el cliente asignen suficiente memoria para los elementos de la matriz.

Cuando un código auxiliar debe asignar o liberar memoria, llama a las funciones de la biblioteca en tiempo de ejecución que, a su vez, llaman a las funciones de [**\_ \_ asignación de usuarios de MIDL**](/windows/desktop/Midl/midl-user-allocate-1) y el [**usuario de MIDL \_ \_**](/windows/desktop/Midl/midl-user-free-1). Estas funciones no se incluyen como parte de la biblioteca en tiempo de ejecución. Debe escribir sus propias versiones de estas funciones y vincularlas a la aplicación. De esta manera, puede decidir cómo administrar la memoria. Al compilar el archivo IDL en modo de compatibilidad de OSF (**/OSF**), no es necesario implementar estas funciones. Debe escribir estas funciones en los prototipos siguientes:

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

Por ejemplo, las versiones de estas funciones para una aplicación solo pueden llamar a funciones de la biblioteca estándar:


```C++
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)
{
    return(malloc(len));
}

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 