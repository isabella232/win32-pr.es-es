---
title: 'Texture2D:: Gather (S, Float, int) (función)'
description: 'Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal. | Texture2D:: Gather (S, Float, int) (función)'
ms.assetid: 5d196c1c-8cc9-4add-9d33-654294314ee2
keywords:
- Recopilación de la función HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d0a58be0580572441f91a3b3f637601d70cd9c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820703"
---
# <a name="texture2dgathersfloatint-function"></a>Texture2D:: Gather (S, Float, int) (función)

Devuelve los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal.

## <a name="syntax"></a>Sintaxis

``` syntax
TemplateType Gather(
  in sampler s,
  in float2 location,
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

Tipo: **float2**

Coordenadas de ejemplo (u, v).

</dd> <dt>

*desplazamiento* \[ de\]
</dt> <dd>

Tipo: **INT2**

Desplazamiento aplicado a las coordenadas de textura antes del muestreo.

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

[Recopilar métodos](texture2d-gather.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




