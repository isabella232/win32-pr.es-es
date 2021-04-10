---
description: Compilar topologías mediante TopoEdit
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Compilar topologías mediante TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92758911113c7500cb13fa814d07321435fafeb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153687"
---
# <a name="building-topologies-by-using-topoedit"></a><span data-ttu-id="2df0c-103">Compilar topologías mediante TopoEdit</span><span class="sxs-lookup"><span data-stu-id="2df0c-103">Building Topologies by Using TopoEdit</span></span>

<span data-ttu-id="2df0c-104">Una topología debe tener los tres nodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2df0c-104">A topology must have the following three nodes:</span></span>

-   <span data-ttu-id="2df0c-105">Nodo de origen: el flujo de un archivo multimedia, que se usa como origen de la topología.</span><span class="sxs-lookup"><span data-stu-id="2df0c-105">Source node: The streams from a media file, which are used as a source for the topology.</span></span>
-   <span data-ttu-id="2df0c-106">Nodo de transformación: transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="2df0c-106">Transform node: A Media Foundation transform (MFT).</span></span> <span data-ttu-id="2df0c-107">Normalmente, estos nodos son codificadores, descodificadores y efectos de la topología.</span><span class="sxs-lookup"><span data-stu-id="2df0c-107">These nodes are usually encoders, decoders, and effects for the topology.</span></span>
-   <span data-ttu-id="2df0c-108">Nodo de salida: receptor de la secuencia que pasa los datos multimedia, los fotogramas de vídeo o las secuencias de audio a la sesión multimedia para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="2df0c-108">Output node: The stream sink that passes the media data, video frames, or audio streams to the Media Session for playback.</span></span>

<span data-ttu-id="2df0c-109">Para obtener información acerca de la estructura de la topología, consulte [acerca de las topologías](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="2df0c-109">For information about topology structure, see [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="2df0c-110">Para compilar una topología, debe agregar los nodos, conectar los nodos y resolver la topología para que pueda reproducirse.</span><span class="sxs-lookup"><span data-stu-id="2df0c-110">To build a topology, you must add the nodes, connect the nodes, and resolve the topology so that it can be played.</span></span>

<span data-ttu-id="2df0c-111">Los nodos de topología se muestran como cuadros, donde el texto muestra el nombre del nodo.</span><span class="sxs-lookup"><span data-stu-id="2df0c-111">Topology nodes are displayed as boxes, with text showing the name of the node.</span></span> <span data-ttu-id="2df0c-112">Los cuadros verdes representan los nodos agregados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2df0c-112">Green boxes represent the nodes that are added by the user.</span></span> <span data-ttu-id="2df0c-113">Cuando se resuelve una topología, TopoEdit puede agregar nodos de transformación a la topología automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2df0c-113">When a topology is resolved, TopoEdit can add transform nodes to the topology automatically.</span></span> <span data-ttu-id="2df0c-114">Aparecen como cuadros azules en el **Panel de topología**.</span><span class="sxs-lookup"><span data-stu-id="2df0c-114">These appear as blue boxes on the **Topology Pane**.</span></span>

<span data-ttu-id="2df0c-115">Las entradas y salidas de la topología se representan en forma de cuadrados negros a lo largo del borde del nodo.</span><span class="sxs-lookup"><span data-stu-id="2df0c-115">Topology inputs and outputs are represented by as black squares along the edge of the node.</span></span> <span data-ttu-id="2df0c-116">La *entrada de nodo* se muestra en el lado izquierdo del nodo y la *salida del nodo* está en el lado derecho del nodo.</span><span class="sxs-lookup"><span data-stu-id="2df0c-116">The *node input* is shown on the left side of the node, and the *node output* is on the right side of the node.</span></span>

<span data-ttu-id="2df0c-117">Los nodos de topología se conectan a través de una *conexión de nodo* que aparece como una línea negra que conecta la entrada de nodo de un nodo con la salida de nodo de otro nodo.</span><span class="sxs-lookup"><span data-stu-id="2df0c-117">The topology nodes are connected through a *node connection* that appears as a black line connecting the node input of one node to the node output of another node.</span></span>

<span data-ttu-id="2df0c-118">En la ilustración siguiente se muestra una topología conectada para un origen de audio.</span><span class="sxs-lookup"><span data-stu-id="2df0c-118">The following illustration shows a connected topology for an audio source.</span></span>

![Ilustración que muestra las conexiones del nodo de origen a dos nodos de transformación y, a continuación, al nodo de salida](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

<span data-ttu-id="2df0c-120">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="2df0c-120">This section contains the following topics:</span></span>



| <span data-ttu-id="2df0c-121">Tema</span><span class="sxs-lookup"><span data-stu-id="2df0c-121">Topic</span></span>                                                                                          | <span data-ttu-id="2df0c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2df0c-122">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="2df0c-123">Agregar nodos de origen con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="2df0c-123">Adding Source Nodes with TopoEdit</span></span>](adding-source-nodes-with-topoedit.md)                     | <span data-ttu-id="2df0c-124">Describe el proceso de agregar nodos de origen a una topología.</span><span class="sxs-lookup"><span data-stu-id="2df0c-124">Describes the process of adding source nodes to a topology.</span></span>    |
| [<span data-ttu-id="2df0c-125">Agregar nodos de transformación con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="2df0c-125">Adding Transform Nodes with TopoEdit</span></span>](adding-transform-nodes-with-topoedit.md)               | <span data-ttu-id="2df0c-126">Describe el proceso de agregar nodos de transformación a una topología.</span><span class="sxs-lookup"><span data-stu-id="2df0c-126">Describes the process of adding transform nodes to a topology.</span></span> |
| [<span data-ttu-id="2df0c-127">Agregar nodos de salida con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="2df0c-127">Adding Output Nodes with TopoEdit</span></span>](adding-output-nodes-with-topoedit.md)                     | <span data-ttu-id="2df0c-128">Describe el proceso de agregar nodos de salida a una topología.</span><span class="sxs-lookup"><span data-stu-id="2df0c-128">Describes the process of adding output nodes to a topology.</span></span>    |
| [<span data-ttu-id="2df0c-129">Conexión y desconexión de nodos de topología</span><span class="sxs-lookup"><span data-stu-id="2df0c-129">Connecting and Disconnecting Topology Nodes</span></span>](connecting-and-disconnecting-topology-nodes.md) | <span data-ttu-id="2df0c-130">Describe el proceso de conexión de dos nodos.</span><span class="sxs-lookup"><span data-stu-id="2df0c-130">Describes the process of connecting two nodes.</span></span>                 |
| [<span data-ttu-id="2df0c-131">Resolver una topología con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="2df0c-131">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)                   | <span data-ttu-id="2df0c-132">Describe el proceso de resolución de la topología.</span><span class="sxs-lookup"><span data-stu-id="2df0c-132">Describes the process of topology resolution.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="2df0c-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2df0c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2df0c-134">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="2df0c-134">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



