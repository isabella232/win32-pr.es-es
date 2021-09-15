---
title: Función Texture2DArray::GatherCmpBlue(S,float,float,int,uint)
description: Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente azul con un valor de comparación junto con el estado de asignación de mosaicos. | Función Texture2DArray::GatherCmpBlue(S,float,float,int,uint)
ms.assetid: 60456C17-F7A4-408A-93A2-DF695CBBEEAA
keywords:
- Función HLSL de GatherCmpBlue
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5bb2d292f63575d6a570296556dbc0622e6672b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465745"
---
# <a name="texture2darraygathercmpbluesfloatfloatintuint-function"></a>Función Texture2DArray::GatherCmpBlue(S,float,float,int,uint)

Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente azul con un valor de comparación junto con el estado de asignación de mosaicos.

## <a name="syntax"></a>Sintaxis


``` syntax
TemplateType GatherCmpBlue(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
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

*CompareValue* \[ En\]
</dt> <dd>

Tipo: **float**

Valor que se compara con cada valor muestreado.

</dd> <dt>

*Desplazamiento* \[ En\]
</dt> <dd>

Tipo: **int**

Desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación **Sample**, **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se tomaron valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **TemplateType**

Valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.

## <a name="remarks"></a>Observaciones

Los ejemplos de textura se pueden usar para la interpolación bilineal.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos de GatherCmpBlue](texture2darray-gathercmpblue.md)
</dt> </dl>

 

 
