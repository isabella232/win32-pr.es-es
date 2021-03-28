---
title: firstbitlow (función)
description: Devuelve la ubicación del primer bit establecido empezando por el bit de orden más bajo y trabajando hacia arriba, por componente.
ms.assetid: 204250f3-1a9b-445d-bd16-4cc9a5d9d60a
keywords:
- firstbitlow (de función HLSL
topic_type:
- apiref
api_name:
- firstbitlow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a647314383bc022b7c3b3e1b5a255a42a099c620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077945"
---
# <a name="firstbitlow-function"></a>firstbitlow (función)

Devuelve la ubicación del primer bit establecido empezando por el bit de orden más bajo y trabajando hacia arriba, por componente.

## <a name="syntax"></a>Sintaxis

``` syntax
int firstbitlow(
  in int value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de de\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

La ubicación del primer bit establecido.

## <a name="remarks"></a>Observaciones

También están disponibles las siguientes versiones sobrecargadas:

``` syntax
uint2 firstbitlow(uint2 value);
uint3 firstbitlow(uint3 value);
uint4 firstbitlow(uint4 value);
```

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 