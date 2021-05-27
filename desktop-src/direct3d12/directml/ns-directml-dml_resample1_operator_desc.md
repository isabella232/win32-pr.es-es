---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Vuelve a muestrear los elementos del tensor de origen al de destino, utilizando los factores de escala para calcular el tamaño del tensor de destino. Puede usar un modo de interpolación lineal o de vecino más próximo.
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
ms.openlocfilehash: 3cf5a49f5c92b835646e146b631abd18b4b19e6b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550400"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a><span data-ttu-id="6b274-104">DML_RESAMPLE1_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="6b274-104">DML_RESAMPLE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="6b274-105">Vuelve a muestrear los elementos del tensor de origen al de destino, utilizando los factores de escala para calcular el tamaño del tensor de destino.</span><span class="sxs-lookup"><span data-stu-id="6b274-105">Resamples elements from the source to the destination tensor, using the scale factors to compute the destination tensor size.</span></span> <span data-ttu-id="6b274-106">Puede usar un modo de interpolación lineal o de vecino más próximo.</span><span class="sxs-lookup"><span data-stu-id="6b274-106">You can use a linear or nearest-neighbor interpolation mode.</span></span> <span data-ttu-id="6b274-107">El operador admite la interpolación en varias dimensiones, no solo en 2D.</span><span class="sxs-lookup"><span data-stu-id="6b274-107">The operator supports interpolation across multiple dimensions, not just 2D.</span></span> <span data-ttu-id="6b274-108">Por lo tanto, puede mantener el mismo tamaño espacial, pero interpolar entre canales o lotes.</span><span class="sxs-lookup"><span data-stu-id="6b274-108">So you can keep the same spatial size, but interpolate across channels or across batches.</span></span> <span data-ttu-id="6b274-109">La relación entre las coordenadas de entrada y salida es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="6b274-109">The relationship between the input and output coordinates is the following.</span></span>

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> <span data-ttu-id="6b274-110">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="6b274-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="6b274-111">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="6b274-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b274-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b274-112">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="6b274-113">Members</span><span class="sxs-lookup"><span data-stu-id="6b274-113">Members</span></span>

`InputTensor`

<span data-ttu-id="6b274-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6b274-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6b274-115">Tensor que contiene los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="6b274-115">The tensor containing the input data.</span></span>


`OutputTensor`

<span data-ttu-id="6b274-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6b274-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6b274-117">Tensor en el que se escriben los datos de salida.</span><span class="sxs-lookup"><span data-stu-id="6b274-117">The tensor to write the output data to.</span></span>


`InterpolationMode`

<span data-ttu-id="6b274-118">Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="6b274-118">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="6b274-119">Este campo determina el tipo de interpolación que se usa para elegir los píxeles de salida.</span><span class="sxs-lookup"><span data-stu-id="6b274-119">This field determines the kind of interpolation used to choose output pixels.</span></span>

- <span data-ttu-id="6b274-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span><span class="sxs-lookup"><span data-stu-id="6b274-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span></span> <span data-ttu-id="6b274-121">Usa el *algoritmo Vecino más* próximo, que elige el elemento de entrada más cercano al centro de píxeles correspondiente para cada elemento de salida.</span><span class="sxs-lookup"><span data-stu-id="6b274-121">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>

- <span data-ttu-id="6b274-122">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="6b274-122">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="6b274-123">Usa el *algoritmo Quadrilinear,* que calcula el elemento de salida haciendo el promedio ponderado de los 2 elementos de entrada vecinos más cercanos por dimensión.</span><span class="sxs-lookup"><span data-stu-id="6b274-123">Uses the *Quadrilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="6b274-124">Puesto que se pueden volver a muestrear las cuatro dimensiones, el promedio ponderado se calcula en un total de 16 elementos de entrada para cada elemento de salida.</span><span class="sxs-lookup"><span data-stu-id="6b274-124">Since all 4 dimensions can be resampled, the weighted average is computed on a total of 16 input elements for each output element.</span></span>


`DimensionCount`

<span data-ttu-id="6b274-125">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="6b274-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="6b274-126">Número de valores de las matrices a las que apuntan *Scales*, *InputPixelOffsets* y *OutputPixelOffsets.*</span><span class="sxs-lookup"><span data-stu-id="6b274-126">The number of values in the arrays that *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* point to.</span></span> <span data-ttu-id="6b274-127">Este valor debe coincidir con el recuento de dimensiones *de InputTensor* y *OutputTensor*, que debe ser 4.</span><span class="sxs-lookup"><span data-stu-id="6b274-127">This value must match the dimension count of *InputTensor* and *OutputTensor*, which has to be 4.</span></span>


`Scales`

<span data-ttu-id="6b274-128">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6b274-128">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6b274-129">Escalas que se aplicarán al volver > cambiar el tamaño de la entrada, donde escala > 1 escala verticalmente la imagen y escala < 1 reducir verticalmente la imagen para esa dimensión.</span><span class="sxs-lookup"><span data-stu-id="6b274-129">The scales to apply when resampling the input, where scales > 1 scale up the image and scales < 1 scale down the image for that dimension.</span></span> <span data-ttu-id="6b274-130">Tenga en cuenta que no es necesario que las escalas sean exactamente `OutputSize / InputSize` .</span><span class="sxs-lookup"><span data-stu-id="6b274-130">Note that the scales don't need to be exactly `OutputSize / InputSize`.</span></span> <span data-ttu-id="6b274-131">Si la entrada después del escalado es mayor que el límite de salida, la recortaremos al tamaño de salida.</span><span class="sxs-lookup"><span data-stu-id="6b274-131">If the input after scaling is larger than the output bound, then we crop it to the output size.</span></span> <span data-ttu-id="6b274-132">Por otro lado, si la entrada después del escalado es menor que el límite de salida, se fijan los bordes de salida.</span><span class="sxs-lookup"><span data-stu-id="6b274-132">On the other hand, if the input after scaling is smaller than the output bound, the output edges are clamped.</span></span>


`InputPixelOffsets`

<span data-ttu-id="6b274-133">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6b274-133">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6b274-134">Desplazamientos que se van a aplicar a los píxeles de entrada antes de volver a realizar el muestreo.</span><span class="sxs-lookup"><span data-stu-id="6b274-134">The offsets to apply to the input pixels before resampling.</span></span> <span data-ttu-id="6b274-135">Cuando este valor es , se usa la esquina superior izquierda del píxel en lugar de su centro, lo que normalmente no `0` dará el resultado esperado.</span><span class="sxs-lookup"><span data-stu-id="6b274-135">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="6b274-136">Para volver a muestrear la imagen mediante el centro de los píxeles y obtener el mismo comportamiento que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), este valor debe ser `0.5` .</span><span class="sxs-lookup"><span data-stu-id="6b274-136">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `0.5`.</span></span>


`OutputPixelOffsets`

<span data-ttu-id="6b274-137">Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6b274-137">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6b274-138">Desplazamientos que se aplicarán a los píxeles de salida después de volver a realizar el muestreo.</span><span class="sxs-lookup"><span data-stu-id="6b274-138">The offsets to apply to the output pixels after resampling.</span></span> <span data-ttu-id="6b274-139">Cuando este valor es , se usa la esquina superior izquierda del píxel en lugar de su centro, lo que normalmente no `0` dará el resultado esperado.</span><span class="sxs-lookup"><span data-stu-id="6b274-139">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="6b274-140">Para volver a muestrear la imagen mediante el centro de los píxeles y obtener el mismo comportamiento que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), este valor debe ser `-0.5` .</span><span class="sxs-lookup"><span data-stu-id="6b274-140">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `-0.5`.</span></span>


## <a name="remarks"></a><span data-ttu-id="6b274-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b274-141">Remarks</span></span>
<span data-ttu-id="6b274-142">Cuando *InputPixelOffsets* se establece en 0,5 y *OutputPixelOffsets* se establece en -0,5, este operador es equivalente a [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="6b274-142">When the *InputPixelOffsets* are set to 0.5, and the *OutputPixelOffsets* are set to -0.5, this operator is equivalent to [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="6b274-143">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="6b274-143">Availability</span></span>
<span data-ttu-id="6b274-144">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="6b274-144">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="6b274-145">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="6b274-145">Tensor constraints</span></span>
<span data-ttu-id="6b274-146">*InputTensor* y *OutputTensor* deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="6b274-146">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="6b274-147">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="6b274-147">Tensor support</span></span>
| <span data-ttu-id="6b274-148">Tensor</span><span class="sxs-lookup"><span data-stu-id="6b274-148">Tensor</span></span> | <span data-ttu-id="6b274-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="6b274-149">Kind</span></span> | <span data-ttu-id="6b274-150">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="6b274-150">Supported dimension counts</span></span> | <span data-ttu-id="6b274-151">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="6b274-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="6b274-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="6b274-152">InputTensor</span></span> | <span data-ttu-id="6b274-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="6b274-153">Input</span></span> | <span data-ttu-id="6b274-154">4</span><span class="sxs-lookup"><span data-stu-id="6b274-154">4</span></span> | <span data-ttu-id="6b274-155">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6b274-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6b274-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="6b274-156">OutputTensor</span></span> | <span data-ttu-id="6b274-157">Resultados</span><span class="sxs-lookup"><span data-stu-id="6b274-157">Output</span></span> | <span data-ttu-id="6b274-158">4</span><span class="sxs-lookup"><span data-stu-id="6b274-158">4</span></span> | <span data-ttu-id="6b274-159">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6b274-159">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="6b274-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b274-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6b274-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="6b274-161">**Header**</span></span> | <span data-ttu-id="6b274-162">directml.h</span><span class="sxs-lookup"><span data-stu-id="6b274-162">directml.h</span></span> |