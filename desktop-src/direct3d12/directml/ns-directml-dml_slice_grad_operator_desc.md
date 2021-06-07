---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Calcula los degradados de apropagación de backpropagation para Slice [(consulte DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
helpviewer_keywords:
- DML_SLICE_GRAD_OPERATOR_DESC
- DML_SLICE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_SLICE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_SLICE_GRAD_OPERATOR_DESC, DML_SLICE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
- directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
ms.openlocfilehash: a22efe9b0b74f5fdc7b498b97784086f40f243b9
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417988"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="4d7ad-103">DML_SLICE_GRAD_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="4d7ad-103">DML_SLICE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="4d7ad-104">Calcula los degradados de apropagación de backpropagation para Slice [(consulte DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="4d7ad-104">Computes backpropagation gradients for Slice (see [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span></span>

<span data-ttu-id="4d7ad-105">Recuerde que [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extrae una subregión de un tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-105">Recall that [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extracts a subregion of an input tensor.</span></span> <span data-ttu-id="4d7ad-106">Dado un *inputGradientTensor* con los  mismos tamaños que la salida de un **DML_SLICE1_OPERATOR_DESC** equivalente, este operador genera  un *outputGradientTensor* con los mismos tamaños que la **entrada de DML_SLICE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_SLICE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of **DML_SLICE1_OPERATOR_DESC**.</span></span> <span data-ttu-id="4d7ad-107">Los elementos segmentados se propagan a la salida y todos los demás elementos se establecen en 0.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-107">The sliced elements are propagated to the output, and all other elements are set to 0.</span></span>

<span data-ttu-id="4d7ad-108">Por ejemplo, considere **una** DML_SLICE1_OPERATOR_DESC que extrae los siguientes elementos de un tensor:</span><span class="sxs-lookup"><span data-stu-id="4d7ad-108">As an example, consider a **DML_SLICE1_OPERATOR_DESC** that extracts the following elements from a tensor:</span></span>

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

<span data-ttu-id="4d7ad-109">Si se proporcionan los mismos *Strides de tamaños inputWindowOffsets* que en el ejemplo anterior, este operador realizaría /  /  la transformación siguiente.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-109">If provided the same *InputWindowOffsets*/*Sizes*/*Strides* as in the above example, this operator would then perform the following transform.</span></span>

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> <span data-ttu-id="4d7ad-110">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="4d7ad-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="4d7ad-111">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="4d7ad-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7ad-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d7ad-112">Syntax</span></span>

```cpp
struct DML_SLICE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* InputWindowOffsets;
  _Field_size_(DimensionCount) const UINT* InputWindowSizes;
  _Field_size_(DimensionCount) const INT* InputWindowStrides;
};
```

## <a name="members"></a><span data-ttu-id="4d7ad-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d7ad-113">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="4d7ad-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4d7ad-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4d7ad-115">Tensor de degradado entrante.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-115">The incoming gradient tensor.</span></span> <span data-ttu-id="4d7ad-116">Esto se obtiene normalmente a partir de la salida de la repropagación de una capa anterior.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="4d7ad-117">Normalmente, este tensor tendría los  mismos tamaños que la salida de la DML_SLICE1_OPERATOR_DESC [correspondiente](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) en el paso hacia delante.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-117">Typically, this tensor would have the same sizes as the *output* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="4d7ad-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4d7ad-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4d7ad-119">Tensor de salida que contiene los degradados de propiedad pendiente.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="4d7ad-120">Normalmente, este tensor tendría los  mismos tamaños que la entrada de la DML_SLICE1_OPERATOR_DESC [correspondiente](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) en el paso hacia delante.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-120">Typically, this tensor would have the same sizes as the *input* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="4d7ad-121">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4d7ad-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4d7ad-122">Número de elementos de las *matrices InputWindowOffsets,* *InputWindowSizes* y *InputWindowStrides.*</span><span class="sxs-lookup"><span data-stu-id="4d7ad-122">The number of elements in the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="4d7ad-123">Este valor debe ser igual *al dimensioncount* proporcionado en *InputGradientTensor* y *OutputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-123">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`InputWindowOffsets`

<span data-ttu-id="4d7ad-124">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4d7ad-124">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4d7ad-125">Vea *InputWindowOffsets* en [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="4d7ad-125">See *InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowSizes`

<span data-ttu-id="4d7ad-126">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4d7ad-126">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4d7ad-127">Vea *InputWindowSizes* en [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="4d7ad-127">See *InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowStrides`

<span data-ttu-id="4d7ad-128">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4d7ad-128">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4d7ad-129">Vea *InputWindowStrides* en [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="4d7ad-129">See *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

<span data-ttu-id="4d7ad-130">Tenga en cuenta **que DML_SLICE1_OPERATOR_DESC**, este operador requiere avances distintos de cero.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-130">Note that unlike **DML_SLICE1_OPERATOR_DESC**, this operator requires non-zero strides.</span></span> <span data-ttu-id="4d7ad-131">Esto se debe a que, con un paso cero, es ambiguo en cuanto a qué elemento de entrada se debe asignar a cada elemento de salida y, por tanto, no se puede realizar la repropagación.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-131">That's because with a zero stride, it's ambiguous as to which input element should map to each output element, and therefore backpropagation can't be performed.</span></span> <span data-ttu-id="4d7ad-132">Al **DML_SLICE1_OPERATOR_DESC**, los avances negativos invierten la dirección de la ventana de entrada a lo largo de ese eje.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-132">Like **DML_SLICE1_OPERATOR_DESC**, negative strides flip the input window direction along that axis.</span></span>

## <a name="availability"></a><span data-ttu-id="4d7ad-133">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="4d7ad-133">Availability</span></span>
<span data-ttu-id="4d7ad-134">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="4d7ad-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4d7ad-135">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="4d7ad-135">Tensor constraints</span></span>
<span data-ttu-id="4d7ad-136">*InputGradientTensor* y *OutputGradientTensor* deben tener los mismos *DataType* y *DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="4d7ad-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4d7ad-137">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="4d7ad-137">Tensor support</span></span>
| <span data-ttu-id="4d7ad-138">Tensor</span><span class="sxs-lookup"><span data-stu-id="4d7ad-138">Tensor</span></span> | <span data-ttu-id="4d7ad-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d7ad-139">Kind</span></span> | <span data-ttu-id="4d7ad-140">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="4d7ad-140">Supported dimension counts</span></span> | <span data-ttu-id="4d7ad-141">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="4d7ad-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4d7ad-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="4d7ad-142">InputGradientTensor</span></span> | <span data-ttu-id="4d7ad-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="4d7ad-143">Input</span></span> | <span data-ttu-id="4d7ad-144">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="4d7ad-144">1 to 8</span></span> | <span data-ttu-id="4d7ad-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4d7ad-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="4d7ad-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="4d7ad-146">OutputGradientTensor</span></span> | <span data-ttu-id="4d7ad-147">Resultados</span><span class="sxs-lookup"><span data-stu-id="4d7ad-147">Output</span></span> | <span data-ttu-id="4d7ad-148">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="4d7ad-148">1 to 8</span></span> | <span data-ttu-id="4d7ad-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4d7ad-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="4d7ad-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d7ad-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4d7ad-151">**Header**</span><span class="sxs-lookup"><span data-stu-id="4d7ad-151">**Header**</span></span> | <span data-ttu-id="4d7ad-152">directml.h</span><span class="sxs-lookup"><span data-stu-id="4d7ad-152">directml.h</span></span> |