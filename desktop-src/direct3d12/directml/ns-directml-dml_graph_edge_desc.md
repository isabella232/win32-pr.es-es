---
UID: NS:directml.DML_GRAPH_EDGE_DESC
title: DML_GRAPH_EDGE_DESC
description: 'Un contenedor genérico para una conexión dentro de un gráfico de operadores DirectML definidos por [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) y que se pasa a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).'
helpviewer_keywords:
- DML_GRAPH_EDGE_DESC
- DML_GRAPH_EDGE_DESC structure
- direct3d12.dml_graph_edge_desc
- directml/DML_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_DESC, DML_GRAPH_EDGE_DESC structure, direct3d12.dml_graph_edge_desc, directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
- directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
ms.openlocfilehash: 636556cec6fa9982ea1a30e02f6019f93b815cf8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721281"
---
# <a name="dml_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="31f99-103">DML_GRAPH_EDGE_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="31f99-103">DML_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="31f99-104">Un contenedor genérico para una conexión dentro de un gráfico de operadores DirectML definidos por [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) y que se pasa a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="31f99-104">A generic container for a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31f99-105">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="31f99-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="31f99-106">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="31f99-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="31f99-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31f99-107">Syntax</span></span>
```cpp
struct DML_GRAPH_EDGE_DESC {
  DML_GRAPH_EDGE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a><span data-ttu-id="31f99-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="31f99-108">Members</span></span>

`Type`

<span data-ttu-id="31f99-109">Tipo: **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**</span><span class="sxs-lookup"><span data-stu-id="31f99-109">Type: **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**</span></span>

<span data-ttu-id="31f99-110">El tipo de borde del gráfico.</span><span class="sxs-lookup"><span data-stu-id="31f99-110">The type of graph edge.</span></span> <span data-ttu-id="31f99-111">Consulte [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) para los tipos disponibles y [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) para Dónde usar cada tipo.</span><span class="sxs-lookup"><span data-stu-id="31f99-111">See [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) for available types, and [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) for where to use each type.</span></span>


`Desc`

<span data-ttu-id="31f99-112">Tipo: \_ \_ tamaño \_ del campo ( \_ inexpress \_ ("depende del tipo de borde")) **const \* void**</span><span class="sxs-lookup"><span data-stu-id="31f99-112">Type: \_Field\_size\_(\_Inexpressible\_("Dependent on edge type")) **const void\***</span></span>

<span data-ttu-id="31f99-113">Puntero a la descripción del borde del gráfico.</span><span class="sxs-lookup"><span data-stu-id="31f99-113">A pointer to the graph edge description.</span></span> <span data-ttu-id="31f99-114">El tipo del struct señalado debe coincidir con el valor especificado en el *tipo*.</span><span class="sxs-lookup"><span data-stu-id="31f99-114">The type of the pointed-to struct must match the value specified in *Type*.</span></span>

## <a name="availability"></a><span data-ttu-id="31f99-115">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="31f99-115">Availability</span></span>

<span data-ttu-id="31f99-116">Esta API se presentó en la versión DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="31f99-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="31f99-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31f99-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="31f99-118">**Header**</span><span class="sxs-lookup"><span data-stu-id="31f99-118">**Header**</span></span> | <span data-ttu-id="31f99-119">directml. h</span><span class="sxs-lookup"><span data-stu-id="31f99-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="31f99-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="31f99-120">See also</span></span>

* [<span data-ttu-id="31f99-121">IDMLDevice1:: CompileGraph (método)</span><span class="sxs-lookup"><span data-stu-id="31f99-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="31f99-122">Estructura de DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="31f99-122">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)