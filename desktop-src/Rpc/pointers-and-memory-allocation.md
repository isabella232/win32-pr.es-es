---
title: Punteros y asignación de memoria
description: La capacidad de cambiar la memoria a través de punteros a menudo requiere que el servidor y el cliente asignen suficiente memoria para los elementos de la matriz.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d634b209c1f6369429c432d5fad5d4e64b47aeae16778efd8916c00e65911e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927365"
---
# <a name="pointers-and-memory-allocation"></a>Punteros y asignación de memoria

La capacidad de cambiar la memoria a través de punteros a menudo requiere que el servidor y el cliente asignen suficiente memoria para los elementos de la matriz.

Cuando un código auxiliar debe asignar o liberar memoria, llama a funciones de biblioteca en tiempo de ejecución que, a su vez, llaman a las funciones [**midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) y [**midl \_ user \_ free**](/windows/desktop/Midl/midl-user-free-1). Estas funciones no se incluyen como parte de la biblioteca en tiempo de ejecución. Debe escribir sus propias versiones de estas funciones y vincularlas a la aplicación. De esta manera, puede decidir cómo administrar la memoria. Al compilar el archivo IDL en modo de compatibilidad con OSF (**/osf**), no es necesario implementar estas funciones. Debe escribir estas funciones en los prototipos siguientes:

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

Por ejemplo, las versiones de estas funciones para una aplicación simplemente pueden llamar a funciones de biblioteca estándar:


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



 

 