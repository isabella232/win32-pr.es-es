---
title: Usar identificadores de enlace y realizar llamadas RPC
description: Un error común entre los programadores de RPC es el control de todas las excepciones.
ms.assetid: 5b452129-4060-49f9-9400-8585fb5714a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b285fc3030b92e2616c850bf79c73e37f0341c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792789"
---
# <a name="using-binding-handles-and-making-rpc-calls"></a><span data-ttu-id="099f4-103">Usar identificadores de enlace y realizar llamadas RPC</span><span class="sxs-lookup"><span data-stu-id="099f4-103">Using Binding Handles and Making RPC Calls</span></span>

<span data-ttu-id="099f4-104">Un error común entre los programadores de RPC es el control de todas las excepciones.</span><span class="sxs-lookup"><span data-stu-id="099f4-104">A common mistake among RPC programmers is handling all exceptions.</span></span> <span data-ttu-id="099f4-105">Muchos programadores estructuran los identificadores de excepción como los siguientes:</span><span class="sxs-lookup"><span data-stu-id="099f4-105">Many programmers structure their exception handles like the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    RpcExcept(1)
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="099f4-106">El problema con este controlador es que detecta todos los errores, incluidos los errores del programa cliente.</span><span class="sxs-lookup"><span data-stu-id="099f4-106">The problem with this handler is that it catches all errors, including errors in the client program.</span></span> <span data-ttu-id="099f4-107">La detección de errores en el programa cliente dificulta la depuración.</span><span class="sxs-lookup"><span data-stu-id="099f4-107">Catching errors in the client program makes debugging more difficult.</span></span> <span data-ttu-id="099f4-108">La manera correcta de estructurar un controlador de excepciones es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="099f4-108">The proper way to structure an exception handler is the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    // Return "non-fatal" errors to clients.  Catching fatal errors
    // makes it harder to debug.
    RpcExcept( ( ( (RpcExceptionCode() != STATUS_ACCESS_VIOLATION) &&
                   (RpcExceptionCode() != STATUS_POSSIBLE_DEADLOCK) &&
                   (RpcExceptionCode() != STATUS_INSTRUCTION_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_DATATYPE_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_PRIVILEGED_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_ILLEGAL_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_BREAKPOINT) &&
                   (RpcExceptionCode() != STATUS_STACK_OVERFLOW) &&
                   (RpcExceptionCode() != STATUS_HANDLE_NOT_CLOSABLE) &&
                   (RpcExceptionCode() != STATUS_IN_PAGE_ERROR) &&
                   (RpcExceptionCode() != STATUS_ASSERTION_FAILURE) &&
                   (RpcExceptionCode() != STATUS_STACK_BUFFER_OVERRUN) &&
                   (RpcExceptionCode() != STATUS_GUARD_PAGE_VIOLATION)
                    )
                    ? EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH ) )
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="099f4-109">Este controlador de excepciones tiene la ventaja de permitir un determinado intervalo de errores a través de.</span><span class="sxs-lookup"><span data-stu-id="099f4-109">This exception handler has the advantage of letting a certain range of errors through.</span></span> <span data-ttu-id="099f4-110">Estos errores nunca serán devueltos por el servidor, ya que indican un problema del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="099f4-110">These errors will never be returned by the server, because they indicate a client side problem.</span></span>

<span data-ttu-id="099f4-111">Además, se recomienda el uso de los atributos estricto de identificador de **\[** [ \_ contexto \_](/windows/desktop/Midl/strict-context-handle) **\]** y de **\[** [ \_ \_ \_ identificador de contexto estricto](/windows/desktop/Midl/type-strict-context-handle)para asegurarse de que **\]** el tiempo de ejecución de RPC crea un identificador de contexto en una interfaz que solo se puede pasar como argumento a los métodos de esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="099f4-111">Additionally, the use of the **\[**[strict\_context\_handle](/windows/desktop/Midl/strict-context-handle)**\]** and **\[**[type\_strict\_context\_handle](/windows/desktop/Midl/type-strict-context-handle)**\]** attributes are recommended to ensure the RPC run time creates a context handle on one interface that can be passed as an argument only to methods of that interface.</span></span> <span data-ttu-id="099f4-112">Si lo hace, se evitarán errores de servidor que se producen cuando los identificadores de contexto se abren y pasan entre diferentes interfaces que existen dentro del mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="099f4-112">Doing so will prevent server failures that occur when context handles are opened and passed between different interfaces that exist within the same process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="099f4-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="099f4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="099f4-114">\_identificador de contexto estricto \_</span><span class="sxs-lookup"><span data-stu-id="099f4-114">strict\_context\_handle</span></span>](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[<span data-ttu-id="099f4-115">escribir \_ el \_ identificador de contexto STRICT \_</span><span class="sxs-lookup"><span data-stu-id="099f4-115">type\_strict\_context\_handle</span></span>](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 