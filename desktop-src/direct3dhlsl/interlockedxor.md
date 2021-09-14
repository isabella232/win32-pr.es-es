---
title: Función InterlockedXor (referencia hlsl)
description: Realiza un xor atómico garantizado.
ms.assetid: 844ca31f-d051-4713-b9e1-dd6712ad36ca
keywords:
- Función HLSL de InterlockedXor
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8ecaf0aa78a3bd2c1d79d10bea1e97299605398
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970719"
---
# <a name="interlockedxor-function-hlsl-reference"></a>Función InterlockedXor (referencia hlsl)

Realiza un xor atómico garantizado.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedXor(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*dest* \[ En\]
</dt> <dd>

Tipo: **R**

Dirección de destino.

</dd> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **T**

Valor de entrada.

</dd> <dt>

*valor \_ de salida* \[ original\]
</dt> <dd>

Tipo: **T**

Opcional. Valor de entrada original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta operación solo se puede realizar en recursos con tipo int o uint y variables de memoria compartida. Hay dos usos posibles para esta función. La primera es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza un XOR atómico de valor en el registro de memoria compartida al que hace referencia dest. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza un valor XORof atómico en la ubicación del recurso a la que hace referencia dest. La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest. Esta operación sobrecargada solo está disponible cuando R es legible y grabable.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|  x     |  x   | x      |  x       | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




