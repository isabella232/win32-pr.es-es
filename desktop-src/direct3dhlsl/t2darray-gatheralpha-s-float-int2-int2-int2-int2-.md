---
title: Función Texture2DArray::GatherAlpha(S,float,int2,int2,int2,int2)
description: Devuelve los componentes alfa de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal. | Función Texture2DArray::GatherAlpha(S,float,int2,int2,int2,int2)
ms.assetid: A7F96B45-A097-437B-A0D0-18555FF76544
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
ms.openlocfilehash: ff6910152c9ac133c819456b9ec7aaeb2406b791
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970479"
---
# <a name="texture2darraygatheralphasfloatint2int2int2int2-function"></a>Función Texture2DArray::GatherAlpha(S,float,int2,int2,int2,int2)

Devuelve los componentes alfa de los cuatro valores de texel que se usarían en una operación de filtrado bi lineal.

## <a name="syntax"></a>Sintaxis


``` syntax
TemplateType GatherAlpha(
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

## <a name="remarks"></a>Observaciones

Las muestras de textura se pueden usar para la interpolación bilineal.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos GatherAlpha](texture2darray-gatheralpha.md)
</dt> </dl>

 

 




