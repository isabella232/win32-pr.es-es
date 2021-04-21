---
UID: NE:directml.DML_GRAPH_EDGE_TYPE
title: DML_GRAPH_EDGE_TYPE
description: Define constantes que especifican un tipo de borde de grafo. Consulte [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) para el uso de esta enumeración.
helpviewer_keywords:
- DML_GRAPH_EDGE_TYPE
- DML_GRAPH_EDGE_TYPE structure
- direct3d12.dml_graph_edge_type
- directml/DML_GRAPH_EDGE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_TYPE, DML_GRAPH_EDGE_TYPE structure, direct3d12.dml_graph_edge_type, directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
- directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
ms.openlocfilehash: d65649fcd2115cc7cdcc1b01da20ef44b0436e6f
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803798"
---
# <a name="dml_graph_edge_type-enumeration-directmlh"></a><span data-ttu-id="a9107-104">DML_GRAPH_EDGE_TYPE enumeración (directml.h)</span><span class="sxs-lookup"><span data-stu-id="a9107-104">DML_GRAPH_EDGE_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="a9107-105">Define constantes que especifican un tipo de borde de grafo.</span><span class="sxs-lookup"><span data-stu-id="a9107-105">Defines constants that specify a type of graph edge.</span></span> <span data-ttu-id="a9107-106">Consulte [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) para el uso de esta enumeración.</span><span class="sxs-lookup"><span data-stu-id="a9107-106">See [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) for the usage of this enumeration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9107-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="a9107-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="a9107-108">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="a9107-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9107-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9107-109">Syntax</span></span>
```cpp
typedef enum DML_GRAPH_EDGE_TYPE {
  DML_GRAPH_EDGE_TYPE_INVALID,
  DML_GRAPH_EDGE_TYPE_INPUT,
  DML_GRAPH_EDGE_TYPE_OUTPUT,
  DML_GRAPH_EDGE_TYPE_INTERMEDIATE
} ;
```

## <a name="constants"></a><span data-ttu-id="a9107-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="a9107-110">Constants</span></span>

| <span data-ttu-id="a9107-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="a9107-111">Name</span></span> | <span data-ttu-id="a9107-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9107-112">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="a9107-113">DML_GRAPH_EDGE_TYPE_INVALID</span><span class="sxs-lookup"><span data-stu-id="a9107-113">DML_GRAPH_EDGE_TYPE_INVALID</span></span> | <span data-ttu-id="a9107-114">Especifica un tipo de borde de grafo desconocido y nunca es válido.</span><span class="sxs-lookup"><span data-stu-id="a9107-114">Specifies an unknown graph edge type, and is never valid.</span></span> <span data-ttu-id="a9107-115">El uso de este valor produce un error.</span><span class="sxs-lookup"><span data-stu-id="a9107-115">Using this value results in an error.</span></span> |
| <span data-ttu-id="a9107-116">DML_GRAPH_EDGE_TYPE_INPUT</span><span class="sxs-lookup"><span data-stu-id="a9107-116">DML_GRAPH_EDGE_TYPE_INPUT</span></span> | <span data-ttu-id="a9107-117">Especifica que el borde del gráfico se describe mediante la [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) gráfico.</span><span class="sxs-lookup"><span data-stu-id="a9107-117">Specifies that the graph edge is described by the [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="a9107-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9107-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span></span> | <span data-ttu-id="a9107-119">Especifica que el borde del gráfico se describe mediante la [estructura DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) gráfico.</span><span class="sxs-lookup"><span data-stu-id="a9107-119">Specifies that the graph edge is described by the [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="a9107-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span><span class="sxs-lookup"><span data-stu-id="a9107-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span></span> | <span data-ttu-id="a9107-121">Especifica que el borde del gráfico se describe mediante la [estructura DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) gráfico.</span><span class="sxs-lookup"><span data-stu-id="a9107-121">Specifies that the graph edge is described by the [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) structure.</span></span><br><br><span data-ttu-id="a9107-122">Disponibilidad de ##</span><span class="sxs-lookup"><span data-stu-id="a9107-122">## Availability</span></span><br><br><span data-ttu-id="a9107-123">Esta API se introdujo en la versión de `1.1.0` DirectML.</span><span class="sxs-lookup"><span data-stu-id="a9107-123">This API was introduced in DirectML version `1.1.0`.</span></span> |


## <a name="requirements"></a><span data-ttu-id="a9107-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9107-124">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a9107-125">**Header**</span><span class="sxs-lookup"><span data-stu-id="a9107-125">**Header**</span></span> | <span data-ttu-id="a9107-126">directml.h</span><span class="sxs-lookup"><span data-stu-id="a9107-126">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="a9107-127">Consulta también</span><span class="sxs-lookup"><span data-stu-id="a9107-127">See also</span></span>

* [<span data-ttu-id="a9107-128">Método IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="a9107-128">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="a9107-129">DML_GRAPH_DESC estructura</span><span class="sxs-lookup"><span data-stu-id="a9107-129">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)     
* [<span data-ttu-id="a9107-130">DML_GRAPH_EDGE_DESC estructura</span><span class="sxs-lookup"><span data-stu-id="a9107-130">DML_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_graph_edge_desc.md)
* [<span data-ttu-id="a9107-131">DML_INPUT_GRAPH_EDGE_DESC estructura</span><span class="sxs-lookup"><span data-stu-id="a9107-131">DML_INPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_input_graph_edge_desc.md)
* [<span data-ttu-id="a9107-132">DML_OUTPUT_GRAPH_EDGE_DESC estructura</span><span class="sxs-lookup"><span data-stu-id="a9107-132">DML_OUTPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_output_graph_edge_desc.md)
* [<span data-ttu-id="a9107-133">DML_INTERMEDIATE_GRAPH_EDGE_DESC estructura</span><span class="sxs-lookup"><span data-stu-id="a9107-133">DML_INTERMEDIATE_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_intermediate_graph_edge_desc.md)