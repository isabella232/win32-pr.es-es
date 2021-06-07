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
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a>DML_ROI_ALIGN_OPERATOR_DESC estructura (directml.h)

Realiza una operación de alineación de ROI, como se describe en el documento [Mask R-CNN (Enmascaramiento de R-CNN).](https://arxiv.org/abs/1703.06870) En resumen, la operación extrae los recortes del tensor de la imagen de entrada y los cambia de tamaño a un tamaño de salida común especificado por las dos últimas dimensiones de *OutputTensor* mediante el *valor interpolationMode especificado.*

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis

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

## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de entrada con dimensiones `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .

`ROITensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de las regiones de interés (ROI). Las dimensiones permitidas de `ROITensor` son `{ NumROIs, 4 }` , o `{ 1, NumROIs, 4 }` `{ 1, 1, NumROIs, 4 }` . Para cada ROI, los valores serán las coordenadas de sus esquinas superior izquierda e inferior derecha en el orden `[x1, y1, x2, y2]` .

`BatchIndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los índices por lotes de los que extraer los ROI. Las dimensiones permitidas de `BatchIndicesTensor` son , , o `{ NumROIs }` `{ 1, NumROIs }` `{ 1, 1, NumROIs }` `{ 1, 1, 1, NumROIs }` . Cada valor es el índice de un lote de *InputTensor.* El comportamiento es indefinido si los valores no están en el intervalo [0, BatchCount).

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de salida. Las dimensiones esperadas de *OutputTensor* son `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .

`ReductionFunction`

Tipo: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**

Función de reducción que se usa al reducir en todas las muestras de entrada que contribuyen a un elemento de salida ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) **o DML_REDUCE_FUNCTION_MAX**). *MinimumSamplesPerOutput* y *MaximumSamplesPerOutput* delimitan el número de muestras de entrada para reducir en .

`InterpolationMode`

Tipo: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**

Modo de interpolación que se va a usar al cambiar el tamaño de las regiones.

- [DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode). Usa el *algoritmo Vecino más* próximo, que elige el elemento de entrada más cercano al centro de píxeles correspondiente para cada elemento de salida.
- **DML_INTERPOLATION_MODE_LINEAR**. Usa el *algoritmo Bilinear,* que calcula el elemento de salida haciendo el promedio ponderado de los 2 elementos de entrada vecinos más cercanos por dimensión. Puesto que solo se cambia el tamaño de dos dimensiones, la media ponderada se calcula en un total de 4 elementos de entrada para cada elemento de salida.

`SpatialScaleX`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Componente X (o ancho) del factor de escalado por el que se multiplican las coordenadas *ROITensor* para que sea proporcional a *InputHeight* y *InputWidth.* Por ejemplo, si *ROITensor* contiene coordenadas normalizadas (valores en el intervalo [0..1]), *SpatialScaleX* normalmente tendría el mismo valor que *InputWidth*.

`SpatialScaleY`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Componente Y (o alto) del factor de escalado por el que se multiplican las coordenadas *ROITensor* para que sea proporcional a *InputHeight* y *InputWidth.* Por ejemplo, si *ROITensor* contiene coordenadas normalizadas (valores en el intervalo [0..1]), *SpatialScaleY normalmente* tendría el mismo valor que *InputHeight*.

`OutOfBoundsInputValue`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Valor que se va a leer *de InputTensor* cuando los ROI están fuera de los límites de *InputTensor.* Esto puede ocurrir cuando los valores obtenidos después de escalar *ROITensor* por *SpatialScaleX* y *SpatialScaleY* son mayores que *InputWidth* *y InputHeight.*

`MinimumSamplesPerOutput`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b>

Número mínimo de muestras de entrada que se usarán para cada elemento de salida. El operador calculará el número de muestras de entrada haciendo y, a continuación, lo fijará en `ScaledCropSize / OutputSize` *MinimumSamplesPerOutput* y *MaximumSamplesPerOutput*.

`MaximumSamplesPerOutput`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b>

Número máximo de muestras de entrada que se usarán para cada elemento de salida. El operador calculará el número de muestras de entrada haciendo y, a continuación, lo fijará en `ScaledCropSize / OutputSize` *MinimumSamplesPerOutput* y *MaximumSamplesPerOutput*.

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de Tensor
*InputTensor,* *OutputTensor* y *ROITensor* deben tener el mismo *datatype*.

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| ROITensor | Entrada | De 2 a 4 | FLOAT32, FLOAT16 |
| BatchIndicesTensor | Entrada | De 1 a 4 | UINT32 |
| OutputTensor | Resultados | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |