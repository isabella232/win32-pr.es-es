---
title: Función Texture2D::GatherCmp(S,float,float,int,uint)
description: Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve su comparación con un valor de comparación junto con el estado de asignación de mosaicos. | Función Texture2D::GatherCmp(S,float,float,int,uint)
ms.assetid: A6610587-97C3-4CE5-86A7-3411D422BC8F
keywords:
- Función GatherCmp HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be8246053e0f7ba6357bdd68dc59059fd225bbc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974649"
---
# <a name="texture2dgathercmpsfloatfloatintuint-function"></a>Función Texture2D::GatherCmp(S,float,float,int,uint)

Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve su comparación con un valor de comparación junto con el estado de asignación de mosaicos.

## <a name="syntax"></a>Sintaxis


``` syntax
TemplateType GatherCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset,
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

Tipo: **int2**

Desplazamiento en los elementos de textura aplicados a las coordenadas de textura antes del muestreo. Debe ser un valor literal.

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación Sample **,** **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se tomaron valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

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

[Métodos gatherCmp](texture2d-gathercmp.md)
</dt> </dl>

 

 
