---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Realiza una circunvolución del *FilterTensor* con *InputTensor*. Este operador realiza una circunvolución hacia delante en los datos enteros.
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: c16690ea1e3049ffeba398bbbaca2003f965a832
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721289"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="19e49-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="19e49-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="19e49-105">Realiza una circunvolución del *FilterTensor* con *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="19e49-105">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="19e49-106">Este operador realiza una circunvolución hacia delante en los datos enteros.</span><span class="sxs-lookup"><span data-stu-id="19e49-106">This operator performs forward convolution on integer data.</span></span> <span data-ttu-id="19e49-107">Los separadores de punto cero opcionales también se pueden usar para restar los valores de punto cero de la entrada y filtrar tensores.</span><span class="sxs-lookup"><span data-stu-id="19e49-107">Optional zero point tensors can also be used to subtract zero point values from the input and filter tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19e49-108">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="19e49-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="19e49-109">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="19e49-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="19e49-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19e49-110">Syntax</span></span>
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```

## <a name="members"></a><span data-ttu-id="19e49-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="19e49-111">Members</span></span>

`InputTensor`

<span data-ttu-id="19e49-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="19e49-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="19e49-113">Tensores que contiene los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="19e49-113">A tensor containing the input data.</span></span> <span data-ttu-id="19e49-114">Las dimensiones esperadas de *InputTensor* son `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="19e49-114">The expected dimensions of the *InputTensor* are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="19e49-115">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="19e49-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="19e49-116">Un tensores opcional que contiene los datos de punto cero de entrada.</span><span class="sxs-lookup"><span data-stu-id="19e49-116">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="19e49-117">Las dimensiones esperadas de *InputZeroPointTensor* son `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="19e49-117">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span>


`FilterTensor`

<span data-ttu-id="19e49-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="19e49-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="19e49-119">Tensores que contiene los datos del filtro.</span><span class="sxs-lookup"><span data-stu-id="19e49-119">A tensor containing the filter data.</span></span> <span data-ttu-id="19e49-120">Las dimensiones esperadas de *FilterTensor* son `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="19e49-120">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="19e49-121">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="19e49-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="19e49-122">Un tensores opcional que contiene los datos del punto cero del filtro.</span><span class="sxs-lookup"><span data-stu-id="19e49-122">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="19e49-123">Las dimensiones esperadas de *FilterZeroPointTensor* son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores, o `{ 1, OutputChannelCount, 1, 1 }` si se requiere la cuantificación por canal.</span><span class="sxs-lookup"><span data-stu-id="19e49-123">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per-channel quantization is required.</span></span>


`OutputTensor`

<span data-ttu-id="19e49-124">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="19e49-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="19e49-125">Tensores en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="19e49-125">The tensor to write the results to.</span></span> <span data-ttu-id="19e49-126">Las dimensiones esperadas de *OutputTensor* son `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="19e49-126">The expected dimensions of the *OutputTensor* are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="19e49-127">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="19e49-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="19e49-128">El número de dimensiones espaciales para la operación de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="19e49-128">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="19e49-129">Las dimensiones espaciales son las dimensiones inferiores del *FilterTensor* de convolución.</span><span class="sxs-lookup"><span data-stu-id="19e49-129">Spatial dimensions are the lower dimensions of the convolution *FilterTensor*.</span></span> <span data-ttu-id="19e49-130">Este valor también determina el tamaño de las matrices de los *progresos*, *Dilations*, *StartPadding* y *EndPadding* .</span><span class="sxs-lookup"><span data-stu-id="19e49-130">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="19e49-131">Solo se admite un valor de 2.</span><span class="sxs-lookup"><span data-stu-id="19e49-131">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="19e49-132">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="19e49-132">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="19e49-133">Una matriz que contiene los progresos de la operación de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="19e49-133">An array containing the strides of the convolution operation.</span></span> <span data-ttu-id="19e49-134">Estos avances se aplican al filtro de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="19e49-134">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="19e49-135">Son independientes de los progresos de tensores incluidos en [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="19e49-135">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="19e49-136">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="19e49-136">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="19e49-137">Una matriz que contiene el dilations de la operación de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="19e49-137">An array containing the dilations of the convolution operation.</span></span> <span data-ttu-id="19e49-138">Dilations son los progresos aplicados a los elementos del kernel de filtro.</span><span class="sxs-lookup"><span data-stu-id="19e49-138">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="19e49-139">Esto tiene el efecto de simular un kernel de filtro mayor al rellenar los elementos de kernel del filtro interno con ceros.</span><span class="sxs-lookup"><span data-stu-id="19e49-139">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="19e49-140">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="19e49-140">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="19e49-141">Una matriz que contiene los valores de relleno que se van a aplicar al principio de cada dimensión espacial del filtro y tensores de entrada de la operación de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="19e49-141">An array containing the padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="19e49-142">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="19e49-142">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="19e49-143">Una matriz que contiene los valores de relleno que se van a aplicar al final de cada dimensión espacial del filtro y tensores de entrada de la operación de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="19e49-143">An array containing the padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="19e49-144">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="19e49-144">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="19e49-145">El número de grupos en los que se va a dividir la operación de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="19e49-145">The number of groups which to divide the convolution operation up into.</span></span> <span data-ttu-id="19e49-146">*GroupCount* se puede usar para lograr una circunvolución de nivel de profundidad estableciendo el valor de *GroupCount* igual al número de canales de entrada.</span><span class="sxs-lookup"><span data-stu-id="19e49-146">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="19e49-147">Esto divide la circunvolución en una circunvolución independiente por canal de entrada.</span><span class="sxs-lookup"><span data-stu-id="19e49-147">This divides the convolution up into a separate convolution per input channel.</span></span>

## <a name="availability"></a><span data-ttu-id="19e49-148">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="19e49-148">Availability</span></span>
<span data-ttu-id="19e49-149">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="19e49-149">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="19e49-150">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="19e49-150">Tensor constraints</span></span>
* <span data-ttu-id="19e49-151">*FilterTensor* y *FilterZeroPointTensor* deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="19e49-151">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="19e49-152">*InputTensor* y *InputZeroPointTensor* deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="19e49-152">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="19e49-153">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="19e49-153">Tensor support</span></span>
| <span data-ttu-id="19e49-154">Tensores</span><span class="sxs-lookup"><span data-stu-id="19e49-154">Tensor</span></span> | <span data-ttu-id="19e49-155">Clase</span><span class="sxs-lookup"><span data-stu-id="19e49-155">Kind</span></span> | <span data-ttu-id="19e49-156">Dimensions</span><span class="sxs-lookup"><span data-stu-id="19e49-156">Dimensions</span></span> | <span data-ttu-id="19e49-157">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="19e49-157">Supported dimension counts</span></span> | <span data-ttu-id="19e49-158">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="19e49-158">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="19e49-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="19e49-159">InputTensor</span></span> | <span data-ttu-id="19e49-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="19e49-160">Input</span></span> | <span data-ttu-id="19e49-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="19e49-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="19e49-162">4</span><span class="sxs-lookup"><span data-stu-id="19e49-162">4</span></span> | <span data-ttu-id="19e49-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="19e49-163">INT8, UINT8</span></span> |
| <span data-ttu-id="19e49-164">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="19e49-164">InputZeroPointTensor</span></span> | <span data-ttu-id="19e49-165">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="19e49-165">Optional input</span></span> | <span data-ttu-id="19e49-166">{1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="19e49-166">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="19e49-167">4</span><span class="sxs-lookup"><span data-stu-id="19e49-167">4</span></span> | <span data-ttu-id="19e49-168">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="19e49-168">INT8, UINT8</span></span> |
| <span data-ttu-id="19e49-169">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="19e49-169">FilterTensor</span></span> | <span data-ttu-id="19e49-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="19e49-170">Input</span></span> | <span data-ttu-id="19e49-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span><span class="sxs-lookup"><span data-stu-id="19e49-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span></span> | <span data-ttu-id="19e49-172">4</span><span class="sxs-lookup"><span data-stu-id="19e49-172">4</span></span> | <span data-ttu-id="19e49-173">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="19e49-173">INT8, UINT8</span></span> |
| <span data-ttu-id="19e49-174">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="19e49-174">FilterZeroPointTensor</span></span> | <span data-ttu-id="19e49-175">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="19e49-175">Optional input</span></span> | <span data-ttu-id="19e49-176">{1, FilterZeroPointChannelCount, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="19e49-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span></span> | <span data-ttu-id="19e49-177">4</span><span class="sxs-lookup"><span data-stu-id="19e49-177">4</span></span> | <span data-ttu-id="19e49-178">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="19e49-178">INT8, UINT8</span></span> |
| <span data-ttu-id="19e49-179">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="19e49-179">OutputTensor</span></span> | <span data-ttu-id="19e49-180">Output</span><span class="sxs-lookup"><span data-stu-id="19e49-180">Output</span></span> | <span data-ttu-id="19e49-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="19e49-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="19e49-182">4</span><span class="sxs-lookup"><span data-stu-id="19e49-182">4</span></span> | <span data-ttu-id="19e49-183">INT32</span><span class="sxs-lookup"><span data-stu-id="19e49-183">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="19e49-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19e49-184">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="19e49-185">**Header**</span><span class="sxs-lookup"><span data-stu-id="19e49-185">**Header**</span></span> | <span data-ttu-id="19e49-186">directml. h</span><span class="sxs-lookup"><span data-stu-id="19e49-186">directml.h</span></span> |