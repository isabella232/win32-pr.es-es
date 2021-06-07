---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Calcula los degradados de apropagación de backpropagation para Slice [(consulte DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
helpviewer_keywords:
- DML_SLICE_GRAD_OPERATOR_DESC
- DML_SLICE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_SLICE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_SLICE_GRAD_OPERATOR_DESC, DML_SLICE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
- directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
ms.openlocfilehash: a22efe9b0b74f5fdc7b498b97784086f40f243b9
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417988"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a>DML_SLICE_GRAD_OPERATOR_DESC estructura (directml.h)

Calcula los degradados de apropagación de backpropagation para Slice [(consulte DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).

Recuerde que [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extrae una subregión de un tensor de entrada. Dado un *inputGradientTensor* con los  mismos tamaños que la salida de un **DML_SLICE1_OPERATOR_DESC** equivalente, este operador genera  un *outputGradientTensor* con los mismos tamaños que la **entrada de DML_SLICE1_OPERATOR_DESC**. Los elementos segmentados se propagan a la salida y todos los demás elementos se establecen en 0.

Por ejemplo, considere **una** DML_SLICE1_OPERATOR_DESC que extrae los siguientes elementos de un tensor:

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

Si se proporcionan los mismos *Strides de tamaños inputWindowOffsets* que en el ejemplo anterior, este operador realizaría /  /  la transformación siguiente.

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis

```cpp
struct DML_SLICE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* InputWindowOffsets;
  _Field_size_(DimensionCount) const UINT* InputWindowSizes;
  _Field_size_(DimensionCount) const INT* InputWindowStrides;
};
```

## <a name="members"></a>Miembros

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de degradado entrante. Esto se obtiene normalmente a partir de la salida de la repropagación de una capa anterior. Normalmente, este tensor tendría los  mismos tamaños que la salida de la DML_SLICE1_OPERATOR_DESC [correspondiente](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) en el paso hacia delante.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida que contiene los degradados de propiedad pendiente. Normalmente, este tensor tendría los  mismos tamaños que la entrada de la DML_SLICE1_OPERATOR_DESC [correspondiente](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) en el paso hacia delante.

`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de elementos de las *matrices InputWindowOffsets,* *InputWindowSizes* y *InputWindowStrides.* Este valor debe ser igual *al dimensioncount* proporcionado en *InputGradientTensor* y *OutputGradientTensor*.

`InputWindowOffsets`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Vea *InputWindowOffsets* en [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

`InputWindowSizes`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Vea *InputWindowSizes* en [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

`InputWindowStrides`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

Vea *InputWindowStrides* en [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

Tenga en cuenta **que DML_SLICE1_OPERATOR_DESC**, este operador requiere avances distintos de cero. Esto se debe a que, con un paso cero, es ambiguo en cuanto a qué elemento de entrada se debe asignar a cada elemento de salida y, por tanto, no se puede realizar la repropagación. Al **DML_SLICE1_OPERATOR_DESC**, los avances negativos invierten la dirección de la ventana de entrada a lo largo de ese eje.

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensor
*InputGradientTensor* y *OutputGradientTensor* deben tener los mismos *DataType* y *DimensionCount.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputGradientTensor | Resultados | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |