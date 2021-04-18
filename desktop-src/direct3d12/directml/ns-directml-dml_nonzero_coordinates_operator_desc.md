---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Calcula las coordenadas de N dimensiones de todos los elementos distintos de cero de la tensores de entrada.
helpviewer_keywords:
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- DML_NONZERO_COORDINATES_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_NONZERO_COORDINATES_OPERATOR_DESC, DML_NONZERO_COORDINATES_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.openlocfilehash: a662ac3b341c07e512e11dcc15cbc9b11ec5f405
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721272"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a><span data-ttu-id="872e8-103">DML_NONZERO_COORDINATES_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="872e8-103">DML_NONZERO_COORDINATES_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="872e8-104">Calcula las coordenadas de N dimensiones de todos los elementos distintos de cero de la tensores de entrada.</span><span class="sxs-lookup"><span data-stu-id="872e8-104">Computes the N-dimensional coordinates of all non-zero elements of the input tensor.</span></span>

<span data-ttu-id="872e8-105">Este operador genera una matriz de valores de MxN, donde cada fila M contiene una coordenada de N dimensiones de un valor distinto de cero de la entrada.</span><span class="sxs-lookup"><span data-stu-id="872e8-105">This operator produces an MxN matrix of values, where each row M contains an N-dimensional coordinate of a non-zero value from the input.</span></span> <span data-ttu-id="872e8-106">Al usar entradas **FLOAT32** o **FLOAT16** , tanto 0 como positivos (0,0 f y-0.0 f) se tratan como cero para los fines de este operador.</span><span class="sxs-lookup"><span data-stu-id="872e8-106">When using **FLOAT32** or **FLOAT16** inputs, both negative and positive 0 (0.0f and -0.0f) are treated as zero for the purposes of this operator.</span></span>

<span data-ttu-id="872e8-107">El operador requiere que el valor de *OutputCoordinatesTensor* tenga un tamaño lo suficientemente grande como para dar cabida a un escenario en el peor de los casos, en el que cada elemento de la entrada es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="872e8-107">The operator requires that the *OutputCoordinatesTensor* has a size large enough to accommodate a worst-case scenario where every element of the input is non-zero.</span></span> <span data-ttu-id="872e8-108">Este operador devuelve el recuento de elementos distintos de cero a través de *OutputCountTensor*, que los llamadores pueden inspeccionar para determinar el número de coordenadas escritas en *OutputCoordinatesTensor*.</span><span class="sxs-lookup"><span data-stu-id="872e8-108">This operator returns the count of of non-zero elements via the *OutputCountTensor*, which callers can inspect to determine the number of coordinates written to the *OutputCoordinatesTensor*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="872e8-109">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="872e8-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="872e8-110">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="872e8-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="872e8-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="872e8-111">Syntax</span></span>

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a><span data-ttu-id="872e8-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="872e8-112">Members</span></span>

`InputTensor`

<span data-ttu-id="872e8-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="872e8-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="872e8-114">Una tensores de entrada.</span><span class="sxs-lookup"><span data-stu-id="872e8-114">An input tensor.</span></span>

`OutputCountTensor`

<span data-ttu-id="872e8-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="872e8-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="872e8-116">Tensores de salida que contiene el recuento de elementos distintos de cero en el tensores de entrada.</span><span class="sxs-lookup"><span data-stu-id="872e8-116">An output tensor that holds the count of non-zero elements in the input tensor.</span></span> <span data-ttu-id="872e8-117">Este tensores debe ser un escalar &mdash; , es decir, los tamaños de este tensores deben ser todos 1.</span><span class="sxs-lookup"><span data-stu-id="872e8-117">This tensor must be a scalar&mdash;that is, the Sizes of this tensor must all be 1.</span></span> <span data-ttu-id="872e8-118">El tipo de este tensores debe ser **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="872e8-118">The type of this tensor must be **UINT32**.</span></span>

`OutputCoordinatesTensor`

<span data-ttu-id="872e8-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="872e8-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="872e8-120">Tensores de salida que contiene las coordenadas de N dimensiones de los elementos de entrada que son distintos de cero.</span><span class="sxs-lookup"><span data-stu-id="872e8-120">An output tensor that holds the N-dimensional coordinates of the input elements which are non-zero.</span></span> 

<span data-ttu-id="872e8-121">Este tensores debe tener *tamaños* de `{1,1,M,N}` (si *DimensionCount* es 4) o `{1,1,1,M,N}` (si *DimensionCount* es 5), donde M es el número total de elementos de la *InputTensor* y N es mayor o igual que la *clasificación efectiva* de *InputTensor*, hasta el *DimensionCount* de la entrada.</span><span class="sxs-lookup"><span data-stu-id="872e8-121">This tensor must have *Sizes* of `{1,1,M,N}` (if *DimensionCount* is 4), or `{1,1,1,M,N}` (if *DimensionCount* is 5), where M is the total number of elements in the *InputTensor*, and N is greater or equal to the *effective rank* of *InputTensor*, up to the *DimensionCount* of the input.</span></span>

<span data-ttu-id="872e8-122">El rango efectivo de un tensores viene determinado por el *DimensionCount* de ese tensores excluyendo las dimensiones iniciales del tamaño 1.</span><span class="sxs-lookup"><span data-stu-id="872e8-122">The effective rank of a tensor is determined by the *DimensionCount* of that tensor excluding leading dimensions of size 1.</span></span> <span data-ttu-id="872e8-123">Por ejemplo, un tensores con tamaños de `{1,2,3,4}` tiene una clasificación 3 efectiva, como un tensores con tamaños de `{1,1,5,5,5}` .</span><span class="sxs-lookup"><span data-stu-id="872e8-123">For example a tensor with sizes of `{1,2,3,4}` has effective rank 3, as does a tensor with sizes of `{1,1,5,5,5}`.</span></span> <span data-ttu-id="872e8-124">Un tensores con tamaños `{1,1,1,1}` tiene una clasificación 0 efectiva.</span><span class="sxs-lookup"><span data-stu-id="872e8-124">A tensor with sizes `{1,1,1,1}` has effective rank 0.</span></span>

<span data-ttu-id="872e8-125">Considere un *InputTensor* con *tamaños* de `{1,1,12,5}` .</span><span class="sxs-lookup"><span data-stu-id="872e8-125">Consider an *InputTensor* with *Sizes* of `{1,1,12,5}`.</span></span> <span data-ttu-id="872e8-126">Este tensores de entrada contiene 60 elementos y tiene un rango efectivo de 2.</span><span class="sxs-lookup"><span data-stu-id="872e8-126">This input tensor contains 60 elements, and has an effective rank of 2.</span></span> <span data-ttu-id="872e8-127">En este ejemplo, todos los tamaños válidos de *OutputCoordinatesTensor* tienen el formato `{1,1,60,N}` , donde N >= 2 pero no mayor que *DimensionCount* (4 en este ejemplo).</span><span class="sxs-lookup"><span data-stu-id="872e8-127">In this example all valid sizes of *OutputCoordinatesTensor* are of the form `{1,1,60,N}`, where N >= 2 but no greater than the *DimensionCount* (4 in this example).</span></span>

<span data-ttu-id="872e8-128">Se garantiza que las coordenadas escritas en este tensores se ordenan por índice de elemento ascendente.</span><span class="sxs-lookup"><span data-stu-id="872e8-128">The coordinates written into this tensor are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="872e8-129">Por ejemplo, si la tensores de entrada tiene 3 valores distintos de cero en las coordenadas {1,0} , {1,2} y {0,5} , los valores escritos en *OutputCoordinatesTensor* serán `[[0,5], [1,0], [1,2]]` .</span><span class="sxs-lookup"><span data-stu-id="872e8-129">For example if the input tensor has 3 non-zero values at coordinates {1,0}, {1,2}, and {0,5}, the values written to the *OutputCoordinatesTensor* will be `[[0,5], [1,0], [1,2]]`.</span></span>

<span data-ttu-id="872e8-130">Aunque esta tensores requiere que la dimensión M sea igual al número de elementos de la tensores de entrada, este operador solo escribirá un máximo de elementos OutputCount en este tensores.</span><span class="sxs-lookup"><span data-stu-id="872e8-130">While this tensor requires its dimension M to equal the number of elements in the input tensor, this operator will only write a maximum of OutputCount elements to this tensor.</span></span> <span data-ttu-id="872e8-131">El OutputCount se devuelve a través del *OutputCountTensor* escalar.</span><span class="sxs-lookup"><span data-stu-id="872e8-131">The OutputCount is returned through the scalar *OutputCountTensor*.</span></span>

> [!NOTE]
> <span data-ttu-id="872e8-132">Los elementos restantes de este tensores más allá de OutputCount no se definen una vez que se completa este operador.</span><span class="sxs-lookup"><span data-stu-id="872e8-132">The remaining elements of this tensor beyond the OutputCount are undefined once this operator completes.</span></span> <span data-ttu-id="872e8-133">No debe basarse en los valores de estos elementos.</span><span class="sxs-lookup"><span data-stu-id="872e8-133">You shouldn't rely on the values of these elements.</span></span>

## <a name="example"></a><span data-ttu-id="872e8-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="872e8-134">Example</span></span>

```
InputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[1.0f,  0.0f, 0.0f,  2.0f],
 [-0.0f, 3.5f, 0.0f, -5.2f]]

OutputCountTensor: (Sizes:{1,1,1,1}, DataType:UINT32)
[4]

OutputCoordinatesTensor: (Sizes:{1,1,8,3}, DataType:UINT32)
[[0, 0, 0],
 [0, 0, 3],
 [0, 1, 1],
 [0, 1, 3],
 [0, 0, 0], // 
 [0, 0, 0], // Values in rows >= OutputCountTensor (4 in
 [0, 0, 0], // this case) are left undefined
 [0, 0, 0]] // 
```

## <a name="availability"></a><span data-ttu-id="872e8-135">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="872e8-135">Availability</span></span>
<span data-ttu-id="872e8-136">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="872e8-136">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="872e8-137">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="872e8-137">Tensor constraints</span></span>
<span data-ttu-id="872e8-138">*InputTensor*, *OutputCoordinatesTensor* y `OutputCountTensor` deben tener el mismo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="872e8-138">*InputTensor*, *OutputCoordinatesTensor*, and `OutputCountTensor` must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="872e8-139">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="872e8-139">Tensor support</span></span>
| <span data-ttu-id="872e8-140">Tensores</span><span class="sxs-lookup"><span data-stu-id="872e8-140">Tensor</span></span> | <span data-ttu-id="872e8-141">Clase</span><span class="sxs-lookup"><span data-stu-id="872e8-141">Kind</span></span> | <span data-ttu-id="872e8-142">Dimensions</span><span class="sxs-lookup"><span data-stu-id="872e8-142">Dimensions</span></span> | <span data-ttu-id="872e8-143">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="872e8-143">Supported dimension counts</span></span> | <span data-ttu-id="872e8-144">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="872e8-144">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="872e8-145">InputTensor</span><span class="sxs-lookup"><span data-stu-id="872e8-145">InputTensor</span></span> | <span data-ttu-id="872e8-146">Entrada</span><span class="sxs-lookup"><span data-stu-id="872e8-146">Input</span></span> | <span data-ttu-id="872e8-147">{[D0], D1, D2, D3, D4}</span><span class="sxs-lookup"><span data-stu-id="872e8-147">{ [D0], D1, D2, D3, D4 }</span></span> | <span data-ttu-id="872e8-148">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="872e8-148">4 to 5</span></span> | <span data-ttu-id="872e8-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="872e8-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="872e8-150">OutputCountTensor</span><span class="sxs-lookup"><span data-stu-id="872e8-150">OutputCountTensor</span></span> | <span data-ttu-id="872e8-151">Output</span><span class="sxs-lookup"><span data-stu-id="872e8-151">Output</span></span> | <span data-ttu-id="872e8-152">{[1], 1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="872e8-152">{ [1], 1, 1, 1, 1 }</span></span> | <span data-ttu-id="872e8-153">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="872e8-153">4 to 5</span></span> | <span data-ttu-id="872e8-154">UINT32</span><span class="sxs-lookup"><span data-stu-id="872e8-154">UINT32</span></span> |
| <span data-ttu-id="872e8-155">OutputCoordinatesTensor</span><span class="sxs-lookup"><span data-stu-id="872e8-155">OutputCoordinatesTensor</span></span> | <span data-ttu-id="872e8-156">Output</span><span class="sxs-lookup"><span data-stu-id="872e8-156">Output</span></span> | <span data-ttu-id="872e8-157">{[1], 1, 1, M, N}</span><span class="sxs-lookup"><span data-stu-id="872e8-157">{ [1], 1, 1, M, N }</span></span> | <span data-ttu-id="872e8-158">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="872e8-158">4 to 5</span></span> | <span data-ttu-id="872e8-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="872e8-159">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="872e8-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="872e8-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="872e8-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="872e8-161">**Header**</span></span> | <span data-ttu-id="872e8-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="872e8-162">directml.h</span></span> |