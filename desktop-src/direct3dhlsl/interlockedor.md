---
title: Interbloqueo (función, referencia de HLSL)
description: Realiza una atómica o atómica garantizada.
ms.assetid: ecbe6b2f-8eff-41d7-9ca3-4487c9ffeaf6
keywords:
- HLSL de la función interbloquet
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36ab900416d6d04e0e47a843aa345c1a01318c50
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2020
ms.locfileid: "104997032"
---
# <a name="interlockedor-function-hlsl-reference"></a>Interbloqueo (función, referencia de HLSL)

Realiza una atómica o atómica garantizada.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedOr(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*dest* \[ de\]
</dt> <dd>

Tipo: **R**

Dirección de destino.

</dd> <dt>

*valor* \[ de de\]
</dt> <dd>

Tipo: **T**

Valor de entrada.

</dd> <dt>

*\_ valor original* \[ fuera\]
</dt> <dd>

Tipo: **T**

Opcional. Valor de entrada original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta operación solo se puede realizar en recursos con tipo int o uint y variables de memoria compartida. Hay dos usos posibles para esta función. El primero es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza una atomicidad o de valor en el registro de memoria compartida al que hace referencia dest. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza una atómica o de valor en la ubicación del recurso al que hace referencia dest. La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest. Esta operación sobrecargada solo está disponible cuando R es legible y grabable.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




