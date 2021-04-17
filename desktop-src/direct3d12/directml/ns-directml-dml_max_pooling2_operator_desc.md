---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Calcula el valor máximo en los elementos de la ventana deslizante sobre la tensores de entrada y, opcionalmente, devuelve los índices de los valores máximos seleccionados.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 7d2dc9d28e8afcaa5cc6277e26f1f663f3f6688f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721302"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a><span data-ttu-id="19472-103">DML_MAX_POOLING2_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="19472-103">DML_MAX_POOLING2_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="19472-104">Calcula el valor máximo en los elementos de la ventana deslizante sobre la tensores de entrada y, opcionalmente, devuelve los índices de los valores máximos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="19472-104">Computes the maximum value across the elements within the sliding window over the input tensor, and optionally returns the indices of the maximum values selected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19472-105">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="19472-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="19472-106">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="19472-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="19472-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19472-107">Syntax</span></span>
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a><span data-ttu-id="19472-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="19472-108">Members</span></span>

`InputTensor`

<span data-ttu-id="19472-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="19472-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="19472-110">Una tensores de entrada de *tamaños* `{ BatchCount, ChannelCount, Height, Width }` si *InputTensor. DimensionCount* es 4 y `{ BatchCount, ChannelCount, Depth, Height, Weight } ` si *InputTensor. DimensionCount* es 5.</span><span class="sxs-lookup"><span data-stu-id="19472-110">An input tensor of *Sizes* `{ BatchCount, ChannelCount, Height, Width }` if *InputTensor.DimensionCount* is 4, and `{ BatchCount, ChannelCount, Depth, Height, Weight } `if *InputTensor.DimensionCount* is 5.</span></span>


`OutputTensor`

<span data-ttu-id="19472-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="19472-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="19472-112">Tensores de salida en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="19472-112">An output tensor to write the results to.</span></span> <span data-ttu-id="19472-113">Los tamaños de los tensores de salida se pueden calcular como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="19472-113">The sizes of the output tensor can be computed as follows.</span></span>

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

<span data-ttu-id="19472-114">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="19472-114">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="19472-115">Un tensores de salida opcional de los índices a la *InputTensor* de entrada tensores de los valores máximos generados y almacenados en *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="19472-115">An optional output tensor of indices to the input tensor *InputTensor* of the maximum values produced and stored in the *OutputTensor*.</span></span> <span data-ttu-id="19472-116">Estos valores de índice son de base cero y tratan la entrada tensores como una matriz unidimensional contigua.</span><span class="sxs-lookup"><span data-stu-id="19472-116">These index values are zero-based and treat the input tensor as a contiguous one-dimensional array.</span></span> <span data-ttu-id="19472-117">Cuando varios elementos de la ventana deslizante tienen el mismo valor, se omiten los valores iguales posteriores y el índice apunta al primer valor encontrado.</span><span class="sxs-lookup"><span data-stu-id="19472-117">When multiple elements within the sliding window have the same value, the later equal values are ignored and the index points to the first value encountered.</span></span> <span data-ttu-id="19472-118">Tanto *OutputTensor* como *OutputIndicesTensor* tienen los mismos tamaños de tensores.</span><span class="sxs-lookup"><span data-stu-id="19472-118">Both the *OutputTensor* and *OutputIndicesTensor* have the same tensor sizes.</span></span>


`DimensionCount`

<span data-ttu-id="19472-119">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="19472-119">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="19472-120">El número de dimensiones espaciales de la tensores de entrada *InputTensor*, que también se corresponde con el número de dimensiones de *la ventana* deslizante.</span><span class="sxs-lookup"><span data-stu-id="19472-120">The number of spatial dimensions of the input tensor *InputTensor*, which also corresponds to the number of dimensions of the sliding window *WindowSize*.</span></span> <span data-ttu-id="19472-121">Este valor también determina el tamaño de las matrices de los *progresos*, *StartPadding* y *EndPadding* .</span><span class="sxs-lookup"><span data-stu-id="19472-121">This value also determines the size of the *Strides*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="19472-122">Debe establecerse en 2 cuando el valor de *InputTensor* es 4D y 3 cuando es un tensores de 5D.</span><span class="sxs-lookup"><span data-stu-id="19472-122">It should be set to 2 when *InputTensor* is 4D, and 3 when it's a 5D tensor.</span></span>


`Strides`

<span data-ttu-id="19472-123">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="19472-123">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="19472-124">El progresa para las dimensiones de la ventana deslizante de tamaños `{ Height, Width }` cuando *DimensionCount* se establece en 2, o `{ Depth, Height, Width }` cuando se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="19472-124">The strides for the sliding window dimensions of sizes `{ Height, Width }` when the *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`WindowSize`

<span data-ttu-id="19472-125">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="19472-125">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="19472-126">Las dimensiones de la ventana deslizante en `{ Height, Width }` cuando *DimensionCount* se establece en 2, o `{ Depth, Height, Width }` cuando se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="19472-126">The dimensions of the sliding window in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`StartPadding`

<span data-ttu-id="19472-127">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="19472-127">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="19472-128">El número de elementos de relleno que se van a aplicar al principio de cada dimensión espacial del *InputTensor* de entrada tensores.</span><span class="sxs-lookup"><span data-stu-id="19472-128">The number of padding elements to be applied to the beginning of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="19472-129">Los valores están en `{ Height, Width }` cuando *DimensionCount* se establece en 2, o `{ Depth, Height, Width }` cuando se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="19472-129">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`EndPadding`

<span data-ttu-id="19472-130">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="19472-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="19472-131">El número de elementos de relleno que se van a aplicar al final de cada dimensión espacial de la *InputTensor* de entrada tensores.</span><span class="sxs-lookup"><span data-stu-id="19472-131">The number of padding elements to be applied to the end of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="19472-132">Los valores están en `{ Height, Width }` cuando *DimensionCount* se establece en 2, o `{ Depth, Height, Width }` cuando se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="19472-132">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`Dilations`

<span data-ttu-id="19472-133">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="19472-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="19472-134">Los valores de cada dimensión espacial del *InputTensor* de entrada tensores por el que se selecciona un elemento dentro de la ventana deslizante para todos los elementos de ese valor.</span><span class="sxs-lookup"><span data-stu-id="19472-134">The values for each spatial dimension of the input tensor *InputTensor* by which an element within the sliding window is selected for every elements of that value.</span></span> <span data-ttu-id="19472-135">Los valores están en `{ Height, Width }` cuando *DimensionCount* se establece en 2, o `{ Depth, Height, Width }` cuando se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="19472-135">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


## <a name="remarks"></a><span data-ttu-id="19472-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19472-136">Remarks</span></span>
<span data-ttu-id="19472-137">**DML_MAX_POOLING2_OPERATOR_DESC** sustituye a la versión anterior [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) por una matriz de constantes *Dilations* adicional.</span><span class="sxs-lookup"><span data-stu-id="19472-137">**DML_MAX_POOLING2_OPERATOR_DESC** supersedes the earlier version [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) with an additional constant array *Dilations*.</span></span> <span data-ttu-id="19472-138">Las dos versiones son equivalentes cuando *Dilations* se establece en `{ 1,1 }` para la entrada 4D `{ 1,1,1 }` o para las características de entrada 5D.</span><span class="sxs-lookup"><span data-stu-id="19472-138">The two versions are equivalent when *Dilations* is set to `{ 1,1 }` for 4D input, or `{ 1,1,1 }` for 5D input features.</span></span>

## <a name="availability"></a><span data-ttu-id="19472-139">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="19472-139">Availability</span></span>
<span data-ttu-id="19472-140">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="19472-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="19472-141">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="19472-141">Tensor constraints</span></span>
* <span data-ttu-id="19472-142">*InputTensor*, *OutputIndicesTensor* y *OutputTensor* deben tener el mismo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="19472-142">*InputTensor*, *OutputIndicesTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="19472-143">*InputTensor* y *OutputTensor* deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="19472-143">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="19472-144">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="19472-144">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="19472-145">DML_FEATURE_LEVEL_3_0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="19472-145">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="19472-146">Tensores</span><span class="sxs-lookup"><span data-stu-id="19472-146">Tensor</span></span> | <span data-ttu-id="19472-147">Clase</span><span class="sxs-lookup"><span data-stu-id="19472-147">Kind</span></span> | <span data-ttu-id="19472-148">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="19472-148">Supported dimension counts</span></span> | <span data-ttu-id="19472-149">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="19472-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="19472-150">InputTensor</span><span class="sxs-lookup"><span data-stu-id="19472-150">InputTensor</span></span> | <span data-ttu-id="19472-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="19472-151">Input</span></span> | <span data-ttu-id="19472-152">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="19472-152">4 to 5</span></span> | <span data-ttu-id="19472-153">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="19472-153">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="19472-154">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="19472-154">OutputTensor</span></span> | <span data-ttu-id="19472-155">Output</span><span class="sxs-lookup"><span data-stu-id="19472-155">Output</span></span> | <span data-ttu-id="19472-156">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="19472-156">4 to 5</span></span> | <span data-ttu-id="19472-157">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="19472-157">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="19472-158">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="19472-158">OutputIndicesTensor</span></span> | <span data-ttu-id="19472-159">Salida opcional</span><span class="sxs-lookup"><span data-stu-id="19472-159">Optional output</span></span> | <span data-ttu-id="19472-160">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="19472-160">4 to 5</span></span> | <span data-ttu-id="19472-161">UINT32</span><span class="sxs-lookup"><span data-stu-id="19472-161">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="19472-162">DML_FEATURE_LEVEL_2_1 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="19472-162">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="19472-163">Tensores</span><span class="sxs-lookup"><span data-stu-id="19472-163">Tensor</span></span> | <span data-ttu-id="19472-164">Clase</span><span class="sxs-lookup"><span data-stu-id="19472-164">Kind</span></span> | <span data-ttu-id="19472-165">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="19472-165">Supported dimension counts</span></span> | <span data-ttu-id="19472-166">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="19472-166">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="19472-167">InputTensor</span><span class="sxs-lookup"><span data-stu-id="19472-167">InputTensor</span></span> | <span data-ttu-id="19472-168">Entrada</span><span class="sxs-lookup"><span data-stu-id="19472-168">Input</span></span> | <span data-ttu-id="19472-169">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="19472-169">4 to 5</span></span> | <span data-ttu-id="19472-170">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="19472-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="19472-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="19472-171">OutputTensor</span></span> | <span data-ttu-id="19472-172">Output</span><span class="sxs-lookup"><span data-stu-id="19472-172">Output</span></span> | <span data-ttu-id="19472-173">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="19472-173">4 to 5</span></span> | <span data-ttu-id="19472-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="19472-174">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="19472-175">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="19472-175">OutputIndicesTensor</span></span> | <span data-ttu-id="19472-176">Salida opcional</span><span class="sxs-lookup"><span data-stu-id="19472-176">Optional output</span></span> | <span data-ttu-id="19472-177">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="19472-177">4 to 5</span></span> | <span data-ttu-id="19472-178">UINT32</span><span class="sxs-lookup"><span data-stu-id="19472-178">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="19472-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19472-179">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="19472-180">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="19472-180">**Minimum supported client**</span></span> | <span data-ttu-id="19472-181">Windows 10, versión 2004 (10,0; Compilación 19041)</span><span class="sxs-lookup"><span data-stu-id="19472-181">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="19472-182">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="19472-182">**Minimum supported server**</span></span> | <span data-ttu-id="19472-183">Windows Server, versión 2004 (10,0; Compilación 19041)</span><span class="sxs-lookup"><span data-stu-id="19472-183">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="19472-184">**Header**</span><span class="sxs-lookup"><span data-stu-id="19472-184">**Header**</span></span> | <span data-ttu-id="19472-185">directml. h</span><span class="sxs-lookup"><span data-stu-id="19472-185">directml.h</span></span> |