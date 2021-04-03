---
title: Indicar errores por excepciones
description: En el caso de los programadores de C tradicionales, los errores se devuelven normalmente a través de los valores devueltos o un parámetro especial \ out \ que devuelve el código de error.
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fafc97e4d9c9d76b965ab67bcd57f4f33100625
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904724"
---
# <a name="indicate-errors-by-exceptions"></a><span data-ttu-id="fe9eb-103">Indicar errores por excepciones</span><span class="sxs-lookup"><span data-stu-id="fe9eb-103">Indicate Errors by Exceptions</span></span>

<span data-ttu-id="fe9eb-104">En el caso de los programadores de C tradicionales, los errores se devuelven normalmente a través de los valores devueltos o un \[ parámetro out especial \] que devuelve el código de error.</span><span class="sxs-lookup"><span data-stu-id="fe9eb-104">For traditional C programmers, errors are commonly returned through return values, or a special \[out\] parameter that returns the error code.</span></span> <span data-ttu-id="fe9eb-105">Esto conduce a las interfaces implementadas de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="fe9eb-105">This leads to interfaces implemented the following way:</span></span>

``` syntax
long sample(...)
{
    ...
    p = new Cbar(...);
    if (p == NULL)
    {
        // cleanup
        ...
        return ERROR_OUTOFMEMORY;
    }
}
```

<span data-ttu-id="fe9eb-106">El problema con este enfoque es que los valores devueltos de RPC son simplemente enteros largos.</span><span class="sxs-lookup"><span data-stu-id="fe9eb-106">The problem with this approach is that RPC return values are simply long integers.</span></span> <span data-ttu-id="fe9eb-107">No tienen ningún significado especial como errores (tenga en cuenta que el [**Estado de error \_ \_ t**](/windows/desktop/Midl/error-status-t) no tiene ninguna semántica especial en el lado servidor), lo que conlleva importantes implicaciones.</span><span class="sxs-lookup"><span data-stu-id="fe9eb-107">They have no special meaning as errors (note that [**error\_status\_t**](/windows/desktop/Midl/error-status-t) has no special semantics on the server side), which carries important implications.</span></span>

<span data-ttu-id="fe9eb-108">En primer lugar, RPC no se avisa de que se produjo un error en la operación. intenta anular las referencias de todos los \[ argumentos in, out \] y \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="fe9eb-108">First, RPC is not alerted that the operation failed; it attempts to unmarshal all \[in, out\] and \[out\] arguments.</span></span> <span data-ttu-id="fe9eb-109">La semántica de errores de los identificadores de contexto también es diferente.</span><span class="sxs-lookup"><span data-stu-id="fe9eb-109">The failure semantics of context handles are also different.</span></span> <span data-ttu-id="fe9eb-110">El paquete devuelto al cliente es esencialmente un paquete correcto, con el código de error escondido en el paquete.</span><span class="sxs-lookup"><span data-stu-id="fe9eb-110">The packet returned to the client is essentially a success packet, with the error code buried deep in the packet.</span></span> <span data-ttu-id="fe9eb-111">Esto también significa que RPC no utiliza la información de error extendida, por lo que el software cliente a menudo no puede discernir dónde se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="fe9eb-111">This also means RPC does not use extended error information, so client software often is unable to discern where the call failed.</span></span>

<span data-ttu-id="fe9eb-112">Indicar errores en las rutinas de servidor RPC mediante la generación de excepciones de control de excepciones estructurado (SEH) (no C++) es un enfoque mucho mejor.</span><span class="sxs-lookup"><span data-stu-id="fe9eb-112">Indicating errors in RPC server routines by throwing Structured Exception Handling (SEH) exceptions (not C++) is a much better approach.</span></span> <span data-ttu-id="fe9eb-113">Cuando se inicia una excepción SEH, el control pasa directamente a la hora de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="fe9eb-113">When an SEH exception is thrown, control goes directly to the RPC run time.</span></span> <span data-ttu-id="fe9eb-114">A veces se produce un error en una rutina que no se puede limpiar correctamente y debe indicar un error a su llamador.</span><span class="sxs-lookup"><span data-stu-id="fe9eb-114">An error sometimes occurs deep in a routine that cannot properly clean up, and it needs to indicate an error to its caller.</span></span> <span data-ttu-id="fe9eb-115">La rutina debe devolver un error a su llamador, que a su vez puede devolver un error al autor de la llamada, etc.</span><span class="sxs-lookup"><span data-stu-id="fe9eb-115">The routine should return an error to its caller, which in turn can return an error to its caller and so on.</span></span> <span data-ttu-id="fe9eb-116">Sin embargo, la última rutina de servidor en la pila debe iniciar una excepción antes de que vuelva a RPC para indicar a RPC que se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="fe9eb-116">However, the last server routine on the stack should throw an exception before it returns to RPC to indicate to RPC that an error occurred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe9eb-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fe9eb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe9eb-118">Control de excepciones</span><span class="sxs-lookup"><span data-stu-id="fe9eb-118">Exception Handling</span></span>](exception-handling.md)
</dt> </dl>

 

 