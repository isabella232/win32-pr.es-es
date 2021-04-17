---
title: La función midl_user_free
description: Los \_ desarrolladores de \_ RPC deben proporcionar la función gratuita de usuario de MIDL.
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713ed05173b709780b6496f233051fa3adddff8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421324"
---
# <a name="the-midl_user_free-function"></a><span data-ttu-id="61cb9-103">La \_ función gratuita de usuario de MIDL \_</span><span class="sxs-lookup"><span data-stu-id="61cb9-103">The midl\_user\_free Function</span></span>

<span data-ttu-id="61cb9-104">Los desarrolladores de RPC deben proporcionar la función **\_ \_ gratuita de usuario de MIDL** .</span><span class="sxs-lookup"><span data-stu-id="61cb9-104">The **midl\_user\_free** function must be supplied by RPC developers.</span></span> <span data-ttu-id="61cb9-105">Asigna memoria para el código auxiliar RPC y las rutinas de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="61cb9-105">It allocates memory for the RPC stubs and library routines.</span></span> <span data-ttu-id="61cb9-106">La **función \_ \_ gratuita de usuario de MIDL** debe coincidir con el prototipo siguiente:</span><span class="sxs-lookup"><span data-stu-id="61cb9-106">Your **midl\_user\_free** function must match the following prototype:</span></span>

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

<span data-ttu-id="61cb9-107">El parámetro *pBuffer* especifica un puntero a la memoria que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="61cb9-107">The *pBuffer* parameter specifies a pointer to the memory that is to be freed.</span></span> <span data-ttu-id="61cb9-108">Tanto la aplicación cliente como la aplicación de servidor deben implementar la función **\_ \_ gratuita de usuario de MIDL** a menos que esté compilando en modo de compatibilidad de OSF ([**/OSF**](/windows/desktop/Midl/-osf)).</span><span class="sxs-lookup"><span data-stu-id="61cb9-108">Both client application and server application must implement the **midl\_user\_free** function unless you are compiling in OSF-compatibility ([**/osf**](/windows/desktop/Midl/-osf)) mode.</span></span> <span data-ttu-id="61cb9-109">La **función \_ \_ gratuita de usuario de MIDL** debe ser capaz de liberar todo el almacenamiento asignado por el usuario de la [**\_ \_ asignación de MIDL**](the-midl-user-allocate-function.md).</span><span class="sxs-lookup"><span data-stu-id="61cb9-109">The **midl\_user\_free** function must be able to free all storage allocated by [**midl\_user\_allocate**](the-midl-user-allocate-function.md).</span></span>

<span data-ttu-id="61cb9-110">Las aplicaciones y los códigos auxiliares llaman al **usuario de MIDL \_ \_ gratis** cuando se trabaja con objetos asignados:</span><span class="sxs-lookup"><span data-stu-id="61cb9-110">Applications and stubs call **midl\_user\_free** when dealing with allocated objects:</span></span>

-   <span data-ttu-id="61cb9-111">La aplicación de servidor debe llamar al **usuario de MIDL \_ \_** para liberar memoria asignada por la aplicación, como cuando se elimina un nodo de datos asignado dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="61cb9-111">The server application should call **midl\_user\_free** to free memory allocated by the application, such as when deleting a dynamically allocated node of data.</span></span>
-   <span data-ttu-id="61cb9-112">El código auxiliar del servidor llama **\_ \_ gratuitamente al usuario de MIDL** para liberar memoria en el servidor después de calcular las referencias de todos los \[ \] argumentos de salida, \[ en \] , \[ los argumentos de salida \] y el valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="61cb9-112">The server stub calls **midl\_user\_free** to release memory on the server after marshaling all \[out\] arguments, \[in\],\[out\] arguments, and the function return value.</span></span>

<span data-ttu-id="61cb9-113">Por ejemplo, el programa de ejemplo RPC de Windows que muestra "Hello, World" implementa de forma gratuita el **usuario de MIDL \_ \_** en términos de la función de C:</span><span class="sxs-lookup"><span data-stu-id="61cb9-113">For example, the RPC Windows sample program that displays "Hello, world" implements **midl\_user\_free** in terms of the C function free:</span></span>


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> <span data-ttu-id="61cb9-114">Si el paquete RpcSs está habilitado (por ejemplo, como resultado de usar el \[ atributo [**enable \_ allocate**](/windows/desktop/Midl/enable-allocate) \] ), el programa de servidor debe usar [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="61cb9-114">If the RpcSs package is enabled (for example, as the result of using the \[ [**enable\_allocate**](/windows/desktop/Midl/enable-allocate)\] attribute), your server program should use [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) to free memory.</span></span> <span data-ttu-id="61cb9-115">Para obtener más información, consulte el [paquete de administración de memoria RPCSS](rpcss-memory-management-package.md).</span><span class="sxs-lookup"><span data-stu-id="61cb9-115">For more information, see [RpcSs Memory Management Package](rpcss-memory-management-package.md).</span></span>

 

 

 