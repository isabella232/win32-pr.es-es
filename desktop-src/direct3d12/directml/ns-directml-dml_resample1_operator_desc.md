---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Vuelve a muestrear los elementos del origen al tensores de destino, usando los factores de escala para calcular el tamaño de tensores de destino. Puede usar un modo de interpolación lineal o más cercano.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
- DML_RESAMPLE1_OPERATOR_DESC
- directml/DML_RESAMPLE1_OPERATOR_DESC
ms.openlocfilehash: 669e828c4d8376e081ef6638aba4a13d517afd88
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721268"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a><span data-ttu-id="5dfc9-104">DML_RESAMPLE1_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="5dfc9-104">DML_RESAMPLE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="5dfc9-105">Vuelve a muestrear los elementos del origen al tensores de destino, usando los factores de escala para calcular el tamaño de tensores de destino.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-105">Resamples elements from the source to the destination tensor, using the scale factors to compute the destination tensor size.</span></span> <span data-ttu-id="5dfc9-106">Puede usar un modo de interpolación lineal o más cercano.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-106">You can use a linear or nearest-neighbor interpolation mode.</span></span> <span data-ttu-id="5dfc9-107">El operador admite la interpolación en varias dimensiones, no solo en 2D.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-107">The operator supports interpolation across multiple dimensions, not just 2D.</span></span> <span data-ttu-id="5dfc9-108">Por lo tanto, puede mantener el mismo tamaño espacial, pero interpolar entre canales o por lotes.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-108">So you can keep the same spatial size, but interpolate across channels or across batches.</span></span> <span data-ttu-id="5dfc9-109">La relación entre las coordenadas de entrada y salida es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-109">The relationship between the input and output coordinates is the following.</span></span>

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> <span data-ttu-id="5dfc9-110">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="5dfc9-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="5dfc9-111">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="5dfc9-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5dfc9-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5dfc9-112">Syntax</span></span>
```cpp
struct DML_RESAMPLE1_OPERATOR_DESC {
  const DML_TENSOR_DESC  *InputTensor;
  const DML_TENSOR_DESC  *OutputTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT                   DimensionCount;
  const FLOAT            *Scales;
  const FLOAT            *InputPixelOffsets;
  const FLOAT            *OutputPixelOffsets;
};
```



## <a name="members"></a><span data-ttu-id="5dfc9-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="5dfc9-113">Members</span></span>

`InputTensor`

<span data-ttu-id="5dfc9-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5dfc9-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5dfc9-115">Tensores que contiene los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-115">The tensor containing the input data.</span></span>


`OutputTensor`

<span data-ttu-id="5dfc9-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5dfc9-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5dfc9-117">Tensores en el que se van a escribir los datos de salida.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-117">The tensor to write the output data to.</span></span>


`InterpolationMode`

<span data-ttu-id="5dfc9-118">Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="5dfc9-118">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="5dfc9-119">Este campo determina el tipo de interpolación que se usa para elegir los píxeles de salida.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-119">This field determines the kind of interpolation used to choose output pixels.</span></span>

- <span data-ttu-id="5dfc9-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span></span> <span data-ttu-id="5dfc9-121">Usa el algoritmo *vecino más cercano* , que elige el elemento de entrada más cercano al centro de píxeles correspondiente para cada elemento de salida.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-121">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>

- <span data-ttu-id="5dfc9-122">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-122">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="5dfc9-123">Usa el algoritmo *Quadrilinear* , que calcula el elemento Output mediante la media ponderada de los dos elementos de entrada vecinos más cercanos por dimensión.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-123">Uses the *Quadrilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="5dfc9-124">Dado que se pueden volver a muestrear las 4 dimensiones, el promedio ponderado se calcula en un total de 16 elementos de entrada para cada elemento de salida.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-124">Since all 4 dimensions can be resampled, the weighted average is computed on a total of 16 input elements for each output element.</span></span>


`DimensionCount`

<span data-ttu-id="5dfc9-125">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5dfc9-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="5dfc9-126">El número de valores de las matrices que se *escalan*, *InputPixelOffsets* y *OutputPixelOffsets* apuntan a.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-126">The number of values in the arrays that *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* point to.</span></span> <span data-ttu-id="5dfc9-127">Este valor debe coincidir con el recuento de dimensiones de *InputTensor* y *OutputTensor*, que tiene que ser 4.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-127">This value must match the dimension count of *InputTensor* and *OutputTensor*, which has to be 4.</span></span>


`Scales`

<span data-ttu-id="5dfc9-128">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="5dfc9-128">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="5dfc9-129">Escalas que se van a aplicar al volver a muestrear la entrada, donde las escalas > 1 escalan verticalmente la imagen y se escalan < 1 reducir verticalmente la imagen de esa dimensión.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-129">The scales to apply when resampling the input, where scales > 1 scale up the image and scales < 1 scale down the image for that dimension.</span></span> <span data-ttu-id="5dfc9-130">Tenga en cuenta que no es necesario que las escalas sean exactas `OutputSize / InputSize` .</span><span class="sxs-lookup"><span data-stu-id="5dfc9-130">Note that the scales don't need to be exactly `OutputSize / InputSize`.</span></span> <span data-ttu-id="5dfc9-131">Si la entrada después del escalado es mayor que el límite de salida, se recortará en el tamaño de salida.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-131">If the input after scaling is larger than the output bound, then we crop it to the output size.</span></span> <span data-ttu-id="5dfc9-132">Por otro lado, si la entrada después del escalado es menor que el límite de salida, se fijan los bordes de salida.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-132">On the other hand, if the input after scaling is smaller than the output bound, the output edges are clamped.</span></span>


`InputPixelOffsets`

<span data-ttu-id="5dfc9-133">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="5dfc9-133">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="5dfc9-134">Desplazamientos que se van a aplicar a los píxeles de entrada antes de volver a muestrear.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-134">The offsets to apply to the input pixels before resampling.</span></span> <span data-ttu-id="5dfc9-135">Cuando este valor es `0` , se usa la esquina superior izquierda del píxel en lugar de su centro, que normalmente no proporcionará el resultado esperado.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-135">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="5dfc9-136">Para volver a muestrear la imagen mediante el centro de los píxeles y obtener el mismo comportamiento que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), este valor debe ser `0.5` .</span><span class="sxs-lookup"><span data-stu-id="5dfc9-136">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `0.5`.</span></span>


`OutputPixelOffsets`

<span data-ttu-id="5dfc9-137">Tipo: \_ tamaño de campo \_ \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="5dfc9-137">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="5dfc9-138">Desplazamientos que se van a aplicar a los píxeles de salida después del remuestreo.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-138">The offsets to apply to the output pixels after resampling.</span></span> <span data-ttu-id="5dfc9-139">Cuando este valor es `0` , se usa la esquina superior izquierda del píxel en lugar de su centro, que normalmente no proporcionará el resultado esperado.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-139">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="5dfc9-140">Para volver a muestrear la imagen mediante el centro de los píxeles y obtener el mismo comportamiento que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), este valor debe ser `-0.5` .</span><span class="sxs-lookup"><span data-stu-id="5dfc9-140">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `-0.5`.</span></span>


## <a name="remarks"></a><span data-ttu-id="5dfc9-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5dfc9-141">Remarks</span></span>
<span data-ttu-id="5dfc9-142">Cuando el valor de *InputPixelOffsets* se establece en 0,5 y el valor de *OutputPixelOffsets* se establece en-0,5, este operador es equivalente a [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="5dfc9-142">When the *InputPixelOffsets* are set to 0.5, and the *OutputPixelOffsets* are set to -0.5, this operator is equivalent to [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="5dfc9-143">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="5dfc9-143">Availability</span></span>
<span data-ttu-id="5dfc9-144">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="5dfc9-144">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5dfc9-145">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="5dfc9-145">Tensor constraints</span></span>
<span data-ttu-id="5dfc9-146">*InputTensor* y *OutputTensor* deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="5dfc9-146">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5dfc9-147">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="5dfc9-147">Tensor support</span></span>
| <span data-ttu-id="5dfc9-148">Tensores</span><span class="sxs-lookup"><span data-stu-id="5dfc9-148">Tensor</span></span> | <span data-ttu-id="5dfc9-149">Clase</span><span class="sxs-lookup"><span data-stu-id="5dfc9-149">Kind</span></span> | <span data-ttu-id="5dfc9-150">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="5dfc9-150">Supported dimension counts</span></span> | <span data-ttu-id="5dfc9-151">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="5dfc9-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5dfc9-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5dfc9-152">InputTensor</span></span> | <span data-ttu-id="5dfc9-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="5dfc9-153">Input</span></span> | <span data-ttu-id="5dfc9-154">4</span><span class="sxs-lookup"><span data-stu-id="5dfc9-154">4</span></span> | <span data-ttu-id="5dfc9-155">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5dfc9-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5dfc9-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5dfc9-156">OutputTensor</span></span> | <span data-ttu-id="5dfc9-157">Output</span><span class="sxs-lookup"><span data-stu-id="5dfc9-157">Output</span></span> | <span data-ttu-id="5dfc9-158">4</span><span class="sxs-lookup"><span data-stu-id="5dfc9-158">4</span></span> | <span data-ttu-id="5dfc9-159">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5dfc9-159">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="5dfc9-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dfc9-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5dfc9-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="5dfc9-161">**Header**</span></span> | <span data-ttu-id="5dfc9-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="5dfc9-162">directml.h</span></span> |