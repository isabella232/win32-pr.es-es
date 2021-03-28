---
title: Función InterlockedCompareStore (referencia de HLSL)
description: Compara de forma atómica el destino con el valor de comparación. Si son idénticos, el destino se sobrescribe con el valor de entrada.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- InterlockedCompareStore de función HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ffb51bbe8fe8150d19a390e62640e64ded5c9
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2020
ms.locfileid: "104420158"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a>Función InterlockedCompareStore (referencia de HLSL)

Compara de forma atómica el destino con el valor de comparación. Si son idénticos, el destino se sobrescribe con el valor de entrada.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*dest* \[ de\]
</dt> <dd>

Tipo: **R**

Dirección de destino.

</dd> <dt>

*comparar \_ valor* \[ en\]
</dt> <dd>

Tipo: **T**

El valor de comparación.

</dd> <dt>

*valor* \[ de de\]
</dt> <dd>

Tipo: **T**

Valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Compara de forma atómica el valor al que hace referencia el *destino* con el *\_ valor de comparación* y almacena el *valor* en la ubicación a la que hace referencia *dest* si los valores coinciden. Esta operación solo se puede realizar en recursos con tipo **int** o **uint** y variables de memoria compartida. Hay dos usos posibles para esta función. El primero es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza la operación en el registro de memoria compartida al que hace referencia *dest*. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza la operación en la ubicación del recurso a la que hace referencia *dest*.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|  x     | x    |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




