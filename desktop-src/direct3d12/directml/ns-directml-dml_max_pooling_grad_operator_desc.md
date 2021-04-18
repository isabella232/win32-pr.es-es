---
UID: NS:directml.DML_MAX_POOLING_GRAD_OPERATOR_DESC
title: DML_MAX_POOLING_GRAD_OPERATOR_DESC
description: Calcula los degradados de propagación de la memoria para la agrupación máxima (vea [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).
helpviewer_keywords:
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- DML_MAX_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_MAX_POOLING_GRAD_OPERATOR_DESC, DML_MAX_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: b7314cb6b9456d9ac9f99e90100085e86f88ffd9
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721363"
---
# <a name="dml_max_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="19a83-103">DML_MAX_POOLING_GRAD_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="19a83-103">DML_MAX_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="19a83-104">Calcula los degradados de propagación de la memoria para la agrupación máxima (vea [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span><span class="sxs-lookup"><span data-stu-id="19a83-104">Computes backpropagation gradients for max pooling (see [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span></span>

<span data-ttu-id="19a83-105">Considere una **DML_MAX_POOLING2_OPERATOR_DESC** 2x2 sin relleno ni dilations y un paso de 1, que realiza lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="19a83-105">Consider a 2x2 **DML_MAX_POOLING2_OPERATOR_DESC** without padding nor dilations and a stride of 1, which performs the following.</span></span>

```
InputTensor             OutputTensor    IndicesTensor
[[1, 2, 3],   MaxPool    [[4, 4],        [[4, 4],
 [2, 4, 2],     -->       [6, 7]]         [7, 8]]
 [5, 6, 7]]
```

<span data-ttu-id="19a83-106">El elemento más grande de cada ventana de 2x2 en el tensores de entrada genera un elemento de la salida.</span><span class="sxs-lookup"><span data-stu-id="19a83-106">The largest element of each 2x2 window in the input tensor produces one element of the output.</span></span> <span data-ttu-id="19a83-107">A continuación se muestra un ejemplo de la salida de **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, dados parámetros similares.</span><span class="sxs-lookup"><span data-stu-id="19a83-107">Below is an example of the output of **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, given similar parameters.</span></span>

```
InputTensor   InputGradientTensor            OutputGradientTensor
[[1, 2, 3],       [[1, 2],     MaxPoolGrad   [[0, 0, 0],
 [2, 4, 2],        [4, 5]]         -->        [0, 3, 0],
 [5, 6, 7]]                                   [0, 4, 5]]
```

<span data-ttu-id="19a83-108">En efecto, este operador usa *InputTensor* para determinar el índice del elemento más grande de cada ventana y distribuye los valores de *InputGradientTensor* a *OutputGradientTensor* basándose en estos índices.</span><span class="sxs-lookup"><span data-stu-id="19a83-108">In effect, this operator uses the *InputTensor* to determine the index of the largest element from each window, and distributes the values of *InputGradientTensor* into the *OutputGradientTensor* based on these indices.</span></span> <span data-ttu-id="19a83-109">Donde se superponen los índices, se suman los valores.</span><span class="sxs-lookup"><span data-stu-id="19a83-109">Where indices overlap, the values are summed.</span></span> <span data-ttu-id="19a83-110">Los elementos de salida sin referencia tienen ceros.</span><span class="sxs-lookup"><span data-stu-id="19a83-110">Any unreferenced output elements are zeroed.</span></span>

<span data-ttu-id="19a83-111">En el caso de una operación de vinculación (donde más de un elemento de una ventana tiene el mismo valor máximo), se elige el elemento con el índice de elemento lógico más bajo.</span><span class="sxs-lookup"><span data-stu-id="19a83-111">In the case of a tie (where more than one element in a window has the same maximum value), the element with the lowest logical element index is chosen.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19a83-112">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="19a83-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="19a83-113">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="19a83-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="19a83-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19a83-114">Syntax</span></span>

```cpp
struct DML_MAX_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  _Field_size_(DimensionCount) const UINT* Dilations;
};
```

## <a name="members"></a><span data-ttu-id="19a83-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="19a83-115">Members</span></span>

`InputTensor`

<span data-ttu-id="19a83-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="19a83-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="19a83-117">La característica de entrada tensores.</span><span class="sxs-lookup"><span data-stu-id="19a83-117">The input feature tensor.</span></span> <span data-ttu-id="19a83-118">Suele ser el mismo tensores que se proporcionó como *InputTensor* para [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) en el paso de avance.</span><span class="sxs-lookup"><span data-stu-id="19a83-118">This is typically the same tensor that was provided as the *InputTensor* to [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="19a83-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="19a83-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="19a83-120">Tensores de degradado entrante.</span><span class="sxs-lookup"><span data-stu-id="19a83-120">The incoming gradient tensor.</span></span> <span data-ttu-id="19a83-121">Normalmente se obtiene a partir de la salida de la propagación de una capa anterior.</span><span class="sxs-lookup"><span data-stu-id="19a83-121">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="19a83-122">Normalmente, este tensores tendría el mismo tamaño que la *salida* de la [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) correspondiente en el paso de avance.</span><span class="sxs-lookup"><span data-stu-id="19a83-122">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="19a83-123">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="19a83-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="19a83-124">Tensores de salida que contiene los degradados retropagados.</span><span class="sxs-lookup"><span data-stu-id="19a83-124">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="19a83-125">Normalmente, este tensores tendría el mismo tamaño que la *entrada* del [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) correspondiente en el paso de avance.</span><span class="sxs-lookup"><span data-stu-id="19a83-125">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="19a83-126">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="19a83-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="19a83-127">El número de elementos de las matrices de los *progresos*, *Windows*, *StartPadding*, *EndPadding* y *Dilations* .</span><span class="sxs-lookup"><span data-stu-id="19a83-127">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, *EndPadding*, and *Dilations* arrays.</span></span> <span data-ttu-id="19a83-128">Este valor debe ser igual al número de dimensiones espaciales (InputTensor DimensionCount-2).</span><span class="sxs-lookup"><span data-stu-id="19a83-128">This value must equal the spatial dimension count (InputTensor's DimensionCount - 2).</span></span> <span data-ttu-id="19a83-129">Dado que este operador solo admite decenas de 4D, el único valor válido para este parámetro es 2.</span><span class="sxs-lookup"><span data-stu-id="19a83-129">As this operator only supports 4D tensors, the only valid value for this parameter is 2.</span></span>

`Strides`

<span data-ttu-id="19a83-130">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="19a83-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="19a83-131">Vea los *avances* en [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="19a83-131">See *Strides* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`WindowSize`

<span data-ttu-id="19a83-132">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="19a83-132">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="19a83-133">Consulte *Windows* en [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="19a83-133">See *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`StartPadding`

<span data-ttu-id="19a83-134">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="19a83-134">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="19a83-135">Consulte *StartPadding* en [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="19a83-135">See *StartPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`EndPadding`

<span data-ttu-id="19a83-136">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="19a83-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="19a83-137">Consulte *EndPadding* en [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="19a83-137">See *EndPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`Dilations`

<span data-ttu-id="19a83-138">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="19a83-138">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="19a83-139">Consulte *Dilations* en [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="19a83-139">See *Dilations* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

## <a name="availability"></a><span data-ttu-id="19a83-140">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="19a83-140">Availability</span></span>
<span data-ttu-id="19a83-141">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="19a83-141">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="19a83-142">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="19a83-142">Tensor constraints</span></span>
* <span data-ttu-id="19a83-143">*InputTensor* y *OutputGradientTensor* deben tener el mismo *tamaño*.</span><span class="sxs-lookup"><span data-stu-id="19a83-143">*InputTensor* and *OutputGradientTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="19a83-144">*InputGradientTensor*, *InputTensor* y *OutputGradientTensor* deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="19a83-144">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="19a83-145">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="19a83-145">Tensor support</span></span>
| <span data-ttu-id="19a83-146">Tensores</span><span class="sxs-lookup"><span data-stu-id="19a83-146">Tensor</span></span> | <span data-ttu-id="19a83-147">Clase</span><span class="sxs-lookup"><span data-stu-id="19a83-147">Kind</span></span> | <span data-ttu-id="19a83-148">Dimensions</span><span class="sxs-lookup"><span data-stu-id="19a83-148">Dimensions</span></span> | <span data-ttu-id="19a83-149">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="19a83-149">Supported dimension counts</span></span> | <span data-ttu-id="19a83-150">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="19a83-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="19a83-151">InputTensor</span><span class="sxs-lookup"><span data-stu-id="19a83-151">InputTensor</span></span> | <span data-ttu-id="19a83-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="19a83-152">Input</span></span> | <span data-ttu-id="19a83-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="19a83-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="19a83-154">4</span><span class="sxs-lookup"><span data-stu-id="19a83-154">4</span></span> | <span data-ttu-id="19a83-155">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="19a83-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="19a83-156">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="19a83-156">InputGradientTensor</span></span> | <span data-ttu-id="19a83-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="19a83-157">Input</span></span> | <span data-ttu-id="19a83-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="19a83-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="19a83-159">4</span><span class="sxs-lookup"><span data-stu-id="19a83-159">4</span></span> | <span data-ttu-id="19a83-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="19a83-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="19a83-161">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="19a83-161">OutputGradientTensor</span></span> | <span data-ttu-id="19a83-162">Output</span><span class="sxs-lookup"><span data-stu-id="19a83-162">Output</span></span> | <span data-ttu-id="19a83-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="19a83-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="19a83-164">4</span><span class="sxs-lookup"><span data-stu-id="19a83-164">4</span></span> | <span data-ttu-id="19a83-165">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="19a83-165">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="19a83-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19a83-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="19a83-167">**Header**</span><span class="sxs-lookup"><span data-stu-id="19a83-167">**Header**</span></span> | <span data-ttu-id="19a83-168">directml. h</span><span class="sxs-lookup"><span data-stu-id="19a83-168">directml.h</span></span> |