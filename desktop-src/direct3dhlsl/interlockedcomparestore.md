---
title: Función InterlockedCompareStore (referencia hlsl)
description: Compara de forma atómica el destino con el valor de comparación. Si son idénticos, el destino se sobrescribe con el valor de entrada.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- Función HLSL interlockedCompareStore
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7dbf13629b9c3b9b38cc3bd72a8a992ab40bd09c0333c155a7c109f71466f23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119249"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a>Función InterlockedCompareStore (referencia hlsl)

Compara de forma atómica el destino con el valor de comparación. Si son idénticos, el destino se sobrescribe con el valor de entrada.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*dest* \[ En\]
</dt> <dd>

Tipo: **R**

Dirección de destino.

</dd> <dt>

*comparar \_ valor* \[ en\]
</dt> <dd>

Tipo: **T**

Valor de comparación.

</dd> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **T**

Valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Compara de forma atómica el valor al que  hace referencia *dest* con el valor compare y almacena el valor en la ubicación a la que *hace referencia dest* si los valores coinciden. *\_* Esta operación solo se puede realizar en recursos con tipo **int** **o uint** y variables de memoria compartida. Hay dos usos posibles para esta función. La primera es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza la operación en el registro de memoria compartida al que hace referencia *dest*. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza la operación en la ubicación del recurso a la que hace referencia *dest*.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|  x     | x    |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




