---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Calcula los degradados de repropagación para la agrupación media [(consulte DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: aaa2b5d2becac421214afe7c643426c1c93cf899
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418014"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="45f53-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="45f53-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="45f53-104">Calcula los degradados de repropagación para la agrupación media [(consulte DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="45f53-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="45f53-105">Considere una 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, sin relleno y un paso de 1, que realiza lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="45f53-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="45f53-106">Cada ventana 2x2 del tensor de entrada se promedia para generar un elemento de la salida (lectura de ceros para los elementos más allá del borde).</span><span class="sxs-lookup"><span data-stu-id="45f53-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="45f53-107">Este es un ejemplo de la salida de DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC **parámetros** similares.</span><span class="sxs-lookup"><span data-stu-id="45f53-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="45f53-108">Observe que los valores de *OutputGradientTensor* representan las contribuciones ponderadas de ese elemento al *outputTensor* durante el operador [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) original.</span><span class="sxs-lookup"><span data-stu-id="45f53-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45f53-109">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="45f53-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="45f53-110">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="45f53-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="45f53-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45f53-111">Syntax</span></span>

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a><span data-ttu-id="45f53-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="45f53-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="45f53-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="45f53-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="45f53-114">Tensor de degradado entrante.</span><span class="sxs-lookup"><span data-stu-id="45f53-114">The incoming gradient tensor.</span></span> <span data-ttu-id="45f53-115">Normalmente, esto se obtiene a partir de la salida de la repropagación de una capa anterior.</span><span class="sxs-lookup"><span data-stu-id="45f53-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="45f53-116">Normalmente, este tensor tendría los  mismos tamaños que la salida de la DML_AVERAGE_POOLING_OPERATOR_DESC [en](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) el paso hacia delante.</span><span class="sxs-lookup"><span data-stu-id="45f53-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="45f53-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="45f53-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="45f53-118">Tensor de salida que contiene los degradados de propiedad pendiente.</span><span class="sxs-lookup"><span data-stu-id="45f53-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="45f53-119">Normalmente, este tensor tendría los  mismos tamaños que la entrada de la DML_AVERAGE_POOLING_OPERATOR_DESC [en](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) el paso hacia delante.</span><span class="sxs-lookup"><span data-stu-id="45f53-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="45f53-120">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="45f53-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="45f53-121">Número de elementos de las matrices *Strides,* *WindowSize,* *StartPadding* y *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="45f53-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="45f53-122">Este valor debe ser igual al recuento de dimensiones espaciales.</span><span class="sxs-lookup"><span data-stu-id="45f53-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="45f53-123">El recuento de dimensiones espaciales es 2 si se proporcionan tensores 4D, o 3 si se proporcionan tensores 5D.</span><span class="sxs-lookup"><span data-stu-id="45f53-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="45f53-124">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="45f53-124">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="45f53-125">Vea *Strides* en [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="45f53-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="45f53-126">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="45f53-126">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="45f53-127">Vea *WindowSize* en [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="45f53-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="45f53-128">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="45f53-128">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="45f53-129">Vea *StartPadding* [en DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="45f53-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="45f53-130">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="45f53-130">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="45f53-131">Vea *EndPadding* en [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="45f53-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="45f53-132">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="45f53-132">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="45f53-133">Vea *IncludePadding* [en DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="45f53-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="45f53-134">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="45f53-134">Availability</span></span>
<span data-ttu-id="45f53-135">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="45f53-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="45f53-136">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="45f53-136">Tensor constraints</span></span>
<span data-ttu-id="45f53-137">*InputGradientTensor* y *OutputGradientTensor* deben tener los mismos *DataType* y *DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="45f53-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="45f53-138">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="45f53-138">Tensor support</span></span>
| <span data-ttu-id="45f53-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="45f53-139">Tensor</span></span> | <span data-ttu-id="45f53-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="45f53-140">Kind</span></span> | <span data-ttu-id="45f53-141">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="45f53-141">Supported dimension counts</span></span> | <span data-ttu-id="45f53-142">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="45f53-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="45f53-143">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="45f53-143">InputGradientTensor</span></span> | <span data-ttu-id="45f53-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="45f53-144">Input</span></span> | <span data-ttu-id="45f53-145">De 4 a 5</span><span class="sxs-lookup"><span data-stu-id="45f53-145">4 to 5</span></span> | <span data-ttu-id="45f53-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="45f53-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="45f53-147">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="45f53-147">OutputGradientTensor</span></span> | <span data-ttu-id="45f53-148">Resultados</span><span class="sxs-lookup"><span data-stu-id="45f53-148">Output</span></span> | <span data-ttu-id="45f53-149">De 4 a 5</span><span class="sxs-lookup"><span data-stu-id="45f53-149">4 to 5</span></span> | <span data-ttu-id="45f53-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="45f53-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="45f53-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45f53-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="45f53-152">**Header**</span><span class="sxs-lookup"><span data-stu-id="45f53-152">**Header**</span></span> | <span data-ttu-id="45f53-153">directml.h</span><span class="sxs-lookup"><span data-stu-id="45f53-153">directml.h</span></span> |