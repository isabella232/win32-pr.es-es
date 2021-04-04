---
title: Rutina de ejecución de contexto de servidor
description: Si la comunicación se interrumpe mientras el servidor mantiene el contexto en nombre del cliente, es posible que se necesite una rutina de limpieza para limpiar el estado mantenido por el servidor en nombre de un cliente determinado.
ms.assetid: b39654e4-6f03-43a0-8a5d-6f24bd0a529c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ad8afb7f698a258d7c4403143e74d566f813a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076167"
---
# <a name="server-context-run-down-routine"></a><span data-ttu-id="81b22-103">Rutina de ejecución de contexto de servidor</span><span class="sxs-lookup"><span data-stu-id="81b22-103">Server Context Run-down Routine</span></span>

<span data-ttu-id="81b22-104">Si la comunicación se interrumpe mientras el servidor mantiene el contexto en nombre del cliente, es posible que se necesite una rutina de limpieza para limpiar el estado mantenido por el servidor en nombre de un cliente determinado.</span><span class="sxs-lookup"><span data-stu-id="81b22-104">If communication breaks down while the server is maintaining context on behalf of the client, a cleanup routine may be needed to clean up the state maintained by the server on behalf of a given client.</span></span> <span data-ttu-id="81b22-105">Esta rutina de limpieza se denomina *rutina de ejecución de contexto*.</span><span class="sxs-lookup"><span data-stu-id="81b22-105">This cleanup routine is called a *context run-down routine*.</span></span> <span data-ttu-id="81b22-106">Cuando se interrumpe una conexión, el código auxiliar del servidor y la biblioteca en tiempo de ejecución llamarán a esta rutina en cada identificador de contexto abierto por el cliente.</span><span class="sxs-lookup"><span data-stu-id="81b22-106">When a connection breaks, the server stub and the run-time library will call this routine on every context handle opened by the client.</span></span>

<span data-ttu-id="81b22-107">La rutina de ejecución de contexto es obligatoria y se declara y se denomina implícitamente, cuando se aplica el \[ atributo de **\_ identificador de contexto** \] a una definición de tipo.</span><span class="sxs-lookup"><span data-stu-id="81b22-107">The context run-down routine is required, and is implicitly declared and named, when you apply the \[**context\_handle**\] attribute to a type definition.</span></span> <span data-ttu-id="81b22-108">El servidor no llamará a la rutina de ejecución de contexto si el atributo de \[ **\_ identificador de contexto** \] se aplicó directamente a un parámetro.</span><span class="sxs-lookup"><span data-stu-id="81b22-108">The server will not call the context run-down routine if the \[**context\_handle**\] attribute was applied directly to a parameter.</span></span>

<span data-ttu-id="81b22-109">La sintaxis de rutina de ejecución de contexto es:</span><span class="sxs-lookup"><span data-stu-id="81b22-109">The context run-down routine syntax is:</span></span>

``` syntax
void __RPC_USER type-id_rundown (type-id);
```

<span data-ttu-id="81b22-110">Tenga en cuenta que el nombre de tipo determina el nombre de la rutina de ejecución de contexto.</span><span class="sxs-lookup"><span data-stu-id="81b22-110">Note that the type name determines the name of the context run-down routine.</span></span>

<span data-ttu-id="81b22-111">El fragmento de código siguiente presenta una rutina de ejecución de contexto de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="81b22-111">The code fragment that follows presents a sample context run-down routine.</span></span> <span data-ttu-id="81b22-112">que llama al procedimiento RemoteClose que se usa en el ejemplo de [desarrollo de interfaces con identificadores de contexto](interface-development-using-context-handles.md), [desarrollo de servidores con identificadores de contexto](server-development-using-context-handles.md)y desarrollo de [cliente mediante identificadores de contexto](client-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="81b22-112">that calls the RemoteClose procedure used in the example in [Interface Development Using Context Handles](interface-development-using-context-handles.md), [Server Development Using Context Handles](server-development-using-context-handles.md), and [Client Development Using Context Handles](client-development-using-context-handles.md).</span></span> <span data-ttu-id="81b22-113">Este procedimiento cierra el identificador de archivo, libera la memoria asociada al archivo y asigna **null** al identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="81b22-113">This procedure closes the file handle, frees the memory associated with the file, and assigns **NULL** to the context handle.</span></span> <span data-ttu-id="81b22-114">Asignar **null** es el resultado de llamar a la función RemoteClose y no es necesario en un escenario de ejecución.</span><span class="sxs-lookup"><span data-stu-id="81b22-114">Assigning **NULL** is a result of calling the RemoteClose function, and is not necessary in a run-down scenario.</span></span> <span data-ttu-id="81b22-115">El tiempo de ejecución de RPC limpia su estado independientemente de si el identificador de contexto está establecido en **null**.</span><span class="sxs-lookup"><span data-stu-id="81b22-115">The RPC run time cleans up its state regardless of whether the context handle is set to **NULL**.</span></span>

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

 

 




