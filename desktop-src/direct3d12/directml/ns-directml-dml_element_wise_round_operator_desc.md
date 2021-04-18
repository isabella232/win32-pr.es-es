---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Redondea cada elemento de *InputTensor* a un valor entero, colocando el resultado en el elemento correspondiente de *OutputTensor*.
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
ms.openlocfilehash: f0964ae133c61b3a596b644630d363f902635585
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721207"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a><span data-ttu-id="c751a-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="c751a-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="c751a-104">Redondea cada elemento de *InputTensor* a un valor entero, colocando el resultado en el elemento correspondiente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="c751a-104">Rounds each element of *InputTensor* to an integer value, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="c751a-105">Este operador es compatible con la ejecución en contexto, lo que significa que *OutputTensor* puede asignar un alias a *InputTensor* durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="c751a-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c751a-106">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="c751a-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="c751a-107">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="c751a-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c751a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c751a-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a><span data-ttu-id="c751a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c751a-109">Members</span></span>

`InputTensor`

<span data-ttu-id="c751a-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c751a-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c751a-111">Tensores de entrada del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="c751a-111">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="c751a-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c751a-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c751a-113">Tensores de salida en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="c751a-113">The output tensor to write the results to.</span></span>


`RoundingMode`

<span data-ttu-id="c751a-114">Tipo: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span><span class="sxs-lookup"><span data-stu-id="c751a-114">Type: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span></span>

<span data-ttu-id="c751a-115">[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) que determina la dirección a la que se va a redondear.</span><span class="sxs-lookup"><span data-stu-id="c751a-115">A [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determining the direction to round towards.</span></span>

* <span data-ttu-id="c751a-116">Si **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: los valores se redondean al entero más cercano, con la mitad de los valores (por ejemplo, 0,5) que se redondean hacia el entero par más cercano.</span><span class="sxs-lookup"><span data-stu-id="c751a-116">If **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded toward the nearest even integer.</span></span>
* <span data-ttu-id="c751a-117">Si **DML_ROUNDING_MODE_TOWARD_ZERO**: los valores se redondean hacia cero.</span><span class="sxs-lookup"><span data-stu-id="c751a-117">If **DML_ROUNDING_MODE_TOWARD_ZERO**: values are rounded toward zero.</span></span> <span data-ttu-id="c751a-118">De este modo, se trunca la parte fraccionaria.</span><span class="sxs-lookup"><span data-stu-id="c751a-118">This effectively truncates the fractional part.</span></span>
* <span data-ttu-id="c751a-119">Si **DML_ROUNDING_MODE_TOWARD_INFINITY**: los valores se redondean al entero más cercano, con la mitad de los valores (por ejemplo, 0,5) que se redondean alejándose de cero (hasta el infinito positivo o negativo, dependiendo del signo del valor).</span><span class="sxs-lookup"><span data-stu-id="c751a-119">If **DML_ROUNDING_MODE_TOWARD_INFINITY**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded away from zero (toward positive or negative infinity, depending on the sign of the value).</span></span>

## <a name="availability"></a><span data-ttu-id="c751a-120">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="c751a-120">Availability</span></span>
<span data-ttu-id="c751a-121">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="c751a-121">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="c751a-122">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="c751a-122">Tensor constraints</span></span>
<span data-ttu-id="c751a-123">*InputTensor* y *OutputTensor* deben tener el mismo *tipo de DataType*, *DimensionCount* y *tamaños*.</span><span class="sxs-lookup"><span data-stu-id="c751a-123">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c751a-124">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="c751a-124">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="c751a-125">DML_FEATURE_LEVEL_3_0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="c751a-125">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="c751a-126">Tensores</span><span class="sxs-lookup"><span data-stu-id="c751a-126">Tensor</span></span> | <span data-ttu-id="c751a-127">Clase</span><span class="sxs-lookup"><span data-stu-id="c751a-127">Kind</span></span> | <span data-ttu-id="c751a-128">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="c751a-128">Supported dimension counts</span></span> | <span data-ttu-id="c751a-129">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="c751a-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c751a-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="c751a-130">InputTensor</span></span> | <span data-ttu-id="c751a-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="c751a-131">Input</span></span> | <span data-ttu-id="c751a-132">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="c751a-132">1 to 8</span></span> | <span data-ttu-id="c751a-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c751a-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="c751a-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c751a-134">OutputTensor</span></span> | <span data-ttu-id="c751a-135">Output</span><span class="sxs-lookup"><span data-stu-id="c751a-135">Output</span></span> | <span data-ttu-id="c751a-136">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="c751a-136">1 to 8</span></span> | <span data-ttu-id="c751a-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c751a-137">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="c751a-138">DML_FEATURE_LEVEL_2_1 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="c751a-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="c751a-139">Tensores</span><span class="sxs-lookup"><span data-stu-id="c751a-139">Tensor</span></span> | <span data-ttu-id="c751a-140">Clase</span><span class="sxs-lookup"><span data-stu-id="c751a-140">Kind</span></span> | <span data-ttu-id="c751a-141">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="c751a-141">Supported dimension counts</span></span> | <span data-ttu-id="c751a-142">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="c751a-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c751a-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="c751a-143">InputTensor</span></span> | <span data-ttu-id="c751a-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="c751a-144">Input</span></span> | <span data-ttu-id="c751a-145">4</span><span class="sxs-lookup"><span data-stu-id="c751a-145">4</span></span> | <span data-ttu-id="c751a-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c751a-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="c751a-147">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c751a-147">OutputTensor</span></span> | <span data-ttu-id="c751a-148">Output</span><span class="sxs-lookup"><span data-stu-id="c751a-148">Output</span></span> | <span data-ttu-id="c751a-149">4</span><span class="sxs-lookup"><span data-stu-id="c751a-149">4</span></span> | <span data-ttu-id="c751a-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="c751a-150">FLOAT32, FLOAT16</span></span> |



## <a name="requirements"></a><span data-ttu-id="c751a-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c751a-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c751a-152">**Header**</span><span class="sxs-lookup"><span data-stu-id="c751a-152">**Header**</span></span> | <span data-ttu-id="c751a-153">directml. h</span><span class="sxs-lookup"><span data-stu-id="c751a-153">directml.h</span></span> |