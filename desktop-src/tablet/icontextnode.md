---
description: Representa un nodo en un árbol de objetos que se crean como parte del análisis de tinta.
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: Interfaz IContextNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dbc9d7a0c1cc6ededf5d59585c806b54d6cfa32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082153"
---
# <a name="icontextnode-interface"></a><span data-ttu-id="88225-103">Interfaz IContextNode</span><span class="sxs-lookup"><span data-stu-id="88225-103">IContextNode interface</span></span>

<span data-ttu-id="88225-104">Representa un nodo en un árbol de objetos que se crean como parte del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="88225-104">Represents a node in a tree of objects that are created as part of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="88225-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="88225-105">Members</span></span>

<span data-ttu-id="88225-106">La interfaz **IContextNode** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="88225-106">The **IContextNode** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="88225-107">**IContextNode** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="88225-107">**IContextNode** also has these types of members:</span></span>

-   [<span data-ttu-id="88225-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="88225-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="88225-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="88225-109">Methods</span></span>

<span data-ttu-id="88225-110">La interfaz **IContextNode** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="88225-110">The **IContextNode** interface has these methods.</span></span>



| <span data-ttu-id="88225-111">Método</span><span class="sxs-lookup"><span data-stu-id="88225-111">Method</span></span>                                                                                  | <span data-ttu-id="88225-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="88225-112">Description</span></span>                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88225-113">**AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="88225-113">**AddContextLink**</span></span>](icontextnode-addcontextlink.md)                                   | <span data-ttu-id="88225-114">Agrega un nuevo [**IContextLink**](icontextlink.md) a la colección de vínculos de contexto del objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="88225-114">Adds a new [**IContextLink**](icontextlink.md) to the **IContextNode** object's context link collection.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="88225-115">**AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="88225-115">**AddPropertyData**</span></span>](icontextnode-addpropertydata.md)                                 | <span data-ttu-id="88225-116">Agrega una parte de los datos específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88225-116">Adds a piece of application-specific data.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="88225-117">**Confirm**</span><span class="sxs-lookup"><span data-stu-id="88225-117">**Confirm**</span></span>](icontextnode-confirm.md)                                                 | <span data-ttu-id="88225-118">Modifica el tipo de confirmación, que controla lo que el objeto [**IInkAnalyzer**](iinkanalyzer.md) puede cambiar sobre **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="88225-118">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the **IContextNode**.</span></span><br/>                                                                         |
| [<span data-ttu-id="88225-119">**ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="88225-119">**ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)                       | <span data-ttu-id="88225-120">Determina si el objeto **IContextNode** contiene datos almacenados en el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="88225-120">Determines whether the **IContextNode** object contains data stored under the specified identifier.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="88225-121">**CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="88225-121">**CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md) | <span data-ttu-id="88225-122">Crea un objeto **IContextNode** secundario que solo contiene información sobre el tipo, el identificador y la ubicación.</span><span class="sxs-lookup"><span data-stu-id="88225-122">Creates a child **IContextNode** object that contains only information on type, identifier, and location.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="88225-123">**CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="88225-123">**CreateSubNode**</span></span>](icontextnode-createsubnode.md)                                     | <span data-ttu-id="88225-124">Crea un nuevo objeto **IContextNode** secundario.</span><span class="sxs-lookup"><span data-stu-id="88225-124">Creates a new child **IContextNode** object.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="88225-125">**DeleteContextLink**</span><span class="sxs-lookup"><span data-stu-id="88225-125">**DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)                             | <span data-ttu-id="88225-126">Elimina un objeto [**IContextLink**](icontextlink.md) de la colección de vínculos del objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="88225-126">Deletes an [**IContextLink**](icontextlink.md) object from the **IContextNode** object's link collection.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="88225-127">**DeleteSubNode**</span><span class="sxs-lookup"><span data-stu-id="88225-127">**DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)                                     | <span data-ttu-id="88225-128">Quita un **IContextNode** secundario.</span><span class="sxs-lookup"><span data-stu-id="88225-128">Removes a child **IContextNode**.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="88225-129">**GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="88225-129">**GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)                                 | <span data-ttu-id="88225-130">Recupera una colección de objetos [**IContextLink**](icontextlink.md) que representa relaciones con otros objetos **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="88225-130">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other **IContextNode** objects.</span></span><br/>                                                                          |
| [<span data-ttu-id="88225-131">**GetId**</span><span class="sxs-lookup"><span data-stu-id="88225-131">**GetId**</span></span>](icontextnode-getid.md)                                                     | <span data-ttu-id="88225-132">Recupera el identificador del objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="88225-132">Retrieves the identifier for the **IContextNode** object.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="88225-133">**GetLocation**</span><span class="sxs-lookup"><span data-stu-id="88225-133">**GetLocation**</span></span>](icontextnode-getlocation.md)                                         | <span data-ttu-id="88225-134">Recupera la posición y el tamaño del objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="88225-134">Retrieves the position and size of the **IContextNode** object.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="88225-135">**GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="88225-135">**GetParentNode**</span></span>](icontextnode-getparentnode.md)                                     | <span data-ttu-id="88225-136">Recupera el nodo primario de este **IContextNode** en el árbol de nodos de contexto.</span><span class="sxs-lookup"><span data-stu-id="88225-136">Retrieves the parent node of this **IContextNode** in the context node tree.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="88225-137">**GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="88225-137">**GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)                     | <span data-ttu-id="88225-138">Recupera el valor que indica si un objeto **IContextNode** se rellena parcialmente o está totalmente rellenado.</span><span class="sxs-lookup"><span data-stu-id="88225-138">Retrieves the value that indicates whether an **IContextNode** object is partially populated or fully populated.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="88225-139">**GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="88225-139">**GetPropertyData**</span></span>](icontextnode-getpropertydata.md)                                 | <span data-ttu-id="88225-140">Recupera datos específicos de la aplicación u otros datos de propiedad dado el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="88225-140">Retrieves application-specific data or other property data given the specified identifier.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="88225-141">**GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="88225-141">**GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)                           | <span data-ttu-id="88225-142">Recupera los identificadores para los que hay datos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="88225-142">Retrieves the identifiers for which there is property data.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="88225-143">**GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="88225-143">**GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)                                   | <span data-ttu-id="88225-144">Recupera el número de trazos asociados al objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="88225-144">Retrieves the number of strokes associated with the **IContextNode** object.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="88225-145">**GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="88225-145">**GetStrokeId**</span></span>](icontextnode-getstrokeid.md)                                         | <span data-ttu-id="88225-146">Recupera el identificador de trazo para el trazo al que hace referencia un valor de índice dentro del objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="88225-146">Retrieves the stroke identifier for the stroke referenced by an index value within the **IContextNode** object.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="88225-147">**GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="88225-147">**GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)                                       | <span data-ttu-id="88225-148">Recupera una matriz de identificadores para los trazos dentro del objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="88225-148">Retrieves an array of identifiers for the strokes within the **IContextNode** object.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="88225-149">**GetStrokePacketDataById**</span><span class="sxs-lookup"><span data-stu-id="88225-149">**GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)                 | <span data-ttu-id="88225-150">Recupera una matriz que contiene los datos de propiedad del paquete para el trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="88225-150">Retrieves an array containing the packet property data for the specified stroke.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="88225-151">**GetStrokePacketDescriptionById**</span><span class="sxs-lookup"><span data-stu-id="88225-151">**GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)   | <span data-ttu-id="88225-152">Recupera una matriz que contiene los identificadores de propiedad de paquete para el trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="88225-152">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="88225-153">**GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="88225-153">**GetSubNodes**</span></span>](icontextnode-getsubnodes.md)                                         | <span data-ttu-id="88225-154">Recupera los nodos secundarios directos del objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="88225-154">Retrieves the direct child nodes of the **IContextNode** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="88225-155">**GetType**</span><span class="sxs-lookup"><span data-stu-id="88225-155">**GetType**</span></span>](icontextnode-gettype.md)                                                 | <span data-ttu-id="88225-156">Recupera el tipo del objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="88225-156">Retrieves the type of the **IContextNode** object.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="88225-157">**GetTypeName**</span><span class="sxs-lookup"><span data-stu-id="88225-157">**GetTypeName**</span></span>](icontextnode-gettypename.md)                                         | <span data-ttu-id="88225-158">Recupera un nombre de tipo legible de este **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="88225-158">Retrieves a human-readable type name of this **IContextNode**.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="88225-159">**IsConfirmed**</span><span class="sxs-lookup"><span data-stu-id="88225-159">**IsConfirmed**</span></span>](icontextnode-isconfirmed.md)                                         | <span data-ttu-id="88225-160">Recupera un valor que indica si se confirma el objeto **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="88225-160">Retrieves a value that indicates whether the **IContextNode** object is confirmed.</span></span> <span data-ttu-id="88225-161">[**IInkAnalyzer**](iinkanalyzer.md) no puede cambiar el tipo de nodo ni los trazos asociados de los objetos **IContextNode** confirmados.</span><span class="sxs-lookup"><span data-stu-id="88225-161">[**IInkAnalyzer**](iinkanalyzer.md) cannot change the node type and associated strokes for confirmed **IContextNode** objects.</span></span><br/> |
| [<span data-ttu-id="88225-162">**LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="88225-162">**LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)                           | <span data-ttu-id="88225-163">Vuelve a crear los datos de propiedad internos y específicos de la aplicación para una matriz de bytes que se creó anteriormente con [**IContextNode:: SavePropertiesData**](icontextnode-savepropertiesdata.md).</span><span class="sxs-lookup"><span data-stu-id="88225-163">Recreates the application-specific and internal property data for an array of bytes that was previously created with [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).</span></span><br/>                  |
| [<span data-ttu-id="88225-164">**MoveSubNodeToPosition**</span><span class="sxs-lookup"><span data-stu-id="88225-164">**MoveSubNodeToPosition**</span></span>](icontextnode-movesubnodetoposition.md)                     | <span data-ttu-id="88225-165">Reordena un objeto **IContextNode** secundario especificado al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="88225-165">Reorders a specified child **IContextNode** object to the specified index.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="88225-166">**RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="88225-166">**RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)                           | <span data-ttu-id="88225-167">Quita una parte de los datos específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88225-167">Removes a piece of application-specific data.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="88225-168">**Reparent**</span><span class="sxs-lookup"><span data-stu-id="88225-168">**Reparent**</span></span>](icontextnode-reparent.md)                                               | <span data-ttu-id="88225-169">Mueve este objeto **IContextNode** de la colección de subnodos del nodo de contexto primario a la colección de subnodos del nodo de contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="88225-169">Moves this **IContextNode** object from its parent context node's subnodes collection to the specified context node's subnodes collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="88225-170">**ReparentStrokeByIdToNode**</span><span class="sxs-lookup"><span data-stu-id="88225-170">**ReparentStrokeByIdToNode**</span></span>](icontextnode-reparentstrokebyidtonode.md)               | <span data-ttu-id="88225-171">Mueve los datos de trazo desde este **IContextNode** al **IContextNode** especificado.</span><span class="sxs-lookup"><span data-stu-id="88225-171">Moves stroke data from this **IContextNode** to the specified **IContextNode**.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="88225-172">**SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="88225-172">**SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)                           | <span data-ttu-id="88225-173">Recupera una matriz de bytes que contiene los datos de propiedad internos y específicos de la aplicación para este **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="88225-173">Retrieves an array of bytes that contains the application-specific and internal property data for this **IContextNode**.</span></span><br/>                                                                                           |
| [<span data-ttu-id="88225-174">**SetLocation**</span><span class="sxs-lookup"><span data-stu-id="88225-174">**SetLocation**</span></span>](icontextnode-setlocation.md)                                         | <span data-ttu-id="88225-175">Actualiza la posición y el tamaño de este **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="88225-175">Updates the position and size of this **IContextNode**.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="88225-176">**SetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="88225-176">**SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)                     | <span data-ttu-id="88225-177">Modifica el valor que indica si este **IContextNode** se rellena parcial o totalmente.</span><span class="sxs-lookup"><span data-stu-id="88225-177">Modifies the value that indicates whether this **IContextNode** is partially or fully populated.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="88225-178">**SetStrokes**</span><span class="sxs-lookup"><span data-stu-id="88225-178">**SetStrokes**</span></span>](icontextnode-setstrokes.md)                                           | <span data-ttu-id="88225-179">Asocia los trazos especificados a este **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="88225-179">Associates the specified strokes with this **IContextNode**.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="88225-180">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88225-180">Remarks</span></span>

<span data-ttu-id="88225-181">Los tipos de nodos se describen en las constantes de [tipos de nodo de contexto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="88225-181">The types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="88225-182">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="88225-182">Examples</span></span>

<span data-ttu-id="88225-183">En el ejemplo siguiente se muestra un método que examina un **IContextNode**; el método hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="88225-183">The following example shows a method that examines an **IContextNode**; the method does the following:</span></span>

-   <span data-ttu-id="88225-184">Obtiene el tipo del nodo de contexto.</span><span class="sxs-lookup"><span data-stu-id="88225-184">Gets the context node's type.</span></span> <span data-ttu-id="88225-185">Si el nodo de contexto es una tinta sin clasificar, una sugerencia de análisis o un nodo de reconocedor personalizado, llama a un método auxiliar para examinar propiedades específicas del tipo de nodo.</span><span class="sxs-lookup"><span data-stu-id="88225-185">If the context node is an unclassified ink, analysis hint, or custom recognizer node, it calls a helper method to examine specific properties of the node type.</span></span>
-   <span data-ttu-id="88225-186">Si el nodo tiene subnodos, examina cada subnodo llamando a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="88225-186">If the node has subnodes, it examines each subnode by calling itself.</span></span>
-   <span data-ttu-id="88225-187">Si el nodo es un nodo de hoja de tinta, examina los datos de trazo del nodo llamando a un método auxiliar.</span><span class="sxs-lookup"><span data-stu-id="88225-187">If the node is an ink leaf node, it examines the stroke data for the node by calling a helper method.</span></span>

<span data-ttu-id="88225-188">Propio InkAnalysis API le permite crear un nodo de línea que contiene palabras de tinta y palabras de texto.</span><span class="sxs-lookup"><span data-stu-id="88225-188">Ihe InkAnalysis API allows you to create a line node that contains ink words and text words.</span></span> <span data-ttu-id="88225-189">Sin embargo, el analizador pasará por alto estos nodos mixtos y los tratará como nodos externos.</span><span class="sxs-lookup"><span data-stu-id="88225-189">However, the parser will ignore these mixed nodes and will treat them like foreign nodes.</span></span> <span data-ttu-id="88225-190">Esto afectará a la precisión de análisis de la detección de anotaciones manuscritas cuando el usuario final escribe en este nodo mixto o en torno a este.</span><span class="sxs-lookup"><span data-stu-id="88225-190">This will have impact the parsing accuracy of detecting ink annotations when the end user writes on or around this mixed node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="88225-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88225-191">Requirements</span></span>



| <span data-ttu-id="88225-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="88225-192">Requirement</span></span> | <span data-ttu-id="88225-193">Value</span><span class="sxs-lookup"><span data-stu-id="88225-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88225-194">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88225-194">Minimum supported client</span></span><br/> | <span data-ttu-id="88225-195">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="88225-195">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="88225-196">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88225-196">Minimum supported server</span></span><br/> | <span data-ttu-id="88225-197">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="88225-197">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="88225-198">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88225-198">Header</span></span><br/>                   | <dl> <span data-ttu-id="88225-199"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="88225-199"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="88225-200">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88225-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88225-201"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88225-201"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="88225-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="88225-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88225-203">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="88225-203">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="88225-204">Tipos de nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="88225-204">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="88225-205">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="88225-205">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="88225-206">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="88225-206">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

