---
description: Conexión y desconexión de nodos de topología
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: Conexión y desconexión de nodos de topología
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08057eba74314ae6b87da418b743a089506a3b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705419"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a><span data-ttu-id="e445b-103">Conexión y desconexión de nodos de topología</span><span class="sxs-lookup"><span data-stu-id="e445b-103">Connecting and Disconnecting Topology Nodes</span></span>

<span data-ttu-id="e445b-104">Para que una topología sea funcional, el nodo de origen y el nodo de salida deben estar conectados.</span><span class="sxs-lookup"><span data-stu-id="e445b-104">For a topology to be functional, the source node and the output node must be connected.</span></span> <span data-ttu-id="e445b-105">Para conectar dos nodos de topología, arrastre la salida de nodo de un nodo a la entrada de nodo del otro nodo.</span><span class="sxs-lookup"><span data-stu-id="e445b-105">To connect two topology nodes, drag the node output of one node to the node input of the other node.</span></span> <span data-ttu-id="e445b-106">TopoEdit muestra la conexión de nodo como una línea negra.</span><span class="sxs-lookup"><span data-stu-id="e445b-106">TopoEdit displays the node connection as a black line.</span></span> <span data-ttu-id="e445b-107">Esto es equivalente a la conexión de nodos de topología mediante una llamada al método [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) .</span><span class="sxs-lookup"><span data-stu-id="e445b-107">This is equivalent to connecting topology nodes by calling the [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) method.</span></span>

<span data-ttu-id="e445b-108">La topología solo se puede resolver si la conexión de nodo es válida; es decir, si los tipos de medios de los dos nodos son compatibles.</span><span class="sxs-lookup"><span data-stu-id="e445b-108">The topology can be resolved only if the node connection is valid; that is, if the media types of the two nodes are compatible.</span></span> <span data-ttu-id="e445b-109">Para obtener información sobre la resolución de topologías, consulte [resolución de una topología con TopoEdit](resolving-a-topology-with-topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="e445b-109">For information about resolving topologies, see [Resolving a Topology with TopoEdit](resolving-a-topology-with-topoedit.md).</span></span>

<span data-ttu-id="e445b-110">Si intenta establecer una conexión desde un nodo que ya está conectado, la nueva conexión de nodo reemplaza a la antigua conexión de nodo.</span><span class="sxs-lookup"><span data-stu-id="e445b-110">If you attempt to make a connection from a node that is already connected, the new node connection replaces the old node connection.</span></span>

<span data-ttu-id="e445b-111">Para eliminar una conexión, seleccione la conexión de nodo y presione la tecla SUPRIMIr o seleccione **eliminar** en el menú de **topología** .</span><span class="sxs-lookup"><span data-stu-id="e445b-111">To delete a connection, select the node connection and press the DELETE key or select **Delete** from the **Topology** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e445b-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e445b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e445b-113">Compilar topologías mediante TopoEdit</span><span class="sxs-lookup"><span data-stu-id="e445b-113">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="e445b-114">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="e445b-114">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



