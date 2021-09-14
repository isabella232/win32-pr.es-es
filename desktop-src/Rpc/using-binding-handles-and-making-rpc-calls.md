---
title: Usar identificadores de enlace y realizar llamadas RPC
description: Un error común entre los programadores de RPC es controlar todas las excepciones.
ms.assetid: 5b452129-4060-49f9-9400-8585fb5714a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b285fc3030b92e2616c850bf79c73e37f0341c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169046"
---
# <a name="using-binding-handles-and-making-rpc-calls"></a>Usar identificadores de enlace y realizar llamadas RPC

Un error común entre los programadores de RPC es controlar todas las excepciones. Muchos programadores estructuran sus identificadores de excepciones de la siguiente manera:

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

El problema con este controlador es que detecta todos los errores, incluidos los errores del programa cliente. Detectar errores en el programa cliente dificulta la depuración. La manera adecuada de estructurar un controlador de excepciones es la siguiente:

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

Este controlador de excepciones tiene la ventaja de dejar pasar un determinado intervalo de errores. El servidor nunca devolverá estos errores, ya que indican un problema del lado cliente.

Además, se recomienda usar los atributos strict **\[** [ \_ context \_ handle](/windows/desktop/Midl/strict-context-handle) y type strict context **\]** **\[** [ \_ \_ \_ handle](/windows/desktop/Midl/type-strict-context-handle)para asegurarse de que el tiempo de ejecución de RPC crea un identificador de contexto en una interfaz que se puede pasar como argumento solo a los métodos de esa **\]** interfaz. Si lo hace, evitará los errores del servidor que se producen cuando se abren los identificadores de contexto y se pasan entre distintas interfaces que existen dentro del mismo proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[strict \_ context \_ handle](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[identificador \_ de contexto estricto de \_ \_ tipo](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 