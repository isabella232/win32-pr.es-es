---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Redondea cada elemento de *InputTensor* a un valor entero, colocando el resultado en el elemento correspondiente de *OutputTensor.*
helpviewer_keywords:
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure
- direct3d12.dml_element_wise_round_operator_desc
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
ms.openlocfilehash: cb9414d0c3e628fa95784480c7402b242d12095b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803048"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a><span data-ttu-id="24b09-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="24b09-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="24b09-104">Redondea cada elemento de *InputTensor* a un valor entero, colocando el resultado en el elemento correspondiente de *OutputTensor.*</span><span class="sxs-lookup"><span data-stu-id="24b09-104">Rounds each element of *InputTensor* to an integer value, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="24b09-105">Este operador admite la ejecución en contexto, lo que significa que *OutputTensor* puede usar el alias *InputTensor* durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="24b09-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24b09-106">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="24b09-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="24b09-107">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="24b09-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="24b09-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24b09-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a><span data-ttu-id="24b09-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="24b09-109">Members</span></span>

`InputTensor`

<span data-ttu-id="24b09-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="24b09-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="24b09-111">Tensor de entrada del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="24b09-111">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="24b09-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="24b09-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="24b09-113">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="24b09-113">The output tensor to write the results to.</span></span>


`RoundingMode`

<span data-ttu-id="24b09-114">Tipo: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span><span class="sxs-lookup"><span data-stu-id="24b09-114">Type: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span></span>

<span data-ttu-id="24b09-115">Un [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determinar la dirección hacia la que se redondea.</span><span class="sxs-lookup"><span data-stu-id="24b09-115">A [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determining the direction to round towards.</span></span>

* <span data-ttu-id="24b09-116">Si **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: los valores se redondea al entero más cercano, con valores a medio camino (por ejemplo, 0,5) redondeados hacia el entero par más cercano.</span><span class="sxs-lookup"><span data-stu-id="24b09-116">If **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded toward the nearest even integer.</span></span>
* <span data-ttu-id="24b09-117">Si **DML_ROUNDING_MODE_TOWARD_ZERO**: los valores se redondea hacia cero.</span><span class="sxs-lookup"><span data-stu-id="24b09-117">If **DML_ROUNDING_MODE_TOWARD_ZERO**: values are rounded toward zero.</span></span> <span data-ttu-id="24b09-118">Esto trunca eficazmente la parte fraccionera.</span><span class="sxs-lookup"><span data-stu-id="24b09-118">This effectively truncates the fractional part.</span></span>
* <span data-ttu-id="24b09-119">Si **DML_ROUNDING_MODE_TOWARD_INFINITY**: los valores se redondean al entero más cercano, con valores a medio camino (por ejemplo, 0,5) redondeados lejos de cero (hacia infinito positivo o negativo, según el signo del valor).</span><span class="sxs-lookup"><span data-stu-id="24b09-119">If **DML_ROUNDING_MODE_TOWARD_INFINITY**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded away from zero (toward positive or negative infinity, depending on the sign of the value).</span></span>

## <a name="availability"></a><span data-ttu-id="24b09-120">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="24b09-120">Availability</span></span>
<span data-ttu-id="24b09-121">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="24b09-121">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="24b09-122">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="24b09-122">Tensor constraints</span></span>
<span data-ttu-id="24b09-123">*InputTensor* y *OutputTensor* deben tener los mismos *datatype,* *dimensioncount* y *tamaños.*</span><span class="sxs-lookup"><span data-stu-id="24b09-123">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="24b09-124">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="24b09-124">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="24b09-125">DML_FEATURE_LEVEL_3_0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="24b09-125">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="24b09-126">Tensor</span><span class="sxs-lookup"><span data-stu-id="24b09-126">Tensor</span></span> | <span data-ttu-id="24b09-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="24b09-127">Kind</span></span> | <span data-ttu-id="24b09-128">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="24b09-128">Supported dimension counts</span></span> | <span data-ttu-id="24b09-129">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="24b09-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="24b09-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="24b09-130">InputTensor</span></span> | <span data-ttu-id="24b09-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="24b09-131">Input</span></span> | <span data-ttu-id="24b09-132">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="24b09-132">1 to 8</span></span> | <span data-ttu-id="24b09-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="24b09-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="24b09-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="24b09-134">OutputTensor</span></span> | <span data-ttu-id="24b09-135">Resultados</span><span class="sxs-lookup"><span data-stu-id="24b09-135">Output</span></span> | <span data-ttu-id="24b09-136">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="24b09-136">1 to 8</span></span> | <span data-ttu-id="24b09-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="24b09-137">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="24b09-138">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="24b09-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="24b09-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="24b09-139">Tensor</span></span> | <span data-ttu-id="24b09-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="24b09-140">Kind</span></span> | <span data-ttu-id="24b09-141">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="24b09-141">Supported dimension counts</span></span> | <span data-ttu-id="24b09-142">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="24b09-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="24b09-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="24b09-143">InputTensor</span></span> | <span data-ttu-id="24b09-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="24b09-144">Input</span></span> | <span data-ttu-id="24b09-145">4</span><span class="sxs-lookup"><span data-stu-id="24b09-145">4</span></span> | <span data-ttu-id="24b09-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="24b09-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="24b09-147">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="24b09-147">OutputTensor</span></span> | <span data-ttu-id="24b09-148">Resultados</span><span class="sxs-lookup"><span data-stu-id="24b09-148">Output</span></span> | <span data-ttu-id="24b09-149">4</span><span class="sxs-lookup"><span data-stu-id="24b09-149">4</span></span> | <span data-ttu-id="24b09-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="24b09-150">FLOAT32, FLOAT16</span></span> |



## <a name="requirements"></a><span data-ttu-id="24b09-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24b09-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="24b09-152">**Header**</span><span class="sxs-lookup"><span data-stu-id="24b09-152">**Header**</span></span> | <span data-ttu-id="24b09-153">directml.h</span><span class="sxs-lookup"><span data-stu-id="24b09-153">directml.h</span></span> |