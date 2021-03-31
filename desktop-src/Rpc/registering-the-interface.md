---
title: Registrar la interfaz
description: El registro de la interfaz que admite un programa de servidor permite que las llamadas a procedimientos remotos de programas cliente se envíen a la rutina de servidor adecuada.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- RPC llamada a procedimiento remoto, tareas, registrar la interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a12de37b39c719de246ceb79a92d6a51fc361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268250"
---
# <a name="registering-the-interface"></a><span data-ttu-id="940e7-104">Registrar la interfaz</span><span class="sxs-lookup"><span data-stu-id="940e7-104">Registering the Interface</span></span>

<span data-ttu-id="940e7-105">El registro de la interfaz que admite un programa de servidor permite que las llamadas a procedimientos remotos de programas cliente se envíen a la rutina de servidor adecuada.</span><span class="sxs-lookup"><span data-stu-id="940e7-105">Registering the interface that a server program supports enables remote procedure calls from client programs to be dispatched to the proper server routine.</span></span> <span data-ttu-id="940e7-106">Los programas de servidor llaman a [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para registrar sus interfaces.</span><span class="sxs-lookup"><span data-stu-id="940e7-106">Server programs call [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to register their interfaces.</span></span> <span data-ttu-id="940e7-107">En el siguiente fragmento de código se muestra su uso:</span><span class="sxs-lookup"><span data-stu-id="940e7-107">The following code fragment demonstrates its use:</span></span>


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



<span data-ttu-id="940e7-108">El primer parámetro de la función [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) es una estructura que el compilador MIDL genera a partir del archivo IDL que define la interfaz (o interfaces) del servidor.</span><span class="sxs-lookup"><span data-stu-id="940e7-108">The first parameter to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is a structure the MIDL compiler generates from the IDL file that defines the interface (or interfaces) for the server.</span></span> <span data-ttu-id="940e7-109">El segundo y el tercer parámetro son un UUID y un vector de punto de entrada, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="940e7-109">The second and third parameters are a UUID and an entry-point vector, respectively.</span></span> <span data-ttu-id="940e7-110">Se establecen en **null** en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="940e7-110">They are set to **NULL** in this example.</span></span> <span data-ttu-id="940e7-111">En muchos casos, el programa de servidor establecerá estos valores de parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="940e7-111">In many instances, your server program will set these parameter values to **NULL**.</span></span> <span data-ttu-id="940e7-112">Los programas de servidor usan el segundo y el tercer parámetro cuando proporcionan varias implementaciones de los mismos procedimientos en una interfaz.</span><span class="sxs-lookup"><span data-stu-id="940e7-112">Server programs use the second and third parameters when they provide multiple implementations of the same procedures in an interface.</span></span> <span data-ttu-id="940e7-113">Para obtener más información, consulte [vectores de punto de entrada](registering-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="940e7-113">For more information, see [Entry-Point Vectors](registering-interfaces.md).</span></span>

<span data-ttu-id="940e7-114">Los programas de servidor también pueden usar [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) para registrar una interfaz.</span><span class="sxs-lookup"><span data-stu-id="940e7-114">Server programs can also use [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) to register an interface.</span></span> <span data-ttu-id="940e7-115">Una ventaja de usar esta función es que proporciona a la aplicación la capacidad de establecer una función de devolución de llamada de seguridad.</span><span class="sxs-lookup"><span data-stu-id="940e7-115">One advantage of using this function is that it provides your application with the ability to set a security-callback function.</span></span> <span data-ttu-id="940e7-116">El uso de funciones de devolución de llamada de seguridad es el método recomendado para proteger una interfaz.</span><span class="sxs-lookup"><span data-stu-id="940e7-116">Using security-callback functions is the recommended approach to securing an interface.</span></span>

> [!Note]  
> <span data-ttu-id="940e7-117">MIDL genera dos estructuras muy similares, una para el cliente y otra para el servidor.</span><span class="sxs-lookup"><span data-stu-id="940e7-117">MIDL produces two very similar structures, one for the client and one for the server.</span></span> <span data-ttu-id="940e7-118">La estructura que se pasa a la función [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) es la versión de servidor de la estructura generada por MIDL.</span><span class="sxs-lookup"><span data-stu-id="940e7-118">The structure passed to the [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) function is the server version of the MIDL-produced structure.</span></span>

 

 

 




