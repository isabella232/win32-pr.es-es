---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Realiza una circunvolución del *FilterTensor* con *InputTensor*. Este operador realiza la circunvolución hacia delante en los datos cuantificados. Este operador es matemáticamente equivalente a descuantificar las entradas, Convolving y, a continuación, cuantificando la salida.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_convolution_operator_desc
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
f1_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.openlocfilehash: 01193b19744f413690a3cb5ecccbb8fa60626cb0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721269"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a>DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC estructura (directml. h)
Realiza una circunvolución del *FilterTensor* con *InputTensor*. Este operador realiza la circunvolución hacia delante en los datos cuantificados. Este operador es matemáticamente equivalente a descuantificar las entradas, Convolving y, a continuación, cuantificando la salida. 

Las funciones de cuantificación lineal utilizadas por este operador son las funciones de cuantificación lineal

### <a name="dequantize-function"></a>Descuantificar función

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>Función cuantificate

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputScaleTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterScaleTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *BiasTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```



## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos de entrada. Las dimensiones esperadas de *InputTensor* son `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos de la escala de entrada. Las dimensiones esperadas de `InputScaleTensor` son `{ 1, 1, 1, 1 }` . Este valor de escala se usa para descuantificar los valores de entrada.


`InputZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores opcional que contiene los datos de punto cero de entrada. Las dimensiones esperadas de *InputZeroPointTensor* son `{ 1, 1, 1, 1 }` . Este valor de punto cero se usa para descuantificar los valores de entrada.


`FilterTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos del filtro. Las dimensiones esperadas de *FilterTensor* son `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos de la escala del filtro. Las dimensiones esperadas de `FilterScaleTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores o `{ 1, OutputChannelCount, 1, 1 }` si se requiere la cuantificación por canal. Este valor de escala se usa para descuantificar los valores de filtro.


`FilterZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores opcional que contiene los datos del punto cero del filtro. Las dimensiones esperadas de *FilterZeroPointTensor* son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores, o `{ 1, OutputChannelCount, 1, 1 }` si se requiere la cuantificación por canal. Este valor de punto cero se usa para descuantificar los valores de filtro.


`BiasTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos de sesgo. Bias tensores es un tensores que contiene datos que se difunden a través de la tensores de salida al final de la circunvolución que se agrega al resultado. Las dimensiones esperadas de BiasTensor son `{ 1, OutputChannelCount, 1, 1 }` para 4D.


`OutputScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos de la escala de salida. Las dimensiones esperadas de OutputScaleTensor son `{ 1, 1, 1, 1 }` . Este valor de escala de entrada se utiliza para cuantificar los valores de salida de circunvolución.


`OutputZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores opcional que contiene los datos del punto cero del filtro. Las dimensiones esperadas de OutputZeroPointTensor son `{ 1, 1, 1, 1 }` . Este valor de punto cero de entrada se utiliza para cuantificar la circunvolución de los valores de salida.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores en el que se van a escribir los resultados. Las dimensiones esperadas de OutputTensor son `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de dimensiones espaciales para la operación de circunvolución. Las dimensiones espaciales son las dimensiones inferiores del filtro de circunvolución tensores *FilterTensor*. Este valor también determina el tamaño de las matrices de los *progresos*, *Dilations*, *StartPadding* y *EndPadding* . Solo se admite un valor de 2.


`Strides`

Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Los progresos de la operación de circunvolución. Estos avances se aplican al filtro de circunvolución. Son independientes de los progresos de tensores incluidos en [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).


`Dilations`

Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Dilations de la operación de circunvolución. Dilations son los progresos aplicados a los elementos del kernel de filtro. Esto tiene el efecto de simular un kernel de filtro mayor al rellenar los elementos de kernel del filtro interno con ceros.


`StartPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Valores de relleno que se van a aplicar al principio de cada dimensión espacial del filtro y tensores de entrada de la operación de circunvolución.


`EndPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Valores de relleno que se van a aplicar al final de cada dimensión espacial del filtro y tensores de entrada de la operación de circunvolución.


`GroupCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Número de grupos en los que se va a dividir la operación de circunvolución. *GroupCount* se puede usar para lograr una circunvolución de nivel de profundidad estableciendo el valor de *GroupCount* igual al número de canales de entrada. Esto divide la circunvolución en una circunvolución independiente por canal de entrada. 

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensores
* *FilterTensor* y *FilterZeroPointTensor* deben tener el mismo *tipo de texto*.
* *InputTensor* y *InputZeroPointTensor* deben tener el mismo *tipo de texto*.
* *OutputTensor* y `OutputZeroPointTensor` deben tener el mismo *tipo de texto*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | INT8, UINT8 |
| InputScaleTensor | Entrada | 4 | FLOAT32 |
| InputZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| FilterTensor | Entrada | 4 | INT8, UINT8 |
| FilterScaleTensor | Entrada | 4 | FLOAT32 |
| FilterZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| BiasTensor | Entrada opcional | 4 | INT32 |
| OutputScaleTensor | Entrada | 4 | FLOAT32 |
| OutputZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| OutputTensor | Output | 4 | INT8, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |