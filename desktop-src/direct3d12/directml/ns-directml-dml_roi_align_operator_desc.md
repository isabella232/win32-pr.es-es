---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Realiza una operación de alineación de ROI, como se describe en el documento [Mask R-CNN (Enmascaramiento de R-CNN).](https://arxiv.org/abs/1703.06870) En resumen, la operación extrae los recortes del tensor de la imagen de entrada y los cambia de tamaño a un tamaño de salida común especificado por las dos últimas dimensiones de *OutputTensor* mediante el *valor interpolationMode especificado.*
helpviewer_keywords:
- DML_ROI_ALIGN_OPERATOR_DESC
- DML_ROI_ALIGN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ROI_ALIGN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ROI_ALIGN_OPERATOR_DESC, DML_ROI_ALIGN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
- directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
ms.openlocfilehash: b9004a77d3b325dd3394d1a3a6b596e94997e9fd
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417959"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a><span data-ttu-id="6a8e7-104">DML_ROI_ALIGN_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="6a8e7-104">DML_ROI_ALIGN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="6a8e7-105">Realiza una operación de alineación de ROI, como se describe en el documento [Mask R-CNN (Enmascaramiento de R-CNN).](https://arxiv.org/abs/1703.06870)</span><span class="sxs-lookup"><span data-stu-id="6a8e7-105">Performs an ROI Align operation, as described in the [Mask R-CNN paper](https://arxiv.org/abs/1703.06870).</span></span> <span data-ttu-id="6a8e7-106">En resumen, la operación extrae los recortes del tensor de la imagen de entrada y los cambia de tamaño a un tamaño de salida común especificado por las dos últimas dimensiones de *OutputTensor* mediante el *valor interpolationMode especificado.*</span><span class="sxs-lookup"><span data-stu-id="6a8e7-106">In summary, the operation extracts crops from the input image tensor and resizes them to a common output size specified by the last 2 dimensions of *OutputTensor* using the specified *InterpolationMode*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a8e7-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="6a8e7-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="6a8e7-108">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="6a8e7-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a8e7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a8e7-109">Syntax</span></span>

```cpp
struct DML_ROI_ALIGN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* ROITensor;
  const DML_TENSOR_DESC* BatchIndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  DML_REDUCE_FUNCTION ReductionFunction;
  DML_INTERPOLATION_MODE InterpolationMode;
  FLOAT SpatialScaleX;
  FLOAT SpatialScaleY;
  FLOAT OutOfBoundsInputValue;
  UINT MinimumSamplesPerOutput;
  UINT MaximumSamplesPerOutput;
};
```

## <a name="members"></a><span data-ttu-id="6a8e7-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="6a8e7-110">Members</span></span>

`InputTensor`

<span data-ttu-id="6a8e7-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6a8e7-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6a8e7-112">Tensor que contiene los datos de entrada con dimensiones `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="6a8e7-112">A tensor containing the input data with dimensions `{ BatchCount, ChannelCount, InputHeight, InputWidth }`.</span></span>

`ROITensor`

<span data-ttu-id="6a8e7-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6a8e7-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6a8e7-114">Tensor que contiene los datos de las regiones de interés (ROI).</span><span class="sxs-lookup"><span data-stu-id="6a8e7-114">A tensor containing the regions of interest (ROI) data.</span></span> <span data-ttu-id="6a8e7-115">Las dimensiones permitidas de `ROITensor` son `{ NumROIs, 4 }` , o `{ 1, NumROIs, 4 }` `{ 1, 1, NumROIs, 4 }` .</span><span class="sxs-lookup"><span data-stu-id="6a8e7-115">The allowed dimensions of `ROITensor` are `{ NumROIs, 4 }`, `{ 1, NumROIs, 4 }`, or `{ 1, 1, NumROIs, 4 }`.</span></span> <span data-ttu-id="6a8e7-116">Para cada ROI, los valores serán las coordenadas de sus esquinas superior izquierda e inferior derecha en el orden `[x1, y1, x2, y2]` .</span><span class="sxs-lookup"><span data-stu-id="6a8e7-116">For each ROI, the values will be the coordinates of its top-left and bottom-right corners in the order `[x1, y1, x2, y2]`.</span></span>

`BatchIndicesTensor`

<span data-ttu-id="6a8e7-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6a8e7-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6a8e7-118">Tensor que contiene los índices por lotes de los que extraer los ROI.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-118">A tensor containing the batch indices to extract the ROIs from.</span></span> <span data-ttu-id="6a8e7-119">Las dimensiones permitidas de `BatchIndicesTensor` son , , o `{ NumROIs }` `{ 1, NumROIs }` `{ 1, 1, NumROIs }` `{ 1, 1, 1, NumROIs }` .</span><span class="sxs-lookup"><span data-stu-id="6a8e7-119">The allowed dimensions of `BatchIndicesTensor` are `{ NumROIs }`, `{ 1, NumROIs }`, `{ 1, 1, NumROIs }`, or `{ 1, 1, 1, NumROIs }`.</span></span> <span data-ttu-id="6a8e7-120">Cada valor es el índice de un lote de *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="6a8e7-120">Each value is the index of a batch from *InputTensor*.</span></span> <span data-ttu-id="6a8e7-121">El comportamiento es indefinido si los valores no están en el intervalo [0, BatchCount).</span><span class="sxs-lookup"><span data-stu-id="6a8e7-121">The behavior is undefined if the values are not in the range [0, BatchCount).</span></span>

`OutputTensor`

<span data-ttu-id="6a8e7-122">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6a8e7-122">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6a8e7-123">Tensor que contiene los datos de salida.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-123">A tensor containing the output data.</span></span> <span data-ttu-id="6a8e7-124">Las dimensiones esperadas de *OutputTensor* son `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="6a8e7-124">The expected dimensions of *OutputTensor* are `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }`.</span></span>

`ReductionFunction`

<span data-ttu-id="6a8e7-125">Tipo: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span><span class="sxs-lookup"><span data-stu-id="6a8e7-125">Type: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span></span>

<span data-ttu-id="6a8e7-126">Función de reducción que se usa al reducir en todas las muestras de entrada que contribuyen a un elemento de salida ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) **o DML_REDUCE_FUNCTION_MAX**).</span><span class="sxs-lookup"><span data-stu-id="6a8e7-126">The reduction function to use when reducing across all input samples that contribute to an output element ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) or **DML_REDUCE_FUNCTION_MAX**).</span></span> <span data-ttu-id="6a8e7-127">*MinimumSamplesPerOutput* y *MaximumSamplesPerOutput* delimitan el número de muestras de entrada para reducir en .</span><span class="sxs-lookup"><span data-stu-id="6a8e7-127">The number of input samples to reduce across is bounded by *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`InterpolationMode`

<span data-ttu-id="6a8e7-128">Tipo: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span><span class="sxs-lookup"><span data-stu-id="6a8e7-128">Type: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span></span>

<span data-ttu-id="6a8e7-129">Modo de interpolación que se va a usar al cambiar el tamaño de las regiones.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-129">The interpolation mode to use when resizing the regions.</span></span>

- <span data-ttu-id="6a8e7-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span><span class="sxs-lookup"><span data-stu-id="6a8e7-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span></span> <span data-ttu-id="6a8e7-131">Usa el *algoritmo Vecino más* próximo, que elige el elemento de entrada más cercano al centro de píxeles correspondiente para cada elemento de salida.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-131">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>
- <span data-ttu-id="6a8e7-132">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-132">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="6a8e7-133">Usa el *algoritmo Bilinear,* que calcula el elemento de salida haciendo el promedio ponderado de los 2 elementos de entrada vecinos más cercanos por dimensión.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-133">Uses the *Bilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="6a8e7-134">Puesto que solo se cambia el tamaño de dos dimensiones, la media ponderada se calcula en un total de 4 elementos de entrada para cada elemento de salida.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-134">Since only 2 dimensions are resized, the weighted average is computed on a total of 4 input elements for each output element.</span></span>

`SpatialScaleX`

<span data-ttu-id="6a8e7-135">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="6a8e7-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="6a8e7-136">Componente X (o ancho) del factor de escalado por el que se multiplican las coordenadas *ROITensor* para que sea proporcional a *InputHeight* y *InputWidth.*</span><span class="sxs-lookup"><span data-stu-id="6a8e7-136">The X (or width) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="6a8e7-137">Por ejemplo, si *ROITensor* contiene coordenadas normalizadas (valores en el intervalo [0..1]), *SpatialScaleX* normalmente tendría el mismo valor que *InputWidth*.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-137">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), then *SpatialScaleX* would usually have the same value as *InputWidth*.</span></span>

`SpatialScaleY`

<span data-ttu-id="6a8e7-138">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="6a8e7-138">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="6a8e7-139">Componente Y (o alto) del factor de escalado por el que se multiplican las coordenadas *ROITensor* para que sea proporcional a *InputHeight* y *InputWidth.*</span><span class="sxs-lookup"><span data-stu-id="6a8e7-139">The Y (or height) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="6a8e7-140">Por ejemplo, si *ROITensor* contiene coordenadas normalizadas (valores en el intervalo [0..1]), *SpatialScaleY normalmente* tendría el mismo valor que *InputHeight*.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-140">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), *SpatialScaleY* would usually have the same value as *InputHeight*.</span></span>

`OutOfBoundsInputValue`

<span data-ttu-id="6a8e7-141">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="6a8e7-141">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="6a8e7-142">Valor que se va a leer *de InputTensor* cuando los ROI están fuera de los límites de *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="6a8e7-142">The value to read from *InputTensor* when the ROIs are outside the bounds of *InputTensor*.</span></span> <span data-ttu-id="6a8e7-143">Esto puede ocurrir cuando los valores obtenidos después de escalar *ROITensor* por *SpatialScaleX* y *SpatialScaleY* son mayores que *InputWidth* *y InputHeight.*</span><span class="sxs-lookup"><span data-stu-id="6a8e7-143">This can happen when the values obtained after scaling *ROITensor* by *SpatialScaleX* and *SpatialScaleY* are bigger than *InputWidth* and *InputHeight*.</span></span>

`MinimumSamplesPerOutput`

<span data-ttu-id="6a8e7-144">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="6a8e7-144">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="6a8e7-145">Número mínimo de muestras de entrada que se usarán para cada elemento de salida.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-145">The minimum number of input samples to use for every output element.</span></span> <span data-ttu-id="6a8e7-146">El operador calculará el número de muestras de entrada haciendo y, a continuación, lo fijará en `ScaledCropSize / OutputSize` *MinimumSamplesPerOutput* y *MaximumSamplesPerOutput*.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-146">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`MaximumSamplesPerOutput`

<span data-ttu-id="6a8e7-147">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="6a8e7-147">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="6a8e7-148">Número máximo de muestras de entrada que se usarán para cada elemento de salida.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-148">The maximum number of input samples to use for every output element.</span></span> <span data-ttu-id="6a8e7-149">El operador calculará el número de muestras de entrada haciendo y, a continuación, lo fijará en `ScaledCropSize / OutputSize` *MinimumSamplesPerOutput* y *MaximumSamplesPerOutput*.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-149">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

## <a name="availability"></a><span data-ttu-id="6a8e7-150">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="6a8e7-150">Availability</span></span>
<span data-ttu-id="6a8e7-151">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="6a8e7-151">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="6a8e7-152">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="6a8e7-152">Tensor constraints</span></span>
<span data-ttu-id="6a8e7-153">*InputTensor,* *OutputTensor* y *ROITensor* deben tener el mismo *datatype*.</span><span class="sxs-lookup"><span data-stu-id="6a8e7-153">*InputTensor*, *OutputTensor*, and *ROITensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="6a8e7-154">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="6a8e7-154">Tensor support</span></span>
| <span data-ttu-id="6a8e7-155">Tensor</span><span class="sxs-lookup"><span data-stu-id="6a8e7-155">Tensor</span></span> | <span data-ttu-id="6a8e7-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a8e7-156">Kind</span></span> | <span data-ttu-id="6a8e7-157">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="6a8e7-157">Supported dimension counts</span></span> | <span data-ttu-id="6a8e7-158">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="6a8e7-158">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="6a8e7-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="6a8e7-159">InputTensor</span></span> | <span data-ttu-id="6a8e7-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a8e7-160">Input</span></span> | <span data-ttu-id="6a8e7-161">4</span><span class="sxs-lookup"><span data-stu-id="6a8e7-161">4</span></span> | <span data-ttu-id="6a8e7-162">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6a8e7-162">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6a8e7-163">ROITensor</span><span class="sxs-lookup"><span data-stu-id="6a8e7-163">ROITensor</span></span> | <span data-ttu-id="6a8e7-164">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a8e7-164">Input</span></span> | <span data-ttu-id="6a8e7-165">De 2 a 4</span><span class="sxs-lookup"><span data-stu-id="6a8e7-165">2 to 4</span></span> | <span data-ttu-id="6a8e7-166">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6a8e7-166">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6a8e7-167">BatchIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="6a8e7-167">BatchIndicesTensor</span></span> | <span data-ttu-id="6a8e7-168">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a8e7-168">Input</span></span> | <span data-ttu-id="6a8e7-169">De 1 a 4</span><span class="sxs-lookup"><span data-stu-id="6a8e7-169">1 to 4</span></span> | <span data-ttu-id="6a8e7-170">UINT32</span><span class="sxs-lookup"><span data-stu-id="6a8e7-170">UINT32</span></span> |
| <span data-ttu-id="6a8e7-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="6a8e7-171">OutputTensor</span></span> | <span data-ttu-id="6a8e7-172">Resultados</span><span class="sxs-lookup"><span data-stu-id="6a8e7-172">Output</span></span> | <span data-ttu-id="6a8e7-173">4</span><span class="sxs-lookup"><span data-stu-id="6a8e7-173">4</span></span> | <span data-ttu-id="6a8e7-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6a8e7-174">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="6a8e7-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a8e7-175">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6a8e7-176">**Header**</span><span class="sxs-lookup"><span data-stu-id="6a8e7-176">**Header**</span></span> | <span data-ttu-id="6a8e7-177">directml.h</span><span class="sxs-lookup"><span data-stu-id="6a8e7-177">directml.h</span></span> |