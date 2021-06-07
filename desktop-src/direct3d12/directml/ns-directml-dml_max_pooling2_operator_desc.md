---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Calcula el valor máximo en los elementos de la ventana deslizante sobre el tensor de entrada y, opcionalmente, devuelve los índices de los valores máximos seleccionados.
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
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417976"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a><span data-ttu-id="ac295-103">DML_MAX_POOLING2_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="ac295-103">DML_MAX_POOLING2_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="ac295-104">Calcula el valor máximo en los elementos de la ventana deslizante sobre el tensor de entrada y, opcionalmente, devuelve los índices de los valores máximos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="ac295-104">Computes the maximum value across the elements within the sliding window over the input tensor, and optionally returns the indices of the maximum values selected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac295-105">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="ac295-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="ac295-106">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="ac295-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ac295-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac295-107">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="ac295-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ac295-108">Members</span></span>

`InputTensor`

<span data-ttu-id="ac295-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ac295-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ac295-110">Un tensor de entrada de *tamaños* si `{ BatchCount, ChannelCount, Height, Width }` *InputTensor.DimensionCount* es 4 y `{ BatchCount, ChannelCount, Depth, Height, Weight } ` si *InputTensor.DimensionCount* es 5.</span><span class="sxs-lookup"><span data-stu-id="ac295-110">An input tensor of *Sizes* `{ BatchCount, ChannelCount, Height, Width }` if *InputTensor.DimensionCount* is 4, and `{ BatchCount, ChannelCount, Depth, Height, Weight } `if *InputTensor.DimensionCount* is 5.</span></span>


`OutputTensor`

<span data-ttu-id="ac295-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ac295-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ac295-112">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="ac295-112">An output tensor to write the results to.</span></span> <span data-ttu-id="ac295-113">Los tamaños del tensor de salida se pueden calcular de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="ac295-113">The sizes of the output tensor can be computed as follows.</span></span>

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

<span data-ttu-id="ac295-114">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ac295-114">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ac295-115">Un tensor de salida opcional de índices para el *tensor inputTensor* de los valores máximos generados y almacenados en *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="ac295-115">An optional output tensor of indices to the input tensor *InputTensor* of the maximum values produced and stored in the *OutputTensor*.</span></span> <span data-ttu-id="ac295-116">Estos valores de índice son de base cero y tratan el tensor de entrada como una matriz unidimensional contigua.</span><span class="sxs-lookup"><span data-stu-id="ac295-116">These index values are zero-based and treat the input tensor as a contiguous one-dimensional array.</span></span> <span data-ttu-id="ac295-117">Cuando varios elementos de la ventana deslizante tienen el mismo valor, se omiten los valores iguales posteriores y el índice apunta al primer valor encontrado.</span><span class="sxs-lookup"><span data-stu-id="ac295-117">When multiple elements within the sliding window have the same value, the later equal values are ignored and the index points to the first value encountered.</span></span> <span data-ttu-id="ac295-118">Tanto *OutputTensor* como *OutputIndicesTensor* tienen los mismos tamaños de tensor.</span><span class="sxs-lookup"><span data-stu-id="ac295-118">Both the *OutputTensor* and *OutputIndicesTensor* have the same tensor sizes.</span></span>


`DimensionCount`

<span data-ttu-id="ac295-119">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ac295-119">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="ac295-120">Número de dimensiones espaciales del *tensor InputTensor* de entrada, que también corresponde al número de dimensiones de la ventana deslizante *WindowSize.*</span><span class="sxs-lookup"><span data-stu-id="ac295-120">The number of spatial dimensions of the input tensor *InputTensor*, which also corresponds to the number of dimensions of the sliding window *WindowSize*.</span></span> <span data-ttu-id="ac295-121">Este valor también determina el tamaño de las matrices *Strides,* *StartPadding* y *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="ac295-121">This value also determines the size of the *Strides*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="ac295-122">Debe establecerse en 2 cuando *InputTensor* es 4D y 3 cuando es un tensor 5D.</span><span class="sxs-lookup"><span data-stu-id="ac295-122">It should be set to 2 when *InputTensor* is 4D, and 3 when it's a 5D tensor.</span></span>


`Strides`

<span data-ttu-id="ac295-123">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="ac295-123">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="ac295-124">Los avances de las dimensiones de ventana deslizante de tamaños cuando DimensionCount está establecido en 2 o cuando `{ Height, Width }` se establece en  `{ Depth, Height, Width }` 3.</span><span class="sxs-lookup"><span data-stu-id="ac295-124">The strides for the sliding window dimensions of sizes `{ Height, Width }` when the *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`WindowSize`

<span data-ttu-id="ac295-125">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="ac295-125">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="ac295-126">Dimensiones de la ventana deslizante en `{ Height, Width }` cuando *DimensionCount* está establecido en 2 o `{ Depth, Height, Width }` cuando se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="ac295-126">The dimensions of the sliding window in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`StartPadding`

<span data-ttu-id="ac295-127">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="ac295-127">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="ac295-128">Número de elementos de relleno que se aplicarán al principio de cada dimensión espacial del tensor *inputTensor.*</span><span class="sxs-lookup"><span data-stu-id="ac295-128">The number of padding elements to be applied to the beginning of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="ac295-129">Los valores están en `{ Height, Width }` cuando *DimensionCount* se establece en 2 o `{ Depth, Height, Width }` cuando se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="ac295-129">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`EndPadding`

<span data-ttu-id="ac295-130">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="ac295-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="ac295-131">Número de elementos de relleno que se aplicarán al final de cada dimensión espacial del tensor *inputTensor.*</span><span class="sxs-lookup"><span data-stu-id="ac295-131">The number of padding elements to be applied to the end of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="ac295-132">Los valores están en `{ Height, Width }` cuando *DimensionCount* se establece en 2 o `{ Depth, Height, Width }` cuando se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="ac295-132">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`Dilations`

<span data-ttu-id="ac295-133">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="ac295-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="ac295-134">Valores de cada dimensión espacial del *tensor inputTensor* por el que se selecciona un elemento dentro de la ventana deslizante para cada elemento de ese valor.</span><span class="sxs-lookup"><span data-stu-id="ac295-134">The values for each spatial dimension of the input tensor *InputTensor* by which an element within the sliding window is selected for every elements of that value.</span></span> <span data-ttu-id="ac295-135">Los valores están en `{ Height, Width }` cuando *DimensionCount* se establece en 2 o `{ Depth, Height, Width }` cuando se establece en 3.</span><span class="sxs-lookup"><span data-stu-id="ac295-135">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


## <a name="remarks"></a><span data-ttu-id="ac295-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac295-136">Remarks</span></span>
<span data-ttu-id="ac295-137">**DML_MAX_POOLING2_OPERATOR_DESC** reemplaza a la versión anterior [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) con una matriz constante *adicional Denciones*.</span><span class="sxs-lookup"><span data-stu-id="ac295-137">**DML_MAX_POOLING2_OPERATOR_DESC** supersedes the earlier version [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) with an additional constant array *Dilations*.</span></span> <span data-ttu-id="ac295-138">Las dos versiones son equivalentes cuando *se establece en Para* la entrada 4D o para las características de entrada `{ 1,1 }` `{ 1,1,1 }` 5D.</span><span class="sxs-lookup"><span data-stu-id="ac295-138">The two versions are equivalent when *Dilations* is set to `{ 1,1 }` for 4D input, or `{ 1,1,1 }` for 5D input features.</span></span>

## <a name="availability"></a><span data-ttu-id="ac295-139">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="ac295-139">Availability</span></span>
<span data-ttu-id="ac295-140">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="ac295-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ac295-141">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="ac295-141">Tensor constraints</span></span>
* <span data-ttu-id="ac295-142">*InputTensor*, *OutputIndicesTensor y* *OutputTensor* deben tener el mismo *DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="ac295-142">*InputTensor*, *OutputIndicesTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="ac295-143">*InputTensor* y *OutputTensor* deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="ac295-143">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ac295-144">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="ac295-144">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="ac295-145">DML_FEATURE_LEVEL_3_0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="ac295-145">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="ac295-146">Tensor</span><span class="sxs-lookup"><span data-stu-id="ac295-146">Tensor</span></span> | <span data-ttu-id="ac295-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac295-147">Kind</span></span> | <span data-ttu-id="ac295-148">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="ac295-148">Supported dimension counts</span></span> | <span data-ttu-id="ac295-149">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="ac295-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ac295-150">InputTensor</span><span class="sxs-lookup"><span data-stu-id="ac295-150">InputTensor</span></span> | <span data-ttu-id="ac295-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac295-151">Input</span></span> | <span data-ttu-id="ac295-152">De 4 a 5</span><span class="sxs-lookup"><span data-stu-id="ac295-152">4 to 5</span></span> | <span data-ttu-id="ac295-153">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ac295-153">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="ac295-154">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="ac295-154">OutputTensor</span></span> | <span data-ttu-id="ac295-155">Resultados</span><span class="sxs-lookup"><span data-stu-id="ac295-155">Output</span></span> | <span data-ttu-id="ac295-156">De 4 a 5</span><span class="sxs-lookup"><span data-stu-id="ac295-156">4 to 5</span></span> | <span data-ttu-id="ac295-157">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ac295-157">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="ac295-158">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="ac295-158">OutputIndicesTensor</span></span> | <span data-ttu-id="ac295-159">Salida opcional</span><span class="sxs-lookup"><span data-stu-id="ac295-159">Optional output</span></span> | <span data-ttu-id="ac295-160">De 4 a 5</span><span class="sxs-lookup"><span data-stu-id="ac295-160">4 to 5</span></span> | <span data-ttu-id="ac295-161">UINT32</span><span class="sxs-lookup"><span data-stu-id="ac295-161">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="ac295-162">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="ac295-162">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="ac295-163">Tensor</span><span class="sxs-lookup"><span data-stu-id="ac295-163">Tensor</span></span> | <span data-ttu-id="ac295-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac295-164">Kind</span></span> | <span data-ttu-id="ac295-165">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="ac295-165">Supported dimension counts</span></span> | <span data-ttu-id="ac295-166">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="ac295-166">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ac295-167">InputTensor</span><span class="sxs-lookup"><span data-stu-id="ac295-167">InputTensor</span></span> | <span data-ttu-id="ac295-168">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac295-168">Input</span></span> | <span data-ttu-id="ac295-169">De 4 a 5</span><span class="sxs-lookup"><span data-stu-id="ac295-169">4 to 5</span></span> | <span data-ttu-id="ac295-170">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ac295-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ac295-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="ac295-171">OutputTensor</span></span> | <span data-ttu-id="ac295-172">Resultados</span><span class="sxs-lookup"><span data-stu-id="ac295-172">Output</span></span> | <span data-ttu-id="ac295-173">De 4 a 5</span><span class="sxs-lookup"><span data-stu-id="ac295-173">4 to 5</span></span> | <span data-ttu-id="ac295-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="ac295-174">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="ac295-175">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="ac295-175">OutputIndicesTensor</span></span> | <span data-ttu-id="ac295-176">Salida opcional</span><span class="sxs-lookup"><span data-stu-id="ac295-176">Optional output</span></span> | <span data-ttu-id="ac295-177">De 4 a 5</span><span class="sxs-lookup"><span data-stu-id="ac295-177">4 to 5</span></span> | <span data-ttu-id="ac295-178">UINT32</span><span class="sxs-lookup"><span data-stu-id="ac295-178">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="ac295-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac295-179">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ac295-180">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="ac295-180">**Minimum supported client**</span></span> | <span data-ttu-id="ac295-181">Windows 10, versión 2004 (10.0; Compilación 19041)</span><span class="sxs-lookup"><span data-stu-id="ac295-181">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="ac295-182">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="ac295-182">**Minimum supported server**</span></span> | <span data-ttu-id="ac295-183">Windows Server, versión 2004 (10.0; Compilación 19041)</span><span class="sxs-lookup"><span data-stu-id="ac295-183">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="ac295-184">**Header**</span><span class="sxs-lookup"><span data-stu-id="ac295-184">**Header**</span></span> | <span data-ttu-id="ac295-185">directml.h</span><span class="sxs-lookup"><span data-stu-id="ac295-185">directml.h</span></span> |