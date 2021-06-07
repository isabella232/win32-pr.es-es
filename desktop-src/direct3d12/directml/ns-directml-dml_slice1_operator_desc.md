---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Extrae una sola subregión (un "segmento") de un tensor de entrada.
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
ms.openlocfilehash: f34525865be9541da879e66e88c29d4a2ab74f00
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417944"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a>DML_SLICE1_OPERATOR_DESC estructura (directml.h)
Extrae una sola subregión (un "segmento") de un tensor de entrada.

La *ventana de* entrada describe los límites del tensor de entrada que se deben tener en cuenta en el segmento. La ventana se define mediante tres valores para cada dimensión.

- El *desplazamiento* marca el *principio de la ventana* en una dimensión.
- El *tamaño* marca la extensión de la ventana en una dimensión. El *final de la ventana* de una dimensión es `offset + size - 1` .
- El *paso* indica cómo recorrer los elementos de una dimensión.
  - La magnitud del paso indica cuántos elementos avanzar al copiar dentro de la ventana.
  - Si un paso es positivo, los elementos se copian a partir *del principio* de la ventana de la dimensión.
  - Si un paso es negativo, los elementos se copian a partir del *final* de la ventana de la dimensión.

En el pseudocódigo siguiente se muestra cómo se copian los elementos mediante la ventana de entrada. Observe cómo los elementos de una dimensión se copian de principio a fin con un paso positivo y se copian de un extremo a otro con un paso negativo.

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

La ventana de entrada no debe estar vacía en ninguna dimensión y la ventana no debe extenderse más allá de las dimensiones del tensor de entrada (no se permiten lecturas fuera de límite). El tamaño y los avances de la ventana limitan eficazmente el número de elementos que se pueden copiar de cada dimensión `i` del tensor de entrada.

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

El tensor de salida no es necesario para copiar todos los elementos accesibles dentro de la ventana. El segmento es válido siempre que `1 <= OutputSizes[i] <= MaxCopiedElements[i]` .

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

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

Tensor del que se extraen los segmentos.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor en el que se escriben los resultados de los datos segmentados.


`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de dimensiones. Este campo determina el tamaño de las *matrices InputWindowOffsets,* *InputWindowSizes* y *InputWindowStrides.* Este valor debe coincidir con *dimensioncount* de los tensores de entrada y salida. Este valor debe estar entre 1 y 8, ambos inclusive, a partir de ; los niveles de características anteriores requieren un valor `DML_FEATURE_LEVEL_3_0` de 4 o 5.


`InputWindowOffsets`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Matriz que contiene el principio (en elementos) de la ventana de entrada en cada dimensión. Los valores de la matriz deben satisfacer la restricción `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowSizes`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Matriz que contiene la extensión (en elementos) de la ventana de entrada en cada dimensión. Los valores de la matriz deben satisfacer la restricción `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowStrides`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Matriz que contiene el paso del segmento a lo largo de cada dimensión del tensor de entrada, en elementos . La magnitud del paso indica cuántos elementos avanzar al copiar dentro de la ventana de entrada. El signo del paso determina si los elementos se copian a partir del principio de la ventana (paso positivo) o al final de la ventana (paso negativo). Es posible que Strides no sea 0.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se usa este mismo tensor de entrada.

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a>Ejemplo 1. Segmento strided con strides positivos

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

Los elementos copiados se calculan como se muestra a continuación. 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a>Ejemplo 2. Segmento con strid con strides negativos

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

Recuerde que las dimensiones con avances de ventana negativos comienzan a copiarse al final de la ventana de entrada para esa dimensión; Esto se realiza agregando `InputWindowSize[i] - 1` al desplazamiento de la ventana. Las dimensiones con un paso positivo simplemente comienzan en `InputWindowOffset[i]` .
- El eje 0 `+1` (paso de la ventana) comienza a copiarse en `InputWindowOffsets[0] = 0` . 
- El eje 1 `+1` (paso de la ventana) comienza a copiarse en `InputWindowOffsets[1] = 0` . 
- El eje 2 `-2` (paso de la ventana) comienza a copiarse en `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` . 
- El eje 3 `+2` (paso de la ventana) comienza a copiarse en `InputWindowOffsets[3] = 1` . 

Los elementos copiados se calculan como se muestra a continuación. 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a>Comentarios
Este operador es similar a [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), pero difiere de dos maneras importantes.

- Los avances de segmento pueden ser negativos, lo que permite invertir valores a lo largo de las dimensiones.
- Los tamaños de ventana de entrada no son necesariamente los mismos que los tamaños de tensor de salida.

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensor
*InputTensor* y *OutputTensor* deben tener los mismos *DataType* y *DimensionCount.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Resultados | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Resultados | De 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |