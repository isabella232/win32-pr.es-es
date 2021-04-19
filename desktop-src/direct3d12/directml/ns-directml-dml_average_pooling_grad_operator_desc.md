---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Calcula los degradados de propagación de la memoria para la agrupación promedio (vea [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
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
ms.openlocfilehash: 79a43e93f504e8d6f36553a4f672ef7e5845610f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721231"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="b43eb-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="b43eb-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b43eb-104">Calcula los degradados de propagación de la memoria para la agrupación promedio (vea [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="b43eb-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="b43eb-105">Considere una **DML_AVERAGE_POOLING_OPERATOR_DESC** 2x2, sin relleno y un paso 1, que realiza lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="b43eb-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="b43eb-106">Cada ventana de 2x2 del tensores de entrada se calcula como promedio para generar un elemento de la salida (lectura de ceros para los elementos más allá del borde).</span><span class="sxs-lookup"><span data-stu-id="b43eb-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="b43eb-107">A continuación se muestra un ejemplo de la salida de **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** determinados parámetros similares.</span><span class="sxs-lookup"><span data-stu-id="b43eb-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="b43eb-108">Observe que los valores de *OutputGradientTensor* representan las contribuciones ponderadas de ese elemento a la *OutputTensor* durante el operador de [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) original.</span><span class="sxs-lookup"><span data-stu-id="b43eb-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b43eb-109">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="b43eb-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="b43eb-110">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b43eb-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b43eb-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b43eb-111">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="b43eb-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="b43eb-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="b43eb-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b43eb-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b43eb-114">Tensores de degradado entrante.</span><span class="sxs-lookup"><span data-stu-id="b43eb-114">The incoming gradient tensor.</span></span> <span data-ttu-id="b43eb-115">Normalmente se obtiene a partir de la salida de la propagación de una capa anterior.</span><span class="sxs-lookup"><span data-stu-id="b43eb-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="b43eb-116">Normalmente, este tensores tendría el mismo tamaño que la *salida* de la [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) correspondiente en el paso de avance.</span><span class="sxs-lookup"><span data-stu-id="b43eb-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="b43eb-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b43eb-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b43eb-118">Tensores de salida que contiene los degradados retropagados.</span><span class="sxs-lookup"><span data-stu-id="b43eb-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="b43eb-119">Normalmente, este tensores tendría el mismo tamaño que la *entrada* del [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) correspondiente en el paso de avance.</span><span class="sxs-lookup"><span data-stu-id="b43eb-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="b43eb-120">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b43eb-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b43eb-121">El número de elementos de las matrices de los *progresos*, *Windows*, *StartPadding* y *EndPadding* .</span><span class="sxs-lookup"><span data-stu-id="b43eb-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="b43eb-122">Este valor debe ser igual al número de dimensiones espaciales.</span><span class="sxs-lookup"><span data-stu-id="b43eb-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="b43eb-123">El número de dimensiones espaciales es 2 si se proporcionan los contadores 4D o 3 si se proporcionan los diez.</span><span class="sxs-lookup"><span data-stu-id="b43eb-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="b43eb-124">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="b43eb-124">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="b43eb-125">Vea los *avances* en [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b43eb-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="b43eb-126">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="b43eb-126">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="b43eb-127">Consulte *Windows* en [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b43eb-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="b43eb-128">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="b43eb-128">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="b43eb-129">Consulte *StartPadding* en [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b43eb-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="b43eb-130">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="b43eb-130">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="b43eb-131">Consulte *EndPadding* en [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b43eb-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="b43eb-132">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="b43eb-132">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="b43eb-133">Consulte *IncludePadding* en [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b43eb-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="b43eb-134">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="b43eb-134">Availability</span></span>
<span data-ttu-id="b43eb-135">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="b43eb-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b43eb-136">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="b43eb-136">Tensor constraints</span></span>
<span data-ttu-id="b43eb-137">*InputGradientTensor* y *OutputGradientTensor* deben tener el mismo *DataType* y *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="b43eb-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b43eb-138">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="b43eb-138">Tensor support</span></span>
| <span data-ttu-id="b43eb-139">Tensores</span><span class="sxs-lookup"><span data-stu-id="b43eb-139">Tensor</span></span> | <span data-ttu-id="b43eb-140">Clase</span><span class="sxs-lookup"><span data-stu-id="b43eb-140">Kind</span></span> | <span data-ttu-id="b43eb-141">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="b43eb-141">Supported dimension counts</span></span> | <span data-ttu-id="b43eb-142">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="b43eb-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b43eb-143">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="b43eb-143">InputGradientTensor</span></span> | <span data-ttu-id="b43eb-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="b43eb-144">Input</span></span> | <span data-ttu-id="b43eb-145">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="b43eb-145">4 to 5</span></span> | <span data-ttu-id="b43eb-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b43eb-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="b43eb-147">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="b43eb-147">OutputGradientTensor</span></span> | <span data-ttu-id="b43eb-148">Output</span><span class="sxs-lookup"><span data-stu-id="b43eb-148">Output</span></span> | <span data-ttu-id="b43eb-149">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="b43eb-149">4 to 5</span></span> | <span data-ttu-id="b43eb-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b43eb-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="b43eb-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b43eb-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b43eb-152">**Header**</span><span class="sxs-lookup"><span data-stu-id="b43eb-152">**Header**</span></span> | <span data-ttu-id="b43eb-153">directml. h</span><span class="sxs-lookup"><span data-stu-id="b43eb-153">directml.h</span></span> |