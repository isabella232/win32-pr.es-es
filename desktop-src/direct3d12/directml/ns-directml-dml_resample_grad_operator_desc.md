---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Calcula los degradados de repropagation para Resample [(vea DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: ff2660257fa619edb72f10efb419f3c15f43fbde
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549730"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a>DML_RESAMPLE_GRAD_OPERATOR_DESC estructura (directml.h)

Calcula los degradados de repropagation para Resample [(vea DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).

**DML_RESAMPLE1_OPERATOR_DESC** escala las dimensiones arbitrarias del tensor de entrada mediante el muestreo del vecino más cercano o la interpolación bilineal. Dado un *inputGradientTensor* con los  mismos tamaños que la salida de un **DML_RESAMPLE1_OPERATOR_DESC** equivalente, este operador genera  un *outputGradientTensor* con los mismos tamaños que la **entrada del DML_RESAMPLE1_OPERATOR_DESC**.

Por ejemplo, considere  una DML_RESAMPLE1_OPERATOR_DESC que realiza un escalado de vecino más próximo de 1,5 veces el ancho y 0,5 veces el alto.

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

Observe cómo el elemento 0 del tensor de entrada (con el valor 1) contribuye a dos elementos de la salida, el primer elemento (con el valor 2) contribuye a un elemento de la salida y los elementos 2 y 3 (con los valores 3 y 4) no contribuyen a ningún elemento de la salida.

La propiedad **DML_RESAMPLE_GRAD_OPERATOR_DESC** realizaría lo siguiente.

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

Observe que los valores de *OutputGradientTensor* representan las contribuciones ponderadas de ese elemento al *outputTensor* durante el operador **DML_RESAMPLE1_OPERATOR_DESC** original.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a>Members

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de degradado entrante. Normalmente, esto se obtiene a partir de la salida de la repropagación de una capa anterior. Normalmente, este tensor tendría los  mismos tamaños que la salida de la DML_RESAMPLE1_OPERATOR_DESC [en](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) el paso hacia delante.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida que contiene los degradados de propiedad pendiente. Normalmente, este tensor tendría los  mismos tamaños que la entrada del DML_RESAMPLE1_OPERATOR_DESC [correspondiente](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) en el paso hacia delante.

`InterpolationMode`

Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Vea *InterpolationMode* en [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de elementos de las *matrices Scales*, *InputPixelOffsets* y *OutputPixelOffsets.* Este valor debe ser igual *al dimensioncount* proporcionado en *InputGradientTensor* y *OutputGradientTensor*.

`Scales`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Vea *Escalas* en [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`InputPixelOffsets`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Vea *InputPixelOffsets* en [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`OutputPixelOffsets`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Vea *OutputPixelOffsets* en [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensor
*InputGradientTensor* y *OutputGradientTensor* deben tener el mismo *DataType.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Resultados | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |