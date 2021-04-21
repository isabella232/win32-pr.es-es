---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Calcula el valor máximo en los elementos de la ventana deslizante sobre el tensor de entrada y, opcionalmente, devuelve los índices de los valores máximos seleccionados.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803668"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a>DML_MAX_POOLING2_OPERATOR_DESC estructura (directml.h)
Calcula el valor máximo en los elementos de la ventana deslizante sobre el tensor de entrada y, opcionalmente, devuelve los índices de los valores máximos seleccionados.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de entrada de *Tamaños* `{ BatchCount, ChannelCount, Height, Width }` si *InputTensor.DimensionCount* es 4 y `{ BatchCount, ChannelCount, Depth, Height, Weight } ` si *InputTensor.DimensionCount* es 5.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida en el que se escriben los resultados. Los tamaños del tensor de salida se pueden calcular como se muestra a continuación.

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida opcional de índices para el tensor *inputTensor* de los valores máximos generados y almacenados en *OutputTensor*. Estos valores de índice se basan en cero y tratan el tensor de entrada como una matriz unidimensional contigua. Cuando varios elementos dentro de la ventana deslizante tienen el mismo valor, se omiten los valores iguales posteriores y el índice apunta al primer valor encontrado. Tanto *OutputTensor* como *OutputIndicesTensor* tienen los mismos tamaños de tensor.


`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de dimensiones espaciales del tensor *inputTensor*, que también corresponde al número de dimensiones de la ventana deslizante *WindowSize.* Este valor también determina el tamaño de las matrices *Strides,* *StartPadding* y *EndPadding.* Debe establecerse en 2 cuando *InputTensor* es 4D y 3 cuando es un tensor 5D.


`Strides`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Los avances de las dimensiones de ventana deslizante de tamaños cuando DimensionCount está establecido en 2 o cuando `{ Height, Width }` se establece en  `{ Depth, Height, Width }` 3.


`WindowSize`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Dimensiones de la ventana deslizante en `{ Height, Width }` cuando *DimensionCount* se establece en 2 o `{ Depth, Height, Width }` cuando se establece en 3.


`StartPadding`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Número de elementos de relleno que se aplicarán al principio de cada dimensión espacial del tensor *inputTensor.* Los valores están en `{ Height, Width }` cuando *DimensionCount* se establece en 2 o `{ Depth, Height, Width }` cuando se establece en 3.


`EndPadding`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Número de elementos de relleno que se aplicarán al final de cada dimensión espacial del tensor *inputTensor.* Los valores están en `{ Height, Width }` cuando *DimensionCount* se establece en 2 o `{ Depth, Height, Width }` cuando se establece en 3.


`Dilations`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Valores de cada dimensión espacial del *tensor inputTensor* por el que se selecciona un elemento dentro de la ventana deslizante para cada elemento de ese valor. Los valores están en `{ Height, Width }` cuando *DimensionCount* se establece en 2 o `{ Depth, Height, Width }` cuando se establece en 3.


## <a name="remarks"></a>Observaciones
**DML_MAX_POOLING2_OPERATOR_DESC** reemplaza a la versión anterior [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) con una matriz constante *adicional Denciones*. Las dos versiones son equivalentes cuando *Se establece en para* la entrada 4D o para las características de entrada `{ 1,1 }` `{ 1,1,1 }` 5D.

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensor
* *InputTensor,* *OutputIndicesTensor y* *OutputTensor* deben tener el mismo *DimensionCount.*
* *InputTensor* y *OutputTensor* deben tener el mismo *DataType.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 4 a 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputTensor | Resultados | De 4 a 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputIndicesTensor | Salida opcional | De 4 a 5 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 4 a 5 | FLOAT32, FLOAT16 |
| OutputTensor | Resultados | De 4 a 5 | FLOAT32, FLOAT16 |
| OutputIndicesTensor | Salida opcional | De 4 a 5 | UINT32 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Windows 10, versión 2004 (10.0; Compilación 19041) |
| **Servidor mínimo compatible** | Windows Server, versión 2004 (10.0; Compilación 19041) |
| **Header** | directml.h |