---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Suma los elementos de una tensores a lo largo de un eje, escribiendo el recuento de ejecución de la suma en el tensores de salida.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 955e70a8cfbb57995d77d73567238d082b96999b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721288"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a>DML_CUMULATIVE_SUMMATION_OPERATOR_DESC estructura (directml. h)

Suma los elementos de una tensores a lo largo de un eje, escribiendo el recuento de ejecución de la suma en el tensores de salida.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```



## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de entrada que contiene los elementos que se van a sumar.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de salida en el que se van a escribir las sumas acumulativas resultantes. Este tensores debe tener los mismos tamaños y tipo de datos que *InputTensor*.


`Axis`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Índice de la dimensión de la que se van a sumar los elementos. Este valor debe ser menor que el valor de *DimensionCount* de *InputTensor*.


`AxisDirection`

Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Uno de los valores de la enumeración [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) . Si se establece en **DML_AXIS_DIRECTION_INCREASING**, la suma se produce recorriendo el tensores a lo largo del eje especificado por el índice de elemento ascendente. Si se establece en **DML_AXIS_DIRECTION_DECREASING**, el valor de inverso es true y la suma se produce recorriendo los elementos por índice descendente.


`HasExclusiveSum`




## <a name="remarks"></a>Observaciones
Este operador es compatible con la ejecución en contexto, lo que significa que se permite que el *OutputTensor* alias del *InputTensor* durante el enlace.

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensores
*InputTensor* y *OutputTensor* deben tener el mismo *tipo de texto* y *tamaños*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |