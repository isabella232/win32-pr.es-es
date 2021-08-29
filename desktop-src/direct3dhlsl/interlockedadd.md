---
title: Función InterlockedAdd (referencia HLSL)
description: Realiza una adición atómica garantizada de valor a la variable de recurso dest.
ms.assetid: b3b9cf5c-0da0-4c72-a83f-a0d96f1cac32
keywords:
- Función HLSL InterlockedAdd
topic_type:
- apiref
api_name:
- InterlockedAdd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3084e5a064688fd031bfe4073f674d10f119de13811299bd10684e7a10c7a36d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982095"
---
# <a name="interlockedadd-function-hlsl-reference"></a>Función InterlockedAdd (referencia HLSL)

Realiza una adición atómica garantizada de valor a la variable de recurso dest.

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedAdd(
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

*valor \_ original de* \[ salida\]
</dt> <dd>

Tipo: **T**

Opcional. Valor de entrada original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta operación solo se puede realizar en recursos con tipo int o uint y variables de memoria compartida. Hay dos usos posibles para esta función. La primera es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza una adición atómica de valor al registro de memoria compartida al que hace referencia dest. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza una adición atómica de valor a la ubicación de recursos a la que hace referencia dest. La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest. Esta operación sobrecargada solo está disponible cuando R es legible y grabable.

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

 

 




