---
description: Resolver una topología con TopoEdit
ms.assetid: da3e2bbc-7c9f-4a15-8842-c1bb00662cd2
title: Resolver una topología con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8397e380b19a6f45736c06e859d2a80456aad079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275819"
---
# <a name="resolving-a-topology-with-topoedit"></a><span data-ttu-id="82bb0-103">Resolver una topología con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="82bb0-103">Resolving a Topology with TopoEdit</span></span>

<span data-ttu-id="82bb0-104">Hay dos tipos de topologías:</span><span class="sxs-lookup"><span data-stu-id="82bb0-104">There are two types of topologies:</span></span>

-   <span data-ttu-id="82bb0-105">Topología parcial.</span><span class="sxs-lookup"><span data-stu-id="82bb0-105">Partial Topology.</span></span> <span data-ttu-id="82bb0-106">El nodo de origen se conecta directamente al nodo de salida.</span><span class="sxs-lookup"><span data-stu-id="82bb0-106">The source node is connected directly to the output node.</span></span> <span data-ttu-id="82bb0-107">En algunos casos, una topología parcial puede tener algunos nodos de transformación intermedios, como efectos, pero no todos.</span><span class="sxs-lookup"><span data-stu-id="82bb0-107">In some cases, a partial topology can have some intermediate transform nodes, such as effects, but not all.</span></span> <span data-ttu-id="82bb0-108">Los nodos de transformación que se omiten suelen ser descodificadores o conversión de formato MFTs, como convertidores de colores y remuestreadores de audio.</span><span class="sxs-lookup"><span data-stu-id="82bb0-108">The transform nodes that are omitted are typically decoders or format conversion MFTs, such as color converters and audio resamplers.</span></span>

-   <span data-ttu-id="82bb0-109">Topología completa.</span><span class="sxs-lookup"><span data-stu-id="82bb0-109">Full Topology.</span></span> <span data-ttu-id="82bb0-110">El nodo de origen se conecta al nodo de salida a través de un nodo de transformación.</span><span class="sxs-lookup"><span data-stu-id="82bb0-110">The source node is connected to the output node through a transform node.</span></span> <span data-ttu-id="82bb0-111">Este tipo de topología debe tener todos los nodos para procesar los datos.</span><span class="sxs-lookup"><span data-stu-id="82bb0-111">This type of topology must have every node to process data.</span></span>

<span data-ttu-id="82bb0-112">TopoEdit solo puede reproducir topologías completas.</span><span class="sxs-lookup"><span data-stu-id="82bb0-112">TopoEdit can only play full topologies.</span></span> <span data-ttu-id="82bb0-113">TopoEdit usa el objeto cargador de topología, proporcionado por Media Foundation, para convertir una topología parcial en una topología completa mediante la inserción de las transformaciones necesarias.</span><span class="sxs-lookup"><span data-stu-id="82bb0-113">TopoEdit uses the topology loader object, provided by Media Foundation, to convert a partial topology into a full topology by inserting the required transforms.</span></span> <span data-ttu-id="82bb0-114">El proceso de creación de una topología completa se denomina resolver una topología.</span><span class="sxs-lookup"><span data-stu-id="82bb0-114">The process of creating a full topology is called resolving a topology.</span></span>

<span data-ttu-id="82bb0-115">Para obtener información sobre los tipos de topología, consulte la sección topologías parciales en acerca de las [topologías](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="82bb0-115">For information about topology types, see the Partial Topologies section in [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="82bb0-116">Antes de resolver una topología, asegúrese de que:</span><span class="sxs-lookup"><span data-stu-id="82bb0-116">Before you resolve a topology ensure that:</span></span>

-   <span data-ttu-id="82bb0-117">La topología contiene un nodo de origen y un nodo de salida.</span><span class="sxs-lookup"><span data-stu-id="82bb0-117">The topology contains a source node and an output node.</span></span>

-   <span data-ttu-id="82bb0-118">Los nodos de origen y de salida están conectados mediante una conexión de nodo válida.</span><span class="sxs-lookup"><span data-stu-id="82bb0-118">The source and the output nodes are connected by a valid node connection.</span></span> <span data-ttu-id="82bb0-119">Durante la resolución de la topología, el cargador de topología comprueba la compatibilidad del tipo de medio de los nodos.</span><span class="sxs-lookup"><span data-stu-id="82bb0-119">During topology resolution, the topology loader checks the media type of the nodes for compatibility.</span></span> <span data-ttu-id="82bb0-120">Si existe una conexión de nodo no válida, se produce un error en el proceso y se muestra un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="82bb0-120">If an invalid node connection exists, then the process fails and an error message is displayed.</span></span>

<span data-ttu-id="82bb0-121">Para resolver una topología, en el menú **topología** , haga clic en **resolver topología**.</span><span class="sxs-lookup"><span data-stu-id="82bb0-121">To resolve a topology, from the **Topology** menu, click **Resolve Topology**.</span></span>

<span data-ttu-id="82bb0-122">La barra de herramientas indica el estado de la topología: **\[ resuelto \]** o **\[ no resuelto \]**.</span><span class="sxs-lookup"><span data-stu-id="82bb0-122">The toolbar indicates the topology status: **\[Resolved\]** or **\[Not Resolved\]**.</span></span>

<span data-ttu-id="82bb0-123">Si TopoEdit resuelve una topología correctamente, el estado de la **topología** se establece en **\[ resolved \]** y se habilitan los controles de reproducción.</span><span class="sxs-lookup"><span data-stu-id="82bb0-123">If TopoEdit resolves a topology successfully, **Topology Status** is set to **\[Resolved\]** and the playback controls are enabled.</span></span>

<span data-ttu-id="82bb0-124">Cada vez que realiza cambios en la topología, el **Estado** de la topología se establece en **\[ no \] resuelto** , lo que indica que se debe volver a resolver.</span><span class="sxs-lookup"><span data-stu-id="82bb0-124">Each time you make changes to the topology, **Topology Status** is set to **\[Not Resolved\]** which indicates that it must be resolved again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82bb0-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82bb0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82bb0-126">Compilar topologías mediante TopoEdit</span><span class="sxs-lookup"><span data-stu-id="82bb0-126">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="82bb0-127">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="82bb0-127">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



