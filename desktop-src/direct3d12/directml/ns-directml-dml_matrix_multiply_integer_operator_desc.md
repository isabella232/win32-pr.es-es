---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Realiza una función de multiplicación de matrices en datos enteros.
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f6ecccf49b0d7123e6f41321c7ba1bf8e8d4ad87
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721245"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="c3a17-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="c3a17-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="c3a17-104">Realiza una función de multiplicación de matrices en datos enteros.</span><span class="sxs-lookup"><span data-stu-id="c3a17-104">Performs a matrix multiplication function on integer data.</span></span>

<span data-ttu-id="c3a17-105">Este operador requiere que la matriz multiplique los idiomas de entrada a 4D, cuyo formato es `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="c3a17-105">This operator requires the matrix multiply input tensors to be 4D, which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="c3a17-106">El operador de multiplicación de la matriz realizará el BatchCount \* ChannelCount número de multiplicaciones de matriz independiente.</span><span class="sxs-lookup"><span data-stu-id="c3a17-106">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span>

<span data-ttu-id="c3a17-107">Por ejemplo, si *ATensor* tiene  los tamaños `{ BatchCount, ChannelCount, M, K }` , y *BTensor* tiene *tamaños* `{ BatchCount, ChannelCount, K, N }` , y *OutputTensor* tiene *tamaños* `{ BatchCount, ChannelCount, M, N }` , el operador de multiplicación de la matriz realizará la multiplicación de las dimensiones de la matriz independiente BatchCount \* ChannelCount {m, K} x {k, n} = {m, n}.</span><span class="sxs-lookup"><span data-stu-id="c3a17-107">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3a17-108">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="c3a17-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="c3a17-109">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="c3a17-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a17-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3a17-110">Syntax</span></span>
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="c3a17-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c3a17-111">Members</span></span>

`ATensor`

<span data-ttu-id="c3a17-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c3a17-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c3a17-113">Tensores que contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="c3a17-113">A tensor containing the A data.</span></span> <span data-ttu-id="c3a17-114">Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="c3a17-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AZeroPointTensor`

<span data-ttu-id="c3a17-115">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c3a17-115">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c3a17-116">Un tensores opcional que contiene los datos de cero puntos de ATensor.</span><span class="sxs-lookup"><span data-stu-id="c3a17-116">An optional tensor containing the ATensor zero point data.</span></span> <span data-ttu-id="c3a17-117">Las dimensiones esperadas de `AZeroPointTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores o `{ 1, 1, M, 1 }` si se requiere la cuantificación por fila.</span><span class="sxs-lookup"><span data-stu-id="c3a17-117">The expected dimensions of the `AZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per-row quantization is required.</span></span> <span data-ttu-id="c3a17-118">Estos valores de punto cero se usan para descuantificar los valores de *ATensor* .</span><span class="sxs-lookup"><span data-stu-id="c3a17-118">These zero point values are used for dequantizing the *ATensor* values.</span></span>


`BTensor`

<span data-ttu-id="c3a17-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c3a17-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c3a17-120">Tensores que contiene los datos de B.</span><span class="sxs-lookup"><span data-stu-id="c3a17-120">A tensor containing the B data.</span></span> <span data-ttu-id="c3a17-121">Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="c3a17-121">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BZeroPointTensor`

<span data-ttu-id="c3a17-122">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c3a17-122">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c3a17-123">Un tensores opcional que contiene los datos de cero puntos de *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="c3a17-123">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="c3a17-124">Las dimensiones esperadas de `BZeroPointTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores, o `{ 1, 1, 1, N }` si se requiere la cuantificación por columna.</span><span class="sxs-lookup"><span data-stu-id="c3a17-124">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="c3a17-125">Estos valores de punto cero se usan para descuantificar los valores de BTensor.</span><span class="sxs-lookup"><span data-stu-id="c3a17-125">These zero point values are used for dequantizing the BTensor values.</span></span>


`OutputTensor`

<span data-ttu-id="c3a17-126">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c3a17-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c3a17-127">Tensores con el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="c3a17-127">A tensor with which to write the results to.</span></span> <span data-ttu-id="c3a17-128">Las dimensiones de este tensores son `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="c3a17-128">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="c3a17-129">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="c3a17-129">Availability</span></span>
<span data-ttu-id="c3a17-130">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="c3a17-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="c3a17-131">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="c3a17-131">Tensor constraints</span></span>
* <span data-ttu-id="c3a17-132">*ATensor* y `AZeroPointTensor` deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="c3a17-132">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="c3a17-133">*BTensor* y `BZeroPointTensor` deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="c3a17-133">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c3a17-134">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="c3a17-134">Tensor support</span></span>
| <span data-ttu-id="c3a17-135">Tensores</span><span class="sxs-lookup"><span data-stu-id="c3a17-135">Tensor</span></span> | <span data-ttu-id="c3a17-136">Clase</span><span class="sxs-lookup"><span data-stu-id="c3a17-136">Kind</span></span> | <span data-ttu-id="c3a17-137">Dimensions</span><span class="sxs-lookup"><span data-stu-id="c3a17-137">Dimensions</span></span> | <span data-ttu-id="c3a17-138">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="c3a17-138">Supported dimension counts</span></span> | <span data-ttu-id="c3a17-139">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="c3a17-139">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="c3a17-140">ATensor</span><span class="sxs-lookup"><span data-stu-id="c3a17-140">ATensor</span></span> | <span data-ttu-id="c3a17-141">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3a17-141">Input</span></span> | <span data-ttu-id="c3a17-142">{BatchCount, ChannelCount, M, K}</span><span class="sxs-lookup"><span data-stu-id="c3a17-142">{ BatchCount, ChannelCount, M, K }</span></span> | <span data-ttu-id="c3a17-143">4</span><span class="sxs-lookup"><span data-stu-id="c3a17-143">4</span></span> | <span data-ttu-id="c3a17-144">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="c3a17-144">INT8, UINT8</span></span> |
| <span data-ttu-id="c3a17-145">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="c3a17-145">AZeroPointTensor</span></span> | <span data-ttu-id="c3a17-146">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="c3a17-146">Optional input</span></span> | <span data-ttu-id="c3a17-147">{1, 1, AZeroPointCount, 1}</span><span class="sxs-lookup"><span data-stu-id="c3a17-147">{ 1, 1, AZeroPointCount, 1 }</span></span> | <span data-ttu-id="c3a17-148">4</span><span class="sxs-lookup"><span data-stu-id="c3a17-148">4</span></span> | <span data-ttu-id="c3a17-149">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="c3a17-149">INT8, UINT8</span></span> |
| <span data-ttu-id="c3a17-150">BTensor</span><span class="sxs-lookup"><span data-stu-id="c3a17-150">BTensor</span></span> | <span data-ttu-id="c3a17-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="c3a17-151">Input</span></span> | <span data-ttu-id="c3a17-152">{BatchCount, ChannelCount, K, N}</span><span class="sxs-lookup"><span data-stu-id="c3a17-152">{ BatchCount, ChannelCount, K, N }</span></span> | <span data-ttu-id="c3a17-153">4</span><span class="sxs-lookup"><span data-stu-id="c3a17-153">4</span></span> | <span data-ttu-id="c3a17-154">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="c3a17-154">INT8, UINT8</span></span> |
| <span data-ttu-id="c3a17-155">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="c3a17-155">BZeroPointTensor</span></span> | <span data-ttu-id="c3a17-156">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="c3a17-156">Optional input</span></span> | <span data-ttu-id="c3a17-157">{1, 1, 1, BZeroPointCount}</span><span class="sxs-lookup"><span data-stu-id="c3a17-157">{ 1, 1, 1, BZeroPointCount }</span></span> | <span data-ttu-id="c3a17-158">4</span><span class="sxs-lookup"><span data-stu-id="c3a17-158">4</span></span> | <span data-ttu-id="c3a17-159">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="c3a17-159">INT8, UINT8</span></span> |
| <span data-ttu-id="c3a17-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c3a17-160">OutputTensor</span></span> | <span data-ttu-id="c3a17-161">Output</span><span class="sxs-lookup"><span data-stu-id="c3a17-161">Output</span></span> | <span data-ttu-id="c3a17-162">{BatchCount, ChannelCount, M, N}</span><span class="sxs-lookup"><span data-stu-id="c3a17-162">{ BatchCount, ChannelCount, M, N }</span></span> | <span data-ttu-id="c3a17-163">4</span><span class="sxs-lookup"><span data-stu-id="c3a17-163">4</span></span> | <span data-ttu-id="c3a17-164">INT32</span><span class="sxs-lookup"><span data-stu-id="c3a17-164">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="c3a17-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3a17-165">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c3a17-166">**Header**</span><span class="sxs-lookup"><span data-stu-id="c3a17-166">**Header**</span></span> | <span data-ttu-id="c3a17-167">directml. h</span><span class="sxs-lookup"><span data-stu-id="c3a17-167">directml.h</span></span> |