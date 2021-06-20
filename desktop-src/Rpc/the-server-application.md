---
title: La aplicación de servidor
description: Vea la parte de la aplicación de servidor de un ejemplo de llamada a procedimiento remoto (RPC). El ejemplo es de la aplicación "Hola mundo" del SDK de plataforma.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b8a2bb66fd415a9b8f778134edb4903f88a717
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406068"
---
# <a name="the-server-application"></a><span data-ttu-id="13b5a-104">La aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="13b5a-104">The Server Application</span></span>

<span data-ttu-id="13b5a-105">El ejemplo siguiente es de la aplicación "Hola mundo" en el directorio RPC Hello del \\ Kit de desarrollo de software (SDK) de plataforma.</span><span class="sxs-lookup"><span data-stu-id="13b5a-105">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="13b5a-106">El lado servidor de la aplicación distribuida informa al sistema de que sus servicios están disponibles.</span><span class="sxs-lookup"><span data-stu-id="13b5a-106">The server side of the distributed application informs the system that its services are available.</span></span> <span data-ttu-id="13b5a-107">A continuación, espera las solicitudes de cliente.</span><span class="sxs-lookup"><span data-stu-id="13b5a-107">It then waits for client requests.</span></span> <span data-ttu-id="13b5a-108">El compilador MIDL debe usarse con el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="13b5a-108">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="13b5a-109">Según el tamaño de la aplicación y las preferencias de codificación, puede optar por implementar procedimientos remotos en uno o varios archivos independientes.</span><span class="sxs-lookup"><span data-stu-id="13b5a-109">Depending on the size of your application and your coding preferences, you can choose to implement remote procedures in one or more separate files.</span></span> <span data-ttu-id="13b5a-110">En este programa de tutorial, el archivo de origen Hellos.c contiene la rutina de servidor principal.</span><span class="sxs-lookup"><span data-stu-id="13b5a-110">In this tutorial program, the source file Hellos.c contains the main server routine.</span></span> <span data-ttu-id="13b5a-111">El archivo Hellop.c contiene el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="13b5a-111">The file Hellop.c contains the remote procedure.</span></span>

<span data-ttu-id="13b5a-112">La ventaja de organizar los procedimientos remotos en archivos independientes es que los procedimientos se pueden vincular con un programa independiente para depurar el código antes de convertirlo en una aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="13b5a-112">The benefit of organizing the remote procedures in separate files is that the procedures can be linked with a standalone program to debug the code before it is converted to a distributed application.</span></span> <span data-ttu-id="13b5a-113">Una vez que los procedimientos funcionan en el programa independiente, puede compilar y vincular los archivos de origen que contienen los procedimientos remotos con la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="13b5a-113">After the procedures work in the standalone program, you can compile and link the source files containing the remote procedures with the server application.</span></span> <span data-ttu-id="13b5a-114">Al igual que con el archivo de origen de aplicación cliente, el archivo de origen de aplicación de servidor debe incluir el archivo de encabezado Hello.h.</span><span class="sxs-lookup"><span data-stu-id="13b5a-114">As with the client-application source file, the server-application source file must include the Hello.h header file.</span></span>

<span data-ttu-id="13b5a-115">El servidor llama a las funciones en tiempo de ejecución [**rpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) y [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para que la información de enlace esté disponible para el cliente.</span><span class="sxs-lookup"><span data-stu-id="13b5a-115">The server calls the RPC run-time functions [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) and [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to make binding information available to the client.</span></span> <span data-ttu-id="13b5a-116">Este programa de ejemplo pasa el nombre del identificador de interfaz **a RpcServerRegisterIf**.</span><span class="sxs-lookup"><span data-stu-id="13b5a-116">This example program passes the interface handle name to **RpcServerRegisterIf**.</span></span> <span data-ttu-id="13b5a-117">Los demás parámetros se establecen en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="13b5a-117">The other parameters are set to **NULL**.</span></span> <span data-ttu-id="13b5a-118">A continuación, el servidor llama [**a la función RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para indicar que está esperando solicitudes de cliente.</span><span class="sxs-lookup"><span data-stu-id="13b5a-118">The server then calls the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to indicate that it is waiting for client requests.</span></span>

<span data-ttu-id="13b5a-119">La aplicación de servidor también debe incluir las dos funciones de administración de memoria a las que llama el código auxiliar del servidor: [**midl \_ user \_ allocate**](the-midl-user-allocate-function.md) y [**midl \_ user \_ free**](the-midl-user-free-function.md).</span><span class="sxs-lookup"><span data-stu-id="13b5a-119">The server application must also include the two memory management functions that the server stub calls: [**midl\_user\_allocate**](the-midl-user-allocate-function.md) and [**midl\_user\_free**](the-midl-user-free-function.md).</span></span> <span data-ttu-id="13b5a-120">Estas funciones asignan y liberan memoria en el servidor cuando un procedimiento remoto pasa parámetros al servidor.</span><span class="sxs-lookup"><span data-stu-id="13b5a-120">These functions allocate and free memory on the server when a remote procedure passes parameters to the server.</span></span> <span data-ttu-id="13b5a-121">En este programa de ejemplo, **midl \_ user \_ allocate** y **midl \_ user \_ free** son simplemente contenedores para las funciones [**malloc**](pointers-and-memory-allocation.md) y **free** de la biblioteca de C.</span><span class="sxs-lookup"><span data-stu-id="13b5a-121">In this example program, **midl\_user\_allocate** and **midl\_user\_free** are simply wrappers for the C-library functions [**malloc**](pointers-and-memory-allocation.md) and **free**.</span></span> <span data-ttu-id="13b5a-122">(Tenga en cuenta que, en las declaraciones de reenvío generadas por el compilador MIDL, "MIDL" está en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="13b5a-122">(Note that, in the MIDL compiler- generated forward declarations, "MIDL" is uppercase.</span></span> <span data-ttu-id="13b5a-123">El archivo de encabezado Rpc rpcl.h define midl user free y midl user allocate para que sea midL user free y \_ \_ \_ \_ \_ \_ MIDL \_ user \_ allocate, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="13b5a-123">The header file Rpcndr.h defines midl\_user\_free and midl\_user\_allocate to be MIDL\_user\_free and MIDL\_user\_allocate, respectively.)</span></span>


```C++
/* file: hellos.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h"
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszSecurity         = NULL; 
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned int    cMinCalls = 1;
    unsigned int    fDontWait = FALSE;
 
    status = RpcServerUseProtseqEp(pszProtocolSequence,
                                   RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                                   pszEndpoint,
                                   pszSecurity); 
 
    if (status) exit(status);
 
    status = RpcServerRegisterIf(hello_ServerIfHandle,  
                                 NULL,   
                                 NULL); 
 
    if (status) exit(status);
 
    status = RpcServerListen(cMinCalls,
                             RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                             fDontWait);
 
    if (status) exit(status);
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



 

 




