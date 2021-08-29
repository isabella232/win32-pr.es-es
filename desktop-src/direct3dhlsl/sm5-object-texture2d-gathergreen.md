---
title: Función Texture2D::GatherGreen(S,float,int)
description: Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente verde con un valor de comparación. | Función Texture2D::GatherGreen(S,float,int)
ms.assetid: 97e1fb52-75f4-4e73-93f1-98b7a5925efc
keywords:
- Función GatherGreen HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bbdcae4e708957bbcd10a6ab365e68b31e959e50695b50a1a7a0a08f3859b152
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671305"
---
# <a name="texture2dgathergreensfloatint-function"></a>Función Texture2D::GatherGreen(S,float,int)

Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente verde con un valor de comparación.

## <a name="syntax"></a>Sintaxis

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*s* \[ en\]
</dt> <dd>

Tipo: **sampler**

Índice de sampler de base cero.

</dd> <dt>

*ubicación* \[ En\]
</dt> <dd>

Tipo: **float2**

Coordenadas de ejemplo (u,v).

</dd> <dt>

*desplazamiento* \[ En\]
</dt> <dd>

Tipo: **int2**

Desplazamiento que se aplica a la coordenada de textura antes del muestreo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **TemplateType**

Valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.

## <a name="remarks"></a>Comentarios

Las muestras de textura se pueden usar para la interpolación bilineal.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos gatherGreen](texture2d-gathergreen.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




