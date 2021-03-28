---
title: Función InterlockedMin (referencia de HLSL)
description: Realiza un mínimo atómico garantizado.
ms.assetid: a6d3d81c-45d7-4e15-b8ec-fa2e30f854ce
keywords:
- InterlockedMin de función HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c85be82f87ce62d03c824e8cd895166c18c262c
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2020
ms.locfileid: "104420156"
---
# <a name="interlockedmin-function-hlsl-reference"></a>Función InterlockedMin (referencia de HLSL)

Realiza un mínimo atómico garantizado.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedMin(
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

Esta operación solo se puede realizar en los recursos con tipo int y uint y las variables de memoria compartida. Hay dos usos posibles para esta función. El primero es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza un mínimo atómico del valor en el registro de memoria compartida al que hace referencia dest. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza una mínima atómica de valor en la ubicación del recurso a la que hace referencia dest. La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest. Esta operación sobrecargada solo está disponible cuando R es legible y grabable.

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

 

 




