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
# <a name="pointers-and-memory-allocation"></a><span data-ttu-id="80154-103">Punteros y asignación de memoria</span><span class="sxs-lookup"><span data-stu-id="80154-103">Pointers and Memory Allocation</span></span>

<span data-ttu-id="80154-104">La capacidad de cambiar la memoria a través de punteros a menudo requiere que el servidor y el cliente asignen suficiente memoria para los elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="80154-104">The ability to change memory through pointers often requires that the server and the client allocate enough memory for the elements in the array.</span></span>

<span data-ttu-id="80154-105">Cuando un código auxiliar debe asignar o liberar memoria, llama a las funciones de la biblioteca en tiempo de ejecución que, a su vez, llaman a las funciones de [**\_ \_ asignación de usuarios de MIDL**](/windows/desktop/Midl/midl-user-allocate-1) y el [**usuario de MIDL \_ \_**](/windows/desktop/Midl/midl-user-free-1).</span><span class="sxs-lookup"><span data-stu-id="80154-105">When a stub must allocate or free memory, it calls run-time library functions that in turn call the functions [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1).</span></span> <span data-ttu-id="80154-106">Estas funciones no se incluyen como parte de la biblioteca en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="80154-106">These functions are not included as part of the run-time library.</span></span> <span data-ttu-id="80154-107">Debe escribir sus propias versiones de estas funciones y vincularlas a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="80154-107">You need to write your own versions of these functions and link them with your application.</span></span> <span data-ttu-id="80154-108">De esta manera, puede decidir cómo administrar la memoria.</span><span class="sxs-lookup"><span data-stu-id="80154-108">In this way, you can decide how to manage memory.</span></span> <span data-ttu-id="80154-109">Al compilar el archivo IDL en modo de compatibilidad de OSF (**/OSF**), no es necesario implementar estas funciones.</span><span class="sxs-lookup"><span data-stu-id="80154-109">When compiling your IDL file in OSF-compatibility (**/osf**) mode, you do not need to implement these functions.</span></span> <span data-ttu-id="80154-110">Debe escribir estas funciones en los prototipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="80154-110">You must write these functions to the following prototypes:</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

<span data-ttu-id="80154-111">Por ejemplo, las versiones de estas funciones para una aplicación solo pueden llamar a funciones de la biblioteca estándar:</span><span class="sxs-lookup"><span data-stu-id="80154-111">For example, the versions of these functions for an application can simply call standard library functions:</span></span>


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



 

 