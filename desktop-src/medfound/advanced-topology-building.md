---
description: Creación de topologías avanzadas
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Creación de topologías avanzadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4cc061d4e557dda4ccbb81eabc55e8e1b3e33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360266"
---
# <a name="advanced-topology-building"></a><span data-ttu-id="97421-103">Creación de topologías avanzadas</span><span class="sxs-lookup"><span data-stu-id="97421-103">Advanced Topology Building</span></span>

<span data-ttu-id="97421-104">En esta sección se describen algunas técnicas avanzadas para crear topologías.</span><span class="sxs-lookup"><span data-stu-id="97421-104">This section describes some advanced techniques for building topologies.</span></span> <span data-ttu-id="97421-105">Puede usar estas técnicas si desea tener más control sobre las topologías que envía a la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="97421-105">You can use these techniques if you want more control over the topologies that you send to the Media Session.</span></span>

<span data-ttu-id="97421-106">Dado que estas técnicas están pensadas para escenarios que van más allá de la funcionalidad proporcionada por el cargador de topología estándar, muchos de los detalles dependerán de los requisitos específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="97421-106">Because these techniques are intended for scenarios that go beyond the functionality provided by the standard topology loader, many of the details will depend on the particular requirements of your application.</span></span> <span data-ttu-id="97421-107">Por lo tanto, esta sección está organizada de forma flexible en torno a subtareas más pequeñas, en lugar de escenarios completos.</span><span class="sxs-lookup"><span data-stu-id="97421-107">Therefore, this section is organized loosely around smaller subtasks, rather than complete, end-to-end scenarios.</span></span>

<span data-ttu-id="97421-108">La aplicación de reproducción típica sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="97421-108">The typical playback application follows these steps:</span></span>

1.  <span data-ttu-id="97421-109">La aplicación crea una topología parcial y la pone en cola en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="97421-109">The application builds a partial topology and queues it on the Media Session.</span></span>
2.  <span data-ttu-id="97421-110">La sesión multimedia invoca el cargador de topología para resolver la topología.</span><span class="sxs-lookup"><span data-stu-id="97421-110">The Media Session invokes the topology loader to resolve the topology.</span></span>

<span data-ttu-id="97421-111">Si desea ir más allá de las capacidades del cargador de topología, hay tres enfoques generales:</span><span class="sxs-lookup"><span data-stu-id="97421-111">If you want to go beyond the capabilities of the topology loader, there are three general approaches:</span></span>

-   <span data-ttu-id="97421-112">Cree una topología completa.</span><span class="sxs-lookup"><span data-stu-id="97421-112">Build a complete topology.</span></span> <span data-ttu-id="97421-113">Al poner en cola la topología en la sesión multimedia, llame a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) con la \_ marca Resolution de MFSESSION SetTopology \_ .</span><span class="sxs-lookup"><span data-stu-id="97421-113">When you queue the topology on the Media Session, call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the MFSESSION\_SETTOPOLOGY\_NORESOLUTION flag.</span></span> <span data-ttu-id="97421-114">Esta marca impide que la sesión multimedia intente resolver la topología.</span><span class="sxs-lookup"><span data-stu-id="97421-114">This flag prevents the Media Session from attempting to resolve the topology.</span></span>

-   <span data-ttu-id="97421-115">Invoque directamente el cargador de topología para resolver la topología.</span><span class="sxs-lookup"><span data-stu-id="97421-115">Directly invoke the topology loader to resolve the topology.</span></span> <span data-ttu-id="97421-116">Después, puede modificar la topología completa antes de ponerla en cola en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="97421-116">You can then modify the full topology before queuing it on the Media Session.</span></span>

-   <span data-ttu-id="97421-117">Implemente un cargador de topología personalizado.</span><span class="sxs-lookup"><span data-stu-id="97421-117">Implement a custom topology loader.</span></span> <span data-ttu-id="97421-118">Con este enfoque, se pone en cola una topología parcial, pero la sesión multimedia invoca el cargador personalizado en lugar de la implementación de Media Foundation estándar.</span><span class="sxs-lookup"><span data-stu-id="97421-118">With this approach, you queue a partial topology, but the Media Session invokes your custom loader instead of the standard Media Foundation implementation.</span></span> <span data-ttu-id="97421-119">Una ventaja de este enfoque es que puede realizar la compilación de topología personalizada dentro del entorno protegido.</span><span class="sxs-lookup"><span data-stu-id="97421-119">One advantage of this approach is that you can perform custom topology building inside the protected environment.</span></span> <span data-ttu-id="97421-120">En ese caso, sin embargo, el cargador de topología debe ser un componente de confianza.</span><span class="sxs-lookup"><span data-stu-id="97421-120">(In that case, however, the topology loader must be a trusted component.</span></span> <span data-ttu-id="97421-121">Para obtener más información, vea [ruta de acceso a medios protegidos](protected-media-path.md)).</span><span class="sxs-lookup"><span data-stu-id="97421-121">For more information, see [Protected Media Path](protected-media-path.md).)</span></span>

<span data-ttu-id="97421-122">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="97421-122">This section contains the following topics.</span></span>



| <span data-ttu-id="97421-123">Tema</span><span class="sxs-lookup"><span data-stu-id="97421-123">Topic</span></span>                                                                          | <span data-ttu-id="97421-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="97421-124">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97421-125">Cargadores de topología personalizados</span><span class="sxs-lookup"><span data-stu-id="97421-125">Custom Topology Loaders</span></span>](custom-topology-loaders.md)                         | <span data-ttu-id="97421-126">Cómo proporcionar una implementación personalizada de [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) para la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="97421-126">How to provide a custom implementation of [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) for the Media Session.</span></span>          |
| [<span data-ttu-id="97421-127">Enlazar nodos de salida a receptores de medios</span><span class="sxs-lookup"><span data-stu-id="97421-127">Binding Output Nodes to Media Sinks</span></span>](binding-output-nodes-to-media-sinks.md) | <span data-ttu-id="97421-128">Cómo preparar los nodos de salida en una topología si usa el cargador de topología fuera de la sesión de medios.</span><span class="sxs-lookup"><span data-stu-id="97421-128">How to prepare the output nodes in a topology if you are using the topology loader outside of the Media Session.</span></span> |
| [<span data-ttu-id="97421-129">Agregar un descodificador a una topología</span><span class="sxs-lookup"><span data-stu-id="97421-129">Adding a Decoder to a Topology</span></span>](adding-a-decoder-to-a-topology.md)           | <span data-ttu-id="97421-130">Cómo seleccionar un descodificador manualmente y agregarlo a una topología.</span><span class="sxs-lookup"><span data-stu-id="97421-130">How to select a decoder manually and add it to a topology.</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="97421-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97421-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97421-132">Topologías</span><span class="sxs-lookup"><span data-stu-id="97421-132">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



