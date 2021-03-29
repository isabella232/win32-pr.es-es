---
title: Entrar en el estado de ejecución
description: Entrar en el estado de ejecución
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959038c8f64fe8750ab1bcf0f06b753371f04136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994167"
---
# <a name="entering-the-running-state"></a><span data-ttu-id="acd7a-103">Entrar en el estado de ejecución</span><span class="sxs-lookup"><span data-stu-id="acd7a-103">Entering the Running State</span></span>

<span data-ttu-id="acd7a-104">Cuando un objeto incrustado realiza la transición al estado en ejecución, el controlador de objetos debe localizar y ejecutar la aplicación de servidor para poder utilizar los servicios que solo proporciona el servidor.</span><span class="sxs-lookup"><span data-stu-id="acd7a-104">When an embedded object makes the transition to the running state, the object handler must locate and run the server application in order to utilize the services that only the server provides.</span></span> <span data-ttu-id="acd7a-105">Los objetos incrustados se colocan en el estado de ejecución explícitamente a través de una solicitud del contenedor, como una necesidad de dibujar un formato no almacenado en caché actualmente o implícitamente por OLE en respuesta a la invocación de una operación, como cuando un usuario del contenedor hace doble clic en el objeto.</span><span class="sxs-lookup"><span data-stu-id="acd7a-105">Embedded objects are placed in the running state either explicitly through a request by the container, such as a need to draw a format not currently cached, or implicitly by OLE in response to invoking some operation, such as when a user of the container double-clicks the object.</span></span>

<span data-ttu-id="acd7a-106">Cuando un objeto vinculado realiza la transición al estado en ejecución, el proceso se conoce como *enlace*.</span><span class="sxs-lookup"><span data-stu-id="acd7a-106">When a linked object makes the transition into the running state, the process is known as *binding*.</span></span> <span data-ttu-id="acd7a-107">En el proceso de enlace, el controlador de objetos pide a su moniker almacenado que busque los datos del vínculo y, a continuación, ejecuta la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="acd7a-107">In the process of binding, the object handler asks its stored moniker to locate the link's data, then runs the server application.</span></span>

<span data-ttu-id="acd7a-108">A primera vista, el enlace de un objeto vinculado parece no ser más complicado que ejecutar un objeto incrustado.</span><span class="sxs-lookup"><span data-stu-id="acd7a-108">At first glance, binding a linked object appears to be no more complicated than running an embedded object.</span></span> <span data-ttu-id="acd7a-109">Sin embargo, los siguientes puntos complican el proceso:</span><span class="sxs-lookup"><span data-stu-id="acd7a-109">However, the following points complicate the process:</span></span>

-   <span data-ttu-id="acd7a-110">Un vínculo puede hacer referencia a un objeto, o una parte de ella, que está incrustado en otro contenedor.</span><span class="sxs-lookup"><span data-stu-id="acd7a-110">A link can refer to an object, or a portion thereof, that is embedded in another container.</span></span> <span data-ttu-id="acd7a-111">Esta capacidad implica una posibilidad de incrustaciones anidadas.</span><span class="sxs-lookup"><span data-stu-id="acd7a-111">This capability implies a potential for nested embeddings.</span></span> <span data-ttu-id="acd7a-112">La resolución de referencias a una jerarquía de este tipo requiere atravesar de forma recursiva un *moniker compuesto*, empezando por el miembro situado más a la derecha.</span><span class="sxs-lookup"><span data-stu-id="acd7a-112">Resolving references to such a hierarchy requires recursively traversing a *composite moniker*, beginning with the rightmost member.</span></span>
-   <span data-ttu-id="acd7a-113">Cuando el origen del vínculo se está ejecutando, OLE se enlaza a la instancia en ejecución del objeto en lugar de ejecutar otra instancia.</span><span class="sxs-lookup"><span data-stu-id="acd7a-113">When the link source is running, OLE binds to the running instance of the object rather than running another instance.</span></span> <span data-ttu-id="acd7a-114">En el caso de los objetos incrustados anidados, uno de los cuales es el origen del vínculo, OLE debe ser capaz de enlazar a un objeto que ya se está ejecutando en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="acd7a-114">In the case of nested embedded objects, one of which is the link source, OLE must be able to bind to an already running object at any point.</span></span>
-   <span data-ttu-id="acd7a-115">La ejecución de un objeto requiere tener acceso al área de almacenamiento del objeto.</span><span class="sxs-lookup"><span data-stu-id="acd7a-115">Running an object requires accessing the storage area for the object.</span></span> <span data-ttu-id="acd7a-116">Cuando se ejecuta un objeto incrustado, OLE recibe un puntero al almacenamiento durante el proceso de carga, que pasa a la aplicación de servidor OLE.</span><span class="sxs-lookup"><span data-stu-id="acd7a-116">When an embedded object is run, OLE receives a pointer to the storage during the load process, which it passes on to the OLE server application.</span></span> <span data-ttu-id="acd7a-117">En el caso de los objetos vinculados, sin embargo, no hay ninguna interfaz estándar para tener acceso al almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="acd7a-117">For linked objects, however, there is no standard interface for accessing storage.</span></span> <span data-ttu-id="acd7a-118">La aplicación de servidor OLE puede utilizar la interfaz del sistema de archivos o algún otro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="acd7a-118">The OLE server application may use the file system interface or some other mechanism.</span></span>

 

 




