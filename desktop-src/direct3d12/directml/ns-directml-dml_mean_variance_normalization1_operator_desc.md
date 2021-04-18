---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Realiza una función de normalización de varianza media en la tensores de entrada. Este operador calculará la media y la varianza de la tensores de entrada para realizar la normalización.
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
ms.openlocfilehash: f3302f8081ed4bf64fa858ac3e303519089d01fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721276"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a>DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC estructura (directml. h)
Realiza una función de normalización de varianza media en la tensores de entrada. Este operador calculará la media y la varianza de la tensores de entrada para realizar la normalización. Este operador realiza el siguiente cálculo.

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

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

Tensores que contiene los datos de entrada. Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, Height, Width }` .


`ScaleTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores opcional que contiene los datos de la escala. Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, Height, Width }` . Cualquier dimensión se puede reemplazar por 1 para difundirla en esa dimensión. Este tensores es obligatorio si se usa *BiasTensor* .


`BiasTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores opcional que contiene los datos de la diferencia. Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, Height, Width }` . Cualquier dimensión se puede reemplazar por 1 para difundirla en esa dimensión. Este tensores es obligatorio si se usa *ScaleTensor* .


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores en el que se van a escribir los resultados. Las dimensiones de este tensores son `{ BatchCount, ChannelCount, Height, Width }` .


`AxisCount`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b>

Número de ejes. Este campo determina el tamaño de la matriz de *ejes* .


`Axes`

Tipo: \_ tamaño de campo \_ \_ (AxisCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \*** 

Ejes en los que se va a calcular la media y la varianza.


`NormalizeVariance`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b>

**True** si la capa de normalización incluye la varianza en el cálculo de la normalización. En caso contrario, **false**. Si es **false**, la ecuación de normalización es `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .


`Epsilon`

Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

Valor de épsilon que se va a usar para evitar la división por cero. Se recomienda un valor de 0,00001 como predeterminado.


`FusedActivation`

Tipo: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***

Capa de activación con fusible opcional que se va a aplicar después de la normalización.


## <a name="remarks"></a>Observaciones
**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** es un superconjunto de la funcionalidad de [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc). Aquí, el establecimiento de la matriz de **ejes** en `{ 0, 2, 3 }` es el equivalente de establecer *CrossChannel* en **false** en **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; al establecer la matriz de **ejes** en `{ 1, 2, 3 }` es equivalente a establecer *Crosschannel* en **true**.

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensores
* *InputTensor* y *OutputTensor* deben tener el mismo *tamaño*.
* *BiasTensor*, *InputTensor*, *OutputTensor* y *ScaleTensor* deben tener el mismo *tipo de texto*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Dimensions | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrada | {BatchCount, ChannelCount, height, width} | 4 | FLOAT32, FLOAT16 |
| ScaleTensor | Entrada opcional | {ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth} | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Entrada opcional | { BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth } | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | {BatchCount, ChannelCount, height, width} | 4 | FLOAT32, FLOAT16 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |

## <a name="see-also"></a>Vea también

[Usar operadores combinados para mejorar el rendimiento](../dml-fused-activations.md)