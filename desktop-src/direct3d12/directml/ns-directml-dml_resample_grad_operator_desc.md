---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Calcula los degradados de propagación de la misma para volver a muestrear (vea [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
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
ms.openlocfilehash: 5808381f2e812ac20399b46672e51acd063bc6a5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721299"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a>DML_RESAMPLE_GRAD_OPERATOR_DESC estructura (directml. h)

Calcula los degradados de propagación de la misma para volver a muestrear (vea [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).

**DML_RESAMPLE1_OPERATOR_DESC** cambia el tamaño de las dimensiones arbitrarias de la tensores de entrada mediante el muestreo de vecino más próximo o la interpolación bilineal. Dado un *InputGradientTensor* con los mismos tamaños que la *salida* de una **DML_RESAMPLE1_OPERATOR_DESC** equivalente, este operador genera una *OutputGradientTensor* con los mismos tamaños que la *entrada* de la **DML_RESAMPLE1_OPERATOR_DESC**.

Como ejemplo, considere una **DML_RESAMPLE1_OPERATOR_DESC** que realiza un ajuste de escala de 1,5 x más cercano en el ancho y 0.5 x en el alto.

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

Observe que el elemento 0 de la entrada tensores (con el valor 1) contribuye a dos elementos de la salida, el primer elemento (con el valor 2) contribuye a un elemento en la salida, y los elementos 2º y tercero (con los valores 3 y 4) contribuyen a no tener elementos de la salida.

El **DML_RESAMPLE_GRAD_OPERATOR_DESC** correspondiente llevaría a cabo lo siguiente.

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

Observe que los valores de *OutputGradientTensor* representan las contribuciones ponderadas de ese elemento a la *OutputTensor* durante el operador de **DML_RESAMPLE1_OPERATOR_DESC** original.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

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

## <a name="members"></a>Miembros

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de degradado entrante. Normalmente se obtiene a partir de la salida de la propagación de una capa anterior. Normalmente, este tensores tendría el mismo tamaño que la *salida* de la [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) correspondiente en el paso de avance.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de salida que contiene los degradados retropagados. Normalmente, este tensores tendría el mismo tamaño que la *entrada* del [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) correspondiente en el paso de avance.

`InterpolationMode`

Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Consulte *InterpolationMode* en [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de elementos de las matrices *Scales*, *InputPixelOffsets* y *OutputPixelOffsets* . Este valor debe ser igual al *DimensionCount* proporcionado en *InputGradientTensor* y *OutputGradientTensor*.

`Scales`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Vea *escalas* en [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`InputPixelOffsets`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Consulte *InputPixelOffsets* en [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`OutputPixelOffsets`

Tipo: \_ tamaño de campo \_ \_ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***

Consulte *OutputPixelOffsets* en [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensores
*InputGradientTensor* y *OutputGradientTensor* deben tener el mismo *tipo de texto*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |