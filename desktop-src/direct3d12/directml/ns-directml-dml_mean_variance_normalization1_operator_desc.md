---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Realiza una función de normalización de varianza media en el tensor de entrada. Este operador calculará la media y la varianza del tensor de entrada para realizar la normalización.
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: 759bf25d4b6a97e70c6de7708a5c9fd0bccae439
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803403"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a>DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC estructura (directml.h)

Realiza una función de normalización de varianza media en el tensor de entrada. Este operador calculará la media y la varianza del tensor de entrada para realizar la normalización. Este operador realiza el cálculo siguiente.

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```
## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de entrada. Las dimensiones de este tensor deben ser `{ BatchCount, ChannelCount, Height, Width }` .

`ScaleTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor opcional que contiene los datos de escala.

Si **DML_FEATURE_LEVEL** es menor que **DML_FEATURE_LEVEL_4_0**, las dimensiones de este tensor deben ser `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` . Las dimensiones ScaleBatchCount, ScaleHeight y ScaleWidth deben coincidir con *InputTensor* o establecerse en 1 para difundir automáticamente esas dimensiones a través de la entrada.

Si **DML_FEATURE_LEVEL** es mayor o igual que **DML_FEATURE_LEVEL_4_0**, cualquier dimensión se puede establecer en 1 y se difunde automáticamente para que coincida con *InputTensor*.

Este tensor es necesario si *se usa BiasTensor.*

`BiasTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***


Tensor opcional que contiene los datos de Bias.

Si **DML_FEATURE_LEVEL** es menor que **DML_FEATURE_LEVEL_4_0**, las dimensiones de este tensor deben ser `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` . Las dimensiones BiasBatchCount, BiasHeight y BiasWidth deben coincidir con *InputTensor* o establecerse en 1 para difundir automáticamente esas dimensiones a través de la entrada.

Si **DML_FEATURE_LEVEL** es mayor o igual que **DML_FEATURE_LEVEL_4_0**, cualquier dimensión se puede establecer en 1 y se difunde automáticamente para que coincida con *InputTensor*.

Este tensor es necesario si se usa *ScaleTensor.*

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor en el que se escriben los resultados. Las dimensiones de este tensor son `{ BatchCount, ChannelCount, Height, Width }` .

`AxisCount`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b>

Número de ejes. Este campo determina el tamaño de la matriz *Axes.*

`Axes`

Tipo: \_ Tamaño de campo \_ \_ (AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types) \*** 

Ejes a lo largo de los que se calculan la media y la varianza.

`NormalizeVariance`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

**TRUE** si la capa normalización incluye Varianza en el cálculo de normalización. De lo contrario, **FALSE**. Si **es FALSE**, la ecuación de normalización es `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .

`Epsilon`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

Valor de epsilon que se usará para evitar la división por cero. Se recomienda un valor de 0,00001 como valor predeterminado.

`FusedActivation`

Tipo: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***

Una capa de activación fusionada opcional que se aplicará después de la normalización.

## <a name="remarks"></a>Observaciones
**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** es un superconjunto de funcionalidad de [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc). Aquí, establecer la matriz **Axes** en equivale a establecer CrossChannel en FALSE en `{ 0, 2, 3 }` **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC;**  mientras que establecer la matriz **Axes** en es equivalente a establecer  `{ 1, 2, 3 }` *CrossChannel* en **TRUE.**

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de Tensor

*BiasTensor,* *InputTensor,* *OutputTensor* y *ScaleTensor* deben tener los mismos *DataType* y *DimensionCount.*

## <a name="tensor-support"></a>Compatibilidad con Tensor

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 y posteriores

| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Entrada opcional | De 1 a 8 | FLOAT32, FLOAT16 |
| BiasTensor | Entrada opcional | De 1 a 8 | FLOAT32, FLOAT16 |
| OutputTensor | Resultados | De 1 a 8 | FLOAT32, FLOAT16 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y posteriores

| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| ScaleTensor | Entrada opcional | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Entrada opcional | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Resultados | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Consulta también

[Uso de operadores fusionados para mejorar el rendimiento](../dml-fused-activations.md)
