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
# <a name="dml_resample1_operator_desc-structure-directmlh"></a>DML_RESAMPLE1_OPERATOR_DESC estructura (directml. h)
Vuelve a muestrear los elementos del origen al tensores de destino, usando los factores de escala para calcular el tamaño de tensores de destino. Puede usar un modo de interpolación lineal o más cercano. El operador admite la interpolación en varias dimensiones, no solo en 2D. Por lo tanto, puede mantener el mismo tamaño espacial, pero interpolar entre canales o por lotes. La relación entre las coordenadas de entrada y salida es la siguiente.

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis
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



## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos de entrada.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores en el que se van a escribir los datos de salida.


`InterpolationMode`

Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Este campo determina el tipo de interpolación que se usa para elegir los píxeles de salida.

- **DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**. Usa el algoritmo *vecino más cercano* , que elige el elemento de entrada más cercano al centro de píxeles correspondiente para cada elemento de salida.

- **DML_INTERPOLATION_MODE_LINEAR**. Usa el algoritmo *Quadrilinear* , que calcula el elemento Output mediante la media ponderada de los dos elementos de entrada vecinos más cercanos por dimensión. Dado que se pueden volver a muestrear las 4 dimensiones, el promedio ponderado se calcula en un total de 16 elementos de entrada para cada elemento de salida.


`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de valores de las matrices que se *escalan*, *InputPixelOffsets* y *OutputPixelOffsets* apuntan a. Este valor debe coincidir con el recuento de dimensiones de *InputTensor* y *OutputTensor*, que tiene que ser 4.


`Scales`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Escalas que se van a aplicar al volver a muestrear la entrada, donde las escalas > 1 escalan verticalmente la imagen y se escalan < 1 reducir verticalmente la imagen de esa dimensión. Tenga en cuenta que no es necesario que las escalas sean exactas `OutputSize / InputSize` . Si la entrada después del escalado es mayor que el límite de salida, se recortará en el tamaño de salida. Por otro lado, si la entrada después del escalado es menor que el límite de salida, se fijan los bordes de salida.


`InputPixelOffsets`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Desplazamientos que se van a aplicar a los píxeles de entrada antes de volver a muestrear. Cuando este valor es `0` , se usa la esquina superior izquierda del píxel en lugar de su centro, que normalmente no proporcionará el resultado esperado. Para volver a muestrear la imagen mediante el centro de los píxeles y obtener el mismo comportamiento que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), este valor debe ser `0.5` .


`OutputPixelOffsets`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Desplazamientos que se van a aplicar a los píxeles de salida después del remuestreo. Cuando este valor es `0` , se usa la esquina superior izquierda del píxel en lugar de su centro, que normalmente no proporcionará el resultado esperado. Para volver a muestrear la imagen mediante el centro de los píxeles y obtener el mismo comportamiento que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), este valor debe ser `-0.5` .


## <a name="remarks"></a>Observaciones
Cuando el valor de *InputPixelOffsets* se establece en 0,5 y el valor de *OutputPixelOffsets* se establece en-0,5, este operador es equivalente a [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensores
*InputTensor* y *OutputTensor* deben tener el mismo *tipo de texto*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |