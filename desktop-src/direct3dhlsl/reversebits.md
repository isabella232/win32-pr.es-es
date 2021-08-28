---
title: reversebits (función)
description: Invierte el orden de los bits, por componente.
ms.assetid: dad46e25-9980-4645-98eb-d834db704fc8
keywords:
- función reversebits HLSL
topic_type:
- apiref
api_name:
- reversebits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9f055764c04f552fe9d7afda2adf1e401352cf3fc3dd3ead16c4ca6377bd4fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853725"
---
# <a name="reversebits-function"></a>reversebits (función)

Invierte el orden de los bits, por componente.

## <a name="syntax"></a>Sintaxis

``` syntax
uint reversebits(
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

Valor de entrada, con el orden de bits invertido.

## <a name="remarks"></a>Comentarios

También están disponibles las siguientes versiones sobrecargadas:

``` syntax
uint2 reversebits(uint2 value);
uint3 reversebits(uint3 value);
uint4 reversebits(uint4 value);
```

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




