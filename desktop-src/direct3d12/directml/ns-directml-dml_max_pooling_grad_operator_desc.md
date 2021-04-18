---
UID: NS:directml.DML_MAX_POOLING_GRAD_OPERATOR_DESC
title: DML_MAX_POOLING_GRAD_OPERATOR_DESC
description: Calcula los degradados de propagación de la memoria para la agrupación máxima (vea [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).
helpviewer_keywords:
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- DML_MAX_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_MAX_POOLING_GRAD_OPERATOR_DESC, DML_MAX_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: b7314cb6b9456d9ac9f99e90100085e86f88ffd9
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721363"
---
# <a name="dml_max_pooling_grad_operator_desc-structure-directmlh"></a>DML_MAX_POOLING_GRAD_OPERATOR_DESC estructura (directml. h)

Calcula los degradados de propagación de la memoria para la agrupación máxima (vea [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).

Considere una **DML_MAX_POOLING2_OPERATOR_DESC** 2x2 sin relleno ni dilations y un paso de 1, que realiza lo siguiente.

```
InputTensor             OutputTensor    IndicesTensor
[[1, 2, 3],   MaxPool    [[4, 4],        [[4, 4],
 [2, 4, 2],     -->       [6, 7]]         [7, 8]]
 [5, 6, 7]]
```

El elemento más grande de cada ventana de 2x2 en el tensores de entrada genera un elemento de la salida. A continuación se muestra un ejemplo de la salida de **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, dados parámetros similares.

```
InputTensor   InputGradientTensor            OutputGradientTensor
[[1, 2, 3],       [[1, 2],     MaxPoolGrad   [[0, 0, 0],
 [2, 4, 2],        [4, 5]]         -->        [0, 3, 0],
 [5, 6, 7]]                                   [0, 4, 5]]
```

En efecto, este operador usa *InputTensor* para determinar el índice del elemento más grande de cada ventana y distribuye los valores de *InputGradientTensor* a *OutputGradientTensor* basándose en estos índices. Donde se superponen los índices, se suman los valores. Los elementos de salida sin referencia tienen ceros.

En el caso de una operación de vinculación (donde más de un elemento de una ventana tiene el mismo valor máximo), se elige el elemento con el índice de elemento lógico más bajo.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis

```cpp
struct DML_MAX_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  _Field_size_(DimensionCount) const UINT* Dilations;
};
```

## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

La característica de entrada tensores. Suele ser el mismo tensores que se proporcionó como *InputTensor* para [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) en el paso de avance.

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de degradado entrante. Normalmente se obtiene a partir de la salida de la propagación de una capa anterior. Normalmente, este tensores tendría el mismo tamaño que la *salida* de la [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) correspondiente en el paso de avance.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de salida que contiene los degradados retropagados. Normalmente, este tensores tendría el mismo tamaño que la *entrada* del [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) correspondiente en el paso de avance.

`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de elementos de las matrices de los *progresos*, *Windows*, *StartPadding*, *EndPadding* y *Dilations* . Este valor debe ser igual al número de dimensiones espaciales (InputTensor DimensionCount-2). Dado que este operador solo admite decenas de 4D, el único valor válido para este parámetro es 2.

`Strides`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Vea los *avances* en [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`WindowSize`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consulte *Windows* en [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`StartPadding`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consulte *StartPadding* en [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`EndPadding`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consulte *EndPadding* en [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`Dilations`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consulte *Dilations* en [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensores
* *InputTensor* y *OutputGradientTensor* deben tener el mismo *tamaño*.
* *InputGradientTensor*, *InputTensor* y *OutputGradientTensor* deben tener el mismo *tipo de texto*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Dimensions | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrada | { BatchCount, ChannelCount, InputHeight, InputWidth } | 4 | FLOAT32, FLOAT16 |
| InputGradientTensor | Entrada | { BatchCount, ChannelCount, OutputHeight, OutputWidth } | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | { BatchCount, ChannelCount, InputHeight, InputWidth } | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |