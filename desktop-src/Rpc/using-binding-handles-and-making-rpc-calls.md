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
# <a name="using-binding-handles-and-making-rpc-calls"></a>Usar identificadores de enlace y realizar llamadas RPC

Un error común entre los programadores de RPC es el control de todas las excepciones. Muchos programadores estructuran los identificadores de excepción como los siguientes:

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

El problema con este controlador es que detecta todos los errores, incluidos los errores del programa cliente. La detección de errores en el programa cliente dificulta la depuración. La manera correcta de estructurar un controlador de excepciones es la siguiente:

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

Este controlador de excepciones tiene la ventaja de permitir un determinado intervalo de errores a través de. Estos errores nunca serán devueltos por el servidor, ya que indican un problema del lado cliente.

Además, se recomienda el uso de los atributos estricto de identificador de **\[** [ \_ contexto \_](/windows/desktop/Midl/strict-context-handle) **\]** y de **\[** [ \_ \_ \_ identificador de contexto estricto](/windows/desktop/Midl/type-strict-context-handle)para asegurarse de que **\]** el tiempo de ejecución de RPC crea un identificador de contexto en una interfaz que solo se puede pasar como argumento a los métodos de esa interfaz. Si lo hace, se evitarán errores de servidor que se producen cuando los identificadores de contexto se abren y pasan entre diferentes interfaces que existen dentro del mismo proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\_identificador de contexto estricto \_](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[escribir \_ el \_ identificador de contexto STRICT \_](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 