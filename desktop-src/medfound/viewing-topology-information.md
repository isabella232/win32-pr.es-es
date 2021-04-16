---
description: Ver información de la topología
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: Ver información de la topología
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c4e6808fb2414de14817c63f9f4736acc9223f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696861"
---
# <a name="viewing-topology-information"></a><span data-ttu-id="107b6-103">Ver información de la topología</span><span class="sxs-lookup"><span data-stu-id="107b6-103">Viewing Topology Information</span></span>

<span data-ttu-id="107b6-104">En TopoEdit, cada elemento de topología, como nodos, entradas de nodo y salidas de nodo, tiene un almacén de atributos asociado que administra el comportamiento del nodo.</span><span class="sxs-lookup"><span data-stu-id="107b6-104">In TopoEdit, each topology item, such as nodes, node inputs, and node outputs, has an associated attribute store that manages the behavior of the node.</span></span> <span data-ttu-id="107b6-105">Para ver los atributos, seleccione el elemento y el **Panel atributos** muestra la información.</span><span class="sxs-lookup"><span data-stu-id="107b6-105">To see the attributes, select the item, and the **Attributes Pane** displays the information.</span></span> <span data-ttu-id="107b6-106">En el caso de las topologías que se cargan desde un archivo XML, es posible que algunos de los nodos no muestren el almacén de atributos completo.</span><span class="sxs-lookup"><span data-stu-id="107b6-106">For topologies that are loaded from an XML file, some of the nodes may not display the entire attribute store.</span></span> <span data-ttu-id="107b6-107">Para ver el almacén de atributos completo, resuelva la topología.</span><span class="sxs-lookup"><span data-stu-id="107b6-107">To see the entire attribute store, resolve the topology.</span></span> <span data-ttu-id="107b6-108">Para obtener más información, vea [resolver una topología con TopoEdit](resolving-a-topology-with-topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="107b6-108">For more information, see [Resolving a Topology with TopoEdit](resolving-a-topology-with-topoedit.md).</span></span>

<span data-ttu-id="107b6-109">En la tabla siguiente se muestra el elemento de topología y los atributos que muestra el panel.</span><span class="sxs-lookup"><span data-stu-id="107b6-109">The following table shows the topology item and the attributes that the pane displays.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="107b6-110">Elemento de topología</span><span class="sxs-lookup"><span data-stu-id="107b6-110">Topology item</span></span></th>
<th><span data-ttu-id="107b6-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="107b6-111">Attributes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="107b6-112">Nodos de topología</span><span class="sxs-lookup"><span data-stu-id="107b6-112">Topology nodes</span></span></td>
<td><ul>
<li><span data-ttu-id="107b6-113"><a href="topology-node-attributes.md">Atributos de nodo de topología</a> para todos los nodos.</span><span class="sxs-lookup"><span data-stu-id="107b6-113"><a href="topology-node-attributes.md">Topology Node Attributes</a> for all nodes.</span></span><br/></li>
<li><span data-ttu-id="107b6-114"><a href="presentation-descriptor-attributes.md">Atributos de descriptor de presentación</a> solo para nodos de origen.</span><span class="sxs-lookup"><span data-stu-id="107b6-114"><a href="presentation-descriptor-attributes.md">Presentation Descriptor Attributes</a> for source nodes only.</span></span><br/></li>
<li><span data-ttu-id="107b6-115">Información de autoridad de confianza de entrada y salida para los nodos de transformación y de salida.</span><span class="sxs-lookup"><span data-stu-id="107b6-115">Input and output trust authority information for transform and output nodes.</span></span><br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="107b6-116">Entrada de nodo</span><span class="sxs-lookup"><span data-stu-id="107b6-116">Node input</span></span></td>
<td><ul>
<li><span data-ttu-id="107b6-117"><a href="media-type-attributes.md">Atributos de tipo de medio</a> para todos los nodos.</span><span class="sxs-lookup"><span data-stu-id="107b6-117"><a href="media-type-attributes.md">Media Type Attributes</a> for all nodes.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="107b6-118">Salida de nodo</span><span class="sxs-lookup"><span data-stu-id="107b6-118">Node output</span></span></td>
<td><ul>
<li><span data-ttu-id="107b6-119"><a href="stream-descriptor-attributes.md">Atributos de descriptor de flujo</a> solo para nodos de origen.</span><span class="sxs-lookup"><span data-stu-id="107b6-119"><a href="stream-descriptor-attributes.md">Stream Descriptor Attributes</a> for source nodes only.</span></span><br/></li>
<li><span data-ttu-id="107b6-120"><a href="media-type-attributes.md">Atributos de tipo de medio</a> para todos los nodos.</span><span class="sxs-lookup"><span data-stu-id="107b6-120"><a href="media-type-attributes.md">Media Type Attributes</a> for all nodes.</span></span><br/></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="107b6-121">Los valores de atributo, excepto las referencias de puntero y los valores de matriz, se pueden cambiar.</span><span class="sxs-lookup"><span data-stu-id="107b6-121">The attribute values, except for pointer references and array values, can be changed.</span></span> <span data-ttu-id="107b6-122">Para cambiar un valor de atributo, escriba el nuevo valor junto al atributo y haga clic en **Guardar** en el **Panel atributos**.</span><span class="sxs-lookup"><span data-stu-id="107b6-122">To change an attribute value, type in the new value next to the attribute and click **Save** on the **Attributes Pane**.</span></span> <span data-ttu-id="107b6-123">El nuevo valor se actualiza en el almacén de atributos y se aplica a la topología solo después de resolverlo.</span><span class="sxs-lookup"><span data-stu-id="107b6-123">The new value is updated in the attribute store and applied to the topology only after it is resolved.</span></span>

## <a name="to-add-a-new-attribute-for-a-node"></a><span data-ttu-id="107b6-124">Para agregar un nuevo atributo para un nodo</span><span class="sxs-lookup"><span data-stu-id="107b6-124">To add a new attribute for a node</span></span>

1.  <span data-ttu-id="107b6-125">Seleccione el nodo haciendo clic en él en el **Panel topología**.</span><span class="sxs-lookup"><span data-stu-id="107b6-125">Select the node by clicking it on the **Topology Pane**.</span></span>

    <span data-ttu-id="107b6-126">Los atributos que se establecen en el nodo se muestran en el **Panel atributos**.</span><span class="sxs-lookup"><span data-stu-id="107b6-126">The attributes that are set on the node are shown on the **Attributes Pane**.</span></span>

2.  <span data-ttu-id="107b6-127">En el **Panel atributos**, haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="107b6-127">On the **Attributes Pane**, click **Add**.</span></span>

    <span data-ttu-id="107b6-128">Se abrirá el cuadro de diálogo **Agregar atributo** .</span><span class="sxs-lookup"><span data-stu-id="107b6-128">This opens the **Add Attribute** dialog box.</span></span>

3.  <span data-ttu-id="107b6-129">En la primera lista desplegable, elija la categoría de atributo.</span><span class="sxs-lookup"><span data-stu-id="107b6-129">From the first drop-down list, choose the Attribute category.</span></span>

    <span data-ttu-id="107b6-130">Las categorías dependen del nodo de la topología.</span><span class="sxs-lookup"><span data-stu-id="107b6-130">The categories depend on the topology node.</span></span> <span data-ttu-id="107b6-131">Por ejemplo, para el nodo de origen, la lista desplegable muestra los **atributos de descriptor de presentación** y los atributos de **nodo** como categorías disponibles.</span><span class="sxs-lookup"><span data-stu-id="107b6-131">For example, for the source node, the drop-down list shows **Presentation Descriptor Attributes** and **Node Attributes** as the available categories.</span></span>

4.  <span data-ttu-id="107b6-132">En la segunda lista desplegable, elija el atributo que desea establecer en el nodo.</span><span class="sxs-lookup"><span data-stu-id="107b6-132">From the second drop-down list, choose the attribute that you want to set on the node.</span></span>

5.  <span data-ttu-id="107b6-133">En el cuadro de edición, agregue el valor para el atributo.</span><span class="sxs-lookup"><span data-stu-id="107b6-133">In the edit box, add the value for the attribute.</span></span>

6.  <span data-ttu-id="107b6-134">Haga clic en **Agregar** para agregar el atributo y volver a la ventana principal, o haga clic en **Cancelar** para cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="107b6-134">Click **Add** to add the attribute and return to the main window, or click **Cancel** to cancel the operation.</span></span>

7.  <span data-ttu-id="107b6-135">En el menú **topología** , haga clic en **resolver topología** para establecer el nuevo atributo en la topología.</span><span class="sxs-lookup"><span data-stu-id="107b6-135">From the **Topology** menu, click **Resolve Topology** to set the new attribute to the topology.</span></span>

## <a name="related-topics"></a><span data-ttu-id="107b6-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="107b6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="107b6-137">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="107b6-137">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 




