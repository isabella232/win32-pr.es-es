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
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803065"
---
# <a name="dml_element_wise_modulus_floor_operator_desc-structure-directmlh"></a><span data-ttu-id="87710-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="87710-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="87710-104">Calcula el módulo, con los mismos resultados que el módulo de Python, para cada par de elementos correspondientes de los tensores de entrada, colocando el resultado en el elemento correspondiente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="87710-104">Computes the modulus, with the same results as the Python modulus, for each pair of corresponding elements from the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="87710-105">Dado que el cociente se redondea hacia -inf, el resultado tendrá el mismo signo que el divisor.</span><span class="sxs-lookup"><span data-stu-id="87710-105">Because the quotient is rounded towards -inf, the result will have the same sign as the divisor.</span></span>

```
f(a, b) = a - (b * floor(a / b))
```

<span data-ttu-id="87710-106">Este operador admite la ejecución en contexto, lo que significa que *OutputTensor* puede crear un alias de uno de los tensores de entrada durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="87710-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87710-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="87710-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="87710-108">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="87710-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="87710-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87710-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="87710-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="87710-110">Members</span></span>

`ATensor`

<span data-ttu-id="87710-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="87710-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="87710-112">Tensor que contiene las entradas del lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="87710-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="87710-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="87710-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="87710-114">Tensor que contiene las entradas del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="87710-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="87710-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="87710-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="87710-116">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="87710-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="87710-117">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="87710-117">Availability</span></span>
<span data-ttu-id="87710-118">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="87710-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="87710-119">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="87710-119">Tensor constraints</span></span>
<span data-ttu-id="87710-120">*ATensor,* *BTensor* y *OutputTensor* deben tener los mismos *DataType,* *DimensionCount* y *Sizes.*</span><span class="sxs-lookup"><span data-stu-id="87710-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="87710-121">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="87710-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="87710-122">DML_FEATURE_LEVEL_3_0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="87710-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="87710-123">Tensor</span><span class="sxs-lookup"><span data-stu-id="87710-123">Tensor</span></span> | <span data-ttu-id="87710-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="87710-124">Kind</span></span> | <span data-ttu-id="87710-125">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="87710-125">Supported dimension counts</span></span> | <span data-ttu-id="87710-126">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="87710-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="87710-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="87710-127">ATensor</span></span> | <span data-ttu-id="87710-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="87710-128">Input</span></span> | <span data-ttu-id="87710-129">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="87710-129">1 to 8</span></span> | <span data-ttu-id="87710-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="87710-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="87710-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="87710-131">BTensor</span></span> | <span data-ttu-id="87710-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="87710-132">Input</span></span> | <span data-ttu-id="87710-133">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="87710-133">1 to 8</span></span> | <span data-ttu-id="87710-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="87710-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="87710-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="87710-135">OutputTensor</span></span> | <span data-ttu-id="87710-136">Resultados</span><span class="sxs-lookup"><span data-stu-id="87710-136">Output</span></span> | <span data-ttu-id="87710-137">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="87710-137">1 to 8</span></span> | <span data-ttu-id="87710-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="87710-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="87710-139">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="87710-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="87710-140">Tensor</span><span class="sxs-lookup"><span data-stu-id="87710-140">Tensor</span></span> | <span data-ttu-id="87710-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="87710-141">Kind</span></span> | <span data-ttu-id="87710-142">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="87710-142">Supported dimension counts</span></span> | <span data-ttu-id="87710-143">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="87710-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="87710-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="87710-144">ATensor</span></span> | <span data-ttu-id="87710-145">Entrada</span><span class="sxs-lookup"><span data-stu-id="87710-145">Input</span></span> | <span data-ttu-id="87710-146">4</span><span class="sxs-lookup"><span data-stu-id="87710-146">4</span></span> | <span data-ttu-id="87710-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="87710-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="87710-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="87710-148">BTensor</span></span> | <span data-ttu-id="87710-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="87710-149">Input</span></span> | <span data-ttu-id="87710-150">4</span><span class="sxs-lookup"><span data-stu-id="87710-150">4</span></span> | <span data-ttu-id="87710-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="87710-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="87710-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="87710-152">OutputTensor</span></span> | <span data-ttu-id="87710-153">Resultados</span><span class="sxs-lookup"><span data-stu-id="87710-153">Output</span></span> | <span data-ttu-id="87710-154">4</span><span class="sxs-lookup"><span data-stu-id="87710-154">4</span></span> | <span data-ttu-id="87710-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="87710-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="87710-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87710-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="87710-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="87710-157">**Header**</span></span> | <span data-ttu-id="87710-158">directml.h</span><span class="sxs-lookup"><span data-stu-id="87710-158">directml.h</span></span> |