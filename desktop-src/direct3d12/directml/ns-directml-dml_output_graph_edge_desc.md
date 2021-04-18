---
UID: NS:directml.DML_OUTPUT_GRAPH_EDGE_DESC
title: DML_OUTPUT_GRAPH_EDGE_DESC
description: 'Describe una conexión dentro de un gráfico de operadores DirectML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) y que se pasa a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Esta estructura se usa para definir una conexión desde una salida de un nodo interno a una salida de grafo.'
helpviewer_keywords:
- DML_OUTPUT_GRAPH_EDGE_DESC
- DML_OUTPUT_GRAPH_EDGE_DESC structure
- direct3d12.dml_output_graph_edge_desc
- directml/DML_OUTPUT_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/05/2020
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
- DML_OUTPUT_GRAPH_EDGE_DESC
- directml/DML_OUTPUT_GRAPH_EDGE_DESC
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
- DML_OUTPUT_GRAPH_EDGE_DESC
ms.openlocfilehash: d1d48de0fa3bf2665269ebf2226de4e9911a1670
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721270"
---
# <a name="dml_output_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="8a02b-104">DML_OUTPUT_GRAPH_EDGE_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="8a02b-104">DML_OUTPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="8a02b-105">Describe una conexión dentro de un gráfico de operadores DirectML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) y que se pasa a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="8a02b-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="8a02b-106">Esta estructura se usa para definir una conexión desde una salida de un nodo interno a una salida de grafo.</span><span class="sxs-lookup"><span data-stu-id="8a02b-106">This structure is used to define a connection from an output of an internal node to a graph output.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a02b-107">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="8a02b-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="8a02b-108">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="8a02b-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a02b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a02b-109">Syntax</span></span>
```cpp
struct DML_OUTPUT_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       GraphOutputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="8a02b-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a02b-110">Members</span></span>

`FromNodeIndex`




`FromNodeOutputIndex`




`GraphOutputIndex`

<span data-ttu-id="8a02b-111">Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a02b-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="8a02b-112">Índice del resultado del gráfico al que se especifica una conexión de una salida de nodo interno.</span><span class="sxs-lookup"><span data-stu-id="8a02b-112">The index of the graph output to which a connection from an internal node output is specified.</span></span>


`Name`

<span data-ttu-id="8a02b-113">Tipo: \_ campo \_ z \_ \_ Maybenull \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="8a02b-113">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="8a02b-114">Un nombre opcional para la conexión del grafo.</span><span class="sxs-lookup"><span data-stu-id="8a02b-114">An optional name for the graph connection.</span></span> <span data-ttu-id="8a02b-115">Si se proporciona, se podría usar dentro de ciertos mensajes de error emitidos por la capa de depuración DirectML.</span><span class="sxs-lookup"><span data-stu-id="8a02b-115">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="8a02b-116">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="8a02b-116">Availability</span></span>

<span data-ttu-id="8a02b-117">Esta API se presentó en la versión DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="8a02b-117">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="8a02b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a02b-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8a02b-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="8a02b-119">**Header**</span></span> | <span data-ttu-id="8a02b-120">directml. h</span><span class="sxs-lookup"><span data-stu-id="8a02b-120">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="8a02b-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a02b-121">See also</span></span>

* [<span data-ttu-id="8a02b-122">IDMLDevice1:: CompileGraph (método)</span><span class="sxs-lookup"><span data-stu-id="8a02b-122">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="8a02b-123">Estructura de DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="8a02b-123">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="8a02b-124">Estructura de DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="8a02b-124">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)