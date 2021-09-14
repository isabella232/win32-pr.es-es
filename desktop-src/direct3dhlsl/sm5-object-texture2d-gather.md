---
title: Función Texture2D::Gather(S,float,int)
description: Devuelve los cuatro valores de texel que se usarían en una operación de filtrado bi lineal. | Función Texture2D::Gather(S,float,int)
ms.assetid: 5d196c1c-8cc9-4add-9d33-654294314ee2
keywords:
- Función Gather HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126884084"
---
# <a name="texture2dgathersfloatint-function"></a>Función Texture2D::Gather(S,float,int)

Devuelve los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.

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

Desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **TemplateType**

Valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.

## <a name="remarks"></a>Observaciones

Las muestras de textura se pueden usar para la interpolación bilineal.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Recopilación de métodos](texture2d-gather.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




