---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Calcula el valor máximo en los elementos de la ventana deslizante sobre la tensores de entrada y, opcionalmente, devuelve los índices de los valores máximos seleccionados.
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
ms.openlocfilehash: 7d2dc9d28e8afcaa5cc6277e26f1f663f3f6688f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721302"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a>DML_MAX_POOLING2_OPERATOR_DESC estructura (directml. h)
Calcula el valor máximo en los elementos de la ventana deslizante sobre la tensores de entrada y, opcionalmente, devuelve los índices de los valores máximos seleccionados.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

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

Una tensores de entrada de *tamaños* `{ BatchCount, ChannelCount, Height, Width }` si *InputTensor. DimensionCount* es 4 y `{ BatchCount, ChannelCount, Depth, Height, Weight } ` si *InputTensor. DimensionCount* es 5.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de salida en el que se van a escribir los resultados. Los tamaños de los tensores de salida se pueden calcular como se indica a continuación.

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

Un tensores de salida opcional de los índices a la *InputTensor* de entrada tensores de los valores máximos generados y almacenados en *OutputTensor*. Estos valores de índice son de base cero y tratan la entrada tensores como una matriz unidimensional contigua. Cuando varios elementos de la ventana deslizante tienen el mismo valor, se omiten los valores iguales posteriores y el índice apunta al primer valor encontrado. Tanto *OutputTensor* como *OutputIndicesTensor* tienen los mismos tamaños de tensores.


`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de dimensiones espaciales de la tensores de entrada *InputTensor*, que también se corresponde con el número de dimensiones de *la ventana* deslizante. Este valor también determina el tamaño de las matrices de los *progresos*, *StartPadding* y *EndPadding* . Debe establecerse en 2 cuando el valor de *InputTensor* es 4D y 3 cuando es un tensores de 5D.


`Strides`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

El progresa para las dimensiones de la ventana deslizante de tamaños `{ Height, Width }` cuando *DimensionCount* se establece en 2, o `{ Depth, Height, Width }` cuando se establece en 3.


`WindowSize`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Las dimensiones de la ventana deslizante en `{ Height, Width }` cuando *DimensionCount* se establece en 2, o `{ Depth, Height, Width }` cuando se establece en 3.


`StartPadding`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

El número de elementos de relleno que se van a aplicar al principio de cada dimensión espacial del *InputTensor* de entrada tensores. Los valores están en `{ Height, Width }` cuando *DimensionCount* se establece en 2, o `{ Depth, Height, Width }` cuando se establece en 3.


`EndPadding`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

El número de elementos de relleno que se van a aplicar al final de cada dimensión espacial de la *InputTensor* de entrada tensores. Los valores están en `{ Height, Width }` cuando *DimensionCount* se establece en 2, o `{ Depth, Height, Width }` cuando se establece en 3.


`Dilations`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Los valores de cada dimensión espacial del *InputTensor* de entrada tensores por el que se selecciona un elemento dentro de la ventana deslizante para todos los elementos de ese valor. Los valores están en `{ Height, Width }` cuando *DimensionCount* se establece en 2, o `{ Depth, Height, Width }` cuando se establece en 3.


## <a name="remarks"></a>Observaciones
**DML_MAX_POOLING2_OPERATOR_DESC** sustituye a la versión anterior [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) por una matriz de constantes *Dilations* adicional. Las dos versiones son equivalentes cuando *Dilations* se establece en `{ 1,1 }` para la entrada 4D `{ 1,1,1 }` o para las características de entrada 5D.

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensores
* *InputTensor*, *OutputIndicesTensor* y *OutputTensor* deben tener el mismo *DimensionCount*.
* *InputTensor* y *OutputTensor* deben tener el mismo *tipo de texto*.

## <a name="tensor-support"></a>Compatibilidad con tensores
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 y versiones posteriores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | de 4 a 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputTensor | Output | de 4 a 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputIndicesTensor | Salida opcional | de 4 a 5 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y versiones posteriores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | de 4 a 5 | FLOAT32, FLOAT16 |
| OutputTensor | Output | de 4 a 5 | FLOAT32, FLOAT16 |
| OutputIndicesTensor | Salida opcional | de 4 a 5 | UINT32 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Windows 10, versión 2004 (10,0; Compilación 19041) |
| **Servidor mínimo compatible** | Windows Server, versión 2004 (10,0; Compilación 19041) |
| **Header** | directml. h |