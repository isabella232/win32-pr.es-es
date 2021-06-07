---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Extrae una sola subregión (un "segmento") de un tensor de entrada.
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: f34525865be9541da879e66e88c29d4a2ab74f00
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417944"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a><span data-ttu-id="3f594-103">DML_SLICE1_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="3f594-103">DML_SLICE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="3f594-104">Extrae una sola subregión (un "segmento") de un tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="3f594-104">Extracts a single subregion (a "slice") of an input tensor.</span></span>

<span data-ttu-id="3f594-105">La *ventana de* entrada describe los límites del tensor de entrada que se deben tener en cuenta en el segmento.</span><span class="sxs-lookup"><span data-stu-id="3f594-105">The *input window* describes the bounds of the input tensor to consider in the slice.</span></span> <span data-ttu-id="3f594-106">La ventana se define mediante tres valores para cada dimensión.</span><span class="sxs-lookup"><span data-stu-id="3f594-106">The window is defined using three values for each dimension.</span></span>

- <span data-ttu-id="3f594-107">El *desplazamiento* marca el *principio de la ventana* en una dimensión.</span><span class="sxs-lookup"><span data-stu-id="3f594-107">The *offset* marks the *beginning of the window* in a dimension.</span></span>
- <span data-ttu-id="3f594-108">El *tamaño* marca la extensión de la ventana en una dimensión.</span><span class="sxs-lookup"><span data-stu-id="3f594-108">The *size* marks the extent of the window in a dimension.</span></span> <span data-ttu-id="3f594-109">El *final de la ventana* de una dimensión es `offset + size - 1` .</span><span class="sxs-lookup"><span data-stu-id="3f594-109">The *end of the window* in a dimension is `offset + size - 1`.</span></span>
- <span data-ttu-id="3f594-110">El *paso* indica cómo recorrer los elementos de una dimensión.</span><span class="sxs-lookup"><span data-stu-id="3f594-110">The *stride* indicates how to traverse the elements in a dimension.</span></span>
  - <span data-ttu-id="3f594-111">La magnitud del paso indica cuántos elementos avanzar al copiar dentro de la ventana.</span><span class="sxs-lookup"><span data-stu-id="3f594-111">The magnitude of the stride indicates how many elements to advance when copying within the window.</span></span>
  - <span data-ttu-id="3f594-112">Si un paso es positivo, los elementos se copian a partir *del principio* de la ventana de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="3f594-112">If a stride is positive, elements are copied starting at the *beginning* of the window in the dimension.</span></span>
  - <span data-ttu-id="3f594-113">Si un paso es negativo, los elementos se copian a partir del *final* de la ventana de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="3f594-113">If a stride is negative, elements are copied starting at the *end* of the window in the dimension.</span></span>

<span data-ttu-id="3f594-114">En el pseudocódigo siguiente se muestra cómo se copian los elementos mediante la ventana de entrada.</span><span class="sxs-lookup"><span data-stu-id="3f594-114">The following pseudo-code illustrates how elements are copied using the input window.</span></span> <span data-ttu-id="3f594-115">Observe cómo los elementos de una dimensión se copian de principio a fin con un paso positivo y se copian de un extremo a otro con un paso negativo.</span><span class="sxs-lookup"><span data-stu-id="3f594-115">Note how elements in a dimension are copied from start to end with a positive stride, and copied from end to start with a negative stride.</span></span>

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

<span data-ttu-id="3f594-116">La ventana de entrada no debe estar vacía en ninguna dimensión y la ventana no debe extenderse más allá de las dimensiones del tensor de entrada (no se permiten lecturas fuera de límite).</span><span class="sxs-lookup"><span data-stu-id="3f594-116">The input window mustn't be empty in any dimension, and the window mustn't extend beyond the dimensions of the input tensor (out-of-bounds reads aren't permitted).</span></span> <span data-ttu-id="3f594-117">El tamaño y los avances de la ventana limitan eficazmente el número de elementos que se pueden copiar de cada dimensión `i` del tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="3f594-117">The window's size and strides effectively limit the number of elements that may be copied from each dimension `i` of the input tensor.</span></span>

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

<span data-ttu-id="3f594-118">El tensor de salida no es necesario para copiar todos los elementos accesibles dentro de la ventana.</span><span class="sxs-lookup"><span data-stu-id="3f594-118">The output tensor isn't required to copy all reachable elements within the window.</span></span> <span data-ttu-id="3f594-119">El segmento es válido siempre que `1 <= OutputSizes[i] <= MaxCopiedElements[i]` .</span><span class="sxs-lookup"><span data-stu-id="3f594-119">The slice is valid so long as `1 <= OutputSizes[i] <= MaxCopiedElements[i]`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f594-120">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="3f594-120">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="3f594-121">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="3f594-121">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3f594-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f594-122">Syntax</span></span>
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a><span data-ttu-id="3f594-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="3f594-123">Members</span></span>

`InputTensor`

<span data-ttu-id="3f594-124">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3f594-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3f594-125">Tensor del que se extraen los segmentos.</span><span class="sxs-lookup"><span data-stu-id="3f594-125">The tensor to extract slices from.</span></span>


`OutputTensor`

<span data-ttu-id="3f594-126">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3f594-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3f594-127">Tensor en el que se escriben los resultados de los datos segmentados.</span><span class="sxs-lookup"><span data-stu-id="3f594-127">The tensor to write the sliced data results to.</span></span>


`DimensionCount`

<span data-ttu-id="3f594-128">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="3f594-128">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="3f594-129">Número de dimensiones.</span><span class="sxs-lookup"><span data-stu-id="3f594-129">The number of dimensions.</span></span> <span data-ttu-id="3f594-130">Este campo determina el tamaño de las *matrices InputWindowOffsets,* *InputWindowSizes* y *InputWindowStrides.*</span><span class="sxs-lookup"><span data-stu-id="3f594-130">This field determines the size of the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="3f594-131">Este valor debe coincidir con *dimensioncount* de los tensores de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="3f594-131">This value must match the *DimensionCount* of the input and output tensors.</span></span> <span data-ttu-id="3f594-132">Este valor debe estar entre 1 y 8, ambos inclusive, a partir de ; los niveles de características anteriores requieren un valor `DML_FEATURE_LEVEL_3_0` de 4 o 5.</span><span class="sxs-lookup"><span data-stu-id="3f594-132">This value must be between 1 and 8, inclusively, starting from `DML_FEATURE_LEVEL_3_0`; earlier feature levels require a value of either 4 or 5.</span></span>


`InputWindowOffsets`

<span data-ttu-id="3f594-133">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="3f594-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="3f594-134">Matriz que contiene el principio (en elementos) de la ventana de entrada en cada dimensión.</span><span class="sxs-lookup"><span data-stu-id="3f594-134">An array containing the beginning (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="3f594-135">Los valores de la matriz deben satisfacer la restricción `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="3f594-135">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowSizes`

<span data-ttu-id="3f594-136">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="3f594-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="3f594-137">Matriz que contiene la extensión (en elementos) de la ventana de entrada en cada dimensión.</span><span class="sxs-lookup"><span data-stu-id="3f594-137">An array containing the extent (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="3f594-138">Los valores de la matriz deben satisfacer la restricción `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="3f594-138">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowStrides`

<span data-ttu-id="3f594-139">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="3f594-139">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="3f594-140">Matriz que contiene el paso del segmento a lo largo de cada dimensión del tensor de entrada, en elementos .</span><span class="sxs-lookup"><span data-stu-id="3f594-140">An array containing the slice's stride along each dimension of the input tensor, in elements.</span></span> <span data-ttu-id="3f594-141">La magnitud del paso indica cuántos elementos avanzar al copiar dentro de la ventana de entrada.</span><span class="sxs-lookup"><span data-stu-id="3f594-141">The magnitude of the stride indicates how many elements to advance when copying within the input window.</span></span> <span data-ttu-id="3f594-142">El signo del paso determina si los elementos se copian a partir del principio de la ventana (paso positivo) o al final de la ventana (paso negativo).</span><span class="sxs-lookup"><span data-stu-id="3f594-142">The sign of the stride determines if elements are copied starting at the beginning of the window (positive stride) or end of the window (negative stride).</span></span> <span data-ttu-id="3f594-143">Es posible que Strides no sea 0.</span><span class="sxs-lookup"><span data-stu-id="3f594-143">Strides may not be 0.</span></span>

## <a name="examples"></a><span data-ttu-id="3f594-144">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3f594-144">Examples</span></span>

<span data-ttu-id="3f594-145">En los ejemplos siguientes se usa este mismo tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="3f594-145">The following examples use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a><span data-ttu-id="3f594-146">Ejemplo 1.</span><span class="sxs-lookup"><span data-stu-id="3f594-146">Example 1.</span></span> <span data-ttu-id="3f594-147">Segmento strided con strides positivos</span><span class="sxs-lookup"><span data-stu-id="3f594-147">Strided slice with positive strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

<span data-ttu-id="3f594-148">Los elementos copiados se calculan como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="3f594-148">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a><span data-ttu-id="3f594-149">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="3f594-149">Example 2.</span></span> <span data-ttu-id="3f594-150">Segmento con strid con strides negativos</span><span class="sxs-lookup"><span data-stu-id="3f594-150">Strided slice with negative strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

<span data-ttu-id="3f594-151">Recuerde que las dimensiones con avances de ventana negativos comienzan a copiarse al final de la ventana de entrada para esa dimensión; Esto se realiza agregando `InputWindowSize[i] - 1` al desplazamiento de la ventana.</span><span class="sxs-lookup"><span data-stu-id="3f594-151">Recall that dimensions with negative window strides start copying at the end of the input window for that dimension; this is done by adding `InputWindowSize[i] - 1` to the window offset.</span></span> <span data-ttu-id="3f594-152">Las dimensiones con un paso positivo simplemente comienzan en `InputWindowOffset[i]` .</span><span class="sxs-lookup"><span data-stu-id="3f594-152">Dimensions with a positive stride simply start at `InputWindowOffset[i]`.</span></span>
- <span data-ttu-id="3f594-153">El eje 0 `+1` (paso de la ventana) comienza a copiarse en `InputWindowOffsets[0] = 0` .</span><span class="sxs-lookup"><span data-stu-id="3f594-153">Axis 0 (`+1` window stride) starts copying at `InputWindowOffsets[0] = 0`.</span></span> 
- <span data-ttu-id="3f594-154">El eje 1 `+1` (paso de la ventana) comienza a copiarse en `InputWindowOffsets[1] = 0` .</span><span class="sxs-lookup"><span data-stu-id="3f594-154">Axis 1 (`+1` window stride) starts copying at `InputWindowOffsets[1] = 0`.</span></span> 
- <span data-ttu-id="3f594-155">El eje 2 `-2` (paso de la ventana) comienza a copiarse en `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` .</span><span class="sxs-lookup"><span data-stu-id="3f594-155">Axis 2 (`-2` window stride) starts copying at `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3`.</span></span> 
- <span data-ttu-id="3f594-156">El eje 3 `+2` (paso de la ventana) comienza a copiarse en `InputWindowOffsets[3] = 1` .</span><span class="sxs-lookup"><span data-stu-id="3f594-156">Axis 3 (`+2` window stride) starts copying at `InputWindowOffsets[3] = 1`.</span></span> 

<span data-ttu-id="3f594-157">Los elementos copiados se calculan como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="3f594-157">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a><span data-ttu-id="3f594-158">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f594-158">Remarks</span></span>
<span data-ttu-id="3f594-159">Este operador es similar a [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), pero difiere de dos maneras importantes.</span><span class="sxs-lookup"><span data-stu-id="3f594-159">This operator is similar to [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), but it differs in two important ways.</span></span>

- <span data-ttu-id="3f594-160">Los avances de segmento pueden ser negativos, lo que permite invertir valores a lo largo de las dimensiones.</span><span class="sxs-lookup"><span data-stu-id="3f594-160">Slice strides may be negative, which allows reversing values along dimensions.</span></span>
- <span data-ttu-id="3f594-161">Los tamaños de ventana de entrada no son necesariamente los mismos que los tamaños de tensor de salida.</span><span class="sxs-lookup"><span data-stu-id="3f594-161">The input window sizes are not necessarily the same as the output tensor sizes.</span></span>

## <a name="availability"></a><span data-ttu-id="3f594-162">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="3f594-162">Availability</span></span>
<span data-ttu-id="3f594-163">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="3f594-163">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="3f594-164">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="3f594-164">Tensor constraints</span></span>
<span data-ttu-id="3f594-165">*InputTensor* y *OutputTensor* deben tener los mismos *DataType* y *DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="3f594-165">*InputTensor* and *OutputTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="3f594-166">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="3f594-166">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="3f594-167">DML_FEATURE_LEVEL_3_0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="3f594-167">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="3f594-168">Tensor</span><span class="sxs-lookup"><span data-stu-id="3f594-168">Tensor</span></span> | <span data-ttu-id="3f594-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f594-169">Kind</span></span> | <span data-ttu-id="3f594-170">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="3f594-170">Supported dimension counts</span></span> | <span data-ttu-id="3f594-171">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="3f594-171">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="3f594-172">InputTensor</span><span class="sxs-lookup"><span data-stu-id="3f594-172">InputTensor</span></span> | <span data-ttu-id="3f594-173">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f594-173">Input</span></span> | <span data-ttu-id="3f594-174">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="3f594-174">1 to 8</span></span> | <span data-ttu-id="3f594-175">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="3f594-175">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="3f594-176">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="3f594-176">OutputTensor</span></span> | <span data-ttu-id="3f594-177">Resultados</span><span class="sxs-lookup"><span data-stu-id="3f594-177">Output</span></span> | <span data-ttu-id="3f594-178">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="3f594-178">1 to 8</span></span> | <span data-ttu-id="3f594-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="3f594-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="3f594-180">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="3f594-180">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="3f594-181">Tensor</span><span class="sxs-lookup"><span data-stu-id="3f594-181">Tensor</span></span> | <span data-ttu-id="3f594-182">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f594-182">Kind</span></span> | <span data-ttu-id="3f594-183">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="3f594-183">Supported dimension counts</span></span> | <span data-ttu-id="3f594-184">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="3f594-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="3f594-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="3f594-185">InputTensor</span></span> | <span data-ttu-id="3f594-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f594-186">Input</span></span> | <span data-ttu-id="3f594-187">De 4 a 5</span><span class="sxs-lookup"><span data-stu-id="3f594-187">4 to 5</span></span> | <span data-ttu-id="3f594-188">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="3f594-188">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="3f594-189">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="3f594-189">OutputTensor</span></span> | <span data-ttu-id="3f594-190">Resultados</span><span class="sxs-lookup"><span data-stu-id="3f594-190">Output</span></span> | <span data-ttu-id="3f594-191">De 4 a 5</span><span class="sxs-lookup"><span data-stu-id="3f594-191">4 to 5</span></span> | <span data-ttu-id="3f594-192">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="3f594-192">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="3f594-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f594-193">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3f594-194">**Header**</span><span class="sxs-lookup"><span data-stu-id="3f594-194">**Header**</span></span> | <span data-ttu-id="3f594-195">directml.h</span><span class="sxs-lookup"><span data-stu-id="3f594-195">directml.h</span></span> |