---
title: Crear un objeto a través de un objeto de clase
description: Crear un objeto a través de un objeto de clase
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38787e7bc32151446cda6ff0a4cfe3f23a0f6eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994579"
---
# <a name="creating-an-object-through-a-class-object"></a><span data-ttu-id="17d4d-103">Crear un objeto a través de un objeto de clase</span><span class="sxs-lookup"><span data-stu-id="17d4d-103">Creating an Object Through a Class Object</span></span>

<span data-ttu-id="17d4d-104">Con la creciente importancia de las redes de equipos, es necesario que los clientes y los servidores interactúen de forma sencilla y eficaz, independientemente de que residan en el mismo equipo o en una red.</span><span class="sxs-lookup"><span data-stu-id="17d4d-104">With the increasing importance of computer networks, it has become necessary for clients and servers to interact easily and efficiently, whether they reside on the same machine or across a network.</span></span> <span data-ttu-id="17d4d-105">Crucial para esto es la capacidad de un cliente de iniciar un servidor, crear una instancia del objeto del servidor y tener acceso a los métodos de las interfaces en el objeto.</span><span class="sxs-lookup"><span data-stu-id="17d4d-105">Crucial to this is a client's ability to launch a server, create an instance of the server's object, and have access to the methods of the interfaces on the object.</span></span>

<span data-ttu-id="17d4d-106">COM proporciona extensiones a este proceso COM básico que lo hacen prácticamente sin problemas a través de una red.</span><span class="sxs-lookup"><span data-stu-id="17d4d-106">COM provides extensions to this basic COM process that make it virtually seamless across a network.</span></span> <span data-ttu-id="17d4d-107">Si un cliente es capaz de identificar el servidor a través de su CLSID, llamar a algunas funciones simples permite a COM realizar todo el trabajo de buscar e iniciar el servidor y activar el objeto.</span><span class="sxs-lookup"><span data-stu-id="17d4d-107">If a client is able to identify the server through its CLSID, calling a few simple functions permit COM to do all the work of locating and launching the server and activating the object.</span></span> <span data-ttu-id="17d4d-108">Las subclaves del registro permiten a los servidores remotos registrar su ubicación, por lo que el cliente no requiere esa información.</span><span class="sxs-lookup"><span data-stu-id="17d4d-108">Subkeys in the registry allow remote servers to register their location, so the client does not require that information.</span></span> <span data-ttu-id="17d4d-109">En el caso de las aplicaciones que desean aprovechar las características de red, las funciones de creación de objetos COM permiten una mayor flexibilidad y eficacia.</span><span class="sxs-lookup"><span data-stu-id="17d4d-109">For applications that want to take advantage of networking features, the COM object creation functions allow more flexibility and efficiency.</span></span>

<span data-ttu-id="17d4d-110">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="17d4d-110">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="17d4d-111">Objetos de clase COM y CLSID</span><span class="sxs-lookup"><span data-stu-id="17d4d-111">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
-   [<span data-ttu-id="17d4d-112">Buscar un objeto remoto</span><span class="sxs-lookup"><span data-stu-id="17d4d-112">Locating a Remote Object</span></span>](locating-a-remote-object.md)
-   [<span data-ttu-id="17d4d-113">Funciones auxiliares de creación de instancia</span><span class="sxs-lookup"><span data-stu-id="17d4d-113">Instance Creation Helper Functions</span></span>](instance-creation-helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="17d4d-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17d4d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17d4d-115">Clientes y servidores COM</span><span class="sxs-lookup"><span data-stu-id="17d4d-115">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




