---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Realiza una operación de alineación de ROI, tal como se describe en el [documento Mask R-CNN](https://arxiv.org/abs/1703.06870). En Resumen, la operación extrae los cultivos de la imagen de entrada tensores y los cambia de tamaño a un tamaño de salida común especificado por las 2 últimas dimensiones de *OutputTensor* mediante el *InterpolationMode* especificado.
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
ms.openlocfilehash: 987aef7d7002892b8af3167fb8da2b74dc80a12e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721251"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a>DML_ROI_ALIGN_OPERATOR_DESC estructura (directml. h)

Realiza una operación de alineación de ROI, tal como se describe en el [documento Mask R-CNN](https://arxiv.org/abs/1703.06870). En Resumen, la operación extrae los cultivos de la imagen de entrada tensores y los cambia de tamaño a un tamaño de salida común especificado por las 2 últimas dimensiones de *OutputTensor* mediante el *InterpolationMode* especificado.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

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

Tensores que contiene los datos de entrada con dimensiones `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .

`ROITensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos de las regiones de interés (ROI). Las dimensiones permitidas de `ROITensor` son `{ NumROIs, 4 }` , `{ 1, NumROIs, 4 }` o `{ 1, 1, NumROIs, 4 }` . Para cada ROI, los valores serán las coordenadas de las esquinas superior izquierda e inferior derecha en el orden `[x1, y1, x2, y2]` .

`BatchIndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores que contiene los índices de lote del que se va a extraer el ROIs. Las dimensiones permitidas de `BatchIndicesTensor` son `{ NumROIs }` , `{ 1, NumROIs }` , `{ 1, 1, NumROIs }` o `{ 1, 1, 1, NumROIs }` . Cada valor es el índice de un lote de *InputTensor*. El comportamiento es indefinido si los valores no están en el intervalo [0, BatchCount).

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos de salida. Las dimensiones esperadas de *OutputTensor* son `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .

`ReductionFunction`

Tipo: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**

Función de reducción que se va a usar al reducir todos los ejemplos de entrada que contribuyan a un elemento Output ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) o **DML_REDUCE_FUNCTION_MAX**). El número de muestras de entrada que se van a reducir en está limitado por *MinimumSamplesPerOutput* y *MaximumSamplesPerOutput*.

`InterpolationMode`

Tipo: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**

El modo de interpolación que se va a utilizar al cambiar el tamaño de las regiones.

- [DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode). Usa el algoritmo *vecino más cercano* , que elige el elemento de entrada más cercano al centro de píxeles correspondiente para cada elemento de salida.
- **DML_INTERPOLATION_MODE_LINEAR**. Usa el algoritmo *Bilinear* , que calcula el elemento de salida mediante la media ponderada de los dos elementos de entrada vecinos más cercanos por dimensión. Dado que solo se cambia el tamaño de 2 dimensiones, el promedio ponderado se calcula en un total de 4 elementos de entrada para cada elemento de salida.

`SpatialScaleX`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

El componente X (o ancho) del factor de escala para multiplicar las coordenadas de *ROITensor* por con el fin de que sean proporcionales a *InputHeight* y *InputWidth*. Por ejemplo, si *ROITensor* contiene coordenadas normalizadas (valores en el intervalo [0.. 1]), entonces *SpatialScaleX* normalmente tendrá el mismo valor que *InputWidth*.

`SpatialScaleY`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

Componente Y (o alto) del factor de escala para multiplicar las coordenadas de *ROITensor* por con el fin de que sean proporcionales a *InputHeight* y *InputWidth*. Por ejemplo, si *ROITensor* contiene coordenadas normalizadas (valores en el intervalo [0.. 1]), *SpatialScaleY* normalmente tendrá el mismo valor que *InputHeight*.

`OutOfBoundsInputValue`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

Valor que se va a leer de *InputTensor* cuando el Rois está fuera de los límites de *InputTensor*. Esto puede ocurrir cuando los valores obtenidos después del escalado de *ROITensor* por *SpatialScaleX* y *SpatialScaleY* son mayores que *InputWidth* y *InputHeight*.

`MinimumSamplesPerOutput`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b>

Número mínimo de muestras de entrada que se van a utilizar para cada elemento de salida. El operador calculará el número de muestras de entrada mediante la acción y, a continuación, la fijará `ScaledCropSize / OutputSize` a *MinimumSamplesPerOutput* y *MaximumSamplesPerOutput*.

`MaximumSamplesPerOutput`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b>

Número máximo de ejemplos de entrada que se van a utilizar para cada elemento de salida. El operador calculará el número de muestras de entrada mediante la acción y, a continuación, la fijará `ScaledCropSize / OutputSize` a *MinimumSamplesPerOutput* y *MaximumSamplesPerOutput*.

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensores
*InputTensor*, *OutputTensor* y *ROITensor* deben tener el mismo *tipo de texto*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| ROITensor | Entrada | de 2 a 4 | FLOAT32, FLOAT16 |
| BatchIndicesTensor | Entrada | de 1 a 4 | UINT32 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |