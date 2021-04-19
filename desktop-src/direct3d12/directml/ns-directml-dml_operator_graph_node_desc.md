---
UID: NS:directml.DML_OPERATOR_GRAPH_NODE_DESC
title: DML_OPERATOR_GRAPH_NODE_DESC
description: 'Describe un nodo dentro de un gráfico de operadores DirectML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) y que se pasa a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).'
helpviewer_keywords:
- DML_OPERATOR_GRAPH_NODE_DESC
- DML_OPERATOR_GRAPH_NODE_DESC structure
- direct3d12.dml_operator_graph_node_desc
- directml/DML_OPERATOR_GRAPH_NODE_DESC
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
- DML_OPERATOR_GRAPH_NODE_DESC
- directml/DML_OPERATOR_GRAPH_NODE_DESC
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
- DML_OPERATOR_GRAPH_NODE_DESC
ms.openlocfilehash: 6081f81044ff2ce384f7906af9c6e80f6b06f774
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721271"
---
# <a name="dml_operator_graph_node_desc-structure-directmlh"></a><span data-ttu-id="0bce1-103">DML_OPERATOR_GRAPH_NODE_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="0bce1-103">DML_OPERATOR_GRAPH_NODE_DESC structure (directml.h)</span></span>
<span data-ttu-id="0bce1-104">Describe un nodo dentro de un gráfico de operadores DirectML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) y que se pasa a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="0bce1-104">Decribes a node within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

<span data-ttu-id="0bce1-105">El comportamiento de este nodo lo define un operador DirectML.</span><span class="sxs-lookup"><span data-stu-id="0bce1-105">The behavior of this node is defined by a DirectML operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bce1-106">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="0bce1-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="0bce1-107">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="0bce1-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0bce1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bce1-108">Syntax</span></span>
```cpp
struct DML_OPERATOR_GRAPH_NODE_DESC {
  IDMLOperator *Operator;
  const char   *Name;
};
```



## <a name="members"></a><span data-ttu-id="0bce1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0bce1-109">Members</span></span>

`Operator`

<span data-ttu-id="0bce1-110">Tipo: <b> [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)\*</b></span><span class="sxs-lookup"><span data-stu-id="0bce1-110">Type: <b>[IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)\*</b></span></span>

<span data-ttu-id="0bce1-111">Operador DirectML que define el comportamiento del nodo.</span><span class="sxs-lookup"><span data-stu-id="0bce1-111">A DirectML operator defining the behavior of the node.</span></span>


`Name`

<span data-ttu-id="0bce1-112">Tipo: \_ campo \_ z \_ \_ Maybenull \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="0bce1-112">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="0bce1-113">Un nombre opcional para la conexión del grafo.</span><span class="sxs-lookup"><span data-stu-id="0bce1-113">An optional name for the graph connection.</span></span> <span data-ttu-id="0bce1-114">Si se proporciona, se podría usar dentro de ciertos mensajes de error emitidos por la capa de depuración DirectML.</span><span class="sxs-lookup"><span data-stu-id="0bce1-114">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="0bce1-115">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="0bce1-115">Availability</span></span>

<span data-ttu-id="0bce1-116">Esta API se presentó en la versión DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="0bce1-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="0bce1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bce1-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0bce1-118">**Header**</span><span class="sxs-lookup"><span data-stu-id="0bce1-118">**Header**</span></span> | <span data-ttu-id="0bce1-119">directml. h</span><span class="sxs-lookup"><span data-stu-id="0bce1-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="0bce1-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bce1-120">See also</span></span>

* [<span data-ttu-id="0bce1-121">IDMLDevice1:: CompileGraph (método)</span><span class="sxs-lookup"><span data-stu-id="0bce1-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="0bce1-122">Estructura de DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="0bce1-122">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="0bce1-123">Estructura de DML_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="0bce1-123">DML_GRAPH_NODE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_node_desc)