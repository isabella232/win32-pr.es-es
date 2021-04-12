---
description: Crear topologías
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Crear topologías
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ec738c82ea2b85bcae7d4c05627b81ad939db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423563"
---
# <a name="creating-topologies"></a><span data-ttu-id="ba8e7-103">Crear topologías</span><span class="sxs-lookup"><span data-stu-id="ba8e7-103">Creating Topologies</span></span>

<span data-ttu-id="ba8e7-104">En esta sección se describen algunos de los procedimientos generales para crear una topología.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-104">This section describes some of the general procedures for creating a topology.</span></span>

<span data-ttu-id="ba8e7-105">Los pasos generales para crear una topología son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ba8e7-105">The general steps for creating a topology are as follows:</span></span>

1.  <span data-ttu-id="ba8e7-106">Cree un nuevo objeto Topology llamando a [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span><span class="sxs-lookup"><span data-stu-id="ba8e7-106">Create a new topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span> <span data-ttu-id="ba8e7-107">Esta función devuelve un puntero a la interfaz [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topología.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-107">This function returns a pointer to the topology's [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

2.  <span data-ttu-id="ba8e7-108">Inicialmente, la topología no contiene ningún nodo.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-108">Initially, the topology does not contain any nodes.</span></span> <span data-ttu-id="ba8e7-109">Para crear nodos para la topología, llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode).</span><span class="sxs-lookup"><span data-stu-id="ba8e7-109">To create nodes for the topology, call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode).</span></span> <span data-ttu-id="ba8e7-110">Esta función devuelve un puntero a la interfaz [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) del nodo.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-110">This function returns a pointer to the node's [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface.</span></span> <span data-ttu-id="ba8e7-111">Debe especificar el tipo de nodo al crear el nodo:</span><span class="sxs-lookup"><span data-stu-id="ba8e7-111">You must specify the node type when you create the node:</span></span>

    -   <span data-ttu-id="ba8e7-112">Nodo de origen.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-112">Source node.</span></span>

    -   <span data-ttu-id="ba8e7-113">Nodo de transformación.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-113">Transform node.</span></span>

    -   <span data-ttu-id="ba8e7-114">Nodo de salida.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-114">Output node.</span></span>

    -   <span data-ttu-id="ba8e7-115">Nodo tee.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-115">Tee node.</span></span>

3.  <span data-ttu-id="ba8e7-116">Inicialice cada nodo.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-116">Initialize each node.</span></span> <span data-ttu-id="ba8e7-117">El proceso de inicialización depende del tipo de nodo, tal y como se describe en los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-117">The initialization process depends on the node type, as described in the topics that follow.</span></span>

4.  <span data-ttu-id="ba8e7-118">Agregue cada nodo a la topología mediante una llamada a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).</span><span class="sxs-lookup"><span data-stu-id="ba8e7-118">Add each node to the topology by calling [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).</span></span>

5.  <span data-ttu-id="ba8e7-119">Conecte los nodos.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-119">Connect the nodes.</span></span> <span data-ttu-id="ba8e7-120">Para conectar un nodo, llame a [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) en el nodo de nivel superior y pase un puntero al nodo de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-120">To connect a node, call [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the upstream node, and pass in a pointer to the downstream node.</span></span>

<span data-ttu-id="ba8e7-121">En los temas siguientes se proporcionan los pasos específicos para cada tipo de nodo.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-121">The following topics give the specific steps for each node type.</span></span>



| <span data-ttu-id="ba8e7-122">Tema</span><span class="sxs-lookup"><span data-stu-id="ba8e7-122">Topic</span></span>                                                    | <span data-ttu-id="ba8e7-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba8e7-123">Description</span></span>                     |
|----------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="ba8e7-124">Crear nodos de origen</span><span class="sxs-lookup"><span data-stu-id="ba8e7-124">Creating Source Nodes</span></span>](creating-source-nodes.md)       | <span data-ttu-id="ba8e7-125">Cómo crear un nodo de origen.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-125">How to create a source node.</span></span>    |
| [<span data-ttu-id="ba8e7-126">Crear nodos de transformación</span><span class="sxs-lookup"><span data-stu-id="ba8e7-126">Creating Transform Nodes</span></span>](creating-transform-nodes.md) | <span data-ttu-id="ba8e7-127">Cómo crear un nodo de transformación.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-127">How to create a transform node.</span></span> |
| [<span data-ttu-id="ba8e7-128">Crear nodos de salida</span><span class="sxs-lookup"><span data-stu-id="ba8e7-128">Creating Output Nodes</span></span>](creating-output-nodes.md)       | <span data-ttu-id="ba8e7-129">Cómo crear un nodo de salida.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-129">How to create an output node.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="ba8e7-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba8e7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba8e7-131">Topologías</span><span class="sxs-lookup"><span data-stu-id="ba8e7-131">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



