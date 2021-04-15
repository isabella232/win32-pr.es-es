---
title: Identificadores de enlace explícitos
description: Para obtener el máximo control sobre el proceso de enlace, las aplicaciones cliente/servidor pueden utilizar identificadores de enlace explícitos.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b391c339ac3747928e3394152e9c0de7c1c7aa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676181"
---
# <a name="explicit-binding-handles"></a><span data-ttu-id="43988-103">Identificadores de enlace explícitos</span><span class="sxs-lookup"><span data-stu-id="43988-103">Explicit Binding Handles</span></span>

<span data-ttu-id="43988-104">Para obtener el máximo control sobre el proceso de enlace, las aplicaciones cliente/servidor pueden utilizar identificadores de enlace explícitos.</span><span class="sxs-lookup"><span data-stu-id="43988-104">For maximum control over the binding process, client/server applications may use explicit binding handles.</span></span> <span data-ttu-id="43988-105">Al igual que los identificadores implícitos, los identificadores de enlace explícitos permiten que la aplicación cliente seleccione un servidor para ejecutar sus llamadas.</span><span class="sxs-lookup"><span data-stu-id="43988-105">Like implicit handles, explicit binding handles enable your client application to select a server to execute its calls.</span></span> <span data-ttu-id="43988-106">Además, los identificadores de enlace explícitos permiten que la aplicación cliente/servidor cree una sesión de comunicación RPC autenticada.</span><span class="sxs-lookup"><span data-stu-id="43988-106">In addition, explicit binding handles enable your client/server application to create an authenticated RPC communication session.</span></span> <span data-ttu-id="43988-107">Con los identificadores explícitos, el cliente puede conectarse a más de un servidor y ejecutar procedimientos remotos en varios servidores.</span><span class="sxs-lookup"><span data-stu-id="43988-107">With explicit handles, your client can connect to more than one server and execute remote procedures on multiple servers.</span></span> <span data-ttu-id="43988-108">Las aplicaciones cliente multiproceso y asincrónicas incluso pueden conectarse a varios servidores y ejecutar varios procedimientos remotos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="43988-108">Multithreaded and asynchronous client applications can even connect to multiple servers and execute multiple remote procedures at the same time.</span></span>

<span data-ttu-id="43988-109">La aplicación cliente debe pasar el identificador explícito como parámetro a cada llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="43988-109">Your client application must pass the explicit handle as a parameter to each remote procedure call.</span></span> <span data-ttu-id="43988-110">Para ajustarse al estándar de OSF, el identificador debe especificarse como el primer parámetro en cada procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="43988-110">To conform to the OSF standard, the handle should be specified as the first parameter on each remote procedure.</span></span> <span data-ttu-id="43988-111">Sin embargo, las extensiones de Microsoft para RPC le permiten especificar el controlador de enlace en otras posiciones.</span><span class="sxs-lookup"><span data-stu-id="43988-111">However, the Microsoft extensions to RPC enable you to specify the binding handle in other positions.</span></span> <span data-ttu-id="43988-112">Para obtener más información, vea [extensiones de Microsoft RPC Binding-Handle](microsoft-rpc-binding-handle-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="43988-112">For more information, see [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).</span></span>

<span data-ttu-id="43988-113">Para crear un identificador explícito, declare el identificador como un parámetro para las operaciones remotas en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="43988-113">To create an explicit handle, declare the handle as a parameter to the remote operations in the IDL file.</span></span> <span data-ttu-id="43988-114">El [ejemplo Hello, World](tutorial.md) se puede redefinir para usar un identificador explícito, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="43988-114">The [Hello, World example](tutorial.md) can be redefined to use an explicit handle as shown:</span></span>

``` syntax
/* IDL file for explicit handles */
 
[ 
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0) 
]
interface hello
{
  void HelloProc([in] handle_t h1,
                 [in, string] char *  pszString); 
}
```

<span data-ttu-id="43988-115">Puede combinar controladores explícitos e implícitos en una sola interfaz.</span><span class="sxs-lookup"><span data-stu-id="43988-115">You can combine explicit and implicit handles in a single interface.</span></span> <span data-ttu-id="43988-116">Si una función tiene un identificador explícito en su lista de parámetros, se usará dicho identificador.</span><span class="sxs-lookup"><span data-stu-id="43988-116">If a function has an explicit handle in its parameter list, that handle will be used.</span></span> <span data-ttu-id="43988-117">Si una función de una interfaz que usa identificadores implícitos no especifica un identificador explícito, se usará el identificador implícito predeterminado.</span><span class="sxs-lookup"><span data-stu-id="43988-117">If a function in an interface using implicit handles does not specify an explicit handle, then the default implicit handle will be used.</span></span>

 

 




