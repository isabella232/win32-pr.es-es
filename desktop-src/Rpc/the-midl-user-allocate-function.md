---
title: La función midl_user_allocate
description: La \_ \_ función de asignación de usuarios de MIDL es un procedimiento que deben proporcionar los desarrolladores de aplicaciones RPC.
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b2e3196de79992f5856b7117b25f05ad782d26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149456"
---
# <a name="the-midl_user_allocate-function"></a><span data-ttu-id="85555-103">Función de \_ asignación de usuarios de MIDL \_</span><span class="sxs-lookup"><span data-stu-id="85555-103">The midl\_user\_allocate Function</span></span>

<span data-ttu-id="85555-104">La función de **\_ \_ asignación de usuarios de MIDL** es un procedimiento que deben proporcionar los desarrolladores de aplicaciones RPC.</span><span class="sxs-lookup"><span data-stu-id="85555-104">The **midl\_user\_allocate** function is a procedure that must be supplied by developers of RPC applications.</span></span> <span data-ttu-id="85555-105">Asigna memoria para el código auxiliar RPC y las rutinas de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="85555-105">It allocates memory for the RPC stubs and library routines.</span></span> <span data-ttu-id="85555-106">La función de **\_ \_ asignación de usuarios de MIDL** debe coincidir con el prototipo siguiente:</span><span class="sxs-lookup"><span data-stu-id="85555-106">Your **midl\_user\_allocate** function must match the following prototype:</span></span>

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

<span data-ttu-id="85555-107">El parámetro *cBytes* especifica el número de bytes que se van a asignar.</span><span class="sxs-lookup"><span data-stu-id="85555-107">The *cBytes* parameter specifies the number of bytes to allocate.</span></span> <span data-ttu-id="85555-108">Las aplicaciones cliente y las aplicaciones de servidor deben implementar la función de **\_ \_ asignación de usuarios de MIDL** a menos que esté compilando en modo de compatibilidad de OSF (/OSF).</span><span class="sxs-lookup"><span data-stu-id="85555-108">Both client applications and server applications must implement the **midl\_user\_allocate** function unless you are compiling in OSF-compatibility (/osf) mode.</span></span> <span data-ttu-id="85555-109">Las aplicaciones y los códigos auxiliares generados llaman de forma directa o indirecta a los **\_ \_ usuarios de MIDL** para administrar los objetos asignados.</span><span class="sxs-lookup"><span data-stu-id="85555-109">Applications and generated stubs call **midl\_user\_allocate** directly or indirectly to manage allocated objects.</span></span> <span data-ttu-id="85555-110">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="85555-110">For example:</span></span>

-   <span data-ttu-id="85555-111">Las aplicaciones de cliente y servidor llaman a la **\_ \_ asignación de usuarios de MIDL** para asignar memoria para la aplicación, como cuando se crea un nuevo nodo en un árbol o lista vinculada.</span><span class="sxs-lookup"><span data-stu-id="85555-111">The client and server applications call **midl\_user\_allocate** to allocate memory for the application, such as when creating a new node in a tree or linked list.</span></span>
-   <span data-ttu-id="85555-112">El código auxiliar del servidor llama a la **\_ \_ asignación de usuarios de MIDL** al calcular las referencias de los datos en el espacio de direcciones del servidor.</span><span class="sxs-lookup"><span data-stu-id="85555-112">The server stub calls **midl\_user\_allocate** when unmarshaling data into the server address space.</span></span>
-   <span data-ttu-id="85555-113">El código auxiliar de cliente llama a la **\_ \_ asignación de usuario de MIDL** al quitar las referencias de datos del servidor al que hace referencia un puntero de \[ salida \] .</span><span class="sxs-lookup"><span data-stu-id="85555-113">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an \[out\] pointer.</span></span> <span data-ttu-id="85555-114">Tenga en cuenta que para \[ \] \[ \] los punteros in, out y \[ Unique \] , el código auxiliar de cliente llama a la **asignación de \_ usuario \_ de MIDL** solo si el \[ valor de \] puntero único era null en la entrada y cambia a un valor distinto de NULL durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="85555-114">Note that for \[in\], \[out\], and \[unique\] pointers, the client stub calls **midl\_user\_allocate** only if the \[unique\] pointer value was null on input and changes to a non-null value during the call.</span></span> <span data-ttu-id="85555-115">Si el \[ puntero único no \] era null en la entrada, el código auxiliar del cliente escribe los datos asociados en la memoria existente.</span><span class="sxs-lookup"><span data-stu-id="85555-115">If the \[unique\] pointer was non-null on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="85555-116">Si **el \_ usuario \_** de la asignación de MIDL no puede asignar memoria, debe devolver un puntero nulo.</span><span class="sxs-lookup"><span data-stu-id="85555-116">If **midl\_user\_allocate** fails to allocate memory, it should return a null pointer.</span></span>

<span data-ttu-id="85555-117">La función de **\_ \_ asignación de usuarios de MIDL** debe devolver un puntero alineado de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="85555-117">The **midl\_user\_allocate** function should return an 8-byte aligned pointer.</span></span>

<span data-ttu-id="85555-118">Por ejemplo, los programas de ejemplo que se proporcionan con el kit de desarrollo de software (SDK) de la plataforma implementan **MIDL \_ User \_ alloca** en términos de la función de C [**malloc**](pointers-and-memory-allocation.md):</span><span class="sxs-lookup"><span data-stu-id="85555-118">For example, the sample programs provided with the Platform Software Development Kit (SDK) implement **midl\_user\_allocate** in terms of the C function [**malloc**](pointers-and-memory-allocation.md):</span></span>


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> <span data-ttu-id="85555-119">Si el paquete RpcSs está habilitado (por ejemplo, como resultado de usar el \[ atributo [**enable \_ allocate**](/windows/desktop/Midl/enable-allocate) \] ), use [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) para asignar memoria en el lado servidor.</span><span class="sxs-lookup"><span data-stu-id="85555-119">If the RpcSs package is enabled (for example, as the result of using the \[ [**enable\_allocate**](/windows/desktop/Midl/enable-allocate)\] attribute), use [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) to allocate memory on the server side.</span></span> <span data-ttu-id="85555-120">Para obtener información adicional sobre cómo \[ **Habilitar la \_ asignación** \] , vea [referencia de MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="85555-120">For additional information on \[**enable\_allocate**\], see [MIDL Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 

 