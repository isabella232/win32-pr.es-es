---
title: Paquete de administración de memoria RpcSs
description: El par de asignador predeterminado/desasignador usado por el código auxiliar y el tiempo de ejecución cuando la asignación de memoria en nombre de la aplicación es el usuario de MIDL de \_ asignación de usuarios \_ o de MIDL \_ \_ .
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca10ebea44fbb202240e981612e16e7960216
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488111"
---
# <a name="rpcss-memory-management-package"></a><span data-ttu-id="b47c2-103">Paquete de administración de memoria RpcSs</span><span class="sxs-lookup"><span data-stu-id="b47c2-103">RpcSs Memory Management Package</span></span>

<span data-ttu-id="b47c2-104">El par de asignador predeterminado/desasignador utilizado por el código auxiliar y el tiempo de ejecución al asignar memoria en nombre de la aplicación es el **usuario de MIDL que \_ \_ asigna** el usuario de / **MIDL \_ \_ gratis**.</span><span class="sxs-lookup"><span data-stu-id="b47c2-104">The default allocator/deallocator pair used by the stubs and run time when allocating memory on behalf of the application is **midl\_user\_allocate**/**midl\_user\_free**.</span></span> <span data-ttu-id="b47c2-105">Sin embargo, puede elegir el paquete RpcSs en lugar del valor predeterminado mediante el atributo ACF de **\[ habilitar \_ asignación \]**.</span><span class="sxs-lookup"><span data-stu-id="b47c2-105">However, you can choose the RpcSs package instead of the default by using the ACF attribute **\[enable\_allocate\]**.</span></span> <span data-ttu-id="b47c2-106">El paquete RpcSs consta de funciones RPC que comienzan con el prefijo **RPCSS** o **RpcSm**.</span><span class="sxs-lookup"><span data-stu-id="b47c2-106">The RpcSs package consists of RPC functions that begin with the prefix **RpcSs** or **RpcSm**.</span></span> <span data-ttu-id="b47c2-107">El paquete RpcSs no se recomienda para las aplicaciones Windows.</span><span class="sxs-lookup"><span data-stu-id="b47c2-107">The RpcSs package is not recommended for Windows applications.</span></span>

> [!Note]  
> <span data-ttu-id="b47c2-108">El paquete de administración de memoria RPCSS está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b47c2-108">The Rpcss Memory Management Package is obsolete.</span></span> <span data-ttu-id="b47c2-109">Se recomienda usar en su lugar la [**\_ \_ asignación de usuarios de MIDL**](/windows/desktop/Midl/midl-user-allocate-1) y el [**\_ usuario \_ de MIDL**](/windows/desktop/Midl/midl-user-free-1) .</span><span class="sxs-lookup"><span data-stu-id="b47c2-109">It is recommended that [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) are used in its place.</span></span>

 

<span data-ttu-id="b47c2-110">En el modo **/OSF** , el paquete RPCSS está habilitado automáticamente para los códigos auxiliares generados por MIDL cuando se usan punteros completos, cuando los argumentos requieren la asignación de memoria o como resultado de usar el atributo **\[ enable \_ allocate \]** .</span><span class="sxs-lookup"><span data-stu-id="b47c2-110">In **/osf** mode, the RpcSs package is enabled for MIDL-generated stubs automatically when full pointers are used, when the arguments require memory allocation, or as a result of using the **\[enable\_allocate\]** attribute.</span></span> <span data-ttu-id="b47c2-111">En el modo predeterminado (Microsoft Extended), el paquete RpcSs solo está habilitado cuando se usa el atributo **\[ enable \_ allocate \]** .</span><span class="sxs-lookup"><span data-stu-id="b47c2-111">In the default (Microsoft extended) mode, the RpcSs package is enabled only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="b47c2-112">El atributo **\[ enable \_ allocate \]** habilita el entorno RPCSS mediante el código auxiliar del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="b47c2-112">The **\[enable\_allocate\]** attribute enables the RpcSs environment by the server-side stubs.</span></span> <span data-ttu-id="b47c2-113">El lado cliente se alerta a la posibilidad de que se pueda habilitar el paquete RpcSs.</span><span class="sxs-lookup"><span data-stu-id="b47c2-113">The client side becomes alerted to the possibility that the RpcSs package may be enabled.</span></span> <span data-ttu-id="b47c2-114">En el modo **/OSF** , el lado cliente no se ve afectado.</span><span class="sxs-lookup"><span data-stu-id="b47c2-114">In **/osf** mode, the client side is not affected.</span></span>

<span data-ttu-id="b47c2-115">Cuando el paquete RpcSs está habilitado, la asignación de memoria en el servidor se logra con el par de asignador y desasignador de administración de memoria RpcSs privado.</span><span class="sxs-lookup"><span data-stu-id="b47c2-115">When the RpcSs package is enabled, allocation of memory on the server side is accomplished with the private RpcSs memory management allocator and deallocator pair.</span></span> <span data-ttu-id="b47c2-116">Puede asignar memoria mediante el mismo mecanismo llamando a [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (o [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)).</span><span class="sxs-lookup"><span data-stu-id="b47c2-116">You can allocate memory using the same mechanism by calling [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (or [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)).</span></span> <span data-ttu-id="b47c2-117">Al volver del código auxiliar del servidor, se libera automáticamente toda la memoria asignada por el paquete RpcSs.</span><span class="sxs-lookup"><span data-stu-id="b47c2-117">Upon return from the server stub, all the memory allocated by the RpcSs package is automatically freed.</span></span> <span data-ttu-id="b47c2-118">En el ejemplo siguiente se muestra cómo habilitar el paquete RpcSs:</span><span class="sxs-lookup"><span data-stu-id="b47c2-118">The following example shows how to enable the RpcSs package:</span></span>

``` syntax
/* ACF file fragment */

[ 
    implicit_handle(handle_t GlobalHandle),
    enable_allocate
]
interface iface
{
}

/*Server management routine fragment. Replaces p=midl_user_allocate(size); */

    p=RpcSsAllocate(size);                /*raises exception */
    p=RpcSmAllocate(size, &status);       /*returns error code */
```

<span data-ttu-id="b47c2-119">La aplicación puede liberar explícitamente la memoria mediante la invocación de la función [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) o [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) .</span><span class="sxs-lookup"><span data-stu-id="b47c2-119">Your application can explicitly free memory by invoking the [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) or [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) function.</span></span> <span data-ttu-id="b47c2-120">Tenga en cuenta que estas funciones no liberan memoria realmente.</span><span class="sxs-lookup"><span data-stu-id="b47c2-120">Note that these functions do not actually free memory.</span></span> <span data-ttu-id="b47c2-121">Lo marcan para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="b47c2-121">They mark it for deletion.</span></span> <span data-ttu-id="b47c2-122">La biblioteca RPC libera la memoria cuando el programa llama a [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) o [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).</span><span class="sxs-lookup"><span data-stu-id="b47c2-122">The RPC library releases the memory when your program calls [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) or [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).</span></span>

<span data-ttu-id="b47c2-123">También puede habilitar el entorno de administración de memoria para la aplicación mediante una llamada a la rutina [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) (y puede deshabilitarla mediante una llamada a la rutina [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) ).</span><span class="sxs-lookup"><span data-stu-id="b47c2-123">You can also enable the memory management environment for your application by calling the [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) routine (and you can disable it by calling the [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) routine).</span></span> <span data-ttu-id="b47c2-124">Una vez habilitado, el código de aplicación puede asignar y desasignar memoria llamando a las funciones del paquete RpcSs.</span><span class="sxs-lookup"><span data-stu-id="b47c2-124">Once enabled, application code can allocate and deallocate memory by calling functions from the RpcSs package.</span></span>

 

 