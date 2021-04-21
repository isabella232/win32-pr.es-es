---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Realiza una función de multiplicación de matriz en datos enteros.
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
ms.openlocfilehash: f498e84208da451b5d25ffef90219c0037ce86fb
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802835"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="4d7f0-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="4d7f0-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="4d7f0-104">Realiza una función de multiplicación de matriz en datos enteros.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-104">Performs a matrix multiplication function on integer data.</span></span>

<span data-ttu-id="4d7f0-105">Este operador requiere que la matriz multiplique los tensores de entrada sea 4D, que tienen el formato `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="4d7f0-105">This operator requires the matrix multiply input tensors to be 4D, which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="4d7f0-106">El operador de multiplicación de matriz realizará batchcount \* channelcount número de multiplicaciones de matrices independientes.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-106">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span>

<span data-ttu-id="4d7f0-107">Por ejemplo, si *ATensor* tiene tamaños de y  BTensor tiene tamaños de y OutputTensor tiene tamaños de , el operador de multiplicación de matriz realizará multiplicaciones de matrices independientes de BatchCount \* ChannelCount de dimensiones `{ BatchCount, ChannelCount, M, K }`   `{ BatchCount, ChannelCount, K, N }`   `{ BatchCount, ChannelCount, M, N }` {M,K} x {K,N} = {M,N}.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-107">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d7f0-108">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="4d7f0-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="4d7f0-109">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="4d7f0-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7f0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d7f0-110">Syntax</span></span>
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="4d7f0-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d7f0-111">Members</span></span>

`ATensor`

<span data-ttu-id="4d7f0-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4d7f0-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4d7f0-113">Tensor que contiene los datos A.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-113">A tensor containing the A data.</span></span> <span data-ttu-id="4d7f0-114">Las dimensiones de este tensor deben ser `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="4d7f0-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AZeroPointTensor`

<span data-ttu-id="4d7f0-115">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4d7f0-115">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4d7f0-116">Tensor opcional que contiene los datos de punto cero de ATensor.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-116">An optional tensor containing the ATensor zero point data.</span></span> <span data-ttu-id="4d7f0-117">Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `AZeroPointTensor` `{ 1, 1, 1, 1 }` una `{ 1, 1, M, 1 }` cuantificación por fila.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-117">The expected dimensions of the `AZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per-row quantization is required.</span></span> <span data-ttu-id="4d7f0-118">Estos valores de punto cero se usan para descuantizar los *valores de ATensor.*</span><span class="sxs-lookup"><span data-stu-id="4d7f0-118">These zero point values are used for dequantizing the *ATensor* values.</span></span>


`BTensor`

<span data-ttu-id="4d7f0-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4d7f0-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4d7f0-120">Tensor que contiene los datos B.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-120">A tensor containing the B data.</span></span> <span data-ttu-id="4d7f0-121">Las dimensiones de este tensor deben ser `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="4d7f0-121">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BZeroPointTensor`

<span data-ttu-id="4d7f0-122">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4d7f0-122">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4d7f0-123">Tensor opcional que contiene los datos de punto cero de *BTensor.*</span><span class="sxs-lookup"><span data-stu-id="4d7f0-123">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="4d7f0-124">Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `BZeroPointTensor` `{ 1, 1, 1, 1 }` una `{ 1, 1, 1, N }` cuantificación por columna.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-124">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="4d7f0-125">Estos valores de punto cero se usan para descuantizar los valores de BTensor.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-125">These zero point values are used for dequantizing the BTensor values.</span></span>


`OutputTensor`

<span data-ttu-id="4d7f0-126">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4d7f0-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4d7f0-127">Tensor con el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-127">A tensor with which to write the results to.</span></span> <span data-ttu-id="4d7f0-128">Las dimensiones de este tensor son `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="4d7f0-128">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="4d7f0-129">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="4d7f0-129">Availability</span></span>
<span data-ttu-id="4d7f0-130">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="4d7f0-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4d7f0-131">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="4d7f0-131">Tensor constraints</span></span>
* <span data-ttu-id="4d7f0-132">*ATensor* y `AZeroPointTensor` deben tener el mismo *datatype*.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-132">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="4d7f0-133">*BTensor* y `BZeroPointTensor` deben tener el mismo *datatype*.</span><span class="sxs-lookup"><span data-stu-id="4d7f0-133">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4d7f0-134">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="4d7f0-134">Tensor support</span></span>
| <span data-ttu-id="4d7f0-135">Tensor</span><span class="sxs-lookup"><span data-stu-id="4d7f0-135">Tensor</span></span> | <span data-ttu-id="4d7f0-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d7f0-136">Kind</span></span> | <span data-ttu-id="4d7f0-137">Dimensions</span><span class="sxs-lookup"><span data-stu-id="4d7f0-137">Dimensions</span></span> | <span data-ttu-id="4d7f0-138">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="4d7f0-138">Supported dimension counts</span></span> | <span data-ttu-id="4d7f0-139">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="4d7f0-139">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="4d7f0-140">ATensor</span><span class="sxs-lookup"><span data-stu-id="4d7f0-140">ATensor</span></span> | <span data-ttu-id="4d7f0-141">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d7f0-141">Input</span></span> | <span data-ttu-id="4d7f0-142">{ BatchCount, ChannelCount, M, K }</span><span class="sxs-lookup"><span data-stu-id="4d7f0-142">{ BatchCount, ChannelCount, M, K }</span></span> | <span data-ttu-id="4d7f0-143">4</span><span class="sxs-lookup"><span data-stu-id="4d7f0-143">4</span></span> | <span data-ttu-id="4d7f0-144">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="4d7f0-144">INT8, UINT8</span></span> |
| <span data-ttu-id="4d7f0-145">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="4d7f0-145">AZeroPointTensor</span></span> | <span data-ttu-id="4d7f0-146">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="4d7f0-146">Optional input</span></span> | <span data-ttu-id="4d7f0-147">{ 1, 1, AZeroPointCount, 1 }</span><span class="sxs-lookup"><span data-stu-id="4d7f0-147">{ 1, 1, AZeroPointCount, 1 }</span></span> | <span data-ttu-id="4d7f0-148">4</span><span class="sxs-lookup"><span data-stu-id="4d7f0-148">4</span></span> | <span data-ttu-id="4d7f0-149">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="4d7f0-149">INT8, UINT8</span></span> |
| <span data-ttu-id="4d7f0-150">BTensor</span><span class="sxs-lookup"><span data-stu-id="4d7f0-150">BTensor</span></span> | <span data-ttu-id="4d7f0-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d7f0-151">Input</span></span> | <span data-ttu-id="4d7f0-152">{ BatchCount, ChannelCount, K, N }</span><span class="sxs-lookup"><span data-stu-id="4d7f0-152">{ BatchCount, ChannelCount, K, N }</span></span> | <span data-ttu-id="4d7f0-153">4</span><span class="sxs-lookup"><span data-stu-id="4d7f0-153">4</span></span> | <span data-ttu-id="4d7f0-154">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="4d7f0-154">INT8, UINT8</span></span> |
| <span data-ttu-id="4d7f0-155">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="4d7f0-155">BZeroPointTensor</span></span> | <span data-ttu-id="4d7f0-156">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="4d7f0-156">Optional input</span></span> | <span data-ttu-id="4d7f0-157">{ 1, 1, 1, BZeroPointCount }</span><span class="sxs-lookup"><span data-stu-id="4d7f0-157">{ 1, 1, 1, BZeroPointCount }</span></span> | <span data-ttu-id="4d7f0-158">4</span><span class="sxs-lookup"><span data-stu-id="4d7f0-158">4</span></span> | <span data-ttu-id="4d7f0-159">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="4d7f0-159">INT8, UINT8</span></span> |
| <span data-ttu-id="4d7f0-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="4d7f0-160">OutputTensor</span></span> | <span data-ttu-id="4d7f0-161">Resultados</span><span class="sxs-lookup"><span data-stu-id="4d7f0-161">Output</span></span> | <span data-ttu-id="4d7f0-162">{ BatchCount, ChannelCount, M, N }</span><span class="sxs-lookup"><span data-stu-id="4d7f0-162">{ BatchCount, ChannelCount, M, N }</span></span> | <span data-ttu-id="4d7f0-163">4</span><span class="sxs-lookup"><span data-stu-id="4d7f0-163">4</span></span> | <span data-ttu-id="4d7f0-164">INT32</span><span class="sxs-lookup"><span data-stu-id="4d7f0-164">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="4d7f0-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d7f0-165">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4d7f0-166">**Header**</span><span class="sxs-lookup"><span data-stu-id="4d7f0-166">**Header**</span></span> | <span data-ttu-id="4d7f0-167">directml.h</span><span class="sxs-lookup"><span data-stu-id="4d7f0-167">directml.h</span></span> |