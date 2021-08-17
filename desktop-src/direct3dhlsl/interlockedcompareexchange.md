---
title: Función InterlockedCompareExchange (referencia hlsl)
description: Compara de forma atómica el destino con el valor de comparación. Si son idénticos, el destino se sobrescribe con el valor de entrada. El valor original se establece en el valor original del destino.
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- Función HLSL interlockedCompareExchange
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46cf8c3fb0e3bc0b21c5bf8bc3d946851ce213b765731518d252495250071228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119259"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a>Función InterlockedCompareExchange (referencia hlsl)

Compara de forma atómica el destino con el valor de comparación. Si son idénticos, el destino se sobrescribe con el valor de entrada. El valor original se establece en el valor original del destino.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
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

*comparar \_ valor* \[ en\]
</dt> <dd>

Tipo: **T**

Valor de comparación.

</dd> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **T**

Valor de entrada.

</dd> <dt>

*valor \_ de salida* \[ original\]
</dt> <dd>

Tipo: **T**

El valor original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Compara de forma atómica el valor al que  hace referencia *dest* con el valor compare *, \_* almacena el valor en la ubicación a la que hace referencia *dest* si los valores coinciden, devuelve el valor original *de dest* en el valor *original. \_* Esta operación solo se puede realizar en recursos con tipo **int** **o uint** y variables de memoria compartida. Hay dos usos posibles para esta función. La primera es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza la operación en el registro de memoria compartida al que hace referencia *dest*. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza la operación en la ubicación de recursos a la que hace referencia *dest*. Esta operación solo está disponible cuando R es legible y grabable.

> [!Note]  
> Si llama [**a**](dx-graphics-hlsl-for.md) **InterlockedCompareExchange** [](dx-graphics-hlsl-while.md) en un bucle de sombreador for o while, para compilar correctamente, debe usar el atributo **\[ allow \_ uav \_ condition \]** en ese bucle.

 

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




