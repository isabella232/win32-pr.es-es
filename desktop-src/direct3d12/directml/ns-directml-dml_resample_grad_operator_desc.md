---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Calcula los degradados de repropagation para Resample [(vea DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 0caba1a560b72a94ed04cacd824414964af82c35
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804044"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="1840c-103">DML_RESAMPLE_GRAD_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="1840c-103">DML_RESAMPLE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="1840c-104">Calcula los degradados de repropagation para Resample [(vea DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="1840c-104">Computes backpropagation gradients for Resample (see [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span></span>

<span data-ttu-id="1840c-105">**DML_RESAMPLE1_OPERATOR_DESC** escala las dimensiones arbitrarias del tensor de entrada mediante el muestreo del vecino más cercano o la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="1840c-105">**DML_RESAMPLE1_OPERATOR_DESC** rescales arbitrary dimensions of the input tensor using either nearest-neighbor sampling or bilinear interpolation.</span></span> <span data-ttu-id="1840c-106">Dado un *inputGradientTensor* con los  mismos tamaños que la salida de un **DML_RESAMPLE1_OPERATOR_DESC** equivalente, este operador genera  un *outputGradientTensor* con los mismos tamaños que la **entrada del DML_RESAMPLE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="1840c-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_RESAMPLE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of the **DML_RESAMPLE1_OPERATOR_DESC**.</span></span>

<span data-ttu-id="1840c-107">Por ejemplo, considere  una DML_RESAMPLE1_OPERATOR_DESC que realiza un escalado de vecino más próximo de 1,5 veces el ancho y 0,5 veces el alto.</span><span class="sxs-lookup"><span data-stu-id="1840c-107">As an example, consider a **DML_RESAMPLE1_OPERATOR_DESC** that performs a nearest-neighbor scaling of 1.5x in the width, and 0.5x in the height.</span></span>

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

<span data-ttu-id="1840c-108">Observe cómo el elemento 0 del tensor de entrada (con el valor 1) contribuye a dos elementos de la salida, el primer elemento (con el valor 2) contribuye a un elemento de la salida y los elementos 2 y 3 (con los valores 3 y 4) no contribuyen a ningún elemento de la salida.</span><span class="sxs-lookup"><span data-stu-id="1840c-108">Notice how the 0th element of the input tensor (with value 1) contributes to two elements in the output, the 1st element (with value 2) contributes to one element in the output, and the 2nd and 3rd elements (with values 3 and 4) contribute to no elements of the output.</span></span>

<span data-ttu-id="1840c-109">La propiedad **DML_RESAMPLE_GRAD_OPERATOR_DESC** realizaría lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="1840c-109">The corresponding **DML_RESAMPLE_GRAD_OPERATOR_DESC** would perform the following.</span></span>

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

<span data-ttu-id="1840c-110">Observe que los valores de *OutputGradientTensor* representan las contribuciones ponderadas de ese elemento al *outputTensor* durante el operador **DML_RESAMPLE1_OPERATOR_DESC** original.</span><span class="sxs-lookup"><span data-stu-id="1840c-110">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original **DML_RESAMPLE1_OPERATOR_DESC** operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1840c-111">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="1840c-111">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="1840c-112">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="1840c-112">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1840c-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1840c-113">Syntax</span></span>

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a><span data-ttu-id="1840c-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="1840c-114">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="1840c-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1840c-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1840c-116">Tensor de degradado entrante.</span><span class="sxs-lookup"><span data-stu-id="1840c-116">The incoming gradient tensor.</span></span> <span data-ttu-id="1840c-117">Normalmente, esto se obtiene a partir de la salida de la repropagación de una capa anterior.</span><span class="sxs-lookup"><span data-stu-id="1840c-117">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="1840c-118">Normalmente, este tensor tendría los  mismos tamaños que la salida de la DML_RESAMPLE1_OPERATOR_DESC [en](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) el paso hacia delante.</span><span class="sxs-lookup"><span data-stu-id="1840c-118">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="1840c-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1840c-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1840c-120">Tensor de salida que contiene los degradados de propiedad pendiente.</span><span class="sxs-lookup"><span data-stu-id="1840c-120">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="1840c-121">Normalmente, este tensor tendría los  mismos tamaños que la entrada del DML_RESAMPLE1_OPERATOR_DESC [correspondiente](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) en el paso hacia delante.</span><span class="sxs-lookup"><span data-stu-id="1840c-121">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`InterpolationMode`

<span data-ttu-id="1840c-122">Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="1840c-122">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="1840c-123">Vea *InterpolationMode* en [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="1840c-123">See *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`DimensionCount`

<span data-ttu-id="1840c-124">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="1840c-124">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="1840c-125">Número de elementos de las *matrices Scales*, *InputPixelOffsets* y *OutputPixelOffsets.*</span><span class="sxs-lookup"><span data-stu-id="1840c-125">The number of elements in the *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* arrays.</span></span> <span data-ttu-id="1840c-126">Este valor debe ser igual *al dimensioncount* proporcionado en *InputGradientTensor* y *OutputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="1840c-126">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`Scales`

<span data-ttu-id="1840c-127">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="1840c-127">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="1840c-128">Vea *Escalas* en [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="1840c-128">See *Scales* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`InputPixelOffsets`

<span data-ttu-id="1840c-129">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="1840c-129">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="1840c-130">Vea *InputPixelOffsets* en [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="1840c-130">See *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`OutputPixelOffsets`

<span data-ttu-id="1840c-131">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="1840c-131">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="1840c-132">Vea *OutputPixelOffsets* en [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="1840c-132">See *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="1840c-133">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="1840c-133">Availability</span></span>
<span data-ttu-id="1840c-134">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="1840c-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="1840c-135">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="1840c-135">Tensor constraints</span></span>
<span data-ttu-id="1840c-136">*InputGradientTensor* y *OutputGradientTensor* deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="1840c-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="1840c-137">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="1840c-137">Tensor support</span></span>
| <span data-ttu-id="1840c-138">Tensor</span><span class="sxs-lookup"><span data-stu-id="1840c-138">Tensor</span></span> | <span data-ttu-id="1840c-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="1840c-139">Kind</span></span> | <span data-ttu-id="1840c-140">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="1840c-140">Supported dimension counts</span></span> | <span data-ttu-id="1840c-141">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="1840c-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="1840c-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="1840c-142">InputGradientTensor</span></span> | <span data-ttu-id="1840c-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="1840c-143">Input</span></span> | <span data-ttu-id="1840c-144">4</span><span class="sxs-lookup"><span data-stu-id="1840c-144">4</span></span> | <span data-ttu-id="1840c-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="1840c-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="1840c-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="1840c-146">OutputGradientTensor</span></span> | <span data-ttu-id="1840c-147">Resultados</span><span class="sxs-lookup"><span data-stu-id="1840c-147">Output</span></span> | <span data-ttu-id="1840c-148">4</span><span class="sxs-lookup"><span data-stu-id="1840c-148">4</span></span> | <span data-ttu-id="1840c-149">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="1840c-149">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="1840c-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1840c-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1840c-151">**Header**</span><span class="sxs-lookup"><span data-stu-id="1840c-151">**Header**</span></span> | <span data-ttu-id="1840c-152">directml.h</span><span class="sxs-lookup"><span data-stu-id="1840c-152">directml.h</span></span> |