---
UID: NE:directml.DML_AXIS_DIRECTION
title: DML_AXIS_DIRECTION
description: Define constantes que especifican la dirección de una operación a lo largo del eje especificado para el operador (por ejemplo, la suma, la selección de los elementos de la parte superior y la selección del elemento mínimo).
ms.topic: reference
tech.root: directml
ms.date: 10/28/2020
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
- DML_AXIS_DIRECTION
- directml/DML_AXIS_DIRECTION
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
- DML_AXIS_DIRECTION
ms.openlocfilehash: 18cd2189f88378245be0824e0a68e5f618008bc7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721228"
---
# <a name="dml_axis_direction-enumeration-directmlh"></a><span data-ttu-id="b909d-103">Enumeración DML_AXIS_DIRECTION (directml. h)</span><span class="sxs-lookup"><span data-stu-id="b909d-103">DML_AXIS_DIRECTION enumeration (directml.h)</span></span>

<span data-ttu-id="b909d-104">Define constantes que especifican la dirección de una operación a lo largo del eje especificado para el operador (por ejemplo, la suma, la selección de los elementos de la parte superior y la selección del elemento mínimo).</span><span class="sxs-lookup"><span data-stu-id="b909d-104">Defines constants that specify the direction of an operation along the given axis for the operator (for example, summation, selecting the top-k elements, selecting the minimum element).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b909d-105">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="b909d-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="b909d-106">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b909d-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b909d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b909d-107">Syntax</span></span>
```cpp
typedef enum DML_AXIS_DIRECTION {
  DML_AXIS_DIRECTION_INCREASING,
  DML_AXIS_DIRECTION_DECREASING
} ;
```

## <a name="constants"></a><span data-ttu-id="b909d-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="b909d-108">Constants</span></span>

| <span data-ttu-id="b909d-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="b909d-109">Name</span></span> | <span data-ttu-id="b909d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b909d-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="b909d-111">DML_AXIS_DIRECTION_INCREASING</span><span class="sxs-lookup"><span data-stu-id="b909d-111">DML_AXIS_DIRECTION_INCREASING</span></span> | <span data-ttu-id="b909d-112">Especifica el orden creciente (del índice inferior al índice alto).</span><span class="sxs-lookup"><span data-stu-id="b909d-112">Specifies increasing order (from the low index to the high index).</span></span> |
| <span data-ttu-id="b909d-113">DML_AXIS_DIRECTION_DECREASING</span><span class="sxs-lookup"><span data-stu-id="b909d-113">DML_AXIS_DIRECTION_DECREASING</span></span> | <span data-ttu-id="b909d-114">Especifica el orden decreciente (del índice alto al índice bajo).</span><span class="sxs-lookup"><span data-stu-id="b909d-114">Specifies decreasing order (from the high index to the low index).</span></span> |


## <a name="requirements"></a><span data-ttu-id="b909d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b909d-115">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b909d-116">**Header**</span><span class="sxs-lookup"><span data-stu-id="b909d-116">**Header**</span></span> | <span data-ttu-id="b909d-117">directml. h</span><span class="sxs-lookup"><span data-stu-id="b909d-117">directml.h</span></span> |