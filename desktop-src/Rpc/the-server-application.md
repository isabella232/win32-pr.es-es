---
title: La aplicación de servidor
description: El ejemplo siguiente es de la aplicación ' Hola mundo ' en el \\ directorio RPC Hello del kit de desarrollo de software (SDK) de la plataforma.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6f13e2c8fecdcff820c62f3076dd2a8edd1a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903500"
---
# <a name="the-server-application"></a><span data-ttu-id="4840a-103">La aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="4840a-103">The Server Application</span></span>

<span data-ttu-id="4840a-104">El ejemplo siguiente es de la aplicación ' Hola mundo ' en el \\ directorio RPC Hello del kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="4840a-104">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="4840a-105">El lado servidor de la aplicación distribuida informa al sistema de que sus servicios están disponibles.</span><span class="sxs-lookup"><span data-stu-id="4840a-105">The server side of the distributed application informs the system that its services are available.</span></span> <span data-ttu-id="4840a-106">Después espera las solicitudes del cliente.</span><span class="sxs-lookup"><span data-stu-id="4840a-106">It then waits for client requests.</span></span> <span data-ttu-id="4840a-107">El compilador MIDL debe usarse con el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="4840a-107">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="4840a-108">En función del tamaño de la aplicación y las preferencias de codificación, puede elegir implementar procedimientos remotos en uno o varios archivos independientes.</span><span class="sxs-lookup"><span data-stu-id="4840a-108">Depending on the size of your application and your coding preferences, you can choose to implement remote procedures in one or more separate files.</span></span> <span data-ttu-id="4840a-109">En este programa tutorial, el archivo de código fuente Hello. c contiene la rutina del servidor principal.</span><span class="sxs-lookup"><span data-stu-id="4840a-109">In this tutorial program, the source file Hellos.c contains the main server routine.</span></span> <span data-ttu-id="4840a-110">El archivo Hellop. c contiene el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="4840a-110">The file Hellop.c contains the remote procedure.</span></span>

<span data-ttu-id="4840a-111">La ventaja de organizar los procedimientos remotos en archivos independientes es que los procedimientos se pueden vincular con un programa independiente para depurar el código antes de que se convierta en una aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="4840a-111">The benefit of organizing the remote procedures in separate files is that the procedures can be linked with a standalone program to debug the code before it is converted to a distributed application.</span></span> <span data-ttu-id="4840a-112">Una vez que los procedimientos funcionan en el programa independiente, puede compilar y vincular los archivos de origen que contienen los procedimientos remotos con la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="4840a-112">After the procedures work in the standalone program, you can compile and link the source files containing the remote procedures with the server application.</span></span> <span data-ttu-id="4840a-113">Al igual que con el archivo de origen de la aplicación cliente, el archivo de origen de la aplicación de servidor debe incluir el archivo de encabezado Hello. h.</span><span class="sxs-lookup"><span data-stu-id="4840a-113">As with the client-application source file, the server-application source file must include the Hello.h header file.</span></span>

<span data-ttu-id="4840a-114">El servidor llama a las funciones en tiempo de ejecución de RPC [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) y [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para hacer que la información de enlace esté disponible para el cliente.</span><span class="sxs-lookup"><span data-stu-id="4840a-114">The server calls the RPC run-time functions [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) and [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to make binding information available to the client.</span></span> <span data-ttu-id="4840a-115">Este programa de ejemplo pasa el nombre del identificador de interfaz a **RpcServerRegisterIf**.</span><span class="sxs-lookup"><span data-stu-id="4840a-115">This example program passes the interface handle name to **RpcServerRegisterIf**.</span></span> <span data-ttu-id="4840a-116">Los demás parámetros se establecen en **null**.</span><span class="sxs-lookup"><span data-stu-id="4840a-116">The other parameters are set to **NULL**.</span></span> <span data-ttu-id="4840a-117">A continuación, el servidor llama a la función [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para indicar que está esperando solicitudes de cliente.</span><span class="sxs-lookup"><span data-stu-id="4840a-117">The server then calls the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to indicate that it is waiting for client requests.</span></span>

<span data-ttu-id="4840a-118">La aplicación de servidor también debe incluir las dos funciones de administración de memoria a las que llama el código auxiliar del servidor: la [**\_ \_ asignación de usuarios de MIDL**](the-midl-user-allocate-function.md) y el [**usuario de MIDL \_ \_**](the-midl-user-free-function.md).</span><span class="sxs-lookup"><span data-stu-id="4840a-118">The server application must also include the two memory management functions that the server stub calls: [**midl\_user\_allocate**](the-midl-user-allocate-function.md) and [**midl\_user\_free**](the-midl-user-free-function.md).</span></span> <span data-ttu-id="4840a-119">Estas funciones asignan y liberan memoria en el servidor cuando un procedimiento remoto pasa parámetros al servidor.</span><span class="sxs-lookup"><span data-stu-id="4840a-119">These functions allocate and free memory on the server when a remote procedure passes parameters to the server.</span></span> <span data-ttu-id="4840a-120">En este programa de ejemplo, la **\_ \_ asignación de usuarios de MIDL** y el usuario de **MIDL \_ \_ Free** son simplemente contenedores para las funciones de la biblioteca de C [**malloc**](pointers-and-memory-allocation.md) y **Free**.</span><span class="sxs-lookup"><span data-stu-id="4840a-120">In this example program, **midl\_user\_allocate** and **midl\_user\_free** are simply wrappers for the C-library functions [**malloc**](pointers-and-memory-allocation.md) and **free**.</span></span> <span data-ttu-id="4840a-121">(Tenga en cuenta que, en las declaraciones adelantadas generadas por el compilador MIDL, "MIDL" está en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="4840a-121">(Note that, in the MIDL compiler- generated forward declarations, "MIDL" is uppercase.</span></span> <span data-ttu-id="4840a-122">El archivo de encabezado Rpcndr. h define el usuario de MIDL \_ \_ Free y el \_ usuario \_ de MIDL asigna para que sea gratuito del usuario de MIDL y que el \_ usuario de \_ MIDL \_ \_ asigne, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="4840a-122">The header file Rpcndr.h defines midl\_user\_free and midl\_user\_allocate to be MIDL\_user\_free and MIDL\_user\_allocate, respectively.)</span></span>


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



 

 




