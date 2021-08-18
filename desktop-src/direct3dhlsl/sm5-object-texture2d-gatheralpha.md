---
title: Función Texture2D::GatherAlpha(S,float,int)
description: Devuelve los componentes alfa de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal. | Función Texture2D::GatherAlpha(S,float,int)
ms.assetid: 4c980e06-d768-479e-bee3-1b2541c23038
keywords:
- Función GatherAlpha HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12ea7c643c8e86925163594856980c20aae09d61cd9421d6060449ed80da81f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789830"
---
# <a name="texture2dgatheralphasfloatint-function"></a>Función Texture2D::GatherAlpha(S,float,int)

Devuelve los componentes alfa de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.

## <a name="syntax"></a>Sintaxis

``` syntax
TemplateType GatherAlpha(
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

*offset* \[ En\]
</dt> <dd>

Tipo: **int2**

Desplazamiento que se aplica a la coordenada de textura antes del muestreo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **TemplateType**

Valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.

## <a name="remarks"></a>Comentarios

Los ejemplos de textura se pueden usar para la interpolación bilineal.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos GatherAlpha](texture2d-gatheralpha.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




