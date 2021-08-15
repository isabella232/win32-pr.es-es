---
title: Función Texture2D::GatherRed(S,float,int)
description: Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente rojo con un valor de comparación. | Función Texture2D::GatherRed(S,float,int)
ms.assetid: 6d2d1556-d52f-4625-93ca-34da399f9a8b
keywords:
- Función GatherRed HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 879ba1cdad400a065fae46bd858db5569390ae0ae2a2ad338bfb9faed62bbdca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508644"
---
# <a name="texture2dgatherredsfloatint-function"></a>Función Texture2D::GatherRed(S,float,int)

Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente rojo con un valor de comparación.

## <a name="syntax"></a>Sintaxis

``` syntax
TemplateType GatherRed(
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



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos gatherRed](texture2d-gatherred.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




