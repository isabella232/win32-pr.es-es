---
title: Aplicación cliente
description: Vea la parte de la aplicación cliente de un ejemplo de llamada a procedimiento remoto (RPC). El ejemplo siguiente es de la aplicación "Hola mundo" en el SDK de plataforma.
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e0b798543cd70e61f3ff1161503fa64710e53e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405018"
---
# <a name="the-client-application"></a><span data-ttu-id="fd6cc-104">Aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="fd6cc-104">The Client Application</span></span>

<span data-ttu-id="fd6cc-105">El ejemplo siguiente es de la aplicación "Hola mundo" en el directorio RPC Hello del \\ Kit de desarrollo de software (SDK) de plataforma.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-105">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="fd6cc-106">El archivo de código fuente Helloc.c contiene una directiva para incluir el archivo de encabezado generado por MIDL, Hello.h.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-106">The Helloc.c source file contains a directive to include the MIDL-generated header file, Hello.h.</span></span> <span data-ttu-id="fd6cc-107">Dentro de Hello.h hay directivas que incluyen Rpc.h y rpc rpc.h, que contienen las definiciones de las rutinas en tiempo de ejecución rpc, **HelloProc** y **Shutdown,** y los tipos de datos que usan las aplicaciones cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-107">Within Hello.h are directives to include Rpc.h and rpcndr.h, which contain the definitions for the RPC run-time routines, **HelloProc** and **Shutdown**, and data types that the client and server applications use.</span></span> <span data-ttu-id="fd6cc-108">El compilador MIDL debe usarse con el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-108">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="fd6cc-109">Dado que el cliente administra su conexión con el servidor, la aplicación cliente llama a funciones en tiempo de ejecución para establecer un identificador para el servidor y liberar este identificador una vez completadas las llamadas a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-109">Because the client is managing its connection to the server, the client application calls run-time functions to establish a handle to the server and to release this handle after the remote procedure calls are complete.</span></span> <span data-ttu-id="fd6cc-110">La función [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combina los componentes del identificador de enlace en una representación de cadena de ese identificador y asigna memoria para el enlace de cadena.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-110">The function [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combines the components of the binding handle into a string representation of that handle and allocates memory for the string binding.</span></span> <span data-ttu-id="fd6cc-111">La función [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) crea un identificador de enlace de servidor, **hello \_ ClientIfHandle**, para la aplicación cliente a partir de esa representación de cadena.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-111">The function [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) creates a server binding handle, **hello\_ClientIfHandle**, for the client application from that string representation.</span></span>

<span data-ttu-id="fd6cc-112">En la llamada a [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), los parámetros no especifican el UUID porque en este tutorial se supone que solo hay una implementación de la interfaz "hello".</span><span class="sxs-lookup"><span data-stu-id="fd6cc-112">In the call to [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), the parameters do not specify the UUID because this tutorial assumes there is just one implementation of the interface "hello."</span></span> <span data-ttu-id="fd6cc-113">Además, la llamada no especifica una dirección de red porque la aplicación usará el valor predeterminado, que es el equipo host local.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-113">In addition, the call does not specify a network address because the application will use the default, which is the local host machine.</span></span> <span data-ttu-id="fd6cc-114">La secuencia de protocolo es una cadena de caracteres que representa el transporte de red subyacente.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-114">The protocol sequence is a character string that represents the underlying network transport.</span></span> <span data-ttu-id="fd6cc-115">El punto de conexión es un nombre que es específico de la secuencia del protocolo.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-115">The endpoint is a name which is specific to the protocol sequence.</span></span> <span data-ttu-id="fd6cc-116">En este ejemplo se usan canalizaciones con nombre para su transporte de red, por lo que la secuencia de protocolo es "ncacn \_ np".</span><span class="sxs-lookup"><span data-stu-id="fd6cc-116">This example uses named pipes for its network transport, so the protocol sequence is "ncacn\_np".</span></span> <span data-ttu-id="fd6cc-117">El nombre del punto de conexión es \\ "pipe \\ hello".</span><span class="sxs-lookup"><span data-stu-id="fd6cc-117">The endpoint name is "\\pipe\\hello".</span></span>

<span data-ttu-id="fd6cc-118">Las llamadas a procedimiento remoto reales, **HelloProc** y **Shutdown,** tienen lugar dentro del controlador de excepciones RPC, un conjunto de macros que permiten controlar las excepciones que se producen fuera del código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-118">The actual remote procedure calls, **HelloProc** and **Shutdown**, take place within the RPC exception handler—a set of macros that let you control exceptions that occur outside the application code.</span></span> <span data-ttu-id="fd6cc-119">Si el módulo rpc en tiempo de ejecución notifica una excepción, el control pasa al [**bloque RpcExcept.**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)</span><span class="sxs-lookup"><span data-stu-id="fd6cc-119">If the RPC run-time module reports an exception, control passes to the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) block.</span></span> <span data-ttu-id="fd6cc-120">Aquí es donde insertaría código para realizar la limpieza necesaria y, a continuación, salir correctamente.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-120">This is where you would insert code to do any needed cleanup and then exit gracefully.</span></span> <span data-ttu-id="fd6cc-121">Este programa de ejemplo simplemente informa al usuario de que se ha producido una excepción.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-121">This example program simply informs the user that an exception occurred.</span></span> <span data-ttu-id="fd6cc-122">Si no desea usar excepciones, puede usar el [ \_ ](/windows/desktop/Midl/comm-status) estado del mensaje de atributos de ACF y el estado de error [para \_ ](/windows/desktop/Midl/fault-status) notificar los errores.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-122">If you do not want to use exceptions, you can use the ACF attributes [comm\_status](/windows/desktop/Midl/comm-status) and [fault\_status](/windows/desktop/Midl/fault-status) to report errors.</span></span>

<span data-ttu-id="fd6cc-123">Una vez completadas las llamadas a procedimiento remoto, el cliente llama primero a [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para liberar la memoria que se asignó para el enlace de cadena.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-123">After the remote procedure calls are completed, the client first calls [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) to free the memory that was allocated for the string binding.</span></span> <span data-ttu-id="fd6cc-124">Tenga en cuenta que una vez creado el identificador de enlace, un programa cliente puede liberar un enlace de cadena en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-124">Note that once the binding handle has been created, a client program can free a string binding at any time.</span></span> <span data-ttu-id="fd6cc-125">A continuación, el [**cliente llama a RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) para liberar el identificador.</span><span class="sxs-lookup"><span data-stu-id="fd6cc-125">The client next calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to release the handle.</span></span>


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



 

 