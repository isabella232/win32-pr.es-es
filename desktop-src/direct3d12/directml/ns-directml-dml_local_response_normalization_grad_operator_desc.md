---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcula los degradados de repropagación para [la normalización de la respuesta local.](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)
helpviewer_keywords:
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_local_response_normalization_grad_operator_desc
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: e858b8ce20df4b1bf12ac9efe360941eb93c54d1
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550410"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a>DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)

Calcula los degradados de repropagación para [la normalización de la respuesta local.](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc)

El tipo de datos y el tamaño de todos los tensores deben ser los mismos.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.5 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    BOOL CrossChannel;
    UINT LocalSize;
    FLOAT Alpha;
    FLOAT Beta;
    FLOAT Bias;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de entrada. Los tamaños de  este tensor deben ser `{ BatchCount, ChannelCount, Height, Width }` .

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de degradado entrante. Normalmente, esto se obtiene a partir de la salida de la repropagación de una capa anterior.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida que contiene los degradados de propiedad pendiente.

`CrossChannel`

Tipo: **[BOOL](../../winprog/windows-data-types.md)**

**TRUE** si la capa LRN suma entre canales; **FALSE** si la capa LRN suma entre dimensiones espaciales.

`LocalSize`

Tipo: **[UINT](../../winprog/windows-data-types.md)**

Número máximo de elementos que se suma por dimensión (la región local se recorta para que todos los elementos estén dentro de los límites). Si *CrossChannel* es **TRUE**, este es el ancho y alto de la región local. Si *CrossChannel* es **FALSE,** este es el número de elementos de la región local. Este valor debe ser al menos 1.

`Alpha`

Tipo: **[FLOAT](../../winprog/windows-data-types.md)**

Valor del parámetro de escalado. Se recomienda un valor de 0,0001 como valor predeterminado.

`Beta`

Tipo: **[FLOAT](../../winprog/windows-data-types.md)**

Valor del exponente. Se recomienda un valor de 0,75 como valor predeterminado.

`Bias`

Tipo: **[FLOAT](../../winprog/windows-data-types.md)**

Valor de sesgo. Se recomienda un valor de 1 como valor predeterminado.

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Restricciones de Tensor
*InputGradientTensor,* *InputTensor* y *OutputGradientTensor* deben tener los mismos *datatype* y *tamaños.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| InputGradientTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Resultados | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |