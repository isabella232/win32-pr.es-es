---
title: firstbithigh (función)
description: Obtiene la ubicación del primer bit establecido a partir del bit de orden más alto y trabajando hacia abajo, por componente.
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- función firstbithigh HLSL
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c62b6f090126887930415fc408da4f4a6c17bc4a99429db61fd298960c07e6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949705"
---
# <a name="firstbithigh-function"></a>firstbithigh (función)

Obtiene la ubicación del primer bit establecido a partir del bit de orden más alto y trabajando hacia abajo, por componente.

## <a name="syntax"></a>Sintaxis

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Ubicación del primer bit establecido.

## <a name="remarks"></a>Comentarios

Para un entero con signo, el primer bit significativo es cero para un número negativo.

También están disponibles las siguientes versiones sobrecargadas:

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
```

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 