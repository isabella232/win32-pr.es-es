---
title: countbits (función)
description: Cuenta el número de bits (por componente) establecido en el entero de entrada.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- función countbits HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f3816152b91fd03348e64c7a36dd41e8b620bd5e5ef8f4463538c44ef974485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793973"
---
# <a name="countbits-function"></a>countbits (función)

Cuenta el número de bits (por componente) establecido en el entero de entrada.

## <a name="syntax"></a>Sintaxis

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **uint**

Valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint**

Número de bits.

## <a name="remarks"></a>Observaciones

También están disponibles las siguientes versiones sobrecargadas:

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




