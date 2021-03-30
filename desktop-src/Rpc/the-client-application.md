---
title: Aplicación cliente
description: El ejemplo siguiente es de la aplicación ' Hola mundo ' en el \\ directorio RPC Hello del kit de desarrollo de software (SDK) de la plataforma.
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f97c7c35e00d3f36c645bfad2825dbada5e3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488182"
---
# <a name="the-client-application"></a>Aplicación cliente

El ejemplo siguiente es de la aplicación ' Hola mundo ' en el \\ directorio RPC Hello del kit de desarrollo de software (SDK) de la plataforma. El archivo de código fuente Helloc. c contiene una directiva para incluir el archivo de encabezado generado por MIDL, Hello. h. Dentro de Hello. h hay directivas para incluir RPC. h y rpcndr. h, que contienen las definiciones de las rutinas en tiempo de ejecución de RPC, **HelloProc** y **Shutdown**, y los tipos de datos que usan las aplicaciones cliente y servidor. El compilador MIDL debe usarse con el ejemplo siguiente.

Dado que el cliente administra su conexión con el servidor, la aplicación cliente llama a las funciones en tiempo de ejecución para establecer un identificador para el servidor y liberar este identificador una vez completadas las llamadas a procedimiento remoto. La función [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combina los componentes del identificador de enlace en una representación de cadena de ese identificador y asigna memoria para el enlace de cadenas. La función [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) crea un identificador de enlace de servidor, **Hello \_ ClientIfHandle**, para la aplicación cliente a partir de esa representación de cadena.

En la llamada a [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), los parámetros no especifican el UUID porque en este tutorial se supone que hay una sola implementación de la interfaz "Hello". Además, la llamada no especifica una dirección de red porque la aplicación usará el valor predeterminado, que es el equipo host local. La secuencia de protocolo es una cadena de caracteres que representa el transporte de red subyacente. El punto de conexión es un nombre que es específico de la secuencia de protocolos. En este ejemplo se usan canalizaciones con nombre para su transporte de red, por lo que la secuencia del protocolo es "ncacn \_ NP". El nombre del punto de conexión es " \\ Pipe \\ Hello".

Las llamadas a procedimientos remotos, **HelloProc** y **Shutdown** reales, tienen lugar dentro del controlador de excepciones RPC, un conjunto de macros que permiten controlar las excepciones que se producen fuera del código de la aplicación. Si el módulo de tiempo de ejecución de RPC informa de una excepción, el control pasa al bloque [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) . Aquí es donde insertaría código para realizar cualquier limpieza necesaria y, a continuación, salir correctamente. Este programa de ejemplo informa simplemente al usuario de que se ha producido una excepción. Si no desea usar excepciones, puede usar los atributos ACF [ \_ Estado de comunicación](/windows/desktop/Midl/comm-status) y [ \_ Estado de error](/windows/desktop/Midl/fault-status) para notificar los errores.

Una vez completadas las llamadas a procedimiento remoto, el cliente llama primero a [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para liberar la memoria que se asignó para el enlace de cadenas. Tenga en cuenta que una vez que se ha creado el identificador de enlace, un programa cliente puede liberar un enlace de cadena en cualquier momento. El cliente siguiente llama a [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) para liberar el identificador.


```C++
/* file: helloc.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h" 
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszUuid             = NULL;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszNetworkAddress   = NULL;
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned char * pszOptions          = NULL;
    unsigned char * pszStringBinding    = NULL;
    unsigned char * pszString           = "hello, world";
    unsigned long ulCode;
 
    status = RpcStringBindingCompose(pszUuid,
                                     pszProtocolSequence,
                                     pszNetworkAddress,
                                     pszEndpoint,
                                     pszOptions,
                                     &pszStringBinding);
    if (status) exit(status);

    status = RpcBindingFromStringBinding(pszStringBinding, &hello_ClientIfHandle);
 
    if (status) exit(status);
 
    RpcTryExcept  
    {
        HelloProc(pszString);
        Shutdown();
    }
    RpcExcept(1) 
    {
        ulCode = RpcExceptionCode();
        printf("Runtime reported exception 0x%lx = %ld\n", ulCode, ulCode);
    }
    RpcEndExcept
 
    status = RpcStringFree(&pszStringBinding); 
 
    if (status) exit(status);
 
    status = RpcBindingFree(&hello_IfHandle);
 
    if (status) exit(status);

    exit(0);
}

/******************************************************/
/*         MIDL allocate and free                     */
/******************************************************/
 
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t len)
{
    return(malloc(len));
}
 
void __RPC_USER midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 