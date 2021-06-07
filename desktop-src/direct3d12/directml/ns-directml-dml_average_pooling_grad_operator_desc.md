---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Calcula los degradados de repropagación para la agrupación media [(consulte DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: aaa2b5d2becac421214afe7c643426c1c93cf899
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418014"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a>DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC estructura (directml.h)

Calcula los degradados de repropagación para la agrupación media [(consulte DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).

Considere una 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, sin relleno y un paso de 1, que realiza lo siguiente.

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

Cada ventana 2x2 del tensor de entrada se promedia para generar un elemento de la salida (lectura de ceros para los elementos más allá del borde). Este es un ejemplo de la salida de DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC **parámetros** similares.

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

Observe que los valores de *OutputGradientTensor* representan las contribuciones ponderadas de ese elemento al *outputTensor* durante el operador [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) original.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a>Miembros

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de degradado entrante. Normalmente, esto se obtiene a partir de la salida de la repropagación de una capa anterior. Normalmente, este tensor tendría los  mismos tamaños que la salida de la DML_AVERAGE_POOLING_OPERATOR_DESC [en](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) el paso hacia delante.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida que contiene los degradados de propiedad pendiente. Normalmente, este tensor tendría los  mismos tamaños que la entrada de la DML_AVERAGE_POOLING_OPERATOR_DESC [en](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) el paso hacia delante.

`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de elementos de las matrices *Strides,* *WindowSize,* *StartPadding* y *EndPadding.* Este valor debe ser igual al recuento de dimensiones espaciales. El recuento de dimensiones espaciales es 2 si se proporcionan tensores 4D, o 3 si se proporcionan tensores 5D.

`Strides`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Vea *Strides* en [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`WindowSize`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Vea *WindowSize* en [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`StartPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Vea *StartPadding* [en DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`EndPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Vea *EndPadding* en [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`IncludePadding`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

Vea *IncludePadding* [en DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensor
*InputGradientTensor* y *OutputGradientTensor* deben tener los mismos *DataType* y *DimensionCount.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Entrada | De 4 a 5 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Resultados | De 4 a 5 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |