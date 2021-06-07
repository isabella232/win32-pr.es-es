---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
description: Calcula el módulo, con los mismos resultados que el módulo de Python, para cada par de elementos correspondientes de los tensores de entrada, colocando el resultado en el elemento correspondiente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_floor_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
ms.openlocfilehash: 8c70bd4649a57270807ac408802fe07edd36d98e
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418083"
---
# <a name="dml_element_wise_modulus_floor_operator_desc-structure-directmlh"></a><span data-ttu-id="e4dfe-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="e4dfe-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e4dfe-104">Calcula el módulo, con los mismos resultados que el módulo de Python, para cada par de elementos correspondientes de los tensores de entrada, colocando el resultado en el elemento correspondiente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="e4dfe-104">Computes the modulus, with the same results as the Python modulus, for each pair of corresponding elements from the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="e4dfe-105">Dado que el cociente se redondea hacia -inf, el resultado tendrá el mismo signo que el divisor.</span><span class="sxs-lookup"><span data-stu-id="e4dfe-105">Because the quotient is rounded towards -inf, the result will have the same sign as the divisor.</span></span>

```
f(a, b) = a - (b * floor(a / b))
```

<span data-ttu-id="e4dfe-106">Este operador admite la ejecución en contexto, lo que significa que *OutputTensor* puede crear un alias de uno de los tensores de entrada durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="e4dfe-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4dfe-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="e4dfe-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e4dfe-108">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="e4dfe-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e4dfe-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4dfe-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="e4dfe-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="e4dfe-110">Members</span></span>

`ATensor`

<span data-ttu-id="e4dfe-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e4dfe-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e4dfe-112">Tensor que contiene las entradas del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="e4dfe-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="e4dfe-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e4dfe-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e4dfe-114">Tensor que contiene las entradas del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="e4dfe-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="e4dfe-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e4dfe-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e4dfe-116">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="e4dfe-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="e4dfe-117">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="e4dfe-117">Availability</span></span>
<span data-ttu-id="e4dfe-118">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="e4dfe-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e4dfe-119">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="e4dfe-119">Tensor constraints</span></span>
<span data-ttu-id="e4dfe-120">*ATensor,* *BTensor* y *OutputTensor* deben tener los mismos *tamaños DataType,* *DimensionCount* y *.*</span><span class="sxs-lookup"><span data-stu-id="e4dfe-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e4dfe-121">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="e4dfe-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="e4dfe-122">DML_FEATURE_LEVEL_3_0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="e4dfe-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="e4dfe-123">Tensor</span><span class="sxs-lookup"><span data-stu-id="e4dfe-123">Tensor</span></span> | <span data-ttu-id="e4dfe-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4dfe-124">Kind</span></span> | <span data-ttu-id="e4dfe-125">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="e4dfe-125">Supported dimension counts</span></span> | <span data-ttu-id="e4dfe-126">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="e4dfe-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e4dfe-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="e4dfe-127">ATensor</span></span> | <span data-ttu-id="e4dfe-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="e4dfe-128">Input</span></span> | <span data-ttu-id="e4dfe-129">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e4dfe-129">1 to 8</span></span> | <span data-ttu-id="e4dfe-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e4dfe-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e4dfe-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="e4dfe-131">BTensor</span></span> | <span data-ttu-id="e4dfe-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="e4dfe-132">Input</span></span> | <span data-ttu-id="e4dfe-133">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e4dfe-133">1 to 8</span></span> | <span data-ttu-id="e4dfe-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e4dfe-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e4dfe-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e4dfe-135">OutputTensor</span></span> | <span data-ttu-id="e4dfe-136">Resultados</span><span class="sxs-lookup"><span data-stu-id="e4dfe-136">Output</span></span> | <span data-ttu-id="e4dfe-137">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="e4dfe-137">1 to 8</span></span> | <span data-ttu-id="e4dfe-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e4dfe-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="e4dfe-139">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="e4dfe-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="e4dfe-140">Tensor</span><span class="sxs-lookup"><span data-stu-id="e4dfe-140">Tensor</span></span> | <span data-ttu-id="e4dfe-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4dfe-141">Kind</span></span> | <span data-ttu-id="e4dfe-142">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="e4dfe-142">Supported dimension counts</span></span> | <span data-ttu-id="e4dfe-143">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="e4dfe-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e4dfe-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="e4dfe-144">ATensor</span></span> | <span data-ttu-id="e4dfe-145">Entrada</span><span class="sxs-lookup"><span data-stu-id="e4dfe-145">Input</span></span> | <span data-ttu-id="e4dfe-146">4</span><span class="sxs-lookup"><span data-stu-id="e4dfe-146">4</span></span> | <span data-ttu-id="e4dfe-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e4dfe-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e4dfe-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="e4dfe-148">BTensor</span></span> | <span data-ttu-id="e4dfe-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="e4dfe-149">Input</span></span> | <span data-ttu-id="e4dfe-150">4</span><span class="sxs-lookup"><span data-stu-id="e4dfe-150">4</span></span> | <span data-ttu-id="e4dfe-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e4dfe-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e4dfe-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e4dfe-152">OutputTensor</span></span> | <span data-ttu-id="e4dfe-153">Resultados</span><span class="sxs-lookup"><span data-stu-id="e4dfe-153">Output</span></span> | <span data-ttu-id="e4dfe-154">4</span><span class="sxs-lookup"><span data-stu-id="e4dfe-154">4</span></span> | <span data-ttu-id="e4dfe-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e4dfe-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="e4dfe-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4dfe-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e4dfe-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="e4dfe-157">**Header**</span></span> | <span data-ttu-id="e4dfe-158">directml.h</span><span class="sxs-lookup"><span data-stu-id="e4dfe-158">directml.h</span></span> |