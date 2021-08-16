---
title: Función Texture2D::GatherGreen(S,float,int2,int2,int2,int2)
description: Devuelve los componentes verdes de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal. | Función Texture2D::GatherGreen(S,float,int2,int2,int2,int2)
ms.assetid: 043434C0-BB12-4A08-A3E5-34C9738DEBDB
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
ms.openlocfilehash: 6d0c7fa8f28a0a0ddc276af696b102df29de1362b948a4a909733cf14df35aa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043593"
---
# <a name="texture2dgathergreensfloatint2int2int2int2-function"></a>Función Texture2D::GatherGreen(S,float,int2,int2,int2,int2)

Devuelve los componentes verdes de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.

## <a name="syntax"></a>Sintaxis


``` syntax
TemplateType GatherGreen(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*S* \[ en\]
</dt> <dd>

Tipo: **SamplerState**

Índice de sampler de base cero.

</dd> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Tipo: **float**

Coordenadas de ejemplo (u,v).

</dd> <dt>

*Offset1* \[ En\]
</dt> <dd>

Tipo: **int2**

Primer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Offset2* \[ En\]
</dt> <dd>

Tipo: **int2**

Segundo componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Offset3* \[ En\]
</dt> <dd>

Tipo: **int2**

Tercer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Offset4* \[ En\]
</dt> <dd>

Tipo: **int2**

Cuarto componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

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

[Métodos gatherGreen](texture2d-gathergreen.md)
</dt> </dl>

 

 




