---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Calcula los degradados de propagación de la misma para el segmento (vea [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
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
ms.openlocfilehash: 63ea67454965d976247c3cdd50aa183f6a676138
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721249"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="a174f-103">DML_SLICE_GRAD_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="a174f-103">DML_SLICE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="a174f-104">Calcula los degradados de propagación de la misma para el segmento (vea [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="a174f-104">Computes backpropagation gradients for Slice (see [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span></span>

<span data-ttu-id="a174f-105">Recuerde que [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extrae una subregión de una tensores de entrada.</span><span class="sxs-lookup"><span data-stu-id="a174f-105">Recall that [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extracts a subregion of an input tensor.</span></span> <span data-ttu-id="a174f-106">Dado un *InputGradientTensor* con los mismos tamaños que la *salida* de una **DML_SLICE1_OPERATOR_DESC** equivalente, este operador genera una *OutputGradientTensor* con los mismos tamaños que la *entrada* de **DML_SLICE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="a174f-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_SLICE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of **DML_SLICE1_OPERATOR_DESC**.</span></span> <span data-ttu-id="a174f-107">Los elementos segmentados se propagan a la salida y todos los demás elementos se establecen en 0.</span><span class="sxs-lookup"><span data-stu-id="a174f-107">The sliced elements are propagated to the output, and all other elements are set to 0.</span></span>

<span data-ttu-id="a174f-108">Como ejemplo, considere un **DML_SLICE1_OPERATOR_DESC** que extrae los siguientes elementos de un tensores:</span><span class="sxs-lookup"><span data-stu-id="a174f-108">As an example, consider a **DML_SLICE1_OPERATOR_DESC** that extracts the following elements from a tensor:</span></span>

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

<span data-ttu-id="a174f-109">Si se proporciona el mismo / *tamaño* / de InputWindowOffsets,*al* igual que en el ejemplo anterior, este operador llevaría a cabo la transformación siguiente.</span><span class="sxs-lookup"><span data-stu-id="a174f-109">If provided the same *InputWindowOffsets*/*Sizes*/*Strides* as in the above example, this operator would then perform the following transform.</span></span>

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> <span data-ttu-id="a174f-110">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="a174f-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="a174f-111">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="a174f-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a174f-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a174f-112">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="a174f-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="a174f-113">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="a174f-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a174f-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a174f-115">Tensores de degradado entrante.</span><span class="sxs-lookup"><span data-stu-id="a174f-115">The incoming gradient tensor.</span></span> <span data-ttu-id="a174f-116">Normalmente se obtiene a partir de la salida de la propagación de una capa anterior.</span><span class="sxs-lookup"><span data-stu-id="a174f-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="a174f-117">Normalmente, este tensores tendría el mismo tamaño que la *salida* de la [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) correspondiente en el paso de avance.</span><span class="sxs-lookup"><span data-stu-id="a174f-117">Typically, this tensor would have the same sizes as the *output* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="a174f-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a174f-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a174f-119">Tensores de salida que contiene los degradados retropagados.</span><span class="sxs-lookup"><span data-stu-id="a174f-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="a174f-120">Normalmente, este tensores tendría el mismo tamaño que la *entrada* de la [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) correspondiente en el paso de avance.</span><span class="sxs-lookup"><span data-stu-id="a174f-120">Typically, this tensor would have the same sizes as the *input* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="a174f-121">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a174f-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="a174f-122">El número de elementos de las matrices *InputWindowOffsets*, *InputWindowSizes* y *InputWindowStrides* .</span><span class="sxs-lookup"><span data-stu-id="a174f-122">The number of elements in the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="a174f-123">Este valor debe ser igual al *DimensionCount* proporcionado en *InputGradientTensor* y *OutputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="a174f-123">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`InputWindowOffsets`

<span data-ttu-id="a174f-124">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="a174f-124">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="a174f-125">Consulte *InputWindowOffsets* en [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="a174f-125">See *InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowSizes`

<span data-ttu-id="a174f-126">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="a174f-126">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="a174f-127">Consulte *InputWindowSizes* en [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="a174f-127">See *InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowStrides`

<span data-ttu-id="a174f-128">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="a174f-128">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="a174f-129">Consulte *InputWindowStrides* en [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="a174f-129">See *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

<span data-ttu-id="a174f-130">Tenga en cuenta que, a diferencia de **DML_SLICE1_OPERATOR_DESC**, este operador requiere progresas distintos de cero.</span><span class="sxs-lookup"><span data-stu-id="a174f-130">Note that unlike **DML_SLICE1_OPERATOR_DESC**, this operator requires non-zero strides.</span></span> <span data-ttu-id="a174f-131">Esto se debe a que, con un intervalo de cero, es ambiguo en qué elemento de entrada se debe asignar a cada elemento de salida y, por tanto, no se puede realizar la propagación.</span><span class="sxs-lookup"><span data-stu-id="a174f-131">That's because with a zero stride, it's ambiguous as to which input element should map to each output element, and therefore backpropagation can't be performed.</span></span> <span data-ttu-id="a174f-132">Como **DML_SLICE1_OPERATOR_DESC**, los progresos negativos voltean la dirección de la ventana de entrada a lo largo de ese eje.</span><span class="sxs-lookup"><span data-stu-id="a174f-132">Like **DML_SLICE1_OPERATOR_DESC**, negative strides flip the input window direction along that axis.</span></span>

## <a name="availability"></a><span data-ttu-id="a174f-133">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="a174f-133">Availability</span></span>
<span data-ttu-id="a174f-134">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="a174f-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a174f-135">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="a174f-135">Tensor constraints</span></span>
<span data-ttu-id="a174f-136">*InputGradientTensor* y *OutputGradientTensor* deben tener el mismo *DataType* y *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="a174f-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a174f-137">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="a174f-137">Tensor support</span></span>
| <span data-ttu-id="a174f-138">Tensores</span><span class="sxs-lookup"><span data-stu-id="a174f-138">Tensor</span></span> | <span data-ttu-id="a174f-139">Clase</span><span class="sxs-lookup"><span data-stu-id="a174f-139">Kind</span></span> | <span data-ttu-id="a174f-140">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="a174f-140">Supported dimension counts</span></span> | <span data-ttu-id="a174f-141">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="a174f-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a174f-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="a174f-142">InputGradientTensor</span></span> | <span data-ttu-id="a174f-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="a174f-143">Input</span></span> | <span data-ttu-id="a174f-144">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a174f-144">1 to 8</span></span> | <span data-ttu-id="a174f-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a174f-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a174f-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="a174f-146">OutputGradientTensor</span></span> | <span data-ttu-id="a174f-147">Output</span><span class="sxs-lookup"><span data-stu-id="a174f-147">Output</span></span> | <span data-ttu-id="a174f-148">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a174f-148">1 to 8</span></span> | <span data-ttu-id="a174f-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a174f-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="a174f-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a174f-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a174f-151">**Header**</span><span class="sxs-lookup"><span data-stu-id="a174f-151">**Header**</span></span> | <span data-ttu-id="a174f-152">directml. h</span><span class="sxs-lookup"><span data-stu-id="a174f-152">directml.h</span></span> |