---
title: Función Buffer::Load(int, uint)
description: Lee los datos del búfer y devuelve el estado de la operación. | Función Buffer::Load(int, uint)
ms.assetid: 0C7FC522-C962-4467-AA3E-6611064C188B
keywords:
- Carga de la función HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eccd5c367e593559b6a719777dfd1535ae2d423a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263844"
---
# <a name="bufferloadint-uint-function"></a>Función Buffer::Load(int, uint)

Lee los datos del búfer y devuelve el estado de la operación.

## <a name="syntax"></a>Sintaxis

``` syntax
 Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Tipo: **int**

Ubicación del búfer.

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación **Sample**, **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se tomaron valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Escriba:

El tipo de valor devuelto coincide con el tipo de la declaración del [**objeto Buffer.**](sm5-object-buffer.md)

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="examples"></a>Ejemplos

En este ejemplo se muestra cómo usar **Cargar**:

``` syntax
Buffer<float4> myBuffer;
float loc;
uint status;
float4 myColor = myBuffer.Load( loc , status );
```

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos de carga](buffer-load.md)
</dt> </dl>

 

 
