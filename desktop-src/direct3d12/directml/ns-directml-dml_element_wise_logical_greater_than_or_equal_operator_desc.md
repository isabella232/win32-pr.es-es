---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
description: Realiza un  valor lógico mayor o igual que en cada par de elementos correspondientes de los tensores de entrada, colocando el resultado (1 para true, 0 para false) en el elemento correspondiente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC, DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
ms.openlocfilehash: 4c20580a67117e6a605dfb0bf6611aca5cfd9e56
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418075"
---
# <a name="dml_element_wise_logical_greater_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="b23be-103">DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="b23be-103">DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b23be-104">Realiza un  valor lógico mayor o igual que en cada par de elementos correspondientes de los tensores de entrada, colocando el resultado (1 para true, 0 para false) en el elemento correspondiente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="b23be-104">Performs a logical *greater than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >= b)
```

> [!IMPORTANT]
> <span data-ttu-id="b23be-105">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="b23be-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b23be-106">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="b23be-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b23be-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b23be-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="b23be-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b23be-108">Members</span></span>

`ATensor`

<span data-ttu-id="b23be-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b23be-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b23be-110">Tensor que contiene las entradas del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="b23be-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="b23be-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b23be-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b23be-112">Tensor que contiene las entradas del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="b23be-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="b23be-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b23be-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b23be-114">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="b23be-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="b23be-115">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="b23be-115">Availability</span></span>
<span data-ttu-id="b23be-116">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="b23be-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b23be-117">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="b23be-117">Tensor constraints</span></span>
* <span data-ttu-id="b23be-118">*ATensor* y *BTensor* deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="b23be-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="b23be-119">*ATensor,* *BTensor* y *OutputTensor* deben tener los mismos *dimensioncount* y *sizes.*</span><span class="sxs-lookup"><span data-stu-id="b23be-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b23be-120">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="b23be-120">Tensor support</span></span>
| <span data-ttu-id="b23be-121">Tensor</span><span class="sxs-lookup"><span data-stu-id="b23be-121">Tensor</span></span> | <span data-ttu-id="b23be-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="b23be-122">Kind</span></span> | <span data-ttu-id="b23be-123">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="b23be-123">Supported dimension counts</span></span> | <span data-ttu-id="b23be-124">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="b23be-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b23be-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="b23be-125">ATensor</span></span> | <span data-ttu-id="b23be-126">Entrada</span><span class="sxs-lookup"><span data-stu-id="b23be-126">Input</span></span> | <span data-ttu-id="b23be-127">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="b23be-127">1 to 8</span></span> | <span data-ttu-id="b23be-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b23be-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b23be-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="b23be-129">BTensor</span></span> | <span data-ttu-id="b23be-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="b23be-130">Input</span></span> | <span data-ttu-id="b23be-131">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="b23be-131">1 to 8</span></span> | <span data-ttu-id="b23be-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b23be-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b23be-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b23be-133">OutputTensor</span></span> | <span data-ttu-id="b23be-134">Resultados</span><span class="sxs-lookup"><span data-stu-id="b23be-134">Output</span></span> | <span data-ttu-id="b23be-135">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="b23be-135">1 to 8</span></span> | <span data-ttu-id="b23be-136">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="b23be-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="b23be-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b23be-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b23be-138">**Header**</span><span class="sxs-lookup"><span data-stu-id="b23be-138">**Header**</span></span> | <span data-ttu-id="b23be-139">directml.h</span><span class="sxs-lookup"><span data-stu-id="b23be-139">directml.h</span></span> |