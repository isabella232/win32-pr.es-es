---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcula los degradados de repropagación para la [normalización por lotes.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: 2b94ac1dcf389d424aaf74d615f36cdf7acc804c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550440"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a>DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)

Calcula los degradados de repropagación para la [normalización por lotes.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) **DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** realiza varios cálculos, que se detallan en las descripciones de salida independientes.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.5 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de entrada. Suele ser el mismo tensor que se proporcionó que *inputTensor* para [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) en el paso de reenvío.

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de degradado entrante. Normalmente, esto se obtiene a partir de la salida de la repropagación de una capa anterior. Este tensor debe tener los mismos tamaños de dimensión que *InputTensor.*

`MeanTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos medio. Suele ser el mismo tensor que se proporcionó que *meanTensor* [**para DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) en el paso hacia delante.

Las dimensiones que no tengan el mismo tamaño que la dimensión correspondiente de *InputTensor* deben tener un tamaño de 1 para que se puedan difundir para que coincidan con la entrada.

Por ejemplo, los tamaños siguientes son aceptables.

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

El siguiente es un error, ya que, para que sea compatible con la difusión, las dimensiones que no coincidan deben tener el tamaño 1.

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de varianza. Suele ser el mismo tensor que se proporcionó que *varianceTensor* [**para DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) en el paso hacia delante. Este tensor debe tener los mismos tamaños de dimensión *que MeanTensor.*

`ScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de escala. Suele ser el mismo tensor que se proporcionó que *ScaleTensor* [**para DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) en el pase hacia delante. Este tensor debe tener los mismos tamaños de dimensión *que MeanTensor.*

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Para cada valor correspondiente de las entradas, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .

Este tensor debe tener los mismos tamaños de dimensión *que InputTensor* / *InputGradientTensor*.

`OutputScaleGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Este tensor debe tener los mismos tamaños de dimensión *que MeanTensor* / *VarianceTensor* / *ScaleTensor'.*

El siguiente cálculo se realiza o cada valor correspondiente en las entradas.

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

se `sum` calcula en todas las dimensiones que deben difundirse. Si no se necesita difusión, no se necesita ninguna suma.

Aquí tiene un ejemplo.

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

El elemento [0, **0,** 0, 0] de es la suma de para los `OutputScaleGradientTensor` `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` 90 elementos (3 \* 5 \* 6) [[0,2], **0**, [0,4], [0,5]].

`OutputBiasGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Este tensor debe tener los mismos tamaños de dimensión *que MeanTensor* / *VarianceTensor* / *ScaleTensor'.*

El siguiente cálculo se realiza o cada valor correspondiente en las entradas.

`OutputBiasGradient = sum(InputGradient)`  

se calcula en todas las dimensiones que se deben `sum` difundir (vea el ejemplo de *OutputScaleGradientTensor).* Si no se necesita ninguna difusión, no se necesita ninguna suma.

`Epsilon`

Tipo: **[FLOAT](../../winprog/windows-data-types.md)**

Valor pequeño que se agrega a la varianza para evitar cero.

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Restricciones de Tensor
*InputGradientTensor,* *InputTensor*, *MeanTensor,* *OutputBiasGradientTensor,* *OutputGradientTensor,* *OutputScaleGradientTensor,* *ScaleTensor* y *VarianceTensor* deben tener los mismos *dataType* y *DimensionCount.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16 |
| InputGradientTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16 |
| MeanTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16 |
| VarianceTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Resultados | De 1 a 8 | FLOAT32, FLOAT16 |
| OutputScaleGradientTensor | Resultados | De 1 a 8 | FLOAT32, FLOAT16 |
| OutputBiasGradientTensor | Resultados | De 1 a 8 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |