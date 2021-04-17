---
title: Inconvenientes
description: Inconvenientes
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a22e409414a1df60e2dd9dff3adbfc6000b953a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532391"
---
# <a name="disadvantages"></a><span data-ttu-id="0371e-103">Inconvenientes</span><span class="sxs-lookup"><span data-stu-id="0371e-103">Disadvantages</span></span>

<span data-ttu-id="0371e-104">Los servidores en proceso proporcionan la velocidad y el tamaño de un controlador de objetos con la funcionalidad de edición de un servidor local.</span><span class="sxs-lookup"><span data-stu-id="0371e-104">In-process servers provide the speed and size advantage of an object handler with the editing capability of a local server.</span></span> <span data-ttu-id="0371e-105">¿Por qué alguna vez elegiría implementar la aplicación OLE como un servidor local en lugar de un servidor en proceso?</span><span class="sxs-lookup"><span data-stu-id="0371e-105">So why would you ever choose to implement your OLE application as a local server rather than an in-process server?</span></span> <span data-ttu-id="0371e-106">Hay varias razones:</span><span class="sxs-lookup"><span data-stu-id="0371e-106">There are several reasons:</span></span>

-   <span data-ttu-id="0371e-107">Seguridad.</span><span class="sxs-lookup"><span data-stu-id="0371e-107">Security.</span></span> <span data-ttu-id="0371e-108">Solo un servidor local tiene el espacio de direcciones aislado del cliente.</span><span class="sxs-lookup"><span data-stu-id="0371e-108">Only a local server has its address space isolated from that of the client.</span></span> <span data-ttu-id="0371e-109">Un servidor de tipo en curso comparte el espacio de direcciones y el contexto del proceso del cliente y, por tanto, puede ser menos sólido en caso de que se produzcan errores o la programación malintencionada.</span><span class="sxs-lookup"><span data-stu-id="0371e-109">An in-process server shares the address space and process context of the client and can therefore be less robust in the face of faults or malicious programming.</span></span>
-   <span data-ttu-id="0371e-110">Granularidad.</span><span class="sxs-lookup"><span data-stu-id="0371e-110">Granularity.</span></span> <span data-ttu-id="0371e-111">Un servidor local puede hospedar varias instancias de su objeto en muchos clientes diferentes, compartiendo el estado del servidor entre objetos en varios clientes de maneras que serían difíciles o imposibles si se implementan como un servidor en proceso, que es simplemente un archivo DLL cargado en cada cliente.</span><span class="sxs-lookup"><span data-stu-id="0371e-111">A local server can host multiple instances of its object across many different clients, sharing server state between objects in multiple clients in ways that would be difficult or impossible if implemented as an in-process server, which is simply a DLL loaded into each client.</span></span>
-   <span data-ttu-id="0371e-112">Compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="0371e-112">Compatibility.</span></span> <span data-ttu-id="0371e-113">Si decide implementar un servidor en proceso, se renuncia a la compatibilidad con OLE 1, que no es compatible con estos servidores.</span><span class="sxs-lookup"><span data-stu-id="0371e-113">If you choose to implement an in-process server, you relinquish compatibility with OLE 1, which does not support such servers.</span></span> <span data-ttu-id="0371e-114">Esto no será una consideración para muchos desarrolladores, pero si es así, es de importancia crítica.</span><span class="sxs-lookup"><span data-stu-id="0371e-114">This will not be a consideration for many developers, but if it is, then it is of critical concern.</span></span>
-   <span data-ttu-id="0371e-115">Imposibilidad de admitir vínculos.</span><span class="sxs-lookup"><span data-stu-id="0371e-115">Inability to support links.</span></span> <span data-ttu-id="0371e-116">Un servidor en proceso no puede servir como origen de vínculo.</span><span class="sxs-lookup"><span data-stu-id="0371e-116">An in-process server cannot serve as a link source.</span></span> <span data-ttu-id="0371e-117">Dado que un archivo DLL no se puede ejecutar por sí mismo, no puede crear un objeto de archivo al que se vinculará.</span><span class="sxs-lookup"><span data-stu-id="0371e-117">Since a DLL cannot run by itself, it cannot create a file object to be linked to.</span></span>

<span data-ttu-id="0371e-118">A pesar de estas desventajas, un servidor en proceso puede ser una opción excelente para su velocidad y tamaño, si se ajusta a todos los demás requisitos.</span><span class="sxs-lookup"><span data-stu-id="0371e-118">Despite these disadvantages, an in-process server can be an excellent choice for its speed and size — if it fits all your other requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0371e-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0371e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0371e-120">Ventajas</span><span class="sxs-lookup"><span data-stu-id="0371e-120">Advantages</span></span>](advantages.md)
</dt> <dt>

[<span data-ttu-id="0371e-121">Servidores en proceso</span><span class="sxs-lookup"><span data-stu-id="0371e-121">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




