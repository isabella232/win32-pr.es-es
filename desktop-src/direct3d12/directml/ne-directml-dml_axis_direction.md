---
UID: NE:directml.DML_AXIS_DIRECTION
title: DML_AXIS_DIRECTION
description: Define constantes que especifican la dirección de una operación a lo largo del eje dado para el operador (por ejemplo, suma, selección de los elementos superiores k y selección del elemento mínimo).
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
ms.openlocfilehash: e54d2abed3843ea9b2a22cb3c385f9edd1541ba5
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417958"
---
# <a name="dml_axis_direction-enumeration-directmlh"></a><span data-ttu-id="9bb71-103">DML_AXIS_DIRECTION enumeración (directml.h)</span><span class="sxs-lookup"><span data-stu-id="9bb71-103">DML_AXIS_DIRECTION enumeration (directml.h)</span></span>

<span data-ttu-id="9bb71-104">Define constantes que especifican la dirección de una operación a lo largo del eje dado para el operador (por ejemplo, suma, selección de los elementos superiores k y selección del elemento mínimo).</span><span class="sxs-lookup"><span data-stu-id="9bb71-104">Defines constants that specify the direction of an operation along the given axis for the operator (for example, summation, selecting the top-k elements, selecting the minimum element).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9bb71-105">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="9bb71-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="9bb71-106">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="9bb71-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9bb71-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9bb71-107">Syntax</span></span>
```cpp
typedef enum DML_AXIS_DIRECTION {
  DML_AXIS_DIRECTION_INCREASING,
  DML_AXIS_DIRECTION_DECREASING
} ;
```

## <a name="constants"></a><span data-ttu-id="9bb71-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="9bb71-108">Constants</span></span>

| <span data-ttu-id="9bb71-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="9bb71-109">Name</span></span> | <span data-ttu-id="9bb71-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bb71-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="9bb71-111">DML_AXIS_DIRECTION_INCREASING</span><span class="sxs-lookup"><span data-stu-id="9bb71-111">DML_AXIS_DIRECTION_INCREASING</span></span> | <span data-ttu-id="9bb71-112">Especifica el orden creciente (del índice bajo al índice alto).</span><span class="sxs-lookup"><span data-stu-id="9bb71-112">Specifies increasing order (from the low index to the high index).</span></span> |
| <span data-ttu-id="9bb71-113">DML_AXIS_DIRECTION_DECREASING</span><span class="sxs-lookup"><span data-stu-id="9bb71-113">DML_AXIS_DIRECTION_DECREASING</span></span> | <span data-ttu-id="9bb71-114">Especifica el orden decreciente (del índice alto al índice bajo).</span><span class="sxs-lookup"><span data-stu-id="9bb71-114">Specifies decreasing order (from the high index to the low index).</span></span> |


## <a name="requirements"></a><span data-ttu-id="9bb71-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bb71-115">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9bb71-116">**Header**</span><span class="sxs-lookup"><span data-stu-id="9bb71-116">**Header**</span></span> | <span data-ttu-id="9bb71-117">directml.h</span><span class="sxs-lookup"><span data-stu-id="9bb71-117">directml.h</span></span> |