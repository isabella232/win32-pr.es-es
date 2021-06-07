---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Realiza una convolución del *filterTensor* con *inputTensor*. Este operador realiza la convolución hacia delante en datos cuantificados. Este operador es matemáticamente equivalente a descuantizar las entradas, implicar y, a continuación, cuantificar la salida.
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
ms.openlocfilehash: 5b98e1f57268cab70c2fb672991bce3d67419db8
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417963"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a>DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC estructura (directml.h)
Realiza una convolución del *filterTensor* con *inputTensor*. Este operador realiza la convolución hacia delante en datos cuantificados. Este operador es matemáticamente equivalente a descuantizar las entradas, implicar y, a continuación, cuantificar la salida. 

Las funciones lineales de cuantificación usadas por este operador son las funciones de cuantificación lineales.

### <a name="dequantize-function"></a>Función Dequantize

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>Función Quantize

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

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

Tensor que contiene los datos de entrada. Las dimensiones esperadas de *InputTensor* son `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de escala de entrada. Las dimensiones esperadas de son `InputScaleTensor` `{ 1, 1, 1, 1 }` . Este valor de escala se usa para descuantizar los valores de entrada.


`InputZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor opcional que contiene los datos de punto cero de entrada. Las dimensiones esperadas de *InputZeroPointTensor* son `{ 1, 1, 1, 1 }` . Este valor de punto cero se usa para descuantizar los valores de entrada.


`FilterTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de filtro. Las dimensiones esperadas del *filterTensor* son `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de escala de filtro. Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `FilterScaleTensor` `{ 1, 1, 1, 1 }` una `{ 1, OutputChannelCount, 1, 1 }` cuantificación por canal. Este valor de escala se usa para descuantizar los valores de filtro.


`FilterZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor opcional que contiene los datos de punto cero de filtro. Las dimensiones esperadas de *FilterZeroPointTensor* son si se requiere una cuantificación por tensor o si se requiere una cuantificación por `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` canal. Este valor de punto cero se usa para descuantizar los valores de filtro.


`BiasTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de sesgo. El tensor de sesgo es un tensor que contiene datos que se difunden a través del tensor de salida al final de la convolución que se agrega al resultado. Las dimensiones esperadas de BiasTensor son `{ 1, OutputChannelCount, 1, 1 }` para 4D.


`OutputScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de escala de salida. Las dimensiones esperadas de OutputScaleTensor son `{ 1, 1, 1, 1 }` . Este valor de escala de entrada se usa para cuantificar los valores de salida de convolución.


`OutputZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor opcional que contiene los datos de punto cero de filtro. Las dimensiones esperadas de OutputZeroPointTensor son `{ 1, 1, 1, 1 }` . Este valor de punto cero de entrada se usa para cuantificar la convolución de los valores de salida.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor en el que se escriben los resultados. Las dimensiones esperadas de OutputTensor son `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de dimensiones espaciales para la operación de convolución. Las dimensiones espaciales son las dimensiones inferiores del tensor *FilterTensor* del filtro de convolución. Este valor también determina el tamaño de las matrices *Strides*, *Posición,* *StartPadding* y *EndPadding.* Solo se admite un valor de 2.


`Strides`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Los avances de la operación de convolución. Estos strides se aplican al filtro de convolución. Son independientes de los avances de tensor incluidos [en DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).


`Dilations`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Las convoluciones de la operación de convolución. Las reparaciones son avances que se aplican a los elementos del kernel de filtro. Esto tiene el efecto de simular un kernel de filtro mayor mediante el relleno de los elementos internos del kernel de filtro con ceros.


`StartPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Valores de relleno que se aplicarán al principio de cada dimensión espacial del filtro y del tensor de entrada de la operación de convolución.


`EndPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Valores de relleno que se aplicarán al final de cada dimensión espacial del filtro y del tensor de entrada de la operación de convolución.


`GroupCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de grupos en los que se va a dividir la operación de convolución. *GroupCount* se puede usar para lograr la convolución por profundidad estableciendo *GroupCount* en el número de canales de entrada. Esto divide la convolución en una convolución independiente por canal de entrada. 

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensor
* *FilterTensor* y *FilterZeroPointTensor* deben tener el mismo *DataType.*
* *InputTensor* y *InputZeroPointTensor* deben tener el mismo *DataType.*
* *OutputTensor* y `OutputZeroPointTensor` deben tener el mismo *DataType.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
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
| OutputTensor | Resultados | 4 | INT8, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |