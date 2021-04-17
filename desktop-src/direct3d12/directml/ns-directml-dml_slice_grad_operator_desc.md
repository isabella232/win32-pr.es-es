---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Calcula los degradados de propagación de la misma para el segmento (vea [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
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
ms.openlocfilehash: 63ea67454965d976247c3cdd50aa183f6a676138
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721249"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a>DML_SLICE_GRAD_OPERATOR_DESC estructura (directml. h)

Calcula los degradados de propagación de la misma para el segmento (vea [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).

Recuerde que [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extrae una subregión de una tensores de entrada. Dado un *InputGradientTensor* con los mismos tamaños que la *salida* de una **DML_SLICE1_OPERATOR_DESC** equivalente, este operador genera una *OutputGradientTensor* con los mismos tamaños que la *entrada* de **DML_SLICE1_OPERATOR_DESC**. Los elementos segmentados se propagan a la salida y todos los demás elementos se establecen en 0.

Como ejemplo, considere un **DML_SLICE1_OPERATOR_DESC** que extrae los siguientes elementos de un tensores:

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

Si se proporciona el mismo / *tamaño* / de InputWindowOffsets,*al* igual que en el ejemplo anterior, este operador llevaría a cabo la transformación siguiente.

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

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

Tensores de degradado entrante. Normalmente se obtiene a partir de la salida de la propagación de una capa anterior. Normalmente, este tensores tendría el mismo tamaño que la *salida* de la [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) correspondiente en el paso de avance.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de salida que contiene los degradados retropagados. Normalmente, este tensores tendría el mismo tamaño que la *entrada* de la [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) correspondiente en el paso de avance.

`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de elementos de las matrices *InputWindowOffsets*, *InputWindowSizes* y *InputWindowStrides* . Este valor debe ser igual al *DimensionCount* proporcionado en *InputGradientTensor* y *OutputGradientTensor*.

`InputWindowOffsets`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consulte *InputWindowOffsets* en [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

`InputWindowSizes`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consulte *InputWindowSizes* en [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

`InputWindowStrides`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consulte *InputWindowStrides* en [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

Tenga en cuenta que, a diferencia de **DML_SLICE1_OPERATOR_DESC**, este operador requiere progresas distintos de cero. Esto se debe a que, con un intervalo de cero, es ambiguo en qué elemento de entrada se debe asignar a cada elemento de salida y, por tanto, no se puede realizar la propagación. Como **DML_SLICE1_OPERATOR_DESC**, los progresos negativos voltean la dirección de la ventana de entrada a lo largo de ese eje.

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensores
*InputGradientTensor* y *OutputGradientTensor* deben tener el mismo *DataType* y *DimensionCount*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Entrada | de 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputGradientTensor | Output | de 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |