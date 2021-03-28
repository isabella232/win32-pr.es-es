---
title: 'Texture2DArray:: GatherRed (S, Float, int) (función)'
description: 'Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | Texture2DArray:: GatherRed (S, Float, int) (función)'
ms.assetid: cb9c21ef-87f4-4c32-b41a-9fc7478713a6
keywords:
- GatherRed de función HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 431d08b77d13540bb48621a6d5ec76f4c775f796
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998141"
---
# <a name="texture2darraygatherredsfloatint-function"></a>Texture2DArray:: GatherRed (S, Float, int) (función)

Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.

## <a name="syntax"></a>Sintaxis

``` syntax
TemplateType GatherRed(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*s* \[ en\]
</dt> <dd>

Tipo: **muestra**

Índice de muestra de base cero.

</dd> <dt>

*Ubicación* \[ de de\]
</dt> <dd>

Tipo: **float3**

Coordenadas de ejemplo (u, v).

</dd> <dt>

*desplazamiento* \[ de\]
</dt> <dd>

Tipo: **INT2**

Desplazamiento que se aplica a la coordenada de textura antes del muestreo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **TemplateType**

Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.

## <a name="remarks"></a>Observaciones

Los ejemplos de textura se pueden usar para la interpolación bilineal.

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos GatherRed](texture2darray-gatherred.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




