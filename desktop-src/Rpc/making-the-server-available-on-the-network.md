---
title: Poner el servidor a disposición en la red
description: Para que una aplicación de servidor pueda aceptar llamadas a procedimientos remotos, debe estar disponible en la red.
ms.assetid: 1fad55e2-7221-4153-b530-b36ea42e03e1
keywords:
- RPC llamada a procedimiento remoto, tareas, que hacen que el servidor esté disponible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2826e4e63e7e78e7f87f6afc120b80e885cd3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075930"
---
# <a name="making-the-server-available-on-the-network"></a><span data-ttu-id="be241-104">Poner el servidor a disposición en la red</span><span class="sxs-lookup"><span data-stu-id="be241-104">Making the Server Available on the Network</span></span>

<span data-ttu-id="be241-105">Para que una aplicación de servidor pueda aceptar llamadas a procedimientos remotos, debe estar disponible en la red.</span><span class="sxs-lookup"><span data-stu-id="be241-105">Before a server application can accept remote procedure calls, it must be available on the network.</span></span> <span data-ttu-id="be241-106">Para ello, el servidor indica al tiempo de ejecución de RPC que está dispuesto a aceptar llamadas en una o varias secuencias de protocolo.</span><span class="sxs-lookup"><span data-stu-id="be241-106">To do this, the server indicates to the RPC Run time that it is willing to accept calls on one or more protocol sequences.</span></span> <span data-ttu-id="be241-107">La elección de las secuencias de protocolo que admite una aplicación de servidor es una decisión importante; las distintas secuencias de protocolo tienen funcionalidades muy diferentes.</span><span class="sxs-lookup"><span data-stu-id="be241-107">Choosing the protocol sequences a server application supports is an important decision; different protocol sequences have very different capabilities.</span></span> <span data-ttu-id="be241-108">Los servidores que esperan que se reciban llamadas localmente deben usar **ncalrpc**.</span><span class="sxs-lookup"><span data-stu-id="be241-108">Servers that expect calls to be received locally should use **ncalrpc**.</span></span> <span data-ttu-id="be241-109">Los servidores que aceptan llamadas remotas deben usar **ncacn \_ IP \_ TCP**.</span><span class="sxs-lookup"><span data-stu-id="be241-109">Servers that accept remote calls should use **ncacn\_ip\_tcp**.</span></span> <span data-ttu-id="be241-110">Los servidores no deben comprobar que la secuencia de protocolos en la que reciben llamadas sea la secuencia de protocolos en la que esperan recibir llamadas.</span><span class="sxs-lookup"><span data-stu-id="be241-110">Servers should not verify that the protocol sequence on which they receive calls is the protocol sequence on which they expect to receive calls.</span></span> <span data-ttu-id="be241-111">Para obtener más información, vea tener cuidado de otros extremos de RPC que se ejecutan en el mismo proceso en las mejores prácticas de programación de RPC.</span><span class="sxs-lookup"><span data-stu-id="be241-111">See Be Wary of Other RPC Endpoints Running in the Same Process in Best RPC Programming Practices for more information.</span></span>

<span data-ttu-id="be241-112">En el ejemplo siguiente se usa **ncacn \_ IP \_ TCP**.</span><span class="sxs-lookup"><span data-stu-id="be241-112">The following example uses **ncacn\_ip\_tcp**.</span></span>

<span data-ttu-id="be241-113">La mayoría de los programas de servidor utilizan todas las secuencias de protocolo disponibles en la red.</span><span class="sxs-lookup"><span data-stu-id="be241-113">Most server programs use all protocol sequences available on the network.</span></span> <span data-ttu-id="be241-114">Para ello, invocan la función [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) , tal y como se muestra en el siguiente fragmento de código:</span><span class="sxs-lookup"><span data-stu-id="be241-114">To do this, they invoke the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function, as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerUseAllProtseq(
    L"ncacn_ip_tcp",
    RPC_C_PROTSEQ_MAX_REQS_DEFAULT,    // Protseq dependent parameter
    NULL);                             // Always specify NULL here.
```



<span data-ttu-id="be241-115">El primer parámetro de la función [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) es la secuencia de protocolos.</span><span class="sxs-lookup"><span data-stu-id="be241-115">The first parameter to the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) function is the protocol sequence.</span></span> <span data-ttu-id="be241-116">El segundo parámetro depende de la secuencia de protocolos.</span><span class="sxs-lookup"><span data-stu-id="be241-116">The second parameter is dependent on the protocol sequence.</span></span> <span data-ttu-id="be241-117">Como se muestra en el fragmento de código, la mayoría de los programas de servidor establecen este parámetro en el **\_ \_ \_ \_ \_ valor predeterminado de PROTSEQ Max req**.</span><span class="sxs-lookup"><span data-stu-id="be241-117">As illustrated in the code fragment, most server programs set this parameter to **RPC\_C\_PROTSEQ\_MAX\_REQS\_DEFAULT**.</span></span> <span data-ttu-id="be241-118">Este valor establece la biblioteca RPC para usar el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="be241-118">This value sets the RPC library to use the default value.</span></span> <span data-ttu-id="be241-119">El tercer parámetro es un descriptor de seguridad y no debe usarse en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="be241-119">The third parameter is a security descriptor and should not be used in applications.</span></span> <span data-ttu-id="be241-120">Para obtener más información, consulte [**seguridad**](security.md).</span><span class="sxs-lookup"><span data-stu-id="be241-120">For more information, see [**Security**](security.md).</span></span>

<span data-ttu-id="be241-121">También puede usar las funciones [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep)o [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) .</span><span class="sxs-lookup"><span data-stu-id="be241-121">You can also use the [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex), [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep), or [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) functions.</span></span>

<span data-ttu-id="be241-122">Después de que una aplicación de servidor Seleccione al menos una secuencia de protocolos, los servidores que usen puntos de conexión dinámicos deben crear información de enlace para cada secuencia de protocolo que use.</span><span class="sxs-lookup"><span data-stu-id="be241-122">After a server application selects at least one protocol sequence, servers that use dynamic endpoints must create binding information for each protocol sequence it uses.</span></span> <span data-ttu-id="be241-123">El servidor almacena la información de enlace en un vector de enlace que, a continuación, puede exportar al servicio del asignador de extremos.</span><span class="sxs-lookup"><span data-stu-id="be241-123">The server stores the binding information in a binding vector that it can then export to the endpoint mapper service.</span></span>

<span data-ttu-id="be241-124">Utilice la función [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) para obtener un vector de enlace para la aplicación de servidor, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="be241-124">Use the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function to obtain a binding vector for the server application, as shown in the following example:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_VECTOR *rpcBindingVector;
 
status = RpcServerInqBindings(&rpcBindingVector);
```



<span data-ttu-id="be241-125">El único parámetro que se pasa a la función [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) es un puntero a un puntero a una estructura de [**\_ \_ Vector de enlace RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) .</span><span class="sxs-lookup"><span data-stu-id="be241-125">The only parameter passed to the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) function is a pointer to a pointer to an [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector) structure.</span></span> <span data-ttu-id="be241-126">La biblioteca en tiempo de ejecución de RPC asigna dinámicamente una matriz de vectores de enlace y almacena la dirección de la matriz en la variable de parámetro (en este caso, **rpcBindingVector**).</span><span class="sxs-lookup"><span data-stu-id="be241-126">The RPC run-time library dynamically allocates an array of binding vectors and stores the address of the array in the parameter variable (in this case, **rpcBindingVector**).</span></span> <span data-ttu-id="be241-127">Cada aplicación de servidor es responsable de liberar este vector de enlace mediante la función [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) una vez que ha terminado de utilizarlo (por ejemplo, después de pasarlo a las funciones adecuadas).</span><span class="sxs-lookup"><span data-stu-id="be241-127">Each server application is responsible for freeing this binding vector using the [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree) function once it has finished using it (for example, after it has passed it to the appropriate functions).</span></span>

 

 




