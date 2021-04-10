---
title: Servidores de In-Process
description: Servidores de In-Process
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4886932b9669aa2d3cdd49979324f9ccc6e03d44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268735"
---
# <a name="in-process-servers"></a><span data-ttu-id="87f94-103">Servidores de In-Process</span><span class="sxs-lookup"><span data-stu-id="87f94-103">In-Process Servers</span></span>

<span data-ttu-id="87f94-104">Si implementa una aplicación de servidor OLE como un servidor en proceso, una DLL que se ejecuta en el espacio de proceso de la aplicación contenedora, en lugar de un servidor local, un archivo EXE que se ejecuta en su propio espacio de proceso, la comunicación entre el contenedor y el servidor se simplifica porque la comunicación entre los dos puede adoptar la forma de llamadas de función normales.</span><span class="sxs-lookup"><span data-stu-id="87f94-104">If you implement an OLE server application as an in-process server — a DLL running in the process space of the container application — rather than as a local server — an EXE running in its own process space — communication between container and server is simplified because communication between the two can take the form of normal function calls.</span></span> <span data-ttu-id="87f94-105">No es necesario realizar llamadas a procedimientos remotos porque las dos aplicaciones se ejecutan en el mismo espacio de proceso.</span><span class="sxs-lookup"><span data-stu-id="87f94-105">Remote procedure calls are not required because the two applications run in the same process space.</span></span> <span data-ttu-id="87f94-106">Como cabría esperar, los objetos que administran el cálculo de referencias de parámetros también son innecesarios, aunque se pueden agregar en el archivo DLL sin interferir con la comunicación entre el contenedor y el servidor.</span><span class="sxs-lookup"><span data-stu-id="87f94-106">As you would expect, the objects that manage the marshaling of parameters are also unnecessary, although they may be aggregated within the DLL without interfering with the communication between container and server.</span></span>

<span data-ttu-id="87f94-107">Cuando una aplicación de servidor OLE se implementa como un servidor en proceso, no es necesario un controlador de objetos independiente porque el propio servidor reside en el espacio de proceso del cliente.</span><span class="sxs-lookup"><span data-stu-id="87f94-107">When an OLE server application is implemented as an in-process server, a separate object handler is not required because the server itself lives in the client's process space.</span></span> <span data-ttu-id="87f94-108">La diferencia principal entre un servidor en proceso y un controlador de objetos es que el servidor puede administrar el objeto en estado de ejecución mientras el controlador no puede.</span><span class="sxs-lookup"><span data-stu-id="87f94-108">The main difference between an in-process server and object handler is that the server is able to manage the object in a running state while the handler cannot.</span></span> <span data-ttu-id="87f94-109">Una consecuencia de esta diferencia es que un servidor debe proporcionar una interfaz de usuario para manipular el objeto en ejecución, mientras que un controlador delega este requisito en el servidor del objeto.</span><span class="sxs-lookup"><span data-stu-id="87f94-109">One consequence of this difference is that a server must provide a user interface for manipulating the running object, while a handler delegates this requirement to the object's server.</span></span> <span data-ttu-id="87f94-110">En la creación de un servidor de tipo en curso, se puede Agregar en el controlador predeterminado de OLE, lo que permite administrar las tareas básicas, como la visualización, el almacenamiento y las notificaciones, mientras que solo se implementan los servicios que el controlador no proporciona o no implementa de la forma que necesite.</span><span class="sxs-lookup"><span data-stu-id="87f94-110">In creating an in-process server, you can aggregate on the OLE default handler, letting it handle basic chores, such as display, storage, and notifications while you implement only those services that the handler either does not provide or does not implement in the way you require.</span></span>

<span data-ttu-id="87f94-111">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="87f94-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="87f94-112">Ventajas</span><span class="sxs-lookup"><span data-stu-id="87f94-112">Advantages</span></span>](advantages.md)
-   [<span data-ttu-id="87f94-113">Desventajas</span><span class="sxs-lookup"><span data-stu-id="87f94-113">Disadvantages</span></span>](disadvantages.md)

## <a name="related-topics"></a><span data-ttu-id="87f94-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="87f94-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87f94-115">Documentos compuestos</span><span class="sxs-lookup"><span data-stu-id="87f94-115">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




