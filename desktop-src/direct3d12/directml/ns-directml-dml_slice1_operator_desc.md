---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Extrae una sola subregión (un "segmento") de una tensores de entrada.
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: 06721a7484426eb293494156a2ec23db6fbf0a6b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721229"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a>DML_SLICE1_OPERATOR_DESC estructura (directml. h)
Extrae una sola subregión (un "segmento") de una tensores de entrada.

En la *ventana Entrada* se describen los límites del tensores de entrada que se deben tener en cuenta en el segmento. La ventana se define con tres valores para cada dimensión.

- El *desplazamiento* marca el *principio de la ventana* en una dimensión.
- El *tamaño* marca la extensión de la ventana en una dimensión. El *final de la ventana* de una dimensión es `offset + size - 1` .
- El *intervalo* indica cómo recorrer los elementos de una dimensión.
  - La magnitud del intervalo indica el número de elementos que se van a avanzar al copiar dentro de la ventana.
  - Si un intervalo es positivo, los elementos se copian empezando por el *principio* de la ventana en la dimensión.
  - Si un intervalo es negativo, los elementos se copian empezando por el *final* de la ventana de la dimensión.

En el siguiente pseudocódigo se muestra cómo se copian los elementos mediante la ventana de entrada. Observe cómo se copian los elementos de una dimensión de principio a fin con un intervalo positivo y se copian de end a Start con un intervalo negativo.

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

La ventana de entrada no debe estar vacía en cualquier dimensión y la ventana no debe se extiende más allá de las dimensiones de la tensores de entrada (no se permiten lecturas fuera de límites). El tamaño de la ventana y los progresos limitan de forma efectiva el número de elementos que se pueden copiar de cada dimensión `i` de la tensores de entrada.

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

El tensores de salida no es necesario para copiar todos los elementos que se pueden alcanzar dentro de la ventana. El segmento es válido, siempre y cuando `1 <= OutputSizes[i] <= MaxCopiedElements[i]` .

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores del que se van a extraer los segmentos.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores en el que se van a escribir los resultados de datos segmentados.


`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Número de dimensiones. Este campo determina el tamaño de las matrices *InputWindowOffsets*, *InputWindowSizes* y *InputWindowStrides* . Este valor debe coincidir con el *DimensionCount* de los idiomas de entrada y salida. Este valor debe estar comprendido entre 1 y 8, de forma inclusiva, a partir de `DML_FEATURE_LEVEL_3_0` ; los niveles de características anteriores requieren un valor de 4 o 5.


`InputWindowOffsets`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Una matriz que contiene el principio (en elementos) de la ventana de entrada en cada dimensión. Los valores de la matriz deben cumplir la restricción `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowSizes`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Una matriz que contiene la extensión (en elementos) de la ventana de entrada en cada dimensión. Los valores de la matriz deben cumplir la restricción `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowStrides`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Una matriz que contiene el intervalo del segmento a lo largo de cada dimensión del tensores de entrada, en elementos. La magnitud del intervalo indica el número de elementos que se van a avanzar al copiar dentro de la ventana de entrada. El signo del intervalo determina si los elementos se copian empezando por el principio de la ventana (intervalo positivo) o el final de la ventana (intervalo negativo). Los progresos no pueden ser 0.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se usa esta misma tensores de entrada.

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a>Ejemplo 1. Segmento progresado con avances positivos

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

Los elementos copiados se calculan como se indica a continuación. 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a>Ejemplo 2. Segmento progresado con avances negativos

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

Recuerde que las dimensiones con una ventana negativa progresan a copiar al final de la ventana de entrada de esa dimensión. Esto se hace agregando `InputWindowSize[i] - 1` al desplazamiento de la ventana. Las dimensiones con un intervalo positivo simplemente empiezan en `InputWindowOffset[i]` .
- El eje 0 ( `+1` intervalo de ventana) comienza a copiarse en `InputWindowOffsets[0] = 0` . 
- El eje 1 ( `+1` intervalo de ventana) comienza a copiarse en `InputWindowOffsets[1] = 0` . 
- El eje 2 ( `-2` intervalo de ventana) comienza a copiarse en `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` . 
- El eje 3 ( `+2` intervalo de ventana) comienza a copiarse en `InputWindowOffsets[3] = 1` . 

Los elementos copiados se calculan como se indica a continuación. 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a>Observaciones
Este operador es similar a [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), pero difiere en dos aspectos importantes.

- Los progresos del segmento pueden ser negativos, lo que permite invertir valores a lo largo de las dimensiones.
- Los tamaños de la ventana de entrada no son necesariamente los mismos que los tamaños de tensores de salida.

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensores
*InputTensor* y *OutputTensor* deben tener el mismo *DataType* y *DimensionCount*.

## <a name="tensor-support"></a>Compatibilidad con tensores
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 y versiones posteriores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | de 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | de 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y versiones posteriores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | de 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | de 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |