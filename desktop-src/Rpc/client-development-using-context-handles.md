---
title: Desarrollo de cliente con identificadores de contexto
description: El único uso de un programa cliente para un identificador de contexto es pasarlo al servidor cada vez que el cliente realiza una llamada a procedimiento remoto.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c7d2dfca901085c743b25eb233ee2493b893e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532367"
---
# <a name="client-development-using-context-handles"></a><span data-ttu-id="46994-103">Desarrollo de cliente con identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="46994-103">Client Development Using Context Handles</span></span>

<span data-ttu-id="46994-104">El único uso de un programa cliente para un identificador de contexto es pasarlo al servidor cada vez que el cliente realiza una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="46994-104">The only use a client program has for a context handle is to pass it to the server each time the client makes a remote procedure call.</span></span> <span data-ttu-id="46994-105">No es necesario que la aplicación cliente tenga acceso al contenido del identificador.</span><span class="sxs-lookup"><span data-stu-id="46994-105">The client application does not need to access the contents of the handle.</span></span> <span data-ttu-id="46994-106">No debe intentar cambiar los datos del identificador de contexto de ningún modo.</span><span class="sxs-lookup"><span data-stu-id="46994-106">It should not try to change the context handle data in any way.</span></span> <span data-ttu-id="46994-107">Los procedimientos remotos que invoca el cliente realizan todas las operaciones necesarias en el contexto del servidor.</span><span class="sxs-lookup"><span data-stu-id="46994-107">The remote procedures that the client invokes perform all necessary operations on the server's context.</span></span>

<span data-ttu-id="46994-108">Antes de solicitar un identificador de contexto de un servidor, los clientes deben establecer un enlace con el servidor.</span><span class="sxs-lookup"><span data-stu-id="46994-108">Prior to requesting a context handle from a server, clients must establish a binding with the server.</span></span> <span data-ttu-id="46994-109">El cliente puede utilizar un identificador de enlace automático, implícito o explícito.</span><span class="sxs-lookup"><span data-stu-id="46994-109">The client may use an automatic, implicit, or explicit binding handle.</span></span> <span data-ttu-id="46994-110">Con un identificador de enlace válido, el cliente puede llamar a un procedimiento remoto en el servidor que devuelva un identificador de contexto abierto (distinto de **null**) o pase uno a través de un parámetro **\[ out \]** en la lista de parámetros del procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="46994-110">With a valid binding handle, the client can call a remote procedure on the server that either returns an opened (non-**NULL**) context handle or passes one through an **\[out\]** parameter in the remote procedure's parameter list.</span></span>

<span data-ttu-id="46994-111">Los clientes pueden usar identificadores de contexto abiertos de la manera que requieran.</span><span class="sxs-lookup"><span data-stu-id="46994-111">Clients may use opened context handles in any way they require.</span></span> <span data-ttu-id="46994-112">Sin embargo, deberían invalidar el identificador cuando ya no lo necesiten.</span><span class="sxs-lookup"><span data-stu-id="46994-112">They should, however, invalidate the handle when they no longer need it.</span></span> <span data-ttu-id="46994-113">Hay dos maneras de hacerlo:</span><span class="sxs-lookup"><span data-stu-id="46994-113">There are two way to do this:</span></span>

-   <span data-ttu-id="46994-114">Para invocar un procedimiento remoto ofrecido por el programa de servidor que libera el contexto y cierra el identificador de contexto (lo establece en **null**).</span><span class="sxs-lookup"><span data-stu-id="46994-114">To invoke a remote procedure offered by the server program that frees the context and closes the context handle (sets it to **NULL**).</span></span>
-   <span data-ttu-id="46994-115">Cuando no se puede tener acceso al servidor, llame a la función [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="46994-115">When the server is unreachable, call the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="46994-116">El segundo enfoque solo limpia el estado del lado cliente y no limpia el estado del lado servidor, por lo que solo se debe usar cuando se sospecha de la partición de red, y el cliente y el servidor realizarán una limpieza independiente.</span><span class="sxs-lookup"><span data-stu-id="46994-116">The second approach only cleans up the client side state, and does not clean up the server-side state, so it should be used only when network partition is suspected, and the client and the server will do an independent cleanup.</span></span> <span data-ttu-id="46994-117">El servidor realiza una limpieza independiente mediante la rutina de ejecución, el cliente lo hace mediante la función [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="46994-117">The server performs independent cleanup through the run-down routine, the client does so using the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="46994-118">En el siguiente fragmento de código se muestra un ejemplo de cómo un cliente puede utilizar un identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="46994-118">The following code fragment presents an example of how a client might use a context handle.</span></span> <span data-ttu-id="46994-119">Para ver la definición de la interfaz que usa este ejemplo, consulte [desarrollo de interfaces mediante identificadores de contexto](interface-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="46994-119">To view the definition of the interface that this example uses, see [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span> <span data-ttu-id="46994-120">Para la implementación del servidor, consulte [desarrollo de servidores con identificadores de contexto](server-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="46994-120">For the server implementation, see [Server Development Using Context Handles](server-development-using-context-handles.md).</span></span>

<span data-ttu-id="46994-121">En este ejemplo, el cliente llama a RemoteOpen para obtener un identificador de contexto que contiene datos válidos.</span><span class="sxs-lookup"><span data-stu-id="46994-121">In this example, the client calls RemoteOpen to obtain a context handle that contains valid data.</span></span> <span data-ttu-id="46994-122">Después, el cliente puede utilizar el identificador de contexto en las llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="46994-122">The client can then use the context handle in remote procedure calls.</span></span> <span data-ttu-id="46994-123">Dado que ya no necesita el identificador de enlace, el cliente puede liberar el identificador explícito que se usa para crear el identificador de contexto:</span><span class="sxs-lookup"><span data-stu-id="46994-123">Because it no longer needs the binding handle, the client can free the explicit handle it used to create the context handle:</span></span>


```C++
// cxhndlc.c  (fragment of client side application)
printf("Calling the remote procedure RemoteOpen\n");
if (RemoteOpen(&phContext, pszFileName) < 0) 
{
    printf("Unable to open %s\n", pszFileName);
    Shutdown();
    exit(2);
}
 
// Now the context handle also manages the binding.
// The variable hBindingHandle is a valid binding handle.
status = RpcBindingFree(&hBindingHandle);
printf("RpcBindingFree returned 0x%x\n", status);
if (status) 
    exit(status);
```



<span data-ttu-id="46994-124">La aplicación cliente de este ejemplo usa un procedimiento denominado RemoteRead para leer un archivo de datos en el servidor hasta que encuentra un final de archivo.</span><span class="sxs-lookup"><span data-stu-id="46994-124">The client application in this example uses a procedure called RemoteRead to read a data file on the server until it encounters an end of file.</span></span> <span data-ttu-id="46994-125">A continuación, cierra el archivo llamando a RemoteClose.</span><span class="sxs-lookup"><span data-stu-id="46994-125">It then closes the file by calling RemoteClose.</span></span> <span data-ttu-id="46994-126">El identificador de contexto aparece como un parámetro en las funciones RemoteRead y RemoteClose como:</span><span class="sxs-lookup"><span data-stu-id="46994-126">The context handle appears as a parameter in the RemoteRead and RemoteClose functions as:</span></span>


```C++
printf("Calling the remote procedure RemoteRead\n");
do 
{
    cbRead = 1024; // Using a 1K buffer
    RemoteRead(phContext, pbBuf, &cbRead);
    // cbRead contains the number of bytes actually read.
    for (int i = 0; i < cbRead; i++)
        putchar(*(pbBuf+i));
} while(cbRead);
 
printf("Calling the remote procedure RemoteClose\n");
if (RemoteClose(&phContext) < 0 ) 
{
    printf("Close failed on %s\n", pszFileName);
    exit(2);
}
```



 

 




