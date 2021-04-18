---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Describe un gráfico de operadores de DirectML utilizados para compilar un operador combinado y optimizado.
helpviewer_keywords:
- DML_GRAPH_DESC
- DML_GRAPH_DESC structure
- direct3d12.dml_graph_desc
- directml/DML_GRAPH_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_DESC, DML_GRAPH_DESC structure, direct3d12.dml_graph_desc, directml/DML_GRAPH_DESC
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_GRAPH_DESC
- directml/DML_GRAPH_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_GRAPH_DESC
ms.openlocfilehash: e72209d19bb26524576783becbbfbf94566d8370
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721282"
---
# <a name="dml_graph_desc-structure-directmlh"></a><span data-ttu-id="c85e5-103">DML_GRAPH_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="c85e5-103">DML_GRAPH_DESC structure (directml.h)</span></span>

<span data-ttu-id="c85e5-104">Describe un gráfico de operadores de DirectML utilizados para compilar un operador combinado y optimizado.</span><span class="sxs-lookup"><span data-stu-id="c85e5-104">Describes a graph of DirectML operators used to compile a combined, optimized operator.</span></span> <span data-ttu-id="c85e5-105">Vea [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="c85e5-105">See [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c85e5-106">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="c85e5-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="c85e5-107">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="c85e5-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c85e5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c85e5-108">Syntax</span></span>
```cpp
struct DML_GRAPH_DESC {
  UINT                      InputCount;
  UINT                      OutputCount;
  UINT                      NodeCount;
  const DML_GRAPH_NODE_DESC *Nodes;
  UINT                      InputEdgeCount;
  const DML_GRAPH_EDGE_DESC *InputEdges;
  UINT                      OutputEdgeCount;
  const DML_GRAPH_EDGE_DESC *OutputEdges;
  UINT                      IntermediateEdgeCount;
  const DML_GRAPH_EDGE_DESC *IntermediateEdges;
};
```



## <a name="members"></a><span data-ttu-id="c85e5-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c85e5-109">Members</span></span>

`InputCount`

<span data-ttu-id="c85e5-110">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c85e5-110">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c85e5-111">El número de entradas del gráfico global.</span><span class="sxs-lookup"><span data-stu-id="c85e5-111">The number of inputs of the overall graph.</span></span> <span data-ttu-id="c85e5-112">Cada entrada de gráfico puede estar conectada a un número variable de nodos internos, por lo que puede ser diferente de *InputEdgeCount*.</span><span class="sxs-lookup"><span data-stu-id="c85e5-112">Each graph input may be connected to a variable number of internal nodes, therefore this may be different from *InputEdgeCount*.</span></span>


`OutputCount`

<span data-ttu-id="c85e5-113">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c85e5-113">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c85e5-114">El número de salidas del gráfico global.</span><span class="sxs-lookup"><span data-stu-id="c85e5-114">The number of outputs of the overall graph.</span></span> <span data-ttu-id="c85e5-115">Cada salida del gráfico puede estar conectada a un número variable de nodos internos, por lo que puede ser diferente de *OutputEdgeCount*.</span><span class="sxs-lookup"><span data-stu-id="c85e5-115">Each graph output may be connected to a variable number of internal nodes, therefore this may be different from *OutputEdgeCount*.</span></span>


`NodeCount`

<span data-ttu-id="c85e5-116">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c85e5-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c85e5-117">Número de nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="c85e5-117">The number of internal nodes in the graph.</span></span>


`Nodes`

<span data-ttu-id="c85e5-118">Tipo: \_ tamaño de campo \_ \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="c85e5-118">Type: \_Field\_size\_(NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)\***</span></span>

<span data-ttu-id="c85e5-119">Los nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="c85e5-119">The internal nodes in the graph.</span></span>


`InputEdgeCount`

<span data-ttu-id="c85e5-120">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c85e5-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c85e5-121">El número de conexiones entre las entradas del gráfico y las entradas de los nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="c85e5-121">The number of connections between graph inputs and inputs of internal nodes in the graph.</span></span>


`InputEdges`

<span data-ttu-id="c85e5-122">Tipo: \_ tamaño de campo \_ \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="c85e5-122">Type: \_Field\_size\_(InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="c85e5-123">Matriz de conexiones entre las entradas del gráfico y las entradas de los nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="c85e5-123">An array of connections between graph inputs and inputs of internal nodes in the graph.</span></span> <span data-ttu-id="c85e5-124">El campo de *tipo* dentro de cada elemento debe establecerse en [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="c85e5-124">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`OutputEdgeCount`

<span data-ttu-id="c85e5-125">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c85e5-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c85e5-126">El número de conexiones entre las salidas del gráfico y las salidas de los nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="c85e5-126">The number of connections between graph outputs and outputs of internal nodes in the graph.</span></span>


`OutputEdges`

<span data-ttu-id="c85e5-127">Tipo: \_ tamaño de campo \_ \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="c85e5-127">Type: \_Field\_size\_(OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="c85e5-128">Matriz de conexiones entre las salidas del gráfico y las salidas de los nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="c85e5-128">An array of connections between graph outputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="c85e5-129">El campo de *tipo* dentro de cada elemento debe establecerse en [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="c85e5-129">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`IntermediateEdgeCount`

<span data-ttu-id="c85e5-130">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c85e5-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c85e5-131">El número de conexiones internas entre los nodos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="c85e5-131">The number of internal connections between nodes in the graph.</span></span>


`IntermediateEdges`

<span data-ttu-id="c85e5-132">Tipo: \_ tamaño de campo \_ \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="c85e5-132">Type: \_Field\_size\_(IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="c85e5-133">Matriz de conexiones entre las entradas y las salidas de los nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="c85e5-133">An array of connections between inputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="c85e5-134">El campo de tipo dentro de cada elemento se debe establecer en [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span><span class="sxs-lookup"><span data-stu-id="c85e5-134">The Type field within each element should be set to [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span></span>


## <a name="remarks"></a><span data-ttu-id="c85e5-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c85e5-135">Remarks</span></span>
<span data-ttu-id="c85e5-136">El gráfico descrito por esta estructura debe ser un gráfico acíclicos dirigido.</span><span class="sxs-lookup"><span data-stu-id="c85e5-136">The graph described by this structure must be a directed acyclic graph.</span></span> <span data-ttu-id="c85e5-137">Debe definir una conexión para la entrada y la salida de cada nodo proporcionado, excepto las entradas y salidas que son opcionales para el operador asociado.</span><span class="sxs-lookup"><span data-stu-id="c85e5-137">You must define a connection for the input and output of each supplied node, except for inputs and outputs that are optional for the associated operator.</span></span>

<span data-ttu-id="c85e5-138">Los nodos pueden usar operadores que se crearon con la marca [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) para ciertas entradas.</span><span class="sxs-lookup"><span data-stu-id="c85e5-138">Nodes may use operators that were created using the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag for certain inputs.</span></span> <span data-ttu-id="c85e5-139">Cualquier entrada de operador que use esta marca debe estar conectada a entradas de grafos.</span><span class="sxs-lookup"><span data-stu-id="c85e5-139">Any operator inputs using this flag must be connected to graph inputs.</span></span> <span data-ttu-id="c85e5-140">Todas las entradas de operador conectadas a la misma entrada de gráfico deben usar u omitir esta marca de forma equivalente.</span><span class="sxs-lookup"><span data-stu-id="c85e5-140">All operator inputs connected to the same graph input must use or omit this flag equivalently.</span></span>

<span data-ttu-id="c85e5-141">Es válido conectar los operadores cuyas entradas y salidas conectadas usan recuentos de dimensiones, tamaños y tipos de datos diferentes.</span><span class="sxs-lookup"><span data-stu-id="c85e5-141">It is legal to connect operators whose connected inputs and outputs use different dimension counts, sizes, and data types.</span></span> <span data-ttu-id="c85e5-142">Esto implica que cada operador interpreta de forma diferente el BLOB de datos tensores.</span><span class="sxs-lookup"><span data-stu-id="c85e5-142">This implies that the tensor data blob is interpreted differently by each operator.</span></span> <span data-ttu-id="c85e5-143">Sin embargo, el campo *TotalTensorSizeInBytes* de entradas y salidas de tensores conectadas debe ser idéntico.</span><span class="sxs-lookup"><span data-stu-id="c85e5-143">The *TotalTensorSizeInBytes* field of connected tensor inputs and outputs must be identical, though.</span></span> <span data-ttu-id="c85e5-144">Los operadores solo deben leer las regiones de los que han escrito los operadores anteriores.</span><span class="sxs-lookup"><span data-stu-id="c85e5-144">Operators should only read regions of tensors written by earlier operators.</span></span> <span data-ttu-id="c85e5-145">No se garantiza que las regiones de relleno de la salida de una operación (que resulten del uso de los progresos) se lean como cero por operadores de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="c85e5-145">Any padding regions in the output of an operation (resulting from the use of strides) are not guaranteed to be read as zero by down-stream operators.</span></span>

## <a name="availability"></a><span data-ttu-id="c85e5-146">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="c85e5-146">Availability</span></span>

<span data-ttu-id="c85e5-147">Esta API se presentó en la versión DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="c85e5-147">This API was introduced in DirectML version `1.1.0`.</span></span>


## <a name="requirements"></a><span data-ttu-id="c85e5-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c85e5-148">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c85e5-149">**Header**</span><span class="sxs-lookup"><span data-stu-id="c85e5-149">**Header**</span></span> | <span data-ttu-id="c85e5-150">directml. h</span><span class="sxs-lookup"><span data-stu-id="c85e5-150">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="c85e5-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="c85e5-151">See also</span></span>

* [<span data-ttu-id="c85e5-152">IDMLDevice1:: CompileGraph (método)</span><span class="sxs-lookup"><span data-stu-id="c85e5-152">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="c85e5-153">DML_GRAPH_NODE_DESC struct</span><span class="sxs-lookup"><span data-stu-id="c85e5-153">DML_GRAPH_NODE_DESC struct</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="c85e5-154">DML_GRAPH_EDGE_DESC struct</span><span class="sxs-lookup"><span data-stu-id="c85e5-154">DML_GRAPH_EDGE_DESC struct</span></span>](./ns-directml-dml_graph_edge_desc.md)